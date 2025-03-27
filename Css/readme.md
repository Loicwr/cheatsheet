# 🎨 **Découvrir le CSS**

---

## 🔹 1️⃣ Comprendre la syntaxe de base
Le CSS (*Cascading Style Sheets*) est utilisé pour styliser les pages HTML. Il se compose de **sélecteurs** et de **règles**.

```css
h1 {
    color: blue;
    font-size: 24px;
}
```
✅ `h1` : **Sélecteur** ciblant la balise `<h1>`  
✅ `{}` : Contient les **déclarations de style**  
✅ `color: blue;` : Définit la **couleur du texte**  
✅ `font-size: 24px;` : Définit la **taille du texte**  
# 🎨 **Découvrir le CSS**

---

## 🔹 1️⃣ Comprendre la syntaxe de base
Le CSS (*Cascading Style Sheets*) est utilisé pour styliser les pages HTML. Il se compose de **sélecteurs** et de **règles**.

```css
h1 {
    color: blue;
    font-size: 24px;
}
```
✅ `h1` : **Sélecteur** ciblant la balise `<h1>`  
✅ `{}` : Contient les **déclarations de style**  
✅ `color: blue;` : Définit la **couleur du texte**  
✅ `font-size: 24px;` : Définit la **taille du texte**  

---

## 🔹 2️⃣ Savoir insérer du CSS de différentes manières
Il existe **quatre façons** d’intégrer du CSS :

### 🟢 CSS en ligne *(inline CSS)*
```html
<p style="color: red; font-size: 18px;">Texte en rouge</p>
```

### 🔵 CSS en interne *(internal CSS)*
```html
<style>
    p {
        color: green;
        font-size: 20px;
    }
</style>
```

### 🟣 CSS externe *(external CSS)*
```html
<link rel="stylesheet" href="styles.css">
```
Dans `styles.css` :
```css
p {
    color: blue;
    font-size: 22px;
}
```

### 🔴 CSS via un préprocesseur *(SASS, LESS)*
```scss
$main-color: blue;
p {
    color: $main-color;
}
```

---

## 🔹 3️⃣ Comprendre les sélecteurs CSS
### 🎯 **Principaux types :**

- **🟠 Classes (`.`)** : Applique un style à plusieurs éléments.
  ```css
  .important { font-weight: bold; color: red; }
  ```

- **🟢 IDs (`#`)** : Applique un style unique.
  ```css
  #titre { font-size: 30px; color: blue; }
  ```

- **🔵 Éléments** : Applique un style aux balises HTML.
  ```css
  p { text-align: center; }
  ```

- **🟣 Sélecteur universel (`*`)** : Applique à tous les éléments.
  ```css
  * { margin: 0; padding: 0; }
  ```

- **🟡 Pseudo-classes (`:`)** : S’appliquent dans un état spécifique.
  ```css
  a:hover { color: green; }
  ```

- **🟠 Pseudo-éléments (`::`)** : Ciblent une partie d’un élément.
  ```css
  p::first-letter { font-size: 30px; color: red; }
  ```

---

## 🔹 4️⃣ Savoir appliquer une mise en forme
```css
h1 {
    color: blue;
    font-family: Arial, sans-serif;
    text-align: center;
}

div {
    width: 300px;
    height: 200px;
    background-color: lightgray;
    border: 2px solid black;
}
```

---

## 🔹 5️⃣ Comprendre le Box Model 📦
Le modèle de boîte CSS est structuré ainsi :
✅ **Content** → Contenu de l'élément  
✅ **Padding** → Espace autour du contenu  
✅ **Border** → Bordure de l’élément  
✅ **Margin** → Espace entre l’élément et les autres éléments  

```css
div {
    width: 200px;
    height: 100px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

---

## 🔹 6️⃣ Découvrir le positionnement en CSS 📍

### ✨ **Valeurs de `position` :**
- **🟢 Static** *(par défaut)* : suit le flux normal.
- **🔵 Relative** : positionné par rapport à sa position initiale.
- **🟣 Absolute** : positionné par rapport à son parent positionné.
- **🟠 Fixed** : reste fixe même en scrollant.
- **🟡 Sticky** : devient fixe lors du scroll.

```css
div {
    position: absolute;
    top: 50px;
    left: 100px;
}
```

---

## 🔹 7️⃣ Comprendre la spécificité CSS ⚖️
### 📊 **Priorité des styles CSS :**
1️⃣ `!important` (**le plus fort**)  
2️⃣ Style **inline** (`style=""`)  
3️⃣ **ID** (`#monID`)  
4️⃣ **Classes** (`.maClasse`), **pseudo-classes**, et **attributs**  
5️⃣ **Sélecteurs d’éléments** (`p`, `h1`)  
6️⃣ **Sélecteur universel** (`*`)  

