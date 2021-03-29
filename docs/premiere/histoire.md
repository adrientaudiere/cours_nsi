# :fa fa-monument: HISTOIRE DE L'INFORMATIQUE <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

## Le développement des machines 


Dès l'antiquité, l'homme a conçu des machines pour l'aider à calculer
comme le boulier ou les abaques. Pourtant, ces machines sont basées sur
des algorithmes que l'homme doit apprendre et exécuter comme c'est le
cas lorsqu'il réalise une division euclidienne. A partir du 17 ème
siècle, on va chercher à créer des machines qui pourront exécuter
automatiquement des algorithmes.

### :fa fa-cogs: Les machines mécaniques


En 1642, **Blaise Pascal** (1623 – 1662) invente une première
calculatrice mécanique, la **Pascaline**, fonctionnant avec des roues
dentées d'horlogerie. Elle permet d'effectuer des additions et des
soustractions de nombre à 6 chiffres en faisant tourner des cadrans en
forme d'étoiles à dix branches. Sur certains modèles, le résultat peut
être conservé en « mémoire » et l'opérateur peut ainsi réaliser des
multiplications ou des divisions en effectuant des additions ou des
soustractions en cascade.

<div class="img-flow" style="max-width:400px;">
<a href="https://commons.wikimedia.org/wiki/File:Arts_et_Metiers_Pascaline_dsc03869.jpg#/media/Fichier:Arts_et_Metiers_Pascaline_dsc03869.jpg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/80/Arts_et_Metiers_Pascaline_dsc03869.jpg/1200px-Arts_et_Metiers_Pascaline_dsc03869.jpg" alt="Arts et Metiers Pascaline dsc03869.jpg"></a> <strong>Une pascaline</strong>, signée par Pascal en 1652, visible au musée des arts et métiers du Conservatoire national des arts et métiers à Paris. <a href="http://creativecommons.org/licenses/by-sa/3.0/" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=186079"><i class="fab fa-wikipedia-w"></i></a>
</div>

En 1671, **Gottfried Wilhelm Leibniz** (1646 – 1716) améliore la
machine de pascal pour qu'elle effectue les multiplications de façon
automatique en y ajoutant des cylindres cannelés dont les cannelures
sont de longueurs inégales. Couplées à une roue dentée, les cannelures,
selon leur longueur, pourront ou non faire tourner la roue. A partir de
1679, il développera également le **calcul binaire** qui d'après lui
devrait largement simplifier le fonctionnement de machines logiques\...
De nombreuses autres machines à calculer sont développées pour étendre
les capacités de calcul mais la prochaine révolution viendra de
l'industrie textile avec les premières tentatives d'automatisation des
métiers à tisser.

<div class="img-flow" style="max-width:220px;">
<img src="premiere/../_img/metier_tisser.JPG" alt="Métier à tisser">
<p class="center-p"> 
Métier à tisser Jacquart. <br> <a href="https://creativecommons.org/licenses/by/3.0/?ref=ccsearch&amp;atype=html" target="_blank" rel="noopener">CC BY 3.0</a>, <a href="https://commons.wikimedia.org/wiki/File:Wooden_Jacquard_loom_MOSI-11_5544.JPG" target="_blank" rel="noopener"><i class="fab fa-wikipedia-w"></i></a> 
</p>
</div>

En 1725, Basile Bouchon (? - ?) invente le premier système de
programmation d'un métier à tisser en utilisant un ruban perforé qui
contrôle le passage des aiguilles dans le tissu. En 1728, son assistant
Jean- Baptiste Falcon (? - ?) améliore son système en utilisant des
cartes perforées rigides reliées entre elles. En 1745,** Jacques de
Vaucanson** (1709 – 1782) remplace les cartes perforées par un cylindre
percé de trous (l'idée sera reprise pour la fabrication des boites à
musique). Ces machines ont toutes le défaut d'être conçues pour ne
réaliser qu'un seul programme. C'est en 1801 que **Joseph-Marie
Jacquard** (1752 – 1834) a l'idée de monter les cartes perforées de
Falcon sur le cylindre de Vaucanson (qui devient alors carré\...) et
invente ainsi **la première machine programmable** (l'idée sera reprise
pour mettre au point les orgues de barbarie).

<div class="img-flow-l" style="max-width:200px;">
<img src="premiere/../_img/music-box.jpg" alt="Boite à musique">
<p class="center-p"> 
Boîte à musique.<br> <a href="https://creativecommons.org/licenses/by-sa/2.0/?ref=ccsearch&amp;atype=html" target="_blank" rel="noopener">CC BY-SA 2.0</a>, <a href="https://www.flickr.com/photos/36692623@N06/5303387162" target="_blank" rel="noopener"><i class="fab fa-flickr"></i></a> 
</p>
</div>


