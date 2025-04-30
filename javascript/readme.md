


# 1. Qu'est-ce que JavaScript (JS) ?

## Le langage de l'interactivité

Imaginez une page web comme une maison :

- **HTML** (*HyperText Markup Language*) est la **structure** de la maison (les murs, le toit, les pièces).
- **CSS** (*Cascading Style Sheets*) est la **décoration** (la couleur des murs, le style des meubles, l'agencement).
- **JavaScript** est **l'électricité et la plomberie** :  
  Il permet aux choses de fonctionner, de réagir :  
  allumer la lumière quand on appuie sur l'interrupteur, ouvrir le robinet pour avoir de l'eau, etc.

### Côté client

JavaScript s'exécute principalement **dans le navigateur web** de l'utilisateur (Chrome, Firefox, Safari...).  
C'est pourquoi on l'appelle souvent un langage **"côté client"** (*client-side*) dans le contexte du front-end.

### Pas Java !

⚠️ **Attention** : JavaScript n'a presque **rien à voir** avec le langage **Java**, malgré la ressemblance du nom.  
C'est une confusion fréquente au début !


# 2. Pourquoi JavaScript est essentiel pour le Front-End ?

Sans JavaScript, les pages web seraient largement **statiques** (comme une affiche). JavaScript permet de :

- **Rendre les pages interactives** : réagir aux actions de l'utilisateur (clics de souris, remplissage de formulaires, survol d'éléments).
- **Modifier le contenu HTML et le style CSS dynamiquement** :  
  Changer du texte, afficher/cacher des éléments, modifier des couleurs ou des tailles après le chargement initial de la page, sans avoir à recharger toute la page.
- **Valider des formulaires** : vérifier que l'utilisateur a bien rempli les champs requis avant d'envoyer les données.
- **Créer des animations et des effets visuels** : menus déroulants, carrousels d’images (sliders), effets de transition...
- **Communiquer avec des serveurs (de manière asynchrone)** :  
  Récupérer ou envoyer des données en arrière-plan sans bloquer l’interface utilisateur (par exemple, charger de nouveaux articles quand on fait défiler une page, ou afficher des suggestions de recherche pendant qu'on tape).  
  Cela se fait souvent avec **AJAX** (*Asynchronous JavaScript and XML*), même si aujourd’hui on utilise plus souvent **JSON** que **XML**.

---

# 3. Comment commencer avec JavaScript ?

#### Outils de base

- Un **navigateur web** : Chrome ou Firefox sont excellents pour les développeurs car ils ont de très bons outils de développement intégrés.
- Un **éditeur de code** :  
  Comme **Visual Studio Code** (gratuit et très populaire), **Sublime Text**, **Atom**...  
  Un simple bloc-notes peut suffire au tout début, mais un éditeur de code vous facilitera grandement la vie.

#### Où écrire le code JS ?

- **Dans le fichier HTML** : directement entre des balises `<script> ... </script>`.  
  C’est bien pour des petits tests rapides.
- **Dans un fichier externe** : méthode recommandée.  
  Vous créez un fichier séparé avec l’extension `.js` (par exemple `monscript.js`) et vous le liez à votre fichier HTML avec une balise :

    ```html 
    <script src="monscript.js"></script> 
    ```
    Généralement placée juste avant la fermeture de la balise `</body>`.


# Déclarations

### Il existe trois type de déclarations de variable en JavaScript

**var**   : On déclare une variable ,éventuellement en initialisant sa valeur.

**let**   : On déclare une variable dont la portée est celle du bloc courant, éventuellement en initialisant sa valeur.

**const** : On déclare une constante nommée, dont la portée est celle du bloc courant,accesible en lecture seule.

# Différents types de données :

| Variable               | Explication                                                                                                                                      | Exemple                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Chaîne de caractères] | Une suite de caractères connue sous le nom de chaîne. Pour indiquer que la valeur est une chaîne, il faut la placer entre guillemets.           | `let myVariable = 'Bob';`                                                                    |
| Nombre                 | Un nombre. Les nombres ne sont pas entre guillemets.                                                                                             | `let myVariable = 10;`                                                                       |
| Booléen                | Une valeur qui signifie vrai ou faux. `true` / `false` sont des mots-clés spéciaux en JS, ils n'ont pas besoin de guillemets.                   | `let myVariable = true;`                                                                     |
| Tableau                | Une structure qui permet de stocker plusieurs valeurs dans une seule variable.                                                                  | `let myVariable = [1,'Bob','Étienne',10];` <br> Référez-vous à chaque élément : `myVariable[0]`, `myVariable[1]`... |
| Objet                  | À la base de toute chose. Tout est un objet en JavaScript et peut être stocké dans une variable. Gardez cela en mémoire tout au long de ce cours.| `let myVariable = document.querySelector('h1');` <br> Tous les exemples ci-dessus sont aussi des objets. |


# 2 type de commentaires possible 

### Sur plusieurs lignes :

/*
Tout ce qui est écrit ici est entre commentaires.
*/

## Sur une seule ligne : 

// Voici un commentaire


# Opérateurs 

### Un opérateur est un symbole mathématique qui produit un résultat en fonction de deux valeurs (ou variables). Le tableau suivant liste certains des opérateurs les plus simples ainsi que des exemples que vous pouvez tester dans votre console JavaScript.

| Opérateur                        | Explication                                                                                                                                         | Symbole(s)     | Exemple                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------|
| Addition                         | Utilisé pour ajouter deux nombres ou concaténer (accoller) deux chaînes.                                                                            | `+`            | `6 + 9;` <br> `"Bonjour " + "monde !";`                                                                  |
| Soustraction, multiplication, division | Les opérations mathématiques de base.                                                                                                              | `-`, `*`, `/`  | `9 - 3;` <br> `8 * 2;` // pour multiplier, on utilise un astérisque <br> `9 / 3;`                        |
| Assignation                      | On a déjà vu cet opérateur : il affecte une valeur à une variable.                                                                                  | `=`            | `let myVariable = 'Bob';`                                                                               |
| Égalité                          | Teste si deux valeurs sont égales et renvoie un booléen `true` / `false` comme résultat.                                                            | `===`          | `let myVariable = 3;` <br> `myVariable === 4;`                                                           |
| Négation, N’égale pas            | Renvoie la valeur logique opposée à ce qui précède ; il change `true` en `false`, etc. Utilisé avec l’opérateur d’égalité, il teste la non-égalité. | `!`, `!==`     | `let myVariable = 3;` <br> `!(myVariable === 3);` <br><br> `let myVariable = 3;` <br> `myVariable !== 3;` |
