---
layout: default
title: Réveil (reveil)
lang: fr_FR
pluginId: reveil
---

Description
==========
Ce plugin permet de créer des réveils.

Création d'un réveil
==========

Paramètre général
---

![introduction01](../images/ConfigurationGeneral.jpg)

* Nom : le nom a déjà été paramétré, mais vous avez la possibilité de le changer.
* Objet parent : ce paramètre permet d'ajouter l'équipement dans un objet Jeedom.
* Catégorie : défini la catégorie de l'équipement.
* Visible : permet de rendre l'équipement visible dans le Dashboard.
* Activer : permet d'activer l'équipement.
* Temps après un snooze : permet de déterminer le temps de snooze

Programmation
---
Nous avons la possibilité de créer plusieurs programmations de réveil.

![introduction01](../images/ConfigurationProgramation.jpg)

Plusieur option sont disponnible dans la configuration d'une programation
* Nom : le nom permet d'identifié la programmation dans les actions et les condition.
* Mode : ce paramètre permet de définir si le reveil est unique ou programmer dans la semaine.
*	Jour actif: Si mode Unique on définie la date unique du reveil, sinon ou choisi les jour de répetiton
*	Heure : Permet de définir l'heure du reveil
*	Reprogrammation : Pour chaque programmation, une url de reconfiguration est disponible pour le lier avec d'autre équipement.

L'url de reprogrammation se présente sous la forme suivante :
URL_Jeedom/plugins/reveil/core/api/jeeReveil.php?apikey=APIKEY&id=ID&prog=IDcmd&day=%DAY&heure=%H&minute=%M
Les champs, "URL_Jeedom, APIKEY, ID, IDcmd", sont automatiquement complétés pour chaque URL.
Il sera impératif de personnaliser cette url et de remplacer les paramètres par les informations à compléter :

- %DAY : Les jours de déclanchements (0 = Dimanche, 1 = Lundi, ...)
- %H : L'heure de déclanchement du réveil
- %M : La minute de déclanchement du réveil

Condition
---
Afin de pouvoir filtrer les déclanchements du réveil nous avons la possibilité de lui ajouter des conditions d'exécution

![introduction01](../images/ConfigurationCondition.jpg)

Cliquer sur "Ajouter une condition" et configurer votre condition
* le trigger (Demarrage, snooze, arret)
* La programmation a prendre en compte
Chaque condition de la liste formera un ET

Action
---
Vous pouvez configurer le séquencement de votre réveil, en triant l'ordre de déclanchemente des actions.
Pour chaque action il est possible de mettre 
* un délai d'attente de son execution,
* le trigger (Demarrage, snooze, arret)
* La programmation a prendre en compte

![introduction01](../images/ConfigurationAction.jpg)

FAQ
====
Peut on interdir un reveil lorsque je suis en congé
---
Les conditions sont votre meilleurs amis pour controler les declanchement du reveil

Est il possible de mettre un delais negatif
---
Oui, le plugin vas analyser les delais d'action dans sa programmation

Peut on dynamiquement changer la programmation
---
Oui, a chaque programmation, on dispose d'un lien vers l'api 
