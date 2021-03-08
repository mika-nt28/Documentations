---
layout: default
title: Beta test (betatest)
lang: fr_FR
pluginId: betatest
---

# Description

Ce plugin a pour objectif de faciliter les echanges entre Devellopeur et Betatesteur

# Dans les plugins en beta
Dans chaque plugin en beta, pour qu'il soit compatible il faut creer un dossier "test"

## Creation d'une campagne de test
A l'interieur du dossier test il faut creer un fichier JSON qui pour indiquer les test a rélaisé, les bouchons (virutel a cree) ou les equipement reel

le Json doit etre sous la forme

{ campaign:{ nom:"Nom de la campagne", description:"Détail et objectif de la campagne de test", equipement:false, virtual:{volet}, testcase:{

}
} }

## Creation d'un test
A l'interieur du dossier test il faut creer un fichier JSON qui pour indiquer les test a rélaisé, les bouchons (virutel a cree) ou les equipement reel

le Json doit etre sous la forme

{ testcase:{ nom:"Nom du test", description:"Ce que l'on coit tester", result:"Resulation attendue" } }
