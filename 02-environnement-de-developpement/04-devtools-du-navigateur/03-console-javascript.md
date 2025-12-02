🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.4.3 Console JavaScript : votre meilleur ami

## Introduction

La **Console JavaScript** est l'outil le plus important pour débugger et tester votre code JavaScript. C'est votre **ligne de communication directe** avec le navigateur : vous lui parlez, il vous répond.

> 💡 **Analogie** : Si votre site web est un restaurant, la Console est comme la cuisine avec un chef qui vous dit : "Le plat est prêt !" ou "Attention, le four est en panne !". C'est là que vous voyez ce qui se passe en coulisses.

La Console vous permet de :
- 📝 Afficher des messages depuis votre code JavaScript (`console.log()`)
- ⚠️ Voir les erreurs JavaScript
- 🧪 Tester du code JavaScript rapidement
- 🔍 Débugger votre code étape par étape
- 📊 Inspecter les valeurs de vos variables

**Important :** La Console est votre **meilleur ami** en tant que développeur JavaScript. Vous l'utiliserez constamment, tous les jours !

---

## Ouvrir la Console

### Méthode 1 : Raccourcis clavier (⚡ Le plus rapide)

| Système | Raccourci |
|---------|-----------|
| **Windows / Linux** | `Ctrl + Shift + J` |
| **Mac** | `Cmd + Option + J` |

**Astuce :** Ce raccourci ouvre **directement** la Console, sans passer par d'autres onglets.

---

### Méthode 2 : Depuis les DevTools

Si les DevTools sont déjà ouverts (`F12`) :
1. Cliquez sur l'onglet **"Console"**

**Ou via le tiroir inférieur :**
- Appuyez sur `Esc` dans n'importe quel onglet des DevTools
- La Console apparaît en bas (pratique pour avoir Elements + Console en même temps)

---

### Méthode 3 : Clic droit sur une erreur

Si vous voyez une icône d'erreur ❌ en haut à droite de la page :
1. Cliquez dessus
2. Cela ouvre les DevTools directement sur la Console avec l'erreur affichée

---

## Interface de la Console

### Vue d'ensemble

```
┌──────────────────────────────────────────────────────┐
│ Console                                 Clear  ⚙️    │
├──────────────────────────────────────────────────────┤
│ All levels  ▼  |  Default  ▼  |  🔍 Filter           │
├──────────────────────────────────────────────────────┤
│                                                      │
│ > console.log("Hello World")                         │
│ Hello World                                          │
│                                                      │
│ ⚠ Warning: This is a warning message                 │
│                                                      │
│ ❌ Uncaught ReferenceError: x is not defined         │
│     at script.js:10                                  │
│                                                      │
├──────────────────────────────────────────────────────┤
│ >  |  ← Zone de saisie (tapez votre code ici)        │
└──────────────────────────────────────────────────────┘
```

**Zones principales :**

1. **Barre d'outils** : Filtres, options, bouton Clear
2. **Zone d'affichage** : Messages, erreurs, résultats
3. **Zone de saisie** (en bas) : Tapez votre code JavaScript ici

---

## Types de messages

La Console affiche différents types de messages avec des icônes et couleurs distinctes :

### 1. Messages normaux (console.log)

```javascript
console.log("Hello World");
```

**Affichage :**
```
> Hello World
```

**Couleur :** Noir (thème clair) ou Blanc (thème sombre)
**Icône :** Aucune (ou ℹ️ dans certains navigateurs)

---

### 2. Avertissements (console.warn)

```javascript
console.warn("Attention : Cette fonctionnalité est dépréciée");
```

**Affichage :**
```
⚠️ Attention : Cette fonctionnalité est dépréciée
```

**Couleur :** Jaune/Orange
**Icône :** ⚠️ Triangle d'avertissement

---

### 3. Erreurs (console.error)

```javascript
console.error("Erreur : Impossible de charger les données");
```

**Affichage :**
```
❌ Erreur : Impossible de charger les données
```

**Couleur :** Rouge
**Icône :** ❌ ou 🔴

---

### 4. Informations (console.info)

```javascript
console.info("Information : Le chargement est terminé");
```

**Affichage :**
```
ℹ️ Information : Le chargement est terminé
```

**Couleur :** Bleu (dans certains navigateurs)
**Icône :** ℹ️

---

### 5. Debug (console.debug)

