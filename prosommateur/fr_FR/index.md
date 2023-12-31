---
layout: default
title: Production Énergie (prosommateur)
lang: fr_FR
pluginId: prosommateur
---

Description
===========

L’autoconsommation est le but dans la production d’énergie. Ce plugin est là pour vous y aidé en contrôlant les activations.

Suivis de la production
=======================

Pour chaque producteur d'énergie vous pouvez crée une gestion
![Exemple de la configuration d'un équipement](../images/ConfigurationProducteurs.jpg)

Pour que le plugin fonctionne il est necessaire de luis configurer 
* la puissance produit instantané, et elle doit etre positive, sinon le plugin propose l'inversion de sense a cocher.
* La puissance sur le réseau, et elle doit etre positive lorsque l'on consome et positive lorsque l'on injecte, sinon le plugin propose l'inversion de sense a cocher.

Commande particulière
=====================

Le plugin a des commandes qui ne sont pas des gestions.
Ces commandes sont des informations issues des calcul du plugin
* Consommation : Image de la consommation actuelle entre production et reseau. Elle est négative lorsque l'on a une consommation sur le réseau
* Production : Moyenne sur une heure glissante de la puissance produite

Gestions des autorisations
==========================

Chaque gestion d'autorisation est une commande booléen de Jeedom et donc exploitable partout sur Jeedom.
Les autorisations sont hiérarchiques, c'est à dire que la puissance produite doit être supérieur ou égale à la somme de toutes les gestions précédentes autorisé.

![Exemple de la configuration d'une gestion](../images/ConfigurationGestions.jpg)

Pour configurer une gestion il faudra saisir
* Consommation autorisé (W): La puissance nominal de l'équipements a activé
* Tolérance (W): La puissance de consommation du réseau autorisé
* Type de filtrage de la production: pour éviter les coupures liée a la production, le plugin embarque un lissage de la production sur une heure ou un temps de maintiens
* Le temps de maintiens: ce paramètre permet de stabiliser la production, on autorise un temps (s) sur lequel on maintien l'activation

Condition
----------
Afin de pouvoir filtrer les allumages inutiles de votre équipement nous avons la possibilité de lui ajouter des conditions d'exécution.

Cliquer sur "Ajouter une condition" et configurer votre condition
Chaque condition de la liste formera un ET

Dans mon exemple si dessous, on voit que j'autorise l'utilisation de la production uniquement si mon eau est inferieur a 35°C

Actions
---------
Les actions sont exécutées dans l'ordre d'apparition en fonction de leur déclencheurs (on ou off).
Vous pouvez aussi bien notifier que de piloté l'équipements