A partir de 1834, le mathématicien **Charles Babbage** (1791 – 1871) a
l'idée de réutiliser les cartes perforées d'un métier Jacquard pour
envoyer des instructions et des données dans une machine à calculer qui
peut soit conserver des résultats en mémoire soit les afficher. En 1843,
sa collaboratrice **Ada Lovelace** (1815-1852) va alors développer un
algorithme permettant de calculer les nombres de Bernoulli sur la
machine analytique de Babbage, c'est le premier programme informatique.
A partir de 1844, **George Boole** (1815 – 1864) développe une nouvelle
théorie mathématique basé sur un algèbre binaire afin de traduire des
concepts logiques en équations. Ada Lovelace propose alors que l'on peut
utiliser cet algèbre pour faire des opérations autres que numériques sur
la machine de Babbage. Faute de financement, ces travaux n'aboutiront
pas.


![Canard de Vaucanson](../_img/canard.jpg ':size=50%')

---

<p class="center-p"> 

 **Canard de Vaucanson** : cet automate, exposé en 1744 au Palais-Royal, qui peut manger et digérer, cancaner et simuler la nage. Il s'agit ici d'une reconstitution publié dans *Scientific American* en 1899. Domaine public, [:fab fa-wikipedia-w:](https://commons.wikimedia.org/w/index.php?curid=1493624) 

</p>

### :fa fa-magnet: Les machines électromécaniques

A partir de 1880, **Hermann Hollerith** (1860 – 1929) travaille pour le
bureau du recensement américain. A cette époque, le recensement est
manuel et le traitement de toutes les données va durer 9 ans. Hollerith
va alors chercher à développer en solitaire une machine permettant de
traiter ces données statistiques de façon automatisée. Il reprend le
système des cartes perforées et l'améliore pour implémenter des
compteurs grâce un signal électrique. En effet, les cartes perforées
sont lues dans une presse dans la partie mobile est constituée de
pointes métalliques correspondant aux différentes catégories à analyser
et la partie fixe est constituée d'un bac rempli de mercure. A chaque
trou, un contact électrique a lieu entre les pointes et le mercure et un
compteur correspondant à la catégorie voulue est implémenté. Il va
également développer une trieuse permettant de ranger les cartes
perforées par catégories : il s'agit d'un meuble à tiroir dont
l'ouverture est pilotée par la machine de traitement (**Machine de
classement de Hollerith**). En 1887, il dépose le brevet de ses machines
qui seront utilisées pour le recensement de 1890 qui durera seulement 6
semaines. L'utilisation des cartes perforées permettra ensuite de
nombreuses statistiques sur la population américaine.


<div class="img-flow" style="max-width:360px;">
<a href="https://commons.wikimedia.org/wiki/File:Hollerith_census_machine_at_CHM_by_Tomwsulcer.jpg#/media/File:Hollerith_census_machine_at_CHM_by_Tomwsulcer.jpg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/Hollerith_census_machine_at_CHM_by_Tomwsulcer.jpg/1200px-Hollerith_census_machine_at_CHM_by_Tomwsulcer.jpg" alt="Hollerith census machine at CHM by Tomwsulcer.jpg"></a>
<p class="center-p"><strong>Réplique de la machine d'Hollerith</strong> <a href="http://creativecommons.org/publicdomain/zero/1.0/deed.en" title="Creative Commons Zero, Public Domain Dedication">CC0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=46063689"><i class="fab fa-wikipedia-w"></i></a>
</p>
</div>

En 1896, suite à ce succès, Hermann Hollerith fonde sa propre compagnie,
la Tabulating Machine Corportation, qui deviendra en 1924,
l'International Business Machines Corporation, plus connue sous le nom
de **IBM**. Ces machines vont rapidement être utilisés partout dans le
monde pour de nombreuses applications et seront utilisées jusque dans
les années 1970 avec l'avènement des disques durs magnétiques inventés
par IBM en 1956. Les premiers **codages de caractère** (notamment le
code **ASCII**) et les premiers **langages de programmation** (notamment
le **FORTRAN**) seront développés pour les cartes perforées à 80
colonnes d'IBM. De nombreuses machines de lectures des cartes perforées
utilisaient des amplificateurs de courant à lampe qui chauffaient
beaucoup et attiraient les insectes provoquant ainsi des
courts-circuits : c'était la principale cause de panne, elle prit le nom
de « bug ».

