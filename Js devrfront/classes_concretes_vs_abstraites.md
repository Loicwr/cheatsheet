
# 🧠 POO : Classes concrètes vs Classes abstraites (JavaScript)

## 🔷 Qu’est-ce qu’une classe concrète ?

> Une **classe concrète** est une classe normale : tu peux créer des **instances directement** à partir d’elle.

### ✅ Exemple :

```js
class Voiture {
  constructor(marque) {
    this.marque = marque;
  }

  rouler() {
    console.log(`${this.marque} roule !`);
  }
}

const v = new Voiture("Toyota"); // ✅ Ça fonctionne
v.rouler(); // Toyota roule !
```

---

## 🧩 Qu’est-ce qu’une classe abstraite ?

> Une **classe abstraite** est une **classe modèle** qu’on **ne peut pas instancier directement**.  
> Elle est **conçue pour être étendue** par d'autres classes.

### ⚠️ JavaScript ne supporte pas directement les classes abstraites, mais on peut les simuler :

```js
class Animal {
  constructor(nom) {
    if (this.constructor === Animal) {
      throw new Error("Classe abstraite, on ne peut pas instancier directement.");
    }
    this.nom = nom;
  }

  parler() {
    throw new Error("Méthode abstraite 'parler()' non implémentée !");
  }
}
```

### ❌ Si on essaie ceci :

```js
const a = new Animal("Toto"); // Erreur !
```

---

## ✅ Exemple de classe concrète qui hérite :

```js
class Chien extends Animal {
  parler() {
    console.log(`${this.nom} aboie`);
  }
}

const rex = new Chien("Rex");
rex.parler(); // Rex aboie
```

---

## ⚖️ Comparatif

| Type de classe     | Peut être instanciée ? | Contient des méthodes complètes ? | Utilisée pour ?                          |
|--------------------|------------------------|------------------------------------|------------------------------------------|
| **Classe concrète** | ✅ Oui                 | ✅ Oui                             | Créer directement des objets             |
| **Classe abstraite** | ❌ Non                | 🟡 Pas forcément                   | Fournir une structure de base à d'autres classes |

---

## 🎯 Pourquoi utiliser des classes abstraites ?

- 🔒 **Encourager la cohérence** dans les classes dérivées
- 🧱 **Partager une base commune** entre plusieurs classes enfants
- ⚙️ **Forcer l'implémentation de certaines méthodes**
