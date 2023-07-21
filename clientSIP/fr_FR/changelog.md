---
layout: default
title: Client SIP (clientSIP)
lang: fr_FR
pluginId: clientSIP
---

# Stable
## 17/03/2021
* Bugfix appel et reception depuis jeedom
* Ajout du nom de l'equipement dans les log

## 10/03/2021
* Dubug REGISTER avec 3CX (autentification par proxy)
  
## 01/05/2020
* Suppression des dépendance avec le plugin play TTS
* Ajout du moteur play TTS
* Suppression de la configuration de codec (inutile car on ne sait pas ce que le plugin peut supporter)
* Mise a jours de la configuration SDP
* BugFix Émission d'un appel

## 03/04/2020
* Séparation du plugin et sa documentation

# Beta
## 21/07/2023
* Conversion du fichier audio TTS au format PCMU (A tester)
* Evaluation des messages (possibilité d'ajouter des commande jeedom et tag #dtmf#)
* Bugfix action dtmf (a verifier)
  
## 14/07/2023
* BugFix sur la récupération des messages d'appel
* Message texte transmis au demon (plus de conversion TTS par PHP)
* Diffusion du message TTS sur le canal du télephone (A tester)

## 11/07/2023
* Ajout de la lecture de message en reception d'appel
* Ajout de messages liste par DTMF et diffusé en audio
* Ajout du retour d'execution des DTMF
* Boucle d'attente DTMF a 30s max
  
## 06/07/2023
* BugFix arret du demon
* Remontées des états du client (Etat appel / Etat connexion)
* Remplacement du format de convertion TTS MP3 vers WAVE pour une compatibilité directe a la diffusion (suppression de 2 conversion)
* Ajout d'un lecteur de fichier wave et diffusion a travers la connexion RTP (non tester)
* BugFix commande DTMF dans le bon champs

## 03/07/2023
* Refonte du plugin et passage sur une demon python (Tous doit etre a revalider et a tester,

# A venir
* Ajout du Speach to text (Google ou autre a définir)
* Couplage avec les interagtion Jeedom
* Ajout des Tag dans les messages (#dtmf#, #value#, ...)
* Mode Ask