### :fa fa-memory: La naissance des ordinateurs

En 1936, **Alan Turing** (1912 – 1954), doctorant de l'université de
Cambridge, propose un modèle abstrait de fonctionnement d'une machine de
calcul, c'est la **machine universelle de Turing**. Pour voir une animation 
d'une machine de Turing, aller sur le site [Interstices](https://interstices.info/comment-fonctionne-une-machine-de-turing/).
 Cette machine est constituée des 4 éléments suivants :

- Le ruban infini divisé en cases contenant chacune un symbole d'un
alphabet fini,

- Une tête de lecture/écriture pouvant se déplacer vers la gauche ou la
droite du ruban,

- Un registre d'état qui mémorise l'état de la machine de Turing, le
nombre d'état étant fini,

- Une table d'action qui, en fonction du symbole lu sur le ruban et de
l'état de la machine, indique le symbole à écrire sur le ruban, le sens
de déplacement de la tête de lecture/écriture et le nouvel état de la
machine.

A partir de 1936, **Konrad Zuse** (1910 – 1995), ingénieur à
l'université de Berlin, commence à développer un calculateur binaire à
virgule flottante programmable entièrement mécanique mais ne parvient
pas à la faire fonctionner. En 1937, **Claude Shannon** (1916 – 2001),
doctorant au MIT, propose un modèle de machine à relais
électromécaniques dans laquelle il utilise l'algèbre de Boole pour
décrire l'état des relais (0 : ouvert, 1 : fermé). En 1938, Helmut
Schreyer (1912 – 1984), doctorant à l'université de Berlin, propose
d'utiliser des tubes électroniques pour effectuer les opérations
booléennes (0 : déchargé, 1 : chargé) mais cette solution ne sera pas
retenue par le gouvernement allemand qui la considère « non
indispensable à l'effort de guerre ». Zuse reprend alors l'idée de
Shannon et il faut attendre 1941 et la troisième version de son
**calculateur**, nommé **Z3**, pour avoir une machine opérationnelle
respectant les principes de la machine de Turing. Il sera utilisé pour
des calculs de vibrations des ailes par l'institut de recherche
aéronautique allemand et détruite en 1943 lors d'un bombardement allié.


<div class="img-flow" style="max-width:320px;">
<a href="https://commons.wikimedia.org/wiki/File:Z3_Deutsches_Museum.JPG#/media/Fichier:Z3_Deutsches_Museum.JPG"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Z3_Deutsches_Museum.JPG/1200px-Z3_Deutsches_Museum.JPG" alt="Z3 Deutsches Museum.JPG"></a>
<p class="center-p"><strong>Réplique du Zuse 3.</strong> (<em>Deutsches Museum</em> de Munich). <a href="http://creativecommons.org/licenses/by-sa/3.0/" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=3632073"><i class="fab fa-wikipedia-w"></i></a>
</p>
</div>

A partir de 1937, **Howard Aiken** (1900 – 1973), chercheur à
l'université d'Harvard, développe une machine de calcul décimal
programmable en collaboration avec IBM, le **ASCC-Harvard Mark 1**. Pour
des raisons financières, il utilise des relais électromécaniques et des
composants déjà utilisé par IBM. Il mesure 16 m de longueur et pèse
4 500 kg. La machine sera opérationnelle en 1943 et servira à des
applications militaires. En 1938, Alan Turing entre dans les services de
renseignements britanniques ou il va développer des méthodes de
décryptage des messages codées allemands. Des calculateurs
électromécaniques, baptisées **Bombes de Turing**, sont construit à cet
effet. Sur la base de ces travaux, Max Newman (1897 - 1984) et Thomas
Flowers (1905 - 1998) développe un autre calculateur, nommé
**Colossus**, fonctionnant avec des tubes électroniques sera construit
en 1943 pour décrypter les codes les plus difficiles. Ces travaux ont
été classés secret-défense et les machines sont détruites après-guerre.
**Turing** et **Newman** continueront à participer à des projets de
calculateurs notamment avec les universités de Manchester et de
Cambridge mais ne pourront jamais utiliser leurs connaissances issues du
programme Colossus.

A partir 1943, au sein du département américain de la Défense, John
**Eckert** (1919 – 1995) et John **Mauchly** (1907 – 1980) commence à
développer le calculateur électronique appelé **ENIAC** (Electronic
Numerical Integrator and Computer) basé sur l'utilisation de tubes
électroniques. Les données sont toujours lues sur des cartes perforées
mais le programme est câblé sur un panneau de connexion externe.
Mesurant plus de 30 m de longueur et pesant 30 tonnes, ENIAC sera
opérationnel en 1946 et sera également utilisé pour des applications
militaires.

