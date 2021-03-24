# ARCHITECTURE MATERIEL, OS ET RÉSEAUX <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>
!> !! Work in progress !!

![Understanding computer technology](../_img/understanding_computer.jpg ':size=70%')

---
<p class="center-p"> 

**Understanding computer technology**. 
*Sources : Première [version](http://usuarios.arnet.com.ar/ngiunta/pages/EQUIPAMIENTO.htm) en italien, deuxième [version](https://www.owensworld.com/funny-pictures/computers-web/computer-technology) (en anglais). Sources retrouvées grâce à [tineye](https://tineye.com/) qui permet la recherche inversée de photo.* 

</p>


!> Réviser le [programme de premiere](../premiere/archi_OS.md). 


## Circuits intégrés


### Les ordinateurs « classiques »

Le processeur (**CPU** pour *Central Processing Unit*) d'un ordinateur s'occupe des calculs principaux, par exemple pour faire tourner le système d'exploitation et les logiciels. Sa rapidité dépend principalement de sa fréquence (nombre d'instructions traitées à la seconde) et de son nombre de cœur (plusieurs cœurs permettent des calculs en parallèle).

Le processeur graphique (**GPU** pour *Graphical Processing Unit*) assure les calculs pour l'affichages des images. La **carte-mère** relie entre eux tous les composants. Mais ce système classique d'organisation des PC n'est pas le seul. Il coexiste avec :
- **les microcontrôleurs** (très faible puissance de calcul), que l'on utilise tout les jours dans notre électroménager et les transports, 
- **les systèmes sur puces** (aussi appelés nano-ordinateurs) qui sont essentiels au fonctionnement de nos téléphones.


### Microcontrôleur


<div class="img-flow" style="max-width:150px;">

<img src="premiere/../_img/Raspberry-Pi-Pico-and-penny-800x533.jpg" alt="Raspberry pico">

