# 🧪 Fonctionnalités essentielles de Sass (explications détaillées)

---

## 🎨 1. Variables

### ➕ À quoi ça sert ?
Les variables permettent de stocker des valeurs réutilisables (couleurs, espacements, tailles, polices, etc.).  
Elles rendent ton code plus maintenable et plus cohérent.

### 🧾 Syntaxe :
```scss
$primary-color: #3498db;
$font-stack: 'Helvetica, sans-serif';
$padding: 1rem;

body {
  background-color: $primary-color;
  font-family: $font-stack;
  padding: $padding;
}
```

### 🎯 Avantages :
- Modifier une seule variable et tout ton style s’ajuste
- Meilleure organisation
- Facilite la création de thèmes (ex: mode sombre)

---

## 🧩 2. Mixins

### ➕ À quoi ça sert ?
Les mixins te permettent de réutiliser des blocs de code CSS avec ou sans paramètres.  
Tu évites les répétitions, et ton CSS devient plus DRY (Don't Repeat Yourself).

### 🧾 Syntaxe :
```scss
@mixin button-style($bg-color, $text-color) {
  background-color: $bg-color;
  color: $text-color;
  padding: 10px 15px;
  border-radius: 4px;
}

.button {
  @include button-style(#3498db, white);
}
```

### 🎯 Avantages :
- Paramétrable (comme une fonction)
- Centralisation de styles
- Réutilisable dans tout le projet

---
## 🧠 3. Fonctions

### ➕ À quoi ça sert ?
Une fonction retourne une valeur. Tu peux l’utiliser pour faire des calculs dynamiques (ex: convertir des unités, ajuster des couleurs…).

### 🧾 Syntaxe :
```scss
@function rem($px, $base: 16) {
  @return $px / $base * 1rem;
}

p {
  font-size: rem(18); // 1.125rem
}
```

### 🎯 Avantages :
- Très utile pour les systèmes de grille, typographie responsive
- Logique centralisée et facilement ajustable
- Fonctionne parfaitement avec les mixins et boucles

---

## 📂 4. Partials & Imports

### ➕ À quoi ça sert ?
Tu peux découper ton code Sass en plusieurs fichiers (partials), pour mieux l’organiser.  
Ensuite, tu les importes dans un fichier principal (style.scss par exemple).

### 🧾 Syntaxe :
**_variables.scss**
```scss
$primary: #e67e22;
```

**style.scss**
```scss
@use 'variables';
```

> Les fichiers commençant par un `_` sont non compilés directement : ce sont des partials.

### 🎯 Avantages :
- Code plus propre et lisible
- Fichiers spécialisés (typographie, layout, composants…)
- Maintenance simplifiée

---
