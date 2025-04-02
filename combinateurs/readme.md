# 🌈 Combinateurs CSS

## 1️⃣ Combinateur descendant (espace)

🔹 **Le combinateur descendant** sélectionne tous les éléments qui sont à l’intérieur d’un autre élément, peu importe leur niveau de profondeur.

### ✨ Exemple :

```css
div p {
  color: red;
}
```

### 🏗️ HTML :

```html
<div>
  <p>Ce texte sera rouge.</p>
  <div>
    <p>Ce texte sera aussi rouge.</p>
    <div>
      <p>Ce texte sera également rouge.</p>
    </div>
  </div>
</div>
```

### 🎨 Schéma :

```html
<div>
  <p>🔴 rouge</p>          <-- Sélectionné
  <div>
    <p>🔴 rouge</p>        <-- Sélectionné
    <div>
      <p>🔴 rouge</p>      <-- Sélectionné
    </div>
  </div>
</div>
```

---

## 2️⃣ Combinateur enfant direct (`>`) 🔵

🔹 **Le combinateur enfant direct** sélectionne uniquement les éléments qui sont des enfants directs de l'élément parent spécifié.

### ✨ Exemple :

```css
div > p {
  color: blue;
}
```

### 🏗️ HTML :

```html
<div>
  <p>Ce texte sera bleu (enfant direct du div).</p>
  <div>
    <p>Ce texte ne sera pas bleu (il est à l'intérieur d'un autre div).</p>
  </div>
</div>
```

### 🎨 Schéma :

```html
<div>
  <p>🔵 bleu</p>            <-- Sélectionné, enfant direct
  <div>
    <p>⚪ non bleu</p>      <-- NON sélectionné, pas enfant direct
  </div>
</div>
```

---

## 3️⃣ Combinateur frère suivant (`+`) 🟢

🔹 **Le combinateur frère suivant** sélectionne l'élément qui suit immédiatement un autre élément dans le même niveau hiérarchique (frère immédiat).

### ✨ Exemple :

```css
h1 + p {
  color: green;
}
```

### 🏗️ HTML :

```html
<h1>Titre 1</h1>
<p>Ce texte sera vert, car il suit immédiatement le <h1>.</p>
<p>Ce texte ne sera pas vert, car il ne suit pas immédiatement un <h1>.</p>
<h1>Titre 2</h1>
<p>Ce texte sera vert, car il suit immédiatement un <h1>.</p>
```

### 🎨 Schéma :

```html
<h1>Titre 1</h1>
<p>🟢 vert</p>               <-- Sélectionné, frère suivant immédiat
<p>⚪ non vert</p>           <-- NON sélectionné, pas frère immédiat

<h1>Titre 2</h1>
<p>🟢 vert</p>               <-- Sélectionné, frère suivant immédiat
```

---


## 4️⃣ Combinateur frère général (`~`) 🟣

🔹 **Le combinateur frère général** sélectionne tous les éléments qui suivent un autre élément, peu importe qu’il y ait d’autres éléments entre eux.

### ✨ Exemple :

```css
h1 ~ p {
  color: purple;
}
```

### 🏗️ HTML :

```html
<h1>Titre 1</h1>
<p>Ce texte sera violet, car il suit un <h1>.</p>
<span>Un autre élément non <p></span>
<p>Ce texte aussi sera violet, car il suit un <h1>.</p>
<h1>Titre 2</h1>
<p>Ce texte sera aussi violet, car il suit un <h1>.</p>
```

### 🎨 Schéma :

```html
<h1>Titre 1</h1>
<p>🟣 violet</p>               <-- Sélectionné, suit un <h1>
<span>⚪ autre élément</span>  <-- NON sélectionné, pas un <p>
<p>🟣 violet</p>               <-- Sélectionné, suit un <h1>

<h1>Titre 2</h1>
<p>🟣 violet</p>               <-- Sélectionné, suit un <h1>
```

---

## 🔥 Récapitulatif visuel des combinateurs

| 🏷️ Combinateur          | 🎨 Exemple CSS             | 🎯 Sélectionne |
|----------------------|--------------------------|-------------|
| **Descendant (` `)**  | `div p { color: red; }`  | 🔴 Tous les `<p>` à l'intérieur d'un `<div>` |
| **Enfant direct (`>`)** | `div > p { color: blue; }` | 🔵 Seulement les `<p>` qui sont enfants directs d'un `<div>` |
| **Frère suivant (`+`)** | `h1 + p { color: green; }` | 🟢 Le premier `<p>` qui suit immédiatement un `<h1>` |
| **Frère général (`~`)** | `h1 ~ p { color: purple; }` | 🟣 Tous les `<p>` qui suivent un `<h1>`, même s'il y a d'autres éléments entre eux |
