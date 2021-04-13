# ALGORITHMIQUE <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

!> !! Work in progress !!


## Définissons un algorithme

D'un point de vue mathématique, un algorithme est une « **suite finie et non ambigüe d’opérations ou d’instructions permettant de résoudre une problème ou d’obtenir un résultat** » (Source : [wiktionary](https://fr.wiktionary.org/wiki/algorithme)). Le mot *algorithme* est une référence au mathématicien perse  **Al-Khwârizmî** (en arabe : الخوارزمي) qui a classifié les algorithmes existants à son époque ($\thicksim780 \thickspace \text{\textendash} \thickspace 850$) en fonction de leurs critères de terminaison (nous en parlerons plus tard).

D'un point de vue des sciences informatiques, un algorithme est une **procédure de calcul définie par une suite finie d’opérations élémentaires obéissant à un enchaînement déterminé**. Il s'agit de résoudre un problème en un certain nombre d'étapes clairement définies dans un dialogue avec un ou des ordinateurs. La grande majorité des algorithmes prennent des **valeurs en entrée** et à la **suite des opérations** des l'algorithme renvoient des **valeurs de sortie**.

```mermaid
graph LR
    A([Données d'entrée]) --> B{Opération}
    subgraph Algorithme 
        B --> C{...}
        C --> D{...}
        C --> E{...}
    end
    E --> F([Données de sortie])
    D --> F
    classDef default fill:#2e789163,stroke:#2e7891,stroke-width:4px;
```

--- 
<p class="center-p"> Schema simplifié d'un algorithme.</p>

<details class="advanced_level">
<summary> <strong> Niveau avancé :</strong></summary>

Un algorithme dois respecter cinq propriétés selon D. Knuth (<abbr title="Donald E. Knuth, Algorithmes, Stanford, CSLI Publications, 2011, 510 p. (ISBN 978-1-57586-620-8)"> 2011 </abbr>) : 
- **Finitude** : « Un algorithme doit toujours se terminer après un nombre fini d’étapes. »
- **Définition précise** : « Chaque étape d'un algorithme doit être définie précisément, les actions à transposer doivent être spécifiées rigoureusement et sans ambiguïté pour chaque cas. »
- **Entrées** : « quantités qui lui sont données avant qu'un algorithme ne commence. Ces entrées sont prises dans un ensemble d'objets spécifié ».
- **Sorties** : « quantités ayant une relation spécifiée avec les entrées ».
- **Rendement** : « toutes les opérations que l'algorithme doit accomplir doivent être suffisamment basiques pour pouvoir être en principe réalisées dans une durée finie par un homme utilisant un papier et un crayon ».
</details>


> Une recette de cuisine peut être réduite à un algorithme. En **entrée** on injecte des ingrédients et on spécifie le matériel utilisé. Ces entrées sont ensuite utilisés par des **instructions élémentaires simples** (couper, frire, mélanger...) pour donner en **sortie** un plat préparé. 

### L'algorithme d'Euclide

L'algorithme antique le plus connu est l'algorithme d'Euclide qui permet de calculer le plus grand commun diviseur (PGCD) de deux nombres entiers, c'est à dire de trouver le plus grand entier qui divise les deux entiers en laissant un reste nul. Cet algorithme simple est décrit ci-dessous grâce à un organigramme, un peuso-code (code en langage naturel) puis sous une version python. 

```mermaid
graph LR
    A[(Soit a et b <br> deux entiers <br> naturels)] --> B{b=0?}
    B ---->|Oui| C([PGCD=a])
    B -->|Non| D[Calculer r le reste <br> de la division <br> euclidienne de a par b]
    D --> E[a reçoit la <br> valeur de b]
    E --> F[b reçoit la <br> valeur de r]
    F --> B
    classDef default fill:#2e789163,stroke:#2e7891,stroke-width:2px;
```
Il s'agit d'un algorithme assez simple mais qui a quand même une caractéristique assez complexe, c'est la boucle dans l'algorithme. En fait, l'algorithme recommencera au début (mais avec de nouvelles valeurs) jusqu'à remplir la condition (b=0). On appelle une fonction qui s'appelle elle même une fonction récursive. C'est au programme de NSI mais en Terminale seulement. Pour comprendre les codes ci-dessous, il faut savoir que a%b (on le lit « a modulo b ») renvoie le reste de la division euclidienne de a par b. Par exemple 15%4=3, 240%13=6 ou encore 17%12=5. Il s'agit bien de la façon de calculer notre petit r.

```pseudo-code
fonction euclide(a, b)
    '''
    Calcul le le plus grand commun diviseur (PGCD) de deux nombres entiers
    paramètres:
        a et b sont deux entiers naturels non nuls
    résultat:
         retourne le PGCD de a et b
    '''
    si b = 0 alors
        retourner a
    sinon
        r=a modulo b
        a=b
        b=r
        euclide(a,b)        
```

```python
def algo_euclide(a, b)
   if b == 0 :
      return a
   return gcd(a%b, a)
```

## Analyse des algorithmes

