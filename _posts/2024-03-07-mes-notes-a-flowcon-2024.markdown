---
layout: post
title:  "notes Flowcon 2024"
date:   2024-03-07 15:22 +0100
categories: agilite notes
---

## Jour 2

Je n'étais pas là jour 1 :).

### Fathi Bellahcene - L'architecture n'appartient pas aux architectes ! @Veepee

Objectifs des architectes d'après Fathi Bellahcene de VPTech à @FlowConFR :
- Traiter ce qui est important (K. Beck)
- Prendre en compte que dans l'e-commerce, ce n'est pas les gros contre les petits mais les rapides contre les grands, et donc favoriser le TTM. 

Conséquence, il faut déléguer : déplacer le pouvoir de décision au niveau des sachants. En créant la confiance, en cherchant à ne pas tendre la relation (notamment en donnant les objectifs et non les moyens pour atteindre les objectifs). 

> Un architecte va donc s'assurer que les personnes qui doivent prendre les bonnes décisions techniques sont dans les bonnes conditions pour le faire, et non prendre ces décisions. 

(Une définition de servant-leader.)

Ce qui ne serait pas si compliqué si chaque équipe n'avait pas son contexte particulier avec ses contraintes et donc des besoins parfois opposés. Mélanger du vieux avec du neuf, comme faire du wardley-mapping dans une urbanisation à l'ancienne.

### João Rosa - Architecture intentionnelle

João Rosa a partagé comment accroître notre conscience des changements qui surviennent dans nos entreprises (par exemple, GDPR, crypto, nouveaux marchés...). 
- Expliciter la taille de vos composants et de l'impact temporelle (et de mettre cela sur un graphique). 
- Considérer que tous les systèmes sont ouverts, ce qui rend la pensée systémique vraiment difficile (le système change l'environnement, c'est ce qu'on appelle la stratégie). 
- Cartographier votre objectif à travers un arbre de fonctionnalités, et non un organigramme. 

Rappelez-vous que le graphique n'est pertinent que sur une courte période. Les données aident à décrire les objectifs commerciaux en objectifs logiciels. 

Et une dernière idée : vous ne pouvez pas forcer les gens à apprendre. On doit guider, pas imposer.

### Luca Minudel - Faut-il remplacer la responsabilité et l'engagement par une meilleure alternative ?

Luca Minudel a commencé par avertir que la responsabilité et l'engagement dépendent fortement du contexte et de l'histoire des personnes et des organisations. 

Déjà, commencez par parler de promesses et non d'engagements. Mais comment se faire confiance mutuellement, c'est-à-dire s'assurer que la prime directive est valide (ie que tout le monde faiot vraiment de son mieux) ? 

Vous avez de la chance si vous pouvez vous rapprocher de problèmes standardisés ou banalisés. Mais face à l'incertitude... l'estimation ne fonctionne pas. Face à l'incertitude, essayer d'améliorer le processus d'estimation ne fonctionne pas. La responsabilité et l'engagement mènent à la culpabilisation. Alors il faut
1) Trouver une alternative à la culpabilisation
2) Accepter la complexité
3) Gérer les risques par l'empirisme

> Passer de "Engagé" à "Fiable" \
> Passer de "Responsable" à "Digne de confiance"

Ce qui nécessite que vous vous mettiez d'accord sur les meilleures pratiques en matière de collaboration et de pratiques techniques, pour nous et pour le client, en les améliorant lorsque des plaintes ou même des incidents majeurs surviennent. Diviser les grandes promesses en petites promesses. Les co-créer avec le client, parier ensemble aide à gérer la complexité. Et... réduire la boucle de rétroaction.

### Roland Flemm et Alexey Krivitsky - Keynote : La valeur des topologies organisationnelles à l'ère des frameworks DIY

 Vive le bricolage ! Chaque nouvelle solution crée un nouveau problème. S'adapter ne signifie pas apprendre l'inconnu. On peut s'adapter à ce que l'on sait déjà faire. Le flux se voit facilement au niveau de l'équipe locale (une fois que vous l'avez vu... vous ne pouvez pas ignorer l'optimisation locale), donc le problème est de passer à l'échelle. Mais partager les connaissances ? Homogénéiser les méthodes ? Coordonner les backlogs et les livraisons au niveau d'une DSI entière ? Car "optimiser les parties d'un système garantit de ne pas optimiser le système". Ainsi, en contrepartie, pour optimiser le système, il faut accepter de sous-optimiser les parties. Les "équipes détachées de l'architecture" : une pratique à explorer, comme moyen de réduire la complexité de l'architecture (c'est le contraire de ce que je conseille par défaut). Ce que je comprends, c'est qu'il faut un effort de communication volontaire. B-level vs C-level : dans ce dernier, les personnes changent d'équipe et les équipes changent de département dès que l'objectif commercial est atteint.

 (J'aime quand la keynote est après le déjeuner et non le matin, comme pour la keynote d'aujourd'hui par Roland Flemm et Alexey Krivitsky à @FlowConFR. Et celle-ci était... assez énergique :).)

### Nigel Kersten - Le logiciel mange de la culture au petit-déjeuner

Nigel Kersten se décrit comme une personne post-devops, après avoir été l'un des premiers SRE chez Google*, avoir construit Puppet, écrit plus de 10 rapports Dora... cela pourrait être surprenant. Tout le monde parle de la culture DevOps, mais le terme culture n'est pas utile ici, il est applicable à tous les aspects de toute pratique professionnelle. Et trop large pour avoir un impact. 

Alors, réduire le terme au sens de Westrum pourrait être un début. Comme parler de sociotechnologie aussi. Et s'assurer que la technologie préexiste au DevOps (API, IaC, virtualisation...). DevOps n'est pas seulement une histoire de collaboration - au contraire, trop de collaboration est douloureuse (par rapport à l'automatisation), et le brainstorming en temps réel est difficile et contre-productif la plupart du temps. Par conséquent, réduire plutôt les interactions, y compris la transmission des contextes. Plus de collaboration ne résoudra pas le problème. 

A ce propose, les prochains progrès technique pourraient être autour des bus, rendant les conversations entre composants moins douloureuses.

* En fait non : je pensais que le rôle avait été inventer à ce moment, mais il existait depuis 2003. Disons qu'il était dans le premier décile :).

### Jean-Philippe Denis - Le système d'exploitation technique et produit de Qonto

Jean-Philippe Denis nous parle d'amélioration continue chez @getqonto. En vrac : le management visuel, c'est pour les équipes / chaque problème est loggé (bac rouge) dans une base de données unique / PDCA / Kaizen / A3 / les problèmes sont résolus par les personnes concernées / one piece flow / analyse de la valeur / méthodologie Shape Up / sources de vérité dynamiques (= présent et futur au même endroit) pour les écrans, flux d'écrans, variantes, API (dynamiques aussi) avec OpenAPI et diagrammes de séquence / pas de priorisation des bugs. Formation à la manière de voir et de logger un problème (PDCA avec un P comme punition). "Nous ne sommes pas parfaits mais presque parfaits dans la vision de nos imperfections." Bon, et je n'aime pas trop cette histoire de supermarché où chaque développeur dit quand il aura fini. Quid du pair-programming voire de l'ensemble-programming ?