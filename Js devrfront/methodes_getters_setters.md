
# ⚙️ Méthodes en JavaScript (POO)

## 📌 Définition

Une **méthode** est une **fonction attachée à un objet ou une classe**.  
Dans le contexte des classes JavaScript (POO), une méthode définit un **comportement** de l’objet.

---

## 🧠 Méthode vs Fonction

| Fonction                      | Méthode                          |
|------------------------------|----------------------------------|
| Définie **en dehors** d’un objet | Définie **dans** une classe ou un objet |
| Appelée seule                | Appelée **via un objet** |
| `function direBonjour() {}`  | `personne.direBonjour()` |

### Exemple :

```javascript
// Fonction
function direBonjour() {
  console.log("Bonjour !");
}
direBonjour();

// Méthode dans une classe
class Personne {
  direBonjour() {
    console.log("Bonjour, je suis une personne.");
  }
}
const p = new Personne();
p.direBonjour(); // Méthode appelée via l'objet
```

---

## 🎯 Utilité des méthodes

Les méthodes permettent :
- D’**ajouter des comportements** à une classe (ex. : marcher, parler, afficher)
- D’**interagir avec les données** internes de l’objet
- De **structurer le code** avec clarté et modularité

---

## 🛠️ Exemple de méthode dans une classe

```javascript
class CompteBancaire {
  constructor(titulaire, solde) {
    this.titulaire = titulaire;
    this.solde = solde;
  }

  deposer(montant) {
    this.solde += montant;
  }

  afficherSolde() {
    console.log(`Solde de ${this.titulaire} : ${this.solde}€`);
  }
}

const compte = new CompteBancaire("Alice", 100);
compte.deposer(50);
compte.afficherSolde(); // Solde de Alice : 150€
```

---

## 🪟 Getters / Setters

### 🎯 À quoi ça sert ?

Les **getters** et **setters** permettent de **contrôler l'accès** aux propriétés d’un objet :
- **Getter** : lire une propriété via une méthode déguisée
- **Setter** : modifier une propriété avec validation ou logique

---

### 🧪 Exemple avec getter/setter

```javascript
class Article {
  constructor(nom, prix) {
    this._nom = nom;
    this._prix = prix;
  }

  get prix() {
    return this._prix + "€";
  }

  set prix(nouveauPrix) {
    if (nouveauPrix > 0) {
      this._prix = nouveauPrix;
    } else {
      console.log("Prix invalide !");
    }
  }
}

const a = new Article("Chaise", 30);
console.log(a.prix); // 30€

a.prix = -10;        // Prix invalide !
a.prix = 45;
console.log(a.prix); // 45€
```

🔐 Remarque : on utilise souvent un nom avec `_` (comme `_prix`) pour différencier la propriété interne du getter/setter.

---

## ✅ Résumé

| Concept       | Description |
|---------------|-------------|
| Méthode       | Fonction dans une classe |
| Fonction      | Fonction globale ou indépendante |
| Getter        | Accès contrôlé en lecture |
| Setter        | Accès contrôlé en écriture |
| Utilité       | Structurer et encapsuler le comportement des objets |

