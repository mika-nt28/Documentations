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
> **Il est nécessaire d'avoir la Freebox Serveur en version 4.2 pour que le plugin fonctionne**

Les informations disponibles de votre Freebox Serveur sur Jeedom sont :

- **Les informations système :**
  - Couper le wifi
  - Redémarrer votre Freebox
  - Les débits internet
  - L'état de votre connexion
  - Gestion du filtrage des appels
- **Téléphone :**
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
  > Si les droits sont OK, le bouton va disparaitre
  > Les droits obligatoires sont en gras

<p><img src="../images/Freebox_OS_screenshot5.png" alt="Authentification 4" width="300" /></p>

## Lier les pièces Freebox avec les Objets Jeedom

> Cette fenêtre n'apparait uniquement que si la Freebox est une DELTA

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

<p><img src="../images/freebox_para.png" alt="MParamètres de la Freebox" width="60" /></p>

- Ouvrir la gestion des accès de la Freebox _(ce réglage se trouve dans le mode avancé)_

<p><img src="../images/freebox_gestion_acces_1.png" alt="Paramètres de gestion des accès de la Freebox" width="600" /></p>

- Cliquer sur l'onglet **Applications**
- Dans la liste, choisir l'Application déclarée lors de l'installation du Plugin _(par défaut : Jeedom Core)_

<p><img src="../images/freebox_gestion_acces_2.jpg" alt="Paramètres de gestion des accès de la Freebox" width="600" /></p>

- **Autoriser tous les droits d'accès**

<p><img src="../images/modification_droit.png" alt="Modification des droits d'accès spécifiques" width="600" /></p>

# Les équipements standards

Cliquer sur le bouton **_Scan équipements standards_**, le plugin va créer les différents équipements standards de la Freebox.

<p><img src="../images/recherche_systeme.png" alt="Recherche des équipements systèmes" width="60" /></p>

Les équipements et les commandes suivants vont être créés :

- **Air Média**
  - Player actuel AirMedia
  - AirMedia Start
  - AirMedia Stop
- **Appareils connectés**
  - Ensemble des appareils connectés à la Freebox
  - Possibilité d'utiliser la commande **_Wake on LAN_** uniquement par scénario
- **Disques**
  - Occupation du disque
- **Freebox Débits**
  - Freebox rate down
  - Freebox rate up
  - Freebox bandwidth up
  - Freebox bandwidth down
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
- **Téléphone**
  - Nombre Appels Manqués / Reçus / Passés
  - Liste Appels Manqués / Reçus / Passés
- **Téléchargements**
  - Nombre de tâches
  - Nombre de tâches actives
  - Nombre de tâches en extraction
  - Nombre de tâches en réparation
  - Nombre de tâches en vérification
  - Nombre de tâches en attente
  - Nombre de tâches en erreur
  - Nombre de tâches stoppées
  - Nombre de tâches terminées
  - Téléchargement en cours
  - Vitesse réception
  - Vitesse émission
  - Start DL
  - Stop DL
- **Wifi**
  - Statut du wifi
  - Wifi On
  - Wifi Off
  - Gestion du filtrage des appels

# Spécificité de Home Adapters (Uniquement Freebox Delta), Appareils connectés, Disque Dur et système

Ces quatre équipements sont vides par défaut lors de leur création sauf pour le système qui intègre les infos communes à toutes les Freebox.

Ouvrir chaque équipement et cliquer sur le bouton "Rechercher"

> Le plugin recherchera et créera les différentes commandes associées

<p><img src="../images/recherche_commandes.png" alt="Recherche des équipements spécifiques" width="800" /></p>

# Le contrôle parental

Cliquer sur le bouton **_Scan Contrôle parental_**, le plugin va créer les différents équipements système de la Freebox.

> Ces contrôles ont été implantés avec la version 4.2 de la Freebox.

<p><img src="../images/recherche_parental.png" alt="Recherche des contrôles parentaux" width="60" /></p>

Les équipements et les commandes suivants vont être créés :

- Etat
- Bloquer
- Autoriser
- Bloquer 30min/1h/2h

# Gérer le filtrage des adresses MAC

Cette gestion se fait uniquement par scénario

<p><img src="../images/add_dell_mac_filtrage.png" alt="Recherche des équipements spécifiques" width="800" /></p>

- Adresse Mac : indiquer l'adresse mac de l'appareil
- Méthode : sélectionner la méthode
  > - **Ajout**
  > - **Supprimer**
- Type de filtrage : sélectionner le filtre
  > - **Liste blanche**
  > - **Liste noire**
- Commentaires

> **A savoir** : l'appareil n'est pas automatiquement supprimer d'une liste si un changement de type de filtrage est fait.

# Fonction Wake on LAN

Cette gestion se fait par la modale depuis le widget des appareils connectés ou depuis un scénario.

<p><img src="../images/wakeonlan.png" alt="Recherche des équipements spécifiques" width="800" /></p>

- Adresse Mac : indiquer l'adresse mac de l'appareil
- Mot de Passe : indiquer le mot de passe
  > Si pas de mot de passe, laisser la case vide

# Freebox Delta

