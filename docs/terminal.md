# Terminal NSI

## Au programme du BAC 2022 : 

1. Structure de données:
    - Structure de données; interface et implémentation  [:fa fa-atlas:](/terminal/algo.md#structure-de-données)
    - Vocabulaire de la programmation orienté objet (classes, attributs, méthodes, objets) [:fa fa-atlas:](/terminal/programmation.md#programmation-orientée-objet)
    - Listes, piles, files, dictionnaires (index et clef) [:fa fa-atlas:](/terminal/algo.md#liste)
    - Arbres (structure hiérarchique), arbre binaire (nœuds, racines, feuilles, sous arbres) [:fa fa-atlas:](/terminal/algo.md#structures-en-arbres)
  
2. Bases de données 
    - Modèle relationnel (relation, attribut, domaine, clef primaire, clef étrangère, schema relationnelle) [:fa fa-atlas:](/terminal/bases_de_donnees.md#le-modèle-relationnel)
    - Base de données relationnelle [:fa fa-atlas:](/terminal/bases_de_donnees.md#le-modèle-relationnel)
    - Langage SQL: requêtes d'interrogation et de mise à jour [:fa fa-atlas:](/terminal/bases_de_donnees.md#le-language-sql)

3. Architectures matérielles, systèmes d'exploitation et réseaux
    - Composants intégrés d'un système sur puce [:fa fa-atlas:](terminal/archi_os_reseaux.md#circuits-intégrés)
    - Gestion de processus et des ressources par un système d'exploitation [:fa fa-atlas:](terminal/archi_os_reseaux.md#gestion-des-processus-et-des-ressources)
    - Protocole de routage [:fa fa-atlas:](terminal/archi_os_reseaux.md#protocoles-de-routage)

4. Langages et programmation
    - Récursivité [:fa fa-atlas:](/terminal/programmation.md#récursivité)
    - Modularité [:fa fa-atlas:](/terminal/programmation.md#modularité)
    - Mise au point de programmes. Gestion des bugs.  [:fa fa-atlas:](/terminal/programmation.md#mise-au-point-de-programme)

5. Algorithmique
    - Algorithme sur les arbres binaires et sur les arbres binaires de recherche [:fa fa-atlas:](/terminal/algo.md#structures-en-arbres)
    - Diviser pour régner [:fa fa-atlas:](/terminal/algo.md#diviser-pour-régner)
  
## Au programme après le bac

- Évènements clés de l'histoire de l'informatique (répartie dans l'ensemble du cours)
- Graphes : structures relationnelles. Sommets, arcs, arêtes, graphes orientés/non orientés [:fa fa-atlas:](/terminal/algo.md#graphe)
- Système de gestion de bases de données relationnelles [:fa fa-atlas:](terminal/bases_de_donnees.md#systèmes-de-gestion-de-bases-de-données-sgbd)
- Sécurisation des communications [:fa fa-atlas:](terminal/archi_os_reseaux.md#sécurisation-des-communications)
- Notion de programme en tant que données. Calculabilité, décidabilité [:fa fa-atlas:](terminal/algo.md#calculabilitédécidabilité)
- Algorithmes sur les graphes [:fa fa-atlas:](/terminal/algo.md#graphe)
- Programmation dynamique [:fa fa-atlas:](terminal/algo.md#programmation-dynamique)
- Recherche textuelle [:fa fa-atlas:](terminal/algo.md#recherche-textuelle)


## Listes des capacités attendues en NSI Terminal

Les capacités indiquées en gris ne sont pas au programme du bac.

### HISTOIRE 

<div class="transparent">

- [ ] Situer dans le temps les principaux évènements de l'histoire de l'informatique et ses protagonistes 

</div>


### DONNÉES
#### Structure de données
- [ ] Spécifier une **structure de données** par son **interface**
    -  Expliquer la difference entre **interface** et **implémentation**

- [ ] Écrire la définition d'une classe (programmation orientée objet)
    - Définir les mots suivants : **classe**, **attribut**, **méthodes**, **instances**, **objets**
    - Coder une classe simple avec des ***setters*** et des ***getters*** 

- [ ] Connaître les structures en **listes**, **piles**, **files** et **dictionnaire**
    - Choisir une structure adaptée à la situation à modéliser
    - Expliquer la différence entre les modes **FIFO** (first in first out) et **LIFO** (last in first out)
    - Distinguer la recherche d'une valeur dans une **liste** et dans un **dictionnaire**

- [ ] Connaître les structures hiérarchiques tels que les **arbres binaires**  
    - Identifier des situations nécessitant une structure en **données arborescente**
    - Calculer des mesures sur un arbre binaire comme la **taille** et la **hauteur**

<div class="transparent">

- [ ] Modéliser des situations sous forme de **graphes**
    - Écrire des implémentations d'un graphe à partir d'une **matrice d'adjacence** 
    - Écrire des implémentations d'un graphe à partir d'une **liste de successeurs/prédécesseurs**

</div>

#### Bases de données

- [ ] Comprendre les concepts du **modèle relationnel**
    - Définir les mots suivants : **relation**, **attributs**, **domaine**, **clef primaire**, **clef étrangère**, **schéma relationnel**
    - Expliquer les **contraintes d'intégrité** (**domaine**, **relation** et **référence**)
    - Distinguer la **structure** d'une base de données de son **contenu**
    - Repérer les **anomalies** dans le schéma d'une base de données (redondances de données, anomalies d'insertion, de suppression, de mise à jour)


<div class="transparent">

- [ ] Lister les services rendus par un **système de gestion de base de données relationnelles** : persistance des données, gestions des accès concurrents, efficacité du traitement des requêtes, sécurisation des accès

</div>

- [ ] Construire des **requêtes SQL d'interrogation** (**SELECT**, **FROM**, **WHERE**, **JOIN**) et d'insertion (**UPDATE**, **INSERT**, **DELETE**) en sachant trier (**ORDER BY**), effectuer des **fonctions d'agrégation** (par ex. **COUNT**) et en enlevant les doublons (**DISTINCT**)

### MACHINES
#### Architectures matérielles, systèmes d'exploitation et réseaux

- [ ] Identifier les principaux composants d'un système sur puce (**SoCs**, *Systems on Chips*) et les avantages de leur intégration en termes de vitesse et de consommation

- [ ] Décrire la création d'un **processus** et l'**ordonnancement** de plusieurs processus par le système d'exploitation
    - comprendre les sorties de la fonction ***top***
    - mettre en évidence le risque d'**interblocage** (deadlock)

- [ ] Identifier la **route** empruntée par un **paquet**
    - expliquer la notion de **table de routage**
    - différencier les **protocoles RIP** et **OSPF**


<div class="transparent">

- [ ] Décrire les principes du **chiffrement**, notamment dans le protocole de communication **HTTPS** (association d'un protocole asymétrique et d'un symétrique)
    - Décrire le principe du **chiffrement symétrique** (**clef partagée**) 
    - Décrire le principe du **chiffrement asymétrique** (**clef privée** / **clef publique**) 
    - Expliquer la notion de **tiers de confiance**

</div>

### PROGRAMMATION
#### Langages et programmation

- [ ] Effectuer des algorithmes sur des structures arborescentes de type **arbres binaires**
    - Calculer la **taille** et la **hauteur** d'un **arbre binaire**
    - **Parcourir** un arbre de différentes façons (infixe - préfixe - suffixe ; ordre en largeur d'abord)
    - Rechercher et insérer une **clef** dans un arbre de recherche
    - Montrer que la recherche dans un **arbre de recherche équilibré** est de **coût logarithmique** (en temps)


<div class="transparent">

- [ ] Effectuer des algorithmes sur des **graphes**
    - **Parcourir** un graphe en **profondeur** d'abord ou en **largeur** d'abord 
    - Repérer la présence d'un **cycle** dans un graphe
    - Chercher un **chemin** dans un graphe

</div>

- [ ] Écrire un algorithme utilisant la méthode "**diviser pour régner**"


<div class="transparent">

- [ ] Écrire un algorithme **dynamique** (par ex. l'alignement des séquences ou le rendu de monnaie)

- [ ] Étudier l'algorithme de **Boyer-Moore** pour la recherche d'un **motif** dans un texte

</div>


