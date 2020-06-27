---
layout: default
title: Accès par QR code (QRacces)
lang: fr_FR
pluginId: QRacces
---

Description
==========
Ce plugin permet de gérer un accès par QR code.
Un QR code est envoyé par mail à l'utilisateur autorisé

Configuration
=============

Un fois l'installation et l'activation du plugin réalisé, nous allons le configurer.

![introduction01](../images/Configuration.JPG)

Ajout de camera
---------------

Il est possible d'ajouter autant de camera que l'on souhaite, cependant plus y a de camera plus votre système sera ralentis
Dans la partie 'Configuration des Camera' cliquer sur 'Ajouter'

* Nom : On donne un nom à notre camera.
* Activation du démon: Permet de choisir si une caméra configurée est utilisée ou non.
* FrameRate: Permet de déterminer combien d'image par seconde le plugin va analyser (plus le framerate est élevé plus il consomme du CPU). Le Frame rate ne doit pas être supérieur au framerate de la camera
* Port de connexion: Saisir un port de votre jeedom libre afin que le plugin puisse communiquer avec le demon de votre camera
* Authentification : on saisit les identifiants de connexion si besoin.
* URL de connexion (rtsp://) : On saisis son url (attention de ne pas se tromper ici, je ne peux pas vous aider à cause du nombre immense de caméra qui existent)

Envoie d'un mail
----------------
Le plugin transmet à l'utilisateur autorisé le QR code uniquement par mail.
Pour cela il utilise le plugin "Mail" qui devra être configurer sur sa partie équipements.
Il n'est pas nécessaire de crée une commande mail par utilisateur, le plugin gère seul cette partie.

Dans la partie 'Email':
* Boite email : Objet Jeedom du plugin mail
* Objet de l'email envoyer : Saisir le texte de l'objet de l'email
* Corps du message: Il est possible d'ajouter un texte qui sera joint dans le mail

Gestion des snapshots
---------------------

Il est possible que le plugin enregistre un snapshot a chaque détection.
* Prendre des Snapshot lors d'une détection : Autorise le plugin à sauvegarder la prise de vue
* Emplacement du dossier Snapshot : Spécifie le dossier où enregistrer les snapshots
* Surveiller la taille du dossier Snapshot de chaque camera : Autorise la surveillance et la suppression des snapshots les plus vieux
* Taille du dossier Snapshot de chaque camera (Mo) : Taille maximal que peut contenir le dossier

Création d'une autorisation utilisateur
=======================================

Rendez-vous dans Plugins => Sécurité => Accès par QR code
Cliquer sur "Ajouter" pour crée une nouvelle autorisation

Utilisateur
-----------
![introduction01](../images/Utilisateur.JPG)

Ici, on retrouve les paramètres courant de Jeedom
* Nom : Nom de la commande d'autorisation
* Email de la personne autorisé : Adresse mail pour l'envoie du QR code
* Objet parent : Objet Jeedom si on veut l'afficher sur le Dashboard
* Activer / Visible : Permet de désactiver totalement l'accès

Gérer un planning d'autorisation
---------------------------------

Pour limiter l'usage de la reconnaissance il est possible de créer des créneaux horaires d'autorisation

* Autorisation (Unique) : Permet que l'autorisation ne soit donnée qu'une seul fois
* Planning : permet de choisir les créneaux horaires dans la semaine ou sur une période choisie

![Planning utilisateur d'autorisation](../images/QRacces_screenshot_Planning.jpg)

Conditionner les actions
------------------------

Il est également possible de renforcer l'autorisation d'un utilisateur grâce à des conditions

![Condition d'exécution des actions de l'utilisateur](../images/ConfigurationConditions.jpg)

Exécuter les actions
--------------------

Lorsque le QRcode sera reconnu, si l’utilisateur est activé, qu'il soit autorisé sur le planning, et qu'il remplisse toutes les conditions, le plugin permet d’exécuter des actions.

> Les actions permetant d'envoyer un fichier (Mail, Slack, Télégrame, ...) receveront automatiquement le snapshot qui a ete pris lors de la détéction

> Ouverture du portail, alert, ...

![Actions spécifique à l'utilisateur](../images/ConfigurationActions.jpg)

FAQ
===

L'utilisateur n'a pas reçu de mail
----------------------------------

* Vérifier le compte mail sur Jeedom
* Vérifier que l'autorisation est armée (Cadenas sur le Dashboard)




