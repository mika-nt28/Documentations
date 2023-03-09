---
layout: default
title: OpenALPR (openalpr)
lang: fr_FR
pluginId: openalpr
---

Description
===========
Plugin permanent de faire de la reconnaissance de plaque d’immatriculation avec nos camera

> Attention avec l'usage de ce plugin
Seules les autorités publiques (les mairies notamment) peuvent
Filmer la voie publique.
Les particuliers ne peuvent filmer que l’intérieur de leur propriété.
Ils ne peuvent pas filmer la voie publique, y compris pour
Assurer la sécurité de leur véhicule garé devant leur domicile.

Installation et configuration
=============================

Installation des dépendances
----------------------------

Pour faciliter la mise en place des dépendance, Jeedom vas gérer seul l’installation et la compilation du logiciel OpenALPR.

Dans le cadre réservé aux dépendances, vous allez avoir le statut de l’installation. Nous avons aussi la possibilité de consulté le log d’installation en temps réel.

![Installation des_dependances](../images/Installation_dependance.jpg)

Nous pouvons voir le statut de configuration et d’activation d’OpenALPR dans le cadre "Démon"

Configuration du plugin et de ses dépendances
----------------------------------------------

![Configuration du démon ALPRD](../images/openalpr_screenshot_configuration.jpg)

### Configuration du demon
* Pays du formats des plaques: Choisir le pays du format
* Format de la plaque : Choisir le format des plaquese
* Nom du site surveiller: Nom du de la zone couverte pars les cameras
* Temps entre 2 detections (s) : Saisir le temps avant la lever de la commande de détéction
* Création automatique de plaque inconnue: Permet à Jeedom de créer une commande pour les plaques non reconnue
* Nombre de thread: Nombre d'image annalysé simultanément
* Nombre de plaque maximum : Nombre de possibilité de plaque remontée par la détection
* Repertoire Snapshot : Choisir l'emplacement par défaut des snapshot
* Taille du dossier Snapshot (Mo) : Taille maximal du dossier de snapshot
* Activer le Snapshot : Permet de déterminer si on veut des snapshot des détectons


### Configuration des Cameras
* Ajouter une caméra : Permet d’ajouter une camera
* Nom: Donner un nom a votre caméra
* Url de la Camera: adresse du flux de votre camera
* Login de connexion à la Camera
* Mots de passe de la Camera

### Configuration avancée de OpenAlpr

