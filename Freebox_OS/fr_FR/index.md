---
layout: default
title: Freebox OS (Freebox_OS)
lang: fr_FR
pluginId: Freebox_OS
---

# Description

Ce plugin permet de récupérer les informations de votre FreeboxOS (Serveur Freebox Révolution ou 4K ou DELTA).

Les informations disponibles de votre Freebox Serveur sur Jeedom sont:

* **Les informations système :**
    * Couper le wifi
    * Redémarrer votre Freebox
    * Les débits internet
    * L'état de votre connexion
* **Téléphone :**
    * Le nombre d'appels en absences
    * Le nombre d'appels passés
    * Le nombre d'appels reçus
* **Disque Dur :**
    * La place disponible dans vos disques connectés à la Freebox Serveur.
* **Réseau :**
    * L’état de chaque équipement DHCP
* **Domotique (uniquement pour la DELTA) :**
    * Récupère les infos de la maison connecté

# Installation et Configuration

Sur la page de configuration du plugin, une fois le plugin installé et actif

Il est possible de personnaliser certaines options de connexion, **mais seules celles par défaut ont été validées**.

![Configuration Plugin](../images/plugin_configuration.png)



* **IP Freebox** : Adresse de connexion de la Freebox *(par défaut : mafreebox.free.fr)*
* **Id de l'application Freebox serveur** : Identifiant utilisé par la Freebox *(par défaut : fr.freebox.jeedom)*
* **Nom de l'application Freebox serveur** : Nom utilisé par la Freebox *(par défaut : Freebox OS For Jeedom)*
* **Version de l'application Freebox serveur** : Version de l'application utilisé par la Freebox  *(par défaut : v1.0.0)*
* **Nom de l'équipement connecté** : Nom de l'équipement utilisé par la Freebox  (par défaut : Jeedom Core)

>L'appairage doit être lancé après chaque sauvegarde de ces paramètres pour leurs prises en compte.


# Appairage

* Cliquer sur le bouton **Appairage** dans l'interface de configuration.
Le message ci-dessous apparait,

![Message Validation](../images/msg_validation.png)

> **Il ne faut pas cliquer tout de suite sur OK, il faut d'abord suivre les
  Indications de *Validation sur la Freebox***

> Le plugin va demander d'une nouvelle connexion de type "API" à la Freebox

## Validation sur la Freebox

> L'opération suivante se fait directement sur l'écran de la Freebox

* **Suivre et valider** les différentes informations affichées sur la Freebox

![Écran Freebox V4](../images/freebox_ecran.jpeg)

## Validation Jeedom

* Maintenant, cliquer sur le bouton **OK** du message dans le navigateur

> Le plugin va vérifier le fonctionnement de la liaison.

# Droit d'accès

Certains droits d'accès supplémentaires sont nécessaires pour l'utilisation du plugin, ils doivent être **obligatoirement attribuer et modifier** directement depuis l'OS de la Freebox

* Se connecter à l'interface de la Freebox (http://mafreebox.free.fr)
* Ouvrir le paramètre Freebox

![Paramètres de la Freebox](../images/freebox_para.png)

* Ouvrir la gestion des accès de la Freebox *(ce réglage se trouve dans le mode avancé)*

![Paramètres de gestion des accès de la Freebox](../images/freebox_gestion_acces_1.png)

* Cliquer sur l'onglet **Applications**
* Dans la liste, choisir l'Application déclaré lors de l'installation du Plugin *(par défaut : Jeedom Core)*

![Paramètres de gestion des accès de la Freebox](../images/freebox_gestion_acces_2.jpg)

* **Autoriser tous les droits d'accès**

