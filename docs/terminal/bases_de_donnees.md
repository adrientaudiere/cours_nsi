# BASES DE DONNÉES <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

## Un peu d'histoire

Sauvegarder des informations sous la forme de données est une activité fondamentale des sociétés humaines. Les premières traces d'écriture sont liées aux besoins de stocker des valeurs (par ex. l'[écriture cunéiforme](https://fr.wikipedia.org/wiki/Cun%C3%A9iforme) des livres de comptes de la cité d'Uruk et Lagash vers 3400 av. J.-C.). L'objectif de stocker des données est donc intimement lié à l'évolution de l'Humanité. 


<div class="timeline">
<div class="container right">
    <i class="icon fa fa-feather-alt"></i>
    <div class="content-timeline">
      <strong>Première écriture </strong>
      <p>
        Les premières écritures (~3400 av. J.-C.) sont en lien directes avec le besoin de recenser des données. Les premiers supports étaient en argile, pierre, parchemin...
      </p>
    </div>
  </div>
  <div class="container left">
    <i class="icon fa fa-scroll"></i>
    <div class="content-timeline">
      <strong>Fiche Papier</strong>
      <p>
        Grâce à l'invention du papier (il y a 2000 ans en Chine), puis de l'imprimerie avec des morceaux de bois (<em>xylographie</em>, VIIe siècle en Asie) et de la presse d'imprimerie par Gutenberg (1451), il est facile produire des feuilles pour stocker des données.
      </p>
    </div>
  </div>
  <div class="container right">
    <div class="date">1960</div>
    <i class="icon fa fa-laptop"></i>
    <div class="content-timeline">
      <strong>Fichier informatique </strong>
      <p>Les premiers fichiers informatiques varient beaucoup selon les logiciels.</p>
    </div>
  </div>
  <div class="container left">
    <div class="date">1970</div>
    <i class="icon fa fa-database"></i>
    <div class="content-timeline">
      <strong>Modèle relationnel</strong> (<em>E.F. Codd.</em>)
      <p>
        Les modèles relationnels permettent des bases de données + complexe, + sécurisé, avec - d'erreurs, et un meilleur contrôle.
      </p>
    </div>
  </div>
  <div class="container right">
    <div class="date">1978</div>
    <i class="icon fa fa-table"></i>
    <div class="content-timeline">
      <strong>Invention des logiciels de type tableurs</strong> (<em>D. Bricklin.</em>)
    </div>
  </div>
  <div class="container left">
    <div class="date period">1980-1990</div>
    <i class="icon fa fa-database"></i>
    <div class="content-timeline">
      <strong>SQL</strong> (<em>Structured Query Language</em>)
      <p>
        SQL devient le langage standard (standardisation <abbr title="American National Standards Institute">ANSI</abbr> en 1986). C'est le début de la commercialisation à grande échelle des bases de données.
      </p>
    </div>
  </div>
   <div class="container right">
    <div class="date">2010</div>
    <i class="icon fa fa-database"></i>
    <div class="content-timeline">
      <strong>NoSQL (<em>Not only SQL</em>)</strong> 
      <p>Apparition d'une nouvelle famille de base de données (pas au programme)</p>
    </div>
  </div>
</div>

<p class="center-p"> <strong> Frise historique </strong> des outils de gestions de bases de données (très simplifiées) </p>

---

Les logiciels types tableurs (par ex. Excel ou LibreOffice Calc) sont apparus à peu près en même temps que les premiers logiciels basées sur les modèles relationnels. Les tableurs sont souvent plus intuitifs et simples au premiers abord mais comporte quand même quelques désavantages quand il s'agit de modéliser des données relativement complexes.


![](../_img/table_BD_vs_tableau.png ':size=70%')

<p class="center-p"> <strong> Table de comparaison  </strong> entre le modèle par tableur et le modèle relationnel </p>

---

## Le modèle relationnel

### Modéliser la bibliothèque du lycée

?> Vous avez pour mission collective de stocker les informations concernant les livres de la bibliothèque du lycée. Prenons 10 livres au hasard pour l'exemple. Proposez une façon de stocker ces informations. 

?> Dans un second temps, on voudrait permettre à toute personne de Scholae d'emprunter des livres. Comment mettre cela en place?


### Contraintes d'intégrité (=règle de cohérence)

- **Entité** : chaque enregistrement (chaque entité) est unique (=> clef primaire)
- **Référence** : les relations (tables) sont liés par des attributs (=> clef étrangère)
- **Domaine** :  les attributs sont typés (INT, BOOL, CHAR ...)
- **Métier** :  toutes autres contraintes (par ex. un mail doit contenir un @) 



![](../_img/table_BD.png ':size=60%')

<p class="center-p"> <strong> Modèle de relation entre deux tables </strong> </p>

---

## Le language SQL


?> Faire les parties 1 à 4 des [exercices en ligne](https://fxjollois.github.io/cours-sql/) de FX Jollois (IUT Paris Descartes). Prenez des notes à chaque fois qu'une information vous semble importante.


![](../_img/SQLite_figure.png ':size=100%')


<p class="center-p"> <strong> Exemple de code SQL </strong> avec à gauche les schéma ou les retours de fonction, et à droite l'état de la base de données. </p>

---

Le code complet de la figure ci-dessus est présenté ci-dessous. Vous pouvez le copier-coller et faire des tests en ligne avec l'[interpréteur SQLite](https://sql.js.org/examples/GUI/index.html). 

```sql
DROP TABLE IF EXISTS Monstres;
DROP TABLE IF EXISTS Types;

CREATE TABLE Monstres (
ID INT PRIMARY KEY,
Classe VARCHAR(20),
Niveau INT,
Type VARCHAR(20)
);

INSERT INTO Monstres VALUES (
  1, "Mage", 75, "Elf"
);
INSERT INTO Monstres VALUES (
  2, "Voleur", 5, "Troll"
);

SELECT Classe, Niveau 
FROM Monstres
WHERE Niveau>5;

CREATE TABLE Types (
 Type VARCHAR(20) 
        PRIMARY KEY,
 Cris VARCHAR(40),
 Humain INT, 
 FOREIGN KEY (Type)
       REFERENCES Monstres (Type)   
);

INSERT INTO Types
VALUES 
  ("Elf", "Yo!", 1),
  ("Troll", "Grrr", 0);

SELECT * From Types;

SELECT * FROM Monstres 
INNER JOIN Types
ON Monstres.Type = Types.Type
```


<details class="advanced_level">
<summary> <strong> Niveau avancé :</strong></summary>

?>  Pour s'exercer au SQL vous pouvez suivre les cours du [COLIBRI](https://colibri.unistra.fr/fr/course/list/notions-de-base-en-sql) de Strasbourg et vous entraîner sur la [Khan academy](https://fr.khanacademy.org/computing/computer-programming/sql).

</details>

## Systèmes de Gestion de Bases de Données (SGBD)

Un **SGBD** (**Systèmes de Gestion de Bases de Données**) est un logiciel qui permet … la gestion de bases de données en facilitant :
- la **création** de nouvelles bases de données et des relations (tables) qui s'y trouve,
- la **spécification des contraintes d'intégrités** et leur **respect** lors des modifications,
- la **modification** (ajout, suppression, mise à jour) de ces bases de données (modification d'entité, d'attribut ou de valeur),
- l'**interrogation** de la base de données (par ex. avec le langage SQL).

Les SGBD permettent souvent de définir plusieurs **niveaux d'utilisateurs** qui ont accès à des données/fonctions différentes. Ils sont souvent organisés sur un modèle **client-serveur** pour permettre à plusieurs utilisateurs d'avoir un **accès simultanés aux données**. Un autre aspect fondamental des SGBD modernes qui utilisent le langage SQL est que l'utilisateur peut demander des résultats sans coder la manière dont ils vont lui être donnés. Par exemple, si vous demandez une liste triée des livres d'une médiathèque datant de l'année 2000, vous ne faîtes aucune recommendation sur les algorithmes qui vont être utilisés (tri fusion par exemple). C'est le SGBD qui se charge de décider de la meilleure manière de calculer la réponse à votre question. C'est la raison pour laquelle le langage SQL est parfois qualifié de **langage déclaratif**.

### Propriétés ACID

En informatique, les propriétés ACID (atomicité, cohérence, isolation et durabilité) sont un ensemble de propriétés qui garantissent qu'une transaction informatique est exécutée de façon fiable ([:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Propri%C3%A9t%C3%A9s_ACID)).

- **Atomicité** : il faut qu'une transaction informatique se fasse complètement ou ne se fasse pas du tout. Cette propriété permet d'éviter des erreurs dûs à des transactions incomplètes. Par exemple, si une requête SQL d'ajout d'une entité n'ajoute qu'une partie des attributs (par ex. à cause d'une coupure de courant), alors il faut annuler la transaction.
 
- **Cohérence** : chaque transaction doit amener le système d'un état valide à un autre état valide. Par exemple, les contraintes d'intégrité d'une base de données doivent être respectées avant et après une requête.
     
- **Isolation** : chaque transaction est indépendante, elles s’exécutent comme si elles étaient seules sur le système. Ainsi une transaction T1 ne peux pas accéder à un état intermédiaire d'une transaction T2 qui est exécuté au même moment. Cela revient à dire que l'exécution de T1 et T2 simultanément doit produire le même résultat que leur exécution successive.
 
- **Durabilité** : la propriété de durabilité assure qu'une fois confirmée, une transaction demeure enregistré même en cas de panne informatique ou d'un autre problème. Par exemple, dans le cas d'une base de données relationnelle, une fois une requête SQL effectuée, la base modifiée doit être sauvegardée de façon permanente. 
 
> À noter qu'en informatique, la sauvegarde de façon permanente est un sujet complexe puisque que les différents supports de stockages informatiques les plus courants on des durées de vies assez courtes (voir une [Infographie](https://www.silkhom.com/quels-supports-de-stockage-pour-conserver-nos-donnees/) de 2012).


## Un peu de SQL sous python

On peut utiliser le langage SQL sous python dans sa version SQLite grâce à la bibliothèque `sqlite3`.

```python
import sqlite3
# Connexion à la base de données
## Créé une nouvelle BD si elle n'existais pas
connexion = sqlite3.connect('maBD.db') 
curseur = connexion.cursor()
# l'utilisation du nom cursor n'est pas au programme

# Exécution d'une requête
curseur.execute ("MA REQUÊTE SQL")

# Affichage des résultats de la requête
for element in curseur:
  print(element)

# Fermeture de la connexion
connexion.close()
```

?> Créer une base de données de vos 5 jeux préférés (ordinateurs, jeux de sociétés, sports...) entièrement sous python.

## Attaque par injection de code SQL

?> À l'aide d'une recherche sur le web, faire un schéma du processus à l'oeuvre lors d'une attaque informatique par injection de code SQL.