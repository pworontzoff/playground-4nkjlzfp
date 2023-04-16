# La Courbe du dragon - programmation 4 - 10 premiers virages de la courbe du dragon niveau 4

## Rappel

Au niveau 4 (avec 4 plis), dans la courbe du dragon, nous avions 15 virages :

```
niveau 1 :         G
niveau 2 : G       G D
niveau 3 : GGD     G GDD
niveau 4 : GGDGGDD G GGDDGDD
```

Et nous avons fait 10 marches d'escaliers en écrivant : 

```C
    repeat (10) {
		draw(50);
		turn(90,RIGHT);
		draw(50);
		turn(90,LEFT);
    } loop;
```

Nous allons maintenant passer au niveau supérieur, notre programme va intégrer du code en plus qui permet de dessiner la courbe du dragon :

@[drawing_dragon_7]({"stubs": ["main.c"],"command": "sh /project/target/run.sh", "project" : "drawing_dragon_7"})

**! Vous pouvez appuyer sur "Run" pour exécuter ce code et visualiser le dessin obtenu.**

*NB : si vous obtenez l'erreur "Unable to open static viewer" ou si rien ne s'affiche, ce n'est pas grave, il faut juste insister sur le bouton "run" (ou "success") et ça devrait finir par fonctionner.*

Dans ce programme, nous avons toujours 10 marches d'escaliers, mais nous avons également :

init_dragon();

qui permet de construire une liste de nombres 0 ou 1 qui indiquent s'ils faut tourner à gauche ou à droite.

On peut le voir comme une suite de 'D' ou de 'G' pour indiquer à la fourmi s'il faut tourner de 90° vers sa gauche ou vers sa droite.

Et nous avons également un moyen de savoir s'il faut tourner à gauche ou à droite selon le numéro du virage en utilisant le code suivant :

```C
G_OU_D(chemin, i) == DROITE
```

Ceci sera VRAI quand il faut tourner à droite et FAUX quand il faut tourner à gauche.

Or, en programmation, 