+++
archetype = "home"
title = "Documentation Ansel Photos"
+++

## Ansel Photos ?

Ansel est un logiciel Open Source de traitement photographique qui
permet de cataloguer ses photographies numériques et d'appliquer des
corrections et effets divers à ses images.

Ansel est un fork de darktable dont le souhait est de supprimer
des parties  qui sont inutiles  pour plusieurs raisons. La  feuille de
route            est           disponible            à           cette
[page](https://github.com/aurelienpierreeng/ansel/wiki#roadmap).

{{% notice warning %}}
Si le flux de  travail relatif à la scène ne vous  intéresse pas / ne
vous convient  pas (barrer  la mauvaise réponse),  ne continuez  pas à
lire. Ce  site n'est pas  pour vous.  Pour plus d'informations  sur le
flux de travail relatif à la scène :{{% button
href="basics/01-intro/" style="tip" %}}Infos{{% /button %}}

{{% /notice %}}


Ansel est installable sous :

{{%  expand title="GNU/Linux"  %}}La
méthode de compilation se trouve sur cette
[page](https://blog.nicolastissot.fr/travailler-sur-une-version-compilee-de-darktable/). Celle
d'Ansel ne diffère pas de celle de darktable.

Il existe aussi une AppImage sur la [page github du projet](https://github.com/aurelienpierreeng/ansel/releases){{%
/expand %}}

{{%   expand   title="Windows"   %}}Un   .exe  se   trouve   à   cette
[page](https://github.com/aurelienpierreeng/ansel/releases).  Pour
autant,  les fonctions  d'import et  d'impression ne  fonctionnent pas
sous Windows  étant donné  que ces  fonctions dépendent  de librairies
n'existant pas sous ce système d'exploitation.{{% /expand %}}

{{%  expand title="Mac/OS"  %}}Le  paquet d'installation  se trouve  à
cette [page](https://github.com/aurelienpierreeng/ansel/releases).{{% /expand %}}

## Documentation

Cette documentation se veut une porte d'accès à ce logiciel décrit par
la  plupart   comme  complexe.   Elle  a   pour  but   de  démystifier
l'utilisation  d'Ansel.  Pour  autant,   elle  ne  se  veut  pas
exhaustive  et  n'a   pas  pour  but  de  faire   tout  découvrir.  Le
développement décrit sera relatif à la scène.

Ce site traitera donc de l'utlisation d'Ansel autour de deux
modules essentiels : 

-   table lumineuse qui va s'occuper de l'importation et du classement
    des images

![screen](lighttable.png?classes=shadow&height=500px)

- chambre noire où est développée l'image

![screen](darktable.png?classes=shadow&height=500px)

## Questions

### Ansel = darktable

Non ou  plus  exactement Ansel  est une  partie  de
darktable. En tout cas, c'est le souhait de son développeur : nettoyer
darktable des trucs inutiles, vieux qui ne marchent pas.

Ce  qui veut  dire aussi  que suivre  ce tutoriel  pour darktable  est
possible  mais nécessitera  quelques adaptations  pour le  configurer,
trouver les modules.  Il sera donc nécessaire de faire une petite
gymnastique entre  le tutoriel  et darktable.  Par exemple,  le module
export est à gauche sur Ansel mais à droite sur darktable.

### Ansel gratuit ?
Il est certes  gratuit mais cela ne  se résume pas à  cette notion. Il
est surtout libre. Il est fait par  des passionnés et ce travail a une
valeur.  Réduire Ansel et son parent darktable à un logiciel
gratuit est  donc un peu  offensant. Libre  veut aussi dire  qu'il est
aussi modifiable.

### Ansel = lightroom ?

Il est très  facile de répondre à cette question  : c'est non. Certes,
ils se ressemblent et c'est parfaitement normal dans l'historique étant
donné  qu'il a  été codé  par  d'anciens utilisateurs  de ce  logiciel
commercial. Cependant, ces deux projets  ont amplement divergés et ces
deux logiciels sont différents dans le fonctionnement. En venant de l'un
vers  l'autre, il  va  falloir changer  la manière  de  faire ;  c'est
valable dans les deux sens.

### Ansel est facile ?
Une réponse de normand est nécessaire : oui et non. Il est très facile
d'utiliser Ansel quand on connait le fonctionnement. Mais "Toucher les
boutons" sans connaître le but donnera des résultats médiocres pour ne
pas dire complétement  râtées. Il est nécessaire  de connaître comment
Ansel  fonctionne pour  pouvoir  développer les  photos sinon  oui
ce logiciel est difficile à utiliser comme tant d'autres.

IL faut savoir que Ansel est aussi utilisé professionnellement par
des photographes.  Il a amplement  mérité cette place étant  donné des
outils  qui ne  sont pas  présents dans  d'autres logiciels  comme les
masques paramétriques.

Ainsi,  apréhender Ansel  est  nécessaire.  Il  existe certes  une
[documentation
darktable](https://docs.darktable.org/usermanual/3.8/fr/)   mais  elle
n'est guère  pratique d'où  l'existence de  cette page,  d'autant qu'à
l'heure de  l'écriture de cette  page, elle n'est  pas à jour  pour la
version 4.

### Mais développer une photo, c'est tricher
La réponse  est non. Une photographie  à la base est  déjà tronquée de
par  le   cadrage  ou   les  paramètres   qui  changent   l'aspect  de
l'image. Partir de ce postulat est déjà faux. D'autre part, développer
sous Ansel remplace simplement le travail qui serait autrement
effectué  par l'appareil  photo. Il  vaut quand  même mieux  contrôler
soi-même le processus.  
Il faut comprendre que le RAW n'est  pas une photo mais un fichier qui
est  à développer  pour  en tirer  une  image. Cela  est  à mettre  en
corrélation  avec le  négatif argentique.  On remplace  simplement les
bains, masquages  et autres  choses manuelles  par un  logiciel. C'est
plus propre...

## Licences

Ansel est un logiciel libre sous licence GPL v3 de même que
darktable.

La documentation est sous licence creative commons CC BY-NC-SA 4.0. 

{{% button href="/more/soutenir/" style="info" %}}Participer{{% /button %}}
