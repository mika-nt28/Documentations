---
layout: default
title: Client SIP (clientSIP)
lang: fr_FR
pluginId: clientSIP
---

Description
===========
Ce plugin a pour but de conneter jeedom a notre reseau Sip de maniere a ce que des interation entre jeedom et son applent soit possible

Installation et configuration
=============================

Installation
------------

Le plugin embarque l'installation de dependance pour faire du TexToSpeach (pas encore actif sur la plugin)
Pour poursuivre la configuration, il est important d'avoir installé ses dependances

Configuration
------------

Pour utiliser se plugin, il est impératif d'avoir configurer un serveur sip et d'y saisir les informations de connexions

![introduction01](../images/ServerSip.jpg)	

Ajouter un client SIP
====================

Avant de commancer le parametrage du client sur jeedom, il est impératif de l'avoir cree sur votre serveur 

![introduction01](../images/ClientSipConfiguration.jpg)	

Configuration general
---------------------
Cette onglet est un standard de jeedom

* Nom de l'équipement : Premet de nommer sur jeedom sur votre reseau sip le client virtuel cree
* Objet parent : Permet d'associer le widget sur votre Jeedom
* Catégorie : Permet d'associer un catégorie
* Activer : Permet d'activer le client sur jeedom et sur le reseau sip
* Visible : Permet de rendre visible ou non le widget sur Jeedom

Configuration du client sip
--------------------------

Afin de pouvoir etablir une connexion il est imperatif d'avoir cree un numero et un authentification sur votre serveur SIP.
Reporter ici les information

* Saisir les informations d'autentificaiton sur le serveur : Identifiant precedement creer
* Saisir le temps d'expiration : Temps d'expiration de votre numero precedement configurer sur votre serveur
* Choisir le type de transport : Type de transport choisie (seul l'udp a ete validé)

Un fois sauvgarder jeedom communiquera avec votre reseau sip

Text To Speach
--------------
Le plugin vas communiquer avec sont interlocuteur a l'aide des interaction jeedom streamer par un text to speach
Configurer le dans cette onglet
* Langue : Permet de choisir la langue de la voix

Commandes jeedom
===============

La liste si dessous décrit chaque commande disponible sous jeedom

* Etat connexion: Cette commande reflete l'etat du client sur le reseau sip
  * Inactif: le client n'est pas enregister et il ne sera pas possible de passer ou recevoir un appel
  *  Enregistrer: le client peut passer ou recevoir un appel
* Etat appel: cette commande determine l'etat de la ligne
  * Racrocher: la ligne est libre
  * Appel en cours: jeedom compose un numero et attend le retour du serveur
  * Sonnerie: Un appel est en cours et attend un reponse
  * Décrocher: Un appel est en cours de conversation
* Appel: Cette commande permet de saisir un numero d'appel
