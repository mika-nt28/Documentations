---
layout: default
title: Acces par QR code (QRacces)
lang: fr_FR
pluginId: QRacces
---

Description
==========
Ce plugin permet de gérer une accès par QRcode.
Un Qr code est envoyé par mail à l'utilisateur autorisé

Configuration
=============

Un fois l'installation et l'activation du plugin réalisé, nous allons le configurer.

![introduction01](../images/Configuration.JPG)

Ajout de camera
---------------

Il est possible d'ajouter autant de camera que l'on souhaite, cependant plus y a de camera plus votre systeme sera ralentis
Dans la partie 'Configuration des Camera' cliquer sur 'Ajouter' 

* Nom : On donne un nom à notre camera.
* Activation du démon: Permet de choisir si une camera configuré est utilisée ou non.
* FrameRate: Permet de determiner combient d'image par seconde le plugin va analysé (plus le framerate est elevé plus il consomme du CPU). Le Frame rate ne doit pas etre superieur au framerate de la camera
* Autentification : on saisi les identifiants de connexion si besoin.
* URL de connexion (rtsp://) : On saisis son url (attention de ne pas se tromper ici, je ne peux pas vous aider à cause du nombre immense de caméra qui existent)

Envoie d'un mail
----------------
Le plugin transmet a l'utilisateur autorisé le QRcode uniquement par mail.
Pour cela il utilise le plugin "Mail" qui devra etre configurer sur ca partie equipement.
Il n'est pas necessaire de cree une commande mail par utilisateur, le plugin gere seul cette partie.

Dans la partie 'Email':
* Boite email : Objet jeedom du plugin mail
* Objet de l'email envoyer : Saisir le text de l'objet de l'email
* Corp du message: Il est possible d'ajouté un texte qui sera joint dans le mail

Gestion des snapshots
---------------------

Il est possible que le plugin enregistre un snapshot a chaque detection.
* Prendre des Snapshot lors d'une detection : Autorise le plugin a sauvgarder la prise de vue
* Emplacement du dossier Snapshot : Spécifie le dosssier ou enregistrer les snapshots
* Surveiller la taille du dossier Snapshot de chaque camera : Autorise la surveillance et la suppression des snapshots les plus vieux
* Taille du dossier Snapshot de chaque camera (Mo) : Taille maximal que peut contenir le dossier

Création d'une autorisation utilisateur
=======================================

Rendez vous dans Plugins => Sécurité => Acces par QRcode
Cliquer sur "Ajouter" pour cree une nouvelle autorisation

Utilisateur
-----------
![introduction01](../images/Utilisateur.JPG)

Ici, on retrouve les parametres courant de jeedom
* Nom : Nom de la commande d'autorisation
* Email de la personne autorisé : Adresse mail pour l'envoie du QRcode
* Objet parent : Objet jeedom si on veux l'afficher sur le dashbord
* Activer / Visible : Permet de desactivé totalement l'acces

Gérer un planning d'autorisation
---------------------------------

Pour limiter l'usage de la reconnaissance il est possible de créer des crenaux horaire d'autorisation

* Autorisation (Unique) : Permet que l'autorisation ne soit donnée qu'une seul fois
* Planning : permet de choisir les crenaux horaire dans la semaine ou sur une periode choisis

![Planning utilisateur d'autorisation](../images/QRacces_screenshot_Planning.jpg)

Conditionner les actions
------------------------

Il est egalment possible de renforcer l'autorisation d'un utilisateur grace a des conditions

![Condition d'execution des action de l'utilisateur](../images/ConfigurationConditions.jpg)

Executer les actions
--------------------

Lorsque le visage sera reconnu, que l’utilisateur est activé, qu'il soit auorisé sur le planning, et qu'il remplisse toutes les conditions, le plugin permet d’exécuter des actions.

> Ouverutre du portail, alert, ...

![Actions spécifique a l'utilisateur](../images/ConfigurationActions.jpg)

FAQ
===

L'utilisateur n'a pas recu de mail
----------------------------------

* Vérifier le compte mail sur Jeeedom
* Verifier que l'autorisation est armée (Cadenas sur le dashbord)




