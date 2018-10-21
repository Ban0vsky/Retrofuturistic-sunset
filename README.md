DEVOIR DE DEVELOPPEMENT WEB DU 21/10/2018 CYRILLE BANOVSKY


INSPIRATIONS:
Pour ce devoir je me suis inspiré de pas mal de chose. A la base, je voulais faire une interface avec comme charte graphique metal gear solid, puis, pour une raison qui m'échappe encore, j'ai préféré m'orienter vers le retrofuturisme. Comme grande inspiration, j'ai donc le mouvement de la vaporwave, des films comme kung fury, des jeux comme hotline miami.

FEATURES:
Le site est séparé en deux grandes parties: le fond et le telephone.
Pour le fond, j'ai utilisé un rotate x sur une div et j'ai ensuite fait deux grilles différentes, composées de longues div, que j'ai animé à vitesse différente pour donner un effet de profondeur. Encore derrière ça, j'ai mis un dégradé pour faire le coucher de soleil et le soleil lui même "brille" avec un jeu de box shadow.
Pour la grille, je n'ai pas réussi à faire une animation qui loop parfaitement et qui est infinie. J'y suis donc allé un peu à la barbare, en mettant un keyframes d'une minute. Comme ça c'est fluide pendant une minute entière, et on a un léger rollback de la grille à la fin.

Le téléphone est également entièrement en 3D. Pour le fond du telephone en static, j'ai utilisé un canvas et du code que j'ai récupéré d'un codepen et adapté à mon besoin. Pour tout le reste, je voulais rajouter des interactions au sein du telephone, mais j'ai manqué de temps, malheureusement.

Pour l'animation du téléphone, tout le code js est de moi. J'ai par contre demandé de l'aide pour les calculs d'inclinaison en fonction de la souris.

Enfin, pour les palmiers, ils sont totalement en 3d CSS. Je les ai fait assez simplement: Pour le tronc, on a simplement un jeu de div ronde et de div en forme de trait pour rejoindre le tronc. L'avantage, c'est que j'ai gagné du temps avec cette technique, le désavantage c'est que si j'avais voulu texturer les palmiers, je n'aurais pas pu. 
Pour les branches en revanche c'était un peu plus compliqué: Les branches en elle-même étaient assez facile à réaliser, fallu une petite heure à toucher aux options de border de div pour trouver une forme qui me convenait. Par contre, pour disposer les feuiilles dessus, c'était bien plus compliqué: il a fallu que j'y aille à taton, en cherchant la disposition quii marche le mieux.
Une fois réalisés, je les ai intégré au code de base et je les ai animé "à la roublarde": ils n'apparaissent pas js, il y en a 4 dans une div quii avancent en boulant quasi parfaitement.


OPTIMISATION:
Je me suis débrouillé avec les will-change pour avoir un minimum de paint possible. Finalement, je n'ai qu'un élément qui paint en permanence et le reste ne bouge pas. Sur ma machine moyenne de gamme (i5 2500k et r9 290) je suis quasiment en 60fps constant. 


BUGS:
Mon bug principal est un bug d'affichage en css. C'est le translate des palmiers qui le produit, et j'ai eu beau traficoter avec les distances, je n'ai pas réussi à le résoudre.


Pour finir, La résolution optimale pour afficher le site est 1980x1200, mais il est adapté à la plupart des autre resolutions, et fonctionne même vaguement sur mobile (même si plusieurs features buggent), à ma grande surprise.

La résolution la plus petite à laquelle rien est cassée est 1320x790. Au dela, les palmiers commencent à flotter dans les airs et la grille commence à devenir de moins en moins visible.