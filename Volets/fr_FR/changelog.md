---
layout: default
title: Gestion de Volets (Volets)
lang: fr_FR
pluginId: Volets
---

# Stable
## 15/07/2024
* Ajout en local des librairies carte openLayers
* Mise a jours du calcul du ratioVertical par obrage (toujours fermé si l'ombre ne cache pas la fenetre)
* Mise a jours du calcul du ratioVertical par ensoleillement directe (Calcule toujours pour l'été)
* Ajout d'une sortie d'Azimuth (Jour/Nuit) si les conditions ne sont pas remplis
* Déplacement du calcul du ratioVertical sur la gestion Azimuth
* Refonte du calcul du ratioVertical 
- Gestion par ombrage, toujours fermé car l'ombrage par du bas
- Gestion ensoleilement directe, calcul de la proportion d'ouverture
* BugFix passage en gestion de nuit a la sortie d'un evenement / condition

## 31/05/2022
* Ajout en local des librairies carte openLayers

## 03/03/2022
* Mise a jours de la gestion Jour/Nuit
* Bugfix warning php

## 08/09/2021
* Bugfix Rechargement de la saison des evenements
* Bugfix Affichage des retour a la ligne dans les conditions multiples
* Bugfix Widget Soleil dans la fenetre (Remplacement par un widget core personalisé)

## 09/04/2021
* Bugfix gestion de saison dans la gestion Evenement

## 30/12/2020
* BugFix sortie de gestion evenementiel 
* BugFix inversion de sens du volet en gestion Azimut pra RatioVertical
* Fusion Gestion Conditionnel et Evenementiel (Les 2 sont toujours active, mais la gestion Evenementiel verifie ses condtions 
* Inverstion du ratio pour qu'il soit un pourcentage d'ouverture
* Bugfix Jour / Nuit par planning
* Creation d'un nouveau calcul du ratioVertical

## 25/06/2020
* Bugfix Jour / Nuit par planning

## 04/06/2020
* BugFix initialisation de la position acutel.

## 11/05/2020
* BugFix autorisation Évènementiel et conditionnel lorsqu'une gestion du même type est déjà active
* Ajout des commandes jour et nuit et suppression des variables en cache.

## 03/04/2020
* Séparation du plugin et sa documentation
* Ajout du support de configuration par Jeedom

# Beta
