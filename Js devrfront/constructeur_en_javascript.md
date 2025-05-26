
# Comprendre le constructeur (`constructor`) en JavaScript

## 🏗️ Qu’est-ce qu’un constructeur ?

Un **constructeur** est une méthode spéciale utilisée dans une **classe** en Programmation Orientée Objet (POO).  
Il est automatiquement appelé lorsqu’un **nouvel objet** est créé avec le mot-clé `new`.

### 🎯 Rôle principal
Initialiser les **propriétés** (attributs) d’un objet.

## 🔧 Exemple simple

```javascript
class Personne {
  constructor(nom, age) {
    this.nom = nom;
    this.age = age;
  }

  sePresenter() {
    console.log(`Bonjour, je m'appelle ${this.nom} et j'ai ${this.age} ans.`);
  }
}

// Création d'une instance
const p1 = new Personne("Alice", 30);
p1.sePresenter(); // Bonjour, je m'appelle Alice et j'ai 30 ans.
```

## 🧠 Détails importants

| Élément             | Explication |
|---------------------|-------------|
| `constructor(...)`  | mot-clé pour déclarer le constructeur |
| `this.nom = nom`    | affecte la valeur reçue à une propriété de l'objet |
| `this`              | représente l’instance courante de la classe |
| Appelé automatiquement ? | ✅ Oui, avec `new` |

## 💥 Si tu n’écris pas de constructeur ?

```javascript
class Voiture {}

const v = new Voiture(); // OK, pas d'erreur
```

JavaScript crée un constructeur vide par défaut.  
Mais pour initialiser des valeurs personnalisées, tu dois déclarer le tien.

## 🎯 Résumé

- Le constructeur initialise les propriétés d’un objet.
- Il est appelé automatiquement avec `new`.
- Une seule méthode `constructor` par classe.
- Il peut recevoir des paramètres.
