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