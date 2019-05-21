Consignes :

- Créer la variable $texte et assigner la valeur "Du texte est stocké"

- Ecrire à la suite un echo affichant le contenu de la variable $texte

- Declarer une seconde variable appelée y ayant pour valeur 30

- Afficher dans un echo le contenu de la variable y à l'intérieur ( à la fin du texte ) du texte suivant "y vaux "

- Creer à la suite deux variables : $m et $n, leur assigner respectivement les valeurs 5 et 7 , puis afficher l'expression
$m + $n en utilisant echo

- Creer une variable $prenom qui a pour valeur ton prénom, à la suite utiliser echo pour afficher sous ces différentes formes :
. En utilisant {$prenom} et des ""
. En utilisant $prenom et des ''
. En réalisant une concatenation et des '', écrire Mon prénom est $prenom


#
# Théorie :
#

En php, vous pouvez déclarer et utiliser des variables, les variables stocke des données, des valeurs.

Pour indiquer à php que nous souhaitons déclarer une variable, on utilise le signe "$"

Exemple :

$data = "du texte";

$data = 5;

Lorsque vous assignez du texte à une variable, vous utiliserez " ", lorsque vous déclarez un nombre,
ceci n'est pas nécessaire.


En php , une variable ne peut pas démarrer par un nombre, ainsi $16f = "avion" retournera une erreur mais $f16 = "avion"
fonctionnera.

Pour rappel, les noms de variables sont sensibles à la casse : $variable est différent de $VARIABLE


- Afficher le contenu d'une variable :

 Pour afficher le contenu d'une variable, vous pouvez utiliser l'instruction "echo", exemple :

 $texte = "Bonjour";

 echo $texte;

 echo "Du texte normal, ensuite affichage de la variable $texte";

 echo "Du texte normal, puis affichage de la variable ".$texte." et on continue à ecrire du texte à la suite ...";


En php , nous utilisons les "." pour séparer les chaines de caracteres des variables, on appelle cela la Concatenation.


On peut également écrire les variables à l'intérieur d'une expression en utilisant {$variable}? ce n'est pas obligatoire mais cela rends votre code plus lisible, exemple :

echo "{$texte} tout le monde !";


#
# A savoir
#


- Portée des variables :

Comme en javascript, les variables en php peuvent avoir une portée globale ( disponible en dehors des fonctions ) ou locale
( disponible uniquement à l'intérieur d'une fonction )

Pour modifier la portée d'une variable, il est également possible d'utiliser le mot clef "global", exemple :

$x = 5;

function machin()
{
    global $x;
    echo $x;
}

La variable $x sera accessible depuis la fonction machin car le mot clef global a été utilisé.


- Variables Statique :

Le mot clef static suivi d'une variable permet de déclarer une variable dont la valeur ne sera pas réinitialisé, exemple :

function mafonction()
{
static $x=0;
echo $x;
$x++
}

Dans cette fonction, la variable x va valoir 0 lors du premier appel de la fonction puis elle va être incrémentée de 1
A la prochaine execution de la fonction, $x vaudra 1 car la variable va conserver sa derniere valeur connue.


