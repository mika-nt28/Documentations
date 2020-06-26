---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Stable

## 11/06/2020

- Bug : Correction Affichage Batterie : Masqué par défaut
- Bug : Template par défaut pour le sabotage et l'ouverture
- Bug : Invertion de la valeur par défaut sur le couvercle + attribution template
- Bug : Détecteur de présence correction des templates et l'inversion des signaux
- Autorisation de supprimer les commandes

## 09/06/2020

- Modification remontée alarme batterie lors de la création de la commande

## 07/06 et 08/06/2020

- Equipement de type "Tiles"

  - Attribution de la catégorie des titles (sécurité, lumière)
  - Correction Bug bouton ON/OFF \* Ajout Info dans log en mode debug
  - Remplacement ' dans le nom de l'équipement ou de la commande par un espace
  - Remplacement "É" dans le nom des commande par "E"
    _ Masquage du bouton ajouter commande
    _ Ajout des types de générique sur certaines commandes
    _ Modification de la visibilité par défaut de certaines commandes (Batterie, Code Pin => non visible)
    _ Correction non apparition commande rechercher dans l'équipement "home Adapter" après une premiere recherche \* Renommage des commandes (ajout Etat dans le cas où la commande et l'info porte le même nom)
    > Pour avoir l'ensemble des nouveautés sur les équipements, il est nécessaire de les supprimer et de cliquer ensuite sur "rechercher les Tiles"

- Ajout commande "refresh" => commande masquer par défaut dans les listes des commandes
- Clean code

## 27/05/2020

- Ajout info lors de la recherche des Tiles
- Amélioration affichage des commandes
- Migration commande API Wifi de V3 à V5
- Séparation des équipements Home et Tiles dans la liste des équipements
- Nettoyage des cron a la suppression du plugin

## 03/04/2020

- Séparation du plugin et sa documentation

## 19/12/2019

- BugFix Syntax Error

## 11/12/2019

- BugFix déconnexion en cas de réponse fausse
- Suppression des équipements réseau en cas de réponse invalide

## 10/12/2019

- Restructuration de la class API
- Création d'un cron de rafraichissement du tocken pour avoir qu'une seul session
- Mise a jours du widget Réseau

## 27/11/2019

- Ajout des widgets pour la partie mobile

# Beta

## 25/06/2020

- **Wifi**
  - Déplacement des commandes vers un équipement spécifique Wifi
  - Ajout icône pour les commandes ON et OFF (Uniquement pour les nouvelles installations)
  - Ajout widget pour le status du wifi (uniquement pour la V4)
  - Passage de l'API de V3 à V5
- **Téléphone**
  - Amélioration du widget
  - Ajout icônes pour les différentes commandes (en couleur pour la V4)
- **Systèmes**
  - Ajout icônes pour les températures et le ventilateur
  - Ajout icônes pour les boutons updates et reboot (en couleur pour la V4)
  - Corrections du sous type des équipements
  - Mise à jour des min et maxi de certaines commandes
- **Airplay**
  - Ajout icône stop et play (Uniquement pour les nouvelles installations, en couleur pour la V4)
- **Tiles**
  - Bug luminosité 0 à 255 + affichage du min/max sur les commandes numériques
  - Ajout BP type Switch/Toggle
  - Déplacement de la fonction rechercher Homeadpater dans la recherche des Tiles (Nécessaire uniquement pour les Freebox DELTA)
  - Regroupement des fonctions Tiles et Homeadapter
  - Ajout info de du type d'action et d'équipement
    > il est nécessaire de cliquer sur "Scan Tiles" pour avoir ces infos
- **Corrections et améliorations**
  - Correction Bug : **Roue crantée en boucle sur activation plugin**
  - Désactivation de la création des équipements à la première installation
  - Ajout commande pour rechercher les équipements systèmes de la Freebox
  - Ajout analyse réseau après la recherche des équipements systèmes
  - Ajout dans la liste des commandes : L'icône, Mini-Maxi
  - Désactivation de la création des équipements à la première installation
    > il faudra cliquer sur "Scan équipements standard"
