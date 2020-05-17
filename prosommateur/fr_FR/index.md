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

Pour que le plugin fonctionne il est impératif de luis configurer la puissance produit instantané
Si votre cette puissance est dans le négatif il est possible de l'inverser car le plugin compare de puissance positive
Si l'on a la possibilité d'avoir une image de la consommation instanée (teleinfo par exemple) nous aurons donc la consommation réelle et ce qui est réinjecter dans le réseau.
Cette puissance est souvent négative, puisque le compteur envoie une puissance consommée et que ce qui nous intéresse c'est la puissance injecter dans le réseau

Commande particulière
=====================

Le plugin a des commandes qui ne sont pas des gestions.
Ces commandes sont des informations issues des calcul du plugin
* Consommation : Image de la consommation actuelle de la production. Elle est négative lorsque l'on a une consommation sur le réseau
* Production : Moyenne sur une heure glissante de la puissance produite

Gestions des autorisations
==========================

Chaque gestion d'autorisation est une commande booléen de Jeedom et donc exploitable partout sur Jeedom.
Les autorisations sont hiérarchiques, c'est à dire que la puissance produite doit être supérieur ou égale à la somme de toutes les gestions précédentes autorisé.

![Exemple de la configuration d'une gestion](../images/ConfigurationGestions.jpg)

Pour configurer une gestion il faudra saisir
* Consommation autorisé (W): La puissance nominal de l'équipements a activé
* Tolérance (W): La puissance de consommation du réseau autorisé
* Le temps de maintien: ce paramètre permet de stabiliser la production, on autorise un temps (s) sur lequel on maintien l'activation

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
