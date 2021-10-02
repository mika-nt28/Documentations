---
layout: default
title: Face détection (facedetection)
lang: fr_FR
pluginId: facedetection
---

# Description

Ce plugin utilise OpenCv pour détecter les visages sur vos camera.

# Installation et Configuration

Pour fonctionner le plugin a besoin d'un logiciel tel que OpenCv, il est impératif de lancer l'installation des dépendances.

![Page de configuration général](../images/ConfigurationGeneral.jpg)

Pendant l'installation des dépendances, qui peut être longue, nous pouvons continuer en configurant nos caméras à scruter.

![Page de configuration camera](../images/ConfigurationCamera.jpg)

Il est assez simple d'ajouter une caméra avec un simple bouton et on y saisit les information de connexion.

* Nom : on donne un nom à notre camera
* Authentification : on saisit ses identifiant de connexion si besoin
* URL de connexion (rtsp://) : on saisit son url

# Ajout d'un groupe actions

Lorsqu'un caméra détecte au moins un visage, les groupes seront mise à jour, il est impératif d'en crée un.
Pour le moment seul 1 groupe est utile, à faire évoluer.

Voici le commandes qui seront automatiquement créées par le plugin

![Liste de commandes](../images/Commandes.jpg)

A chaque détection de visage dans un groupe il sera possible d'effectuer des actions.
