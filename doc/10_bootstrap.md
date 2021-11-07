Qu'est-ce que Bootstrap?
--------------------------------------------------------

- Bootstrap est un cadriciel client (_front-end_) gratuit pour un 
  développement web plus rapide et plus facile
- Bootstrap comprend des gabarits de design basés sur le HTML et le CSS pour la
  typographie, les formulaires, les buttons, les tableaux, la navigation, 
  les images, etc., ainsi que des extensions JavaScript optionnelles
- Bootstrap donne aussi la possibilité de créer des designs réactifs

### Qu'est-ce qu'un _design réactif_ ? 

Le but d'un design réactif est de créer des sites web qui s'ajustent 
automatiquement à la taille de l'écran, d'un petit téléphone jusqu'aux 
grands écrans d'un ordinateur. 

### Pourquoi utiliser Bootstrap ?

- Avantages de Bootstrap:
    - **Facie d'utilisation** : n'importe qui avec des connaissances de HTML 
      et CSS peut utiliser Bootstrap
    - **Fonctionnalités réactives** : le CSS réactif de Bootstrap s'ajuste 
      aux différentes tailles de l'écran
    - **Approche _mobile en premier_** : Avec Bootstrap, le support 
      d'appareils mobiles est au coeur du cadriciel
    - **Compatibilité des navigateurs** : Bootstrap 4 est compatible avec 
      tous les navigateurs modernes (Chrome, Firefox, Edge, Safari, Opera, ...)

### Comment créer une page avec Bootstrap

- Créer un document HTML5
- Inclure les bons fichiers CSS et JavaScript
- Utiliser des `<div>`s avec les bonnes classes CSS Bootstrap pour structurer 
  votre page
- Utiliser les autres balises HTML avec des classes CSS Bootstrap CSS pour 
  le contenu de la page

**Notes** :

- Dans ce cours, Bootstrap est très important pour le TP3, mais beaucoup moins
important pour l'examen
- On va seulement faire la base en classe, et vous devrez _jouer_ avec pour 
  le TP3

### Le système de grille Bootstrap 4

- Le système de grille Bootstrap est construit à l'aide de _flexbox_ et 
  permet jusqu'à 12 colonnes sur la page.

- Si vous n'avez pas besoin de 12 colonnes individuellement, vous pouvez 
  grouper des colonnes ensemble pour obtenir des colonnes plus larges

- Le système de grille est réactif et les colonnes vont être réarrangées 
  automatiquement dépendamment de la largeur de l'écran.

- Assurez-vous que le total de la largeur de colonnes est de 12 ou moins. 
  Il n'est pas nécessaire que le total soit exactement 12

#### Example: `bs4_ex1.html`

### Exemple : Table Bootstrap

- Une table Bootstrap peut être construite de la même façon qu'une simple 
  table HTML, mais en ajoutant des classes CSS spécifiques à Bootstrap
- Au minimum, la classe `table` doit être spécifiée, plus 
  d'autres classes pour modifier les couleurs
- Des classes CSS classes peuvent aussi être ajoutées aux balises `tr` et `td` 
  pour modifier des cellules particulières
- Pour que la table soit réactive, placez la table dans une balise
  `<div class="table-responsive">`
    - des barres de défilement vont être ajoutées automatiquement si 
      nécessaire à la place d'écraser la table pour entre dans la fenêtre
    - `table-responsive-sm`, `table-responsive-md`,
      `table-responsive-lg` et `table-responsive-xl` peuvent aussi être 
      utilisées

#### File `bs4_ex2.html`

### Barre de Navigation

- Le prochain exemple démontre un gabarit de base pour un site web avec une 
  barre de navigation en haut de la page
- Cet exemple est basé sur les exemples présents sur le site de la W3Schools
- La barre de navigation (`navbar`) est repliable : si l'écran n'est pas 
  assez large, alors la barre se transformera en un menu activé par un bouton
- La `navbar` est fixé au haut de la page, donc si la page a beaucoup de 
  contenu, la barre va rester visible au haut de la page lorsque 
  l'utilisateur utilise les barres de défilement pour se déplacer dans la page
    - Pour s'assurer que la barre de navigation ne recouvre pas le contenu 
      au début de la page, la déclaration `padding-top: 50px` est ajoutée au 
      `body` pour décaler le contenu
- Les items dans la `navbar` sont placés dans une `<ul>`, avec les `<li>`s 
  qui contiennent les liens (les balises `<a>`)

#### Exemple `bs4_contact.html`

- Cet exemple contient la même `navbar` que l'exemple précédent, mais avec 
  une  `<dl>` comme contenu sous la barre de navigation
- En général, la même (ou presque la même) `navbar` va être utilisée dans 
  plusieurs pages différentes, sinon dans toutes les pages, d'un site web
- Il n'est pas pratique de copier et coller le même code dans chaque fichier,
  mais pour l'instant, il n'y a pas d'autres choix
- Lorsque vous apprendrez la programmation web côté serveur, que ce soit en 
  JavaScript, en Python, en PHP, ..., vous verrez comment éviter de copier 
  et coller des éléments (`navbar`, `footer`, ...) dans toutes les pages : 
  pour cela, vous utiliserez probablement des gabarits HTML  
