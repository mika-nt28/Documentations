---
layout: default
title: SPA Balboa (balboa)
lang: fr_FR
pluginId: balboa
---
# Stable
## 22/12/2020
* Bugfix Suppression des conditions dans les modes

## 21/12/2020
* Bugfix Changement de mode sans conditions

## 01/12/2020
* Ajout de la personnalisation des actions dans les modes
* Bugfix mise a jours de le température uniquement lorsque la pompe de circulation est active

## 27/11/2020
* Interdiction de mise a jours les temperatures si la valeur reçus est a 255

## 19/09/2020
* Bugfix erreur serveur 

## 18/09/2020
* Correction bug emmission d'un ordre

## 14/09/2020
* Retour a une connexion direct sur le SPA (plantage de jeedom) 

## 19/08/2020
* suppression du cron daily de programmation de la filtration hebdo (plantage de jeedom) 

## 01/07/2020
* Bugfix mise a jours du filtrage quotidien
* Conditionnement de la mise a jour de la température du spa uniquement lorsque la pompe de circulation est en route

# 23/06/2020
* Création d'un serveur de connexion intermédiaire

## 22/04/2020
* Ajout de timeout sur les connexion pour libérer le flux
* Lecture écriture en boucle tant que le client est connecté
* Connexion et Déconnexion au SPA lors de chaque requête

## 03/04/2020
* Séparation du plugin et sa documentation

# Beta
## 22/04/2021
* Netoyage du code
* Creation de commande groupé (Etat + actions)
* Commande toogle passé en commande unitaire
