#  Algorithmique <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

!> !! Work in progress !!

!> Réviser le [programme de première](../premiere/types_construits.md) sur les types construits.

## Liste 

!> Attention, les listes Python sont en fait des tableaux dynamiques. On parle ici du type abstrait de liste.

https://pixees.fr/informatiquelycee/term/c5c.html
    Une liste est une structure de données permettant de regrouper des données. Une liste L est composée de 2 parties : sa tête (souvent notée car), qui correspond au dernier élément ajouté à la liste, et sa queue (souvent notée cdr) qui correspond au reste de la liste. Voici les opérations qui peuvent être effectuées sur une liste :

    obtenir une liste vide (vide)
    tester si une liste est vide (estVide)
    obtenir le dernier élément ajouté à la liste (car)
    obtenir une liste contenant tous les éléments d'une liste à l'exception du dernier élément ajouté (cdr)
    construire une liste à partir d'un élément et d'un autre liste (cons)



## Listes chaînées

!> Work in progress

https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/res/res_listes.pdf

https://isn-icn-ljm.pagesperso-orange.fr/basthon-notebook/?from=https://isn-icn-ljm.pagesperso-orange.fr/notebook/listes_cha%C3%AEn%C3%A9e_TD.ipynb



https://pixees.fr/informatiquelycee/term/c5c.html

    Les listes, les piles ou les files sont des "vues de l'esprit" présentes uniquement dans la tête des informaticiens, on dit que ce sont des types abstraits de données (ou plus simplement des types abstraits). L'implémentation de ces types abstraits, afin qu'ils soient utilisables par une machine, est loin d'être une chose triviale. L'implémentation d'un type de données dépend du langage de programmation. Il faut, quel que soit le langage utilisé, que le programmeur retrouve les fonctions qui ont été définies pour le type abstrait (pour les listes, les piles et les files cela correspond aux fonctions définies ci-dessus).

    Pour implémenter les listes (ou les piles et les files), beaucoup de langages de programmation utilisent 2 structures : les tableaux et les listes chaînées.



## Piles et files

Il existe deux structures de données très utilisées en informatiques : les files (aussi appelé FIFO pour *First In First Out*) et les piles (aussi appelé LIFO pour *Last In First Out*). Ces structures sont des types particuliers de liste.


![](../_img/fifo_lifo.png ":size=60%")

<p class="center-p"> Comparaison des structures **File** et **Pile**.</p>

---


https://docs.python.org/fr/3/tutorial/datastructures.html#using-lists-as-stacks


### Piles

Une pile (LIFO pour *Last In First Out*) est une façon de structurer des données qui est très utilisée en informatique. Par exemple, des cartons de déménagement qu'on empile forme une pile. Le dernier carton arrivé (Last In) sur le tas est le premier à être enlever. 
En informatique, on utilise par exemple les piles dans les piles d'appels de fonctions ou encore pour parcourir des graphes.

On peut lister quelques opérations courantes sur les piles :

- la création d’une pile,

- l'empilement d’un élément sur une pile,

- le dépilement d’une pile,

- la consultation du sommet d’une pile.

### files

Une file (FIFO pour *First In First Out*) est une structure dans laquelle les premiers éléments arrivés sont les premiers à sortir. Une file ressemble à une file d'attente à la boulangerie, le premier arrivé devant la porte sera le premier servi. En informatique, on utilise les files,  


##  Dictionnaires

https://pixees.fr/informatiquelycee/term/c6c.html



## Structures en arbres

!> Work in progress

https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/co/section_chapitre3.html

###  Arbres binaires

###  Arbres binaires de recherche

### Autres structures arborescentes

## Graphe

!> Work in progress

https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/co/section_chapitre4.html

### Définition d'un graphe

### Parcours en profondeurs et en largeur

## Diviser pour régner

!> !! Work in progress

https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/co/section_chapitre6.html


## Programmation dynamique

!> Work in progress

https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/co/section_chapitre6.html

## Recherche textuelle

?> Faire le TD sur l'algorithme de Boyer-Moore (modifié de Stéphan Van Zuijlen (CC-BY-NC)).

## Calculabilité/décidabilité

?> Lire le [chapitre 0](https://isn-icn-ljm.pagesperso-orange.fr/NSI-TLE/co/section_chapitre0.html) de Stéphan Van Zuijlen. Expliquer en deux phrases la notion de décidabilité.
