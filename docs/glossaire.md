# Glossaire

## Liste de termes pour la Première

<div class="list_of_terms">

### Langages de programation

> Python

Langage de programmation [haut niveau](#bas_haut_niveau), [open source](#open_source), interprété, multi-paradigme et multiplateformes. Ce langage de programmation est le plus populaire depuis 2022 ([Source](https://www.tiobe.com/tiobe-index/)). Python est utilisé dans les domaines de la gestion d’infrastructure, l’analyse de données ou encore le développement de logiciels et d'applications. Il est notamment très utilisés dans les [projets libres]((https://code.gouv.fr/#/stats)) du gouvernement français.


> JavaScript (JS)

Langage de programmation qui permet de créer du contenu mis à jour de façon dynamique, de contrôler le contenu multimédia, d’animer des images, et tout ce à quoi on peut penser. On peut écrire de très nombreux [algorithmes](https://github.com/TheAlgorithms/Javascript/blob/master/Graphs/Dijkstra.js) avec JavaScript

> Langage bas/haut niveau <a name="bas_haut_niveau"></a>

> Logiciel libre, logiciel open source <a name="open_source"></a>



</div>

## Liste de termes pour la Terminale

<div class="list_of_terms">

### Structure de données

> Dictionnaire vs Tableau (également appelé Liste en python)

- un **dictionnaire** est une collection qui associe une clé à une valeur. Par exemple, il est possible d’associer la clé 'nom' à un nom et la clé 'prenom' à un prénom.

'''python
mon_dico = 
'''

- un **tableau** (aussi appelé abusivement **liste** en python) permet de stocker plusieurs valeurs (chaîne, nombre) dans une structure unique. 

> Piles 

Une pile est une structure de données qui ne permet que deux opérations : empiler un élément (qui consiste à ajouter un élément en haut de la pile) et dépiler un élément (qui consiste à retirer le dernier élément empilé et à lire son contenu). On parle de structure LIFO (*Last In First out*, dernier rentré premier sorti).

> Files

Une file est une structure de données qui ne permet que deux opérations : enfiler un élément (qui consiste à ajouter un élément à la fin de la file) et défiler un élément (qui consiste à retirer le premier élément enfilé et à lire son contenu). On parle de structure FIFO (*First In First out*, premier rentré premier sorti).

> Structure en Arbres (hauteur et degré)

Définition

> Arbres binaires

Arbre dans lequel tous le nœuds internes ne peuvent avoir que deux fils au maximum, c’est-à-dire de n’être que de degré 2, et dont la hauteur est illimitée.



### Programmation orientée objet

> Objet

Définition

> Classe

Définition

> Attribut

Définition

> Méthode

Définition

> Instance

Définition

### Modèle relationnel

> Relation

Définition

> Attribut

Définition

> Contrainte d'intégrité

Définition (parler du domaine)

> Clef primaire

Définition

> Clef étrangère

Définition

> Schéma relationnel

Définition

> SQL

Définition

> Bases de données

Définition

### Architectures matérielles

> SoCs

Définition

### Systèmes d'exploitation

> Processus

Définition

> Ordonnancement

Définition

### Réseaux

> Table de routage

Définition

> Protocole RIP _vs_ OSPF

Définition

> HTTP vs HTTPS

Définition

> Protocole TSL

Définition

> Chiffrement symétrique

Définition

> Chiffrement asymétrique

Définition

### Algorithmique

> Parcours infixe, préfixe et suffixe d'un arbre binaire

Définition

> Coût logarithmique

Définition

> Diviser pour mieux régner

Définition

> Algorithme dynamique

Définition

> Algorithme de Boyer-Moore

Définition

</div>

## Unité de mesure en informatique

Voici les mesures en informatiques selon le système international de notation scientifique.

| Unité (fr)  | Abbreviation (fr) | Correspondance       | Écriture    | En anglais (abbr.) |
| ----------- | ----------------- | -------------------- | ----------- | ------------------ |
| bit         | b                 | Un bit               |             | bit (b)            |
| octet       | o                 | 8 bits               |             | byte (B)           |
| kilo-octet  | ko                | 1 000 octets         | Millier     | kilo-byte (kB)     |
| Méga-octet  | Mo                | 1 000 000 octets     | Million     | Mega-byte (MB)     |
| Giga-octet  | Go                | 1 000 000 000 octets | Milliard    | Giga-byte (GB)     |
| Tera-octet  | To                | 1 000 Go             | Billion     | Tera-byte (TB)     |
| Peta-octet  | Po                | 1 000 000 Go         | Billiard    | Peta-byte (GB)     |
| Exa-octet   | Eo                | 1 000 000 000 Go     | Trillion    | Exa-byte (EB)      |
| Zetta-octet | Zo                | 1 000 Eo             | Trilliard   | Zetta-byte (ZB)    |
| Yotta-octet | Yo                | 1 000 Eo             | Quadrillion | Yotta-byte (YB)    |

!> Les notations en anglais prêtent à confusion : les mesures avec un b minuscule sont 8 fois plus petites que les mesures avec un B majuscule.

$$
8Mb = 8 000 bits = 1 Mo (1000 octets) = 1 MB
$$
$$
32 Gb != 4 GB = 4 Go
$$

L'utilisation de ce système basé sur la base de 10 est imprécis en informatique qui se base sur la base 2 pour calculer
la mémoire d'un ordinateur. Il est maintenant recommandé d'utiliser un système dérivé qui prend en compte le caractère binaire
des mesures en informatique. Les préfixes binaires sont de la forme :

| Nom  | Symbole | Puissance de 2                                       |
| ---- | ------- | ---------------------------------------------------- |
| kibi | Ki      | $2^{10} = 1\,024 $                                   |
| mébi | Mi      | $2^{20} = 1\,048\,576 $                              |
| gibi | Gi      | $2^{30} = 1\,073\,741\,824 $                         |
| tébi | Ti      | $2^{40} = 1\,099\,511\,627\,776 $                    |
| pébi | Pi      | $2^{50} = 1\,125\,899\,906\,842\,624 $               |
| exbi | Ei      | $2^{60} = 1\,152\,921\,504\,606\,846\,976 $          |
| zébi | Zi      | $2^{70} = 1\,180\,591\,620\,717\,411\,303\,424$      |
| yobi | Yi      | $2^{80} = 1\,208\,925\,819\,614\,629\,174\,706\,176$ |

L’usage de cette norme de préfixe binaire ne s’est pas encore généralisé totalement. Certains logiciels et systèmes d’exploitations (comme Ubuntu à partir de la version 10.10 et Mac OS X à partir de Snow Leopard) se sont mis à jour avec cette norme et propose donc des valeurs en GiO plutôt qu'en GO. D'autres entreprises, comme Microsoft Windows pour ne pas les citer, continuent d'utiliser des valeurs binaires avec des préfixes SI (système international). Les fabricants de périphérique de stockage utilisent également les préfixes SI car la valeur est ainsi plus élevé. Un disque dur de 1 To est en fait un disque dur pouvant contenir 0.91 TiO, ce qui est moins vendeur...

## Divers

<div class="list_of_terms">

> Dossier caché

Un dossier caché est un dossier invisible sauf à le demander expressément. Il s'agit d'un moyen de simplifier le cheminement dans l'arbre des dossiers. On symbolise ces dossiers par un point devant le nom (par ex. ".monDossier").

Les dossiers cachés sont visibles via la commande ls -a (a pour all) et sont accessibles par leur chemins comme les dossiers normaux.
Les fichiers cachés suivent le même principe.

> Fichier caché

Sous Linux les fichiers et dossiers cachés sont matérialisés par un point devant leur nom.Exemple : .sshLes fichiers et dossiers cachés sont visibles via la commande ls -a (a pour all) et sont accessibles par leur chemins comme les dossiers normaux. Exemple de chemin : ~/.ssh

> Git 

Git est un langage TO DO
[Fiche de commande](https://training.github.com/downloads/fr/github-git-cheat-sheet.pdf)


</div>


