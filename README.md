# Best API challenge

> Quelle sera la team à afficher en premier SON logo ? 


## Objectif :

Afficher SON logo sur l'écran, le plus rapidement possible 
(plus de détails dans le thread) 

## Challenge :

Plusieurs possibilités de gagner :
- être la première team a avoir un livrable fonctionnel
- être la team à avoir l'API la plus rapide à répondre aux requêtes 
- être la team à avoir l'API la robuste aux tests de charge


## Plus de détails sur le déroulement du challenge :

Le challenge sera en 2 temps in cha Allah : 
1. Construction des interfaces front end (team web VS team mobile). Ici le gagnant du challenge frontend sera qui aura livré en premier une solution fonctionnelle 
2. Construction des APIs (teams backend splités en fonction des différents langages). Ici 3 gagnants possibles : 
   - la team la plus rapide à livrer
   - la team ayant l'API la plus rapide 
   - la team ayant l'API qui supporte le mieux à un test de charge 

### Mode visuel :

La team front doit faire une page web dans le navigateur / une app mobile qui affiche un cadre quadrillé avec N x N pixels (100x100 par exemple). 
Pour chaque backend qui va être fait, on va avoir un thread au niveau du front qui va choisir un pixel au hasard dans le quadrillage, et envoyer ses coordonnées à l'API.

C'est là où la team backend intervient : chacune des teams backend devra faire une API avec une route qui va prendre en input des coordonnées (exemple : x=12 et y=34). Le serveur interrogera sa base de données qui stocke le logo de son langage (avec le même quadrillage carré) et renverra le code couleur hexadécimal de cette coordonnée particulière au front (exemple : #123456). 

Donc une fois que le front récupère la couleur, il l'affiche sur son quadrillage, et dès que c'est fait, il refait une demande au backend aussi tôt sur une autre coordonnées qu'il aura choisi de manière aléatoire.

A la fin, le serveur le plus rapide correspondrait au logo imprimé sur le cadre quadrillé

### Mode test de charge :

Dans ce mode là, le front va faire appel (de manière beaucoup plus intensive) une des APIs, avec par exemple 60 rps.
Le retour de l'API ne sera pas forcément utilisé par le front, par contre le front devra calculer à chaque fois le temps qu'aura mis l'API pour répondre, et afficher la moyenne à l'écran.
Les APIs sont testés 1 par 1, et l'API ayant le temps de réponse moyen le plus bas aura gagné cette partie duchallenge.

## Règles :

 - Les participants n'auront le droit de coder seulement durant les sessions de live coding 
 - Mise en cache interdite
