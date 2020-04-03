=== Installation des dépendance
Pour facilité la mise en place des dépendance, jeedom vas gérer seul l’installation et la compilation du logiciel OpenALPR.

Dans la cadre réservé aux dépendances, vous allez avoir le statut de l’installation. Nous avons aussi la possibilité de consulté le log d’installation en temps réel.

image::../images/Installation_dependance.jpg[]

=== Configuration du plugin et de ses dépendance
image::../images/openalpr_screenshot_configuration.jpg[]

Les paramettre de configuration général sont:

* Création automatique de plaque inconnue: Permet a jeedom de créer une commande pour les plaque non reconue
* Activer le Snapshot: Permet de déterminer si on veut des snapshot des détécton
* Choisir l'emplacement par defaut des snapshot
* Choisir les commandes d'alerte (mail, slack...) separer par des &&
* Choisir le nombre d'images envoyé
* Personnalisé les paramettre par defaut de OpenAlpr

*  state_id_img_size_percent
*  ocr_img_size_percent
*  Calibrage de votre camera améliore la précision de la détection dans les cas où des plaques d'immatriculation sont capturés à un angle raide (Utilisez l'utilitaire openalpr-utils-calibration pour calibrer votre camera fixe pour ajuster un angle )
*  La détection ignorera plaques qui sont trop grands. Ceci est une bonne technique de l'efficacité à utiliser si les plaques vont être à une distance fixe de la caméra (par exemple, vous ne verrez jamais plaques qui remplissent la totalité de l'image
*  Augmentation détection d'itération est le pourcentage que le cadre de LBP augmente chaque itération. Il doit être supérieur à 1,0. Une valeur de 1,01 signifie augmentation de 1%, 1,10 augmentation de 10% de chaque fois. Ainsi, une augmentation de 1% serait ~ 10x plus lent que 10% à traiter, mais il a une plus grande chance de l'atterrissage directement sur la plaque et d'obtenir une détection forte
*  La force minimale de détection détermine comment assurer l'algorithme de détection doit être avant de signaler qu'une région de la plaque existe. Techniquement, cela correspond à LBP voisins les plus proches (par exemple, combien de détectives sont regroupés autour de la même zone). Par exemple, 2 = très indulgent, 9 = très stricte
*  La détection n'a pas nécessairement besoin d'une image de très haute résolution pour détecter les plaques. En utilisant une image d'entrée plus petit doit encore trouver les plaques et le fera plus rapidement. Peaufiner les valeurs de max_detection_input va redimensionner l'image d'entrée si elle est plus grande que ces tailles (exprimées en pixels
*  Technique utilisée pour trouver des régions de plaque d'immatriculation d'une image. La valeur peut être réglée sur les résultats doivent correspondre un textpattern de post-traitement si un modèle est disponible.
*  Contourne la détection de la plaque. Si elle est positionnée à 1, la bibliothèque suppose que chaque zone prévue est une zone de la plaque susceptible.
*  OpenALPR peut balayer la même image plusieurs fois avec randomisation différent. Mettre ce paramètre à une valeur plus grande que 1 peut augmenter la précision, mais augmentera le temps de traitement linéaire
*  OpenALPR détecte les cultures de plaque à contraste élevé et utilise une technique de détection de bord alternatif. Mettre cette option à 0.0 classerait toutes les images comme contraste élevé, la mise à 1.0 classerait pas d'images comme contraste élevé.
*  max_plate_angle_degrees
*  ocr_min_font_point
*  Minimum de confiance OCR à considérer(%)
*  Tout caractère OCR inférieur à ce parametre sera ignorée.
*  Mode Débug
* Ajouter une camera : Permet d’ajouter une camera
* Resau jeedom: Permet de déterminer sur quel jeedom l’analyse va se faire
* Plugin source camera: determine la maniere de configurer une camera
* Url de la Camera: adresse du flux de votre camera
* Login de connexion a la Camera
* Mots de pass de la Camera

Nous pouvons voir le status de configuration et d’activation d’OpenALPR dans le cadre "Démon"

image::../images/Status_Demon.jpg[]
Si tous les voyant sont au vert, nous pouvons passée a la suite
