+++
archetype = "home"
title = "Documentation R&Darktable"
+++

## R&Darktable ?

R&Darktable est un logiciel Open Source de traitement photographique qui
permet de cataloguer ses photographies numériques et d'appliquer des
corrections et effets divers à ses images.

R&Darktable est un fork de darktable  dont le souhait est de supprimer
des parties  qui sont inutiles  pour plusieurs raisons. La  feuille de
route            est           disponible            à           cette
[page](https://github.com/Aurelien-Pierre/R-Darktable/wiki).

{{% notice warning %}}
Si le flux de  travail relatif à la scène ne vous  intéresse pas / ne
vous convient  pas (barrer  la mauvaise réponse),  ne continuez  pas à
lire. Ce  site n'est pas  pour vous.  Pour plus d'informations  sur le
flux de travail relatif à la scène :{{% button
href="basics/01-intro/" style="tip" %}}Infos{{% /button %}}

{{% /notice %}}


R&Darktable est installable sous :

{{%  expand title="GNU/Linux  avec  la méthode  de compilation"  %}}La
méthode            se            trouve           sur            cette
[page](https://blog.nicolastissot.fr/travailler-sur-une-version-compilee-de-darktable/). Celle
de R&Darktable ne diffère pas de celle de darktable.{{%
/expand %}}

{{%   expand   title="Windows"   %}}Un   .exe  se   trouve   à   cette
[page](https://github.com/Aurelien-Pierre/R-Darktable/releases).  Pour
autant,  les fonctions  d'import et  d'impression ne  fonctionnent pas
sous Windows  étant donné  que ces  fonctions dépendent  de librairies
n'existant pas sous ce système d'exploitation.{{% /expand %}}

Quant à darktable, il est installable sous :

{{%  expand title="GNU/Linux"  %}}Selon votre  système d'exploitation,
darktable est installable via plusieurs méthodes :
* la plus simple  est de l'installer par le système  de packages de la
distribution. L'inconvénient majeur est que la version ne sera souvent
pas à jour.
* une méthode  par des dépôts tiers. Il existe  pour les distribitions
Debia, Ubuntu,  Fedora ou OpenSuse  des dépôts permettant  d'avoir une
version    à   jour.    La   procédure    est   décrite    sur   cette
[page](https://software.opensuse.org/download.html?project=graphics:darktable&package=darktable).
*   La  troisième   est  beaucoup   plus  ardue.   Il  s'agit   de  la
  compilation. La méthode se trouve à cette [page](https://blog.nicolastissot.fr/travailler-sur-une-version-compilee-de-darktable/).{{% /expand %}}

{{%  expand title="Mac/OS"  %}}Le  paquet d'installation  se trouve  à
cette [page](https://github.com/darktable-org/darktable/releases).{{% /expand %}}

{{%  expand  title="Windows"  %}}Le  fichier exe  se  trouve  à  cette
[page](https://github.com/darktable-org/darktable/releases).{{% /expand %}}


## Documentation

Cette documentation se veut une porte d'accès à ce logiciel décrit par
la  plupart   comme  complexe.   Elle  a   pour  but   de  démystifier
l'utilisation  de  R&Darktable.  Pour  autant,   elle  ne  se  veut  pas
exhaustive  et  n'a   pas  pour  but  de  faire   tout  découvrir.  Le
développement décrit sera relatif à la scène.

Ce  site traitera  donc de  l'utlisation de  R&Darktable autour  de deux
modules essentiels : 

-   table lumineuse qui va s'occuper de l'importation et du classement
    des images

-   chambre noire où est développée l'image

## Questions

### R&Darktable = darktable

Non ou  plus  exactement  R&Darktable  est une  partie  de
darktable. En tout cas, c'est le souhait de son développeur : nettoyer
darktable des trucs inutiles, vieux qui ne marchent pas.

Ce  qui veut  dire aussi  que suivre  ce tutoriel  pour darktable  est
possible  mais nécessitera  quelques adaptations  pour le  configurer,
trouver les modules.  Il sera donc nécessaire de faire une petite
gymnastique entre  le tutoriel  et darktable.  Par exemple,  le module
export est à gauche sur R&Darktable mais à droite sur darktable.

### darktable sans D ?
Oui, ce  nom a  été choisi  comme cela dès  le départ.  Il n'y  a donc
aucune majuscule à mettre même en début de phrase.

### R&Darktable gratuit ?
Il est certes  gratuit mais cela ne  se résume pas à  cette notion. Il
est surtout libre. Il est fait par  des passionnés et ce travail a une
valeur.  Réduire  R&Darktable et  son parent  darktable à  un logiciel
gratuit est  donc un peu  offensant. Libre  veut aussi dire  qu'il est
aussi modifiable.

### R&Darktable = lightroom ?

Il est très  facile de répondre à cette question  : c'est non. Certes,
ils se ressemblent et c'est parfaitement normal dans l'historique étant
donné  qu'il a  été codé  par  d'anciens utilisateurs  de ce  logiciel
commercial. Cependant, ces deux projets  ont amplement divergés et ces
deux logiciels sont différents dans le fonctionnement. En venant de l'un
vers  l'autre, il  va  falloir changer  la manière  de  faire ;  c'est
valable dans les deux sens.

### R&Darktable est facile ?
Une réponse de normand est nécessaire : oui et non. Il est très facile
d'utiliser R&Darktable  quand on connait le  fonctionnement. "Toucher les
boutons" sans connaître le but donnera des résultats médiocres pour ne
pas dire complétement  râtées. Il est nécessaire  de connaître comment
R&Darktable  fonctionne pour  pouvoir  développer les  photos sinon  oui
ce logiciel est difficile à utiliser.

IL faut savoir que R&Darktable est aussi utilisé professionnellement par
des photographes.  Il a amplement  mérité cette place étant  donné des
outils  qui ne  sont pas  présents dans  d'autres logiciels  comme les
masques paramétriques.

Ainsi,  apréhender R&Darktable  est  nécessaire.  Il  existe certes  une
[documentation
darktable](https://docs.darktable.org/usermanual/3.8/fr/)   mais  elle
n'est guère  pratique d'où  l'existence de  cette page,  d'autant qu'à
l'heure  de l'écriture  de cette  page, elle  n'est pas  à jour  de la
dernière version.

### Mais développer une photo, c'est tricher
La réponse  est non. Une photographie  à la base est  déjà tronquée de
par  le   cadrage  ou   les  paramètres   qui  changent   l'aspect  de
l'image. Partir de ce postulat est déjà faux. D'autre part, développer
sous  R&Darktable remplace  simplement le  travail qui  serait autrement
effectué  par l'appareil  photo. Il  vaut quand  même mieux  contrôler
soi-même le processus.  
Il faut comprendre que le RAW n'est  pas une photo mais un fichier qui
est  à développer  pour  en tirer  une  image. Cela  est  à mettre  en
corrélation  avec le  négatif argentique.  On remplace  simplement les
bains, masquages  et autres  choses manuelles  par un  logiciel. C'est
plus propre...

## Licences

R&Darktable est  un logiciel  libre sous  licence GPL  v3 de  même que
darktable.

La documentation est sous licence creative commons CC BY-NC-SA 4.0. 

## Participer
Etant donné  sa licence,  participer à ce  projet est  une possibilité
souhaitée.  Dans cette  hypothèse, cliquer  sur  le crayon  en haut  à
droite.
