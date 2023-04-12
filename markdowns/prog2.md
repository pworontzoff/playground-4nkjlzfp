# La Courbe du dragon - programmation 2

## Réponse à la question pécédente

```
niveau 1 :         G
niveau 2 : D       G G
niveau 3 : DDG     G DGG
niveau 4 : DDGDDGG G DDGGDGG
```
<br>
Pour passer du niveau 3 au niveau 4, on remarque que la première partie du chemin est égale au chemin du niveau précédent :
<br><br>
niveau 3 : **DDG&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;G DGG**
<br>
niveau 4 : **DDGDDGG** G DDGGDGG
<br><br>
Ensuite, on a (toujours un "G" qui correspond au tout premier pli effectué)

Ensuite, on doit lire de gauche à droite le chemin précédent et inverser les G et les D et on obtient la deuxième moitié du chemin !



@[drawing_dragon_curve]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_curve"})

**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*
