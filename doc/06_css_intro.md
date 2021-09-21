Les attributs du cours précédent (révision)
-------------------------------------------

En vrac, nous avons vu :

- les identifiants : `id="idenfiant"`
- l'infobulle : `title="Information à afficher dans l'infobulle"`

Les balises du cours précédent (révision)
-----------------------------------------

En vrac, nous avons vu :

- les caractères spéciaux : Voir le [liste](04b_html_symboles.md) sur le site
  web
- les images : `<img src="lien" alt="texte alternatif" >`
- les figures : `<figure></figure>`
- les légendes pour les figures : `<figcaption></figcaption>`
- les conteneurs génériques :
    - pour un ensemble d'éléments : `<div></div>`
    - dans une ligne : `<span></span>`
- les conteneurs spécifiques (avec un rôle) :
    - les en-têtes : `<header></header>`
    - la navigation : `<nav></nav>`
    - les pieds de page : `<footer></footer>`
    - les sections : `<section></section>`
    - les informations complémentaires : `<aside></aside>`
    - les articles : `<article></article>`

Les liens vus au cours précédent (révision)
-------------------------------------------

En vrac, nous avons vu les liens :

- vers un identifiant : `href="#nom-de-identifiant"`
- vers un courriel : `href="mailto:courriel@ecrire.ici"`
- vers un numéro de téléphone **sans** extension :
  `href="tel:000-000-0000"`
- vers un numéro de téléphone **avec** extension (ex. 1234) :
  `href="tel:000-000-0000p1234"`
- vers un pseudo ou un numéro Skype : `href="callto:pseudo_skype"`

Le pouvoir des catégories
-------------------------

Est-ce qu'il existe des éléments, dans nos pages web, qui réfèrent à une même
catégorie ? Prenez simplement notre pièce la *Jalousie du Barbouillé*. Dans
cette page, vous retrouvez plusieurs *didascalies*, plusieurs *noms de
personnage* (au début des dialogues) et plusieurs
*indications à l'acteur* (ce que nous avons surligné). Il serait intéressant
d'informer le navigateur que toutes les didascalies qu'elles sont des
didascalies. Cette utilité sera importante pour le CSS. Heureusement, les
catégories existent en HTML. Le principe est d'ajouter un attribut qui informe
sur la catégorie des éléments. En gros, nous leur ajoutons un type.