> La Freebox Delta permet d'avoir un pack de sécurité ainsi que la connexion avec certains équipements.

Cliquer sur le bouton **_Scan Tiles_**,les équipements et les commandes des différents équipements connectés vont être créés

<p><img src="../images/recherche_tiles.png" alt="Recherche des équipements spécifiques Freebox delta" width="60" /></p>

## Statut Alarme

> Le plugin remonte l'état de l'alarme par la commande "Etat de l alarme"

![Temps de rafraichissement](../images/alarme_statut.png)
Les valeurs possibles sont :

- **idle** = Alarme désactivée
- **alarm_1_arming** = L'alarme principale est activée, c'est un compte à rebours lorsque seuls les capteurs ne se trouvant pas dans la zone peuvent déclencher l'alerte
- **alarm_2_arming** = L'alarme partielle est activée, c'est un compte à rebours lorsque seuls les capteurs ne se trouvant pas dans la zone peuvent déclencher l'alerte
- **alarm_1_armed** = Alarme totale activée
- **alarm_2_armed** = Alarme partielle activée
- **alarm1_alert_timer** = L'alarme principale a été déclenchée par un capteur dans le fuseau horaire et la sirène sonnera après un compte à rebours
- **alarm2_alert_timer** = L'alarme de nuit a été déclenchée par un capteur dans le fuseau horaire et la sirène sonnera après un compte à rebours
- **alert** = La sirène sonne

> le système d'alarme est compatible avec Homebridge et l'application mobile : aucune configuration n'est à faire.
> Pour permettre l'intégration, des commandes d'infos ont été ajoutées pour permettre d'interagir avec le plugin Alarme.
>
> - **Actif** = Info Binaire (1 = Alarme Activée)
> - **Statut** = Info Binaire (1 = Sirène active)

![Temps de rafraichissement](../images/alarme_dashboard.png)

## Statut de la télécommande

> Le plugin remonte l'historique de la télécommande, il affichera la dernière action faite par la télécommande.

> Les valeurs possibles sont :

- **null** ou **0** = Aucun état
- **1** = Alarme principale
- **2** = Désactivation
- **3** = Alarme secondaire

## Les caméras

> les caméras sont créées, avec votre accord, dans le plugin caméra, si celui-ci est installé.

![Recherche des équipements spécifique Freebox delta](../images/msg_camera.png)

> La caméra ne sera pas visible dans le plugin Freebox.
> Si le message n'apparait pas, vérifier les droits sur l'OS de la Freebox

# Temps de rafraichissement (cron) des équipements

Il est possible de modifier le cron de rafraichissement de chaque équipement, par défaut :

- Home Adapter, FREEBOX - Télécommande (Alarme), Contrôle parental et Mes équipements sauf disque Dur = **Cron réglé à 5 minutes**
- Disque Dur = **Cron réglé à 1 heure**
- Ensemble des Tiles sauf FREEBOX - Télécommande (Alarme) = **Cron réglé à 1 minute**

> Ce cron permet de rafraichir les différentes commandes de type infos, l'équipement est actualisé automatiquement en cas d'action d'une commande.
> Les commandes d'action ne sont pas concernées par ce cron.

> Plus le temps est court, plus il y aura de la charge sur la CPU de la Freebox.

<p><img src="../images/cron.png" alt="Temps de rafraichissement" width="800" /></p>

# Les tiles

> Chaque équipement n'est pas forcement intégré dans le système vue l'évolution de la Freebox

Afin de pouvoir intégrer les nouveaux systèmes.

- Mettre le plugin en mode débug
- Redémarrer le Démon
- Faire **_Scan des tiles_**

Ouvrir un sujet (si aucun sujet ne traite pas déjà cette demande) sur le community et fournir les infos suivantes

- Faire une copie d'écran de l'équipement
<p><img src="../images/tiles1.png" alt="Equipement tiles 1" width="800" /></p>

- Faire une copie d'écran des commandes de l'équipement
<p><img src="../images/tiles2.png" alt="Equipement tiles 2" width="800" /></p>

