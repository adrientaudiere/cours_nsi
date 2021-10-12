# Programmation <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

!> !! Work in progress !!

## Récursivité

Résoudre un problème de façon récursive c'est **décomposer un problème en sous-problèmes identiques** de plus en plus petits jusqu’à obtenir un problème suffisamment petit pour qu’il puisse être résolu de manière triviale.

?> Regarder la [vidéo](https://www.youtube.com/watch?v=U3nGNJTxYc4&feature=emb_imp_woyt) sur la tour de Hanoï vue comme un processus récursif. 


<div class="nutshell">

Les trois règles d'un **algorithme récursif** : 
- Il s’**appelle lui même**;
- Il doit avoir un **état trivial**, ce qui permet de définir une condition d’arrêt;
- Il doit conduire vers cet **état d’arrêt**, pour éviter les boucles infinis.

</div>

### Fonction récursive

Une fonction **récursive** est donc une fonction qui va **s’appeller elle-même**. Comme dans le cas des boucle "while", il est crucial de penser à la condition d'arrêt de la fonction au risque de tomber dans une boucle infini. L'utilisation des fonctions récursives est souvent liée à la notion de récurrence en mathématiques.


?> Éxaminer le programme ci-dessous et tenter de prévoir son résultat avant de l'exécuté sous [pythontutor](https://pythontutor.com/) pour vérifier votre prévision et comprendre la suite du processus de pile/dépiler.

```python
def fonct(n):
    if n>0:
        fonct(n-1)
    print(n)

fonct(5)
```

<details>
<summary> <strong> Réponse </strong></summary>
 
- On appelle la fonction *fonct* avec le paramètre n = 3 ; n est supérieur à 0 donc appel de la fonction *fonct* avec le paramètre n = 2

- 2e appel de la fonction *fonct* avec le paramètre n = 2 ; n est toujours supérieur à 0 donc appel de la fonction *fonct* avec le paramètre n = 1

- 3e appel de la fonction *fonct* avec le paramètre n = 1 ; n > 0 donc appel de la fonction *fonct* avec le paramètre n = 0

- 4e appel de la fonction *fonct* avec le paramètre n = 0 ; n = 0 donc on exécute l'instruction *print(n)* => affichage : 0

- on "dépile" (3e appel, n = 1) : on exécute l'instruction print(n) => affichage : 1

- on "dépile" (2e appel, n = 2) : on exécute l'instruction print(n) => affichage : 2

- on "dépile" (1er appel, n = 3) : on exécute l'instruction print(n) => affichage : 3

Il ne faut jamais perdre de vu qu'à chaque nouvel appel de la fonction fonct le paramètre n est différent. 
Voici un schéma expliquant le processus en termes de pile d'exécution :

![](../_img/answer_recursivite.png ":size=90%")

<p class="center-p"> <strong> Schéma d'explication de la pile d'exécution (David Roche - CC-BY-CA) </strong>
</p>

</details>


?> Expliquez pour chaque script ci-dessous (f, g, h, p) pourquoi on obtient une erreur. 

```python
def f(n):
    return n * f(n-1)

print(f(3))
```


```python
def h(n):
    if(n==0):
        return 1
    return n * h(n)-1

print(h(3))
```

```python
def g(n):
    if(n==0):
        return 1
    return n * g(n+1)

print(g(3))
```

```python
def p(n):
    if(n==0):
        return 1
    return n * p(n-2)

print(p(3))
```

?> À l'aide de la fonction *fonct* vu précédement, écrire une fonction *fact(x)* qui calcule la factorielle d'un nombre x. 


?> La figure ci-dessous vous présente une fonction qui calcule la somme des valeurs d'une variable de trois façons différentes. Expliquez chacune de ses fonctions puis tester à l'aide de site [pythontutor](https://pythontutor.com/).

![](../_img/fig_recursivite.png ":size=60%")

<p class="center-p"> <strong> Comparaison des boucles while et For avec une implémentation récursive. </strong>
</p>


<details class="advanced_level">
<summary> <strong> Niveau avancé :</strong></summary>

?> À l'aide du script ci-dessous calculer puis comparer les vitesses de calcul.

```python
from timeit import default_timer as timer 
from random import randint
# les deux fonctions ici
L=[randint(0,100) for i in range(1000)]

debut=timer()
print(sommeliste(L))
fin=timer()
print(fin-debut)

debut=timer()
print(somme(L))
fin=timer()
print(fin-debut)
```
</details>

<details class="advanced_level">
<summary> <strong> Niveau avancé :</strong></summary>

?> Regarder la [vidéo](https://www.youtube.com/watch?v=PW_Pka9iBko) sur le flocon de Koch. Lancer ensuite le programme ci-dessous ()

```python

import turtle as t

def koch(longueur, n):
    if n == 0:
        t.forward(longueur)
    else:
        koch(longueur/3, n-1)
        t.left(60)
        koch(longueur/3, n-1)
        t.right(120)
        koch(longueur/3, n-1)
        t.left(60)
        koch(longueur/3, n-1)

def flocon(taille, etape):
    koch(taille, etape)
    t.right(120)
    koch(taille, etape)
    t.right(120)
    koch(taille, etape)

flocon(100, 3)
```


</details>


![](../_img/image_recu_lesmignons.jpg ":size=60%")

<p class="center-p"> <strong> Mème (Van Zuijlen Stéphan - CC-BY-NC). </strong>
</p>

### Exercices récursivité

1. La fonction ci-dessous permet de tester si un mot est un palindrome (mot qui se lit dans les deux sens, [:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Palindrome). Que renvoient *est_palindrome("selles")* ; *est_palindrome("radar")* ; *est_palindrome("selle")*?

```python
def est_palindrome(mot):
    mot=mot.lower()
    for i in range(len(mot)//2): 
        if mot[i]!=mot[-i-1]:
            return False
    return True
```

2. Écrire une version récursive *rec_est_palindrome*. Pour cela identifier l'état trivial (donc la condition d'arrêt) et utiliser l'idée que "selles" est un palindrome si "s"= "s" et "elle" est un palindrome.

3. Modifier votre programme pour qu’il considère que la phrase "Karine alla en Irak" soit un palindrome.


<details class="advanced_level">
<summary> <strong> Niveau avancé :</strong></summary>

?> Faire le [TP](https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/res/res_tp_tour_de_hanoi.pdf) sur la tour de Hanoï du site isn-icn-ljm.

</details>

## Modularité

!> Work in progress

## Programmation objet

Jusqu'à maintenant, nous avons principalement utilisé le paradigme de programmation impérative qui repose sur les notions de : 
- **séquence d'instructions** (les instructions d'un programme s'exécutent dans l'ordre dans lequel on les écrit)
- **affectation** (on attribue une valeur à une variable, par exemple : texte = "Youpi")
- les instructions conditionnelles (if / else) et les boucles (while et for)

Il existe d'autre manière de programmer, le paradigme de la programmation objet en est un. Dans ce paradigme ... 

!> Work in progress

?> Créer une classe chien qui à les attributs _nom_, _points_de_santé_ et _aboiement_ (chaîne de caractères). Vous devez également définir les méthodes _mordre(autre_chien)_(fait baisser les points de santé d’un autre chien),_manger_(augmente les points de santé),_grogner_(renvoie « Grrr... » + son aboiement),_machouiller(chaîne)_(renvoie la chaîne de caractères mélangée) ainsi qu'une méthode_\_\_repr\_\__.

?> Créer un combat automatique entre deux chiens: les valeurs de dégâts et de pv gagner quand il mange sont tirées au hasard, chaque chien grogne avant d'attaquer, les chiens attaquent puis mangent chacun leur tour, le combat s'arrête quand les pv d'un chien tombe à 0 et le gagnant mâchouille.

## Mise au point de programme

!> Work in progress

## Programmation fonctionnelle

!> Work in progress
