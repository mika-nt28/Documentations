---
layout: default
title: Face détection (facedetection)
lang: fr_FR
pluginId: facedetection
---

# Description

Ce plugin utilise OpenCv pour détecter les visages sur vos camera.

# Installation et Configuration

Pour fonctionner le plugin a besoin de certain logiciel comme OpenCv, il est impératif de lancer l'installation des dépendances

![Page de configuration général](../images/ConfigurationGeneral.jpg)

Pendant l'installation des dépendances, qui peuvent être long, nous pouvons continuer en configurant nos camera à scruter

![Page de configuration camera](../images/ConfigurationCamera.jpg)

Il est assez simple d'ajouter une caméra avec un simple bouton et on y saisi les information de connexion

* Nom : On donne un nom à notre camera
* Authentification : on saisit ses identifiant de connexion si besoin
* URL de connexion (rtsp://) : On saisit son url

# Ajout d'un groupe actions

Lorsqu'un camera détecte au moins un visage les groupes seront mise à jour, il est impératif d'en crée 1
Pour le moment seul 1 groupe est utile, à faire évoluer

Voici le commandes qui seront automatiquement crée par le plugin

![Liste de commandes](../images/Commandes.jpg)

A chaque détection de visage dans un groupe il sera possible d'effectuer des actions
