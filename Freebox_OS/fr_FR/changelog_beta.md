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

# 07/08/2022, 15/08/2022, 28/08/2022, 19/09/2022, 21/09/2022, 22/09/2022

 > **Il est necessaire de lancer un "reset API Freebox" après chaque mise à jour beta (voir documentation beta)** 

- Création d'un Cron semaine pour rechercher la version de l'API valide
- Utilisation de la dernière version de l'API valide pour l’ensemble des équipements
- Ajout d'un bouton dans la modale “Appairage” pour rechercher la version de l'API
- Ajout fonctionnalité core V4.3


- **Gestion réseau**

  > **Pour l'ensemble des nouveautés ci-dessous, il faut lancer le scan "Scan équipements standard"**

  - Nouvel équipement
  - il réuni plusieurs commandes partagées dans plusieurs équipements

  > - Gérer le filtrage mac pour le wifi
  > - Ajouter - supprimer une IP Fixe” pour les équipements

- **Network**

  - Correction de la lecture des ports
  - Correction Ajout mac adresse en liste noire ou blanche

- **Airmedia**

  > **Pour l'ensemble des nouveautés ci-dessous, il faut lancer le scan "Scan équipements standard"**

    - Réécriture complète de cette partie
    - Les anciennes commandes seront supprimées car non compatible

- **Tiles**

  - Correction du refresh équipement si le cron global n’est pas actif
  - Uniquement pour la beta (21.09.2022): Ajout de log pour tester

- **Appareils connectés** (28/08/2022)

  - Correction de l'ordre des appareils (en premier les connectés suivi des nons connectés)
  - Réécriture de la commande de refresh et de création des commandes en vue de l'ajout de futures améliorations
  - Les commandes suivantes seront supprimer lors de la prochaine mise a jour car elle est désormais intégré dans la gestion réseau :
    > - "Ajouter supprimer IP Fixe"
    > - "Wake on LAN"

- **Wifi** (28/08/2022)

  > - La commande "Ajout - Supprimer filtrage Mac" sera supprimer lors de la prochaine mise à jour car elle est désormais intégré dans la gestion réseau

- **Contrôle Parental** (17.08.2022)
  - Correction du bug sur la recherche des nouveaux contrôles


- **Appairage** (21.09.2022, 22/09/2022)
  - Ajout Bouton pour ignorer la vérification des droits 
  - Ajout Bouton pour faire un reset de l'API de la freebox



# A TESTER

- Recherche des appareils connectés (y compris Wifi)
- Tester les nouvelles commandes de l'équipement **Gestion réseau**
  > - Vérifier que si le type de périphérique est changé dans la Freebox, est bien pris en compte dans Jeedom
  > - Tester le nouveau système de commande pour mettre les IP
