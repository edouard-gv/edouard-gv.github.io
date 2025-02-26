---
layout: post
title:  "EntityManagerService, canal historique"
date:   2025-02-21 11:00:00 +0100
categories: craft
---

— « Bon, où c'est qu'on met le calcul de la remise ? »

Silence. Puis, comme souvent, la pièce se divise en factions.

L'école de la Commande ouvre le bal.

— « C'est évident : la remise est une propriété de la commande. C'est le seul endroit où on a une vision complète du montant total et des produits. Pas de commande sans prix, donc pas de remise sans commande. »

— « Attends… », rétorque l'adepte du Panier. « Tu oublies que la commande, c'est l'aboutissement du processus. En amont, c'est le panier qui existe. Si on veut donner un feedback à l'utilisateur avant la validation, c'est lui qui doit calculer la remise. »

— « Ok, mais ton panier est un simple conteneur ! Il n'a pas de montant encore, juste une structure. Si tu le fais parler avec un repository pour récupérer les règles de prix, il devient une sorte de Frankenstein… Et on va donner un accès à la base de données à un Value Object ? Sérieusement ? »

— « Pourquoi pas ? » Un partisan du Client prend la parole. « Après tout, la remise dépend du client. Ses achats passés, ses conditions spécifiques… C'est lui qui sait quelles règles de remise appliquer. »

— « Tu veux dire que le client va savoir tout le pricing ? Il va devoir connaître toutes les subtilités du calcul de commande ? On est en train de créer une énorme entité obèse ! »

Une tension monte. Et là, la voix du EntityManagerService, canal historique, s'élève.

— « Franchement, ce qu'on est en train de faire, c'est disperser du métier un peu partout. Il nous faut une brique dédiée. Un service. »

Soupirs. Murmures. Regards noirs des thuriféraires du DDD tactique.

— « Et voilà, encore un service qui vide nos objets de leur logique métier. À ce rythme, autant coder ça en script procédural… »

— « Boah, ce n'est pas parce qu'un service calcule quelque chose que tout le reste devient anémique. Il peut orchestrer des objets riches. L'important, c'est que la commande ne porte pas une logique trop large et que les invariants restent valides. »

— « Donc, un PricingService qui interroge le Client, le Panier et la Commande sans tout leur injecter ? »

— « Et on laisse les objets jouer leur rôle : le panier structure l'achat, la commande valide l'achat et le client influence le prix. Et le service fait parler tout ça sans casser les invariants. »

Silence.

Puis, hochements de tête. Certains visages grimacent encore, d'autres ont l'air plus convaincu. Peut-être convaincu qu'il faut juste avancer.

— « Bon… on le code ? »