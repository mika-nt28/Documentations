---
layout: default
title: Plex (plex)
lang: fr_FR
pluginId: plex
---
Contrôler vos clients plex grâce à votre domotique.
Créer des réveil, musical grâce à l'association de plex et de Jeedom.

Qu'est-ce que PLEX?
===================

Plex organise vidéo, musique et photos à partir de bibliothèques de médias personnels et les cours d'eau pour les téléviseurs intelligents, des boîtes en streaming et les appareils mobiles. Il est un système de lecteur multimédia et suite logicielle composée de plusieurs applications de lecture pour les interfaces utilisateur.


Configuration
=============

Configuration des serveur Plex
------------------------------
La première chose à réaliser est de connecter Jeedom aux serveurs Plex.
Il est possible de disposer de plusieurs serveurs

![introduction01](../images/plex_screenshot_configuration3.JPG)

Cliquez sur "Ajouter" et complétez les 3 champs d'informations pour la connexion à chaque serveur

* Adresse IP du serveur
* Le port de connexion
* Son nom, attention de bien respecter la casse de ce paramètre

Configuration d'un compte Plex
------------------------------
Il est recommandé de se connecteur avec un compte plex pour sécuriser les connexions.
Pour lier se compte à Jeedom il faut saisir vos identifiants

Pour connaître les informations liées à votre installation Plex, je vous conseille d'ouvrir la page de configuration de votre serveur Plex.
![introduction01](../images/plex_screenshot_ServeurConfiguration.jpg)

Nota:

Des indicateurs de démon sont également présents sur cette page de configuration.
Le démon permet de scruter l'état de médias en cours et détermine si une pause est établie sur le Player.


Configuration des clients Plex
==============================

Configuration de l'équipements
-----------------------------
Nous allons nous rendre sur la page de paramétrage des clients Plex Plugins > Multimedia > Plex.
Arrivé sur cette page, nous allons pouvoir accéder à nos clients déjà configurés, ou en ajouter un.

![introduction01](../images/plex_screenshot_configuration1.JPG)

Vous l'aurez deviné, pour ajouter un client, il suffit de cliquer sur le bouton "Ajouter" et de nommer l'équipement dans la fenêtre qui va apparaître.

![introduction01](../images/plex_screenshot_configuration2.JPG)

Commencez par personnaliser les paramètres généraux (activer, visible, parent)

Paramètre du client
------------------

Pour lier Jeedom a un client plex, il faudra sélectionner un client.
Pour qu'un client soit visible dans le plugin il faut que celui-ci soit ouvert et connecter au serveur/
Certain client n'est disponible que dans leur retour d'état, dans ce cas il faut qu'un media soit en cours de lecture pour qu'il soit visible

Activer l'option "Heartbeat" pour que le démon surveille votre client et mette à jours ses état de lecture.

Si votre client est sur la même machine que votre serveur alors le serveur remontra un IP localhost.
Si Jeedom n'est pas sur cette même machine alors il faut luis spécifier l'adresse IP du client sur le réseau

Ajoutez un incrément pour le volume.

Utilisation du widget
=====================

![introduction01](../images/plex_screenshot_widget_principal.jpg)

L'écran principal du widget permet les fonctions de base :

* Saut arrière
* Saut avant
* Reculer
* Avancer
* Affichage du menu
* Lecture / Pause
* Stop

Mais aussi de choisir le média en cliquant sur les affiches arrière.
Il permet également d'accéder aux différents menus.

![introduction01](../images/plex_screenshot_widget_Télécommande.jpg)

A droite, la télécommande qui permet de naviguer directement sur votre écran.

![introduction01](../images/plex_screenshot_widget_Liste.jpg)

Le menu de gauche permet des sélectionner une librairie et leur media associé.

![introduction01](../images/plex_screenshot_widget_Detail.jpg)

Mais aussi le détail du media.

