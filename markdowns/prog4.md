# La Courbe du dragon - programmation 4 - 10 premiers virages de la courbe du dragon niveau 4

## Rappel

Au niveau 4 (avec 4 plis), dans la courbe du dragon, nous avions 15 virages :

```
niveau 1 :         G
niveau 2 : G       G D
niveau 3 : GGD     G GDD
niveau 4 : GGDGGDD G GGDDGDD
```

Et nous avons fait 10 marches d'escaliers...

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

@[drawing_dragon_7]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_7"})

**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*
