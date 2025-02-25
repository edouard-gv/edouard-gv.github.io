---
layout: post
title:  "Construire pour AWS sa couche python comportant des bibliothèques natives"
date:   2021-11-25 18:19:52 +0100
categories: jekyll update
---

## TL; DR;

Ce billet peut intéresser qui a besoin d'ajouter dans une lambda AWS des lib python native, c'est à dire qui doivent être compilées sur l'environnement cible. Comme numpy par exemple, ou en ce qui me concernait ici, pycurl. Pour faire court, vous pouvez aller sur le poste StackOverFlow associé : [https://stackoverflow.com/questions/67729764/errors-when-trying-to-call-pycurl-in-a-lambda-on-aws](https://stackoverflow.com/questions/67729764/errors-when-trying-to-call-pycurl-in-a-lambda-on-aws)

Mais j'ai trouvé que le chemin était aussi intéressant que l'arrivée (même si ça fait toujours plaisir de faire son premier sommet à 4000 mètres - ce qui a été un peu mon impression un fois arrivé ). C'est ce chemin que je vous propose de partager ici.

## Les motivations du voyage


Je trouve le blog d'Arolla long à charger, de même que les deux sites perso d'une amie et le mien. J'aimerais rendre ça objectif en mettant une petite sonde, car je n'ai pas accès à google analytics. Je demande à Netvigie, c'est une dizaine d'euros par mois par URL. Je me dis qu'une lambda AWS pourrait faire la mesure, puis pousser ça dans un Elasticsearch, surtout qu'AWS propose un service Elasticsearch tout fait.

## Jour 1, matin : arrivée sans encombre au camp de base local


![carte jour 1](/media/Layer-AWS-carte-j1.png)

En une heure, j'ai ma stack OpenSearch (ex « ELK ») déployée dans AWS, par la console, en mode light vraiment pas sécurisé, grâce au tuto officiel : [https://docs.aws.amazon.com/opensearch-service/latest/developerguide/gsgcreate-domain.html](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/gsgcreate-domain.html)

