# :fa fa-project-diagram: Bases de la programmation <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

##  Pseudo-code : les instructions principales d'algorithmique.

Pour écrire un algorithme il est souvent plus simple de passer par une étape d'écriture en pseudo-code avant de coder à proprement parler dans un langage de programmation choisis. Nous détaillons ici les instructions principales d'algorithmique et leur écriture en pseudo-code (avec des exemples en français et en anglais) ainsi que leur implémentation en python comme exemple de programmation.

**Affectation de variables (symbolisées par <-, -> , :=, voir =)**

```pseudo-code
Ma_variable <- 5
Ma_variable2 = 10
```

```python
Mon_age = 82
```

**Instruction répétitive (boucle _for_, pour)**

```pseudo-code
Pour 'variable de valeur de début à valeur de fin' faire [...] fin pour
For X in Y...Z do [...] end
```

```python
for i in range(10):
    print(i)
```

**Répéter une action jusqu'à une condition (boucle _while_, tant que)**

```pseudo-code
Tant que 'condition' faire [...]
While X>Y do [...]
```

```python
i=10
while i > 0:
    print(i)
    i = i-1
```

**Instruction conditionnelle**

```pseudo-code
Si condition1 alors [...] sinon si condition2 alors [...] sinon [...] fin si
If X>Y do [...] else if [X>Z] do [...] else do [...]
```

```python
X=2
Y=6
Z=X+Y
if X>Y:
    print('X > Y')
elif X>Z:
    print('X > Z')
else:
    print('You loose')
```

**Entrée/sortie**

```pseudo-code
Lire un fichier / Read file
Lire une entrée clavier /  Read input
Afficher à l'écran / Print
```

```python
mon_fichier = open('filename')
mon_mot = input()
print(mon_mot)
```

Un script en pseudo-code permet d'utiliser tous les ingrédients (que nous verrons au fur et à mesure du cours) d'un programme informatique :

- des **données** sous forme de constantes (non modifiables) ou de variables (modifiables),
- des **opérateurs** arithmétiques (+, -, / …), relationnels (==, !=, > …) et logique (et, ou, …),
- des **expressions** (par ex. b/a),
- des **instructions** (par ex. des affectations x <- b/a),
- des **fonctions** qui automatisent les tâches répétitives.

## Quelques notions de base sur la programmation

Un **programme informatique** est un ensemble d'opérations destinées à être exécutées par un ordinateur. Un programme peut être écrit dans une ou plusieurs langages de programmation et peux être constitué d'un ou de plusieurs (parfois plusieurs centaines de milliers) de fichier.

### Les différents types de langage de programmation

Un ordinateur ne « comprend » que les suites de 0 et de 1, on parle de
langage binaire ou **langage machine**. Mais aucun humain ne parle le
langage machine. Au cours de l'histoire de l'informatique, les humains
ont inventé des langages qui utilise des instructions qui sont
**traduites** en langage machine (en suite de 0/1) grâce à un programme
que l'on appelle **l'interpréteur** (convertit le programme ligne par
ligne, ) ou le **compilateur** (analyse le programme dans son ensemble
avant de le convertir).

Il existe un gradient des langages de programmation le long d'un **axe
de compromis** rapidité _vs_ facilité d'utilisation :

- depuis les langages de **bas niveau** qui permettent des programmes
  très rapides car la traduction en langage machine est facile ; mais
  qui sont complexes à utiliser (car très éloignés du langage
  naturel), on dit que ce sont des langages « proches de la machine ».
- Jusqu'aux langages de **haut niveau** : ils sont plus faciles à
  utiliser par les humains car plus proches du langage naturel.

