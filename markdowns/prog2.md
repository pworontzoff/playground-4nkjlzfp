# La Courbe du dragon - programmation 2 - dessiner une deuxième marche d'escalier

## Réponse à la question pécédente

```
niveau 1 :         G
niveau 2 : G       G D
niveau 3 : GGD     G GDD
niveau 4 : GGDGGDD G GGDDGDD
```

<br>
Pour passer du niveau `3 au` niveau 4, on remarque que la première partie du chemin est égale au chemin du niveau précédent :
<br><br>

niveau 3 : `GGD G GDD`
<br>
niveau 4 : `GGDGGDD` G GGDDGDD
<br><br>
Ensuite, on a (toujours un "G" qui correspond au tout premier pli effectué)
<br><br>
Ensuite, on doit lire à l'envers (de droite à gauche) le chemin précédent et inverser les G et les D et on obtient la deuxième moitié du chemin !

<br><br>

## Dessiner avec du code : un segment de droite

<br>

Amusons-nous à dessiner avec du code !

Ce que nous allons faire maintenant est très simple : faire tracer un segment de droite grâce à notre petit programme ci-dessous !

Voici le programme qui permet de le faire :

@[drawing_dragon_1]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_1"})

Comme on le voit la commande

```C
draw(100);
```

permet de tracer un segment de droite de 100 pixels en partant du centre de la feuille et en traçant ver la droite.

Qui peut dire ce qu'est un pixel ?

## Dessiner avec du code : deux segments de droites

Voici maintenant un programme qui fait tracer un segment de droite vers la droite**, puis fait un virage vers la droite à 90° et 

Voici le programme qui permet de le faire :

@[drawing_dragon_1]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_1"})

Comme on le voit la commande

```C
draw(100);
```

permet de tracer un segment de droite de 100 pixels en partant du centre de la feuille.




**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*
