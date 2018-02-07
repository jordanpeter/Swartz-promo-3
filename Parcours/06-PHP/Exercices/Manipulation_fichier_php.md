# Manipulation fichier en php.

Beaucoup de personnes qui commence le php se demande comment marche les fichiers en php. Alors j’ai fait un petit récapitulatif de ce que je sais faire et j'espère que cela va vous aider.

## Fichier : 

**Ecrire et créer un fichier c'est assez simple en général : pour cela on utilise** 
```
$fp = fopen("nom du fichier","mode");
```

Pour le nom du fichier prenons texte.txt, le mode correspond à ce que l'on veut faire : 
* **"r"** pour indiquer la lecture et 
* **"a"** ou **"w"** pour l'écriture. 
* **"a"** signifie qu'on ouvre et on se place à la fin du fichier et 
* **"w"** au début. 

A ces trois lettres on peut rajouter le signe **"+"** pour indiquer qu'il faut créer le fichier s'il n'existe pas. 
Pour les fichiers de type binaire on rajoute aussi **"b"**, donc 
```
$fp=fopen("texte.txt","w+"); 
fclose($fp); 
```

va créer un fichier texte.txt. Pour l'instant le fichier est vide. 
_Remarquez qu'un fois qu'on a fini de travailler sur un fichier, on le ferme avec **fclose()**_; 

**Disons que je veuille rajouter dans ce fichier un texte** : 
```
$texte="Mon premier ajout"; 
$fp=fopen("texte.txt","a"); 
fwrite($fp,"$texte"); 
fclose($fp);
```

Voila mon fichier texte.txt contient du texte. 

### Voyons d'autres méthodes d'ajout : 
On peut aussi utiliser aussi **fputs()**; 
```
$fp=fopen("texte.txt","a"); 
fputs($fp," est :"); 
fputs($fp,"\n"); 
fputs($fp,"cette portion de texte."); 
fclose($fp); 
```

On voit ici que **fputs($fp,"\n");** sert à sauter une ligne. 
Il existe **fseek();** qui permet de deplacer le pointeur ou on veut dans le fichier. 

### Voyons maintenant comment récupérer les infomations contenues dans le fichier "texte.txt" 

Pour lire le fichier tous simplement on fait : 
```
$fp = fopen("fichier.txt","r"); 
```

Apres tout dépend de ce qu'on veut récupérer : 
**fread();**peut récupérer la quantité de caractères qu'on veut. 
```
$fichier_texte=fread($fp,"11"); 
echo"$fichier_texte"; 
```

ceci provoquera l'affichage de "Mon premier", il y a ausi **fgets();** 
```
$fichier_texte=fgets($fp,1024); 
echo"$fichier_texte"; 
```

**fgets();** prend la ligne complète soit "Mon premier ajout". 
#### Pour avoir tout le contenu on peut par exemple parcourir le fichier ligne par ligne 
```
while(!feof($fp)) 
{ 
$fichier_texte=fgets($fp,1024); 
echo"$fichier_texte"; 
} 
```

Ou encore extraire tous les n charactères sur la totalité du fichier (ici n=10) 
```
while(!feof($fp)) 
{ 
$fichier_texte=$fichier_texte=fread($fp,"10"); 
echo"$fichier_texte"; 
} 
```

Ou pour finir, récupérer tout d'un coup avec fread() connaissant la taille du fichier. 
Pour cela on utilise **filesize();** : 
```
$taille=filesize("texte.txt"); 
$fichier_textel=fread($fp,$taille); 
```
## Voyons maitenant quelques fonctions appliquer aux fichiers 

* **copy($source, $dest)**
Copie le fichier $source vers $dest et retourne true si succès ou false si echec 

* **rename($source, $dest)**
Renomme le fichier $source en $dest et retourne true si succès ou false si echec 

* **unlink($file)**
Supprime le fichier $file et retourne true si succès ou false si echec 

* **mkdir($dir, $mode)** 
Créée le dossier $dir avec les droits unix $mode (exprimés en octal) et retourne true si succès ou false si echec 

* **rmdir($dir)**
Supprime le dossier $dir et retourne true si succès ou false si echec 

* **fileatime($file)**
Retourne la date à laquelle le fichier $file a été accédé pour la dernière fois ou false si échec 

* **filectime($file)**
Retourne l'heure à laquelle le fichier $file a été accédé pour la dernière fois ou false si échec 

* **filemtime($file)**
Retourne la date de dernière modification du fichier $file ou false si échec 

* **fileperms($file)**
Retourne les permissions associées au fichier $file ou false si échec 

* **filesize($file)**
Retourne la taille du fichier $file (en octets) ou false si échec 

* **filetype($file)**
Retourne le type du fichier $file (fifo, char, dir, block, link, file, unknown) ou false si échec 

* **is_dir($file)**
Retourne true si $file est un répertoire ou false sinon 

* **is_executable($file)**
Retourne true si $file est exécutable ou false sinon 

* **is_file($file)**
Retourne true si $file est un fichier ou false sinon 

* **is_link($file)**
Retourne true si $file est un lien symbolique ou false sinon 

* **is_readable($file)**
Retourne true si $file est accessible en lecture ou false sinon 

* **is_writable($file)**
Retourne true si $file est accessible en écriture ou false sinon 

* **touch($file)**
Change la date de dernière modification du fichier $file en maintenant 

## En bonus :

#### Vérifier l'existence d'un fichier : Permet de vérifier si un fichier ou non. 
```
$fichier="fichier.txt"; 
if(file_exists("$fichier")) 
{ echo "Le fichier existe ..."; } 
else { echo "Le fichier n'existe pas !"; 
} 
```

### Statut d'un fichier : Evoque les differents droits sur un fichier 
```
$fichier="fichier.txt"; 

if (is_readable("$fichier")) { 
echo "Le fichier peut être lu"; } 
else { echo "Le fichier ne peut pas être lu !";
} 

if (is_executable("$fichier")) { 
echo "Le fichier peut être exécuté"; } 
else { echo "Le fichier ne peut pas être exécuté !";
} 

if (is_writable("$fichier")) { 
echo "On peut écrire dans ce fichier"; } 
else { echo "Ecriture impossible dans ce fichier !";
} 
```
#### Compteur grâce au fichier texte : Voici un petit compteur tout bête. 
```
$fp = fopen("compteur.txt","r+"); 
$nbvisites = fgets($fp,255); 
$nbvisites++; 
fseek($fp,0); 
fputs($fp,$nbvisites); 
fclose($fp); 
echo"Vous êtes le $nbvisites visiteurs";
```

On onvre en lecture et écriture, puis on met dans la variable $nbvisites les 255 premiers caratères, on y ajoute 1. 
Ensuite on se place au début du fichier, on crée le résultat et on n'oublie pas de fermer.

# Bon LOL
