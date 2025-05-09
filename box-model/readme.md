# 📦 Comprendre le Box Model en CSS

Le **Box Model** (ou modèle de boîte) est un concept fondamental en CSS. Il décrit la manière dont les éléments HTML sont modélisés et affichés sur une page web. Chaque élément est considéré comme une boîte rectangulaire, composée de plusieurs couches.

## 🧱 Structure du Box Model

Voici les **quatre** couches principales du Box Model :

```
+-----------------------------+
|        Margin (extérieur)   |
|  +------------------------+ |
|  |     Border (bordure)   | |
|  |  +-------------------+ | |
|  |  | Padding (espace)  | | |
|  |  | +---------------+ | | |
|  |  | | Content       | | | |
|  |  | +---------------+ | | |
|  |  +-------------------+ | |
|  +------------------------+ |
+-----------------------------+
```

### 1. `Content`
- C'est le contenu réel de l'élément (texte, image, etc.).
- Ses dimensions sont définies via `width` et `height`.

### 2. `Padding`
- Espace **interne** entre le contenu et la bordure.
- Sert à **créer de l'espace** autour du contenu, à l'intérieur de l'élément.

### 3. `Border`
- Bordure **entourant** le padding et le contenu.
- Peut être de différentes **épaisseurs**, **styles**, et **couleurs** (`solid`, `dashed`, etc.).

### 4. `Margin`
- Espace **externe** autour de l'élément.
- Sert à **séparer** les éléments les uns des autres.

---

## 🧮 Calcul de la taille totale d’un élément

Par défaut, la taille totale d’un élément est :

```
Largeur totale = margin + border + padding + width
Hauteur totale = margin + border + padding + height
```

Exemple :

```css
div {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
}
```

- Largeur totale = 200 + 20*2 + 5*2 = **250px**
- Hauteur totale = dépend de `height`, calcul similaire

---

## 🛠️ `box-sizing` : maîtriser le Box Model

Le comportement par défaut peut être modifié avec `box-sizing`.

### ✅ `content-box` (par défaut)
- `width` et `height` ne prennent en compte que le **contenu**.
- Padding et border s’ajoutent **en plus**.

### ✅ `border-box`
- `width` et `height` incluent **le padding et la bordure**.
- Plus facile pour des mises en page précises.

```css
* {
  box-sizing: border-box;
}
```

---

## 🎯 Exemple pratique

```html
<div class="box">Hello!</div>
```

```css
.box {
  width: 300px;
  padding: 20px;
  border: 5px solid #333;
  margin: 30px;
  box-sizing: border-box;
}
```

Avec `border-box`, la largeur **totale** reste **300px**.

---

## 📚 Ressources complémentaires

- [MDN Web Docs - Box Model](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_box_model)
- [CSS-Tricks Guide to Box Model](https://css-tricks.com/the-css-box-model/)

<img src="../images/css-box-model.svg">