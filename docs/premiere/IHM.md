# Interfaces homme-machine <span onclick="window.print()" class="pdf-link"> :fa fa-file-pdf:</span>

## Introduction : le Web (:fa fa-spider:) utilise Internet (:fa fa-network-wired:)

### Le web : un ensemble de documents reliés par des liens hypertextes

Le "**World Wide Web**" (en anglais la toile d'araignée), plus
communément appelé "Web" a été développé au CERN (Conseil Européen
pour la Recherche Nucléaire) par le Timothy John Berners-Lee et Robert
Cailliau au début des années 90. La première page web est toujours
consultable [ici](http://info.cern.ch/hypertext/WWW/TheProject.html).
Pour plus d'information historique voir cette [figure
interactive](http://www.evolutionoftheweb.com/?hl=fr) et ces [15 dates
importantes](https://www.01net.com/actualites/les-15-dates-qui-ont-fait-le-web-615826.html).

Le **Web** est un système **hypertexte** public fonctionnant sur
Internet. Il permet de consulter, avec un logiciel client, appelé
**navigateur**, des **pages** accessibles sur des **sites**. Les liens
hypertextes, ou **hyperliens**, sont des textes augmentés de renvois
automatiques qui permettent de lier les pages Web entre elles. En
cliquant sur un lien, on peut ouvrir une autre page du même site ou d'un
autre site. Le système hypertexte permet, à partir d'un document, de
consulter d'autres documents en cliquant sur des mots clés.

Le contenu des pages Web est édité en langage **HTML** (HyperText Markup
Language) et mis en forme en langage **CSS** (Cascading Style Sheet). Le
web utilise le protocole de communication client-serveur nommé **HTTP**,
**HyperText Transfer Protocol** (ou **HTTPS** pour sa version
sécurisée). Enfin, les **URL** (Uniform Resource Locator) permet de
d'identifier les localisations, c'est-à-dire les les adresses des
ressources que l'on cherche.

Une chose très importante à bien avoir à l'esprit : beaucoup de
personnes confondent "**web**" et "**internet**". Le web utilise le
réseau Internet puisque HTTP est un des nombreux protocoles de la couche
d'application s'exécutant au dessus des protocoles TCP et IP. Comme
nous venons de le voir, le web est la combinaison de trois technologies
: **HTTP** (protocole de communication), **URL** (emplacement d'une
ressource) et **HTML + CSS** (édition et mise en page). D'ailleurs on
trouve autre chose que le "web" sur internet, par exemple, les emails
avec le protocole SMTP (Simple Mail Transfert Protocol) et les
transferts de fichiers avec le protocole FTP (File Transfert Protocol).

?> Aller sur le site [internet live stats](https://www.internetlivestats.com/one-second/) et trouver le nombre de recherches google effectués et d'emails envoyés en 30 secondes.

### Internet : un protocole pour communiquer dans un réseau informatique globale

Dès les années cinquante, les ordinateurs ont été mis en réseau pour
échanger des informations, mais de façon très liée aux constructeurs
d'ordinateurs ou aux opérateurs téléphoniques. Les réseaux généraux
indépendants des constructeurs sont nés aux États-Unis avec le projet
militaire ArpaNet (1970) et en France avec Cyclades (1971). Le
projet ArpaNet a rapidement évolué pour devenir la paire de protocole
TCP-IP (1974).

Schématiquement, le modèle internet est un langage de communication qui
est structuré en quatre couches :

- Une couche **application** qui contient les logiciels réseaux
  (protocole **HTTP** pour le web, FTP pour le transfert de fichiers ou
  encore SMTP pour les mails),

- Une couche **transport** basée le plus souvent sur le protocole
  **TCP** (_Transmission Control Protocol_). Le protocole UPD (User
  Datagram Protocol) est plus simple mais est sensible à certaines erreurs
  de transmission.

- Une couche **réseau** basée le plus souvent sur le protocole **IP**
  (_Internet Protocol_). Elle permet d'acheminer les données au bon
  destinataire dans le réseau, en laissant aux couches supérieures le soin
  de les réordonner (TCP) et de les interpréter (Application)

- Une couche **physique** qui concrétise le transport de données
  (câbles, Wi-Fi ).

#### IP (Internet Protocol)

<!--
<div class="img-flow" style="max-width:320px;">
<img src="premiere/../_img/ip_seb_sauvage.png" alt="protocole IP">
<p class="center-p"> <strong>Protocole IP</strong>, par
<a href="https://sebsauvage.net/comprendre/tcpip/index.html" target="_blank" rel="noopener" rel="noopener">Seb Sauvage</i></a>
</p>
</div> -->

Dans le modèle Internet, le protocole **IP** rajoute à chaque petit paquet de données (votre message) différentes informations :

- l'adresse de l'expéditeur (votre adresse IP),
- l'adresse IP du destinataire,
- différentes données supplémentaires de contrôle

L'adresse IP est une adresse unique attribuée à chaque ordinateur sur
Internet (c'est-à-dire qu'il n'existe pas sur Internet deux
ordinateurs ayant la même adresse IP). Tout comme avec l'adresse
postale, il faut connaître au préalable l'adresse IP de l'ordinateur
avec lequel vous voulez communiquer. L'adresse IP se présente le plus
souvent sous forme de 4 nombres (entre 0 et 255) séparés par des points.
Par exemple: 2.4.158.190

#### TCP (Transmission Control Protocol)

**TCP** est un protocole fiable, qui permet l'acheminement sans erreur de
données issues d'une machine à une autre machine. Son rôle est de
fragmenter le message à transmettre de manière à pouvoir le faire passer
sur la couche internet. A l'inverse, sur la machine destination, TCP
replace dans l'ordre les fragments transmis sur la couche internet pour
reconstruire le message initial.

<!-- <img src="premiere/../_img/tcp_seb_sauvage.png" alt="protocole TCP">

---

<p class="center-p"> <strong>Protocole TCP</strong>, par <a href="https://sebsauvage.net/comprendre/tcpip/index.html" target="_blank" rel="noopener" rel="noopener">Seb Sauvage</i></a> </p>

---  -->

## :fa fa-cubes: Les composants du WEB

### URL

Une URL (Uniform Resource Locator) est une chaîne de caractères
décrivant l'emplacement d'une ressource. Elle contient dans l'ordre :

$$\textcolor{red}{Nom\_du\_protocole}://\textcolor{blue}{nom.de.domaine}/\textcolor{purple}{chemin\_vers\_la/page}$$

<div class="img-flow-l" style="max-width:280px;">

<a href="https://commons.wikimedia.org/wiki/File:PageRank-hi-res.png#/media/Fichier:PageRank-hi-res.png"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/PageRank-hi-res.png/1200px-PageRank-hi-res.png" alt="PageRank-hi-res.png"></a> Illustration du PageRank. <a href="https://creativecommons.org/licenses/by-sa/2.5" title="Creative Commons Attribution-Share Alike 2.5">CC BY-SA 2.5</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=2776582"><i class="fab fa-wikipedia-w"></i></a>

</div>

Les **moteurs de recherche** sont des applications qui explorent le web
à l'aide de robots, appelés _spiders_ ou _crawlers_. Suite à cette
exploration, les pages sont **indexées**, de la même façon que des
livres sont numérotés dans une bibliothèque. Lors d'une recherche
effectuée par le client, le résultat de la requête présentera les pages
indexées selon un ordre de pertinence défini par un algorithme. Le plus
connu de ces algorithmes est le **PageRank** de Google qui mesure
quantitativement la popularité d'une page web et attribue un score à
chaque page.

Ce score est proportionnel au nombre de fois qu'un utilisateur cliquant
aléatoirement sur les liens arriverait sur cette page. Le PageRank est
donc d'autant plus élevé qu'une page a des liens qui pointent vers elles
et que ces pages ont des PageRank élevés. Ce schéma s'appelle un graphe
et permet une représentation simple d'un réseau comportant un système de
liens complexes.

À la suite d'une URL, il peux y avoir une liste de paramètres de
requêtes indiquée après un "?" :

$$ \textcolor{red}{Nom_du_protocole}://\textcolor{blue}{nom.de.domaine}/\textcolor{purple}{chemin_vers_la/page}\Large{?}\normalsize{\textcolor{green}{nom=Saquet\&age=30}} $$

Il s'agit des paramètres d'une requête **GET** (voire partie sur le protocole HTTP).

?> Aller sur la page wikipedia suivante : <https://fr.wikipedia.org/w/index.php?search=bilbo>. Sur quelle page se retrouve t'on. Avec la même méthode faire une recherche directe du mot clé "_informatique_".

### HTML :fab fa-html5: (le fond) & CSS :fab fa-css3-alt: (la forme)

HTML n'est pas un langage de programmation (contrairement à python,
JavaScript et PHP par ex.). En effet, ce langage ne permet aucun calcul,
test, ou boucle. HTML et CSS sont des langages interprétés par un
navigateur (par ex. Firefox). Les versions utilisées aujourd'hui sont
[HTML5](https://developer.mozilla.org/fr/docs/Web/Guide/HTML/HTML5) :fab fa-html5: et
CSS3 :fab fa-css3-alt:.

### HTML : un langage balisé

Le langage HTML est un langage à **balises**. Les balises sont des mots
clés insérés entre \< et \>. Une balise s'ouvre sous la forme \<\...\>
(par ex. \<img\>), et se ferme sous la forme \</\...\> (par ex.
\</img\>). On peut enchâsser des balises les unes à l'intérieur des
autres, en respectant l'ordre de fermeture inverse de l'ordre
d'ouverture ; a contrario \<balise1\> \<balise2\> \</balise1\>
\</balise2\> est incorrect.

La balise \<html\> délimite le code. La balise \<head\> sert à définir
l'en-tête de la page et la balise \<body\> à insérer son contenu. La
balise \<title\> placée dans l'en-tête permet de donner un titre à la
page. Pour respecter les standards DOM, un document HTML doit être
organisé de la façon suivante :

```html
<! DOCTYPE html>
<html>
  <head>
    <!-- commentaire : en tête du document -->
    <meta charset="utf-8" />
    <!---définition du codage des caractères -->
    <title> </title>
    <!-- titre de la page -->
  </head>

  <body>
    <!-- corps de la page -->
    ...
  </body>
</html>
```

La balise utilisée pour le codage des caractères est d'un type
particulier, elle s'ouvre et se ferme toute seule sous la forme : \<meta \... /\>.
Voici une liste des balises principales. Vous trouverez plein
d'information complémentaires sur les sites suivants : mémento des
balises sur le site
[openclassroom](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1608357-memento-des-balises-html),
toutes les balises sur le site
[MDN](https://developer.mozilla.org/fr/docs/Apprendre/Commencer_avec_le_web/Les_bases_HTML),
une introduction au base du langage HTML sur le site
[MDN](https://developer.mozilla.org/fr/docs/Apprendre/Commencer_avec_le_web/Les_bases_HTML).

#### Balises de premier niveau

Les balises de premier niveau structurent une page HTML, indispensables pour réaliser le « code minimal » d'une page web (voir exemple ci-dessus).

- Description : **\<html\>**
- En-tête de la page : **\<head\>**
- Corps de la page : **\<body\>**

#### Balises sectionnantes : permettent de construire le squelette de votre site web

<div class="img-flow" style="max-width:320px;">
<p><a href="https://commons.wikimedia.org/wiki/File:Plan_html_5.png#/media/File:Plan_html_5.png"><img src="https://upload.wikimedia.org/wikipedia/commons/b/bd/Plan_html_5.png" alt="Plan html 5.png"></a> Exemple de structure d'une page HTML-5. <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=30209550"><i class="fab fa-wikipedia-w"></i></a></p>
</div>

- **\<header\>** :
- **\<nav\>** : Liens principaux de navigation
- **\<section\>** : Section de page
- **\<article\>** : Article (contenu autonome)
- **\<aside\>** : Informations complémentaires
- **\<footer\>** : Pied de page

#### Balises de structuration du texte

- **\<abbr\>** : Abréviation
- **\<strong\>** : Mise en valeur forte
- **\<em\>** : Mise en valeur normale
- **\<h1\>** : Titre de niveau 1
- **\<h2\>** : Titre de niveau 2
- ...
- **\<h6\>\*\*** : Titre de niveau 6
- **\<img /\>** : Image
- **\<a\>** : Lien hypertexte
- **\<br /\>** : Retour à la ligne
- **\<p\>** : Paragraphe

#### Balises de liste : permettent de créer des listes (à puces, numérotées, listes de définitions...)

- **\<ul\>** : Liste à puces, non numérotée
- **\<ol\>** : Liste numérotée
- **\<li\>** : Élément de la liste à puces
- **\<dl\>** : Liste de définitions
- **\<dt\>** : Terme à définir
- **\<dd\>** : Définition du terme

#### Balises de tableau

- **\<table\>** : Tableau
- **\<caption\>** : Titre du tableau
- **\<tr\>** : Ligne de tableau
- **\<th\>** : Cellule d'en-tête
- **\<td\>** : Cellule
- **\<thead\>** : Section de l'en-tête du tableau
- **\<tbody\>** : Section du corps du tableau
- **\<tfoot\>** : Section du pied du tableau

#### Balises de formulaire

- **\<form\>** : Formulaire
- **\<fieldset\>** : Groupe de champs
- **\<legend\>** : Titre d'un groupe de champs
- **\<label\>** : Libellé d'un champ
- **\<input /\>** : Champ de formulaire (texte, mot de passe, case à cocher, bouton, etc.)
- **\<textarea\>** : Zone de saisie multi-ligne
- **\<select\>** : Liste déroulante
- **\<option\>** : Élément d'une liste déroulante
- **\<optgroup\>** : Groupe d'éléments d'une liste déroulante

#### Balises génériques ou balise universelles

- **\<span\>** : Balise générique de type _inline_
- **\<div\>** : Balise générique de type _block_

Avant d'attaquer la création d'un site, il est indispensable d'élaborer
une maquette sur papier de son site afin de connaître l'ensemble des
boites et de pouvoir créer toutes les balises nécessaires. Il est très
courant d'avoir recours à un graphiste pour cette étape.

?> Créer un compte puis se connecter sur [FreeCodeCamp](https://www.freecodecamp.org/) et faire tous les
exercices de la section « Basic HTML and HTML5 » dans la session _Responsive Web Design Certification_.

### CSS : ajouter une mise en page à notre fond HTML

CSS est un langage qui permet de spécifier la forme du document (par
opposition au contenu donné par html), en précisant les attributs d'une
balise. La bonne pratique consiste à définir les styles dans un document
à part, dont on en précise la localisation dans l'en-tête du document
html : \<link rel="stylesheet" type="text/css" href="style.css"\>.

Les **sélecteurs** CSS comportent une ou plusieurs **propriétés
**auxquelles sont affectées des valeurs.Les sélecteurs peuvent être des
**sélecteurs d'éléments** (par ex. pour modifier tous les paragraphes du
document), de **classe** (précisés dans la balise html par
**class**= "nom_de_classe"), ou d'**identifiant**(précisés dans la
balise html par **id** = "nom_d'identifiant"). Plusieurs éléments
d'une page peuvent être de la même classe, par contre un identifiant est
unique.

_Voici les exemples les plus courants de sélecteurs :_

```css
p {
  /*modifie tous les paragraphes*/
  ...;
}
p,
h1 {
  /*modifie tous les paragraphes et tous les titres h1*/
  ...;
}
p em {
  /*modifie les textes en italique dans les paragraphes*/
  ...;
}
h3 + p {
  /*modifie les paragraphes qui suivent les titres h3*/
  ...;
}
.deux {
  /*modifie les éléments dont l'attribut class='deux'*/
  ...;
}
\#trois {
  /*modifie l'élément dont l'attribut id='trois'*/
  ...;
}
a[title] {
  /*modifie tous les liens qui ont un attribut title*/
  ...;
}
a[href="#section1"] {
  /*modifie l'élément dont l'attribut href='#section1'*/
  ...;
}
a:hover {
  /*modifie les liens lorsque la souris survole le lien*/
  ...;
}
a:visited {
  /*modifie les liens lorsque ils ont été consultés*/
  ...;
}
```

Les **propriétés les plus courantes** sont les suivantes (les parties en italiques sont des commentaires, des descriptifs):

- **background-color** : white, silver, gray, black, red, maroon, lime, green, yellow, olive, blue, navy, fuchsia, purple, teal
- **background-image** : url('image.jpg')
- **background-position** : center, top, left, bottom, right, top, left, top right, bottom left, bottom right
- **border** :_super-propriété_ pouvant regrouper toutes les propriétés des bordures
  - border-width : 1px _(px pour pixel)_
  - border-color : rgb(143,75,246) _(chaque composante entre 0 et 255)_
  - border-style : none, solid, dotted, dashed, double, groove, ridge, inset, outset
  - border-radius : 10px/20px _(arrondi horizontal/vertical)_
- **color** : #FFFFFF *(*couleur du texte, ici du blanc)\*
- **font-family** : _police d'écriture, en mettre plusieurs au cas où_
- **font-size** : xx-small, x-small, small, medium, large, x-large, xx-large _(ou en pixel, ou en multiple de la taille normal, ex : 1.3em)_
- **font-style** : normal, italic, oblique
- **font-weight** : normal, bold
- **margin** : _marges extérieures à la boite en pixel ou auto, centrage automatique_
- **padding** : _marges intérieures à la boite en pixel_

- **height** : _hauteur de la boite_
- **max-height** :_hauteur maximum de la boite_
- **min-height** :_hauteur minimum de la boite_

- **width**: _largeur de la boite en pixel ou en % de la largeur totale_
- **max-width** :_largeur maximum de la boite_
- **min-width** :_largeur minimum de la boite_

- **opacity** :_entre 0 et 1_
- **text-decoration** : none, line-through, overline, underline, blink
- **text-align** : left, center, right, justify
- **text-shadow** : 2px 2px 0px blue

?> Faire l'exercice [Build a Robot](https://projects.raspberrypi.org/en/projects/build-a-robot).

?> Se connecter sur [FreeCodeCamp](https://www.freecodecamp.org/) et faire tous les exercices de la section "Basic CSS".

### HTTP

Le web utilise le protocole de communication client-serveur nommé
**HTTP**, **HyperText Transfer Protocol** (ou **HTTPS** pour sa version
sécurisée). Dans ce protocole, le client va envoyer différents types de
requêtes, appelées méthodes, au serveur pour lui demander d'effectuer
une action. La méthode la plus courante est la requête **GET** pour
récupérer une page web, elle s'écrit ainsi :

| Requête                          | Explication                                 |
| -------------------------------- | ------------------------------------------- |
| GET / HTTP/                      | 1.1 Méthode / Protocole utilisé             |
| Host: www.scholae.fr             | Page à récupérer                            |
| User-Agent : Firefox 65.0        | Client                                      |
| Accept : text/html               | Type de fichier que veut recevoir le client |
| Accept-Language : fr-FR          | Langue qu'utilise le client                 |
| Referer : <https://www.qwant.fr> | Page d'où vient le client                   |

?> Ouvrez votre outil de développement sur votre navigateur (Ctrl+Maj+I sous firefox). Naviguez sur la page de [scholae.fr](https://scholae.fr). Décrire les requêtes GET qui sont utilisés lors du chargement de la page.

Il existe d'autres méthodes tels que HEAD (pour demander des
informations sur la source) ou **POST** (pour transmettre des données au
serveur, très utilisé pour les formulaires). La méthode **GET stocke les
paramètres dans l'URL** elle même alors que la méthode **POST stocke les
paramètres dans le corps de la requête**. La méthode GET n'est pas approprié pour
faire transiter des informations confidentielles puisque toute l'information
est écrite en claire dans l'URL.

Dans le cas des méthodes POST, les actions du client sont envoyées au serveur souvent pour qu'il modifie l'affichage de la
page, on parle alors de web interactif ou de web dynamique. Les langages les plus utilisés en web dynamique sont le **JavaScript** et le **PHP**.

Le protocole HTTP n'est pas sécurisé, il est notamment très sensible aux attaques par l'homme du milieu. Nous verrons en Terminale comment le protocole [HTTPS](../terminal/archi_os_réseaux.md) résout se problème en chiffrant les paquets.

### Javascript :fab fa-js

En combinant HTML et CSS on obtient un site qui permet une très faible
variété d'interactions avec l'utilisateur. Pour ces interactions
hommes-machines il existe plusieurs langages qui peuvent être compiler
soit côté **client** (c'est à dire sur la machine de celui qui consulte
le site) soit côté **serveur**. Javascript (JS) est un langage de
programmation à l'origine côté client mais certaines bibliothèque JS
permettent également une utilisation côté serveur (par ex. Node.js).
D'autre langage comme PHP sont clairement orientés serveur.

Pour une introduction à Javascript quand on connaît déjà python, voire le [site de Pascal Grossé](https://python-carnot.fr/ressources/javascript).

Pour inclure des fonctions JS dans notre fichier, il existe plusieurs
méthodes :

- (i) On peut l'inclure directement dans le **_body_** ou le **_head_** de notre fichier html,

```html
<script>
  alert("Au secours !!");
</script>
```

- (ii) la solution la plus recommandé est de faire comme avec le css, un
  fichier JS séparé dans lequel on écrit les fonctions et que l'on importe à la fin du body.

```html
<script src="script.js" \>
  \
</script>
```

?> Pourquoi écrit t'on le script à la fin du body alors qu'on appelle le fichier css au début du fichier html ? Il faut faire une recherche sur le web pour répondre à cette question.

Le JS permet la majorité des fonctions évènementielles sur le web.
C'est devenu un langage incontournable pour presque tous les
développeurs. Il existe de nombreuses ressources très bien écrites en
ligne à commencer par les cours
d'[Openclassroom](https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript)

?> Faire l'exercice en ligne [Pixel Art](https://projects.raspberrypi.org/en/projects/pixel-art).

?> Naviguez sur le site [state of JS](https://2020.stateofjs.com/fr-FR/technologies/). Qu'en comprenez-vous ?

?> :fas fa-dungeon: Fabriquer un site internet localement sur un sujet de votre choix. Vous pouvez vous aider de tutoriel (par ex. sur
[Openclassroom](https://openclassrooms.com/fr/courses) ou encore du [cours](https://www.pierre-giraud.com/html-css-apprendre-coder-cours/) de Pierre Giraud).

?> :fas fa-dungeon: Jouer au jeu [js robot](https://lab.reaal.me/jsrobot).
