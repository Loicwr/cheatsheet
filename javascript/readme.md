


# 1. Qu'est-ce que JavaScript (JS) ?

## C'est le langage de l'interactivité

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


# 3. Comprendre la structure du code et la syntaxe en JavaScript

La "syntaxe" d'un langage, c'est un peu comme sa grammaire et son orthographe. Ce sont les règles qui définissent comment écrire du code pour que l'ordinateur (ou plus précisément, le moteur JavaScript) puisse le comprendre.

* **ECMAScript vs JavaScript :**
    * **ECMAScript (ES) :** C'est la **spécification**, la **norme** officielle du langage. Imaginez-la comme les règles officielles de la langue française définies par l'Académie française. Elle décrit comment le langage *doit* se comporter, quelles fonctionnalités il doit avoir, et quelle syntaxe utiliser. Cette norme évolue avec le temps, donnant lieu à différentes versions (ES5, ES6/ES2015, ES2016, ES2017, etc.). ES6 (ou ES2015) a été une mise à jour majeure qui a introduit beaucoup de nouveautés très utilisées aujourd'hui (`let`, `const`, fonctions fléchées, classes, etc.).
    * **JavaScript (JS) :** C'est l'**implémentation** la plus populaire de la norme ECMAScript. C'est le langage concret que vous allez écrire et que les navigateurs (Chrome, Firefox...) ou d'autres environnements (comme Node.js) comprennent. Différents moteurs JavaScript (V8 dans Chrome/Node.js, SpiderMonkey dans Firefox...) implémentent la norme ECMAScript.
    * **En résumé pour un débutant :** Quand on parle de "JavaScript", on parle généralement du langage tel qu'il est utilisé aujourd'hui, qui suit les règles de la norme ECMAScript la plus récente supportée par les environnements d'exécution. Vous apprendrez donc "JavaScript" en suivant les règles "ECMAScript".

* **L'importance de la ponctuation :**
    La ponctuation en JavaScript est cruciale, chaque signe a un rôle précis :
    * **Point-virgule (`;`) :** Il marque la **fin d'une instruction** (une commande). C'est comme le point à la fin d'une phrase en français. Nous y reviendrons avec l'insertion automatique.
        ```javascript
        let message = "Bonjour"; // Fin de l'instruction
        console.log(message);   // Fin de l'instruction
        ```
    * **Accolades (`{}`) :** Elles définissent un **bloc de code**. On les utilise pour regrouper plusieurs instructions, par exemple dans les fonctions, les conditions (`if`/`else`), les boucles (`for`/`while`).
        ```javascript
        if (heure < 18) { // Début du bloc if
          console.log("Bonne journée !");
          console.log("Il fait encore jour.");
        } // Fin du bloc if
        ```
    * **Parenthèses (`()`) :** Elles ont plusieurs usages :
        * Pour appeler des fonctions : `maFonction()`
        * Pour définir les paramètres d'une fonction : `function addition(a, b) { ... }`
        * Pour grouper des expressions (priorité des opérations) : `let resultat = (5 + 3) * 2;`
        * Dans les structures de contrôle (`if`, `for`, `while`) : `if (condition) { ... }`
    * **Crochets (`[]`) :** Principalement utilisés pour définir et accéder aux éléments des **tableaux** (listes).
        ```javascript
        let couleurs = ["rouge", "vert", "bleu"]; // Définition d'un tableau
        let premiereCouleur = couleurs[0]; // Accès au premier élément (indice 0)
        ```
    * **Guillemets (`'` ou `"`) :** Pour définir des **chaînes de caractères** (texte). Vous pouvez utiliser les simples ou les doubles, mais soyez cohérent dans votre projet.
        ```javascript
        let prenom = 'Alice';
        let nom = "Dupont";
        ```
    * **Virgule (`,`) :** Pour séparer des éléments dans une liste (paramètres de fonction, éléments de tableau, propriétés d'objet).

* **Standard & Environnement d'exécution :**
    * **Standard :** C'est la norme ECMAScript dont nous venons de parler. Elle assure que le code JavaScript écrit en suivant les règles fonctionnera de manière similaire dans différents endroits.
    * **Environnement d'exécution (Runtime Environment) :** C'est le "programme" qui lit, comprend et exécute votre code JavaScript. Pour le développement front-end, l'environnement principal est le **navigateur web** (Chrome, Firefox, Safari, Edge...). Chaque navigateur possède son propre moteur JavaScript intégré. Cet environnement fournit non seulement le moteur pour exécuter le JS, mais aussi des objets et des API spécifiques (comme `window`, `document`, `console` dans le navigateur) qui permettent à votre code d'interagir avec la page web ou le navigateur lui-même.
    * *(Note : Il existe d'autres environnements, comme Node.js, qui permet d'exécuter du JavaScript côté serveur, mais pour le front-end, vous vous concentrerez sur l'environnement du navigateur).*

# 4. Ce qu'est une instruction

Une **instruction** (ou "statement" en anglais) est une **unité de code unique qui effectue une action**. C'est une commande que vous donnez à l'ordinateur. En JavaScript, les instructions sont généralement séparées par un point-virgule (`;`).

Exemples d'instructions :

* Déclarer une variable : `let age;`
* Assigner une valeur à une variable : `age = 30;`
* Déclarer et assigner en une seule fois : `let nom = "Bob";`
* Appeler une fonction : `console.log("Bonjour !");`
* Une structure de contrôle entière (`if`, `for`) peut aussi être considérée comme une instruction complexe, même si elle contient d'autres instructions à l'intérieur de blocs `{}`.

# 5. Ce qu'est l'insertion automatique (ou implicite) de point-virgule (ASI)

* **Le principe :** JavaScript essaie d'être "gentil". Si vous oubliez un point-virgule à la fin d'une ligne où il devrait y en avoir un, le moteur JavaScript va *souvent* (mais pas toujours !) l'ajouter automatiquement pour vous au moment où il analyse le code. C'est l'ASI (Automatic Semicolon Insertion).
* **Le piège :** Bien que cela puisse sembler pratique, l'ASI peut parfois entraîner des erreurs très difficiles à trouver, car le moteur peut insérer un point-virgule là où vous ne le vouliez pas, ou ne pas en insérer là où il en faudrait un dans des cas complexes. Par exemple :
    ```javascript
    // Exemple où l'ASI peut causer un problème
    return // ASI insère un point-virgule ici !
    { // Cet objet ne sera jamais retourné
      statut: "ok"
    }
    // Le code ci-dessus est interprété comme :
    // return;
    // { statut: "ok" }; // Ce bloc est juste ignoré ou cause une erreur
    ```
* **La bonne pratique (surtout pour les débutants) :** **Toujours mettre explicitement les points-virgules à la fin de chaque instruction.** Cela rend votre code plus clair, plus prévisible et vous évite les problèmes potentiels liés à l'ASI. C'est une habitude adoptée par la grande majorité des développeurs et des outils de formatage de code.


# 6. Comment commencer avec JavaScript ?

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