La configuration des paramètres peut être défini avec l'utilitaire openalpr-utils-calibrate.exe sur windows avec une image de la camera.
[Vous pouvez télécharger les outils pour windows x64](https://github.com/openalpr/openalpr/releases/download/v2.3.0/openalpr-2.3.0-win-64bit.zip)

* state_id_img_size_percent:
* ocr_img_size_percent:
* Masque de capture: Pemet de limiter la detection dans une certaine zone
* Calibration: Le calibrage de votre caméra améliore la précision de la détection dans les cas où les plaques du véhicule sont capturées à un angle prononcé. Utilisez l'utilitaire openalpr-utils-calibrate pour calibrer votre caméra fixe afin de l'ajuster à un angle. Une fois cela fait, mettez à jour la configuration avec les valeurs obtenues à partir de l'outil
* Taille maximum de la plaques: La détection ignorera les plaques trop grandes. C'est une bonne technique d'efficacité à utiliser si le plaques vont être à une distance fixe de la caméra (par exemple, vous ne verrez jamais de plaques qui remplissent toute l'image)}
* Augmentation a chaque iteration: Pourcentage que le cadre de LBP augmente chaque itération. Il doit être supérieur à 1,0. Une valeur de 1,01 signifie augmentation de 1%, 1,10 augmentation de 10% de chaque fois. Ainsi, une augmentation de 1% serait ~ 10x plus lent que 10% à traiter, mais il a une plus grande chance de l'atterrissage directement sur la plaque et d'obtenir une détection forte
* Sensibilité de la detection: La force minimale de détection détermine comment assurer l'algorithme de détection doit être avant de signaler qu'une région de la plaque existe. Techniquement, cela correspond à LBP voisins les plus proches (par exemple, combien de détectives sont regroupés autour de la même zone). Par exemple, 2 = très indulgent, 9 = très stricte
* Redimentionner l'image: La détection n'a pas nécessairement besoin d'une image de très haute résolution pour détecter les plaques. En utilisant une image d'entrée plus petit doit encore trouver les plaques et le fera plus rapidement. Peaufiner les valeurs de max_detection_input va redimensionner l'image d'entrée si elle est plus grande que ces tailles (exprimées en pixels)
* Technique de detection: Technique utilisée pour trouver des régions de plaque d'immatriculation d'une image}
* Utilisé le format de plaque local: Les résultats doivent correspondre un textpattern de post-traitement si un modèle est disponible.
* Saut de detection: Contourne la détection de la plaque. Si elle est positionnée à 1, la bibliothèque suppose que chaque zone prévue est une zone de la plaque susceptible.
* Multi-analyse: OpenALPR peut balayer la même image plusieurs fois avec randomisation différent. Mettre ce paramètre à une valeur plus grande que 1 peut augmenter la précision, mais augmentera le temps de traitement linéaire
* Detection par contraste: OpenALPR détecte les cultures de plaque à contraste élevé et utilise une technique de détection de bord alternatif. Mettre cette option à 0.0 classerait toutes les images comme contraste élevé, la mise à 1.0 classerait pas d'images comme contraste élevé.
* max_plate_angle_degrees:
* ocr_min_font_point:
* Minimum de confiance OCR à considérer(%):
* Tout caractère OCR inférieur à ce parametre sera ignorée:

Paramétrage de mes groupes et de mes plaques
=============================================

![introduction01](../images/MesGroupes.jpg)

Vérification d'une image
-----------------

Il est possible de lancer une détection manuelle, ou par scénario de cette en passant en message l'url de votre image

![introduction01](../images/TestManuel.jpg)

Groupe de plaques
------------------

Dans un premier temps, il faut créer un nouveau groupe et le nommer.
Comme dans tous les plugins Jeedom vous avez un bouton ajouter un équipement sur la gauche de votre fenêtre.
![introduction01](../images/Configuration_equipement.jpg)

Ce nouveau groupe a besoin d'être paramétré.

* Nom du groupe : Le nom a déjà été paramétrée mais vous avez la possibilité de la changer
* Objet parent : Ce paramétré permet d'ajouter l'équipement dans un objet Jeedom
* Catégorie : Déclare l'équipement dans une catégorie
* Visible : Permet de rendre l'équipement visible dans le Dashboard
* Activer : Permet d'activer l'équipement
* Mode de mise a jours : permet de déterminé si les états des commandes représenteront la visibilité sur l'image ou un changement à chaque passage (cette deuxième option peut poser des problèmes si on reste devant la caméra)
* Camera autoriser : ce champ permet de spécifier quel camera à le droit de mettre à jours se groupe

Le groupe "Plaques détectées inconnu" se créer automatiquement dès qu’une plaque a été détecté et qu’elle n’existe pas sous Jeedom.

Plaques d'immatriculation
--------------------------

![introduction01](../images/Configuration_commande.jpg)

A la création du groupe certaine commande ont été ajouté automatiquement, il ne faut pas les supprimer.
* Dernier déclencheur : Indique la dernière plaque qui a été vue sur la camera
* Détection manuel : permet de spécifier une url d'une image a analysé
* État du groupe : informe l'état de détection du groupe

Pour compléter votre groupe vous devez ajouter autant de commandes que vous avez de plaque à détecter

* Nom : Donner un nom à votre plaque de manière à la retrouve facilement dans Jeedom
* Numéro de la plaque: Numéro de la plaque (sans les tirets) (il est possible de remplacer des caractères par de ** en cas de flotte avec de plaque qui se suive

>AX**
AX123**
AX**WW
123
**123WW
**WW

* Historiser: Très utiles si vous voulez visualiser sur le panel les entée
* Afficher: si vous voulez que la plaque apparaisse sur le Dashboard
* Déplacer: ce bouton permet de déplacer une plaque d’un groupe a un autre
* Enfin pensez sauvegarder.

Il est possible également de d'initialisé l'état de base (si vous avez choisi un changement à chaque passage) avec les boutons "Absent" et "Présent".

Condition et Action
-------------------
A chaque détection du plugin il est possible d'exécuter des actions.
Ses actions sont autorisées par des conditions
