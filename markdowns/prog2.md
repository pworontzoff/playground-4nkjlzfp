# La Courbe du dragon - programmation 2

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

Amusons-nous à dessiner avec du code !

Ce que nous allons faire maintenant est très simple : faire tracer un segment de droite grâce à notre petit programme ci-dessous :

@[drawing_dragon_curve]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_curve"})

**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*
