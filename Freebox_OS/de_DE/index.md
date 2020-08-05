---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Description

Ce plugin permet de récupérer les informations de votre FreeboxOS (Serveur Freebox Révolution ou 4K ou DELTA).

Les informations disponibles de votre Freebox Serveur sur Jeedom sont :

- **Les informations système :**
  - Couper le wifi
  - Redémarrer votre Freebox
  - Les débits internet
  - L'état de votre connexion
- **Téléphone :**
  - Le nombre d'appels en absence
  - Le nombre d'appels passés
  - Le nombre d'appels reçus
- **Disque Dur :**
  - La place disponible dans vos disques connectés à la Freebox Serveur.
- **Appareils connectés :**
  - L’état de chaque équipement DHCP
- **Domotique (uniquement pour la DELTA) :**
  - Récupère les infos de la maison connectée

# Installation et Configuration

Sur la page de configuration du plugin, une fois le plugin installé et actif

Il est possible de personnaliser certaines options de connexion, **mais seules celles par défaut ont été validées**.

![Configuration Plugin](../images/plugin_configuration.png)

- **IP Freebox** : Adresse de connexion de la Freebox _(par défaut : mafreebox.freebox.fr)_
- **Id de l'application Freebox serveur** : Identifiant utilisé par la Freebox _(par défaut : fr.freebox.jeedom)_
- **Nom de l'application Freebox serveur** : Nom utilisé par la Freebox _(par défaut : Freebox OS For Jeedom)_
- **Version de l'application Freebox serveur** : Version de l'application utilisée par la Freebox _(par défaut : v1.0.0)_
- **Nom de l'équipement connecté** : Nom de l'équipement utilisé par la Freebox (par défaut : Jeedom Core)

- **Ajouter automatiquement les équipements détectés dans :** : Indiquer la pièce par défaut

> L'appairage doit être lancé après chaque sauvegarde de ces paramètres pour leur prise en compte.

# Appairage

- Cliquer sur le bouton **Appairage** dans l'interface de configuration.
  Le message ci-dessous apparait,

![Message Validation](../images/msg_validation.png)

> **Il ne faut pas cliquer tout de suite sur OK, il faut d'abord suivre les
> Indications de _Validation sur la Freebox_**

> Le plugin va demander une nouvelle connexion de type "API" à la Freebox

## Validation sur la Freebox

> L'opération suivante se fait directement sur l'écran de la Freebox

- **Suivre et valider** les différentes informations affichées sur la Freebox

![Écran Autorisation Application Freebox V4](../images/freebox_ecran.jpeg)

## Validation Jeedom

- Maintenant, cliquer sur le bouton **OK** du message dans le navigateur

> Le plugin va vérifier le fonctionnement de la liaison.

# Droits d'accès

Certains droits d'accès supplémentaires sont nécessaires pour l'utilisation du plugin, ils doivent être **obligatoirement attribués et modifiés** directement depuis l'OS de la Freebox

- Se connecter à l'interface de la Freebox (http://mafreebox.freebox.fr)
- Ouvrir les paramètres de la Freebox

![Paramètres de la Freebox](../images/freebox_para.png)

- Ouvrir la gestion des accès de la Freebox _(ce réglage se trouve dans le mode avancé)_

![Paramètres de gestion des accès de la Freebox](../images/freebox_gestion_acces_1.png)

- Cliquer sur l'onglet **Applications**
- Dans la liste, choisir l'Application déclarée lors de l'installation du Plugin _(par défaut : Jeedom Core)_

![Paramètres de gestion des accès de la Freebox](../images/freebox_gestion_acces_2.jpg)

- **Autoriser tous les droits d'accès**

