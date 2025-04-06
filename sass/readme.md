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