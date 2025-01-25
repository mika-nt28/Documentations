---
layout: default
title: Production Energie (prosommateur)
lang: fr_FR
pluginId: prosommateur
---

# Stable
## 25/07/2024
* BugFix remise a zero des compteurs apres une sauvegarde ou redémarage du démon
* BugFix Stockage virtuel négatif
* BugFix Utilisation du stockage virtuel non demandé

## 15/07/2024
* Restructuration du codeet des phases de calcul
* Ajout d'une commande stockage virtuel (injection dans le reseau)
* Consommation revue (delta entre la produdtion et la conso vue sur le reseau)
* Ajout des parametre de puissance a utiliser sur le reseau / batterie / stockage virtuel
* Activation des different mode de consomation pour chaque equipement
* Ajout de la gestion des batteries et du stockage virtuel (injections sur le reseau)
* Lissage de la production obligatoire (sera mise a jours si necessaire)
* Formule possible dans le champs Batterie et Consommation
  
## 26/07/2022
* Ajout d'une configuration sur la durée du lissage de production
  
## 20/04/2021
* Initialisation de l'etat de gestion a Off au démarrage du démon / sauvgarde
* BugFix execution des actions

## 03/01/2021
* Bugfix : Correction bug sur la sauvegarde des gestions
* 
## 27/07/2020
* Correction enregisterement des actions et conditions

## 03/04/2020
* Séparation du plugin et sa documentation

# Beta

