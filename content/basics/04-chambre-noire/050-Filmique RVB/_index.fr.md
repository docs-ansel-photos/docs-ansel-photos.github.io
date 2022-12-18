+++
disableMermaid = false
title = "Filmique RVB"
weight = 50
+++

Dans un premier temps, l'ajustement se fait sur l'exposition relative du
blanc et du noir.

Sur le blanc, il s'agit de récupérer de la texture dans les éléments
clairs tout en n'augmentant pas trop cette valeur pour ne pas perdre de
contraste. L'idée est d'utiliser le contour blanc pour faire coïncider
ce blanc au blanc de l'image.

Sur le noir, l'ajuster permet d'obtenir un vrai noir. Dans une partie
des cas, la valeur absolue de l'exposition du noir approche celle du
blanc.

De même que le module exposition, si le flux de travail relatif à la
scène est sélectionné, ce module sera activé avec certains paramètres.

Le bouton zones  sur et sous exposées  en bas à droite  alerte sur les
zones nommées.  Cette caractéristique est  toutefois à mettre  en lien
avec le bouton d'à  coté juste à sa gauche zones  sur et sous exposées
en RAW. En effet, en RAW si  la zone est sur-exposée, les pixels n'ont
en fait pas d'informations. Il ne  sera donc pas possible de récupérer
des données  sur ces  pixels et augmenter  l'exposition du  blanc pour
diminuer la  sur-exposition ne changera  rien du  tout à ce  niveau et
diminuera même le contraste.

![Vue chambre noire](noir-blanc.png?classes=shadow&height=500px)

Au terme de ces réglages, la courbe aura une certaine forme. Elle va
peut être avoir aux extrémités un écrêtage symbolisé par une partie
orange. Cela signifie qu'une plage des ombres ou hautes-lumières aura le
même rendu. Le réglage va se faire dans l'onglet look. Pour enlever ou
diminuer cet écrêtage, il suffit de diminuer la latitude qui est le
pourcentage que l'on donne aux tons moyens symbolisé sur la courbe par
les deux points blanc. En diminuant, cela laissera plus de place aux
autres zones de la courbe et fera diminuer les parties oranges. La
deuxième manière est de jouer sur la balance ombres/hautes lumières qui
donnera une importance à l'une ou l'autre de ces deux zones, ce réglage
s'applique  très bien  dans  le  cas où  seulement  une extrémité  est
écrêtée.

![Vue chambre noire](look.png?classes=shadow&height=500px)

Le contraste peut être augmenté tout en le maintenant en dessous de 1.5.
Au delà, l'écrêtage peut être trop important pour que les deux
précédents réglages le corrigent un minimum. Il faut aussi préciser que
l'écrêtage peut être aussi quelque chose de voulu et que tout n'est pas
à corriger. Chacun a son style de développement.

Il faut toutefois  voir que filmique RVB est un  module technique. Son
but est  de faire rentrer la  plage dynamique du cliché  dans la plage
dynamique  de l'écran.  Il  n'a  pas de  but  créatif.  C'est le  rôle
d'autres modules.

En ce qui concerne les autres onglets, il n'y a pas lieu d'y toucher
dans un cadre débutant.
