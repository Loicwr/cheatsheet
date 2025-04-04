# 🎉 CSS Grid - Le Guide Complet pour Démarrer

## Introduction

**CSS Grid Layout** est un système de mise en page 2D puissant qui permet de créer des designs complexes avec facilité. Contrairement aux autres systèmes comme Flexbox, CSS Grid te permet de contrôler à la fois les lignes et les colonnes, tout en offrant une grande flexibilité et adaptabilité pour des designs responsives.

Que tu sois débutant ou plus expérimenté, ce guide te mènera pas à pas pour comprendre et maîtriser **CSS Grid** de manière ludique et visuelle ! 😎

---

## 🧱 1. La Base : Créer une Grille

Tout commence par la définition d'un conteneur en grille. Pour ce faire, il suffit d’ajouter `display: grid` à ton élément.

```css
.container {
  display: grid;
}
```

### 🛠️ Que fait ce code ?

- **`display: grid;`** : Cela transforme l'élément en conteneur de grille, prêt à recevoir des éléments enfants qui seront placés dans un format de lignes et de colonnes.

---

## 📏 2. Définir des Colonnes et des Lignes

Une fois ton conteneur en grille, tu peux définir le nombre de colonnes et de lignes que tu veux utiliser.

### Colonnes :

```css
.container {
  grid-template-columns: 1fr 3fr;
}
```
Ce code crée **deux colonnes** : la première occupe 1 fraction de l'espace (1fr), et la deuxième 3 fractions de l'espace.

### Lignes :

```css
.container {
  grid-template-rows: auto auto 1fr;
}
```

Ici, on définit **trois lignes** : les deux premières s'ajustent à la taille de leur contenu (`auto`), et la troisième occupe l'espace restant (`1fr`).

---

## 🧩 3. Placer les Éléments dans la Grille

Tu as créé la grille, maintenant tu veux positionner les éléments à l'intérieur. C'est là que tu utilises `grid-column` et `grid-row`.

### Placer un élément dans une colonne et une ligne spécifiques :

```css
.main {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}
```

- **`grid-column: 2 / 3;`** : Cet élément commence à la colonne 2 et finit à la colonne 3.
- **`grid-row: 2 / 3;`** : L'élément commence à la ligne 2 et finit à la ligne 3.

### Tu peux aussi utiliser des `span` pour étendre un élément sur plusieurs lignes ou colonnes :

```css
.header {
  grid-column: span 2;
}
```

Cela fait en sorte que l'élément `.header` occupe **deux colonnes**.

---

## 🔄 4. Réagir aux Écrans Plus Petits (Responsive)

Une des grandes forces de CSS Grid est la capacité de s’adapter aux différentes tailles d’écran. En utilisant les **media queries**, tu peux redéfinir la structure de la grille sur les petits écrans.

### Exemple :

```css
@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
  }

  .sidebar, .main, .footer {
    grid-column: 1 / -1;
  }
}
```

- Ici, sur les petits écrans (moins de 768px de large), on passe à **une seule colonne** (1fr).
- Tous les éléments sont réorganisés en une **seule colonne** verticale pour s'adapter à l'écran.

---
