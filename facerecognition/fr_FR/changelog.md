---
layout: default
title: Reconnaissance facial (facerecognition)
lang: fr_FR
pluginId: facerecognition
---

# Stable
## 11/05/2020
### Apprentissage
* Refonte global de l'apprentissage
* Extraction des visages lors de l'import de photo ou de prise de snap par la camera
* Extraction du visage lors d'un snap camera à l'apprentissage
* Si plusieurs visage sur une photo de l'apprentissage, alors elle ne sera pas retenue pour l'apprentissage et nous crée des images séparer de chaque visage
* Suppression et recréation du fichier data de reconnaissance des visages
* Apprentissage uniquement de l'utilisateur en cours

### Démon
* Encodage de l'url en argument du démon
* Analyse en multi-thread
* Ajout des paramètres Largeur et Hauteur minimal du cadre des visages
* BugFix couleur du cadre aléatoire (dernier utilisateur analyse)

### Panel
* BugFix suppression de plusieurs photo
* BugFix affichage des Snapchat sur le panel
* Limitation de la hauteur d'affichage des Snapshots sur le panel

### Configuration utilisateur
* Snapshot envoyer en action si plugin compatible (mail, slack, telegram, ...)
* Correction fautes de frappe
* Ajout de l'aide contextuel
* Ajout d'un paramètre de sélection des caméras permettant l’exécution d'un action
* Ajout d'un paramètre de sélection des caméras permettant l’évaluation d'une condition

## 17/04/2020
* Ajout de la sensibilité de détection (plus il est faible, plus la détection es sensible)
* Limitation de l'import d'image a  5Mo et au format jpg, jpeg, png, tiff (Refus + message d'erreur
* Ajout de la personnalisation des couleurs de cadre par utilisateur
* Refonte du code d'apprentissage
* Bugfix affichage de la dernière liste de Snapchat sur le panel

## 08/04/2020
* Bugfix suppression de Snapchat
* Refonte de l'apprentissage des visages

## 04/04/2020
* Bugfix suppression d'utilisateur
* BugFix Suppression Snapchat détection
* BugFix Url changelog

## 03/04/2020
* Séparation du plugin et sa documentation

## 02/04/2020
* Gestion de la suppression d'utilisateur
* Ajout de la recherche de camera USB
* Ajout d'un planning
* Ajout de la prise de Snapchat a la détection

## 18/12/2020
* Première sortie stable avec néanmoins beaucoup de fausse détection

## 28/03/2020
* Refonte de la présentation de configuration des cameras
* Ajout d'un paramètre Framerate au démon de manière à configurer le nombre d'image analysé par le plugin (attention à ne pas demander plus d'analyse que d'image fournis par la camera)
* Le démon ne s'arrête plus et parcourt toute les images de la camera (bugfix du retard d'image)
* Changement du fichier de détection de visage par l'officiel OpenCV
* Création d'une connexion au démon python
* Mise a jours dynamique du fichier de data de nos apprentissage sur le visage
* Prise de Snapchat depuis la camera dynamique (sans les cadres)
* Suppression de la limitation du nombre de photo pour lancer l'apprentissage de nos visages
* Mise a jours de droit sur les dossier

# Beta
## 17/06/2020
* Bugfix import de photo pour l'apprentissage
* Bugfix sauvegarde de snapshot lors de l'usage par GPU 
* Bugfix alert et prise de snapshot unique de detection (a confirmer)

## 15/06/2020
* Ajout de l'affichage des etat utilisateur sur le panel
* Gestion de l'etat de détéction par le demon

## 11/06/2020
* Bugfix envoie du snapshot a la detection
* Prise du snapshot et signalement uniquement au debut de la detection (a tester sur de long detection)

## 10/06/2020
* Restructuration du code
* Prise de snapshot par le demon (perte de l'envoie du snapshot dans les actions)
* Bugfix detection KO
* Bugfix prise de capture du visage par la camera dans l'apprentissage

## 09/06/2020
* BugFix Erreur de detection
* Deplacement du fichier d'apprentissage des visages vers le dossier data

## 06/06/2020
* Bugfix connexion par caméra USB

## 04/06/2020
* BugFix chemin incorecte vers les scriptes python

## 03/06/2020
* Refonte du code python pour integrer dans une class l'analyse
* Utilisation du GPU si compatible
* Verification de l'installation de dependance
* Suppression et deplacement des fichiers pour le nettoyage sur V4

# A venir

