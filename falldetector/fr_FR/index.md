---
layout: default
title: Reconnaissance de chute (falldetector)
lang: fr_FR
pluginId: falldetector
---

Description
==========
Ce plugin utilise OpenCv pour détecter et reconnaitre les situations de chute.an 9

Installation et Configuration
=============================

Pour fonctionner le plugin a besoin de certains logiciels comme [OpenCv](https://github.com/opencv/opencv/wiki) ou il est impératif de lancer l’installation des dépendances.

![Page de configuration général](../images/ConfigurationGeneral.jpg)

Configuration des cameras
------------------------
Vous pouvez configurer vos cameras (une après l’autre) simplement en cliquant sur le bouton « ajouter » et en saisissant les informations de connexion.

* Nom : On donne un nom à notre camera.
* Activation du démon: Permet de choisir si une camera configuré est utilisée ou non.
* FrameRate: Permet de determiner combient d'image par seconde le plugin va analysé (plus le framerate est elevé plus il consomme du CPU). Le Frame rate ne doit pas etre superieur au framerate de la camera
* Autentification : on saisi les identifiants de connexion si besoin.
* URL de connexion (rtsp://) : On saisis son url (attention de ne pas se tromper ici, je ne peux pas vous aider à cause du nombre immense de caméra qui existent)

Configuration de prise de vue 
-----------------------------

Il est possible que le plugin enregistre un snapshot a chaque detection.
Pour cela il faut l'autoriser dans la configuration du plugin.
Apres l'activation, le plugin vous demande ou enregister les snap, il vous est libre de le choisir.

Pour ne pas remplir les disques avec des snapshot, il est possible de limiter la taille de chaque dossier camera

Creation d'un utilisateur
=========================

Rendez vous sur la page de configuration du plugin

![Page de liste utilisateurs](../images/ListeUtilisateurs.jpg)

Comme sur tous les plugins Jeedom, il vous suffit de cliquer sur « Ajouter » pour créer un nouvelle utilisateur.

Configurer l'utilisateur
-----------------------

![Page de configuration utilisateur](../images/ConfigurationUtilisateur.jpg)

* Nom : Nommer l’utilisateur.
* Objet parent: Choisir un objet parent.
* Catégorie : Sélectionner une catégorie.
* Activer : Activer si vous autorisez l’utilisateur.
* Visible : Afficher sur le dashboard.
Executer les actions
--------------------

Lorsque le visage sera reconnu et que l’utilisateur est activé, le plugin permet d’exécuter des actions.

![Actions spécifique a l'utilisateur](../images/ConfigurationActions.jpg)

Conditionner les actions
------------------------

Il est possible de conditionner l’exécution des actions avec l’onglet Condition

![Condition d'execution des action de l'utilisateur](../images/ConfigurationConditions.jpg)
