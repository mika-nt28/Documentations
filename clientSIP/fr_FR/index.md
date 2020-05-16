---
layout: default
title: Client SIP (clientSIP)
lang: fr_FR
pluginId: clientSIP
---

# Description

Ce plugin a pour but de connecter jeedom a notre réseau SIP de manière a ce que des interaction entre jeedom et son appellent soit possible

# Installation et configuration

## Installation


Le plugin embarque l'installation de dépendance pour faire du TexToSpeach (pas encore actif sur la plugin)
Pour poursuivre la configuration, il est important d'avoir installé ses dépendances

## Configuration

Pour utiliser se plugin, il est impératif d'avoir configurer un serveur SIP et d'y saisir les informations de connexions

![Server SIP](../images/ServerSip.jpg)	

# Ajouter un client SIP

Avant de commencer le paramétrage du client sur jeedom, il est impératif de l'avoir créé sur votre serveur 

![Client SIP Configuration](../images/ClientSipConfiguration.jpg)	

# Configuration général

Cette onglet est un standard de jeedom

* Nom de l'équipement : Permet de nommer sur jeedom sur votre réseau SIP le client virtuel crée
* Objet parent : Permet d'associer le widget sur votre Jeedom
* Catégorie : Permet d'associer un catégorie
* Activer : Permet d'activer le client sur jeedom et sur le réseau SIP
* Visible : Permet de rendre visible ou non le widget sur Jeedom

## Configuration du client SIP

Afin de pouvoir établir une connexion il est impératif d'avoir créé un numéro et un authentification sur votre serveur SIP.
Reporter ici les information

* Saisir les informations d'authentification sur le serveur : Identifiant précédemment créer
* Saisir le temps d'expiration : Temps d'expiration de votre numéro précédemment configurer sur votre serveur
* Choisir le type de transport : Type de transport choisie (seul l'udp a été validé)

Un fois sauvegarder jeedom communiquera avec votre réseau SIP

## Text To Speach

Le plugin va communiquer avec son interlocuteur à l'aide des interaction jeedom streamer par un text to speach
Configurer le dans cette onglet
* Langue : Permet de choisir la langue de la voix

# Commandes jeedom

La liste si dessous décrit chaque commande disponible sous jeedom

* Etat connexion: Cette commande reflète l'état du client sur le réseau SIP
  * Inactif: le client n'est pas enregistré et il ne sera pas possible de passer ou recevoir un appel
  *  Enregistrer: le client peut passer ou recevoir un appel
* Etat appel: cette commande détermine l'état de la ligne
  * Raccrocher: la ligne est libre
  * Appel en cours: jeedom compose un numéro et attend le retour du serveur
  * Sonnerie: Un appel est en cours et attend un réponse
  * Décrocher: Un appel est en cours de conversation
* Appel: Cette commande permet de saisir un numéro d'appel
