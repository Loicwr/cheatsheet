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
