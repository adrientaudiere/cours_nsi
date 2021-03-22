# DÉCOUVRIR LE LANGAGE PYTHON <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

!> !! Work in progress !!

## IDE

Sur vos machines plusieurs IDE sont déjà installés (listés du plus simple au plus complet)

- IDLE
- Tonny
- Anaconda (une suite de logiciel dont le logiciel Spyder)
- VScodium (que nous utiliserons sans doute plus tard)


## Comprendre python avec des tortues 

?> Réaliser ces [exercices](https://hourofpython.trinket.io/a-visual-introduction-to-python#/welcome/an-hour-of-code) en ligne** :











--- Cours MANDON ----------------------



I.  Les bases du Python.

    1.  Commentaires.

Les commentaires sur une ligne, ou en fin de ligne, commencent par \# ;
ils sont indispensables pour la compréhension, la réutilisation
ultérieure et la relecture d'un programme.

On peut mettre des commentaires de plusieurs lignes entre triples
guillemets : \"\"\"...\"\"\"

Pour des raisons de compatibilité sur les différents systèmes, évitez
les accents ainsi que tous les caractères spéciaux dans les noms de
variables (cf. ci dessous). Vous pouvez en mettre dans les commentaires.

I.  1.  Expressions.

Outre les opérations arihtmétiques standard, on dispose des opérateurs
suivants:

-   //
-   \%
-   \*\*

I.  1.  Variables

> Le nom des variables suit quelques règles de base :

-   un nom de variable est une suite de lettres (a → z , A → Z) et/ou de
    chiffres (0 → 9), qui doit toujours commencer par une lettre ;

<!-- -->

-   seules les lettres ordinaires sont autorisées. Les lettres
    accentuées, les cédilles, les espaces, les caractères spéciaux tels
    que \$, \#, @, etc. sont à proscrire, à l'exception du caractère \_
    (tiret bas ou underscore) ;
-   la casse est significative (les caractères majuscules et minuscules
    sont distingués). Par exemple, **Nombre, nombre, NOMBRE sont des
    variables différentes. Soyez attentifs !**
-   prenez l'habitude d'écrire l'essentiel des noms de variables en
    caractères minuscules (y compris la première lettre). Il s'agit
    d'une simple convention, mais elle est largement respectée.
    N'utilisez les majuscules qu'à l'intérieur même du nom, pour en
    augmenter éventuellement la lisibilité, comme dans
    **nomDeFamille**. Par contre, si vous utilisez le nombre 
    souvent, c'est une constante ; on écrira alors la variable
    correspondante en majuscules PI = 3.14159.
-   N'hésitez pas à donner des noms clairs à vos variables. Par exemple,
    nomDeFamille est plus clair que nf.
-   De plus, les variables ne peuvent pas être un des « mots
    réservés » suivant utilisés par le langage lui-même :

and asassert break class continue def del

elif else exceptexec Falsefinally for from global

if importin is lambdaNonenonlocalnot or pass

print raise return Truetry whilewithyield

I.  1.  Booléens

Les booléens sont des variables qui ne prennent que deux valeurs : vrai
ou faux (True et False respectivement en Python, avec des majuscules)

Les variables booléennes sont utilisées pour les tests lors des boucles
ou des conditionnelles. On peut les combiner à l'aide des connecteurs
logiques : et, ou, non qui sont en Python and, or, not.

*Opérateurs de comparaison* :

x == y*\# x est égal à y*

x != y*\# x est différent de y*

x \> y*\# x est plus grand que y*

x \< y*\# x est plus petit que y*

x \>= y*\# x est plus grand que, ou égal à y*

x \<= y*\# x est plus petit que, ou égal à y*

Opérateurs logiques :

a and b\# « et » mathématique

a or b\# « ou » mathématique

not(a)\# « non » mathématique

I.  1.  Typage

Au paragraphe précédent, on a vu les variables de type « booléen ».
Toutes les variables ont un type ; voici ci-dessous les types
*simples* :

-   int : nombre entier
-   float : nombre décimal (nombre à virgule « qui se finit »). On ne
    peut pas réprésenter en machines des nombres réels « compliqués »
    comme  ou ![](./ObjectReplacements/Obj100){width="0.681cm"
    height="0.681cm"} , on en a juste des approximations
-   str : chaîne de caractères, comme « bonjour le monde ». Les chaînes
    de caractère sont entre guillemets simples ou doubles \"bonjour le
    monde\" ou 'bonjour le monde'
-   bool : booléens

Le type d'une variable est obtenu avec l'instruction type(var).

Exemple :

\>\>\> a = \"coucou\"

\>\>\> type(a)

\<type \'str\'\>

On peut forcer une variable d'un type à devenir une variable d'un autre
type ; attention cela peut causer des erreurs ! Pour changer le type
d'une variable, on utilise le type que l'on veut affecter :

Exemple :

\>\>\> a = 23.1

\>\>\> type(a)

\<type \'float\'\>

\>\>\> a = str(a)

\>\>\> a

'23.1'

\>\>\> b = 23.1

\>\>\> b = int(b)

\>\>\>b

23

\>\>\> c = "bonjour"

\>\>\> int(c)

Traceback (most recent call last):

File \"\<ipython-input-20-089eb950f64f\>\", line 1, in \<module\>

 int(c)

ValueError: invalid literal for int() with base 10: \'bonjour\'

*Quelques opérations sur les chaînes de caractères données par des
exemples *:

Les chaînes de caractères sont un type particulier de liste, que l'on
verra ultérieurement plus en détail.

-   La *concaténation et la répétition* :

\>\>\> a = \"j\'aime \"

\>\>\> b = \"pas \"

\>\>\> c = \"les mathématiques\"

\>\>\> print(a+c)\# concaténation

j'aime les mathématiques

\>\>\> print(3\*b)\# répétition

paspaspas

-   Longueur d'une chaîne de caratères :

\>\>\> len(\"j\'aime \")

7\# *Comptez bien tous les caractères !*

-   Obtenir un caractère ou un morceau d'une chaîne de caractères :

\>\>\> a = \"bonjour\"

\>\>\> len(a)

7

\>\>\> a\[0\]

'b'

\>\>\> a\[6\]

'r'

\>\>\> a\[7\]

Traceback (most recent call last):

 File \"\<ipython-input-7-9cf13ba20553\>\", line 1, in \<module\> a\[7\]

IndexError: string index out of range

Comment fonctionne le comptage des caractères ?

\>\>\> a\[1 :3\]

'on'

Quels sont les indices (numéros) des caractères affichés dans cette
commande ?

I.  1.  Instructions conditionnelles

Le « si *condition* alors *instruction* (sinon *instruction*) » se
traduit par :

if *condition* :

 *instruction 1*

(else :)

 instruction 2

suite du programme

Vous remarquez l'indentation, c'est à dire le fait que l'instruction est
décalée vers la droite (en général de 4 espaces). Ceci traduit le fait
que l'instruction 1 sera exécutée uniquement si la condition dans le
« si » est vraie, l'instruction 2 étant exécutée uniquement si la
condition est fausse. Bien sûr, l'instruction 1 peut être formée de
plusieurs instructions élémentaires. Si l'on imbrique plusieurs « si »,
alors on indentera à chaque fois les instructions. N'oubliez pas les
« : ».

L'ensemble if *condition* : *instruction 1* forme une instruction
composée.

La condition évalue un booléen, cf. notebook nsi\_1\_2\_controle.ipynb.

L'instruction « if...elif...elif...etc...(else :) » permet de choisir
entre plusieurs alternatives (elif est la contraction de else if)

I.  1.  Instructions répétitives

Le « tant que » est traduit par :

while *condition *:

*instruction*

suite du programme

Même remarque sur l'indentation, ainsi que sur la condition qui est un
booléen, qu'au paragraphe précédent

Le « pour » est traduit par :

for *variable* in *séquence* :

*instruction 1*

suite du programme

Par exemple, « for i in range(0, 10, 3) : » exécutera l'instruction 1
pour les valeurs de *i* respectivement égales à 0, 3, 6, 9. Si on écrit
range(0, 10) , alors *i* prend toutes les valeurs de 0 à *9* (10 exclu).

Lorsque l'on a une condition compliquée à tester pour sortir d'une
boucle par exemple, il est souvent pratique d'utiliser un booléen
(exemple : un jeu que l'on peut finir de plusieurs manières à
l'intérieur de la boucle, cf. exercice « deviner un nombre »). Dans ce
cas, si « continuer » est le nom de la variable booléenne, on écrit
« while continuer », et non « while continuer == True » qui est un
pléonasme informatique !

*Remarque :* de nombreux programmes utilisent l'instruction break pour
sortir d'une boucle, voire d'un test. Cette instruction est à éviter
autant que possible, pour des raisons de bonnes pratiques de
programmation. En effet elle rend les programmes moins lisibles, et est
source d'erreurs difficilement corrigeables. Au lycée, sans interface
graphique, il n'y a *aucune* utilisation nécessaire de cette
instruction. En conséquence, elle vous est interdite d'usage. Vous devez
néanmoins savoir qu'elle existe. Quel que soit le niveau, l'utiliser
avec un for ou un if est de la mauvaise programmation. Avec un while, on
voit des exemples comme suit :

+-----------------+-------------------------------+--------------------+
| while True :    | Que l'on peut remplacer par : | var\_bool = True   |
|                 |                               |                    |
|  if condition : |                               | while var\_bool :  |
|                 |                               |                    |
|  break          |                               |  if condition :    |
|                 |                               |                    |
|  \...           |                               |  var\_bool = False |
|                 |                               |                    |
|                 |                               |  else :            |
|                 |                               |                    |
|                 |                               |  \...              |
+-----------------+-------------------------------+--------------------+

I.  1.  Modules

Une bibliothèque (ou un module) est un ensemble de fonctions
préprogrammées, ainsi le programmeur n'a pas à les refaire.

On inclut une bibliothèque dans un programme à l'aide de la commande
« import ».

Nous utiliserons les bibliothèque « math », qui permet de calculer des
cosinus, des racines carrées, des valeurs absolues... et la bibliothèque
« random », qui permet d'obtenir des nombres aléatoires. Ultérieurement,
nous utiliserons également des bibliothèques graphiques pour les
interfaces.

On tape si nécessaire en début de programme :

\>\>\> from math import \*

\>\>\> from random import \*

I.  1.  Lisibilité des programmes et fonctions

Pour être lisible, un programme doit être structuré en fonctions, que
l'on écrira au début du programme. Lorsque l'on réfléchit à un problème
que l'on veut programmer, il faut le faire en termes de fonctions : « je
veux d'abord une fonction qui me permet de rentrer mes données », « je
veux une fonction qui teste si une variable est positive et dans ce cas
calcule sa racine carrée » etc...

Les fonctions ressemblent à ce que vous utilisez en mathématiques quand
vous écrivez ![](./ObjectReplacements/Obj101){width="1.669cm"
height="0.751cm"} . Vous avez en *paramètre d'entrée* un nombre *x*, une
fonction qui fait « un truc », et en *paramètre de retour ou de sortie*
un nombre *y*, résultat de la fonction. En informatique on peut avoir 0,
1 ou plusieurs paramètres d'entrée, et de même en sortie.

La syntaxe pour les fonctions est :

def *nom\_de\_fonction* (*variables passées en paramètre, à utiliser
dans la fonction*)* *:

instructions

return (*variable*)

L'appel dans le programme se fait par :

*variable\_resultat *= *nom\_de\_fonction *(*variables à passer en
paramètre*)

Exemple : le programme suivant teste vos capacités en calcul mental

\# F. Mandon

\#

\# Programme de test de connaissance sur les tables de multiplication

\# bibliotheques

from random import \*

\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

\# 

\# Fonctions

\#

\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

def alea10():

\"\"\"

Choix d\'un nombre aléatoire entre 2 et 10

\@param : aucun paramètre d'entrée

\@return n : entier n ≥ 2 et n ≤ 10

\"\"\"

n = randint(2,10)

return (n)

def testTable(x,y,z):

\"\"\"

Teste si le produit de deux nombres est égal à un troisième

\@param x, y, z : trois nombres (a priori de type entier, mais ce n'est
pas obligatoire)

\@return gagne : booleen, qui vaut Vrai si z = x\*y et Faux sinon

\"\"\"

if z == x\*y:

 gagne = True

else:

 gagne = False

return(gagne)

\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

\#

\# Programme principal

\#

\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

a = alea10()

b = alea10()

print(\"Que vaut le produit de \",a,\" par \",b,\" ?\")

c = int(input())

juste = testTable(a,b,c)

if juste:

 print(\"Bravo !\")

else:

 print(\"Lamentable\...\")

Dans le code, on met tous les import en premier, puis toutes les
fonctions, puis le programme principal.

Vous remarquez que les fonctions sont commentées (on dit *spécifiées*),
on indique d'abord leur nom, puis les noms et types des variables
passées en paramètre (avec d'éventuelles restrictions), et enfin le(s)
nom(s) et type(s) de la/des variable(s) renvoyée(s). Les spécifications
sont mises entre triples guillemets.

On peut préciser dans les commentaires la « stratégie » de la fonction,
si elle est un peu compliquée. La spécification est *indispensable*. Il
est préférable de taper les commentaires au fur et à mesure, pendant que
l'on sait ce que l'on vient de faire... Il est même fréquent de le faire
avant de construire la fonction, en laissant cette dernière vide si elle
est compliquée à faire !

A terme, vous devez dans les spécifications :

-   Définir l'objectif de la fonction
-   Identifier les paramètres de la fonction : ce qui est en entrée, ce
    qui est en sortie
-   Choisir un nom de fonction clair
-   Choisir des noms de variables clairs
-   Donner les types des paramètres, et préciser s'il y a des conditions
    dessus (on parle de préconditions pour les paramètres d'entrée et de
    postconditions pour les paramètres de sortie).

Les variables crées à l'intérieur des fonctions sont *locales*,
c'est-à-dire qu'elles n'existent pas en dehors des fonctions. Si dans le
programme précédent donné en exemple, vous faites un print(z) dans le
programme principal, il y aura une erreur.

*Remarque* : évitez les petites blagues qui consiste à donner des noms
rigolos, mais ne facilitent pas la compréhension

def ensedelephant (var icelle)... pour une fonction qui calculerait
l'écart entre deux dates ne rend pas les choses très claires !