Il existe trois axes de vérifications d'un algorithme:
- **la terminaison** : est-que l'algorithme ne tourne pas de manière infinie ?
- **La correction** : est-que le résultat renvoyé est le bon ?
- **La complexité** :  quel est le temps d'exécution d'un algorithme et la mémoire qu'il requiert?

https://isn-icn-ljm.pagesperso-orange.fr/1-NSI/res/res_cours_algo.pdf


### :fa fa-stopwatch: Coût d'un algorithme (complexité temporelle)

Pour mesurer la complexité temporelle d'un algorithme on compte le nombre maximal d'opérations exécutées par un programme. Chaque affectation (a = 2), comparaison (a>0), accès en mémoire (lire fichier a.txt), et opération élémentaire (a+b) compte pour une opération (une unité de temps). 
Ainsi, la complexité (noté T(n)) de l'expression `a <- a*b+3` est égale à 5 (une affectation, un accès à la mémoire pour a, un accès à la mémoire pour b, une multiplication, une addition).

#### L'exemple du parcours séquentiel d'un tableau

Pour illustrer la complexité temporelle (coût d'un algorithme), prenons l'exemple du parcours séquentiel d'un tableau. Il y a deux cas à traiter : 
- (i) l'entier recherché est présent dans le tableau en position j,
- (ii) l'entier n'est pas dans le tableau qui contient n élements.


```pseudo code
                                                 Nombre d'opérations       
                                               cas (i)          cas (ii)
tr ← Faux                                      (1 op.)          (1 op.)
i ← 1                                          (1 op.)          (1 op.)
tant que i <= longueur(t) et que tr == FAUX   (j+1 op.)        (n+1 op.) 
    si t[i]==x :                               (j op.)          (n op.) 
        tr ← VRAI                              (1 op.)          (0 op.)
    fin si
    i ← i+1                                    (j op.)          (n op.)
fin tant que
renvoyer la valeur de tr                       (1 op.)          (1 op.)

                                         TOTAL = 3j+5             3n+4
```

Le **coût de l’algorithme** est donné par le **nombre d’opérations effectuées dans le pire des cas**. 

?> Dans notre exemple, quel est le coût de l'algorithme ? <abbr title="Ici, le nombre d'opérations maximum est atteint lorsque le nombre recherché se situe en dernière position (position n)"> <i class="fas fa-life-ring"></i> Indices </abbr>. <!-- 3n+5 -->

#### Différents ordres de grandeur

Le coût d'un algorithme dépend très souvent de la taille (notée *N*) du jeux de données en entrée. Il existe un grand nombre d'ordre de grandeurs ([:fa fa-wikipedia-w](https://fr.wikipedia.org/wiki/Analyse_de_la_complexit%C3%A9_des_algorithmes)) dont les principaux sont les suivants :
- Complexité **constante** *0(1)* : si le nombre d'opérations ne dépend pas de N,
- Complexité **logarithmique** *0(log N)* : si le nombre d'opérations est proche de log(N),
- Complexité **linéaire** *0(N)* : si le nombre d'opérations est d'ordre N,
- Complexité **quadratique** *0(N²)* : si le nombre d'opérations est d'ordre $N^2$,
- Complexité **exponentielle** *0($2^N$)* : si l'ordre est une forme de puissance de N.

Le coût de l'algorithme du parcours séquentiel d'un tableau (3n+5) est linéaire (noté).

![Représentation graphique des principaux ordres de grandeur des complexités algorithmiques](../_img/complexite.png ':size=80%')

<p class="center-p"> 

Représentation graphique des **principaux ordres de grandeur** des complexités algorithmiques. 

</p>

?> Compter le nombre d'opération faire_la_fete() exécutées par les algorithmes suivants avec n=3. Exprimer le nombre d'opération faire_la_fete() exécutées par les algorithmes 1 à 4 en fonction de n. Puis noter le type de complexité de tout les algorithmes.


```python
# Algo 1
for i in range (1, 5*n/n):
    faire_la_fete()

# Algo 2
for i in range(1, n):
    for j in range(1, n):
        faire_la_fete()

# Algo 3
for i in range(1, n):
    for j in range(1, i):
        faire_la_fete()

# Algo 4
for i in range(5, n-5):
    for j in range(i-5, i+5):
        faire_la_fete()

# Algo 5
for i in range(1, n):
    for j in range(1, i):
        for k in range(1, j):
            faire_la_fete()
```

<!-- 
Algo 1 : 5                  -> Constant
Algo 2 : n*n=n²             -> Quadratique
Algo 3 : n*(n+1)/2          -> Quadratique O(n²)
Algo 4 : (n-9)*11 = 11n-99  -> Linéaire O(n)
Algo 4 : (n-9)*11 = 11n-99  -> O()
-->



http://www.monlyceenumerique.fr/nsi_premiere/algo_a/a2_complexite.php

## Algorithme de tri
http://www.monlyceenumerique.fr/nsi_premiere/algo_a/a3_tri_invariant.php#4

### Tri par insertion


### Tri par sélection


?> Écrire un algorithme en pseudo code qui calcule la moyenne de trois nombres a, b et c. Le résultat sera stocké dans une variable moy. 

?> Écrire un algorithme qui permet d’échanger le contenu de deux variables var1 et var2
