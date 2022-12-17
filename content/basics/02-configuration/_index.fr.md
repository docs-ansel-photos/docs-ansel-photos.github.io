+++
disableToc = false
title = "Configuration"
weight = 10
+++

Ansel est un logiciel complet qui comporte beaucoup d'outils. Il
convient de  le paramétrer  un minimum.  Cela se  fait par  la fenêtre
accessible par la  roue crantée sur tout onglet du  logiciel située en
haut plutôt à droite.

{{% notice info %}} Comme dit  auparavant, à terme, il sera inutile de
suivre totalement cette partie pour configurer Ansel puisque les
fonctions restantes seront en relation avec le flux de travail relatif
à la scène. Si les options sont inexistantes, il ne faut pas en tenir compte.

Ce sera toujours essentiel pour darktable dans l'hypothèse
où ce serait votre souhait.  {{% /notice %}}

### Onglet général

Il s'agit de sélectionner :
* la langue fr
* le  thème elegant-grey. Il  permet de  développer une photo  dans de
    bonnes conditions. Un  thème trop contrasté noir ou  blanc sera un
    facilitateur  d'erreurs  en  terme  de  saturation,  contraste  et
    exposition.

### Traitement

Dans le cadre d'un flux de travail relatif à la scène ce dont il
est question dans ce tutoriel, il est nécessaire de désactiver :

-   la courbe de base
-   la netteté

Il existe aussi l'option  du flux de travail  par défaut. Il
permet  de faire  un  développement de  base ou  non  selon le  module
central  (courbe de  base ou  filmique  rvb). Dans  un premier  temps,
sélectionner le flux de travail relatif à la scène (rvb) est une bonne
option.  Cela activera filmique RVB et exposition avec des réglages de
base.

{{% notice warning %}}
En tout cas, dans le cadre d'un flux de travail rvb, il ne faut
pas utiliser la courbe de base ou le flux de travail relatif à l'écran
qui active cette courbe de base.
{{% /notice %}}

Pour ce qui  est de l'adaptation chromatique,  l'originel désigne dans
le flux  de travail  la présence  d'une seule  balance des  blancs, au
contraire du flux moderne qui en  contient "deux" : balance des blancs
et calibration des couleurs :
* La balance des blancs rendra neutre les
couleurs qui doivent l'être (blanc et gris)
* la  calibration des couleurs fera le  reste du travail  sur les
couleurs. 

Il faut noter qu'il n'y aura pas plus de manipulations de
modules au  niveau du nombre.   En effet,  la balance des  blancs sera
réglée automatiquement sur le point de référence neutre du boîtier, le
plus souvent  D65.  Ce nouveau  flux permettra d'obtenir  de meilleurs
développements, c'est donc celui qui sera utilisé dans le tutoriel.

### Partie stockage

Le fichier xmp est un fichier texte qui accompagne chaque raw. Chaque
raw peut avoir plusieurs fichiers xmp ce qui symbolise les clones, pour
pouvoir avoir plusieurs versions de développement. darktable modifie les
xmp et non les raw.

Donc afin de pouvoir développer plus sereinement avec des clones,
activer les fichiers xmp est nécessaire pour une gestion facile de
ceux-ci.

Les autres parties sont à votre discrétion et ne seront pas décrites
ici. En effet, elles ne sont pas nécessaires dans un premier temps pour
développer une photo.

{{% notice tip %}}
Il ne faut pas oublier de redémarrer Ansel pour que les nouvelles
préférences soient prises en compte.
{{% /notice %}}
