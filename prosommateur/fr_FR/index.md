---
layout: default
title: Production Energie (prosommateur)
lang: fr_FR
pluginId: prosommateur
---

Description
===========

L’autoconsommation est le bute dans la production d’énergie. Ce plugin est la pour vous y aidé en contrôlant les activations.

Suivis de la production
=======================

Pour chaque producteur d'energie vous pouvez cree une gestion
![Exemple de la configuration d'un equipement](../images/ConfigurationProducteurs.jpg)

Pour que le plugin fonctionne il est imperatif de luis configurer la puissance produit instantané
Si votre cette puissance est dans le negatif il est possible de l'inverser car le plugin compare de puissance positive
Si l'on a la possibilité d'avoir une image de la consomation instané (teleinfo par exemple) nous aurrons donc la consomation reel et ce qui est reinjecter dans le reseau.
Cette puissance est souvant negative, puisque le compteur envoie une puissance consommé et que ce qui nous interresse c'est la puissance injecter dans le reseau

Commande particuliere
=====================

Le plugin a des commande qui ne sont pas des gestion.
Ces commandes sont des information issue des calcul du plugin
* Consomation : Image de la consomation actuel de la production. Elle est negative lorsque l'on a un consommation sur le reseau
* Production : Moyenne sur une heure glissante de la puissance produite

Gestions des autorisations
==========================

Chaque gestion d'autorisation est une commande booléen de jeedom et donc exploitable partout sur jeedom.
Les autorisation sont hierachique, c'est a dire que la puissance produite doit etre supperieur ou egale a la somme de toute les gestion precedente autorisé.

![Exemple de la configuration d'une gestion](../images/ConfigurationGestions.jpg)

Pour configurer une gestion il faudras saisir 
* Consommation autorisé (W): La puissance nominal de l'equipement a activé
* Tolérance (W): La puissance de consommation du resau autorisé
* Le temps de maintien: ce parametre permet de stabilisé la production, on autorise un temps (s) sur lequel on maintien l'activation

Condition
----------
Afin de pouvoir filtrer les allumages inutile de votre equipement nous avons la possibilité de lui ajouter des conditions d'execution.

Cliquer sur "Ajouter une condition" et configurer votre condition
Chaque condition de la liste formera un ET

Dans mon example si dessous, on voit que j'autorise l'utilisation de la production uniquement si mon eau est inferieur a 35°C

Actions
---------
Les actions sont executé dans l'ordre d'apparition en fonction de leur declancheurs (on ou off).
Vous pouvez aussi bien notifié que de piloté l'equipement
