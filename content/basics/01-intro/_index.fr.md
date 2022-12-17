+++
disableToc = false
title = "Introduction"
weight = 2
+++

Ce tutoriel va s'attacher à décrire  le flux de travail sous Ansel
de l'importation jusqu'à  l'exportation de l'image avec,  bien sûr, le
développement.

Ansel n'est pas aussi difficile que l'on voudrait faire croire. Il
s'agit tout  simplement de partir d'une  base saine et de  savoir quoi
utiliser.

Ansel possède  environ 80  modules dans la  chambre noire  (à la
date  d'écriture). Certains  sont  redondants,  appartiennent au  flux
relatif à l'affichage ou à la  scène. Comme dit auparavant, ce site ne
traitera que du flux relatif à la scène ; ce pour plusieurs raisons :
* la facilité : parler de tout serait beaucoup trop long
* sa supériorité ; le flux  de travail relatif à l'affichage se trouve
  dans l'espace  de couleur  Lab. Pour rester  simple et  reprendre un
  paragraphe                           de                          cet
  [article](https://darktable.fr/posts/2020/01/darktable-3-rgb-ou-lab-quels-modules-au-secours/),
  "Lab ne marche  pas pour des images à fort  contraste, ne marche pas
  si bien  pour des images à  contraste modéré, et encode  les valeurs
  des pixels  de façon perceptuelle  et non  physique, ce qui  va nous
  poser  problème pour  la suite.  Lab n’a  jamais été  construit pour
  faire de la retouche mais seulement pour étudier la vision humaine."
  
Avec  ces  notions,  il  est  facile  de  clarifier  l'utilisation  de
darktable et en faire un logiciel "facile" ou tout au moins plus clair.

{{% notice info %}}
Certaines parties ne seront plus valables pour Ansel  qui sera libéré  de ces
considérations. Il sera ainsi plus  facile de débuter un apprentissage
sur Ansel.

Par contre, cette configuration sera nécessaire pour darktable.
{{% /notice %}}

Il va se découper en plusieurs étapes :
* configuration
* table lumineuse
* chambre noire
* export

Ainsi, les différentes actions du processus seront vues :
* import
* classement
* recherche
* développement
* export
