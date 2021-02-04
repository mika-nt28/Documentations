---
layout: default
title: EIB / KNX (eibd)
lang: fr_FR
pluginId: eibd
---

# Stable
## 03/12/2020
* Bugfix "PHP Warning:  Illegal string offset 'id' in /var/www/html/plugins/eibd/core/class/eibd.class.php on line 864"
* Bugfix "PHP Warning:  Illegal string offset 'id' in /var/www/html/plugins/eibd/core/class/eibd.class.php on line 962"
* Bugfix DPT 18.001 avec la valeur 17

## 12/10/2020
* Ajout d'une condition de log level different de Aucun pour le log du demon

## 08/09/2020
* Ajout du Template Station Météo
* Ajout du paramètre de contrôle dpt 18.xxx

## 16/07/2020
* Bugfix nombre de level dans la création automatique
* Ajout du FT12cemi
* BugFix Création et affichage des objets automatiquement

## 16/06/2020
* Ajout de log pour l'identification du plantage de demon lorsque les flag sont mauvais
* Ajout d'un test si FlagWrite actif on renvoie l'info contenue dans jeedom plutot que d'interroger le bus

## 29/04/2020
* Mise à jours du Template Lumière avec l'ajout des widgets standard

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
## 04/02/2021
* Interdiction d'envoyer une requet si demon NOK
* Mise en place du temps d'attente entre 2 commande READ
* Bugfix retour d'etat en creation template dans arbo
* Ajout du parent dans la creation template dans l'arbo

## 21/01/2021
* Ajout du nom du nouvelle equipement dans la selection Template / Commande depuis l'arboressance
* Désactivation de l'option lorsque deja utilisé
* Bugfix Read d'un gad

## 14/01/2021
* Bugfix logique de selection Template / Commande depuis l'arboressance
* Bugfix flag initialisation

## 06/01/2021
* Mise a jours des droit sur le port USB au lancement du démon

## 19/12/2020
* Ajout d'un systeme de creation d'equipement par template depuis l'arboressance (fonctionnement inverse d'une creation par template)

# Prochainement
* Recherche des objets existants sur la creation manuel pour mise a jours en arboressance
* Prise en compte des spécifité du plugin lors de la duplication