```javascript
console.debug("Debug : Valeur de la variable = 42");
```

**Note :** Moins utilisé, parfois caché par défaut. Visible en activant les messages "Verbose" dans les filtres.

---

## console.log() : La commande la plus importante

### Syntaxe de base

```javascript
console.log("Votre message");
```

Le message apparaît dans la Console. Simple et efficace !

---

### Afficher différents types de données

**Texte (string) :**
```javascript
console.log("Bonjour !");
// Bonjour !
```

**Nombre (number) :**
```javascript
console.log(42);
// 42

console.log(3.14);
// 3.14
```

**Booléen (boolean) :**
```javascript
console.log(true);
// true

console.log(false);
// false
```

**Variable :**
```javascript
let nom = "Marie";
console.log(nom);
// Marie
```

---

### Afficher plusieurs valeurs

Vous pouvez afficher plusieurs valeurs séparées par des virgules :

```javascript
console.log("Nom:", "Marie", "Age:", 25);
// Nom: Marie Age: 25
```

**Très utile pour le debug :**
```javascript
let x = 10;
let y = 20;
console.log("x =", x, "y =", y);
// x = 10 y = 20
```

---

### Afficher des objets

```javascript
let utilisateur = {
  nom: "Dupont",
  prenom: "Jean",
  age: 30
};

console.log(utilisateur);
// { nom: "Dupont", prenom: "Jean", age: 30 }
```

**L'objet est interactif !** Cliquez sur le triangle pour déplier et voir toutes les propriétés.

```
▶ { nom: "Dupont", prenom: "Jean", age: 30 }

// Clic sur ▶
▼ { nom: "Dupont", prenom: "Jean", age: 30 }
    nom: "Dupont"
    prenom: "Jean"
    age: 30
    ▶ [[Prototype]]: Object
```

---

### Afficher des tableaux

```javascript
let fruits = ["Pomme", "Banane", "Orange"];
console.log(fruits);
// (3) ["Pomme", "Banane", "Orange"]
```

**Cliquez pour déplier :**
```
▶ (3) ["Pomme", "Banane", "Orange"]

// Clic sur ▶
▼ (3) ["Pomme", "Banane", "Orange"]
    0: "Pomme"
    1: "Banane"
    2: "Orange"
    length: 3
    ▶ [[Prototype]]: Array
```

---

### console.log avec labels

Ajoutez un label pour savoir ce que vous affichez :

```javascript
let score = 150;
console.log("Score du joueur:", score);
// Score du joueur: 150
```

**Meilleure pratique :** Toujours mettre un label descriptif !

```javascript
// ❌ Pas clair
console.log(x);

// ✅ Clair
console.log("Valeur de x:", x);
```

---

## Autres méthodes console utiles

### console.table() - Affichage en tableau

**Parfait pour les tableaux d'objets :**

```javascript
let utilisateurs = [
  { nom: "Dupont", age: 30 },
  { nom: "Martin", age: 25 },
  { nom: "Dubois", age: 35 }
];

console.table(utilisateurs);
```

**Affichage :**
```
┌─────────┬─────────┬─────┐
│ (index) │   nom   │ age │
├─────────┼─────────┼─────┤
│    0    │ "Dupont"│ 30  │
│    1    │ "Martin"│ 25  │
│    2    │ "Dubois"│ 35  │
└─────────┴─────────┴─────┘
```

**Beaucoup plus lisible qu'avec console.log !**

---

### console.clear() - Effacer la console

```javascript
console.clear();
```

Efface tous les messages de la Console. Utile quand il y a trop de messages.

**Raccourci :** Cliquez sur 🚫 "Clear console" en haut de la Console.

---

### console.count() - Compter les appels

```javascript
function ajouterProduit() {
  console.count("Produit ajouté");
}

ajouterProduit();  // Produit ajouté: 1
ajouterProduit();  // Produit ajouté: 2
ajouterProduit();  // Produit ajouté: 3
```

**Utile pour :** Compter combien de fois une fonction est appelée.

---

### console.time() / console.timeEnd() - Mesurer le temps

```javascript
console.time("Temps de chargement");

// Code à mesurer
for (let i = 0; i < 1000000; i++) {
  // Calcul
}

console.timeEnd("Temps de chargement");
// Temps de chargement: 15.234ms
```

