# PHP

## Table des matières

- [Introduction](php-introduction.md) :point_left:
- [Variables](php-variables.md)
- [Conditions](php-conditions.md)
- Drill : [Exercices sur les Conditions](php-exercices-conditions.md)
- [Tableaux (array)](php-array.md)
- [Boucles](php-boucles.md)
- [Fonctions](php-fonctions.md)
- [Formulaires](php-formulaires.md)


## PHP : "Hypertext Preprocessor"
Logiciel qui tourne du côté **Backend**, c'est à dire au niveau du _serveur web_. (Le **Frontend** désigne à contrario ce qui se passe du côté _Client_ c'est à dire le _navigateur_).

PHP permet au Serveur Web de "réfléchir avant de parler" et en informatique, "réfléchir" c'est manipuler des informations et les retourner au Client (le navigateur) dans n'importe quel format (très souvent : du HTML, du XML, du JSON, voir du texte simple, du CSS, du javascript...).

## Pourquoi utiliser du PHP si cela retourne autre chose ?
Parce que cela vous permet de créer des pages de manière **dynamique** plutôt que **statique**.

Imagine que tu doives créer une page web permettant de dire "Bonjour !" à chacun des quelques 7 milliards d'habitants vivant sur Terre.
Cela signifie que tu dois créer 7 milliards de pages HTML telles que celle-ci, accessibles à une adresse url du style : http://citizens.net/humans/jose-garcia.html (c'est un exemple d'URL, il ne fonctionne pas vraiment).

```HTML
<html>
<head>...</head>
<body><h1>Bonjour José Garcia !</h1></body>
</html>
```
...Cela te prendrait des années. En plus, il te faudrait déjà en effacer (les décès) et en ajouter (les naissances)... Pas terrible.

Et si tu ne créais qu'un seul fichier (un "script php") à qui on envoie le nom de l'humain via l'adresse URL et qui "crée" le HTML dynamiquement ?

L'adresse URL deviendrait, par exemple,  http://citizens.net/humans/index.php?name=jose-garcia


```PHP
<html>
<head>...</head>
<body><h1>Bonjour <?php echo $_GET['nom']; ?>!</h1></body>
</html>
```

Il suffirait alors que chacun reçoive son URL personnalisé et voilà !


## Installation

### Serveur de développement / de staging / de production
Quand on développe, on ne travaille pas directement sur le serveur hébergeant le site ou l'application car la moindre faute de frappe pourrait provoquer une erreur et "casser" le site, incommodant des milliers de personnes. Pas bien...

Pour éviter cela, on travaille sur son propre ordinateur, c'est plus facile et cela permet de tester sans gêner personne. Cela permet aussi de travailler sans connexion internet (dans le train par exemple). C'est ce qu'on appelle un _environnement de développement local_  ou simplement un _serveur de développement_. Le serveur final est appelé lui un _serveur de production_. C'est lui que l'on rend accessible à tout le monde.
Il t'arrivera aussi de travailler avec un _environnement de staging_ présentant du code à faire valider avant sa mise en production.

### Installer un serveur de développement local
Il y a énormément de manière de faire cela, mais pour ces premiers exercices, il nous faut juste avoir un serveur permettant de jouer avec du PHP.
Cela tombe bien, PHP inclut un petit serveur de développement local. Il te suffit donc d'installer PHP sur ta machine et c'est fait !

#### 1. Installation :

`sudo apt install apache2 php mysql-server libapache2-mod-php php-mysql` 

n'oublie pas d'installer xampp 

`sudo chmod 755 xampp-linux-*-installer.run`

1. Pour lancer le serveur, il suffit de taper ceci dans le Terminal: 

 ``` cd opt/jenesaisplus/apache2 stop ``` 
 ``` cd opt/jenesaisplus/mysql stop ``` 
 ``` cd etc/xampp/xampp start ```

2. Pour créer ton premier fichier PHP, il te faudra aller dans le dossier htacess et le chmoder en 777 et par la suite tu pourras aller créer un dossier nommé comme ton projet et y mettre un index.php. Rédige "Hello !" que tu feras afficher dans un echo.

#### 2. A présent, ouvre ton navigateur à l'adresse http://localhost:80/tondossier

Tu devrais voir le sympathique message "Hello !" que tu t'es adressé. Tu viens de créer ton premier script en PHP. Fais-toi un gros câlin, tu l'as bien mérité.

![Giphy](http://media1.giphy.com/media/35gNg6o2HYjSg/giphy.gif)

### Exercices

- Prends quelques minutes et joue avec ton fichier index.php. Mets-y une image.
- Crée une deuxième page dans le même dossier (`cats.php`) et ajoute un peu de contenu et surtout un lien sur chacune des deux pages permettant de passer de l'une à l'autre.
- Fait ? Bravo, tu viens de créer ton premier site internet !
Voici un chaton pour fêter cela.

![Giphy](http://media0.giphy.com/media/nsMPhWK6bfxHq/giphy.gif)


Rendez-vous à la prochaine leçon : [Variables et Conditions](./php-variables.md).