Dès 1944, conscients de la difficulté à câbler le programme sur le
tableau de connexion, Eckert et Mauchly démarrent un autre projet nommé
**EDVAC** (Electronic Discrete Variable Automatic Computer) en
collaboration avec John von Neumann (1903-1957) qui rédige, en 1945, le
« Premier rapport sur la conception d'EDVAC ». Le modèle d'architecture
proposé, appelé couramment **architecture de Von Neumann**, est novateur
et est toujours utilisé aujourd'hui. La première innovation est la
**séparation entre l'unité de commande**, qui organise le flot de
séquencement des instructions, **et l'unité arithmétique**, chargée de
l'exécution de ces instructions. La seconde innovation, la plus
fondamentale, est l'idée du **programme enregistré :** les instructions
au lieu d'être codées sur un support externe (cartes perforées, tableau
de connexion), sont enregistrées dans une mémoire interne selon un
codage conventionnel. Un compteur contient l'**adresse de
l'instruction** en cours d'exécution et est automatiquement incrémenté
après exécution de l'instruction. Un **emplacement de mémoire** peut
contenir indifféremment des instructions et des données, et une
conséquence majeure est qu'**un programme peut être traité comme une
donnée** par un autre programme.

<div class="img-flow" style="max-width:320px;">
<a href="https://commons.wikimedia.org/wiki/File:Manchester_baby_head_on.JPG#/media/File:Manchester_baby_head_on.JPG"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Manchester_baby_head_on.JPG/1200px-Manchester_baby_head_on.JPG" alt="Manchester baby head on.JPG"></a>
<p class="center-p"><strong>Réplique du SSEM (<em>the Baby</em>).</strong> <a href="https://creativecommons.org/licenses/by-sa/4.0" title="Creative Commons Attribution-Share Alike 4.0">CC BY-SA 4.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=25760994"><i class="fab fa-wikipedia-w"></i></a>
</p>
</div>



Suite aux départs d'Eckert, de Mauchly et de Von Neumann, le projet
EDVAC n'aboutit qu'en 1951 alors que d'autres machines basées sur
l'architecture de Von Neumann avaient déjà été réalisées. Il est cinq
fois moins grand que l'ENIAC et ne pèse que 8 tonnes. Il sera utilisé
pendant 10 ans pour des applications militaires. En 1946, sous la
direction de Max Newman, Frederic Williams (1911 – 1977) et Thomas
Kilburn (1921 – 2001), de l'université de Manchester, développèrent une
mémoire utilisant l'écran dans tube cathodique pour le stockage de bits,
nommée « tube williams » qu'ils expérimentèrent sur un mini-calculateur
nommé SSEM et surnommé « The baby ». En 1949, ils construisirent ensuite un second calculateur,
**Manchester Mark 1**, en y ajoutant une mémoire secondaire à tambour
magnétique. Cette machine fut la première à être commercialisée à partir
de 1951 par la compagnie Ferranti.

En 1946, **Maurice Wilkes** (1913 – 2010), de l'université de
Cambridge, lança également un projet de calculateur à programme
enregistré nommé EDSAC (Electronic Delay Storage Automatic Calculator)
qui fonctionna à partir de 1949 et fut le premier à pouvoir utiliser des
sous-programmes.

### :fa fa-microchip: La révolution électronique : du transistor au microprocesseur

En 1947, **John Bardeen**(1908 – 1991), **William Shockley** (1910 – 1989)
et **Walter Brattain **(1902 – 1987), chercheurs pour les
laboratoires Bell, inventent le **transistor**. En 1956, ils reçoivent
le prix Nobel de physique pour cette invention. Il s'agit d'un
**composant semi-conducteur** à trois électrodes qui permet de faire
circuler le courant d'une électrode d'entrée (source) vers une électrode
de sortie (drain) en commandant la troisième électrode (grille). Si la
grille est alimentée, le courant passe de la source au drain ; si la
grille n'est pas alimentée, le courant ne passe pas.


<div class="img-flow" style="max-width:280px;">
<a href="https://commons.wikimedia.org/wiki/File:Intel_C4004_b.jpg#/media/File:Intel_C4004_b.jpg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Intel_C4004_b.jpg/1200px-Intel_C4004_b.jpg" alt="Intel C4004 b.jpg"></a>
<p class="center-p"><strong>Processeur Intel C4004.</strong> <a href="https://creativecommons.org/licenses/by-sa/4.0" title="Creative Commons Attribution-Share Alike 4.0">CC BY-SA 4.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=50603727"><i class="fab fa-wikipedia-w"></i></a>
</p>
</div>

