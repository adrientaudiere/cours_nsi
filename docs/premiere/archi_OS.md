# ARCHITECTURE MATÈRIEL ET SYSTÈME D'EXPLOITATION <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

## :fa fa-laptop: Introduction : c'est quoi un ordinateur

Un ordinateur est « un système de **traitement de l'information**
programmable tel que défini par **Alan Turing** et qui fonctionne par la
lecture séquentielle d'un **ensemble d'instructions**, organisées en
**programmes**, qui lui font exécuter des **opérations logiques et
arithmétiques**. Sa structure physique actuelle fait que toutes les
opérations reposent sur la **logique binaire** et sur des nombres formés
à partir de **chiffres binaires** »
([:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Ordinateur)). L'aspect
binaire a été abordé dans le cours sur le codage. Nous avons utilisé
l'aspect suite d'instruction organisées en programmes à travers au
langage python. Dans ce chapitre, nous allons étudier l'**architecture
de l'ordinateur de Von Neumann** qui permet les opérations arithmétiques
et logiques. Pour un aspect historique de l'apparition des ordinateurs,
référez-vous au cours [Histoire de l'informatique](premiere/histoire.md).


Nous verrons ensuite la notion de **système d'exploitation** (souvent
abrégé **OS** pour « Operating System ») à travers l'exemple de l'OS
GNU/Linux. Le système d'exploitation (dont les plus connus sont Windows,
Mac OsX, Linux et Android) est une couche qui simplifie l'accès à la
machine. L'OS fait le lien entre (i) la partie matérielle (processeur,
mémoire interne et externe, périphériques comme les écrans, les souris,
les claviers...) et (ii) la partie logicielle qui permet d'interagir
facilement avec un ordinateur (logiciel de traitement de texte,
navigateur internet, jeux...). La partie matérielle est également
appelée ***Hardware*** et la partie logicielle ***Software***.

?> Citer le système d'exploitation, ainsi que 4 logiciels présents sur vos postes informatiques de Scholae.

## :fa fa-sitemap: L'architecture de la machine de Von Neumann


<div class="img-flow" style="max-width:320px;">

![Architecture de Von Neumann](/../_img/Von_Neumann_architecture_fr.svg)

<p class="center-p"><strong>Architecture de Von Neumann </strong> : l'unité de contrôle et l'UAL forment l'<strong>unité centrale</strong> aussi appelé <strong>processeur</strong>. <p>
</div>

L'architecture de Von Neumann d'un ordinateur se résume par le schéma
suivant : **L'unité arithmétique et logique UAL** (en anglais ALU :
*Arithmetical and Logical Unit*) effectue les opérations arithmétiques
(incrémentation, décrémentation, addition, soustraction, propagation de
la retenue...) et logiques (ET, OU, NON, NOR, NAND, XOR). Elle est
intègre souvent une unité de calcul en virgule flottante (en anglais
FPU : floating-point unit) afin d'accélérer les calculs sur les nombres
réels. L'UAL contient plusieurs **registres** (petites mémoires d'accès
rapides) dont les principaux sont **l'accumulateur** qui sert à stocker
les données traitées par l'UAL et **le registre d'état** servant à
stocker les résultats de la dernière instruction traitée.

L'unité de contrôle ou **séquenceur** (en anglais : *Control Unit*) gère
le séquencement des instructions au rythme d'une horloge. Il gère
l'envoi des instructions à l'UAL. Elle contient également des registres
dont les principaux sont le **registre d'instruction** qui stocke
l'instruction en cours d'exécution et le **compteur ordinal** qui stocke
l'adresse de l'instruction suivante.

**La mémoire** contient à la fois les données et le programme qui
indique à l'unité de contrôle les instructions à effectuer. Elle se
divise entre **mémoire volatile** pour les programmes et données en
cours de fonctionnement (registres du processeur, mémoire cache, mémoire
vive RAM) et **mémoire permanente** pour les programmes et données de
base de la machine (disque dur, mémoire morte ROM). La mémoire volatile
est beaucoup plus rapide que la mémoire permanente, c'est pourquoi la
mémoire vive sert de stockage temporaire des données que le disque dur
doit transférer au processeur. L'**unité de gestion des bus** (ou unité
entrées-sorties) gère les flux d'informations entrant et sortant.

