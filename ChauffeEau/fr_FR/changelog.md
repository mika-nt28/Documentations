---
layout: default
title: Gestion du Chauffe-Eau (ChauffeEau)
lang: fr_FR
pluginId: ChauffeEau
---

# Stable
## 27/01/2024
* BugFix : Non rallumage du chauffe-eau après délestage et heure de dispo dépassé
  
## 23/01/2023
* BugFix creation de cron douche (Arret et redemarrage complet du demon a la sauvegarde


## 19/07/2021
* BugFix non démarrage du chauffe-eau lorsqu'une condition n'est pas active
* BugFix Simulation de température Forcage de la date de valeur meme si pas de changement de valeur
* Forcage du nettoyage des cron

## 01/07/2021
* Simulation de température: Ajout des conditions au paramettrage
* Simulation de température: Ajout de parametrage des douches bain
* Autorisation de la mise a jours de la date de départ (Date de fin - Temps de chauffe) tans que le cycle n'est pas commancée

## 17/02/2021
* BugFix Selection de commande

## 12/02/2021
* Evalution du temps additionnel

## 25/06/2020
* Interdiction de la repetition si on est a moins de 60 seconde de la repetition

## 26/04/2020
* Bugfix $_nextTime  non initialisé

## 08/04/2020
* Désactivation du la gestion de défaillance des sondes
* Conditionnement a la simulation de température de la chute de température quotidienne (douche, bain)

## 03/04/2020
* Séparation du plugin et sa documentation

## 07/01/2020
* Ajout de la température extérieure pour la simulation de température
* Mise à jour de la cartographie de perte du chauffe-eau

## 27/11/2019
Ajout d'un déclencheur pour le changement de mode.
Ce déclencheur est très utile pour la notification par exemple.

# Beta
## 01/02/2023
* BugFix Arret de la chauffe a la consigne ou 30 min apres (En test)
## 26/01/2023
* Modification de l'etat du demon lorsque l'on a pas d'etat chauffe-eau ou Temperature eau
