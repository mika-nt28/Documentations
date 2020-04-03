==== Groupe de plaques
Il est possible de lancer une detection manuel, ou par scénario de cette en passant en message l'url de votre image

image::../images/TestManuel.jpg[]

==== Groupe de plaques
Dans un premier temps, il faut créer un nouvelle groupe  et le nommé.
Comme dans tous les plugins Jeedom vous avez un bouton ajouté un equipement sur la gauche de votre fenetre.

image::../images/Configuration_equipement.jpg[]

Ce nouvelle équipement a besoin d'être paramétré.

* Nom du groupe : Le nom a déjà été paramétrée mais vous avez la possibilité de la changer
* Objet parent : Ce paramétré permet d'ajouter l'équipement dans un objet Jeedom
* Catégorie : Déclare l'équipement dans une catégorie
* Visible : Permet de rendre l'équipement visible dans le Dashboard
* Activer : Permet d'activer l'équipement

Le groupe "Plaques détectées inconnu" ce créer automatiquement des qu’une plaque a ete détécté et qu’elle n’existe pas sous jeedom.
Pour créer votre groupe et comme partout sur jeedom vous avez le bouton "Ajouter" sur la gauche de votre écran.

==== Plaques d'imatriculation

Maintenant que votre équipement est crée et configurée, on vas pouvoir y ajouter des commandes.
Le groupe "Plaques détectées inconnu" ce créer automatiquement des qu’une plaque a ete détécté et qu’elle n’existe pas sous jeedom.
Pour créer votre groupe et comme partout sur jeedom vous avez le bouton "Ajouter" sur la gauche de votre écran.

Exemple de configuration

image::../images/Configuration_commande.jpg[]

* Nom : Donner un nom a votre plaque de manière a la retrouve facilement dans Jeedom
* Numero de la plaque: Numero de la plaque (sans les tirets) (il est possible de remplacé des caractere par de ** en cas de flotte avec de plaque qui se suive

 AX**
AX123**
AX**WW
123
**123WW
**WW

* Historiser: Tres utiles si vous voulez visualiser sur le panel les entée
* Afficher: si vous voulez que la plaque apparaisse sur le dashbord
* Déplacer: ce bouton permet de déplacer une plaque d’un groupe a un autre
* Enfin pensez sauvegarder.