Les catégories en HTML, l'attribut `class="categorie"`
------------------------------------------------------------------------------------------------------------------
([Référence](https://www.w3schools.com/tags/att_class.asp))

Il s'agit d'un attribut global. C'est-à-dire qu'il est possible d'ajouter l'
attribut `class` sur toutes les balises HTML. Cet attribut permet d'ajouter, à
la base, une catégorie. Il est même possible d'ajouter plusieurs catégories.
Pour y ajouter plusieurs catégories, nous ajoutons un simple espace blanc entre
les noms de catégories. Il y a quelques règles sur les noms utilisés pour les
catégories.

- Il doit être **significatif**.
- Il **ne doit pas** y avoir d'**espaces** dans un nom.
- Il **ne faut pas** utilisé de **caractères spéciaux** (les
  **tirets** `-` sont **acceptés**).

Voici deux exemples, dans la pièce *La Jalousie du Barbouillé*, nous pouvons
ajouter la catégorie `didascalie` à nos *didascalies*.

```html

<section id="scene-1">
    <h3>Scène première (<em>Le Barbouillé</em>)</h3>
    <p class="didascalie">
        <em>
            Le barbouillé entre sur la scène par le côté jardin. Il avance
            songeux vers le centre de la scène. Il garde ces yeux vers le base.
            Il se place devant le public. Lentement, il relève tête et il
            regarde le public dans les yeux.
        </em>
    </p>

    <p>
        <strong>Le Barbouillé</strong>
        <mark>(au public)</mark>
        : Il faut avouer que je suis le plus malheureux de tous les hommes !
        J’ai une femme qui me fait enrager.
    </p>

    <p class="didascalie">
        <em>
            Le Barbouillé se déplace vers le côté cours tout en regardant le
            public.
        </em>
    </p>

    <p>
        <strong>Le Barbouillé</strong>
        <mark>(au public)</mark>
        : Au lieu de me donner du soulagement et de faire les choses à mon
        souhait, elle me fait donner au diable vingt fois le jour.
    </p>

    <p class="didascalie">
        <em>
            Le Barbouillé se tourne vers le côté jardins et il continue à
            discourir.
        </em>
    </p>

    <p>
        <strong>Le Barbouillé</strong>
        <mark>(au public)</mark>
        : Au lieu de se tenir à la maison, elle aime la promenade, la bonne
        chère, et fréquente je ne sais quelle sorte de gens.
    </p>

    <p class="didascalie">
        <em>
            Arrivé au côté jardin, le Barbouillé se retourne vers le public.
        </em>
    </p>

    <p>
        <strong>Le Barbouillé</strong>
        <mark>(au public)</mark>
        : Ah ! pauvre Barbouillé, que tu es misérable ! Il faut pourtant la
        punir. Si tu la tuais... L’intention ne vaut rien, car tu serais pendu.
        Si tu la faisais mettre en prison… La carogne en sortirait avec son
        passe-partout. Que diable faire donc ?
    </p>
</section>
```

Nous pouvons, aussi, ajouter la catégorie `dialogue` à nos *répliques*. De plus,
nous pouvons modifier les balises autour du nom des personnages. Nous avons vu,
la semaine dernière, la balise
`<span></span>` qui donne un conteneur générique. Nous verrons son utilité dans
un prochaine section.

```html

<section id="scene-1">
    <h3>Scène première (<em>Le Barbouillé</em>)</h3>
    <p class="didascalie">
        <em>
            Le Barbouillé entre sur la scène par le côté jardin. Il avance
            songeux vers le centre de la scène. Il garde ces yeux vers le base.
            Il se place devant le public. Lentement, il relève tête et il
            regarde le public dans les yeux.
        </em>
    </p>

    <p class="dialogue">
        <span>Le Barbouillé</span>
        <mark>(au public)</mark>
        : Il faut avouer que je suis le plus malheureux de tous les hommes !
        J’ai une femme qui me fait enrager.
    </p>

    <p class="didascalie">
        <em>
            Le Barbouillé se déplace vers le côté cours tout en regardant le
            public.
        </em>
    </p>

    <p class="dialogue">
        <span>Le Barbouillé</span>
        <mark>(au public)</mark>
        : Au lieu de me donner du soulagement et de faire les choses à mon
        souhait, elle me fait donner au diable vingt fois le jour.
    </p>

    <p class="didascalie">
        <em>
            Le Barbouillé se tourne vers le côté jardins et il continue à
            discourir.
        </em>
    </p>

    <p class="dialogue">
        <span>Le Barbouillé</span>
        <mark>(au public)</mark>
        : Au lieu de se tenir à la maison, elle aime la promenade, la bonne
        chère, et fréquente je ne sais quelle sorte de gens.
    </p>

    <p class="didascalie">
        <em>
            Arrivé au côté jardins, le Barbouillé se retourne vers le public.
        </em>
    </p>

    <p class="dialogue">
        <span>Le Barbouillé</span>
        <mark>(au public)</mark>
        : Ah ! pauvre Barbouillé, que tu es misérable ! Il faut pourtant la
        punir. Si tu la tuais... L’intention ne vaut rien, car tu serais pendu.
        Si tu la faisais mettre en prison… La carogne en sortirait avec son
        passe-partout. Que diable faire donc ?
    </p>
</section>
```

À quoi ressemble le CSS
-----------------------

La syntaxe du CSS est assez simple. Le langage fonctionne par
***propriété***. En gros, le principe est d'attribuer des valeurs à des
propriétés prédéfinies. Ces propriétés sont des placés dans des blocs qui
indiquent que cette propriété est appliquée à une balise. Sans plus attendre,
voici la syntaxe générale du CSS :

```css
balise {
    propriété-1: valeur-de-la-propriété;
    propriété-2: valeur-de-la-propriété;
    propriété-3: valeur-de-la-propriété;
/ / . . .
}

/*********************************************************************
 * En CSS, les commentaires utilisent les mêmes caractères qu'en Java.
 *
 * Les commentaires de ligne : // Le commentaire...
 * 
 * Les blocs de commentaires (sur plusieurs lignes) : /* Le commentaire ...*/
```

Ajouter du CSS au HTML
----------------------

Avant de voir nos premières propriétés, voyons comment ajouter le CSS à un
fichier HTML. Il existe deux solutions possibles : lié un fichier
*CSS* ou ajouter dans une balise `<style></style>`.

Ajouter dans le document HTML, la balise `<style></style>`
----------------------------------------------------------------------------------------------------------------------
([Référence](https://www.w3schools.com/tags/tag_style.asp))

Cette balise, placé dans la balise `<head></head>` permets de définir sur CSS
pour le document uniquement. Elle s'utilise comme suit :

```html

<head>
    <meta charset="utf-8">
    <title>Titre du site</title>
    <style>
        balise {
            propriété-1: valeur-de-la-propriété;
            propriété-2: valeur-de-la-propriété;
            propriété-3: valeur-de-la-propriété;
        / / . . .
        }
    </style>
</head>
```

### Avantage de la balise

La balise permet de réduire le nombre de fichiers sur le site. De plus, vous
êtes assuré d'avoir toujours le style dans votre page web.

### Désavantage de la balise

Ceci alourdit de manière importante votre page web. De plus, votre code ne peut
pas être réutilisé dans d'autre page web.

### Utilisation de la balise dans le cadre de ce cours

À moins que ce soit expressément demandé, nous **n'utiliserons pas**
cette balise. Pour vos TP, vous devrez utiliser la prochaine balise.

Lier un fichier CSS et HTML, la balise `<link href="lien" rel="type" >`
----------------------------------------------------------------------------------------------------------------------------------
([Référence](https://www.w3schools.com/tags/tag_link.asp))

Cette balise, placé dans la balise `<head></head>` permets de lier un fichier
CSS dans une page web. Nous verrons plus tard qu'il est possible de lier d'autre
ressource qu'un fichier CSS. Pour les fichiers CSS, cette balise s'utilise comme
suit :

```html

<head>
    <meta charset="utf-8">
    <title>Titre du site</title>
    <link rel="stylesheet" href="./css/styles.css">
</head>
```

### Fichier CSS

Les fichiers CSS ont toujours l'extension `.css`. Vous créez votre fichier
exactement comme les fichiers HTML dans Visual Studio Code, mais vous
sélectionnez ***CSS (.css)*** comme type de fichier. Par habitude et convention
personnelle, je place toujours mes fichiers CSS dans un dossier `./css/` situé à
la racine du site web (à côté de notre page web). Ceci permet de simplifier la
vue dans le dossier et la recherche des fichiers. J'applique la même logique aux
images et vidéo.

#### Le code de base d'un fichier CSS

```css
@charset "utf-8";
```

### L'attribut `href="lien"`

Il s'agit ni plus ni moins que du même attribut que pour la balise
`<a href="lien"></a>`. Son but, dans la balise `<link>` est d'informer du lien (
chemin) vers notre ressource (fichier CSS).

### Avantage de la balise

La balise permet de lier le CSS sans alourdir la page. De plus, vous pouvez
réutiliser le fichier sur plus d'un site et vous pouvez toujours ajouter plus
d'un fichier CSS. Il est donc possible de spécialiser nos fichiers.

### Désavantage de la balise

Nous sommes dépendants de l'existence des fichiers CSS. S'il est déplacé,
renommé ou supprimé, il faut modifier notre page web en conséquence.

### Utilisation de la balise dans le cadre de ce cours

À moins que ce soit expressément demandé, nous **utiliserons toujours**
cette balise.

L'attribut `rel="type"`
--------------------------------------------------------------------------------------
([Référence](https://www.w3schools.com/tags/att_link_rel.asp))

Cet attribut permet de spécifier le type de ressource lié par la balise
`<link>`. Concernant les fichiers de style CSS, il faut comprendre que nous
utilisons le type `rel="stylesheet"`. Il en existe d'autres, mais nous les
verrons plus tard. Pour le moment, il ne sont pas utiles.

Notre première propriété CSS, `color`
-------------------------------------------------------------------------------------------------------
([Référence](https://www.w3schools.com/cssref/pr_text_color.asp))

Cette propriété permet de modifier la couleur d'écriture. Il existe plusieurs 
manières d'écrire une couleur :

- Avec son nom (exemple : rouge = `red`) ; il existe des codes de nom
  prédéfini (supporté par tous les navigateurs). Cliquez sur ce
  [lien](https://www.w3schools.com/colors/colors_names.asp) pour connaître les
  différents noms.
- Il existe la couleur hexadécimale
  (exemple : rouge = `#ff0000`)
- Il existe la couleur RGB (exemple
  : rouge = `rgb(255, 0, 0)`)
- Il existe la couleur RGBA (exemple
  : rouge = `rgb(255, 0, 0, 1)`)
- Le mot clé `currentcolor` qui permet de réutiliser automatiquement la couleur
  mentionnez dans la balise.

Cette propriété, comme toutes les autres, s'utilise simplement en indiquant son
nom (`color`) et sa valeur.

```css
balise {
    color: valeur;
}
```

Comment ajouter les titres en bleu foncé dans notre pièce.
----------------------------------------------------------

Pour que nos textes soient écrits en bleu foncé, il faut spécifier, toujours
dans le fichier CSS, la balise du titre (`h1`, `h2`, `h3`, etc.) et, dans notre
bloc, attribuer la valeur `darkblue` à la propriété
`color`.

```css
h1 {
    color: darkblue;
}

h2 {
    color: darkblue;
}

h3 {
    color: darkblue;
}
```

### Simplifions notre CSS

Parfois, comme dans l'exemple précédent, plusieurs balises auront le même style.
Toutefois, répéter plusieurs fois le même code alourdit le fichier et il s'agit
d'une grande source d'erreur de la part de la personne développée. Heureusement
pour nous, le CSS supporte une syntaxe « *généreuse* » pour ces cas de figure.
Nous pouvons appliquer un bloc de style à plusieurs balises, il suffit de
séparer chaque balise par une virgule. La syntaxe générale est alors :

```css
balise-1, balise-2, balise-3, /*...*/, balise-n {
    propriete-1: valeur;
    /*...*/
    propriete-n: valeur;
}
```

Ainsi, notre exemple précédent devient simplement :

```css
h1, h2, h3 {
    color: darkblue;
}
```

Ordre application des styles
----------------------------

Après notre bloc de style, dans l'exemple précédent, ajoutez le code suivant :

```css
h2 {
    color: deeppink;
}
```

Que remarquez-vous ? Réessayez avec plusieurs couleurs différentes l'une à la
suite de l'autre. Choisissez des couleurs donc la différence est marquante,
personnellement j'ai pris :

```css
h1, h2, h3 {
    color: darkblue;
}

h2 {
    color: deeppink;
}

h2 {
    color: darkgreen;
}

h2 {
    color: darkred;
}

h2 {
    color: goldenrod;
}

h2 {
    color: grey;
}
```

La couleur qui s'affiche est toujours la dernière indiquée. Il s'agit du
**principe de la cascade**. Nous pouvons définir plusieurs fois un bloc de
style, mais ce sera toujours la dernière valeur indiquée qui sera sélectionnée.
Maintenant, ajoutez le mot clé `!important` après l'une des valeurs, sauf la
dernière, et avant le point virgule. N'oubliez pas le `!` et d'ajouter un espace
entre la valeur et le mot clé. Que remarquez-vous ?

```css
h2 {
    color: darkgreen !important;
}
```

Maintenant, ajoutez un deuxième `!important` dans un second bloc, plus bas que
votre précédent. Que remarquez-vous ?

```css
h2 {
    color: darkgreen !important;
}

h2 {
    color: darkred;
}

h2 {
    color: goldenrod !important;
}
```

Peut importe si vous ajoutez des valeurs après une propriété avec ce mot clé, le
navigateur utilisera la dernière valeur avec le mot clé
`!important`. Selon vous, quelle est l'explication ? \[su\_spoiler title="
Pourquoi `!important` ?"\]

Pourquoi `!important` ?
-----------------------

Ce mot clé appose une très haute priorité à votre valeur. Seule une autre
propriété avec le mot clé `!important` pourra changer votre valeur à ce moment.


Qu'est-ce qui ce passe avec deux fichiers CSS ?
-----------------------------------------------

Ajoutez un second fichier CSS à votre projet. Ajoutez-y le code suivant :

```css
h2 {
    color: lawngreen !important;
}
```

Pour l'ajouter dans votre page HTML, ajoutez une nouvelle balise
`<link>` situé après la précédente. Personnellement, j'ai appelé mon second
fichier `app.css`. Mon `<head></head>` est devenu :

```html
<head>
    <meta charset="utf-8">
    <title>La Jalousie du Barbouillé</title>
    <link rel="stylesheet" href="./css/style.css">
    <link rel="stylesheet" href="./css/app.css">
</head>
```

Que remarquez-vous ? Qu'est-ce qui ce passe si nous inversons les deux
balises `<link>` ? Qu'est-ce qui se passe qui vous retirez les mots clés
`!important` du second fichier (dans l'ordre des `<link>`) ? Par la suite,
qu'est-ce qui arrive si nous enlevons tous les `!important` ? Finalement,
qu'est-ce qui arrive si nous inversons à nouveau les fichiers ?

*Principe de la cascade* en CSS
-------------------------------

Pour conclure ce chapitre d'introduction, nous allons établir formellement le **
principe de la cascade** en CSS.

> Lors de la liaison des styles CSS, le navigateur appliquera la
> dernière valeur indiquée. Cette valeur est déterminée par le dernier
> style lu. De plus, lorsque la page web lie plusieurs feuilles de
> style, la dernière propriété lue est
> présente dans la dernière feuille liée.

Bien évidemment, ce principe s'applique aux styles donnés dans les
balises `<style></style>`. Il faut voir le contenu de ces balises comme une
feuille de style.

Système de couleur
------------------

### RGB

Il existe plusieurs formulations pour écrire une couleur. En premier lieu, vous
devez comprendre comment l'ordinateur affiche une couleur à écran. Pour le
système informatique, un écran n'est ni plus ni moins qu'une grille de pixel.
Chaque pixel est composé de trois couleurs
(rouge, vert et bleu). Chaque couleur possède 256 intensités. Ainsi, un pixel va
afficher un mélange de ces trois couleurs selon l'intensité de chacune. Il
s'agit du système **RGB**. Ainsi, la couleur rouge « pure » aura une intensité
de rouge de 255 (la valeur 0 compte comme une intensité donc [256 − 1 = 255]
au maximum) tandis qu'intensité des deux autres sera de 0.

### Hexadécimale

Par la suite, il existe un autre système de couleur. Il s'agit du système
hexadécimal. Les nombres hexadécimaux sont des nombres encodés sur une base 16
au lieu de 10. En gros, le système hexadécimal et RGB sont identiques. Il s'agit
simplement du format d'encodage. Néanmoins, les nombres hexadécimaux sont plus
faciles à comprendre pour le navigateur et il s'agit des codes utilisés dans le
monde du web. Un peu plus bas, je vous ai ajouté un tableau comparatif (non
exhaustif) entre les différents systèmes. La base 16 fonctionne comme suit :
Tout les chiffres de 0 à 9 sont représenté par leur équivalent décimal,
toutefois, les nombres de 10 à 15, sont représentés par les lettres de
l'alphabet de A à F. Par la suite, une rajoutons une décimale, ainsi 16 devient
10, 17 devient 11, etc. Voici une courte liste de valeur de décimale à
hexadécimale

|Décimale|0|1|9|10|13|15|16|25|26|50|100|150|200|255|
|--------------|---|---|---|----|----|----|----|----|----|----|-----|-----|-----|-----|
|Hexadécimale|0|1|9|A|D|F|10|19|1A|32|64|96|C8|FF|

Voici un
[convertisseur](https://sebastienguillon.com/test/javascript/convertisseur.html)
pour vous aidez. Dans ce système, chaque couleur (rouge, vert et bleu)
est représentée par deux chiffres dans l'ordre suivant Rouge-Vert-Blue. Ainsi,
le nombre `#FF0000` représente 255 rouges, 0 vert et 0 bleu. Le nombre `#00FF00`
représente 0 rouge, 255 vert et 0 bleu. Le nombre
`#0000FF` représente 0rouge, 0 vert et 255 bleu.

### Noms

Il s'agit d'un système de convention des couleurs. Il s'agit du système que vous
avons pris aujourd'hui. Je vous le recommande fortement dès que possible. Il
s'agit d'une normalisation de certaines couleurs. Prenez par exemple la
couleur `LawnGreen`. Grâce au système de nommage, vous êtes assuré que cette
couleur sera la même d'une plateforme, d'un navigateur et d'une version à
l'autre.

### RGBA

Même système que le RGB, mais elle ajoute une quatrième valeur. Cette valeur,
qui oscille entre 0 et 1, représente la transparence de la couleur. Lorsque nous
avons un rouge « pure » qui s'affiche pleinement, sa valeur RGBA
est `(255, 0, 0, 1)`. Si nous avons la valeur `(255, 0, 0, 0.5)`, alors le rouge sera à moitié transparent. De même
si `(255, 0, 0, 0)`, la couleur sera complètement transparente.

### Tableau de comparaison

    Nom (français)   Nom (normalisé) Valeur RGB    Valeur hexadécimale
    --------------   -------------   ----------    ------------------------
    Noir             `black`         (0, 0, 0)         `#000000`
    Rouge            `red`           (255, 0, 0)       `#FF0000`
    Rouge foncé      `darkred`       (139, 0, 0)       `#8B0000`
    Indigo           `indigo`        (75, 00, 130)     `#4B0082`
    Vert lime        `limegreen`     (50, 205, 50)     `#32CD32`
    Blanc            `white`         (255, 255, 255)   `#FFFFFF`

### Un sélecteur de couleur

Pour vous aidez à choisir vos couleurs, prenez le sélecteur de couleur
de [W3Schools.com](https://www.w3schools.com/colors/colors_picker.asp). 

------------------------------------------------------------------------

Notes écrites par Godefroy Borduas, modifiées par Denis Rinfret.

   
