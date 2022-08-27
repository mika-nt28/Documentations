---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Info

## Important

> **_Pour rappel_** s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de corrections de bugs mineurs.
>
> **Attention Il est nécessaire d'avoir la Freebox serveur en version 4.3 pour que le plugin fonctionne**

## Fil d'actualité

> [Voir le fil d'actualité du plugin sur communauty](https://community.jeedom.com/t/info-plugin-freebox-mise-a-jour-des-composants-de-la-delta-tiles-systeme/30673)

# Changelog BETA

# 07/08/2022, 15/08/2022, 28/08/2022

- Création d'un Cron semaine pour rechercher la version de l'API valide
- Utilisation de la dernière version de l'API valide pour l’ensemble des équipements
- Ajout d'un bouton dans la modale “Appairage” pour rechercher la version de l'API

- **Network**

  - Correction de la lecture des ports
  - Correction Ajout mac adresse en liste noire ou blanche

- **Airmedia**

  - Réécriture complète de cette partie
  - Les anciennes commandes seront supprimées car non compatible

- **Tiles**

  - Correction du refresh équipement si le cron global n’est pas actif

- **Appareils connectés** (28/08/2022)

  - Correction de l'ordre des appareils (en premier les connectés suivi des nons connectés)
  - Réécriture de la commande de refresh et de création des commandes en vue de l'ajout de future amélioration
  - Ajout de nouvelle commande pour mettre IP fixe et choisir les types de périphérique
    > - Les anciennes commandes seront supprimer lors de la prochaine mise à jour
    > - "Ajouter supprimer IP Fixe" pour les équipements "Appareils connectés" et "Appareils connectés Wifi Invité"

- **Wifi** (28/08/2022)

  - Ajout de nouvelle commande Gérer le filtrage des adresses MAC
    > - Les anciennes commandes seront supprimer lors de la prochaine mise à jour
    > - "Ajout - Supprimer filtrage Mac" pour l'équipement "WIFI"

- **Contrôle Parental** (17.08.2022)

- Correction bug sur la recherche des nouveaux contrôles

# A TESTER

- Recherche des appareils connectés (y compris Wifi)
- Vérifier que si le type de périphérique est changé dans la freebox, est bien prise en compte dans Jeedom
