---
layout: default
title: Volet proportionel (voletProp)
lang: fr_FR
pluginId: voletProp
---

# Stable
## 15/04/2021
* Ajout d'un test du parmetre de mouvement avant un monté ou une descente manuel pour executer un stop et mettre a jours la position
* Suppression du temps d'attente et du STOP dans une synchro 0 ou  100%
* Attente en proportionnel gérer par le demon => Stop possible a tout moment
* Suppression du parametre d'utilisation de l'etat du plugin (automatique si on a pas de retour d'etat)

## 06/01/2021
* Bugfix sens de mouvement apres la synchronisation
* Bugfix pas des synchronisation si on est deja a 0 ou 100
* Nettoyage du code et utilisation des commandes de mouvement du plugin dans la logique plutot que directement les commandes configuré

## 02/12/2020
* Simplification de la synchronisation

## 10/11/2020
* Bugfix lever du flag mouvement lors d'un detection de fin de course
* Interdiction lancement du demon si le temps de montée ou descente est a 0
* Valeur par defaut a 0 du temps de montée ou descente si non defini

## 25/06/2020
* Ajout du temps de descente

## 04/05/2020
* Suppression initialisation des synchro
* Suppression de la configuration d'état  sur action manuel (inutile)
* Suppression des End dans le test de retour d'état

## 03/04/2020
* Séparation du plugin et sa documentation

# Beta