**Utile pour :** Optimiser les performances de votre code.

---

### console.group() - Grouper les messages

```javascript
console.group("Informations utilisateur");
  console.log("Nom: Dupont");
  console.log("Âge: 30");
  console.log("Email: dupont@example.com");
console.groupEnd();
```

**Affichage :**
```
▼ Informations utilisateur
    Nom: Dupont
    Âge: 30
    Email: dupont@example.com
```

Le groupe peut être replié/déplié en cliquant sur le triangle.

---

### console.assert() - Vérifier une condition

```javascript
let age = 15;
console.assert(age >= 18, "L'utilisateur doit être majeur");
// ❌ Assertion failed: L'utilisateur doit être majeur
```

**Affiche une erreur uniquement si la condition est false.**

```javascript
let age = 25;
console.assert(age >= 18, "L'utilisateur doit être majeur");
// (rien n'est affiché car la condition est vraie)
```

---

## Tester du code JavaScript en direct

La Console est aussi un **interpréteur JavaScript interactif**. Vous pouvez taper n'importe quel code JavaScript et il s'exécute immédiatement !

### Calculs simples

```javascript
> 2 + 2
4

> 10 * 5
50

> 100 / 4
25
```

---

### Variables

```javascript
> let nom = "Marie"
undefined

> nom
"Marie"

> nom.toUpperCase()
"MARIE"
```

