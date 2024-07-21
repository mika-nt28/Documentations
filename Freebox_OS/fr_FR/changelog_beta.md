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
> **Attention : Il est nécessaire d'avoir la Freebox serveur en version 4.7 pour que le plugin fonctionne.**

## Fil d'actualité

> [Voir le fil d'actualité du plugin sur Community](https://community.jeedom.com/t/info-plugin-freebox-mise-a-jour-des-composants-de-la-delta-tiles-systeme/30673)

# Changelog BETA

# 2024

## 22/07/2024

- Amélioration info vers Community pour le Core 4.4
- Ajout Info du type de mode Eco pour le wifi
- Ajout du mode de veille pour la planification du Wifi

## 11/07/2024

- Amélioration log 
- Correction warning PHP8

## 11/04/2024

- Correction bug lors de la migration de la box DELTA à ULTRA

## 10/04/2024

- **Général**

- Nettoyage lors de l'installation des commandes obsolètes lors de la migration de box (révolution->ULTRA, DELTA->ULTRA).

- **Management**

- Amélioration Log

- **Wifi**

- Amélioration widget Wifi pour prendre en compte le mode économie d'énergie (Box ULTRA).

- **VM/CONTROLE PARENTAL/Disque**


- Non actualisation de l'équipement (de type VM / Contrôle parental) s'il n'est pas trouvé sur la Freebox et désactivation de l'équipement.

- **Disques**

  - Non actualisation de l’équipement si pas de disque et désactivation de l’équipement.

- **Tiles**

  - Si la box n'est plus compatible avec cette fonction :
      - Désactivation de l'équipement
      - Suppression CRON GLOBAL titles

# 02/03/2024

- Amélioration LOG pour 4.4