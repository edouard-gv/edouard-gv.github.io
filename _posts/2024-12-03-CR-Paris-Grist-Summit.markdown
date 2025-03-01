---
layout: post
title:  "CR du Paris Grist Summit 2024"
date:   2024-12-03 21:23:00 +0100
categories: craft notes
---

Et c'est parti pour l'aprem du #GristParisSubmit avec notamment des membres du Grist Labs et une grosse communauté de la Direction interministérielle du numérique (DINUM) !

# Gérer le budget participatif de Marseille et de Malakoff avec l'aide de Grist

Après une petite discussion au déjeuner sur comment faire du TDD avec Grist (qui a dérapé sur comment avoir différents environnements par exemple test/prod, et quoi et comment déployer d'un environnement à l'autre), Bertille Mazari d'Open Source Politics nous présente comment le budget participatif de la Ville de Marseille est géré sous Grist :
- enrichissement intuitif, et facilité par des automatisations,
- gestion fine des permissions pour que les services ne voient que les projets qui les concernent 
- des widgets quand il fallait présenter des données agrégées venant éventuellement d'autres services
- liaisons dynamiques entre projets et propositions
- animation de la partie finale : export vers la plateforme de participation en ligne.

À venir : interconnexion avec les autres systèmes, mais aussi l'utilisation du widget carte.

Son collègue enchaîne avec l'exemple de Malakoff, insistant sur l'intérêt des droits fins permettant aux citoyens d'interagir directement avec l'outil.

Côté tech, il insiste sur l'intérêt de l'usage de la table d'attributs pour gérer facilement ces droits.

# Cours de Dmitry Sagalovskiy (himself :-) ) sur les formules dans Grist

Dmitry Sagalovskiy de Grist Labs enchaine sur un petit cours sur les formules dans Grist, en partant des bases - je n'insisterai pas sur ce qui ressemble aux tableurs classiques comme excel, sur les bases de python ni sur les bases de parcours des relations entre tables.

- Retourner la valeur None fait une cellule vide.
- L'usage d'IA pour générer les formules m'interpelle, comme tout usage de l'IA Gen pour générer du code (noté : elle n'a pas accès à vos données, juste à la structure).
- Générer du markdown pour les liens et une présentation sympathique
- Pour formater les dates, le faire en python permet de calculer des clés de regroupement (mois, trimestre....) (mais je préfère utiliser le formatage de colonne si c'est juste pour de l'affichage).
- $group permet d'accéder à l'objet d'agrégation dans les vues résumées, et on peut ensuite récupérer les données groupées dans la table elle-même ! Ou sinon, le calcul peut être fait directement en python avec la fonction lookup - voire être généré directement à partir du menu add column :).
- Ne pas oublier de order_by quand on look_up_one.
- La fonction PREVIOUS permet de récupérer le précédent élément dans le groupe par rapport à la ligne (par exemple, afficher la commande précédente du client de la commande en cours, ou calculer l'encours du client au moment de la commande de manière récursive en ajoutant le montant de la commande en cours à l'encours de la commande précédente).
- Pour les colonnes d'audit, elles se créent en un clic à partir du menu nouvelle colonne si l'on ne se souvient plus comment faire :) - et on peut aussi récupérer le $user pour savoir qui l'a fait. Les trigger formula permettent aussi de faire des snapshot values (capturer l'adresse d'expédition au moment de l'expédition et qu'elle ne bouge plus même si l'adresse du client évolue).

Et j'ai eu ma réponse, comment désactiver une colonne en fonction d'un état : en utilisant les droits fins sur les colonnes et conditionnant sur une combinaison de $rec. !

# Framework de TU (post conf)

J'ai essayé de mettre en oeuvre ces quelques apprentissage dans une espèce de démo de test-unitaire avec droits fins etc. visible ici : https://crafting.getgrist.com/3gqKavY43Xeo/Bonus-Kata