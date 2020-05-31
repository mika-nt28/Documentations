---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Stable

## 27/05/2020
* Ajout info lors de la recherche des Tiles
* Amélioration affichage des commandes
* Migration commande API Wifi de V3 à V5
* Séparation des équipements Home et Tiles dans la liste des équipements
* Nettoyage des cron a la suppression du plugin

## 03/04/2020
* Séparation du plugin et sa documentation

## 19/12/2019
* BugFix Syntax Error

## 11/12/2019
* BugFix déconnexion en cas de réponse fausse
* Suppression des équipements réseau en cas de réponse invalide

## 10/12/2019
* Restructuration de la class API
* Création d'un cron de rafraichissement du tocken pour avoir qu'une seul session
* Mise a jours du widget Réseau

## 27/11/2019
* Ajout des widgets pour la partie mobile

# Beta
## 31/05/2020
* Equipement de type "Tiles"
    * Remplacement ' dans le nom de l'équipement ou de la commande par un espace
    * Remplacement "É" dans le nom des commande par "E"
    * Début ajout type de générique sur les commandes
    * Masquage du bouton ajouter commande
    * Correction non apparition commande rechercher dans l'équipement "home Adapter" après une premiere recherche
    * Modification de la visibilité par défaut de certaines commandes (Batterie, Code Pin => non visible)
    * Renommage des commandes (ajout ETAT dans le cas où la commande et l'info porte le même nom)
    > Pour avoir l'ensemble des nouveautés sur les équipements, il est nécessaire de les supprimer et de cliquer ensuite sur "rechercher les Tiles"

* Ajout commande "refresh" => commande masquer par défaut dans les listes des commandes
