---
layout: default
title: Reconnaissance facial (facerecognition)
lang: fr_FR
pluginId: facerecognition
---

# Stable
## 17/04/2020
* Ajout de la sensibilité de détection (plus il est faible, plus la detection es sensible) 
* Limitation de l'import d'image a  5Mo et au format jpg, jpeg, png, tiff (Refus + message d'erreur
* Ajout de la personnalisation des couleurs de cadre par utilisateur
* Refonte du code d'apprentissage
* Bugfix affichage de la derniere liste de snapshot sur le panel
## 08/04/2020
* Bugfix suppression de snapshot
* Refonte de l'apprentissage des visages
## 04/04/2020
* Bugfix suppression d'utilisateur
* BugFix Suppression snapshot detection
* BugFix Url changelog
## 03/04/2020
* Separation du plugin et sa documentation
## 02/04/2020
* Gestion de la suppression d'utilisateur
* Ajout de la recherche de camera USB
* Ajout d'un planning
* Ajout de la prise de snapshot a la detection
## 18/12/2020
* Premiere sortie stable avec neanmoins beaucoup de fausse detection
## 28/03/2020
* Refonte de la presentation de configuration des cameras
* Ajout d'un parametre Framerate au demon de maniere a configurer le nombre d'image annalysé par le plugin (attention a ne pas demander plus d'analyse que d'image fournis par la camera)
* Le demon ne s'arret plus et parcout toute les images de la camera (bugfix du retard d'image)
* Changement du fichier de detection de visage par l'officiel OpenCV
* Creation d'une connexion au demon python
* Mise a jours dynamique du fichier de data de nos apprentissage sur le visage
* Prise de snapshot depuis la camera dynamique (sans les cadres)
* Suppression de la limitation du nombre de photo pour lancer l'apprentissage de nos visages
* Mise a jours de droit sur les dossier
# Beta
## 30/04/2020
* Encodage de l'url en argument du demon
* Si plusieurs visage sur une photo de l'aprentissage, alors elle ne sera pas retenu pour l'apprentissage et nous cree des images séparer de chaque visage
## 28/04/2020
* Analyse en multi-thread
* Extraction du visage lors d'un snap camera a l'apprentissage
* Suppression et recreation du fichier data de reconnaissance des visages
* BugFix Hauteur minimal d'un visage
## 24/04/2020
* Ajout des parametres Largeur et Hauteur minimal du cadre des visages
## 22/04/2020
* BugFix suppression de plusieurs photo
* Apprentissage uniquement de l'utilisateur en cours
* BugFix couleur du cadre aleatroire (dernier utilisateur analyse)
## 20/04/2020
* Snapshot envoyer en action si plugin compatible (mail, slack, telegram, ...)
* Correction fautes de frappe
* Ajout de l'aide contextuel dans la configuration du plugin
## 18/04/2020
* Ajout d'un parametre de sélection des cameras permettant l’exécution d'un action
* Ajout d'un parametre de sélection des cameras permettant l’evalation d'une condition
* Ajout de l'aide contextuel a chaque element de configuration utilisateur
* BugFix affichage des snapshot sur le panel
* Limitation de la hauteur d'affichage des snapshots sur le panel

# A venir

* Refonte du module d'apprentissage pour extraire de chaque photo uniquement le visage a détécter
* Lancement de la reconnaissance dans un autre thread pour evité les latence de camera