![Modification des droits d'accès](../images/freebox_autorisation_acces_API.png)

# Les équipements système

Cliquer sur le bouton **_Scan équipements standards_**, le plugin va créer les différents équipements système de la Freebox.

![Recherche des équipements systèmes](../images/recherche_systeme.png)

Les équipements et les commandes suivants vont être créés :

- **Air Média**
  - Player actuel AirMedia
  - AirMedia Start
  - AirMedia Stop
- **Appareils connectés**
  - Ensemble des appareils connectés à la Freebox
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
  - Redirection de ports
  - 4G si la carte est présente dans la Freebox
- **Téléphone**
  - Nombre Appels Manqués / Reçus / Passés
  - Liste Appels Manqués / Reçus / Passés
- **Téléchargements**
  - Nombre de tâche(s)
  - Nombre de tâche(s) active(s)
  - Nombre de tâche(s) en extraction
  - Nombre de tâche(s) en réparation
  - Nombre de tâche(s) en vérification
  - Nombre de tâche(s) en attente
  - Nombre de tâche(s) en erreur
  - Nombre de tâche(s) stoppée(s)
  - Nombre de tâche(s) terminée(s)
  - Téléchargement en cours
  - Vitesse réception
  - Vitesse émission
  - Start DL
  - Stop DL
- **Wifi**
  - Statut du wifi
  - Active/Désactive le wifi
  - Wifi On
  - Wifi Off

# Spécificité de Home Adapters (Uniquement Freebox Delta), Appareils connectés, Disque Dur et système

Ces 4 équipements sont vides par défaut lors de leur création sauf pour le système qui intégre les infos communes à toutes les Freebox

Ouvrir chaque équipement et cliquer sur le bouton "Rechercher"

> Le plugin recherchera et créera les différentes commandes associées

![Recherche des équipements spécifique](../images/recherche_commandes.png)

# Le contrôle parental

Cliquer sur le bouton **_Scan Contrôle parental_**, le plugin va créer les différents équipements système de la Freebox.

> Ces contrôles ont été implantés avec la version 4.2 de la Freebox.

![Recherche des équipements systèmes](../images/recherche_parental.png)

Les équipements et les commandes suivants vont être créés :

- **Air Média**
  - Etat
  - Bloquer
  - Autoriser
  - Bloquer 30min/1h/2h

# Freebox Delta

> La Freebox Delta permet d'avoir un pack de sécurité ainsi que la connexion avec certains équipements.

Cliquer sur le bouton **_Scan Tiles_**,les équipements et les commandes des différents équipements connectés vont être créés

![Recherche des équipements spécifique Freebox delta](../images/recherche_tiles.png)

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
> Pour permettre l'intégration, des commandes d'infos ont été ajoutées pour permettre d'interagir avec le plugin Alarme
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

![Temps de rafraichissement](../images/cron.png)

# Troubleshotting

**Je n'ai pas le message d'autorisation qui apparait sur la Freebox**

![Écran Freebox V4](../images/freebox_ecran.jpeg)

> Vérifier dans les réglages de l'OS de la Freebox que le paramètre **Permettre les nouvelles demandes d'association** est coché*(Paramètres de la Freebox -> Gestion des accès -> Onglet paramètres)*

![Association](../images/freebox_association.png)

**Je n'ai pas le niveau de batterie sur le capteur de présence de la Freebox et/ou sur la télécommande**

> Ces infos ne sont pas remontées à la Freebox donc impossible de les avoir dans Jeedom.

**Je ne peux pas commander la sirène de l'alarme de la Freebox**

> Il n'est pas possible de commander directement cette sirène
> [Voir Bugtracker Freebox FS#30650](https://dev.freebox.fr/bugs/task/30650)

**J'ai le message "Version d’API inconnue"**

> Le micrologiciel de la Freebox doit être au minimun en version 4.2.x.

**J'ai le message "unknown host, use ip address or mafreebox.freebox.fr" et le Demon NOK**

> Suite à la mise à jour de la Freebox 4.2.3
>
> Free a changé l'’adresse de la Freebox **_mafreebox.free.fr_**, celle-ci ne fonctionne plus il faut remplacer par **_mafreebox.freebox.fr_**
>
> Voir le paragraphe **Installation et Configuration**
