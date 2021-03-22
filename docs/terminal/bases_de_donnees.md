# BASES DE DONNÉES <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>
!> !! Work in progress !!

## Modèle relationnel

### Un peu d'histoire

<div class="timeline">
  <div class="container left">
    <i class="icon fa fa-scroll"></i>
    <div class="content-timeline">
      <strong>Fiche Papier</strong>
      <p>
        Fiche Papier  </p>
    </div>
  </div>
  <div class="container right">
    <div class="date">1960</div>
    <i class="icon fa fa-laptop"></i>
    <div class="content-timeline">
      <strong>Fichier informatique dépendant des logiciels applicatifs</strong>
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
      <strong>NoSQL (Not only SQL)</strong> 
      <p>Apparition d'une nouvelle famille de base de données (pas au programme)</p>
    </div>
  </div>
</div>

<p class="center-p"> <strong> Frise historique </strong> des outils de gestions de bases de données (très simplifiées) </p>

---

![](../_img/table_BD_vs_tableau.png ':size=70%')

Les logiciels types tableurs (par ex. Excel ou LibreOffice Calc) sont apparus à peu près en même temps que les premiers logiciels basées sur les modèles relationnels. Les tableurs sont souvent plus intuitifs et simples au premiers abord mais comporte quand même quelques désavantages quand il s'agit de modéliser des données relativement complexes.

<p class="center-p"> <strong> Table de comparaison  </strong> entre le modèle par tableur et le modèle relationnel </p>

---

### Contraintes d'intégrité (=règle de cohérence)

- **Entité** : chaque enregistrement (chaque entité) est unique (=> clef primaire)
- **Référence** : les relations (tables) sont liés par des attributs (=> clef étrangère)
- **Domaine** :  les attributs sont typés (INT, BOOL, CHAR ...)
- **Métier** :  toutes autres contraintes (par ex. un mail doit contenir un @) 



![](../_img/table_BD.png ':size=60%')

<p class="center-p"> <strong> Modèle de relation entre deux tables </strong> </p>

---

## Bases de données relationnelles : le language SQL


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

