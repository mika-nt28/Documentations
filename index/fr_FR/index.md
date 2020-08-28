---
layout: default
title: Liste des plugins
lang: fr_FR
---

# info

# Protocole domotique

## EIB / KNX (eibd)

Ce plugin permet de communiquer entre Jeedom et votre installation KNX.
Jeedom deviendra donc un équipement de votre installation.
Des fonctions d'auto-configuration (auto-include, parser ETS5) ont été implémentées pour permettre une mise en place rapide.

- [Documentation]({{site.baseurl}}/eibd/{{page.lang}})
- [Changelog]({{site.baseurl}}/eibd/{{page.lang}}/changelog)

## Global Cache (globalcache)

Ce plugin a pour objet de connecter Jeedom à vos équipements **global cache**.

- [Documentation]({{site.baseurl}}/globalcache/{{page.lang}})
- [Changelog]({{site.baseurl}}/globalcache/{{page.lang}}/changelog)

## Mochad - X10 (mochad)

Ce plugin permet de gérer vos équipements x10 grâce à votre CM15 ou CM19

- [Documentation]({{site.baseurl}}/mochad/{{page.lang}})
- [Changelog]({{site.baseurl}}/mochad/{{page.lang}}/changelog)

# Automatisme

## Arrosage automatique (arrosageAuto)

Ce plugin a pour objet de gérer facilement et automatiquement votre arrosage automatique.

- [Documentation]({{site.baseurl}}/arrosageAuto/{{page.lang}})
- [Changelog]({{site.baseurl}}/arrosageAuto/{{page.lang}}/changelog)

## Gestion du Chauffe-Eau (ChauffeEau)

Ce plugin permet de gérer votre chauffe-eau.
Il va estimer le temps nécessaire pour une chauffe complète de votre ballon.
Si votre installation est équipée d'une sonde de température, le plugin arrêtera la chauffe dès qu'il atteindra sa température désirée.
Après l'heure programmée, le plugin arrêtera la chauffe et attendra le prochain créneau, réduit du temps de chauffage calculé.

Le plugin embarque une régulation configurable par hystérésis.

- [Documentation]({{site.baseurl}}/ChauffeEau/{{page.lang}})
- [Changelog]({{site.baseurl}}/ChauffeEau/{{page.lang}}/changelog)

## Volet proportionnel (voletProp)

Ce plugin a pour but de permettre de gérer ses volets de manière proportionnel

- [Documentation]({{site.baseurl}}/voletProp/{{page.lang}})
- [Changelog]({{site.baseurl}}/voletProp/{{page.lang}}/changelog)

## Gestion de Volets (Volets)

Ce plugin a pour objectif de gérer facilement et automatiquement vos volets.

- [Documentation]({{site.baseurl}}/Volets/{{page.lang}})
- [Changelog]({{site.baseurl}}/Volets/{{page.lang}}/changelog)

# Communication

## Client SIP (clientSIP)

Ce plugin a pour but de connecter Jeedom a notre réseau SIP

- [Documentation]({{site.baseurl}}/clientSIP/{{page.lang}})
- [Changelog]({{site.baseurl}}/clientSIP/{{page.lang}}/changelog)

## Free SMS (FreeSms)

Ce plugin vous permet d'envoyer des sms à votre portable Free via le service de notification proposé par Free.

- [Documentation]({{site.baseurl}}/FreeSms/{{page.lang}})
- [Changelog]({{site.baseurl}}/FreeSms/{{page.lang}}/changelog)

# Énergie

## Production Énergie (prosommateur)

L’autoconsommation est le but dans la production d’énergie. Ce plugin est là pour vous y aidé en contrôlant les activations.

- [Documentation]({{site.baseurl}}/prosommateur/{{page.lang}})
- [Changelog]({{site.baseurl}}/prosommateur/{{page.lang}}/changelog)

# Santée

## Withings / Nokia (withings)

Plugin pour appareils Withings / Nokia, il permet de récupérer les informations des balances withings (poids, masse graisseuse mais pas le CO2) et des bracelets (distance, nombre de pas, heures de sommeil profond, heures de sommeil léger...)

