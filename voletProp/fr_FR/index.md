---
layout: default
title: Volet proportionnel (voletProp)
lang: fr_FR
pluginId: voletProp
---

Description
===
Ce plugin a pour but de permettre de gérer ses volets de manière proportionnel

Paramétrage d'un volet proportionnel
===

![introduction01](../images/Configuration.jpg)

La page de configuration est assez simple.

Général
---

* Nom du volet : Le nom a déjà été paramétrée mais vous avez la possibilité de la changer
* Objet parent : Ce paramétré permet d'ajouter l'équipement dans un objet Jeedom
* Catégorie : Déclare l'équipement dans une catégorie
* Visible : Permet de rendre l'équipement visible dans le Dashboard
* Activer : Permet d'activer l'équipement
* Délais minimal : Permet de déterminer le délai entre 2 commandes (Attention plus le délai est grand et plus le petite montée seront impossible).
* Synchro : Sélectionner les types de synchro que vous souhaité.

Objet de control du volet
---

* Objet de montée : Commande Jeedom permettant de contrôler la montée (Action -> Défaut)
* Objet de stop  : Commande Jeedom permettant de contrôler le stop (Action -> Défaut)
* Objet de descente : Commande Jeedom permettant de contrôler la descente (Action -> Défaut)

Objet d'état du volet
---

Les états de mouvement sont définis comme une condition, c'est à dire qu'il faut définir un objet (de votre équipement connecter au volet) ainsi qu'un opérande et une valeur.
* Utiliser les états surs :
 * Les mouvement Jeedom : Permet, si cochée de mettre à jours la hauteur par le retour d'état, ou sinon de forcer la valeur demander

* Condition d'état montée : Cette état indique au plugin une montée
* Condition d'état descente  : Cette état indique au plugin une descente
* Condition d'état arrêt  : Cette état indique au plugin un arrêt de mouvement

* Fin de course  :  Commande Jeedom représentant la fin de course(info -> Binaire :1 = Volet complètement fermée)

Délais
---

* Temps total : Temps total que met le volet pour une fermeture ou une ouverture
* Temps de décollement : Temps avant lequel le volet se décolle du sol
