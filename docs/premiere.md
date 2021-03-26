# Première NSI

## Les Outils

## Progression prévue

Sur l'année 36 semaines x 2 séquences = 72 séquences (comptons 5 semaines pour faire face aux imprévus) :

- Présentation de l'UE et des outils (1 séance)
- Histoire de l'informatique (2 séances)
- Base de la programmation (4 séances)
- Introduction à python (3 séances)
- Codage et typage (8 séances)
- Types construits (6 séances)
- Données en tables (3 séances)
- Interface Homme-Machine (8 séances)
- Architecture et système d'exploitation (5 séances)
- Algorithmique (12 séance)

- En parallèle (15 séances) : Projet web, séances de devoir surveillé, séances de fichage de cours en commun


## Listes des capacités attendues en NSI 1ère

### HISTOIRE

- Situer dans le temps les principaux évènements de l'histoire de l'informatique et ses protagonistes 
    

### DONNÉES

#### Représentation des données : Types et valeurs de bases

- Compter en base 2, 10, 16  
    
    - Passer de la **base 10** à la **base 2**  
    - Passer de la **base 10** à la **base 16**

- Évaluer le nombre de **bits** nécessaires à l'écriture en base 2 d'un entier
    
- Savoir calculer le **complément à 2**

- Comprendre la notion de **nombre flottant**
    - Expliquer pourquoi 0.2 + 0.1 == 0.3 n'est pas un bon test

- Savoir utiliser les **valeurs booléennes** et les **opérateurs booléens** (AND, NOT, AND NOT, OR, XOR)

- Expliquer succintement les caractéristiques et les interêts des **systèmes d'encodages** ASCII, IS0-2259-1, UTF-8


#### Représentation des données : types construits (ex. avec python)
- Comprendre l'utilisation et la syntaxe python des **p-uplets** (tuples)

- Créer, lire et modifier un **tableau** 
    - Construire un tableau par compréhension

- Construire des **matrices** a[i][j] sous forme de tableau de tableau 
    
- Construire et manipuler un **dictionnaire** 
    - Savoir utiliser les méthodes 'keys()', 'values()' et 'items()' :
    - Itérer les élements d'un dictionnaires

#### Traitements des données en tables
- **Importer** une table en format csv
- **Sélectionner** les lignes d'une table selon des **conditions**
    - Savoir rechercher des doublons de lignes
- **Trier** une table en sélectionnant la colonne de tri
- **Fusionner** deux tables en respectant les **domaines de valeurs**

### MACHINES
#### Interactions hommes machines sur le Web
- Identifier les différents **composants permettant d'interagir** avec une application web à travers des **évenements**
- Analyser et modifier les **méthodes exécutées** lors d'un clic sur un bouton d'une page Web (par ex. en **javascript**)
- Distinguer les exécutions côté **client** et côté **serveur**
- Savoir passer des paramètres à un site grâce au **protocole http**
    - Distinguer les transmissions de paramètres **GET** et **POST**
    - Comprendre le fonctionnement d'un formulaire simple
- Reconnaître quand et pourquoi la transmission est **chiffrée**

#### Architecture matérielles et systèmes d'exploitation
- Connaître le modèle d'**architecture séquentielle** de **von Neumann**
     - Distinguer les rôles et les caractéristiques des constituants d'une machine
     - Dérouler l'éxecution d'une séquence d'instructions simples du type language machine
       
- Décrire les **protocoles de communications** aux seins des **réseaux** de machines
    - Comprendre l'intérêt du découpage de données en **paquets** et leur **encapsulation**
    - Dérouler le fonctionnement d'un protocole simple de **récupération de perte de paquets** (bits alterné)

- Lister les fonctions principales d'un **système d'exploitation**

- Utiliser les commandes de base **Unix** dans un **terminal**
    - Se déplacer dans l'**arborescence** des dossiers
    - Copier, déplacer, supprimer, exécuter un fichier
    - Gérer les **droits** et les **permissions** d'accès aux fichiers

- Identifier le rôle des **capteurs** et **actionneurs** dans un système homme machine

- Réaliser par programmation une interface homme machine (**IMH**) répondant à un cahier des charge donné

### PROGRAMMATION
#### Language et programmation
- Connaître les **constructions élémentaires** 
    - Comprendre les notions de séquences, affectations, conditionnelles, boucles bornées et non bornées, appels de fonction

- Repérer dans un **nouveau language de programmation** ses caractéristiques

- Savoir construire une **fonction** 
    - **Prototyper** une fonction
    - Décrire les **préconditions** sur les arguments
    - Décrire les **postconditions** sur les résultats

- Mettre au point un programme en le **testant**

- Savoir utiliser une **bibliothèque** et savoir expliquer l'intérêt de ce sysytème d'extension du language

#### Algorithmique

- Savoir écrire un algorithme simple en pseudo-code et en python
    - Écrire un **algorithme de recherche** d'une occurence sur des valeurs de type quelconque 
    - Écrire un **algorithme calcul d'une moyenne** d'un tableau
    - Écrire un **algorithme de tri** par **insertion** et par **sélection**
    - Décrire un **invariant de boucle** qui prouve la **correction** des tris par insertion et par sélection
    - Calculer le **coût temporel** (linéaire, quadratique, ...) et **spatial** de ces algorithmes 
    - Justifier la **terminaison** de ces algorithmes

- Savoir écrire un **algorithme d'apprentissage** à travers l'exemple des **k plus proches voisins** 

- Montrer la **terminaison** de la recherche dichotomique à l'aide d'un **variant de boucle** 

- Résoudre un problème grâce à un **algorithme gloutons** (par ex. problème du rendu de monnaie)
