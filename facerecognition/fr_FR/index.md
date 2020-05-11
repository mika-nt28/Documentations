---
layout: default
title: Reconnaissance facial (facerecognition)
lang: fr_FR
pluginId: facerecognition
---

Description
==========
Ce plugin utilise OpenCv pour détecter et reconnaitre votre visage. Attention, toute de même aux permissions que vous accordez au plugin car on peut le tromper avec des photos … ou son jumeau

Ce plugin est compatible avec toute camera disposant d'un flux rstp http ou une camera USB

> Le plugin est encore jeune et peut encore comporter quelques bugs mais il évolue régulièrement : n’hésitez pas à me contacter sur le site de Jeedom Community avec toutes vos remarques et suggestions.

Installation et Configuration
=============================

Pour fonctionner le plugin a besoin de certains logiciels comme [OpenCv](https://github.com/opencv/opencv/wiki) ou il est impératif de lancer l’installation des dépendances.

![Page de configuration général](../images/ConfigurationGeneral.jpg)

L’installation des dépendances peut prendre beaucoup de temps (plus de 4h lors de mes derniers tests) et par conséquent je vous invite a être patient et a poursivre la configuration

Configuration des cameras et de leurs demon
--------------------------------------------
Vous pouvez configurer vos cameras (une après l’autre) simplement en cliquant sur le bouton « ajouter » et en saisissant les informations de connexion.

* Nom : On donne un nom à notre camera.
* Activation du démon: Permet de choisir si une camera configuré est utilisée ou non.
* Port du démon: Il est impératif de saisir un port libre différent pour chaque caméra, celui çi interagit avec le démon dynamiquement (mise à jours des visage reconnus, prise de snapshots etc…)
* FrameRate: Permet de determiner combient d'image par seconde le plugin va analysé (plus le framerate est elevé plus il consomme du CPU). Le Frame rate ne doit pas etre superieur au framerate de la camera
* Sensibilité : Permet de regle la qualité de detection. Plus il est important et plus la detection est strict
* Taille minimal du visage a la detection (pixel) : Permet de specifier la taille minimal sur la photo que doit avoir un visage
* Autentification : on saisi les identifiants de connexion si besoin.
* URL de connexion (rtsp://) : On saisis son url (attention de ne pas se tromper ici, je ne peux pas vous aider à cause du nombre immense de caméra qui existent)

> La sensiblité couplé a la taille minimal permete d'obtenir un stabilité dans le detection et limiter les faux positif.
Plus les parametres sont stricte, et la precision de la detection important mais il est plus difficile d'avoir une detection.
C'est porpre a chaqu'un de trouvé le meilleur compromis

> Exemple Taille 110x110, sensibilité 13, framerate 15

Configuration de prise de vue
-----------------------------

Il est possible que le plugin enregistre un snapshot a chaque detection.
* Prendre des Snapshot lors d'une detection : Autorise le plugin a sauvgarder la prise de vue
* Emplacement du dossier Snapshot : Spécifie le dosssier ou enregistrer les snapshots
* Surveiller la taille du dossier Snapshot de chaque camera : Autorise la surveillance et la suppression des snapshots les plus vieux
* Taille du dossier Snapshot de chaque camera (Mo) : Taille maximal que peut contenir le dossier

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
* Apprendre le visage : Outils d’apprentissage de votre visage.
* Couleur du cadre : Permet de donner une couleur au cadres lors de la detection

Apprentissage de votre visage
-----------------------------

Avant de pouvoir utiliser la reconnaissance faciale, nous devons d’abord recueillir une librairie d’images du visage que nous voulons reconnaître. L’apprentissage peut être effectuer sur plusieurs jours ou semaines pour recueillir des exemples de leur visage dans:

* Conditions d’éclairage
* Heures de la journée
* Humeurs et états émotionnels
* Angle de prise de vue

L'outil d'apprentissage a besoin que l'on cree une librairie du visage a reconnaitre avant de lancer la creation de ses parametre avec le bouton "Valider"
![Apprentissage utilisateur](../images/facerecognition_screenshot_ApprentissageUtilisateur.jpg)

### Import des photos

L'outil embarque la possibilité de telecharger une photo

![Outil d'acquisition d'un visage par import de photo](../images/facerecognition_screenshot_ApprentissageImport.jpg)

> L'extention doit etre *.jpg *.png .jpeg" *.tiff

> La taille maximal de la photo doit etre inferieur a 5Mo

Pour importer vos photos, cliquer sur "Telecharger", puis selectionner vos photos 1 par 1.
A chaque import, le plugin vas analyser la photo telecharger et importer dans la librairie chaque visage reconnue

> Une photo peut etre refusé si aucun visage n'est reconnue, vous pouvez jouer sur la sensibilité

### Prendre un snapshot d'un visages sur nos camera

Pour utiliser la fonction de prise de vue, il vous faut

![Outil d'acquisition d'un visage par camera](../images/facerecognition_screenshot_ApprentissageCamera.jpg)

* Selectionner la camera
* Verifer que le visage a reconnaitre est present sur la camera (cadre autour du visage)
* Cliquer sur "Ajouter"

A chaque ajout, le plugin vas importer dans la librairie chaque visage reconnue.
Si pas de visage sur la camera l'action est ignoré

### Lancement de l'apprentissage

Pour finir l'apprentissage, le plugin a besoin de que l'on lance une compilation de critere de reconnaissance.
A la fin de la compilation les nouveaux parametre seront automatiquement mise a jours dans le demon de chaque camera et votre nouvelle utilisateur sera alors reconnue

![Apprentissage utilisateur](https://www.pyimagesearch.com/wp-content/uploads/2018/06/pi_face_recognition_dataset.jpg)

Gerer un planning d'autorisation
---------------------------------

Pour limiter l'usage de la reconnaissance il est possible de créer des crenaux horaire d'autorisation

* Autorisation (Unique) : Permet que l'autorisation ne soit donnée qu'une seul fois
* Planning : permet de choisir les crenaux horaire dans la semaine ou sur une periode choisis

![Apprentissage utilisateur](../images/facerecognition_screenshot_Planning.jpg)

Conditionner les actions
------------------------

Il est egalment possible de renforcer l'autorisation d'un utilisateur grace a des conditions

![Condition d'execution des action de l'utilisateur](../images/ConfigurationConditions.jpg)

Executer les actions
--------------------

Lorsque le visage sera reconnu, que l’utilisateur est activé, qu'il soit auorisé sur le planning, et qu'il remplisse toutes les conditions, le plugin permet d’exécuter des actions.

> Ouverutre du portail, alert, ...

![Actions spécifique a l'utilisateur](../images/ConfigurationActions.jpg)
