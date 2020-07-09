---
layout: default
title: EIB / KNX (eibd)
lang: fr_FR
pluginId: eibd
---

# Stable
## 16/06/2020
* Ajout de log pour l'identification du plantage de demon lorsque les flag sont mauvais
* Ajout d'un test si FlagWrite actif on renvoie l'info contenue dans jeedom plutot que d'interroger le bus

## 29/04/2020
* Mise a jours du Template Lumière avec l'ajout des widgets standard

## 15/04/2020
* Branche d'installation du GitHub de knxd remplacé

## 03/04/2020
* Séparation de la documentation

## 17/03/2020
* Correction valeur de sous-type automatique, lors d'une création automatique de commande, si le dpt n'est pas configuré sous jeedom
* Synonyme anglais sur les Templates
* Ajout de la catégorie sur les Templates
* Correction bug création automatique unitaire des objets
* Recherche des gad dans les groupes de la vue bâtiment
* Bugfix DPT 19.xxx

## 13/12/2019
* BugFix : ***erreur : Call to a member function getHumanName() on null***

## 11/12/2019
* Refonte de moteur de Template pour simplifier la maintenance
* Ajout du Template AireZone
* Correction de bug
* Initialisation des valeur a la sauvegarde (si FlagInit est actif)
* Ajout d'une vue liste pour simplifier la configuration de base

# Beta
## 09/07/2020
* BugFix recherche maximal de level sur l'autocreate

# Prochainement
* Recherche des objets existants sur la creation manuel pour mise a jours en arboressance
* Mise a jours des arboressance d'objet en creation manuel
* Ajout d'un systeme de parse manuel pour la creation des equipement Template dans l'arboressance