- [Documentation]({{site.baseurl}}/withings/{{page.lang}})
- [Changelog]({{site.baseurl}}/withings/{{page.lang}}/changelog)

# Monitoring

|                                                                                                     |          |                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                |
| --------------------------------------------------------------------------------------------------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="{{site.baseurl}}/Freebox_OS/images/Freebox_OS_icon.png" class="pluginLogo" width="100" /> | Freebox  | Ce Plugin permet de récupérer les informations disponibles sur les box Freebox Révolution/Delta/Pop.Pour les Freebox Delta, il permet aussi de récupèrer les équipements connectés (Domotique)                                                             | [Documentation]({{site.baseurl}}/Freebox_OS/{{page.lang}})<br/>[Market](https://market.jeedom.com/index.php?v=d&p=market_display&id=1666)<br/>[Changelog]({{site.baseurl}}/Freebox_OS/{{page.lang}}/changelog) |
| <img src="{{site.baseurl}}/libreNMS/images/libreNMS_icon.png" class="pluginLogo" width="100" />     | LibreNMS | LibreNMS est une AutoDiscovery PHP/MySQL/SNMP réseau de surveillance qui comprend la prise en charge d'une large gamme de matériel réseau et les systèmes d'exploitation, y compris Cisco, Linux, FreeBSD, Juniper, Brocade, Foundry, HP et beaucoup plus. | [Documentation]({{site.baseurl}}/libreNMS/{{page.lang}})<br/>[Market](https://market.jeedom.com/index.php?v=d&p=market_display&id=3446)<br/>[Changelog]({{site.baseurl}}/libreNMS/{{page.lang}}/changelog)     |

# Multimédia

|                                                                                                           |                                |                                                                                                                                                                                                                                           |                                                                                                                                                                                                                      |
| --------------------------------------------------------------------------------------------------------- | ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="{{site.baseurl}}/freeCrytal/images/freecrystal_icon.png" class="pluginLogo" width="100" />      | Freebox Crytal                 | Ce plugin permet de récupérer les informations de votre Freebox Crystal.</br>Certains éléments sont rendus actifs par Jeedom (Redémarrage des Freebox, présence DHCP) mais nécessitent une installation supplémentaire sur votre serveur. | [Documentation]({{site.baseurl}}/freeCrytal/{{page.lang}})<br/>[Market](https://market.jeedom.com/index.php?v=d&p=market_display&id=1139)<br/>[Changelog]({{site.baseurl}}/freeCrytal/{{page.lang}}/changelog)       |
| <img src="{{site.baseurl}}/FreeboxMini4k/images/FreeboxMini4k_icon.png" class="pluginLogo" width="100" /> | Télécommande Freebox mini4K    | Contrôler votre Freebox mini4K                                                                                                                                                                                                            | [Documentation]({{site.baseurl}}/FreeboxMini4k/{{page.lang}})<br/>[Market](https://market.jeedom.com/index.php?v=d&p=market_display&id=3756)<br/>[Changelog]({{site.baseurl}}/FreeboxMini4k/{{page.lang}}/changelog) |
| <img src="{{site.baseurl}}/telecfree/images/telecfree_icon.png" class="pluginLogo" width="100" />         | Freebox Révolution (telecfree) | Plugin pour commander le Freebox Player de la Freebox Révolution                                                                                                                                                                          | [Documentation]({{site.baseurl}}/telecfree/{{page.lang}})<br/>[Market](https://market.jeedom.com/index.php?v=d&p=market_display&id=2032)<br/>[Changelog]({{site.baseurl}}/telecfree/{{page.lang}}/changelog)         |
| <img src="{{site.baseurl}}/plex/images/plex_icon.png" class="pluginLogo" width="100" />                   | Plex                           | CContrôler vos clients Plex grâce à votre domotique. </br> Créer des réveil, musical grâce à l'association de Plex et de Jeedom.                                                                                                          | [Documentation]({{site.baseurl}}/plex/{{page.lang}})<br/>[Market](https://market.jeedom.com/index.php?v=d&p=market_display&id=1380)<br/>[Changelog]({{site.baseurl}}/plex/{{page.lang}}/changelog)                   |

# Organisation

## Réveil (reveil)

Ce plugin permet de créer des réveils.

- [Documentation]({{site.baseurl}}/reveil/{{page.lang}})
- [Changelog]({{site.baseurl}}/reveil/{{page.lang}}/changelog)

## Cave à Vin (CaveVin)

Et si on domotisait notre cave à vin !
Ce plugin Jeedom nous permet de créer virtuellement notre cave, si on veut on peut domotiser la présence de la bouteille.

- [Documentation]({{site.baseurl}}/CaveVin/{{page.lang}})
- [Changelog]({{site.baseurl}}/CaveVin/{{page.lang}}/changelog)

# Confort

## SPA Balboa (balboa)

Ce plugin a pour objet de connecter Jeedom à vos Sap **balboa**.

- [Documentation]({{site.baseurl}}/balboa/{{page.lang}})
- [Changelog]({{site.baseurl}}/balboa/{{page.lang}}/changelog)

## Luminothérapie (luminotherapie)

Ce plugin permet de créer des ambiances lumineuse

- [Documentation]({{site.baseurl}}/luminotherapie/{{page.lang}})
- [Changelog]({{site.baseurl}}/luminotherapie/{{page.lang}}/changelog)

# Sécurité

## Face detection (facedetection)

Ce plugin utilise OpenCv pour détecter les visages sur vos camera.

- [Documentation]({{site.baseurl}}/facedetection/{{page.lang}})
- [Changelog]({{site.baseurl}}/facedetection/{{page.lang}}/changelog)

## Reconnaissance facial (facerecognition)

Ce plugin utilise OpenCv pour détecter et reconnaitre votre visage. Attention, toute de même aux permissions que vous accordez au plugin car on peut le tromper avec des photos … ou son jumeau

- [Documentation]({{site.baseurl}}/facerecognition/{{page.lang}})
- [Changelog]({{site.baseurl}}/facerecognition/{{page.lang}}/changelog)

## Reconnaissance de chute (falldetector)

Ce plugin utilise OpenCv pour détecter et reconnaitre les situations de chute.an 9

- [Documentation]({{site.baseurl}}/falldetector/{{page.lang}})
- [Changelog]({{site.baseurl}}/falldetector/{{page.lang}}/changelog)

## Motion (motion)

Motion est un logiciel de détection vidéo et qui permet de diffuser un flux vidéo via internet par le protocole HTTP. C’est une solution simple pour diffuser le flux de sa webcam en ligne ou pour détecter des mouvements dans le champ d’une caméra par exemple.
Dans ce plugin motion sera utilisé pour ces capacité de détection de mouvement

- [Documentation]({{site.baseurl}}/motion/{{page.lang}})
- [Changelog]({{site.baseurl}}/motion/{{page.lang}}/changelog)

## OpenALPR (openalpr)

Plugin permanent de faire de la reconnaissance de plaque d’immatriculation avec nos camera

> Attention avec l'usage de ce plugin
> Seules les autorités publiques (les mairies notamment) peuvent filmer la voie publique.
> Les particuliers ne peuvent filmer que l’intérieur de leur propriété.
> Ils ne peuvent pas filmer la voie publique, y compris pour assurer la sécurité de leur véhicule garé devant leur domicile.

- [Documentation]({{site.baseurl}}/openalpr/{{page.lang}})
- [Changelog]({{site.baseurl}}/openalpr/{{page.lang}}/changelog)

## Acces par QR code (QRacces)

Ce plugin permet de gérer une acces par QRcode.
Un Qr code est envoyé par mail à l'utilisateur autorisé

- [Documentation]({{site.baseurl}}/QRacces/{{page.lang}})
- [Changelog]({{site.baseurl}}/QRacces/{{page.lang}}/changelog)
