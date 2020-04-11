---
layout: default
title: Reconnaissance facial (facerecognition)
lang: fr_FR
pluginId: facerecognition
---

# Stable
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
## 11/04/2020
* Limitation de l'import d'image a  5Mo et au format jpg, jpeg, png, tiff (Refus + message d'erreur
* BugFix Activation de la camera toujours coché
				
## 09/04/2020
* Ajout de la personnalisation des couleurs de cadre par utilisateur
* Refonte du code d'apprentissage
