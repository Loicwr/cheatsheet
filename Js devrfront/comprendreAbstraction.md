## Lundi 26 / 05 / 2025

## Est-ce que JS est un langage Orienté Objet ?

JavaScript est bel et bien un langage orienté objet, bien qu'il adopte une approche unique . Son héritage prototypique, combiné à la syntaxe de classe ES6 moderne, prend en charge les principes fondamentaux de la programmation orientée objet tels que l'encapsulation, l'héritage, le polymorphisme et l'abstraction

## Comprendre ce qu'est l'abstraction.

#### 📘 Définition simple :
L’abstraction, c’est le fait de masquer les détails complexes d’un système pour ne montrer que ce qui est essentiel à l’utilisateur.

C’est comme utiliser un smartphone : tu vois l’écran, les boutons, les apps — mais tu ne sais pas (et tu n’as pas besoin de savoir) comment le processeur, la mémoire ou le système d’exploitation fonctionnent en interne.

#### 🧠 Objectif de l’abstraction en POO :
Cacher les détails internes (implémentation)

Offrir une interface simple (méthodes publiques)

Éviter les erreurs de manipulation

Rendre le code plus clair et maintenable

#### 🛠️ Exemple en JavaScript :

class MachineACafe {
  constructor() {
    this._eau = 100; // % d'eau
  }

  faireUnCafe() {
    if (this._eau >= 20) {
      console.log("Voici votre café ☕");
      this._eau -= 20;
    } else {
      console.log("Pas assez d'eau !");
    }
  }
}

#### ✅ Que voit l’utilisateur ?

const machine = new MachineACafe();
machine.faireUnCafe(); // ☕

#### ❌ Que ne voit-il pas ?
La gestion interne du niveau d’eau

Comment le café est "préparé"

Quelle logique est derrière faireUnCafe()

####  Pourquoi c’est utile ?
L’utilisateur n’a pas besoin de connaître la complexité.

Le développeur peut modifier l’intérieur sans casser l’usage.

Le code est plus lisible et modulaire.

#### 💬 Métaphore concrète :
Imagine une voiture :
Tu tournes la clé ou appuies sur un bouton pour démarrer.
Tu n’as pas besoin de savoir comment fonctionne le moteur, l’injection, l’allumage, etc.
Tu interagis avec une interface simple (volant, pédales, boutons).

C’est ça l’abstraction.

#### 🆚 À ne pas confondre avec :
Concept	Ce que c’est
Abstraction	Cacher la complexité pour ne montrer que l’essentiel
Encapsulation	Cacher les données internes (sécurité + protection)
Héritage	Réutiliser les propriétés/méthodes d’une autre classe
Polymorphisme	Un même comportement adapté à des objets différents
