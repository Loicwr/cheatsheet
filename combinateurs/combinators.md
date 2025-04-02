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