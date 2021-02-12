---
layout: default
title: Volet proportionel (voletProp)
lang: fr_FR
pluginId: voletProp
---

# Stable
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
## 12/02/2021
* Suppression du temps d'attente et du STOP dans une synchro 0 ou  100%

## 02/02/2021
* Bugfix Charge CPU a cause du demon

## 22/01/2021
* Attente en proportionnel gérer par le demon => Stop possible a tout moment

## 08/01/2021
* Suppression du parametre d'utilisation de l'etat du plugin (automatique si on a pas de retour d'etat)
