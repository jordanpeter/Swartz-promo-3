# MasterMind

## Objectif

- dÃ©velopper un mastermind en HTML - CSS - JS

## CrÃ©er un MasterMind

[RÃ©gles du jeux ici] (https://fr.wikipedia.org/wiki/Mastermind)
PrÃ©cision : pour le mode normal, la solution  = 4 couleurs diffÃ©rentes

### Le jeu

* CrÃ©er en HTML 3 div (minimum - vous pouvez faire comme vous voulez)
	- une pour l'historique des rÃ©ponses
	- une pour les rÃ©ponses actuelles
	- une pour le choix des couleurs (placer 6 ronds de couleurs diffÃ©rentes)

* En JS : faire en sorte que quand on clique sur une couleur, elle se place dans la div des rÃ©ponses.

* Faire en sorte que quand les 4 couleurs sont placÃ©es dans la div rÃ©ponse, elles se dÃ©placent dans la div historique.

* Il faut que quand les couleurs arrivent dans l'historique, sur la droite, s'affiche des boules noires ou blanches qui indiquent si :
	- elles sont bien placÃ©es
	- elles sont juste mais pas au bon endroit

PS : il ne faut pas que les boules noires et blanches soient dans le mÃªme ordre que les boules de couleur (sinon c'est trop facile)

Astuce : faire apparaÃ®tre d'abord les boules noires puis les boules blanches.

* Faire une fonction qui crÃ©er une solution automatique Ã  chaque dÃ©but de partie. (utiliser le random)

### Astuce

* Utiliser le innerHTML et autres
* Utiliser une class "rond" et juste modifier le background-color (pour les dÃ©placements dans les diffÃ©rentes div)


### Bonus

* Faire en sorte que quand on se trompe on puisse retirer les couleurs des rÃ©ponses actuelles.
