---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Info

## Important

> **_Pour rappel_**, s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de corrections de bugs mineurs.
>
> **Attention : Il est nécessaire d'avoir la Freebox serveur en version 4.8.13 pour que le plugin fonctionne.**

## Fil d'actualité

> [Voir le fil d'actualité du plugin sur Community](https://community.jeedom.com/t/info-plugin-freebox-mise-a-jour-des-composants-de-la-delta-tiles-systeme/30673)

# Changelog BETA

# 2024

## 12/11/2024

- Amélioration log

- **Téléphone**
- Ajout des commandes pour uniquement les nouveaux appel manqués et reçus
- Correction bug si la liste est vide
- Correction traduction

## 11/11/2024

- Correction création disque
- Correction requête pour le téléphone

## 10/11/2024

- Correction bug bouton lancement de l'authentification

## 11/10/2024

- Correction bug bouton lancement de l'authentification
- Correction type de regroupement d'appareil pour les débits
- Correction du demon : il sera redemarré uniquement si l'authentification a été faite lors de la première installation.

## 27/09/2024

- Correction bug installation depuis Market

## 20 et 25 /09/2024

- Correction bug setConfiguration sur la création des commandes
- Traduction
- Ajout Firmware dans le lien communauty
- Clean code
- Correction PHP 8
- Traduction
- Core mini 4.2
- Traitement fonction Deprecated

> **ATTENTION : IL FAUT RELANCER UNE RECHERCHE DES EQUIPEMENTS STANDARDS ET PARENTAL**

## 05/09/2024

- Correction PHP 8
- Correction bug remise a zéro téléphonie

## 23/08/2024

- Correction bug authentification

## 21/08/2024

> **ATTENTION : IL FAUT RELANCER UNE RECHERCHE DES EQUIPEMENTS STANDARDS ET PARENTAL**

- **Ensemble des équipements standards**

- Reprise de l'ensemble des mises à jour
- Amélioration info vers Community pour le Core 4.4

- **Contrôle parental**

- Ajout commande pour "appareil associé"
- Ajout commande pour "Vacances associées au profil"

> **ATTENTION : Il faudra supprimer la commande ETAT et renommer ETAT(1) en ETAT**

- **Afficheur**

- Ajout commandes pour forcer l'orientation
- Ajout commandes pour cacher la clef Wifi

- **Systeme**

- Ajout commande info sur la mise à jour du firmware de la Freebox Serveur avec les valeurs suivantes
      - Le processus de mise à jour est en cours d\'initialisation
      - Le micrologiciel est en cours de mise à jour
      - Le micrologiciel est à jour
      - Une erreur s'est produite pendant la mise à jour
- Ajout info de la langue d'affichage

- **Wifi**
- Ajout Info du type de mode Eco pour le wifi
- Ajout du mode de veille pour la planification du Wifi
