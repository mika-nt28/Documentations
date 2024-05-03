---
layout: default
title: Accès par QR code (QRacces)
lang: fr_FR
pluginId: QRacces
---
# Stable
## 03/05/2024
* Mise a jour affichage image pour compatibilité Jeedom 4.4
* suppression de l'envoie et regenration automatique du QRcode a chaque envoie
* Ajout d'un bouton pour la regénération et l'envoie du QRcode
* Débug de la détéction
* Ajout d'un cadre de détéction sur l'image camera panel
* Abaissement de la tempo de 0.1s apres l'annalyse de l'image pour baisser la consomation CPU (Beta a voir la dégradation de la détéction)

## 03/08/2022
* Accecibilité de la configuration camera sur la page de configuration des utilisateurs et sur le panel
* Refonte de la présentation du panel
* Mise a jours du planning depuis le panel
* Ajout d'une tempo de 1s apres l'annalyse de l'image pour baisser la consomation CPU (Beta a voir la dégradation de la détéction)
* Mise a jours de l'affichage de l'image par evenement apres l'ecriture par le demon
* Dependance installé par package
* Envoie du QRcode par tous plugin de transmission d'image
* Acces a la configuration planning du widget

## 26/07/2022
* BugFix affichage du QRcode dans la configuration utilisateur

## 17/07/2020
* Ajout de la commande detect
* Mise a jours du scripte d'installation

## 16/07/2020
* Bugfix Suppression camera
* Ajout d'un parametre d'activation de prise de video

# Beta

## 03/08/2022
* Envoie du QRcode par tous plugin de transmission d'image (toutes les commande de type message sont compatible mais seul certain plugin sont capable de transmetre une image)
* BugFix de l'image QRcode affiché dans le core de message HTML

# A venir
