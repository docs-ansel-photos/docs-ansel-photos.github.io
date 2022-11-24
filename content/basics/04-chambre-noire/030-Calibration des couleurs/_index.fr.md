+++
disableMermaid = false
title = "Calibration des couleurs"
weight = 30
+++

Module essentiel, c'est la nouvelle balance des blancs. Comme spécifié
dans les préférences, l'adaptation chromatique moderne ne comporte pas
uniquement ce module calibration des couleurs mais aussi la balance
des blancs. Ce dernier est activé automatiquement, si bien qu'il n'est
pas utile d'y revenir. Ce tutoriel ne s'occupera que de cette facette de
la balance des blancs, l'adaptation chromatique ; donc uniquement de
l'onglet CAT.

Les paramètres de base à l'ouverture du module (illuminant et espace de
travail) sont initialisés à l'aide des métadonnées Exif du fichier raw.
Il existe plusieurs options pour les modifier :

-   utiliser la pipette de sélecteur de couleurs pour sélectionner une
    couleur neutre dans l'image, sinon l'image entière. Cette méthode ne
    sera pas valable pour les scènes artificielles

-   la détection par sélection des bords (accessible dans le menu de
    l'illuminant). L'algorithme trouve la couleur moyenne du dégradé des
    bords. Cette méthode est sensible aux aberrations chromatiques, au
    bruit et est mal adaptée aux images à haute résolution. Par contre,
    elle convient très bien aux scènes artificielles

-   la détection par sélection des surfaces qui combine les deux
    méthodes précédentes (accessible aussi dans le menu de
    l'illuminant). Elle est donc moins sensible au bruit et aux surfaces
    non neutres. Cependant, des textures colorées nettes risquent de
    faire échouer l'algorithme, par exemple l'herbe verte

Après l'option choisie, un illuminant avec une température ainsi que
l'espace de couleur seront sélectionnés. A gauche de la couleur de
l'illuminant se trouve la température de couleur corrélée (CCT), elle
est la plus proche en Kelvin de l'illuminant utilisé. Elle informe en
même temps de la correspondance de l'illuminant :

-   lumière du jour : cela signifie qu'il est proche d'un spectre idéal
    de la lumière du jour (valeur significative)

-   corps noir : il est proche d'un spectre idéal de corps noir
    Planckien (valeur significative)

-   non valide : chiffre de température probablement erronée étant donné
    que cette valeur est trop éloignée du spectre de la lumière du jour
    et du corps noir

Ensuite, il sera toujours temps de changer si les paramètres ne
conviennent pas :

-   l'espace d'adaptation chromatique : il faut en retenir deux ; le
    Bradford linéaire le plus approprié pour la lumière du jour et les
    corps noirs mais pas pour les illuminants plus difficiles (LED
    bleues par exemple) et le cat16 plus robuste pour ces types de
    lumière difficile

-   l'illuminant en sélectionnant celui qui correspond

-   la température de l'illuminant

Au niveau fonctionnement, et ce dans la majeure partie des images, il
est assez facile d'obtenir un bon résultat.

Le paramétrage à l'ouverture du module est généralement de bonne
facture. Si seule la température n'est pas la bonne, il suffit de la
modifier. Dans le cas où plusieurs options sont erronées, il peut être
intéressant de partir sur la sélection de la couleur neutre par la
pipette ou les algorithmes. Il est un peu plus compliqué à comprendre
qu'une simple balance des blancs mais le résultat n'en sera que
meilleure sur les couleurs. En effet, la balance des blancs ne s'occupe
que du blanc là où la calibration des couleurs prend en compte les
couleurs.

Il faut aussi ajouter deux paramètres :

-   la compression du gamut. C'est une méthode non destructive pour
    tenter de comprimer la saturation afin de faire rentrer l'image
    entière dans l'espace colorimétrique du travail du pipeline.
    L'exemple le plus parlant est la présence de LED bleues ce qui peut
    entraîner un écrêtage de mauvaise facture du gamut dans l'image
    finale. La présence du gamut peut se voir avec le bouton en bas de
    l'image, le panneau attention.

-   écrêter les valeurs RVB négatives du gamut pour éviter un mauvais
    niveau de noir ainsi que le problème d'écrêtage avec les lumières
    bleues.

Il est certain que ces explications restent basiques. Une utilisation
experte peut être faite avec ce module, mais là n'est pas le sujet de ce
tutoriel.
