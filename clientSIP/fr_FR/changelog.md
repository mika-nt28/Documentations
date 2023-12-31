---
layout: default
title: Client SIP (clientSIP)
lang: fr_FR
pluginId: clientSIP
---

# Stable
## 04/08/2023
* Refonte du plugin et passage sur une demon python (Tous doit etre a revalider et a tester,
* Remontées des états du client (Etat appel / Etat connexion)
* Décrochage automatique lors d'un appel
* Racrochage automatique 30s sans activité (Lecture de message ou DTMF)
* Ecoute des DTMF et execution des actions associé (A venir saisi de valeur par DTMF)
* Evaluation des messages (possibilité d'ajouter des commande jeedom et tag #dtmf#) ==> filtré par numero et diffusion général + action DTMF (séparé dans une prochaine version)
* Conversion des message en TTS
* Conversion du fichier audio TTS au format PCMA/PCMU 
* Diffusion du message TTS sur le canal du télephone

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


# A venir
* Ajout du Speach to text (Google ou autre a définir)
* Couplage avec les interaction Jeedom
* Ajout des Tag dans les messages (#dtmf#, #value#, ...)
* Mode Ask

