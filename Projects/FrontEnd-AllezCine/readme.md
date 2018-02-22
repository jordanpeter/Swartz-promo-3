# Travail Intégration

- Repository : `frontend-AllezCine`
- Temps nécessaire : 2 semaines
- Travail : équipe

## Objectifs d'apprentissage
- respecter un design fourni
- consolider les acquis en git, HTML, CSS, Bootstrap
- utiliser javascript et jQuery dans un projet réaliste
- avoir un nouveau projet à ajouter à son portfolio

## Le Travail d'intégration Front-End

Ce TI conclut les deux mois de front-end que nous avons eus ensemble.
Vous avez **3 travaux en rendre**.
- Un site en ONE PAGE avec un design fourni ([yes !](layout-one-page.jpg)). [[Accès rapide]](#c-la-newsletter-bonus)
- Un site de fans (Design non fourni) [[Accès rapide]](#b-site-de-fans)
- Création d’une newsletter pour faire la promo des nouveautés sur votre site. [[Accès rapide]](#c-la-newsletter-bonus)

Pour cela, vous devez utiliser toutes les technos vues depuis le début, c’est à dire :
- HTML
- CSS
- JavaScript
- jQuery
- Responsive design
- Bootstrap
- Font Awesome Icons

**Avant toute chose**, sachez qu'il vous faudra rédiger un readme.md indiquant :
- la description du projet
- les noms des membres de l'équipe 

**Utilisation d'un kanban**

Utiliser l'onglet [Projects] de votre repo pour créer et organiser votre travail grâce à ceci :
![kanban](https://github.com/becodeorg/BeCode/blob/master/img/kanban.jpg)

Des colonnes "to do", "in progress", "done" pour faire simple et des tickets attribués aux bonnes personnes. Ceci pour vous/nous permettre de visualiser clairement et simplement l'avancement du projet.

## A . Site avec LAYOUT

Vous allez réaliser, en groupe, un site internet de location et vente des films. ATTENTION, il s'agit d'un site en **one-page** !

- [Cliquez ici pour voir le layout](layout-one-v2.jpg)
- On met également à votre disposition quelques affiches de films, histoire de vous faire gagner un peu de temps (les titres, années et genre sont dans les noms des images. De rien.)

### Entrée
Lorsqu’on entre dans le site, il faut **contraindre l’utilisateur à indiquer son âge**.
S’il a 18 ans et plus, l’autoriser à entrer sur le site, sinon le rediriger vers IMDB. (Pour cela utiliser JS ou jQuery pour un pop-up).

Une fois sur le site, faire apparaître n’importe où sur le site une box pour la **mise en garde de cookies**. (on en voit ces derniers temps partout sur le net)

 Lorsqu’on clique sur les boutons [login ou register], faire apparaître en JS ou jQuery dans une box un formulaire de connexion. (voir le site http://www.commeaucinema.com)
 Ce formulaire de connexion contiendra :
 - identifiant,
 - password,
 - un bouton [OK],
 - un bouton [Créer un compte],
 - un [rester connecté],
 - un lien [Si vous avez oublié votre mot de passe],
 - et un lien [cancel].
 Pour le formulaire register
 - nom
 - E-mail
 - Password
 - Confirm password
 - Conditions générales d'utilisation [bouton select]
 - Bouton Register

(Difficulté : faire disparaître le formulaire lorsqu'on clique sur CANCEL, sur le formulaire ou sur le bouton register, et vice versa ).

### Menu
Un **menu** en bootstrap avec des sous-menus. (**Menu hamburger pour le responsive**).

Comme c’est une onepage, les liens du menu doivent pointer vers les sections dédiées.

### En-tête
Le **jumbotron** de l'entête doit faire 100% de la largeur de l'écran dans lequel il y a un slide (Cf layout). Faire fonctionner le **slide** en CSS ou en JS ou jQuery)

### Les boutons réseaux sociaux
Les **boutons de réseaux sociaux** sont en position fixe. Si on clique sur un bouton, il doit s’allonger avec une animation (ici utilisez juste du CSS).

### Section Films
Chaque film doit comporter :
- une affiche,
- un titre,
- l’année de sortie,
- et le genre.

Si on clique sur l’image ou titre du film, faire apparaître dans un modal (Bootstrap) le trailer youtube du film, la description, le réalisateur, l’année de sortie du film, le genre, les acteurs…

### Section Featured Movies
Créer des boutons pour filtrer les films par genre (Jquery ou JS).
Si on clique sur le bouton ACTION par exemple, afficher uniquement les films d’actions, etc...

Lorsqu’on clique sur le bouton “plus des films”, afficher les autres films cachés. Faire disparaître le bouton “plus des films” et le remplacer par le bouton “Moins des films” si on clique sur “moins des films”, cacher les films et faire réapparaître le bouton “plus des films“  (En jQuery sera plus facile, avec un toggle par exemple).

### Section Shop Movie
Utiliser les deux petits boutons à droite pour faire défiler les films de gauche à droite et vise-versa (Jquery, bootstrap, JS au choix)

### Section Contact Us
Créer un formulaire (dans la page HTML, pas dans un pop-up). Faites en sorte que les entrées du formulaire s'affichent dans un pop-up lorsqu’on clique sur “Send Message”. (Pas de traitement en php, prochainement promis)

Bonus : mettre une map dans la section Contact us.


### Section Footer
Faites en sorte que lorsqu’on clique sur le petit bouton rouge avec la flèche blanche, on monte jusqu’à l'entête du site, le petit bouton disparaît une fois que l'entête apparaît.

CONTRAINTE : créer ce bouton en pur JS avec createElement(), createTextNode() et compagnie(), l’afficher sur le DOM, le positionner puis le styler en CSS dans la feuille de style.

FAITES QUE LE SITE SOIT RESPONSIVE (Bootstrap + Media queries)


## B. Site de fans
Il n'y a pas de layout imposé mais rien ne vous empêche de reprendre celui de site A.

Réaliser un site internet sur un personnage de ton choix (série télé, film, jeu vidéo,...). Le mieux étant que ce personnage soit cross-media (par exemple Batman est présent dans des films, dans des séries, des jeux vidéos, des comics,...) pour la partie "présentation". Tâchez de choisir un personnage qui soit dans au moins deux media.

Minimum 5 pages avec :
- **Présentation**
- **Biographie**
- **Photographies** (Galerie de photos du personnages),
- **Goodies** (page de simulation d'achat de produits dérivés),
- **Contact** (je vous fais pas un dessin)

**BONUS PAS OBLIGATOIRE** : Au lieu de faire 5 pages, faites 5 onglets et réalisez ce site sur une seule page web.

### Présentation
La particularité de cette page est qu'elle contiendra un sous-menu avec des onglets. Un onglet par medium dans lequel le personnage apparaît. (minimum deux onglets). Pour reprendre l'exemple de Batman, vous pourriez faire un onglet [Batman 1989] et parler brièvement de Batman dans ce film puis un autre onglet [Gotham] et parler brièvement de Batman dans cette série. Si vous n'êtes pas inspiré pour le contenu, vous pouvez reprendre du texte de wikipedia mais MENTIONNEZ VOS SOURCES ! (au moins dans le readme.md qui se trouvera obviously dans le repo de votre projet).

### Biographie
Il faudra que la vie du personnage soit “chapitrée” (exemple : "enfance, adolescence, vie d'adulte, fin de vie". OU encore "saison 1, saison 2, ..."). On devra cliquer sur le titre du chapitre pour dérouler le texte. Cela permettra d'éviter les spoilers. (par exemple avec une méthode toggle avec peut-être un paramètre de vitesse)

### Photographies
Réalisez une galerie de photos du personnage. Utilisez du jQuery pour rendre ça joli. Un caroussel, une lighbox,... Faites le code vous-même ou utilisez un plugin, faites comme vous voulez.

### Goodies
Une page avec une liste de produits dérivés avec le montant par pièce, un champs pour que l'utilisateur indique combien d'items il veut acheter. En cliquant sur le bouton [Prévisualisation avant achat], l'utilisateur voit le total de son achat. L'affichage se fait soit dans un pop-up (alert) ou dans la page HTML (prévoyez un emplacement pour l'affichage).
BONUS : Si le montant est inférieur à 15€, l'utilisateur devra payer 10€ de frais de livraison. Si le montant est compris entre 16€ et 30€, les frais s'élèvent uniquement à 7€. Si le montant de la commande s'élève à plus de 31€, les frais de livraison sont gratuits.

### Contact
Réalisez un formulaire de contact qui vérifiera que tous les champs sont remplis. Si les champs sont vides, attribuez-leur un fond de couleur pour les mettre en évidence et indiquez en dessous des champs vides une mention "ce champs doit être renseigné".

### Footer
Y mentionner
- les membres de votre équipe avec un lien vers les repos respectifs
- un lien qui mènera vers le site de location que vous avez réalisez (site A ^^)


**Conseils**

1. Réalisez d'abord le HTML, placez-y le contenu, ensuite écrivez les scripts nécessaires.
2. N'oubliez pas de bien :
- coder correctement votre HTML (les titres avec des h1, h2 ; les paragraphes dans des balises p ; ...). Un code bien organisé et toujours plus facile à traiter.
- nommer correctement vos ID. Utilisez des noms qui aient du sens, facile à vous situer sur votre page.

## C. La newsletter (BONUS)

Utiliser ce site https://putsmail.com/tests/new pour tester votre newsletter.
Vous pouvez utiliser les TABLES, ou du HTML5 (certains webmails acceptent du HTML5 mais mais mais attention avec du CSS)

Référence : [Voici une newsletter que j’ai reçu de la part de Yves Rocher](http://pictures.yvesrocher.com/NL/2017-06/06/be-fr/jun_6_be-fr_a2_online.html), s’inspirer à souhait et c’est essentiellement des tables.

Bonne chance et bon courage. (PS : on vous aime)

### REMARQUES :
Vous travaillez en groupe. Organisez-vous. Communiquez (rappelez-vous les bienfaits des réunions scrum).

Si vous avez des remarques ou des questions, n'hésitez pas à utiliser l'onglet [Issues](https://github.com/becodeorg/BXLAnderlecht/issues) de GitHub pour vous exprimer.

### Cat Tax : Maru

![Maru](https://s-media-cache-ak0.pinimg.com/736x/01/db/73/01db734bfbebad88776671495bc09cf5.jpg)
