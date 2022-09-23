---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Description

Ce plugin permet de récupérer les informations de votre FreeboxOS (Serveur Freebox Révolution ou 4K ou DELTA ou POP).

> Toutes les infos ne sont pas encore disponibles pour la Freebox POP
>
> **Il est nécessaire d'avoir la Freebox Serveur en version 4.3 pour que le plugin fonctionne**

Les informations disponibles de votre Freebox Serveur sur Jeedom sont :

- **Les informations système :**
  - Couper le wifi
  - Redémarrer votre Freebox
  - Les débits internet
  - L'état de votre connexion
  - Gestion du filtrage des appels
- **Téléphone :** sur les dernieres 24h
  - Le nombre d'appels en absence
  - Le nombre d'appels passés
  - Le nombre d'appels reçus
- **Disque Dur :**
  - La place disponible dans vos disques connectés à la Freebox Serveur.
- **Appareils connectés sur le LAN et le Wifi Invité:**
  - L’état de chaque équipement DHCP
  - Possibilité d'utiliser la commande **_Wake on LAN_** uniquement par scénario
- **Domotique (uniquement pour la DELTA) :**
  - Récupère les infos de la maison connectée

# Installation et Configuration

Une fois le plugin installé et actif, aucune configuration n'est nécessaire.

# Appairage (Authentification)

Il faut se rendre dans la page principale du plugin et cliquer

<p><img src="../images/appairage.png" alt="Modale Appairage" width="60" /></p>

Il faut ensuite suivre les différents écrans pour valider l'appairage

<p><img src="../images/Freebox_OS_screenshot2.png" alt="Authentification 1" width="300" /></p>

## Réglages

Dans la fenêtre ci-dessous, il est possible de modifier

- **IP Freebox** : Adresse de connexion de la Freebox _(par défaut : mafreebox.freebox.fr)_
- **Nom de l'équipement connecté** : Le nom de la Jeedom (ce champ est verrouillé)
- **Ajouter automatiquement les équipements détectés dans :** : Indiquer la pièce par défaut
- Il est possible de cliquer sur le bouton **Reset configuration** pour avoir les paramètres par défaut
- Ne pas oublier de cliquer sur **Sauvegarder**

> Il est impératif que votre Jeedom soit nommé pour continuer l'appairage du plugin avec votre Freebox

<p><img src="../images/Freebox_OS_screenshot3.png" alt="Authentification 2" width="300" /></p>

## Authentification

Dans la fenêtre ci-dessous, il va être réalisée l'authentification sur la Freebox

- Cliquer sur le bouton **Lancement de l'Authentification**
- Suivre à la fois les identifications sur cet écran ainsi que sur la Freebox

<p><img src="../images/Freebox_OS_screenshot4.png" alt="Authentification 3" width="300" /></p>

## Vérification des droits

Dans la fenêtre ci-dessous, Le système va contrôler les droits qui sont attribués à l'application

- Voir la section des Droits d'accès (dans cette documentation) pour modifier les droits sur la Freebox
- Une fois les droits réglés, cliquer sur le bouton **Vérification des droits**
  > Si les droits sont OK, le bouton va **suivant** deviendra visible
  > Les droits obligatoires sont en gras

<p><img src="../images/Freebox_OS_screenshot5.png" alt="Authentification 4" width="300" /></p>

## Lier les pièces Freebox avec les Objets Jeedom

> Cette fenêtre n'apparait uniquement que si la Freebox est une DELTA
>
> Il est possible d'activer ou désactiver le cron "Actualisation Globale des Tiles"
>
> <b>Ne pas oublier</b> de cliquer sur sauvegarder pour prendre en compte les changements

<p><img src="../images/Freebox_OS_screenshot6.png" alt="Authentification 4" width="300" /></p>

## Scan

Dans la fenêtre ci-dessous, Il est possible de lancer le scan des différents équipements.

<p><img src="../images/Freebox_OS_screenshot7.png" alt="Authentification 5" width="300" /></p>

## Authentification terminée

L'authentification est réussie.

<p><img src="../images/Freebox_OS_screenshot8.png" alt="Authentification 6" width="300" /></p>

# Droits d'accès

Certains droits d'accès supplémentaires sont nécessaires pour l'utilisation du plugin, ils doivent être **obligatoirement attribués et modifiés** directement depuis l'OS de la Freebox

- Se connecter à l'interface de la Freebox (http://mafreebox.freebox.fr)
- Ouvrir les paramètres de la Freebox

<p><img src="../images/freebox_para.png" alt="Paramètres de la Freebox" width="100" /></p>

- Ouvrir la gestion des accès de la Freebox _(ce réglage se trouve dans le mode avancé)_

<p><img src="../images/freebox_gestion_acces_1.png" alt="Paramètres de gestion des accès de la Freebox" width="600" /></p>

- Cliquer sur l'onglet **Applications**
- Dans la liste, choisir l'Application déclarée lors de l'installation du Plugin _(par défaut : Plugin Freebox OS)_

<p><img src="../images/freebox_gestion_acces_2.jpg" alt="Paramètres de gestion des accès de la Freebox" width="500" /></p>

- **Autoriser tous les droits d'accès**

<p><img src="../images/modification_droit.png" alt="Modification des droits d'accès spécifiques" width="500" /></p>

# Les équipements standards

Cliquer sur le bouton **_Scan équipements standards_**, le plugin va créer les différents équipements standards de la Freebox.

<p><img src="../images/recherche_systeme.png" alt="Recherche des équipements systèmes" width="60" /></p>

Les équipements et les commandes suivants vont être créés :

