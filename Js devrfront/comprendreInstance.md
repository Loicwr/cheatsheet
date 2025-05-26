## Lundi 26 / 05 / 2025

##  Comprendre le principe d'instance.

#### 📘 Définition :
Une instance, c’est un objet concret créé à partir d’une classe.

La classe est comme un plan, un modèle, une recette.
L’instance est l’objet réel que tu crées en utilisant ce modèle.

#### 🛠️ Exemple en JavaScript :

class Voiture {
  constructor(marque) {
    this.marque = marque;
  }

  klaxonner() {
    console.log(`${this.marque} fait : Bip bip !`);
  }
}

// Création d'instances :
const v1 = new Voiture("Toyota");
const v2 = new Voiture("Tesla");

#### 🔍 Ici :

Voiture est une classe

v1 et v2 sont des instances de la classe Voiture

Chaque instance a ses propres données (marque) et peut utiliser les méthodes de la classe

#### 🧠 Comment ça fonctionne ?
Quand on écrit :

js
Copier
Modifier
const v1 = new Voiture("Toyota");
new Voiture(...) appelle le constructeur de la classe.

Une nouvelle instance (objet) est créée automatiquement.

Le mot-clé this dans le constructeur pointe vers cet objet.

Les propriétés (comme marque) sont attachées à l’instance, pas à la classe elle-même.

#### 📌 Caractéristiques d’une instance :
Élément	Exemple dans le code
Classe	Voiture
Instance	v1 ou v2
Création	new Voiture("Tesla")
Accès aux attributs	v1.marque
Accès aux méthodes	v1.klaxonner()

#### 🧩 Résumé visuel :

Classe :         Voiture
                  │
       ┌──────────┴──────────┐
       ↓                     ↓
  Instance : v1         Instance : v2
  { marque: "Toyota" }  { marque: "Tesla" }
