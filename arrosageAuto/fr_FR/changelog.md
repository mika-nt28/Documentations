---
layout: default
title: Arrosage automatique (arrosageAuto)
lang: fr_FR
pluginId: arrosageAuto
---
# Stable
## 15/09/2022 - Refontes du plugin général (configuration a reprendre si besoin)
* Coeficient forcé a 100% lors de la sauvegarde
* Correction des unité d'affichage
* Ajout de parametre manquant au model Tuyere, Turbine et Oscillant - Temps et distance
* Bugfix calcul de pluviometrie Tuyere pour prise en compte de la surface couverte
* Bugfix calcul de pluviometrie Turbine et Oscillant pour prise en compte de la surface couverte et du temps de mouvement
* Refonte de la configuration des arroseur
* Mise à jour du panel avec configuration des plantation des arroseurs par branche  
* Coeficient appliqué sur la pluviometrie
* Ajout de la commande info pluviometrie
* Ajout de la commande temps apres correction du coeficient
* Refonte de la gestion des plantations

## 12/04/2021
* Bugfix reprogrammation

## 08/03/2021
* Suppression de la baisse de pression en fonction de l'angle d'ouverture

## 29/11/2020
* Ajout de log sur le bilan debit et pression
* Bugfix sur le temps de declage (temps maximal des branches précédente)
* Bugfix sur l'initalisation des valeurs dans le decalage pour les branches suivantes
* Bugfix interdiction du decalage si le temps est a 0
* Bugfix arrosage lorsque trop de pluie la veille

## 04/11/2020
* Correction temps d'arrosage negatif
* Recherche de la prochaine programmation lorsque le programmation est passé
* Ajout de l'unité sur la configuration du temps entre 2 branches

## 03/08/2020
* Bugfix Programation INF

## 03/04/2020
* Séparation du plugin et sa documentation

## 07/03/2020
* Correction vérification météo

## 06/03/2020
* Ajout de la vérification de la météo avant le démarrage de l'arrosage

## 03/03/2020
* Passage de l'arrosage a la seconde.
* BugFix reprogrammation lorsque la condition est fausse.

## 15/02/2020
* Correction du défaut a la création des commandes avec le version 4.xxx

# Beta
## 04/01/2023
* Ajout des label et des aides sur les paramètres arroseurs
* Mise a jours de l'initialisation des arroseur
* Ajout d'une recherche  differetnt de l'equipement par défaut sur le pannel
