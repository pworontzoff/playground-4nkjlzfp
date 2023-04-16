# La Courbe du dragon - programmation 3 - 10 marches d'escaliers

## 2 marches d'escalier

Le programme qui permet de tracer 2 marches d'escalier est donc

@[drawing_dragon_4]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_4"})

**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*

N'y a-t-il pas des instructions qui se répètent ?

Avec nos programmes sur ce site, nous pouvons utiliser des boucles plutôt que de réécrire plusieurs fois les mêmes insctructions !

Nous pouvons écrire par exemple :

```C
repeat(2) {
draw(15);
turn(30,LEFT);
} loop;
```

plutôt que d'écrire 

```C
draw(15);
turn(30,LEFT);
draw(15);
turn(30,LEFT);
```

Ou bien nous pouvons écrire par exemple :

```C
repeat(5) {
draw(15);
turn(30,LEFT);
} loop;
```

plutôt que d'écrire 

```C
draw(15);
turn(30,LEFT);
draw(15);
turn(30,LEFT);
draw(15);
turn(30,LEFT);
draw(15);
turn(30,LEFT);
draw(15);
turn(30,LEFT);
```
C'est plus court à écrire et ça donne le même résultat !

## 2 marches d'escalier en boucle



## 10 marches d'escalier en boucle



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

@[drawing_dragon_curve]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_curve"})

**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*