```css
p {
    color: blue;
}
p.special {
    color: red;
}
#unique {
    color: green;
}
```
🎯 Si un `<p>` a la classe `special` et l’ID `unique`, il sera **vert** car l’ID est prioritaire.

---

## 🚀 **Conclusion**
Tu as maintenant une bonne base en CSS ! 🎨  
Si tu veux approfondir un point, n'hésite pas à explorer davantage ! 🚀

---

## 🔹 2️⃣ Savoir insérer du CSS de différentes manières
Il existe **quatre façons** d’intégrer du CSS :

### 🟢 CSS en ligne *(inline CSS)*
```html
<p style="color: red; font-size: 18px;">Texte en rouge</p>
```

### 🔵 CSS en interne *(internal CSS)*
```html
<style>
    p {
        color: green;
        font-size: 20px;
    }
</style>
```

### 🟣 CSS externe *(external CSS)*
```html
<link rel="stylesheet" href="styles.css">
```
Dans `styles.css` :
```css
p {
    color: blue;
    font-size: 22px;
}
```

### 🔴 CSS via un préprocesseur *(SASS, LESS)*
```scss
$main-color: blue;
p {
    color: $main-color;
}
```

---

## 🔹 3️⃣ Comprendre les sélecteurs CSS
### 🎯 **Principaux types :**

- **🟠 Classes (`.`)** : Applique un style à plusieurs éléments.
  ```css
  .important { font-weight: bold; color: red; }
  ```

- **🟢 IDs (`#`)** : Applique un style unique.
  ```css
  #titre { font-size: 30px; color: blue; }
  ```

- **🔵 Éléments** : Applique un style aux balises HTML.
  ```css
  p { text-align: center; }
  ```

- **🟣 Sélecteur universel (`*`)** : Applique à tous les éléments.
  ```css
  * { margin: 0; padding: 0; }
  ```

- **🟡 Pseudo-classes (`:`)** : S’appliquent dans un état spécifique.
  ```css
  a:hover { color: green; }
  ```

- **🟠 Pseudo-éléments (`::`)** : Ciblent une partie d’un élément.
  ```css
  p::first-letter { font-size: 30px; color: red; }
  ```

---

## 🔹 4️⃣ Savoir appliquer une mise en forme
```css
h1 {
    color: blue;
    font-family: Arial, sans-serif;
    text-align: center;
}

div {
    width: 300px;
    height: 200px;
    background-color: lightgray;
    border: 2px solid black;
}
```

---

## 🔹 5️⃣ Comprendre le Box Model 📦
Le modèle de boîte CSS est structuré ainsi :
✅ **Content** → Contenu de l'élément  
✅ **Padding** → Espace autour du contenu  
✅ **Border** → Bordure de l’élément  
✅ **Margin** → Espace entre l’élément et les autres éléments  

```css
div {
    width: 200px;
    height: 100px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

---

## 🔹 6️⃣ Découvrir le positionnement en CSS 📍

### ✨ **Valeurs de `position` :**
- **🟢 Static** *(par défaut)* : suit le flux normal.
- **🔵 Relative** : positionné par rapport à sa position initiale.
- **🟣 Absolute** : positionné par rapport à son parent positionné.
- **🟠 Fixed** : reste fixe même en scrollant.
- **🟡 Sticky** : devient fixe lors du scroll.

```css
div {
    position: absolute;
    top: 50px;
    left: 100px;
}
```

---

## 🔹 7️⃣ Comprendre la spécificité CSS ⚖️
### 📊 **Priorité des styles CSS :**
1️⃣ `!important` (**le plus fort**)  
2️⃣ Style **inline** (`style=""`)  
3️⃣ **ID** (`#monID`)  
4️⃣ **Classes** (`.maClasse`), **pseudo-classes**, et **attributs**  
5️⃣ **Sélecteurs d’éléments** (`p`, `h1`)  
6️⃣ **Sélecteur universel** (`*`)  

```css
p {
    color: blue;
}
p.special {
    color: red;
}
#unique {
    color: green;
}
```
🎯 Si un `<p>` a la classe `special` et l’ID `unique`, il sera **vert** car l’ID est prioritaire.