En 1958, **Jack Kilby** (1923 – 2005), ingénieur pour Texas instrument,
associe plusieurs transistors ensemble pour effectuer des fonctions
logiques de l'algèbre de Boole. Il miniaturise ses montages et les
intègrent dans des puces en silicium. Il invente ainsi le **circuit
intégré** pour lequel il obtient le prix Nobel de physique en 2000. En
1971, Marcian Hoof (1937 – ) et Federico Faggin (1941 – ), ingénieurs
pour Intel, invente le premier **microprocesseur**, nommé Intel 4004,
contenant 2300 transistors. Il effectue de opérations logiques et
arithmétiques sur 4 bits à une fréquence maximal de 740 kHz. Ce
microprocesseur est le premier circuit à intégrer en une seule puce
toutes les fonctions de l'architecture de Von Neumann.

En 1972, **François Gernelle** (1944 – ) met au point le **Micral**, le
premier ordinateur personnel (en anglais : personal computer, PC) à
partir d'un microprocesseur Intel 8008. Par la suite, c'est l'**Altair
8800** équipé d'un microprocesseur Intel 8080 et commercialisé en 1975
qui lancera l'industrie informatique. En effet, **Bill Gates** (1955 - )
et **Paul Allen** (1953 – 2018), les fondateurs de Microsoft, ainsi que
**Steve Jobs** (1955 – 2011) et **Steve Wozniak** (1950 - ), les
fondateurs d'Apple, vont entrer dans l'histoire de l'informatique grâce
à cette machine : les premiers en développant le premier interpréteur
permettant de programmer sur cette machine, les seconds en la copiant
pour commercialiser leur propre machine, l'Apple 1.

### :fa fa-sitemap: Architecture de Von Neumann

L'architecture de Von Neumann d'un ordinateur se résume par le schéma
suivant : **L'unité arithmétique et logique UAL** (en anglais ALU :
Arithmetical and Logical Unit) effectue les opérations arithmétique
(incrémentation, décrémentation, addition, soustraction, propagation de
la retenue\...) et logiques (ET, OU, NON, NOR, NAND, XOR). Elle est
intègre souvent une unité de calcul en virgule flottante (en anglais
FPU : floating-point unit) afin d'accélérer les calculs sur les nombres
réels. L'UAL contient plusieurs **registres** (petites mémoires d'accès
rapides) dont les principaux sont **l'accumulateur** qui sert à stocker
les données traitées par l'UAL et **le registre d'état** servant à
stocker les résultats de la dernière instruction traitée. L'unité de
contrôle ou **séquenceur** (en anglais : Control Unit) gère le
séquencement des instructions au rythme d'une horloge. Il gère l'envoi
des instructions à l'UAL. Elle contient également des registres dont les
principaux sont le **registre d'instruction** qui stocke l'instruction
en cours d'exécution et le **compteur ordinal** qui stocke l'adresse de
l'instruction suivante. **La mémoire** contient à la fois les données et
le programme qui indique à l'unité de contrôle les instructions à
effectuer. Elle se divise entre **mémoire volatile** pour les programmes
et données en cours de fonctionnement (registres du processeur, mémoire
cache, mémoire vive RAM) et **mémoire permanente** pour les programmes
et données de base de la machine (disque dur, mémoire morte ROM). La
mémoire volatile est beaucoup plus rapide que la mémoire permanente,
c'est pourquoi la mémoire vive sert de stockage temporaire des données
que le disque dur doit transférer au processeur. L'**unité de gestion
des bus** (ou unité entrées-sorties) gère les flux d'informations
entrant et sortant.

Un **microprocesseur** est un circuit intégré qui contient toutes les
composantes de l'architecture de Von Neumann. Il contient en effet une
mémoire cache permettant d'accélérer le traitement en limitant l'accès à
la mémoire vive. Le cache d'instructions reçoit les prochaines
instructions à exécuter et le cache de données manipule les données.

![Architecture de Von Neumann](/../_img/Von_Neumann_architecture_fr.svg ':size=60%')

<p class="center-p"> <strong>Architecture de Von Neumann </strong> : l'unité de contrôle et l'UAL forment l'<strong>unité centrale</strong> aussi appelé <strong>processeur</strong>. <p>

?> **Activité** : Faire une frise chronologique de l'histoire de l'informatique en illustrant avec des photos (des personnages et de machines) trouvées sur internet. Vous pouvez utiliser le site [frisechronos.fr/](https://frisechronos.fr/).