Un **microprocesseur** est un circuit intégré qui contient toutes les
composantes de l'architecture de Von Neumann. Il contient en effet une
mémoire cache permettant d'accélérer le traitement en limitant l'accès à
la mémoire vive. Le cache d'instructions reçoit les prochaines
instructions à exécuter et le cache de données manipule les données.

## :fa fa-language: Du matériel au programme : du rôle du langage en informatique

### Le langage assembleur

Pour rappel, un **processeur** est constitué de milliards de transistors
qui utilise la présence de courant pour effectuer des calculs. Les
processeurs font tourner des **programmes** (suite d'instructions
élémentaires) qui ont besoins de **données** et qui **sont eux-mêmes des
données**. Ces données (y compris le programme) sont enregistrées dans
la **mémoire** sous forme **binaire**. Par conséquent pour qu'un
processeur effectue un calcul il faut lui passer des commandes du type
« 01001010 01011101 11011101 00101010 11110111 ».

Pour permettre aux humains de donner des instructions à l'ordinateur,
les fabricants de processeurs ont inventé un langage qui représente le
langage machine sous une forme lisible par un humain tout en restant
très rapide à exécuter, car de plus bas niveau possible. Ce langage le
plus bas niveau lisible par un humain est appelé langage assembleur. Il
dépend du processeur utilisé. Vous pouvez voir quelques exemples de
codes assembleurs (extension .asm) sur
[:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Assembleur#Exemples_simples).
Le nom **mov** correspond à l'instruction 10101101 01111001 dans un
langage assembleur. Le programme assembleur est un programme qui va
transcrire le langage assembleur en langage machine.


?> À l'aide de recherche sur internet, trouver les instructions
en langage assembleur x86 pour (i) incrémenter une valeur, (ii) comparer
deux nombres, (iii) additionner deux nombres.

?> [TP](https://adrientaudiere.github.io/cours_nsi/_doc/TP-VonNeumann_vanZuijlen.pdf) sur VonNeumann (auteur vanZuijlen, [CC-BY-NC](https://creativecommons.org/licenses/by-nc/2.0/fr/))


### Langages de haut niveau

Coder en assembleur est plus facile qu'en binaire, mais cela reste
fastidieux en particulier à cause de la **manipulation des données** qui
doivent être placées octet par octet dans la mémoire ou dans les
registres. À cela s'ajoute la diversité des langages assembleurs en
fonction des processeurs qui empêchent la **portabilité** (un programme
est dit non portable s'il fonctionne sur certaines machines et pas
d'autres) du langage. Enfin les langages assembleurs ont un nombre de
fonctions très restreints ce qui les rend plus **fastidieux** à écrire
et paradoxalement **plus long à maîtriser** que d'autres langages.

![Échelle de niveau des langages informatiques](../_img/echelle_niveau_langage_informatique.svg ':size=50%')

<p class="center-p"> 
<strong>Échelle de niveau des langages informatiques.</strong>
<p>

Pour résoudre ces inconvénients (gestion de la mémoire, portabilité
faible, abstraction faible qui rend le développement de logiciel plus
ardu), il existe ensemble de langages qui sera traduit en langage
assembleur :**** les langages de haut niveau****. Plus un langage est de
haut niveau plus il a un niveau d'abstraction élavé et moins il****
dépend du processeur et du système d'exploitation. En revanche, les
langages de bas niveaux sont plus rapides et permettent une gestion fine
de la mémoire.

?> À l'aide du site [Rosetta code](http://www.rosettacode.org/wiki/Hello_world/Graphical),
trouver comment écrire « hello world » dans les langages suivants : AArch64, Assembly, C, C++, Rust, Python (avec la library Tkinter), Java, Javascript et PHP.

## :fab fa-linux: Le système d'exploitation Linux

### C'est quoi un système d'exploitation

?> À faire : Regarder cette [**vidéo**](https://invidious.tube/watch?v=SpCP2oaCx8A). Quelles sont les trois idées clés de cette vidéo ?

Un **système d'exploitation** est un ensemble de programme qui **gèrent les
ressources matérielles et logicielles** d'un ordinateur. Il fait le lien
entre les programmes (logiciels) utilisés et le matériel. Dans les
systèmes d'exploitation modernes, on trouve l'**ordonnanceur** qui décide
quel programme s'exécute à un instant t, le **gestionnaire de mémoire**, les
**pilotes de périphériques**, la **pile réseau** qui implémente les protocoles
réseaux (notamment TCP/IP) et le **système de fichier**.

Hormis Windows, la majorité des systèmes d'exploitation (Linux, Android,
macOS, iOS...) respectent un ensemble de standards regroupés sous le nom
de **POSIX** (Portable Operation System Interface). Les systèmes POSIX sont
**multi-utilisateurs** : il peut exister plusieurs utilisateurs sur une
machine qui ont des droits différents sur les fichiers (lire, écrire,
exécuter). Un utilisateur spécial appelé ***root*** ou super-utilisateurs
est l'**administrateur système** (ça peut être vous sur votre ordinateur
personnel). L'administrateur système peut également gérer les utilisateurs
en les affectant à des groupes auxquels il pourra donner des **droits de
lecture, d'écriture et/ou d'exécution**.

Dans les systèmes POSIX, le système de fichier est structuré en
**arborescence** : des **fichiers** sont inclus dans des **dossiers**, eux-mêmes
rangés dans des dossiers et ceux jusqu'à avoir un dossier unique (le
**répertoire racine** noté « / »). Un chemin commençant par « / » est un
**chemin absolu**, sinon on parle de **chemin relatif** (sous entendu par
rapport au répertoire courant, c'est-à-dire celui dans lequel vous vous
trouvez).

### Le système GNU/linux

Les ordinateurs de Scholae fonctionnent grâce au système d'exploitation
**GNU/Linux**. Il existe aujourd'hui de très nombreuses variations autour du
noyau Linux que l'on appelle **distribution** (cf. cet [arbre des
distributions :fab fa-wikipedia-w:](https://upload.wikimedia.org/wikipedia/commons/1/1b/Linux_Distribution_Timeline.svg?uselang=fr)).
Pour choisir une distribution, le site
[Distrowatch](https://distrowatch.com/dwres.php?resource=major) est une
référence.

?> À l'aide du site [top500](https://www.top500.org/statistics/treemaps/) qui recense les 500 plus gros ordinateurs au monde, trouver les 5 pays
qui en hébergent le plus grand nombre et indiquer les 3 systèmes d'Exploitation les plus utilisés par ces ordinateurs.

En 1983, Richard Stallman initie le **projet GNU** [:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Projet_GNU) (pour Gnu is Not Unix)
avec l'objectif de créer un système d'exploitation libre pour concurrencer Microsoft. Il est également l'inventeur de la notion de
**copyleft**[:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Copyleft) et de **logiciel libre** [:fab fa-wikipedia-w:](https://fr.wikipedia.org/wiki/Logiciel_libre) :

- **Liberté** parce que les programmes libres respectent la liberté des utilisateurs,
- **Égalité**, parce qu'à travers un programme libre, personne n'a du pouvoir sur personne,
- **Fraternité** parce que nous encourageons la coopération entre les utilisateurs.

?> Rechercher sur internet le sens des commandes suivantes dans un terminal Linux. Puis tester ces commandes dans votre terminal et expliquer ce que fait chaque ligne :

```bash
pwd
man pwd
mkdir "dossier_en_plus",
cd dossier_en_plus/
touch "nouveau_fichier.txt"
ls -la
cp nouveau_fichier.txt ../nouveau_fichier.txt
cd ..
find -name "nouveau_fichier.txt"
find -name "svg" 
```

?> S'entraîner à utiliser **Linux** en ligne de commande grâce à [Pixees.fr](https://pixees.fr/informatiquelycee/n_site/nsi_prem_cmd_base_linux.html). Vous ferez en particulier la section « Gestion des utilisateurs et des groupes ».