Deux heures plus tard, j'ai un bout de code en local qui tourne dans mon PyCharm, qui me permet de voir mes premières données dans Kibana [(1)](#note1).  
[https://github.com/edouard-gv/web-monitor/blob/f22f17058ced0ec69cef8cd5c9c1b774b640d760/monitor.py](https://github.com/edouard-gv/web-monitor/blob/f22f17058ced0ec69cef8cd5c9c1b774b640d760/monitor.py)

![mesures](/media/Layer-AWS-Premières-mesures-manuelles.png)

Avec les requirements suivant :

*   pycurl~=7.43.0.5
*   certifi~=2020.12.5
*   requests~=2.25.1

Pourquoi PyCurl ? Car c'était, d'après moi, la seule librairie qui permette de mesurer les différents temps réseau finement, notamment le temps de résolution DNS.

Bref, ça marche sur mon environnement local : j'étais arrivé sans encombre au camp de base. Mais, comme parfois, c'est le passage dans l'environnement de prod qui va se révéler le plus long. Surtout si celui-ci est dans le cloud.

Ce n'est en effet que deux jours plus tard que j'arriverai à faire fonctionner ce code dans une lambda.

### Quand il ne suffit pas de copier le code en prod

Le souci vient que mon code référence trois librairies, dont une native, `pycurl`. Voilà donc ce que j'avais comme erreur en lançant le code dans une lambda :

    Unable to import module 'lambda\_function': No module named 'pycurl';

Pour celles ou ceux qui me proposent d'utiliser une autre lib que `pycurl`, comme `libcurl2`, j'ai deux réponses : la première, comme je le disais en introduction, c'est que `libcurl2` ne me donnent pas les temps de résolution de DNS, temps du premier octet, temps du dernier octet, cf [https://stackoverflow.com/questions/744532/getting-ttfb-time-till-first-byte-for-an-http-request](https://stackoverflow.com/questions/744532/getting-ttfb-time-till-first-byte-for-an-http-request). La seconde, Boulet l'illustre mieux que moi 😉 : [http://www.bouletcorp.com/2021/03/05/conseils-depannage/](http://www.bouletcorp.com/2021/03/05/conseils-depannage/).

### Après-midi : perdu dans la forêt des services AWS

Première étape : comprendre que j'ai besoin de construire une couche lambda (lambda layer), c'est-à-dire un endroit où mettre les lib python dont dépend mon code. J'avais vu ça sur un autre projet, où les lib étaient comitées dans le code dans des sous-repertoires layer/…, qui était déployés par la chaine CI/CD que je n'avais pas regardée de près sur cette partie-là. De toutes façons, on ne les utilisait pas en local car c'étaient « les versions pour la prod », et ça avait été mis par les architectes AWS, ils savaient ce qu'ils faisaient (aujourd'hui je ferai autrement).

En tous cas, je comprends qu'il va falloir construire cette couche lambda, contenant les lib python. Je chausse mes crampons stackoverflow et je quitte le camp de base.

Là, j'ai dû défragmenter cette partie du cerveau où commençaient à s'empiler mes expériences AWS. Je me souvenais avoir utilisé des pipelines qui utilisaient des images pour compiler. Et puis y a CodeDeploy, CloudFormation. J'ai cherché un peu par-là, en me demandant s'il fallait que je crée une pipeline pour construire mon image à déployer, mélangeant avec ce qu'on doit faire quand on déploie une lambda en java.

Je me suis bien perdu, et j'ai donc dû revenir au camp de base, la nuit tombait.

## Jour 2 : sur le bon chemin du col, on croise un drôle d'oiseau DLL

![carte jour 2](/media/Layer-AWS-carte-j2.png)

Après une nuit de sommeil, les idées plus au clair et donc mes recherches google mieux dirigées, je suis tombé sur un tuto du support aws [https://aws.amazon.com/fr/premiumsupport/knowledge-center/lambda-layer-simulated-docker/](https://aws.amazon.com/fr/premiumsupport/knowledge-center/lambda-layer-simulated-docker/)

L'idée est simplement de zipper les librairies organisées suivant la bonne hiérarchie. Développant sur une Surface Go, sans docker, sous windows, j'ai commencé à essayer de copier et zipper les librairies que PyCharm avaient ajouté dans mon venv, mais je ne suis pas allé au bout, il y a trop de choses. Et ça commençait à sentir pas très bon : je vois une DLL pour pycurl dans mes lib python pycharm. Je me dis bien que ça ne va pas tourner sur les env linux d'AWS lambda... L'orage grondait...

C'est bien pour ça que le tuto propose de passer par une image docker pour générer les dépendances. Du coup je change de PC (un vieux portable linux), et je suis le tuto pas à pas (sauf quand le tuto propose d'uploader le zip via le CLI : si comme moi vous ne voulez pas utiliser le CLI, on peut trouver dans la console où uploader les zip).

### Jour 2, midi : le ciel s'obscurcit , pycurl a besoin de dépendances natives

Le tuto ne fonctionne pas : la construction via `pip` de la librairy `pycurl` demande des dépendances qui ne sont pas sur l'image docker fournie pourtant par AWS. Dans le fatras des messages d'erreur, la ligne qui m'intéresse est celle-ci :

    Could not run curl-config: \[Errno 2\] No such file or directory: 'curl-config': 'curl-config';

Je teste quand même le process complet mais sur le code dont j'ai commenté les dépendance `pycurl`, avec un `requirements.txt` qui ne contient donc que `certifi` et `requests` : construction de la layer dans un répertoire vide, zip et upload, et j'ai ma première victoire, le ciel s'éclaircit, j'ai l'impression d'être arrivé au pied du bon col. J'y planterai ma tente.

Dans le détail, ça consiste à :

1.  mettre `requirements.txt` dans un répertoire vide
1.  lancer `docker run -v "$PWD":/var/task "public.ecr.aws/sam/build-python3.6" /bin/sh -c "pip install -r requirements.txt -t python/lib/python3.6/site-packages/; exit"`
1.  zipper le repertoire généré `zip -r mypythonlibs.zip python > /dev/null`
1.  uploader ce zip comme une couche lambda dans la console, et toujours dans la console référencer cette couche dans la configuration de la lambda
1.  Bonus : supprimer (en sudo) le répertoire généré, pour ne pas oublier de le faire à l'itération suivante

Je me dis que je pourrais quand même tenter un raccourci : je fais l'hypothèse que les librairies linux devraient quand même se ressembler, et tente de générer la couche via mon ubuntu, sans passer par l'image docker, ce qui revient à simplement lancer dans un répertoire ne contenant que `requirements.txt` la commande `pip install -r requirements.txt -t python/lib/python3.6/site-packages/` (en lieu du 2. de la séquence précédente).

Mais mon ubuntu n'est pas AWS compatible, j'ai l'erreur suivante quand je lance la lambda :

    Unable to import module 'lambda\_function': libssl.so.1.0.0: cannot open shared object file: No such file or directory

Je retourne me coucher dans ma tente...

## Jour 3 : construire sa propre image docker pour générer la couche lambda


![carte jour 3](/media/Layer-AWS-carte-j3.png)

En surfant un peu, je commence à sentir qu'il va bien falloir que je me débatte avec une image docker ad-hoc. Je crois que ce qui m'a mis sur le chemin est cet article-là : [https://github.com/awslabs/serverless-image-handler/issues/44](https://github.com/awslabs/serverless-image-handler/issues/44), ça n'avait rien à voir, mais il était sorti en tapant pycurl aws dans google.

Là, il a fallu que je défragmente mes souvenirs docker, ça faisait plus d'un an que je n'avais pas construit une image docker. Mais c'est comme le vélo. Je suis arrivé assez vite à construire une image à partir de ce dockerfile :

    FROM public.ecr.aws/sam/build-python3.6
    
    RUN yum install libcurl-devel python36-devel -y
    
    RUN yum install nss-devel -y
    ENV PYCURL\_SSL\_LIBRARY=nss

Sans oublier les -y après les yum.

Donc, pour construire ma couche, au lieu d'utiliser l'image d'aws classique, je devais utiliser la mienne :

*   En la construisant via `docker build -t build-python3.6-with-pycurl`
*   Puis en l'utilisant à l'étape 2 : `docker run -v "$PWD":/var/task "public.ecr.aws/sam/build-python3.6-with-pycurl" /bin/sh -c "pip install -r requirements.txt -t python/lib/python3.6/site-packages/; exit"` (noter le nom de mon image `build-python3.6-with-pycurl` au lieu de `build-python3.6`)

J'ai dû faire quelques itérations, ajouter les dépendances les unes après les autres, comme chaque fois une petite montée à gravir. Jusqu'à arriver devant une montée un peu plus abrupte que les autres : je tombai sur cette insulte de gcc (alors qu'on ne s'était pas parlé depuis quinze ans au moins !)
    
    src/pycurl.h:5:10: fatal error: Python.h: No such file or directory
         #include <Python.h>
                  ^~~~~~~~~~
        compilation terminated.
        error: command 'gcc' failed with exit status 1
    
J'ai cru être à nouveau dans une impasse, mais c'était juste qu'il y avait un dernier petit raidillon avant le col ouvrant sur le chemin large menant au sommet...

### Le raidillon du lien symbolique

Pour une raison que j'ignore, la distribution linux d'AWS ne met pas ses header C là où d'autres l'imagineraient. C'est en fouinant toujours sur StackOverFlow, que je voyais que les réponses à ce genre de question étaient : « sais-tu où est Python.h » ? Facile sur son poste, mais sur une image Docker qu'on lance en exec... Obligé de me rappeler comment me loguer en ssh sur une image docker, retrouver la syntaxe de find, greper tout ça, me rendre compte que c'est dans `/var/lang/include`, décrypter la commande `gcc` et les `-I` pour me rendre compte que gcc s'attend d'avoir ses header file dans `/usr/include`.  
Et tant que j'étais en ssh sur mon image, j'ai pu y faire directement mes itérations (c'est à dire lancer le `pip install` dans mon image), pour me rendre compte qu'il suffisait juste de faire le bon lien symbolique, que j'ai ensuite recopié dans mon dockerfile, qui est devenu :

    FROM public.ecr.aws/sam/build-python3.6
    
    RUN yum install libcurl-devel python36-devel -y
    
    RUN yum install nss-devel -y
    ENV PYCURL\_SSL\_LIBRARY=nss
    
    RUN ln -s /usr/include /var/lang/include

Je suis confiant, le col est en vue, plus qu'à lancer la construction via cette nouvelle image docker.

### Le ruisseau du backend ssl

Effectivement, gcc ne dit plus rien, ma nouvelle couche est là, plus qu'à la zipper, l'uploader, la faire référencer par ma lambda. Forcément, je me prends les pieds dans un dernier ruisseau, à force de copier bêtement de stackoverflow, je n'avais pas le bon backend ssl à l'exécution dans AWS :

    pycurl: libcurl link-time ssl backend (openssl) is different from compile-time ssl backend (nss)

Mais le gué pour franchir le ruisseau n'est pas loin, une petite modification dans le docker file :

    FROM public.ecr.aws/sam/build-python3.6
    
    RUN yum install libcurl-devel python36-devel -y
    
    RUN yum install openssl-devel -y
    ENV PYCURL\_SSL\_LIBRARY=openssl
    
    RUN ln -s /usr/include /var/lang/include

### L’arrivée au sommet !

On relance tout (image, layer, zip, upload), comme un dernier petit sprint, et c'est l'arrivée au sommet, sous le soleil !

J'ai pu profiter de la vue en mangeant mon sandwich, et j'imaginais le programme pour le prochain week-end de rando : pouvoir déployer ma lambda en automatique (CI/CD).

## D’autres chemins


Depuis, j'ai découvert que j'aurais pu passer par d'autres chemins, notamment en suivant celles et ceux qui ont cherché à installer numpy / panda, et qui sont beaucoup plus nombreux. J'ai ainsi entendu parler des sentiers suivants :

*   **Pour ne pas recompiler**. Le sentier des wheels (merci Dimitri) : si votre bibliothèque est publiée sous forme de wheel, vous pouvez dézipper celle correspondant à \*manylinux1\_x86\_64.whl pour construire votre layer à la main. Exemple : [https://korniichuk.medium.com/lambda-with-pandas-fd81aa2ff25e](https://korniichuk.medium.com/lambda-with-pandas-fd81aa2ff25e)
*   **Pour recompiler, mais sans Docker**. Le sentier d'EC2 sur Amazon Linux, encore mieux balisé via l'IDE cloud d'AWS, Cloud9 : [https://towardsdatascience.com/python-packages-in-aws-lambda-made-easy-8fbc78520e30](https://towardsdatascience.com/python-packages-in-aws-lambda-made-easy-8fbc78520e30)
*   **Pour ne pas faire le lien symbolique**. Le sentier gcc, en résinstallant gcc, g++ etc. dans l'image docker : [https://github.com/chedabob/LambdaZipper/blob/master/Dockerfile](https://github.com/chedabob/LambdaZipper/blob/master/Dockerfile)

## Tout ça pour ça

Ce que je ne savais pas, c'est que l'ECS Elastic-stack finalement me coûtera plus cher qu'un abonnement Netvigie (30€ par mois), et qu'on ne peut pas l'éteindre sans le supprimer. Un mois plus tard, je le supprimerai donc, sans avoir même réussi à sauvegarder les données que j'y avais indexées, n'ayant pas réussi à créer un snapshot de l'index [(2)](#note2).  
Ce n'est donc pas demain que je monterai un concurrent de NetVigie :).

![carte générale](/media/Layer-AWS-carte.png)

* * *

[(1)](#ref1): En vrai j'ai changé de modèle de donnée depuis : avant, je poussais un objet par ping et par URL, avec les quatre mesures dans quatre attributs de cet objet  maintenant je pousse quatre objets, un par mesure, avec le nom de la mesure dans un attribut. Bonne pratique data, plus facile à gérer dans Kibana.

[(2)](#ref2): Si vous voulez savoir comment créer des snapshot d'index ES : [https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-managedomains-snapshots.html#es-managedomains-snapshot-prerequisites](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-managedomains-snapshots.html#es-managedomains-snapshot-prerequisites). Comme d'habitude, c'est la gestion de la sécurité qui pose le plus de soucis. Je me suis arrêté au message "Credential should be scoped to correct service: 'es'. " alors qu'il m'avait bien pourtant semblé avoir modifié les relations d'approbation de manière à y associer le fournisseur d'identité es.amazonaws.com.
