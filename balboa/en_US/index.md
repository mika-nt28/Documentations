Description
====
Ce plugin a pour objet de connecter Jeedom à vos Sap __balboa__.

Configuration
=============

Ajout d'un SPA
---------------

Rendez vous sur la pages de configuration du plugin Plugins => Confort => SPA Balboa
Comme partout dans jeedom vous avez le bouton "Ajouter" qui vas vous cree votre equipemnet

* Nom de l'équipement : Nom saisi lors de la creation de l'equipement, mais peut etre encore modifié
* Adresse IP de l'equipement : Adresse IP du module wifi de votre SPA
* Objet parent : Objet Jeedom associé a votre SPA
* Catégorie : choisissez la categorie dans laquel vous souhaiter regrouper votre SPA
* Etat du widget : Parametre de visibilité et d'activation de votre equipement
* Unité de temps : Ce parametre permet de configurer votre SPA Balboa et synchronise l'heure de jeedom et du SPA
* Unité de température : Ce parametre permet de configurer votre SPA Balboa

![Page de configuration d'un SPA](../images/balboa_screenshot_Equipement.jpg)   

Creation de mode de fonctionnement
----------------------------------

Pour automatiser plus facilement notre SPA, le plugin propose la creation de mode.
Il est possible d'ajouter autant de mode que l'on souhaite.

![Creation d'un mode pour notre SPA](../images/balboa_screenshot_Mode.jpg)  

Pour chaque mode, il est possible de le conditionner, c'est a dire de definir des conditions pour lequel on autorise l'execution du mode.
Chaque condition peut etre activé ou non.
Nous pouvons autoriser le plugin a surveiller que nos conditions soit reunis pour executer automatiquement le mode, si le champs *Activer si condition vrai* est coché

Pour chaque mode on vient determiner les actions sur notre SPA

* Température de consigne du SPA 
* Activation de la pompe 1 du SPA
* Activation de la pompe 2 du SPA

Les mode peuvent etre declanché par : 
* Ses condition si le champs *Activer si condition vrai* est coché
* Gere en externe par jeedom grace a la commande *Mode actif / Mode du SPA*

Programmation hebdomadaire des filtrations
-------------------------------------------

La gestion de votre SPA est capable en toute autonomie de gere automatiquement les filtrations quotidien.
Dans cette partie je vous propose de programmer la filtration hebdomadaire.

![Page de configuration de la filtration hebdomadaire d'un SPA](../images/balboa_screenshot_Filtration.jpg) 

Pour ajouter un crenaux, vous cliquer et glisser vers la fin du crenaux
> seul 2 crenaux sont autoriser

> Pour supprimer un crenaux, utiliser le clique droit

Commandes
=========

Voici toute les commandes qui sont automatiquement cree lors de l'ajout d'un SPA

* Température : Temperature actuel de l'eau de votre SPA
* Consigne / Etat Consigne : Consigne de chauffage actuel de votre SPA
* Range / Etat Range : Limite de consigne de température de votre SPA
* Etat chauffage : Etat du rechauffeur d'eau
* Temps de chauffage : Temps estimé pour une chauffe complete
* Mode de chauffage / Etat Mode de chauffage : type de chauffage
* Eclairage / Etat éclairage : Activation et etat de l'eclairage de votre SPA
* Blower / Etat Blower : Activation et état du blower de votre SPA
* Pompe 1 / Etat Pompe 1 : Activation et état de la pompe 1 de votre SPA
* Pompe 2 / Etat Pompe 2 : Activation et état de la pompe 2 de votre SPA
* Etat Pompe de circulation : Activation et état de la pompe de circulation de votre SPA
* Mode actif / Mode du SPA : Activation et état des mode de votre SPA
* Priming: Flag d'ammorcage de la pompe

FAQ
===

Ici les reponses a vos questions
