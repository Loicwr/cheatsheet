## ## Lundi 26 / 05 / 2025

##  Qu’est-ce qu’une classe ?

#### 📘 Définition simple :
Une classe est un modèle (ou plan de construction) qui permet de créer des objets avec les mêmes propriétés et comportements.

Elle décrit ce qu’un objet sait faire (ses méthodes) et ce qu’il possède (ses attributs).

#### 📦 Métaphore concrète :
Imagine une classe comme un plan de fabrication de voitures.
Chaque voiture construite à partir de ce plan est une instance.

La classe Voiture définit :

des attributs : marque, couleur, vitesse

des méthodes : démarrer(), freiner(), klaxonner()

#### 🛠️ En JavaScript : Comment on crée une classe ?
class Voiture {
  constructor(marque, couleur) {
    this.marque = marque;
    this.couleur = couleur;
  }

  demarrer() {
    console.log(`${this.marque} démarre.`);
  }
}

#### 🧪 Exemple d’utilisation (instances) :

const v1 = new Voiture("Toyota", "rouge");
const v2 = new Voiture("Tesla", "noire");

v1.demarrer(); // Toyota démarre.
v2.demarrer(); // Tesla démarre.

#### 📌 Une classe contient généralement :
Élément	Rôle
constructor()	Fonction spéciale qui initialise l'objet
Attributs	Les données propres à chaque instance (this.nom)
Méthodes	Les fonctions que l’objet peut exécuter

#### 📌 Classe vs Objet
Terme	Définition
Classe	Le plan / modèle (défini avec class)
Objet	Une instance concrète créée à partir de la classe

#### 🧩 Résumé visuel :

class Chien
  ├── Propriété : nom
  └── Méthode : aboyer()

↓   (new)
Objet (instance) : new Chien("Rex")
  ├── nom = "Rex"
  └── peut appeler aboyer()
