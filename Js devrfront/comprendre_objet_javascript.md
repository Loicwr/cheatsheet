
# 🧱 Comprendre ce qu’est un objet en JavaScript

## 📌 Définition

En JavaScript, un **objet** est une **structure de données** qui permet de **regrouper des informations** (valeurs) sous forme de paires **clé/valeur**.

Un objet représente **une entité du monde réel** avec :
- des **propriétés** (attributs, données)
- des **méthodes** (comportements, fonctions)

---

## 📦 Exemple simple

```javascript
const voiture = {
  marque: "Toyota",
  modele: "Corolla",
  annee: 2020,
  demarrer: function() {
    console.log("La voiture démarre.");
  }
};

console.log(voiture.marque); // "Toyota"
voiture.demarrer();          // "La voiture démarre."
```

- `marque`, `modele`, `annee` sont des **propriétés**
- `demarrer` est une **méthode**

---

## 🧠 Syntaxe d’un objet

```javascript
const monObjet = {
  cle1: valeur1,
  cle2: valeur2,
  cle3: function() {
    // code
  }
};
```

---

## 🎯 Pourquoi utiliser des objets ?

- Pour **organiser les données** liées entre elles
- Pour **modéliser des éléments** du monde réel (ex : une personne, une voiture, un produit)
- Pour **encapsuler des comportements** dans des méthodes

---

## 🛠️ Accès aux données

### Avec la notation pointée :
```javascript
console.log(voiture.modele); // "Corolla"
```

### Ou la notation entre crochets :
```javascript
console.log(voiture["modele"]); // "Corolla"
```

---

## 🔄 Modification et ajout de propriétés

```javascript
voiture.couleur = "rouge";          // ajout
voiture.annee = 2021;               // modification
```

---

## 🧱 Objet vs Classe

- Une **classe** est un **modèle** (comme un plan de construction)
- Un **objet** est une **instance concrète** créée à partir de cette classe

```javascript
class Animal {
  constructor(nom) {
    this.nom = nom;
  }
}

const chat = new Animal("Minou"); // objet "chat" à partir de la classe "Animal"
```

---

## ✅ Résumé

| Terme        | Signification |
|--------------|----------------|
| Objet        | Structure contenant des données et des comportements |
| Propriétés   | Données stockées dans l’objet |
| Méthodes     | Fonctions associées à l’objet |
| Accès        | `objet.propriete` ou `objet["propriete"]` |
| Classe       | Modèle pour créer des objets |

---

Les objets sont **au cœur de JavaScript** et de la programmation orientée objet.
