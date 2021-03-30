# DONNÉES EN TABLES <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

## :fa fa-play-circle: Introduction

Pour stocker des données de façon fiable et organisé il existe plusieurs
façons de procéder. Les jeux de données les plus complexes utilisent des
logiciels de bases de données (**SGDB** = **système de gestion de bases de
données**). Pour des petits jeux de données simples, il existe des formats
de stockages plus simple comme le **JSON** ou encore le **CSV**.

Les données doivent être décrites, par un **descripteur** compréhensible
pour celui qui veut les interpréter. Par exemple, considérons
l'organisation d'une médiathèque. Lors de son inscription chaque abonné
fournit des données (nom, prénom, adresse...). Ces données seront
associées aux **descripteurs** « Nom », « Prénom », « Adresse »... Ces
données des abonnés seront regroupées dans **collection** sous forme de
une **table**. Chaque ligne de la table est un abonné, chaque colonne
est un **descripteur**. De la même manière, on peut faire une
**collection** des ouvrages avec les **descripteurs** (Titre, Type de
livres, Auteur(s), Emprunté par...). Chacune de ces collections,
c'est-à-dire chacune de ces tables, peuvent être liés entre elles dans
une base de données.

?> Faire un schéma qui représente les données d'une médiathèque et leur
relations.

?> Dans l'exemple de la médiathèque, qu'elle est le descripteur qui
permet de faire le lien entre la table (collection) des abonnées et
celle des ouvrages ?

## :fa fa-file-csv: Le format CSV

Le format **CSV** (de l'anglais *comma separated value*, c'est-à-dire
« **valeurs séparées par des virgules** ») est un format texte utilisé
couramment pour représenter des données structurées en tableau. On peut
facilement importer ou exporter des fichiers *.csv* avec un tableur (par
ex. Libreoffice Calc).

?> Ouvrir les fichiers results.csv et Pokemon.csv avec
Libreoffice Calc puis avec le logiciel VScodium. Les deux logiciels
réagissent-ils pareil à l'ouverture d'un fichier CSV ?

Dans le format CSV, chaque ligne représente un **enregistrement** (par
exemple chaque ligne correspond à un match ou à un nom de Pokémon). Sur
chaque ligne, les différents **attributs** de l'enregistrement (qui
correspondent à des colonnes) sont réparés par une virgule (il existe
d'autres types de **séparateur** comme la tabulation ou le point virgule).

Le format JSON est un peu différent et permet l'imbrication de données
plus complexes. Par exemple, si vous voulez faire la liste des joueurs
qui ont participé à chaque match du fichier *results.csv* et que vous
voulez indiquez leur âge, il faut faire un deuxième tableau en CSV alors
qu'en JSON on peut l'inclure directement dans le même fichier.

?> Convertir le fichier <a href="https://adrientaudiere.github.io/cours_nsi/_doc/pokemon.csv" target="_blank" rel="noopener"> pokemon.csv</a> en JSON grâce à ce
[site](https://csvjson.com/csv2json).

## :fab fa-python: Importer/exporter les fichiers CSV avec python

### Importer des données CSV

Pour importer un fichier CSV dans un environnement python en vue
d'utiliser les données ensuite, on utilise la bibliothèque **csv**. Dans
cette bibliothèque, deux fonctions principales permettent d'importer un
fichier .csv :

- la fonction ***reader()*** renvoie un objet *csv.reader* qui est une
**liste**.

```python
import csv # importation de la bibliothèque csv

file = open("test.csv", "r") # ouverture du fichier (ici par chemin relatif)

csvenliste = csv.reader(file, delimiter = ",") #initialisation d'un lecteur de fichier, ici delimiter est facultatif puisque la virgule est la valeur par défaut

for ligne in csvenliste:  #parcours du lecteur avec une boucle
    print(ligne)  #affichage ligne à ligne

file.close()  #fermeture du fichier
```

- la fonction ***DictReader()*** renvoie un objet **dictionnaire** ordonné *csv.DictReader*.

```python
import csv  #importation de la bibliothèque csv

file = open("test.csv", "r")  # ouverture du fichier (ici par chemin relatif)

csvendico = csv.DictReader(file)  #initialisation d'un lecteur de fichier avec création automatique de dictionnaire

for ligne in csvendico:  #parcours du lecteur avec une boucle
    print(dict(ligne))  affichage ligne à ligne

file.close()  #fermeture du fichier
```


### Exporter des données CSV

?> La fonction ci-dessous permet d'exporter un fichier csv vers
votre ordinateur. Annoter le code ligne par ligne avec des commentaires
qui explique ce que fait la ligne de code.

```python
import csv
def vers_csv(nom_de_la_table, ordre, nom_du_fichier_csv):
    table=eval(nom_de_la_table)
    with open(nom_du_fichier_csv+'.csv',"w") as fic:
        dic=csv.DictWriter(fic, fieldnames=ordre)
        dic.writeheader()
        for ligne in table:
            dic.writerow(ligne)
    return None

table_exemple=[{'nom': 'Dupont', 'prenom': 'Jean-Claude', 'age': '32'},{'nom': 'Duteil', 'prenom': 'Paul', 'age': '41'},{'nom': 'Claudon', 'prenom': 'Goery', 'age': '37'},{'nom': 'Tonton', 'prenom': 'Pierre', 'age': '54'},{'nom': 'Penard', 'prenom': 'Bob', 'age': '18'},{'nom': 'Herpoix', 'prenom': 'Stephane', 'age': '55'},{'nom': 'Salicorne', 'prenom': 'Bruno', 'age': '15'},{'nom': 'Poiteau', 'prenom': 'Maxe', 'age': '33'},{'nom': 'Clanget', 'prenom': 'Gilles', 'age': '54'},{'nom': 'Luillier', 'prenom': 'Martin', 'age': '34'},{'nom': 'Clanget', 'prenom': 'Justine', 'age': '14'},{'nom': 'Gillier', 'prenom': 'Paul', 'age': '16'}]
ordre = ['nom', 'prenom', 'age']
vers_csv('table_exemple', ordre, 'mon_fichier_example')
```


## :fa fa-keyboard: Manipulez les données


?> Faire le TP Titanic en ouvrant le fichier [TP_Titanic.ipynb](https://adrientaudiere.github.io/cours_nsi/_doc/TP_Titanic.ipynb) (TP issus du site https://isn-icn-ljm.pagesperso-orange.fr/) avec VScodium.
