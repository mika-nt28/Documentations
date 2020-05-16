---
layout: default
title: Freebox Crystal (freeCrystal)
lang: fr_FR
pluginId: freeCrystal
---

Ce plugin permet de récupérer les informations de votre Freebox Crystal.
Certains éléments sont rendus actifs par Jeedom (Redémarrage des Freebox, présence DHCP) mais nécessitent une installation supplémentaire sur votre serveur.

Installation : Présence DHCP
====
Pour que le service de vérification de présence des adresses DHCP fonctionne, il est nécessaire d'installer arp-scan
Dans un terminal :

> `sudo apt-get install arp-scan` : installation du paquet permettant de scanner le réseaux
> `sudo visudo -s`
Ajouter la ligne :
> 'www-data ALL=NOPASSWD: /usr/bin/arp-scan`

Installation : Redémarrage des Freebox
===
Pour le redémarrage des Freebox (serveur et Player), il est nécessaire de donner les droits au script

> `#sudo chmod -R 777 /usr/share/nginx/www/jeedom/plugins/freeCrystal/ressources/`
