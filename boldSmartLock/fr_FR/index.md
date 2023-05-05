---
layout: default
title:  Bold Smart Lock (boldSmartLock)
lang: fr_FR
pluginId: boldSmartLock
---
# Description

Plugin permettant de piloter les serrures Bold Smart Lock.
Pour fonctionner, il vous faut une Bold connect ainsi qu'un cylindre

# Configuration du plugin

![Page de configuration du plugin ](../images/boldSmartLock_screenshot_Configuration.jpg)

Le plugin n'a pas besoin de dépendance, il communique avec les serveurs Bold au travers de leur API
Pour fonctionner le plugin a besoin d'information 
* Client ID : a determiné si besoin spécifique,  par défaut **BoldAppStaging**
* Secret key  : a determiné si besoin spécifique,  par défaut **aivM9yDBV2cngb4XeV8tJmyd**
* Login : votre login de connexion a bold
* Mots de pass : votre mots de passe de connexion a bold

# Configuration Equipements

![Page de configuration des equipements](../images/boldSmartLock_screenshot_Equipements.jpg)

## Autodetection
A venir une auto detection et creation des equipements (en attente des premier retour de connexion)

## Parametres
![Page de configuration equipement](../images/boldSmartLock_screenshot_Equipement.jpg)
Paramtrage standard a jeedom, attention que le numero de serie de la serrure soit spécifié

## Commandes

Pour cette premiere version seul les commande
* Etat
* Ouvrir
* Fermer
