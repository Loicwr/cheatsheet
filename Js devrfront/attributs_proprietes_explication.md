
# 🧱 Comprendre les Attributs / Propriétés en JavaScript (POO)

## 📌 Définition générale

En JavaScript, un **attribut** (ou **propriété**) est une **valeur associée à un objet**.  
C’est une donnée qui décrit une **caractéristique** de l’objet.

Dans la **Programmation Orientée Objet (POO)**, les objets ont des propriétés pour stocker leur état.

---

## 🧠 Terme : Attribut ou Propriété ?

- En JavaScript, le terme **propriété** est utilisé.
- En POO (tous langages confondus), on parle souvent **d’attributs**.
- Dans le contexte JavaScript, ces deux termes sont **équivalents**.

---

## 🏗️ Comment sont créées les propriétés ?

Les propriétés sont souvent définies dans le **constructeur** d’une classe avec `this`.

### Exemple :

```javascript
class Utilisateur {
  constructor(prenom, age) {
    this.prenom = prenom; // propriété prénom
    this.age = age;       // propriété age
  }
}
```

- `this.prenom = prenom` crée une propriété `prenom` attachée à l’objet.
- `this` fait référence à l’objet courant.

---

## 🔍 Accéder et modifier les propriétés

Une fois qu’un objet est créé, on peut accéder ou modifier ses propriétés avec la notation pointée `objet.propriete`.

```javascript
const user1 = new Utilisateur("Léa", 25);

console.log(user1.prenom); // "Léa"
console.log(user1.age);    // 25

user1.age = 26;
console.log(user1.age);    // 26
```

---

## 📦 Propriétés publiques vs privées (ES2022+)

Par défaut, toutes les propriétés sont **publiques** en JavaScript, ce qui signifie qu’elles peuvent être lues ou modifiées de l’extérieur de l’objet.

Depuis ES2022, on peut créer des **propriétés privées** avec un `#` devant leur nom :

```javascript
class Secret {
  #motDePasse;

  constructor(mdp) {
    this.#motDePasse = mdp;
  }

  afficher() {
    console.log("Le mot de passe est confidentiel.");
  }
}

const s = new Secret("1234");
s.afficher();              // OK
console.log(s.#motDePasse); // ❌ Erreur : propriété privée
```

---

## 🧠 Récapitulatif

| Élément                    | Description |
|----------------------------|-------------|
| Propriété (ou attribut)    | Donnée attachée à un objet |
| `this.nom = valeur`        | Création d'une propriété dans un constructeur |
| `objet.propriete`          | Accès à une propriété |
| Propriétés publiques       | Accessibles de l’extérieur |
| Propriétés privées (`#`)   | Accessibles uniquement dans la classe |

---

## ✅ Bonnes pratiques

- Toujours initialiser les propriétés dans le `constructor`.
- Utiliser des noms clairs pour les propriétés (`nom`, `email`, `age`, etc.).
- Utiliser `#` pour cacher les données sensibles si nécessaire.