**Microcontrôleur** Raspberry pico. [Source](https://www.raspberrypi.org/blog/raspberry-pi-pico-what-did-you-think/) 

</div>

La miniaturisation des circuits intégrées a permit l'avènement des microcontrôleurs. Les microcontrôleurs sont des circuits intégrés regroupant sur quelques $cm^2$ un microprocesseur peu puissant, de la mémoire, des ports d'entrées-sorties, des périphériques et des bus de communication. Les microcontrôleurs ont des capacités de calcul et de mémoire très faibles. En revanche, son coût et sa consommation d'energie sont très faibles. On les utilise dans des systèmes informatiques embarqués (voiture, avion, lave linge, montre connectée...). 


<div class="img-flow-l" style="max-width:170px;">

<p><a href="https://commons.wikimedia.org/wiki/File:Architecture_Harvard.png#/media/File:Architecture_Harvard.png"><img src="https://upload.wikimedia.org/wikipedia/commons/6/69/Architecture_Harvard.png" alt="Architecture Harvard.png"></a> <strong>Architecture de Harvard.</strong> <a href="https://creativecommons.org/licenses/by-sa/1.0" title="Creative Commons Attribution-Share Alike 1.0">CC BY-SA 1.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=19215968"><i class="fab fa-wikipedia-w"></i></a></p>

</div>

Les microcontrôleurs reposent souvent sur l'**architecture de Harvard** (car inventé à l'université d'Harvard). Dans cette architecture, la mémoire des programmes est dissocié physiquement de la mémoire des données. L'Unité Arithmétique et Logique (UAL) communique avec les deux types de mémoire grâce à deux bus distinct. Cette architecture peut se montrer plus rapide que l'architecture de von Neumann (voir [cours première](../premiere/archi_OS.md)) au prix d'une complexité accrue de la structure.




### Système sur puce (SoC)

Dans un ordinateur de bureau ou dans des serveurs, le processeur (CPU) ainsi que les différentes **cartes** (carte son, carte graphique (GPU), carte réseau) et les **mémoires** (vives et statiques) sont interconnectés à l'aide d'un **bus** et branchées sur la **carte mère**. 


<div class="img-flow" style="max-width:300px;">
<p><a href="https://commons.wikimedia.org/wiki/File:Raspberry_Pi_3_B%2B_(39906369025).png#/media/File:Raspberry_Pi_3_B+_(39906369025).png"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Raspberry_Pi_3_B%2B_%2839906369025%29.png/1200px-Raspberry_Pi_3_B%2B_%2839906369025%29.png" alt="Raspberry Pi 3 B+ (39906369025).png"></a> <strong>Systèmes sur puce </strong>: le Raspberry pi 3 B+ <a href="https://creativecommons.org/licenses/by-sa/2.0" title="Creative Commons Attribution-Share Alike 2.0">CC BY-SA 2.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=67384207"><i class="fab fa-wikipedia-w"></i></a></p>
</div>

Les **systèmes sur puce** (abréviation SoC pour *system on a chip*) et un système informatique complet comprenant l'ensemble des composants d'un ordinateur (CPU, cartes, mémoires, capteurs...). Ces SoC sont très économes en energie et miniatures ce qui explique leur présence dans les smartphones, les nano-ordinateurs (par ex. les [Rasperry Pi](https://fr.wikipedia.org/wiki/Raspberry_Pi)) et certaines consoles de jeux. Le CPU des SoC consommant moins d'energie, il chauffe moins et permet donc de s'affranchir de la présence d'un ventilateur.
La distance réduite entre les composant permet également une circulation plus rapide de l'information.

Le principal inconvénient des SoC est l'impossibilité de mettre à jour une partie de la puce. Si on veux améliorer une partie seulement de son matériel (par ex. changer la GPU pour jouer à de nouveaux jeux), il faut changer toute la puce.

| Type                 | microcontrôleur                                                                | SoC                                                                            |
| -------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| Nom                  | Raspberry Pi pico                                                              | Raspberry Pi 3 Model B+                                                        |
| Consommation de base | 8,50 mA ([source](https://datasheets.raspberrypi.org/pico/pico-datasheet.pdf)) | 350 mA ([source](https://www.pidramble.com/wiki/benchmarks/power-consumption)) |
| Mémoire vive         | 264KB                                                                          | 1GB                                                                            |
| Mémoire flash inclus | 2MB                                                                            | aucune (étendable)                                                             |
| Taille               | 21x51mm                                                                        | 56x85mm                                                                        |
| Prix                 | 4                                                                              | 30                                                                             |

----

<p class="center-p"> <strong> Tableau de comparaison d'un microcontrôleur et d'un Soc.</strong> </p>

![raspberry-pi-4](../_img/raspberry-pi-4.png ':size=60%')

---

<p class="center-p"> <strong> Composition du Raspberry pi 4.</strong> <a href="https://creativecommons.org/licenses/by-sa/4.0" title="Creative Commons Attribution-Share Alike 4.0">CC BY-SA 4.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=83463602"><i class="fab fa-wikipedia-w"></i></a></p>

---

## Gestion des processus et des ressources

Un **programme informatique** est une description statique d'une tâche. C'est en quelque sorte une recette de cuisine. Un **processus** est une instance d'une tâche en cours d'exécution, c'est la réalisation de la recette de cuisine. La réalisation (le processus) dépend de la recette (du programme) mais également du cuisinier. Ce cuisinier c'est le système d'exploitation qui le fournit. Un ***thread*** (tâche) est une suite d'instruction au sein d'un processus. On les appelles également *processus léger*. La différence fondamentale entre processus et *thread* est que les processus ne partagent pas leur mémoire alors que les threads d'un même processus peuvent accéder aux variables globales.

### L'ordonnanceur


<div class="img-flow" style="max-width:270px;">
<p class="center-p"><a href="https://commons.wikimedia.org/wiki/File:Diagramme_etat_processus.svg#/media/Fichier:Diagramme_etat_processus.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Diagramme_etat_processus.svg/1200px-Diagramme_etat_processus.svg.png" alt="Diagramme etat processus.svg"></a>Diagramme état-transition suivi par les processus des systèmes d'exploitation modernes. Domaine public, <a href="https://commons.wikimedia.org/w/index.php?curid=9559518"><i class="fab fa-wikipedia-w"></i></a></p>
</div>

Pour gérer les différents processus en cours sur un ordinateur, il faut un « chef d'orchestre » qui va nommer les processus (les tâches), et décider de l'ordre d'exécution. Lors de la création d'un nouveau processus, il sera identifié par un numéro propre (PID), le numéro du processus père (PPID) et par l'identifiant de l'utilisateur qui a lancé ce processus (UID). Chaque processus se verra allouer de la mémoire virtuelle qui stockera le code du programme à exécuter, les variables (globales, et locales sous formes d'une pile) et les bibliothèques si nécessaire. 

Tous les programmes listés précédemment par la commande top semble s'exécuter en même temps. Pourtant on sait que notre ordinateur est limité par le nombre de processeur pour effectuer des calculs. Comment le processeur peux exécuter autant d'instruction en même temps? Cette **exécution concurrente** est rendu possible par les systèmes d'exploitation **multitâches** (tout les OS modernes le sont) qui utilise un **ordonnanceur de processus**.

L'**ordonnanceur** du système d'exploitation va définir les **états** de chaque processus. Les états les plus courants sont :
- Initialisation (processus en cours de création)
- Prêt (= en attente; processus prêt à s'exécuter)
- Exécution (processus en cours d'exécution)
- Bloqué (processus en pause, par ex. quand il attend une réponse de l'utilisateur ou d'un autre processus)
- Terminé

```mermaid
graph LR
    A(Initialisation) --> B(Prêt)
    B ---> |mise en exécution <br> par l'ordonnanceur| C(Exécution)
    C --> |interruption <br> par l'ordonnanceur| D(Suspendu)
    D --> B
    C -->| | E(Terminé)
    D ---> |interruption <br> anormale | E
    B ---> |interruption <br> anormale | E
    classDef default fill:#2e789163,stroke:#2e7891,stroke-width:4px;
```

<p class="center-p"><strong>Schéma des états de processus</strong> les plus courants.</p>

---

En tant normal, l'état des processus variera entre prêt, en attente et en exécution. L'ordonnanceur suspend (très) régulièrement les processus pour allouer de la ressource à d'autres processus. Ainsi, plusieurs tâches s'exécutent les une à la suite des autres, mais tellement rapidement qu'on a l'impression que les processus s'exécutent simultanément. On parle de *pseudo-parallélisme*. Le terme de **calcul parallèle** est reservé au processus qui s'exécute sur deux processeurs différents.

Dans certains cas il existe des situations d'interblocage (*deadlock* en anglais). Cela se produit quand deux processus concurrents s'attendent mutuellement. Par exemple supposons un système possédant les ressources (au sens de ressource informatique) R1 et R2 et avec les processus A et B en cours d'exécution, il y a interblocage dans le cas suivant :
- Le processus A réserve la ressource R1
- Le processus B réserve la ressource R2
- Le processus A demande la ressource R2, et tombe en attente (sans libérer la ressource R1);
- Le processus B demande la ressource R1, et tombe en attente;

Il existe des solutions pour éviter et résoudre ces interblocages qui ne sont pas au programme. Si cela vous intéresse vous pouvez visiter le [site](http://www.uqac.ca/pguerin/8INF341/Cours9_Interblocage.html) de Patrice Guérin de l'UQAC.



### Gestion des processus sous Unix

Sous linux les commandes <a href="https://debian-facile.org/doc:systeme\:ps">ps</a> et <a href="https://debian-facile.org/doc:systeme\:top">top</a>  permettent d'avoir accès aux processus en cours et à leurs caractéristiques.

```bash
ps -aef
top
```

?> **Exercice 1** : sur votre ordinateur, lancer firefox puis trouver le PID et le PPID du processus. Avec la commande *kill*, tuer le processus firefox. Est-il toujours présent dans la liste des processus?





## Protocoles de routage

### Routeurs et topologie

### Protocole RIP

### Protocole OSPF

### Commande UNIX de gestion des protocoles

- ip route
- ping
- traceroute

## Sécurisation des communications

### Cryptographie symétrique

### Cryptographie asymétrique

### Authentification des participants

### Protocole HTTPS