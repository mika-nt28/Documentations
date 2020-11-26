---
layout: default
title: SPA Balboa (balboa)
lang: fr_FR
pluginId: balboa
---

# Description

Ce plugin a pour objet de connecter Jeedom à vos SPA __balboa__.

# Configuration


## Ajout d'un SPA

Rendez-vous sur la pages de configuration du plugin Plugins => Confort => SPA Balboa
Comme partout dans jeedom vous avez le bouton "Ajouter" qui vas vous crée votre équipement

* Nom de l'équipement : Nom saisi lors de la création de l'equipement, mais peut être encore modifié
* Adresse IP de l'equipement : Adresse IP du module wifi de votre SPA
* Objet parent : Objet Jeedom associé à votre SPA
* Catégorie : choisissez la catégorie dans laquelle vous souhaiter regrouper votre SPA
* Etat du widget : Paramètre de visibilité et d'activation de votre equipement
* Unité de temps : Ce paramètre permet de configurer votre SPA Balboa et synchronise l'heure de jeedom et du SPA
* Unité de température : Ce paramètre permet de configurer votre SPA Balboa

![Page de configuration d'un SPA](../images/balboa_screenshot_Equipement.jpg)

## Création de mode de fonctionnement

Pour automatiser plus facilement notre SPA, le plugin propose la création de mode.
Il est possible d'ajouter autant de mode que l'on souhaite.

![Création d'un mode pour notre SPA](../images/balboa_screenshot_Mode.jpg)

Pour chaque mode, il est possible de le conditionner, c'est à dire de définir des conditions pour lequel on autorise l'exécution du mode.
Chaque condition peut être activé ou non.
Nous pouvons autoriser le plugin à surveiller que nos conditions soient réunies pour exécuter automatiquement le mode, si le champs *Activer si condition vrai* est coché

Pour chaque mode on vient déterminer les actions sur notre SPA

* Température de consigne du SPA
* Activation de la pompe 1 du SPA
* Activation de la pompe 2 du SPA

Les mode peuvent être déclenché par :
* Ses condition si le champs *Activer si condition vrai* est coché
* Gere en externe par jeedom grâce à la commande *Mode actif / Mode du SPA*

## Programmation hebdomadaire des filtrations

La gestion de votre SPA est capable en toute autonomie de gère automatiquement les filtrations quotidien.
Dans cette partie je vous propose de programmer la filtration hebdomadaire.

![Page de configuration de la filtration hebdomadaire d'un SPA](../images/balboa_screenshot_Filtration.jpg)

Pour ajouter un créneaux, vous cliquer et glisser vers la fin du créneaux
> seul 2 créneaux sont autoriser

> Pour supprimer un créneaux, utiliser le clic droit

# Commandes

Voici toute les commandes qui sont automatiquement crée lors de l'ajout d'un SPA

* Température : Température actuel de l'eau de votre SPA
* Consigne / Etat Consigne : Consigne de chauffage actuel de votre SPA
* Range / Etat Range : Limite de consigne de température de votre SPA
* Etat chauffage : Etat du réchauffeur d'eau
* Temps de chauffage : Temps estimé pour une chauffe complète
* Mode de chauffage / Etat Mode de chauffage : type de chauffage
* Eclairage / Etat éclairage : Activation et état de l'éclairage de votre SPA
* Blower / Etat Blower : Activation et état du blower de votre SPA
* Pompe 1 / Etat Pompe 1 : Activation et état de la pompe 1 de votre SPA
* Pompe 2 / Etat Pompe 2 : Activation et état de la pompe 2 de votre SPA
* Etat Pompe de circulation : Activation et état de la pompe de circulation de votre SPA
* Mode actif / Mode du SPA : Activation et état des mode de votre SPA
* Priming: Flag d'amorçage de la pompe

# FAQ

