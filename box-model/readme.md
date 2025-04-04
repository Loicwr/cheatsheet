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