Un même problème peut être résolu par de nombreux langage. Le site [Rosettacode](http://www.rosettacode.org/) (en référence à la [pierre de rosette](https://fr.wikipedia.org/wiki/Pierre_de_Rosette)) propose de très nombreux exemples. Par exemple, le [jeu de Nim](https://fr.wikipedia.org/wiki/Jeux_de_Nim) consiste à faire jouer deux joueurs qui enlèvent alternativement 1 à 3 jetons d'un tas initial de 12 jetons. Le joueur qui prend le dernier jeton à perdu. Voici le code pour 4 langages qui permettent de coder ce jeux ([Rosetta code](http://www.rosettacode.org/wiki/Nim_game) propose 42 langage...).

```python
print("Py Nim\n")

def getTokens(curTokens):
 global tokens

 print("How many tokens would you like to take? ", end='')
 take = int(input())

 if (take < 1 or take > 3):
  print("Number must be between 1 and 3.\n")
  getTokens(curTokens)
  return

 tokens = curTokens - take
 print(f'You take {take} tokens.')
 print(f'{tokens} tokens remaining.\n')

def compTurn(curTokens):
 global tokens

 take = curTokens % 4
 tokens = curTokens - take
 print (f'Computer takes {take} tokens.')
 print (f'{tokens} tokens remaining.\n')


tokens = 12
while (tokens > 0):
 getTokens(tokens)
 compTurn(tokens)

print("Computer wins!")
```

```js
class Nim {
  constructor(tokens, printFun) {
    this.startTokens = tokens;
    this.tokens = tokens;
    this.printFun = printFun;
  }

  playerTurn(take) {
    take = Math.round(take);

    if (take < 1 || take > 3) {
      this.printFun("take must be between 1 and 3.\n");
      return false;
    }
    this.tokens -= take;
    this.printFun("Player takes " + take + " tokens.");
    this.printRemaining();

    if (this.tokens === 0) {
      this.printFun("Player wins!\n");
    }
    return true;
  }

  computerTurn() {
    let take = this.tokens % 4;
    this.tokens -= take;
    this.printFun("Computer takes " + take + " tokens.");
    this.printRemaining();

    if (this.tokens === 0) {
      this.printFun("Computer wins.\n");
    }
  }

  printRemaining() {
    this.printFun(this.tokens + " tokens remaining.\n");
  }
}

let game = new Nim(12, console.log);
while (true) {
  if (
    game.playerTurn(parseInt(prompt("How many tokens would you like to take?")))
  ) {
    game.computerTurn();
  }
  if (game.tokens == 0) {
    break;
  }
}
```

```c
#include  <stdio.h>

int playerTurn(int numTokens, int take);
int computerTurn(int numTokens);

int main(void)
{
 printf("Nim Game\n\n");

 int Tokens = 12;

 while(Tokens > 0)
 {
  printf("How many tokens would you like to take?: ");

  int uin;
  scanf("%i", &uin);

  int nextTokens = playerTurn(Tokens, uin);

  if (nextTokens == Tokens)
  {
   continue;
  }

  Tokens = nextTokens;

  Tokens = computerTurn(Tokens);
 }
 printf("Computer wins.");

 return 0;
}

int playerTurn(int numTokens, int take)
{
 if (take < 1 || take > 3)
 {
  printf("\nTake must be between 1 and 3.\n\n");
  return numTokens;
 }
 int remainingTokens = numTokens - take;

 printf("\nPlayer takes %i tokens.\n", take);
 printf("%i tokens remaining.\n\n", remainingTokens);

 return remainingTokens;
}

int computerTurn(int numTokens)
{
 int take = numTokens % 4;
 int remainingTokens = numTokens - take;

 printf("Computer takes %u tokens.\n", take);
 printf("%i tokens remaining.\n\n", remainingTokens);

 return remainingTokens;
}
```

```ruby
[12, 8, 4].each do |remaining|
  puts "There are #{remaining} dots.\nHow many dots would you like to take? "
  unless (num=gets.to_i).between?(1, 3)
    puts "Please enter one of 1, 2 or 3"
    redo
  end
  puts "You took #{num} dots, leaving #{remaining-num}.\nComputer takes #{4-num}.\n\n"
end

puts "Computer took the last and wins."
```

### Compilation et interprétation

Le programme tel que nous l'écrivons est appelé programme source (ou
**_code source_**). Comme déjà signalé plus haut, il existe deux
techniques principales pour effectuer la traduction d'un programme
source en langage machine : l'interprétation et la compilation.

