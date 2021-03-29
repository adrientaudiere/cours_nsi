# BASES DE DONNÉES <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>
!> !! Work in progress !!

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

## Systèmes de Gestion de Bases de Données (SGBD)

Un **SGBD** (**Systèmes de Gestion de Bases de Données**) est un logiciel qui permet … la gestion de bases de données en facilitant :
- la **création** de nouvelles bases de données et des relations (tables) qui s'y trouve,
- la **spécification des contraintes d'intégrités** et leur **respect** lors des modifications,
- la **modification** (ajout, suppression, mise à jour) de ces bases de données (modification d'entité, d'attribut ou de valeur),
- l'**interrogation** de la base de données (par ex. avec le langage SQL).

Les SGBD permettent souvent de définir plusieurs **niveaux d'utilisateurs** qui ont accès à des données/fonctions différentes. Ils sont souvent organisés sur un modèle **client-serveur** pour permettre à plusieurs utilisateurs d'avoir un **accès simultanés aux données**. Un autre aspect fondamental des SGBD modernes qui utilisent le langage SQL est que l'utilisateur peut demander des résultats sans coder la manière dont ils vont lui être donnés. Par exemple, si vous demandez une liste triée des livres d'une médiathèque datant de l'année 2000, vous ne faîtes aucune recommendation sur les algorithmes qui vont être utilisés (tri fusion par exemple). C'est le SGBD qui se charge de décider de la meilleure manière de calculer la réponse à votre question. C'est la raison pour laquelle le langage SQL est parfois qualifié de **langage déclaratif**.

### Propriétés ACID

!> !! Work in progress !!

## Un peu de SQL sous python

!> !! Work in progress !!

## Attaque par injection de code SQL

?> À l'aide d'une recherche sur le web, faire un schéma du processus à l'oeuvre lors d'une attaque informatique par injection de code SQL.


!> !! Work in progress !!