- **Air Média**
  - Player actuel AirMedia
  - AirMedia Start
  - AirMedia Stop
- **Appareils connectés** et **Appareils connectés Wifi Invité**
  - Ensemble des appareils connectés à la Freebox
  - Possibilité d'utiliser la commande **_Wake on LAN_** uniquement par scénario
- **Disque Dur**
  - Occupation du disque
- **Freebox Débits**
  - Freebox rate down, rate up, bandwidth up, bandwidth down
  - Freebox media
  - Freebox state
- **Player**
  - Mac
  - Type
  - Modèle
  - Version
  - API disponible
  - Disponible sur le réseau
  - Etat (allumé ou éteint)
    > La commande est créée uniquement si le player renvoie son état.
    > Il faut absolument que le player soit sous tension et pas en veille prolongée. (Révolution)
    > Les Player mini4K ne sont pas compatibles, les players POP ne sont pas encore compatibles.
- **Partage Windows - Mac**
  - Activer / Désactiver le Partage de fichiers Mac, Windows, FTP
  - Activer / Désactiver le Partage Imprimante (disponible uniquement si SMBv2 n'est pas actif)
- **Système**
  - Update
  - Reboot
  - Freebox firmware version
  - Mac
  - Vitesse ventilateur
  - Températures _(temp sw, temp cpub, temp cpum)_
  - Allumée depuis
  - board name
  - serial
  - 4G si la carte est présente dans la Freebox
- **Téléphone** sur les dernieres 24h
  - Nombre Appels Manqués / Reçus / Passés
  - Liste Appels Manqués / Reçus / Passés
- **Téléchargements**
  - Nombre de tâches
  - Nombre de tâches actives, en extraction, en réparation, en vérification, en attente, en erreur, stoppées, terminées
  - Téléchargement en cours
  - Vitesse réception, émission
  - Start, Stop
- **VM** (uniquement pour les freebox compatible)
  - Statut
  - Action possible : Stop, Redémarrer, Start
  - info : Nb de CPU, Adresse Mac, Mémoire, Port USB, Ecran Virtuel, Type de Disque
- **Wifi**
  - Statut du wifi
  - Wifi On Off
  - Gestion du filtrage des appels


# Gestion réseau

Cet équipement permet de :

> - Attribuer une adresse IP fixe
> - Gérer le filtrage des addresses MAC
> - Fonction Wake on LAN

<p><img src="../images/Modif_equip_IP.png" alt="Modification des équipements" width="800" /></p>

- Sélectionner l'appareil connecté : Choisir par mis la liste le nom de l'équipement
- Sélection modification Appareil : Sélectionner la modification voulue

  > - **Ajouter IP fixe**
  > - **Supprimer IP fixe**
  > - **Modifier l'équipement**
  > - **Modifier le type de périphérique**
  > - **Modifier l'équipement**
  > - **Ajouter Liste noire Wifi**
  > - **Ajouter Liste blanche Wifi**
  > - **Supprimer Liste noire Wifi**
  > - **Supprimer Liste blanche Wifi**
  > - **Modifier Liste noire Wifi**
  > - **Modifier Liste blanche Wifi**
  > - **Wake on LAN**

- Choix IP : Indiquer l'adresse IP de l'appareil
- Sélection Nom Appareil : Indiquer le nom de l'appareil
- Commentaires : permet de saisir soit un commentaire ou un mot de passe
- Sélection Type de périphérique : Sélectionner le type de périphérique
- Modifier l'appareil : Permet d'envoyer la modification sur la freebox

## Attribuer une adresse IP ou changer le type de périphérique

Il faut avoir les valeurs les champs suivants renseignés

- Sélectionner l'appareil connecté
- Sélection modification Appareil avec une valeur suivante

  > - **Ajouter IP fixe**
  > - **Supprimer IP fixe**
  > - **Modifier l'équipement**
  > - **Modifier le type de périphérique**
  > - **Modifier l'équipement**

- Choix IP : Indiquer l'adresse IP de l'appareil
- Sélection Nom Appareil : Indiquer le nom de l'appareil
- Commentaires : permet de saisir un commentaire
- Sélection Type de périphérique : Sélectionner le type de périphérique
- Modifier l'appareil : Permet d'envoyer la modification sur la freebox

## Gérer le filtrage des adresses MAC

<p><img src="../images/Modif_equip_filtrage.png" alt="Modification des équipements" width="800" /></p>

Il est possible de faire cela avec les commandes depuis les équipements appareils connectés ou wifi
Il faut avoir les valeurs les champs suivants renseignés

- Sélectionner l'appareil connecté
- Sélection modification Appareil avec une valeur suivante

  > - **Ajouter Liste noire Wifi**
  > - **Ajouter Liste blanche Wifi**
  > - **Supprimer Liste noire Wifi**
  > - **Supprimer Liste blanche Wifi**
  > - **Modifier Liste noire Wifi**
  > - **Modifier Liste blanche Wifi**

- Commentaires : permet de saisir un commentaire ou un mot de passe
- Modifier l'appareil : Permet d'envoyer la modification sur la freebox

> **A savoir** : l'appareil n'est pas automatiquement supprimer d'une liste si un changement de type de filtrage est fait.

## Fonction Wake on LAN

<p><img src="../images/Modif_equip_wol.png" alt="Modification des équipements" width="800" /></p>

- Sélectionner l'appareil connecté
- Sélection modification Appareil avec une valeur suivante

  > - **Wake on LAN**

  - Commentaires : permet de saisir un mot de passe
  - Modifier l'appareil : Permet d'envoyer la modification sur la freebox

Cette gestion se fait par la modale depuis le widget des appareils connectés ou depuis un scénario.
