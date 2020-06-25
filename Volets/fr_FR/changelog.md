---
layout: default
title: Gestion de Volets (Volets)
lang: fr_FR
pluginId: Volets
---

# Stable
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
## 25/06/2020
* Inverstion du ratio pour qu'il soit un pourcentage d'ouverture
* Bugfix Jour / Nuit par planning

## 24/06/2020
* Correction du calcul, la hauteur calculé est la hauteur entre le sous toit et le soleil sur le mur alors que precedement utilisé du sol au soleil sur le mur
* Mise  a jours du ratioVertical par rapport au nouveau calcul de hauteur

## 23/06/2020
* Reapplication du calcul initial pour retrouver un comportement initial
* Mise en log du nouveau cacul avec suppression des arrondies superflux apportant toujours un calcule erroné.

## 08/06/2020
* Creation d'un nouveau calcul du ratioVertical