**Note :** La Console affiche `undefined` quand une instruction ne retourne rien (comme la déclaration d'une variable).

---

### Fonctions

```javascript
> function direBonjour(nom) {
    return "Bonjour " + nom;
  }
undefined

> direBonjour("Jean")
"Bonjour Jean"
```

---

### Accéder au DOM

Vous pouvez manipuler la page en cours directement depuis la Console !

```javascript
> document.title
"Ma Page Web"

> document.title = "Nouveau Titre"
"Nouveau Titre"
// Le titre de la page change instantanément !
```

```javascript
> document.querySelector('h1')
<h1>Mon Titre</h1>

> document.querySelector('h1').textContent = "Nouveau Titre"
"Nouveau Titre"
// Le titre H1 de la page change !
```

---

### Tester une fonction avant de l'écrire

Avant d'écrire une fonction dans votre fichier JavaScript, testez-la dans la Console :

```javascript
> let prix = 100;
> let reduction = 0.2;
> let prixFinal = prix - (prix * reduction);
> prixFinal
80

// Ça marche ! Maintenant je peux l'écrire dans mon code
```

---

## Lire et comprendre les erreurs

Les erreurs JavaScript apparaissent en **rouge** dans la Console. Apprendre à les lire est essentiel !

### Anatomie d'une erreur

```
❌ Uncaught ReferenceError: userName is not defined
    at script.js:15:5
```

**Décomposition :**

1. **❌ Uncaught** : L'erreur n'a pas été gérée (caught)
2. **ReferenceError** : Le type d'erreur
3. **userName is not defined** : Le message explicatif
4. **at script.js:15:5** :
   - Fichier : `script.js`
   - Ligne : `15`
   - Colonne : `5`

**Cliquez sur `script.js:15`** pour ouvrir le fichier dans l'onglet Sources et voir exactement où est l'erreur !

---

### Types d'erreurs courantes

#### 1. ReferenceError

**Signifie :** Une variable n'existe pas

```javascript
console.log(userName);
// ❌ ReferenceError: userName is not defined
```

**Solution :** Vérifiez l'orthographe ou déclarez la variable.

---

#### 2. TypeError

**Signifie :** Mauvais type de données ou méthode inexistante

```javascript
let nombre = 5;
nombre.toUpperCase();
// ❌ TypeError: nombre.toUpperCase is not a function
```

**Explication :** `toUpperCase()` est une méthode pour les strings, pas pour les nombres.

**Solution :** Vérifiez le type de vos données.

---

#### 3. SyntaxError

**Signifie :** Erreur de syntaxe JavaScript

```javascript
let nom = "Jean;
// ❌ SyntaxError: Invalid or unexpected token
```

**Explication :** Guillemet fermant manquant.

**Solution :** Vérifiez votre syntaxe (parenthèses, guillemets, points-virgules).

---

#### 4. RangeError

**Signifie :** Un nombre est en dehors de la plage autorisée

```javascript
let tableau = new Array(-1);
// ❌ RangeError: Invalid array length
```

**Solution :** Vérifiez les valeurs numériques.

---

### Stack trace (Trace de la pile)

Quand une erreur se produit dans une fonction appelée par une autre fonction, la Console montre la **pile d'appels** :

```javascript
function fonction1() {
  fonction2();
}

function fonction2() {
  fonction3();
}

function fonction3() {
  console.log(variableInexistante);
}

fonction1();
```

**Erreur affichée :**
```
❌ ReferenceError: variableInexistante is not defined
    at fonction3 (script.js:10)
    at fonction2 (script.js:6)
    at fonction1 (script.js:2)
    at script.js:13
```

**Lecture de bas en haut :**
1. L'erreur se produit à la ligne 10 (dans `fonction3`)
2. `fonction3` a été appelée par `fonction2` (ligne 6)
3. `fonction2` a été appelée par `fonction1` (ligne 2)
4. `fonction1` a été appelée à la ligne 13

**Très utile pour :** Comprendre le cheminement qui a mené à l'erreur.

---

## Autocomplétion et aide intégrée

### Autocomplétion

Commencez à taper dans la Console, et l'autocomplétion vous aide :

```javascript
> docu
  document
  documentElement
```

Appuyez sur **Tab** pour compléter.

**Pour les objets :**
```javascript
> let texte = "hello";
> texte.
  toUpperCase
  toLowerCase
  substring
  indexOf
  ...
```

---

### Voir les propriétés d'un objet

Tapez un objet suivi d'un point `.` pour voir toutes ses propriétés et méthodes :

```javascript
> console.
  log
  error
  warn
  table
  clear
  ...
```

---

### $0 - Élément actuellement sélectionné

Si vous inspectez un élément dans l'onglet Elements, vous pouvez y accéder dans la Console avec `$0` :

```javascript
// Inspectez un <h1> dans l'onglet Elements
> $0
<h1>Mon Titre</h1>

> $0.textContent
"Mon Titre"

> $0.style.color = "red"
// Le titre devient rouge !
```

**Autres raccourcis :**
- `$0` : Dernier élément sélectionné
- `$1` : Avant-dernier élément sélectionné
- `$2`, `$3`, `$4` : Éléments sélectionnés précédemment

---

### $$ - querySelector shortcut

`$$()` est un raccourci pour `querySelectorAll()` :

```javascript
> $$('p')
// Retourne tous les <p> dans un tableau

> $$('.card')
// Retourne tous les éléments avec la classe "card"
```

**Équivalent à :**
```javascript
> Array.from(document.querySelectorAll('p'))
```

---

## Filtrer les messages

En haut de la Console, vous avez des filtres :

### Filtrer par niveau

```
All levels  ▼
```

Cliquez pour choisir ce que vous voulez voir :
- ✅ **Errors** : Erreurs uniquement
- ✅ **Warnings** : Avertissements uniquement
- ✅ **Info** : Informations uniquement
- ✅ **Verbose** : Tous les messages, y compris debug

**Utile quand** vous avez beaucoup de messages et voulez vous concentrer sur les erreurs.

---

### Filtrer par texte

```
🔍 Filter
```

Tapez un mot pour ne voir que les messages contenant ce mot :

```
Filter: "utilisateur"

Résultat :
✅ Utilisateur connecté
✅ Données utilisateur chargées
❌ Produit ajouté  ← Caché (ne contient pas "utilisateur")
```

---

### Filtrer par source

Vous pouvez filtrer par fichier source :

- Cliquez sur le nom du fichier (ex: `script.js:15`)
- Seuls les messages de ce fichier s'affichent

---

## Paramètres de la Console

Cliquez sur **⚙️** (Settings) en haut de la Console pour accéder aux options :

### Options utiles

**✅ Preserve log**
- Garde les messages même après un rechargement de page
- **Recommandé :** Activé (sinon vous perdez tous les messages au refresh)

**✅ Show timestamps**
- Affiche l'heure de chaque message
- Utile pour mesurer le temps entre les événements

**✅ Autocomplete from history**
- Suggère des commandes que vous avez déjà tapées
- Pratique pour répéter des tests

**✅ Group similar messages in console**
- Regroupe les messages identiques
- Réduit le bruit quand un message se répète

---

## Cas d'usage pratiques

### Scénario 1 : "Ma fonction ne s'exécute pas"

**Problème :** Vous avez écrit une fonction mais rien ne se passe.

**Solution avec la Console :**

```javascript
// Votre code
function direBonjour() {
  console.log("Bonjour !");
}

// Dans la Console, testez :
> direBonjour()
Bonjour !
```

Si ça fonctionne dans la Console mais pas dans votre page :
- Vérifiez que votre script est bien chargé
- Vérifiez que la fonction est bien appelée

---

### Scénario 2 : "Je ne sais pas quelle valeur a ma variable"

**Solution :**

```javascript
// Dans votre code
let score = calculerScore();
console.log("Score:", score);  // Affichez la valeur !
```

Dans la Console :
```
Score: 150
```

Maintenant vous savez que `score` vaut 150.

---

### Scénario 3 : "Mon calcul est faux"

**Problème :** Votre calcul ne donne pas le résultat attendu.

**Solution :** Affichez les étapes intermédiaires :

```javascript
let prix = 100;
let tva = 0.2;

console.log("Prix de base:", prix);
console.log("TVA:", tva);

let prixTTC = prix + (prix * tva);
console.log("Prix TTC:", prixTTC);
```

**Console :**
```
Prix de base: 100
TVA: 0.2
Prix TTC: 120
```

Vous voyez chaque étape et pouvez identifier où est le problème.

---

### Scénario 4 : "Mon tableau est-il correctement rempli ?"

**Solution avec console.table() :**

```javascript
let produits = [
  { nom: "Ordinateur", prix: 800 },
  { nom: "Souris", prix: 25 },
  { nom: "Clavier", prix: 60 }
];

console.table(produits);
```

**Affichage en tableau clair :**
```
┌─────────┬──────────────┬──────┐
│ (index) │     nom      │ prix │
├─────────┼──────────────┼──────┤
│    0    │ "Ordinateur" │ 800  │
│    1    │ "Souris"     │  25  │
│    2    │ "Clavier"    │  60  │
└─────────┴──────────────┴──────┘
```

---

### Scénario 5 : "Je veux tester si un élément existe"

```javascript
> document.querySelector('.menu')
<nav class="menu">...</nav>  ✅ Trouvé

> document.querySelector('.inexistant')
null  ❌ N'existe pas
```

---

## Bonnes pratiques

### 1. Utilisez console.log généreusement pendant le développement

```javascript
function calculerTotal(panier) {
  console.log("Panier reçu:", panier);

  let total = 0;

  for (let item of panier) {
    console.log("Ajout de:", item.prix);
    total += item.prix;
  }

  console.log("Total calculé:", total);
  return total;
}
```

**N'ayez pas peur d'ajouter des console.log !** C'est le moyen le plus simple de comprendre ce qui se passe.

---

### 2. Ajoutez des labels descriptifs

```javascript
// ❌ Pas clair
console.log(x);
console.log(y);

// ✅ Clair
console.log("Position X:", x);
console.log("Position Y:", y);
```

---

### 3. Utilisez les bons niveaux de message

```javascript
// Information normale
console.log("Utilisateur connecté");

// Avertissement
console.warn("Cette API est dépréciée");

// Erreur
console.error("Impossible de charger les données");
```

**Avantage :** Vous pouvez filtrer par niveau dans la Console.

---

### 4. Supprimez les console.log en production

**Avant de mettre votre site en ligne**, supprimez ou commentez vos `console.log()` :

```javascript
// En développement
console.log("Debug: Score =", score);

// En production - commentez ou supprimez
// console.log("Debug: Score =", score);
```

**Pourquoi ?**
- Les console.log ralentissent légèrement le code
- Les utilisateurs peuvent les voir dans la Console
- Ce n'est pas professionnel

---

### 5. Utilisez la Console pour apprendre

Testez tout ce que vous apprenez dans la Console :

```javascript
// Vous apprenez les méthodes de tableau ?
> let fruits = ["pomme", "banane"];
> fruits.push("orange");
> fruits
["pomme", "banane", "orange"]

// Vous comprenez immédiatement l'effet !
```

**La Console est votre bac à sable d'apprentissage.**

---

## Raccourcis clavier utiles

| Action | Windows/Linux | Mac |
|--------|---------------|-----|
| Ouvrir Console | `Ctrl + Shift + J` | `Cmd + Option + J` |
| Effacer Console | `Ctrl + L` | `Cmd + K` |
| Ligne suivante (multiligne) | `Shift + Entrée` | `Shift + Entrée` |
| Exécuter code | `Entrée` | `Entrée` |
| Commande précédente | `↑` | `↑` |
| Commande suivante | `↓` | `↓` |
| Rechercher | `Ctrl + F` | `Cmd + F` |

---

## Code multiligne dans la Console

Pour écrire plusieurs lignes de code, utilisez **Shift + Entrée** pour passer à la ligne sans exécuter :

```javascript
> function calculer(a, b) {  ← Shift + Entrée
    return a + b;            ← Shift + Entrée
  }                          ← Entrée (exécute)
undefined

> calculer(5, 3)
8
```

---

## Astuces avancées

### Styliser les messages

Vous pouvez ajouter du style CSS à vos messages :

```javascript
console.log("%cBienvenue !", "color: blue; font-size: 24px; font-weight: bold;");
```

**Affichage :**
```
Bienvenue !  (en gros et en bleu)
```

**Syntaxe :**
- `%c` dans le message indique le début du style
- Le deuxième argument contient le CSS

---

### Inspecter un objet en profondeur

```javascript
> let user = { nom: "Dupont", details: { age: 30, ville: "Paris" } };
> console.dir(user)
// Affiche l'objet sous forme d'arbre dépliable
```

---

### Mesurer le temps entre deux points

```javascript
console.time("Chargement des données");

// Votre code asynchrone
fetch('/api/data')
  .then(response => response.json())
  .then(data => {
    console.timeEnd("Chargement des données");
    // Chargement des données: 234.56ms
  });
```

---

### Afficher un tableau de bord

```javascript
console.group("📊 Statistiques de la page");
  console.log("Visiteurs:", 1523);
  console.log("Pages vues:", 4892);
  console.log("Temps moyen:", "2m 34s");
console.groupEnd();
```

---

## Résumé

### La Console JavaScript, c'est quoi ?

Un outil pour :
- ✅ Afficher des messages depuis votre code
- ✅ Voir les erreurs JavaScript
- ✅ Tester du code en direct
- ✅ Débugger votre application
- ✅ Inspecter les valeurs des variables

### Commandes essentielles

```javascript
console.log()      // Afficher un message
console.error()    // Afficher une erreur
console.warn()     // Afficher un avertissement
console.table()    // Afficher un tableau
console.clear()    // Effacer la console
```

### Pour débugger efficacement

1. **Ajoutez des console.log()** à chaque étape importante
2. **Lisez attentivement les erreurs** - elles vous disent exactement où est le problème
3. **Testez votre code** dans la Console avant de l'écrire dans votre fichier
4. **Utilisez les filtres** pour vous concentrer sur ce qui est important
5. **N'oubliez pas de supprimer** les console.log() avant la mise en production

### Raccourcis à retenir

- `Ctrl + Shift + J` : Ouvrir la Console
- `Ctrl + L` : Effacer la Console
- `Shift + Entrée` : Nouvelle ligne sans exécuter

---

## Pour aller plus loin

La Console JavaScript est la base du debugging. Maîtrisez-la d'abord, puis explorez :

- **2.4.4 Onglet Sources** : Debugging avancé avec breakpoints
- **2.4.5 Mode Responsive** : Tester votre site sur différents appareils
- **5.12 Gestion des erreurs** : try...catch et gestion d'erreurs avancée

---

## Conseil final

> 💡 **La Console est votre meilleur ami !**

Plus vous l'utilisez, plus vous devenez efficace. Prenez l'habitude :
- D'avoir la Console **toujours ouverte** pendant le développement
- De tester chaque fonction dans la Console avant de l'intégrer
- De lire attentivement chaque erreur (elles contiennent souvent la solution)
- D'utiliser `console.log()` généreusement pour comprendre votre code

**Les développeurs professionnels passent une grande partie de leur temps dans la Console.** C'est normal, c'est un outil indispensable ! 🚀

Avec la pratique, lire et comprendre les messages de la Console deviendra une seconde nature. Vous gagnerez un temps précieux et éviterez beaucoup de frustration.

Bon debugging ! 🐛🔨

⏭️ [Onglet Sources : aperçu du debugging](/02-environnement-de-developpement/04-devtools-du-navigateur/04-onglet-sources-debugging.md)
