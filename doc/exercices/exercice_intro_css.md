# Exercice intro CSS

## But : formatter le document `intro_css.html`

1. Ajoutez une feuille de style externe, nommée `intro_css.css`, au document
   source `intro_css.html`

2. Ajoutez le contenu des fichiers d'exemples ( `ex1.html`, ... ) au bon endroit
   dans le document HTML.
    - Basez-vous sur les notes de cours sur GitHub, ou directement sur le
      fichier `08_css.md` dans les notes de cours, pour savoir où placer le
      contenu des exemples dans le document HTML.
    - Vous devrez remplacer les balises `<pre>` correspondantes aux exemples
      avec le bon contenu. Exemple : remplacez `<pre>ex1.html</pre>` par le
      contenu du fichier `ex1.html`
    - Assurez-vous que le contenu du fichier est affiché sous sa forme source,
      comme l'exemple de la section *Le CSS a résolu de gros problèmes*, qui
      affiche du code HTML dans la page dans sa forme brute.
3. Il manque une image (`css_ex6.png`). Affichez l'exemple dans un 
   navigateur, prenez une capture d'écran et enregistrez l'image dans le 
   bon dossier pour qu'elle s'affiche dans la page. Le titre `<h4>` juste avant 
   cette image devrait être de la classe `important`
4. Réorganisez le contenu du document HTML avec des 
   `<section>` qui englobent un `h3` et toutes les balises qui suivent 
   jusqu'au `<h3>` suivant. Donc vous devez briser le document en sections 
   selon les `<h3>`. Ajoutez la classe `.important` aux sections *Sélecteurs 
   CSS* et *Le modèle de boîtes du CSS* et 
5. Formatez le document selon les consignes de base suivantes. Vous pouvez 
   aller plus loin que ce qui est demandé, mais vous devez suivre au moins 
   ce qui est demandé.
   1. Ajoutez une image de fond pour toute la page. Faites attention pour 
      que le texte soit lisible facilement. Vous pouvez modifier les 
      couleurs de fond des différentes balises pour que le texte soit plus 
      facile à lire 
   2. Les `h1` et `h2`  
      - doivent être centrées sur la page
      - la largeur doit correspondre à son contenu
      - la largeur maximale doit être de 80%
      - il doit y avoir une bordure de 2px avec les coins arrondis
      - la couleur de fond doit être différente de celle de la page (couleur 
        au choix)
   3. Le code source des exemples doit apparaître dans des genres de boîte avec 
      des couleurs différentes des autres parties du document. **Note** : il 
      n'est pas nécessaire d'avoir de la coloration syntaxique sur les 
      exemples de code.
   4. Pour toutes les sections :
      - changez la couleur de fond des sections (couleur différente des 
        autres couleurs de fond)
      - largeur de 90%, centrée sur la page
      - police de caractères, taille et couleur des `h3` différentes des 
        valeurs par défaut
   5. Pour les sections de la classe `important`, modifiez leur style 
      qu'elles soient plus faciles à repérer (pour qu'elle plus importante en 
      fin de compte)
   6. Les balises `<code>` doivent avoir une couleur de fond différente et 
      une bordure (à votre choix), ainsi qu'une taille de police de 10% plus 
      grande que la valeur par défaut
6. Créez une table des matières pour la page à l'aide d'une liste `<ul>`
   - les liens doivent aller vers chacune des `<h3>`
   - donnez un `id` à votre table des matières
   - appliquez un style différent à table des matières : la `<ul>` de la 
     table des matières doit être affichée différemment des autres `<ul>`