#### L'interprétation

Le logiciel interpréteur est utilisé à chaque fois que l'on veut faire
fonctionner le programme. Chaque ligne du programme source analysé est
traduite au fur et à mesure en quelques instructions du langage machine,
qui sont ensuite directement exécutées. Les implémentations des langages
Python, Javascript utilisent quasiment uniquement cette technique. On
parle alors de **langages interprétés** (mais c'est un raccourcis, on
pourrais créer une implémentation de python compilée). L'interprétation
permet de tester les modifications apportées à un programme très
rapidement et sans créer un objet intermédiaire qui peut prendre de la
place de stockage. En revanche, la compilation permet des optimisations
très importantes qui rendent les programmes beaucoup plus efficaces en
termes d'exécution.

#### La compilation

La compilation consiste à traduire la totalité du code source en une
seule fois. Le logiciel compilateur lit toutes les lignes du programme
source et produit une nouvelle suite de codes, écrits en langage
machine, que l'on appelle programme objet (ou code objet). Celui-ci
peut désormais être exécuté indépendamment du compilateur et être
conservé tel quel dans un fichier appelé fichier exécutable. Le _C++_,
par exemple, est un langage compilé.

#### Choix du langage python

Il existe de nombreux langages **libres**, **gratuits, performants,
bien documentés,** et **portables** (c'est-à-dire qui fonctionnent sur
différents systèmes d'exploitation tels que **Windows**, **Unix**...). Le
langage bas-niveau dominant est sans conteste le **C/C++** et ses
variantes ainsi que le java. Vous pouvez aller vous en rendre compte en
regardant l'indice de popularité [TIOBE](https://www.tiobe.com/tiobe-index/) qui recense un grand nombre
de langage. Mais, le choix du langage est surtout fonction de votre
domaine d'application (jeux, application mobile, analyses de données).

**Python** quand à lui est un langage haut-niveau dont la syntaxe est
assez lisible et qui est très populaire (cf le classement
[TIOBE](https://www.tiobe.com/tiobe-index/)). Ce langage permet de très
nombreuses applications (depuis l'intelligence artificielle jusqu'à la
création de site web) grâce à une grande communauté et de très nombreux
modules.

> :fa fa-microscope: Le mouvement du **logiciel libre** (_Free Software_) fait campagne pour la liberté des utilisateurs de l'informatique ;
> c'est un mouvement qui lutte pour la liberté et la justice. Quand on dit qu'un logiciel est « libre » [free\], on entend
> par là qu'il respecte [**les libertés essentielles de l'utilisateur**](https://www.gnu.org/philosophy/free-sw.html) :
> la liberté de l'utiliser, de l'étudier, de le modifier et d'en
> redistribuer des copies, modifiées ou non. C'est une question de
> liberté, pas de prix -- pensez à « liberté d'expression » et pas à
> « entrée libre » (think of "free speech", not "free beer"). Il est souvent le produit de la collaboration bénévole de plusieurs développeurs dispersés dans le monde entier. <br>
> Des exemples de logiciels libres : le système d'exploitation **GNU/Linux**, la suite **Open Office**.
> Un logiciel non libre est dit **propriétaire** (par ex. le système d'exploitation **Windows**, la suite **Microsoft Office**). Le
> mouvement de l'**open source** (code source accessible à tous), met surtout l'accent sur les avantages pratiques et ne fait pas campagne pour des principes. Pour en savoir plus, aller visiter le site du [GNU](https://www.gnu.org/philosophy/free-sw.html) dont la traduction française est très bien faîte.

## :fa fa-brain: Exercices

Attention pour faire ses exercices il faut certaines connaissances en python (voir le chapitre [suivant](premiere/python.md)).

### Introduction

1. On dispose de la formule $C=0.55556\times(F-32)$ pour convertir les degrés
   Fahrenheit en degrés Celsius :
   où $F$ est une température en degrés Fahrenheit et $C$ la
   température correspondante en degrés Celsius.
   - Écrire un programme qui convertit en degrés Celsius une température rentrée au clavier en degrés Fahrenheit.
   - Même question pour la conversion inverse.
2. Écrire un programme qui permute et affiche les valeurs de trois
   variables $a$, $b$, $c$ qui sont entrées au clavier : $a \Rightarrow b$ ,
   $b \Rightarrow c$ , $c \Rightarrow a$.

### Boucles et conditions

3. Écrire un programme qui lit une valeur et affiche sa table de
    multiplication (on se limitera aux 12 premiers termes). Faire une
    variante du programme précédent qui affiche la table de
    multiplication de tous les chiffres compris entre 2 et 9 (inclus).
    Pensez à laisser un espace entre deux tables de multiplication (print() imprime une ligne vide).
4. :fa fa-award: Écrire un programme qui affiche un triangle rempli d'étoiles (\*)
    sur un nombre de lignes donné passé en paramètre, exemple :
    - 1ère version : à l'aide de deux boucles for, en imprimant les \*
      une par une.
    - 2ème version : avec une seul boucle for, et une chaîne de
      caractères où vous accumulerez des étoiles (pour ceux qui vont un
      peu plus vite, print(« machin » end= '') évite de passer à la ligne.
5. Écrire un programme qui teste si un nombre _a_ est divisible par un
    nombre _b_, les deux étant rentrés au clavier. Le programme
    retournera un message signalant la divisibilité ou non, et
    éventuellement le reste dans le cas où _a_ n'est pas divisible par
    _b_.
6. :fa fa-award: Programmation d'un petit jeu de devinette. L'ordinateur choisit au
    hasard un nombre compris entre 1 et 100. Le but du jeu est de le
    deviner en un nombre d'essai minimal. À chaque tentative,
    l'ordinateur, indique « gagné », « trop petit » ou « trop grand ».
    L'utilisateur dispose d'un nombre d'essais limités.
    Écrire l'algorithme en « langage naturel ». Programmer le jeu, et le tester.
    On utilisera la bibliothèque _random._ Pour cela, on écrit « import random » en début de programme.
    *nombre* = random.randint(a, b) renverra un nombre aléatoire tel que $a \le Nombre \le b$.
    Pour plus d'informations sur le bibliothèque random et de possibilités voir la [**documentation**](https://docs.python.org/3.5/library/random.html).
7. Écrire une fonction qui retourne la factorielle d'un nombre (par exemple $6!=6 \times 5 \times 4 \times 3 \times 2 \times 1$).
8. :fa fa-award: Un nombre entier est dit parfait s'il est égal à la somme de ses diviseurs (sauf lui-même). Ainsi $6 = 1 + 2 + 3$ est parfait.
    - Écrire une fonction somme_div qui retourne la somme des diviseurs d'un nombre passé en paramètre.
    - Écrire une fonction parfait qui teste si un nombre passé en paramètre est parfait et qui retourne 1 s'il l'est et 0 sinon. Écrire un programme principal qui affiche tous les nombres parfaits inférieurs à une certaine limite.
9. :fa fa-award: Deux nombres M et N sont appelés nombres_amis si la somme des diviseurs propres (sauf M) de M est égale à N et la somme des diviseurs propres de N est égale à M.
    - Écrire une fonction amis qui retourne le nombre_amis (s'il existe) d'un nombre passé en paramètre , cette fonction utilise la fonction
      somme_div de l'exercice 8. - Écrire un programme principal qui affiche tous les nombres_amis inférieurs à une certaine limite.
