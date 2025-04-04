# 🎨 Cheatsheet Flexbox - Fun & Coloré

## 🏗️ Conteneur Flex

```css
.container {
  display: flex; /* 🎬 Active Flexbox */
  flex-direction: row; /* 🔄 Direction des éléments */
  justify-content: flex-start; /* 📏 Alignement horizontal */
  align-items: stretch; /* 📐 Alignement vertical */
  flex-wrap: nowrap; /* 🔀 Gestion du retour à la ligne */
  gap: 10px; /* 📏 Espace entre les éléments */
}
```
### 🌟 Propriétés du conteneur

- `display: flex;` → 🎬 Active Flexbox
- `flex-direction:` 🔄
  - `row` (par défaut) → ⬅️➡️ De gauche à droite
  - `row-reverse` → ➡️⬅️ De droite à gauche
  - `column` → ⬆️⬇️ De haut en bas
  - `column-reverse` → ⬇️⬆️ De bas en haut
- `justify-content:` (Alignement horizontal) 📏
  - `flex-start` (par défaut) → ⬅️ Aligné à gauche
  - `flex-end` → ➡️ Aligné à droite
  - `center` → 🎯 Centre horizontalement
  - `space-between` → ↔️ Espace maximal entre les éléments
  - `space-around` → 🔄 Espace égal autour des éléments
  - `space-evenly` → ➖ Espace uniforme
- `align-items:` (Alignement vertical) 📐
  - `stretch` (par défaut) → ↕️ Étire les éléments
  - `flex-start` → ⬆️ Aligné en haut
  - `flex-end` → ⬇️ Aligné en bas
  - `center` → 🎯 Centre verticalement
    - `baseline` → 📏 Alignement sur la ligne de base du texte
- `flex-wrap:` (Gestion du retour à la ligne) 🔀
  - `nowrap` (par défaut) → 🚫 Pas de retour à la ligne
  - `wrap` → 🔄 Retour à la ligne si nécessaire
  - `wrap-reverse` → 🔁 Retour à la ligne inversé
- `gap:` → 📏 Ajoute un espacement entre les éléments

---

## 🎭 Éléments flexibles

```css
.item {
  flex-grow: 1; /* 📈 Augmentation de taille */
  flex-shrink: 1; /* 📉 Réduction de taille */
  flex-basis: auto; /* 📏 Taille de base */
  align-self: auto; /* 🎯 Alignement individuel */
  order: 0; /* 🔢 Ordre d'affichage */
}
```

### 🔥 Propriétés des éléments

- `flex-grow:` → 📈 Définit la croissance relative de l'élément
  - `0` (par défaut) → 🚫 Ne grandit pas
  - `1` → 📦 Prend l'espace disponible
- `flex-shrink:` → 📉 Définit la réduction de l'élément
  - `1` (par défaut) → 📏 Peut rétrécir
  - `0` → 🚫 Ne rétrécit pas
- `flex-basis:` → 📏 Définit la taille initiale
  - `auto` (par défaut) → 🔄 Taille automatique
  - `100px`, `50%`, etc.
- `align-self:` 🎯 (Alignement individuel)
  - `auto` (par défaut) → Suit `align-items`
  - `flex-start`, `flex-end`, `center`, `stretch`, `baseline`
- `order:` → 🔢 Définit l'ordre d'affichage des éléments
  - `0` (par défaut)
  - Chiffre positif/négatif pour réorganiser l'ordre

---

## 🎨 Exemple complet

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.item {
  flex: 1 1 200px; /* 📦 flex-grow, flex-shrink, flex-basis */
  order: 2;
  align-self: flex-start;
}
```
## Image css flexbox  
<img src="../images/flexbox.webp"
---