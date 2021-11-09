# Découvrir le langage python <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

## :fa fa-terminal: Environnements de développement

Pour lancer le programme python (une fois qu'il est installé sur votre machine) il existe une façon très simple. Vous ouvrez votre terminal :fa fa-terminal: et vous écrivez `python`. Vous pouvez ensuite écrire vos commandes python et observer le retour du programme directement dans le terminal. C'est ce qu'on appelle le mode dynamique.

?> Lancer les commandes suivantes dans votre terminal. Quelle est la version de python que vous utilisez? Quels sont les résultats affichés dans le terminal?

```python
python # lancer le programme python
print('Salut' + 'à toi')
1+3
print(3*4)
quit() # quitter le programme python
```

> Remarque sur les **commentaires** dans le code. Les caractères suivants un dièse (**#**) sont des commentaires, ils n'influent en rien sur le programme mais nous permettent d'annoter le programme pour d'autres utilisateurs, ou pour nous plus tard. On peut mettre des commentaires de plusieurs lignes entre triples guillemets : """ ... """. **Il est très important de commenter son code**. La relecture du programme, la recherche de bug et sa réutilisation future nécessitent des commentaires réguliers dans le code.

Le problème du terminal, c'est que c'est long de relancer chaque script (ensemble d'instruction) et que l'historique est difficile à conserver. Pour simplifier l'utilisation des langages informatique on utilise des environnements de développement intégré (IDE pour _integrated development environment_) Sur vos machines plusieurs IDE sont déjà installés (listés du plus simple au plus complet):

- IDLE
- Tonny
- Anaconda (une suite de logiciel dont le logiciel Spyder)
- VScodium (que nous utiliserons sans doute plus tard)

?> Ouvrir le logiciel VScodium, créer un nouveau fichier, y recopier le code déjà testé ci-dessus et lancer le script à l'aide de la flèche verte.

## :fa fa-spell-check: Quelques règles de sémantique

Chaque langage a des règles obligatoires (leur manquement entraîne une erreur) et des conventions (règles de bonnes conduite). En python, les noms des **variables** suivent quelques règles :fa fa-exclamation-triangle: et conventions :fa fa-heartbeat: :

- :fa fa-exclamation-triangle: le nom d'une variable ne doit contenir que des lettres (a → z , A → Z), des chiffres et le symbole "\_" (underscore = tiret du bas) et doit commencer par une lettre
- :fa fa-exclamation-triangle: les minuscules et les majuscules sont différenciées (_ma_var_et_Ma_var_ sont deux variables différentes),
- :fa fa-exclamation-triangle: certains mots sont « réservés » par python (voir tableau ci-dessous), on ne peut donc pas les utiliser comme nom de variable,
- :fa fa-heartbeat: il est conseillé de n'écrire les variables qu'avec des minuscules sauf les nombres constants (par exemple si vous utilisez souvent $\pi$ vous pouvez définir cette constante ainsi $PI=3.14$),
- :fa fa-heartbeat: les accents et les caractères spéciaux sont fortement déconseillés (sauf dans les commentaires) car ils peuvent ne pas être pris correctement en charge par certains OS,
- :fa fa-heartbeat: plus un nom de variable sera clair, plus il sera facile de relire votre code. Par exemple, préférer _nom_de_famille_ à _ndf_; et préférer _moyenne_age_(ou_moy_age_) à _m_age_ pour nommer une variable qui représente une moyenne d'âge.

<details>
<summary> <strong>Tableau des mots réservés en python</strong>. <a href="https://fr.wikibooks.org/wiki/Programmation_Python/Tableau_des_mots_r%C3%A9serv%C3%A9s" target="_blank" rel="noopener">Source</a> </summary>

---

<p class="center-p"> <strong>Tableau des mots réservés en python</strong> qui ne peuvent pas être utilisé comme nom de variable. Les mots en gras sont des mots que nous utiliserons durant les cours de NSI. <a href="https://fr.wikibooks.org/wiki/Programmation_Python/Tableau_des_mots_r%C3%A9serv%C3%A9s" target="_blank" rel="noopener">Source</a> </p>

| Mot        | Définition                                                               |
| ---------- | ------------------------------------------------------------------------ |
| **and**    | Opérateur ET booléen logique                                             |
| as         |                                                                          |
| **assert** |                                                                          |
| break      | Sortie de boucle                                                         |
| **class**  | Définition de classe d'objet ( Programmation Orientée Objet)             |
| continue   |                                                                          |
| **def**    | Définition de fonction                                                   |
| del        | Suppression de                                                           |
| **elif**   | Condition contraire                                                      |
| **else**   | Contraire                                                                |
| except     | Sauf (à utiliser après "try")                                            |
| exec       |                                                                          |
| finally    |                                                                          |
| **for**    | Boucle                                                                   |
| **from**   | De                                                                       |
| global     | Définition (ou utilisation) dans une fonction d'une variable globale     |
| **if**     | Condition                                                                |
| **import** | Importation de module                                                    |
| **in**     | Contient                                                                 |
| **is**     | Est                                                                      |
| **is not** | N'est pas                                                                |
| lambda     | Définition d'une fonction Lambda                                         |
| **not**    | Négation logique                                                         |
| **or**     | Opérateur de choix OU booléen logique                                    |
| pass       |                                                                          |
| **print**  | Afficher                                                                 |
| raise      |                                                                          |
| **return** | Stopper la fonction courante (renvoyer sa valeur)                        |
| **sort**   | Classer par ordre alphabétique                                           |
| try        | Essayer (généralement suivi de "except" : sauf)                          |
| **while**  | Boucle                                                                   |
| yield      | S'emploie uniquement dans une fonction, et renvoie son résultat régénéré |

</details>

## :fab fa-python: Bases de python

### Symboles arithmétiques

En plus des signes d'arithmétiques **+**, **-**, **\*** et **/**, on peut utiliser les symboles suivants : **//**, **%**, **\*\***.

?> Utiliser les symboles //, % et \*\* dans des opérations avec des nombres simples. Essayer d'en déduire l'usage de ces trois symboles.

- De plus, les variables ne peuvent pas être un des « mots
  réservés » suivant utilisés par le langage lui-même :

### Typage

Chaque variable a un type. Sous python, pour connaître le type d'une variable _var_ il suffit d'écrire _type(var)_. Les types les plus simples sont les types :

- **int** (_integer_) pour les variables constituées de nombres entiers,
- **float** pour les variables constituées de nombres décimal (à virgule),
- **str** pour les variables constituées de chaîne de caractères (par ex. "Ba oui, c'est Scho!"),
- **bool** pour les variables constituées de booléens (True/False)

?> Remplacer les trois petits points du code ci-dessous pour obtenir un type _int_. Modifier ensuite votre variable pour obtenir chacun des trois autres types simples vu ci-dessus.

```python
var = ...
type(var)
```

On peut forcer une variable d'un type à devenir une variable d'un autre
type ; attention cela peut causer des erreurs ! Pour changer le type
d'une variable, on utilise le type que l'on veut affecter :

```python
a = 23.1
type(a)
# <type 'float'>

a = str(a)
a
# '23.1'

b = 23.1
b = int(b)
b
# 23

c = "bonjour"
int(c)
# Traceback (most recent call last):
#   File "<ipython-input-20-089eb950f64f>", line 1, in <module>
#       int(c)
#   ValueError: invalid literal for int() with base 10: 'bonjour'
```

?> Lancer le script ci-dessous et expliquer les résultats ou les erreurs

```python
a = "Je suis né en " + "1989"
b = "Je suis né en " + 1989
c = "Je suis né en " * "1989"
d = "Je suis né en " * 1989
```

#### Zoom sur les booléens (bool)

Pour rappel, une variable booléennes est une variable qui n'autorise que deux valeurs : True et False.
On utilise souvent ces variables dans des tests. On peut combiner ces variables à l'aide des connecteurs
logiques **and**, **or** et **not**.

```python
# Tests logiques
x == y # x est égal à y
x != y # x est différent de y
x > y  # x est plus grand que y
x < y  # x est plus petit que y
x >= y # x est plus grand que, ou égal à y
x <= y # x est plus petit que, ou égal à y
```

```python
# Connecteurs logiques
a and b # « et » mathématique
a or b  # « ou » mathématique
not(a)  # « non » mathématique
```

?> Tester le code ci-dessous. À votre avis, comment python compare deux chaînes de caractère?

```python
a = "Arrivé"
b = "Sortir"

a == b
a != b
a > b
a < b
```

#### Zoom sur les chaînes de caractères (str)

Les **chaînes de caractères** sont un type particulier de **liste**. Les listes sont des **types complexes** que nous verrons plus tard. On peut effectuer des **opérations** sur ces chaînes, en particulier la **concatenation** (« addition » de texte ensemble) et la répétition (« multiplication » d'une chaîne de caractères). Pour sélectionner la Xème lettre d'une chaîne, on peut utiliser l'écriture chaîne[x-1].
On peut également connaître la longueur d'une chaîne (le nombre de caractère) avec la fonction `len`.

```python
a = "J'aime "
b = "beaucoup "
c = "manger "
d = "à Scholae."
print(a+c+d)
print(a+3*b+c+d)
print(a[1])
print("Cette phrase comporte " + str(len(a+b+c+d)) + " caractères")
```

?> Essayer de relancer la dernière ligne de code ci-dessus en enlevant la fonction `str`. Que se passe t'il?

?> Que renvoie `print(a[0])`, `print(a[1:5])` et `print(a[len(a)])`? Expliquer pourquoi.

### Instructions conditionnelles

Le « si _condition_ alors _instruction_ (sinon _instruction_) » s'écrit en python en utilisant l'indentation (4 espaces). C'est l'un des rares langages à utiliser l'indentation comme structure de code (de nombreux langage utilise les {} pour encadrer les conditions). Les conditions sont des booléens (par exemple le résultat d'un test d'égalité).

```python
if condition :
    ... # instruction 1
else:
    ... # instruction 2
suite_du_programme
```

On peut emboîter des conditions dans des conditions, il faut alors bien faire attention aux indentations.

```python
if condition_1 :
    if condition_2 :
        ... # instruction 1
    else :
        ... # instruction 2
else:
    ... # instruction 3
```

Lorsque l'on a plusieurs alternative possible on utilise le mot clé `elif` (abréviation de _else if_).

```python
if condition_1 :
    ... # instruction 1
elif condition_2 :
    ... # instruction 2
elif condition_3 :
    ... # instruction 3
else:
    ... # instruction 4
```

### Boucle while (tant que)

La boucle while est une structure qui répète une instruction jusqu'à ce qu'une condition (de type _bool_) soit remplie. L'indentation est encore primordiale. Attention, il faut bien vérifier que la condition va être atteinte, sinon la boucle while ne s'arrêtera jamais.

```python
a=0
while a<10:
    print(a)
    a = a+1
```

### Boucle for (pour)

La boucle for s'écrit selon la séquence **for** var **in** sequences_de_valeur :

```python
for i in range(0,10):
    print(i)
```

?> Lancer la commande ci-dessus. Expliquer ce que vous voyez puis modifier le code pour afficher uniquement les nombres paires de 2 à 20. Il faut utiliser la fonction _if_.

?> Faire les exercices de la fin de la partie [programmation](/docs/premiere/programmation.md).

### Utilisation de bibliothèques (ou modules)

Dans tout les langages informatiques avec une communauté conséquente, il existe vite un problème à résoudre : comment ne pas recoder (mal) ce qui a déjà été (bien) codé tout en gardant une langage qui ne deviennent pas trop imposant à installer? Autrement dit comment ne pas réinventer la roue tout en permettant aux codeurs qui n'ont pas besoins de roues de ne pas avoir à télécharger cette roue avec le langage. Une solution très utilisée est l'utilisation de **bibliothèques** (aussi appelées modules ou packages). Ces bibliothèques sont des ensembles de fonctions cohérentes.

Par exemple, la bibliothèque « math » permet de calculer, entre autres, des cosinus et des racines carrées. La bibliothèque « random » est utilisé pour générer des nombres aléatoires. Pour charger une bibliothèque on utilise la code **from** _nom_bibliotheque_ **import** \*. Ici l'étoile indique que l'on veut charger toute la bibliothèque. Si on a seulement besoins d'une ou quelques fonction(s) on remplace l'étoile par le nom des fonctions souhaitées.

```python
from math import * # importation de toute les fonctions de la bibliothèque math
from random import uniform # importation de la fonction uniform de la bibliothèque random
```

### Fonctions et spécification

Python est un langage qui permet facilement de créer et d'utiliser des fonctions. Une fonction est une **suite d'instruction** qui prend des **paramètres en entrée**, **mouline** puis renvoie des **paramètres de sortie** (ou modifie une variable). Le nombre de paramètres d'entrée et de sortie peut être nul. Le choix d'un bon nom de fonction et de bon nom de paramètre est centrale dans la qualité d'un code.

> Il existe une citation célèbre en informatique, attribué à Phil Karlton : "There are only two hard things in Computer Science: cache invalidation and naming things" qui peut se traduire par « Il n'y a que deux choses difficiles en les sciences informatiques, l'invalidation de cache ([:fab fa-wikipedia-w:](https://en.wikipedia.org/wiki/Cache_invalidation)) et nommer les choses ». Cette citation est célèbre car elle souligne le caractère cruciale et difficile de l'attribution de nom aux fonctions et aux variables en informatiques.

```python
def bonjour():
    '''
    Cette fonction sans paramètre d'entrée dit bonjour!
    '''
    return("Bonjour")

a = bonjour()
print(a)
```

Les paramètres d'entrées sont indiqués dans les parenthèses de la fonction. Les paramètres de sortie sont renvoyés grâce à la commande `return`.

```python
def bonjour_personnalise(nom, prenom):
    '''
    Cette fonction dit bonjour de façon personnalisé

    Parameters:
        nom (str): nom de famille
        prenom (str): prénom

    Returns:
        Une chaîne de caractère disant bonjour à la personne dont le nom
        de famille et le prénom ont été donnés en entrée.

    Raises:
        TypeError: if nom or prenom is not a string
    '''
    return("Bonjour "+ prenom + " " + nom)

b = bonjour_personnalise("Sy", "Omar")
print(b)
help(bonjour_personnalise)
```

?> Que renvoie `print(b)` si vous changer l'ordre des valeurs "Sy" et "Omar"? Et si vous écrivez b = bonjour_personnalise(prenom="Omar", nom="Sy")

L'ordre des paramètres d'entrée est important. Si vous ne connaissez pas l'ordre il y a deux solutions. Soit il faut faire une recherche (commande `help` ou recherche sur le Web), soit il faut nommer les valeurs des paramètres sous la forme ma_fonction(param1="valeur_param1", param2="valeur_param2"). La partie entre ''' est ce qu'on appelle la **docstring** (documentation de code). On parle aussi de **spécification** de la fonction. Cette docstring est indispensable à une fonction. Elle est ce qui va apparaître aux utilisateurs qui utiliserons la commande `help(votre_fonction)`. Cela ne vous empêche pas de commenter certaines lignes de codes importantes et/ou cruciales pour comprendre votre fonction. En python, il n'y a pas de convention dominante pour structurer le docstring, mais pour une bonne spécification il faut que votre docstring:

- Définisse l'**objectif** de la fonction,
- Liste les **paramètres d'entrée et de sortie** de la fonction (en particulier leur format et leur type),
- Précise les conditions pour que votre fonction fonctionne:
  - **Précondition**: condition sur les paramètres d'entrée (par ex. mon paramètre doit être une variable de type \_int\ et doit être positif),
  - **Postcondition**: condition sur les paramètres de sortie (par ex. la postcondition d'une fonction qui fait la somme de deux nombres positifs est que cette somme doit être positive). Il s'agit souvent de conditions que l'on testera grâce à des tests unitaires par exemple avec le framework unittest de python (pas au programme).

Lorsqu'une variable est créées à l'intérieur d'une fonction, elle n'existe pas en dehors de cette fonction. On dit que la variable est **locale**.

?> :fa fa-award: Écrire un script qui met en évidence le caractère locale d'une variable définie dans une fonction.

##  :fa fa-keyboard: Comprendre python avec des tortues

?> Réaliser ces [exercices](https://hourofpython.trinket.io/a-visual-introduction-to-python#/welcome/an-hour-of-code) en ligne.