![Modification des droits d'accès](../images/freebox_autorisation_acces_API.png)

# Les équipements

Le plugin va automatiquement créer tous les équipements et les commandes dont il est capable d'exécuter ou de récupérer leurs informations.

* **ADSL**
    * Freebox rate down
    * Freebox rate up
    * Freebox bandwidth up
    * Freebox bandwidth down
    * Freebox media
    * Freebox state
* **Système**
    * Update
    * Reboot
    * Statut du wifi
    * Active/Désactive le wifi
    * Wifi On
    * Wifi Off
    * Freebox firmware version
    * Mac
    * Vitesse ventilateur
    * temp sw','temp_sw
    * Allumée depuis
    * board name
    * temp cpub
    * temp cpum
    * serial
    * Redirection de ports
* **Téléphone**
    * Nombre Appels Manqués
    * Nombre Appels Reçus
    * Nombre Appels Passés
    * Liste Appels Manqués
    * Liste Appels Reçus
    * Liste Appels Passés
    * Faire sonner les téléphones DECT
    * Arrêter les sonneries des téléphones DECT
* **Téléchargements**
    * Nombre de tâche(s)
    * Nombre de tâche(s) active
    * Nombre de tâche(s) en extraction
    * Nombre de tâche(s) en réparation
    * Nombre de tâche(s) en vérification
    * Nombre de tâche(s) en attente
    * Nombre de tâche(s) en erreur
    * Nombre de tâche(s) stoppée(s)
    * Nombre de tâche(s) terminée(s)
    * Téléchargement en cours
    * Vitesse réception
    * Vitesse émission
    * Start DL
    * Stop DL
* **AirPlay**
    * Player actuel AirMedia
    * AirMedia Start
    * AirMedia Stop

# Spécificité de Home Adapters (Uniquement Freebox Delta), Réseau et Disque Dur

Ces 3 équipements sont vides à la création par le plugin

Ouvrir chaque équipement et cliquer sur le bouton "Rechercher"
> Le plugin recherchera et créera les différentes commandes associées


![Recherche des équipements spécifique](../images/RechercheCommandes.jpg)


# Freebox Delta

> La Freebox Delta permet d'avoir un pack de sécurité ainsi que la connexion avec certain équipement.

Cliquer sur le bouton ***Rechercher les tiles***, le plugin va créer les différents équipements connectés à la Freebox Delta

![Recherche des équipements spécifique Freebox delta](../images/recherche_tiles.png)

## Statut Alarme
> Le plugin remonte l'état de l'alarme par la commande "info_État de lalarme"

![Temps de rafraichissement](../images/alarme_statut.png)
Les valeurs possibles sont :
* **idle** = Alarme désactivée
* **alarm_1_arming** = L'alarme principale est activée, c'est un compte à rebours lorsque seuls les capteurs ne se trouvant pas dans la zone peuvent déclencher l'alerte
* **alarm_2_arming** = L'alarme partielle est activée, c'est un compte à rebours lorsque seuls les capteurs ne se trouvant pas dans la zone peuvent déclencher l'alerte
* **alarm_1_armed** = Alarme totale activée
* **alarm_2_armed** = Alarme partielle activée
* **alarm1_alert_timer** = L'alarme principale a été déclenchée par un capteur dans le fuseau horaire et la sirène sonnera après un compte à rebours
* **alarm2_alert_timer** = L'alarme de nuit a été déclenchée par un capteur dans le fuseau horaire et la sirène sonnera après un compte à rebours
* **alert** = La sirène sonne

## Les caméras
> les caméras sont créées, avec votre accord, dans le plugin caméra, si celui-ci est installé.

![Recherche des équipements spécifique Freebox delta](../images/msg_camera.png)

> La caméra ne sera pas visible dans le plugin Freebox.
>
> Si le message n'apparait pas, vérifier les droits sur l'OS de la Freebox

# Récurrence de la mise à jour des équipements

Il est possible de modifier le temps de rafraichissement de chaque équipement. Par défaut, le temps est de 300s.
Plus le temps est cours, plus il y aura de la charge sur la CPU de la Freebox.

![Temps de rafraichissement](../images/Temps_de_rafraichissement.jpg)

# Troubleshotting

**Je n'ai pas le message d'autorisation qui apparait sur la Freebox**

![Écran Freebox V4](../images/freebox_ecran.jpeg)
>
>Vérifier dans les réglages de l'OS de la Freebox que le paramètre **Permettre les nouvelles demandes d'association** est coché*(Paramètres de la Freebox -> Gestion des accès -> Onglet paramètres)*

![Écran Freebox V4](../images/freebox_association.png)

**Je n'ai pas le niveau de batterie sur le capteur de présence de la Freebox**

>Ces infos ne sont pas remontés par le capteur à la Freebox

**Je ne peux pas commander la sirène de l'alarme de la Freebox**

>Il n'est pas possible de commander directement cette sirène [Voir Bugtracker Freebox FS#30650](https://dev.freebox.fr/bugs/task/30650)