---
layout: default
title: Android TV (AndroidTV)
lang: fr_FR
pluginId: AndroidTV
---
# Description

Plugin permettant de piloter les terminaux android (TV, Shield, freebox mini 4k, Smartphone, etc..)

# Fonctions disponibles
Infos :
* nom de l'appareil
* état (allumé/éteint) (buggé pour l'instant)
* application en cours
* résolution
* version Android
* espace disque disponible
* status de lecture (play, pause, arrêt)
* nom du titre en cours de lecture

Actions :
* accueil, retour
* allumage, extinction
* volume+, volume-, slider volume
* haut, bas, gauche, droite
* clic, entrer
* démarrage, lecture, pause, arrêt
* précédent, suivant
* lancement des applications : Youtube, FranceTV, Plex, Spotify, VLC, TF1, Google, Facebook, Molotov, Netflix, etc.

Scénarios possibles :
* Allumer la box -> lancer Molotov -> lecture avec commande vocale Google Home/ifttt (ex: "OK Google, mets la télé en route").
* Commander l'allumage de l'ampli (Yamaha dans mon cas) lorsque la box est allumée (car parfois le HDMI CEC).
* Si Netflix lancé -> lumière salon à 50%

# Equipements testés
Actuellement le plugin a été vérifié sur les matériels suivants:
* Nvidia Shield (pas de configurations supplémentaires a effectuer).
* Oneplus 5t (pas de configurations supplémentaires à effectuer).
* Freebox mini 4k (pas de configurations supplémentaires à effectuer).
* Xiaomi Mibox TV (Le port 5555 servant à ADB n'est pas ouvert par défaut), il faut connecter la box en USB et lancer les commandes suivantes:
    - adb connect
    - adb tcpip 5555
    - adb connect 192.168.x.x:5555
    - débrancher le cable
* Samsung Galaxy (Le port 5555 servant à ADB n'est pas ouvert par défaut), il faut connecter la téléphone en USB et lancer les commandes suivantes:
    - adb connect
    - adb tcpip 5555
    - adb connect 192.168.x.x:5555
    - débrancher le cable
*  Lenovo Yoga 1 (pas de configurations supplémentaires a effectuer).


![Screenshot5](../images/Screenshot3.png)

Vous pouvez également changer la couleur du bandeau du bas ou le rendre transparent.

![Screenshot6](../images/Screenshot4.png)

# Prévisualisation

![Screenshot1](../images/Screenshot1.png)

![Screenshot2](../images/Screenshot2.png)

![Screenshot3](../images/Screenshot3.png)

![Screenshot4](../images/Screenshot4.png)

![Screenshot7](../images/Screenshot7.png)

# Configuration du plugin

Après téléchargement du plugin, il faut l’activer, celui-ci ne nécessite aucune autre configuration.

# Configuration des équipements

La partie configuration du plugin permet de :

* Renseigner l'adresse IP de l'équipement. (N'hésitez pas à utiliser l'assistant de configuration pour configurer votre équipement.)

# FAQ

## Est-ce que ce plugin s'appuie sur des API tiers ?

> Le plugin utilise le service ADB (Android Debug Bridge) pour récupérer les informations et envoyer les commandes de votre Android.
Le plugin installe le paquet debian 'adb-tools'

## Je ne vois pas mes applications dans le panneau droit ?

> La liste n'est pas générée dynamiquement en fonction les applications installées sur votre Android. Le nombre est limité à 6. Se reporter a la doc pour rendre visible ou non une application.

## Lorsque je clique sur une application, rien ne ce passe pourquoi?

> Entre les appareils équipés d'android TV, smartphone, box opérateurs, le nom des applications ne sont pas les memes, il faut donc modifier la commande ADB.
> 1) Pour cela lancer la commande shell ```sudo adb shell "pm list packages"|cut -f 2 -d ":"```
> 2) Repérer le nom de l'application, par exemple "com.google.android.youtube.tv"
> 3) Remplacer le nom de l'appli dans le champs commande de l'application (dans onglet "liste des applications" dans la configuration de l'équipement)

![Screenshot8](../images/Screenshot8.png)

## Je ne vois pas l'option "débogage par reseau", que faire ?

> Sur certains appareils Android, cette option est désactivée et le port 5555 servant a ADB n'est pas ouvert par défaut, pour remedier a cela il faut executer les commandes suivantes
> - Pour les freebox il faut toujours activer le debogage USB et connecter l'appareil a votre ordinateur (ou Jeedom) en USB.
> - Activer le debogage par reseaux.
> - Assurez vous que l'appareil est bien reconnu par l'ordinateur avec la commande "adb devices" (Votre appareil devrait etre listé)
> - Lancer la commande "adb tcpip 5555" (cette commande ouvre le port 5555)
> - Vous pouvez maintenant deconnecter le cable USB et profiter de votre plugin.