- Fournir les logs sous forme de texte et non une copie d'écran
  > [Voir le paragraphe **11** Formatez correctement](https://community.jeedom.com/t/comment-nous-aider-a-vous-aider-ou-comment-poser-une-bonne-question/34932)

```
    [2020-08-24 07:37:41][DEBUG] : ┌───────── Commande trouvée pour l'équipement FREEBOX : FREEBOX - Eclairage Canapé -- Pièce : Salon (Node ID 9)
[2020-08-24 07:37:41][DEBUG] : │ Label : Enclenché -- Name : switch_state
[2020-08-24 07:37:41][DEBUG] : │ Type (eq) : light -- Action (eq): intensity_picker
[2020-08-24 07:37:41][DEBUG] : │ Index : 0 -- Value Type : bool -- Access : rw
[2020-08-24 07:37:41][DEBUG] : │ Valeur actuelle :
[2020-08-24 07:37:41][DEBUG] : │ Range : ----- -- Range color : -
[2020-08-24 07:37:41][DEBUG] : │ Name: Etat -- Type : info -- LogicalID : 0 -- Template Widget / Ligne : core::light/0-- Type de générique : LIGHT_STATE -- Inverser : 0 -- Icône :  -- Min/Max : default/default
[2020-08-24 07:37:41][DEBUG] : │ No Repeat pour l'info avec le nom : Etat
[2020-08-24 07:37:41][DEBUG] : │ Name: On -- Type : action -- LogicalID : PB_On -- Template Widget / Ligne : core::light/1-- Type de générique : LIGHT_ON -- Inverser : 0 -- Icône :  -- Min/Max : default/default
[2020-08-24 07:37:41][DEBUG] : │ Name: Off -- Type : action -- LogicalID : PB_Off -- Template Widget / Ligne : core::light/0-- Type de générique : LIGHT_OFF -- Inverser : 0 -- Icône :  -- Min/Max : default/default
[2020-08-24 07:37:41][DEBUG] : └─────────
[2020-08-24 07:37:41][DEBUG] : ┌───────── Commande trouvée pour l'équipement FREEBOX : FREEBOX - Eclairage Canapé -- Pièce : Salon (Node ID 9)
[2020-08-24 07:37:41][DEBUG] : │ Label : Luminosité -- Name : luminosity
[2020-08-24 07:37:41][DEBUG] : │ Type (eq) : light -- Action (eq): intensity_picker
[2020-08-24 07:37:41][DEBUG] : │ Index : 2 -- Value Type : int -- Access : rw
[2020-08-24 07:37:41][DEBUG] : │ Valeur actuelle : 254
[2020-08-24 07:37:41][DEBUG] : │ Range : ----- -- Range color : -
[2020-08-24 07:37:41][DEBUG] : │ Name: Etat Luminosité -- Type : info -- LogicalID : 2 -- Template Widget / Ligne : /0-- Type de générique : LIGHT_COLOR -- Inverser : 0 -- Icône :  -- Min/Max : 0/255
[2020-08-24 07:37:41][DEBUG] : │ No Repeat pour l'info avec le nom : Etat Luminosité
[2020-08-24 07:37:41][DEBUG] : │ Name: Luminosité -- Type : action -- LogicalID : 2 -- Template Widget / Ligne : default/0-- Type de générique : LIGHT_SET_COLOR -- Inverser : 0 -- Icône :  -- Min/Max : 0/255
[2020-08-24 07:37:41][DEBUG] : └─────────
```

# Troubleshotting

**Je n'ai pas le message d'autorisation qui apparait sur la Freebox**

> Vérifier dans les réglages de l'OS de la Freebox que le paramètre **Permettre les nouvelles demandes d'associations** est coché _(Paramètres de la Freebox -> Gestion des accès -> Onglet paramètres)_

![Association](../images/freebox_association.png)

**Je n'ai pas le niveau de batterie sur le capteur de présence de la Freebox et/ou sur la télécommande**

> - ces infos ne sont pas remontées à la Freebox donc impossible de les avoir dans Jeedom.
> - Elles ne sont donc pas disponibles sur la page santé (il est indiqué secteur ou N/A)

**Je ne peux pas commander la sirène de l'alarme de la Freebox**

> Il n'est pas possible de commander directement cette sirène
> [Voir Bugtracker Freebox FS#30650](https://dev.freebox.fr/bugs/task/30650)

**J'ai le message "Version d’API inconnue"**

> Le micrologiciel de la Freebox doit être au minimun en version 4.2.x.

**J'ai le message "unknown host, use ip address or mafreebox.freebox.fr" et le Demon NOK**

> Suite à la mise à jour de la Freebox 4.2.3
>
> Free a changé l'adresse de la Freebox **_mafreebox.free.fr_**, celle-ci ne fonctionne plus il faut remplacer par **_mafreebox.freebox.fr_**
>
> Voir le paragraphe **Installation et Configuration**

**J'ai le widget des appareils connectés qui n'est plus disponible**

- Le widget a été renommé lors de la dernière mise à jour

  > Il faut faire une **recherche des équipements supplémentaires** pour avoir le nouveau widget

**J'ai les messages suivants qui apparaissent "Missing device_name" ou "Votre Jeedom n'a pas de Nom, il est impossible de continuer" lors de l'appairage**

- Votre Jeedom n'a pas de Nom

  > Il est impératif que votre Jeedom soit nommé pour continuer l'appairage du plugin avec votre Freebox
  >
  > Se rendre dans Réglages -> Système -> Configuration -> onglet Général et mettre un nom

  > Recommencer ensuite l'authentification en n'oubliant pas de faire un reset de la configuration

  > <p><img src="../images/nom_jeedom_1.png" alt="Missing device_name" width="800" /></p>

  > <p><img src="../images/nom_jeedom_2.png" alt="Nom Jeedom" width="800" /></p>

**J'ai le messages suivant qui apparait "API incorrecte"**

> **Il est nécessaire d'avoir la Freebox en version 4.2 minimum pour que le plugin fonctionne**

**Erreur CronDaily avec des noms d'appareils avec des icônes**

> Il ne faut pas que les noms d'appareils comportent des icônes.
