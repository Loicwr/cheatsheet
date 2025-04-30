# Déclarations

## Il existe trois type de déclarations de variable en JavaScript

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

## Sur plusieurs lignes :

/*
Tout ce qui est écrit ici est entre commentaires.
*/

## Sur une seule ligne : 

// Voici un commentaire
