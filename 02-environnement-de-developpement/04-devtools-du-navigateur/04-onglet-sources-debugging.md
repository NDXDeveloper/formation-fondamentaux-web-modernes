🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.4.4 Onglet Sources : aperçu du debugging

## Introduction

L'**onglet Sources** est votre **débogueur JavaScript professionnel**. C'est là que vous pouvez mettre en pause votre code, l'examiner ligne par ligne, et comprendre exactement ce qui se passe à chaque étape.

> 💡 **Analogie** : Si la Console est comme avoir un thermomètre pour prendre la température, l'onglet Sources est comme avoir un microscope pour voir les détails cellulaires. Vous pouvez examiner votre code au ralenti, image par image.

Avec l'onglet Sources, vous pouvez :
- 🔍 Voir tous les fichiers de votre site
- ⏸️ Mettre en pause l'exécution du code
- ➡️ Avancer ligne par ligne dans votre code
- 👁️ Inspecter les valeurs des variables à chaque étape
- 🐛 Comprendre pourquoi un bug se produit

**Important :** L'onglet Sources peut sembler intimidant au début, mais c'est un outil **extrêmement puissant** qui deviendra indispensable une fois que vous le maîtriserez.

---

## Ouvrir l'onglet Sources

### Méthode 1 : Via les DevTools

1. Ouvrez les DevTools (`F12`)
2. Cliquez sur l'onglet **"Sources"**

### Méthode 2 : Raccourci direct (Windows/Linux)

`Ctrl + Shift + O` : Ouvre les DevTools sur l'onglet Sources

### Méthode 3 : Depuis la Console

Quand une erreur apparaît dans la Console :
1. Cliquez sur le lien du fichier (ex: `script.js:15`)
2. Cela ouvre le fichier dans l'onglet Sources

---

## Interface de l'onglet Sources

### Vue d'ensemble

```
┌──────────────────────────────────────────────────────────────┐
│ Sources                                               ⚙️ ⋮  │
├────────────────┬─────────────────────┬───────────────────────┤
│                │                     │                       │
│   Panneau      │   Éditeur de code   │   Panneau de debug    │
│   Fichiers     │                     │                       │
│                │ 1  let x = 10;      │  ▶ Call Stack         │
│ ▼ Page         │ 2  let y = 20;      │  ▶ Scope              │
│   ▼ (no domain)│ 3  ●console.log(x); │  ▶ Breakpoints        │
│     index.html │ 4  let z = x + y;   │  ▶ Watch              │
│   ▼ css/       │ 5  console.log(z);  │                       │
│     style.css  │                     │  Paused on breakpoint │
│   ▼ js/        │                     │                       │
│   ● script.js  │                     │  [▶] [↷] [↓] [↗] [↘]  │
│                │                     │                       │
└────────────────┴─────────────────────┴───────────────────────┘
```

**Trois panneaux principaux :**

1. **Panneau Fichiers (gauche)** : Arborescence de tous les fichiers du site
2. **Éditeur de code (centre)** : Contenu du fichier sélectionné
3. **Panneau de debug (droite)** : Outils de débogage

---

## Panneau Fichiers (File Tree)

### Navigation dans les fichiers

Le panneau de gauche montre **tous les fichiers** chargés par votre page :

```
▼ Page
  ▼ localhost:5500
    index.html
    ▼ css/
      style.css
      reset.css
    ▼ js/
      script.js
      utils.js
    ▼ images/
      logo.png
```

**Cliquez sur un fichier** pour l'ouvrir dans l'éditeur central.

---

### Types de fichiers

Vous verrez différents types de fichiers :

- **HTML** : `.html`
- **CSS** : `.css`
- **JavaScript** : `.js`
- **Images** : `.jpg`, `.png`, `.svg`
- **Fichiers externes** : Librairies (jQuery, Bootstrap, etc.)

**Astuce :** Vous pouvez inspecter le code source de n'importe quel site pour apprendre !

---

### Rechercher un fichier

**Raccourci :** `Ctrl + P` (Windows/Linux) ou `Cmd + P` (Mac)

Une boîte de recherche apparaît :
```
Open file: |_
```

Tapez le nom du fichier et appuyez sur Entrée pour l'ouvrir.

**Exemple :**
```
Tapez "script" → Trouve script.js
Tapez "style" → Trouve style.css
```

**Très utile** quand vous avez beaucoup de fichiers !

---

## L'éditeur de code

### Visualisation du code

Le panneau central affiche le contenu du fichier avec :

- **Numéros de ligne** (à gauche)
- **Coloration syntaxique** (code en couleur)
- **Possibilité de scroller** pour voir tout le fichier

```javascript
1  // Mon script
2  let utilisateur = {
3    nom: "Dupont",
4    age: 30
5  };
6
7  console.log(utilisateur);
```

---

### Code en lecture seule

**Important :** Le code affiché est **en lecture seule**. Vous ne pouvez pas le modifier directement ici.

**Pour modifier votre code :**
1. Ouvrez le fichier dans VS Code
2. Modifiez-le
3. Sauvegardez
4. Rafraîchissez la page (`F5`)

---

### Pretty Print (Code minifié)

Si vous ouvrez un fichier minifié (tout sur une ligne), cliquez sur **{ }** en bas de l'éditeur pour le formater :

```javascript
// Avant (minifié)
let x=10;let y=20;console.log(x+y);

// Après Pretty Print
let x = 10;
let y = 20;
console.log(x + y);
```

**Utile pour :** Lire le code de librairies externes minifiées.

---

## Les Breakpoints (Points d'arrêt)

Les **breakpoints** sont le cœur du debugging. Ils permettent de **mettre en pause** l'exécution de votre code à un endroit précis.

### Qu'est-ce qu'un breakpoint ?

Un breakpoint est un **point d'arrêt** dans votre code. Quand le code atteint cette ligne, il se met **en pause** et vous pouvez inspecter l'état de votre application.

> 💡 **Analogie** : C'est comme mettre un film sur pause pour examiner une scène en détail.

---

### Ajouter un breakpoint

**Méthode simple :**
1. Ouvrez votre fichier JavaScript dans l'onglet Sources
2. **Cliquez sur le numéro de ligne** où vous voulez mettre en pause
3. Un **point bleu** (🔵) apparaît sur la ligne

```javascript
1  function calculer(a, b) {
2    let resultat = a + b;  🔵 ← Breakpoint ici
3    return resultat;
4  }
```

**Pour retirer un breakpoint :** Cliquez à nouveau sur le point bleu.

---

### Exécution avec breakpoint

Quand votre code atteint un breakpoint :

1. **L'exécution se met en pause** ⏸️
2. La ligne en cours est **surlignée**
3. Le panneau de debug devient actif
4. Vous pouvez inspecter toutes les variables

```javascript
1  function calculer(a, b) {
2  ➤ let resultat = a + b;  🔵 ← PAUSE ICI
3    return resultat;
4  }
```

**La flèche ➤** indique où en est l'exécution.

---

### Breakpoints conditionnels

Vous pouvez créer un breakpoint qui ne se déclenche que si une condition est vraie.

**Comment faire :**
1. **Clic droit** sur le numéro de ligne
2. Sélectionnez **"Add conditional breakpoint"**
3. Entrez une condition, exemple : `x > 100`
4. Le breakpoint apparaît en **orange** 🟠

```javascript
1  for (let i = 0; i < 1000; i++) {
2    calculer(i);  🟠 ← Se déclenche seulement si i > 100
3  }
```

**Très utile pour :** Débugger une boucle qui s'exécute des centaines de fois.

---

## Contrôles de débogage

Quand le code est en pause, vous avez des boutons de contrôle :

```
[▶] Resume    : Reprendre l'exécution
[↷] Step Over : Passer à la ligne suivante
[↓] Step Into : Entrer dans une fonction
[↗] Step Out  : Sortir de la fonction actuelle
[↘] Step      : Avancer d'une instruction
```

### 1. ▶ Resume (Reprendre)

**Raccourci :** `F8`

Reprend l'exécution normale jusqu'au prochain breakpoint (ou la fin du script).

**Utilisation :**
- Vous avez inspecté ce que vous vouliez
- Vous voulez continuer jusqu'au prochain breakpoint

---

### 2. ↷ Step Over (Passer par-dessus)

**Raccourci :** `F10`

**Exécute la ligne actuelle** et passe à la suivante, **sans entrer** dans les fonctions.

```javascript
1  let x = 10;
2  ➤ calculer(x);     // Step Over : exécute calculer() sans y entrer
3  console.log("fin");
```

Après Step Over, vous êtes à la ligne 3, `calculer()` a été exécutée.

**Utilisation :** Quand vous ne voulez pas débugger l'intérieur d'une fonction.

---

### 3. ↓ Step Into (Entrer dans)

**Raccourci :** `F11`

**Entre dans la fonction** de la ligne actuelle pour la débugger.

```javascript
1  let x = 10;
2  ➤ calculer(x);     // Step Into : entre dans calculer()
3  console.log("fin");

// Vous vous retrouvez ici :
function calculer(a) {
  ➤ let resultat = a * 2;
    return resultat;
}
```

**Utilisation :** Quand vous voulez voir ce qui se passe à l'intérieur d'une fonction.

---

### 4. ↗ Step Out (Sortir)

**Raccourci :** `Shift + F11`

**Sort de la fonction actuelle** et revient à la fonction qui l'a appelée.

```javascript
function calculer(a) {
  let resultat = a * 2;
  ➤ return resultat;  // Step Out : retourne à l'appelant
}

// Vous vous retrouvez ici :
let x = 10;
calculer(x);
➤ console.log("fin");
```

**Utilisation :** Quand vous êtes dans une fonction et voulez en sortir rapidement.

---

### Résumé des contrôles

| Contrôle | Raccourci | Action |
|----------|-----------|--------|
| **Resume** | `F8` | Continue jusqu'au prochain breakpoint |
| **Step Over** | `F10` | Ligne suivante (sans entrer dans les fonctions) |
| **Step Into** | `F11` | Entre dans la fonction |
| **Step Out** | `Shift + F11` | Sort de la fonction actuelle |

**Astuce :** Mémorisez `F10` (Step Over), c'est le plus utilisé !

---

## Panneau de debug (droite)

### Call Stack (Pile d'appels)

Montre **la chaîne des fonctions** qui ont été appelées pour arriver au point actuel.

```
Call Stack
  fonction3 (script.js:10)  ← Vous êtes ici
  fonction2 (script.js:6)   ← Appelée par fonction2
  fonction1 (script.js:2)   ← Appelée par fonction1
  (anonymous) (script.js:13) ← Code principal
```

**Lecture de bas en haut :**
1. Le code principal appelle `fonction1`
2. `fonction1` appelle `fonction2`
3. `fonction2` appelle `fonction3`
4. Vous êtes actuellement dans `fonction3`

**Cliquez sur une ligne** pour voir le code de cette fonction.

---

### Scope (Portée)

Montre **toutes les variables** accessibles au point actuel :

```
▼ Scope
  ▼ Local
    a: 10
    b: 20
    resultat: 30
  ▼ Closure
    (aucune)
  ▼ Global
    window: Window
    document: document
    console: Console
```

**Types de scope :**

- **Local** : Variables de la fonction actuelle
- **Closure** : Variables capturées des fonctions parentes
- **Global** : Variables globales (window, document, etc.)

**Survolez une variable** pour voir sa valeur en détail.

---

### Watch (Surveillance)

Permet de **surveiller des expressions** personnalisées.

**Comment ajouter une watch expression :**
1. Cliquez sur **"+"** dans le panneau Watch
2. Tapez l'expression à surveiller : `x + y`, `utilisateur.nom`, etc.
3. La valeur s'affiche et se met à jour à chaque étape

```
▼ Watch
  x + y: 30
  utilisateur.nom: "Dupont"
  prix * 1.2: 120
```

**Très utile pour :** Suivre des calculs ou des propriétés spécifiques pendant le débogage.

---

### Breakpoints (Liste)

Liste **tous vos breakpoints** avec leurs emplacements :

```
▼ Breakpoints
  ☑ script.js:15
  ☑ script.js:42
  ☐ utils.js:8 (disabled)
```

**Actions possibles :**
- **Cocher/Décocher** : Activer/Désactiver un breakpoint
- **Clic** : Aller au breakpoint dans le code
- **Clic droit > Remove** : Supprimer le breakpoint

**Bouton "Deactivate all breakpoints"** : Désactive tous les breakpoints d'un coup.

---

## Debugging en action : Exemple concret

Imaginons ce code avec un bug :

```javascript
function calculerTotalPanier(panier) {
  let total = 0;

  for (let item of panier) {
    total += item.prix * item.quantite;
  }

  return total;
}

let panier = [
  { nom: "Pomme", prix: 2, quantite: 3 },
  { nom: "Banane", prix: 1.5, quantite: 2 }
];

let total = calculerTotalPanier(panier);
console.log("Total:", total);
```

### Étape 1 : Ajouter un breakpoint

Cliquez sur la ligne 5 pour ajouter un breakpoint :

```javascript
3
4  for (let item of panier) {
5    total += item.prix * item.quantite;  🔵 ← Breakpoint
6  }
```

---

### Étape 2 : Rafraîchir la page

Appuyez sur `F5`. Le code s'exécute et **se met en pause** au breakpoint.

```javascript
4  for (let item of panier) {
5  ➤ total += item.prix * item.quantite;  🔵 PAUSE
6  }
```

---

### Étape 3 : Inspecter les variables

Dans le panneau **Scope**, vous voyez :

```
▼ Local
  total: 0
  item: {nom: "Pomme", prix: 2, quantite: 3}
```

Vous pouvez vérifier que `item.prix` et `item.quantite` ont les bonnes valeurs.

---

### Étape 4 : Avancer pas à pas

Appuyez sur `F10` (Step Over) pour exécuter la ligne.

**Après l'exécution :**

```
▼ Local
  total: 6     ← A changé ! (2 * 3 = 6)
  item: {nom: "Pomme", prix: 2, quantite: 3}
```

Appuyez encore sur `F10` pour passer à l'itération suivante de la boucle.

---

### Étape 5 : Observer le calcul

Au deuxième passage :

```
▼ Local
  total: 6
  item: {nom: "Banane", prix: 1.5, quantite: 2}
```

Appuyez sur `F10` :

```
▼ Local
  total: 9     ← 6 + (1.5 * 2) = 9 ✓
```

Le calcul est correct ! Vous pouvez appuyer sur `F8` (Resume) pour continuer.

---

## Inspecter les valeurs

### Survoler une variable

Dans l'éditeur, **survolez n'importe quelle variable** avec la souris :

```javascript
total += item.prix * item.quantite;
         ↑
    Survolez "item"
```

Une **info-bulle** apparaît avec la valeur complète de l'objet :

```
item: {
  nom: "Pomme",
  prix: 2,
  quantite: 3
}
```

---

### Console en parallèle

Vous pouvez utiliser la **Console** en même temps que le débogueur !

Quand le code est en pause :
1. Ouvrez la Console (appuyez sur `Esc`)
2. Tapez le nom d'une variable
3. Sa valeur s'affiche

```javascript
> item
{nom: "Pomme", prix: 2, quantite: 3}

> item.prix * item.quantite
6
```

**Très pratique** pour tester des expressions pendant le debug !

---

## Breakpoints spéciaux

### Exception breakpoints

Vous pouvez mettre en pause automatiquement quand une **erreur** se produit.

**Comment activer :**
1. Dans le panneau Breakpoints
2. Cochez **"Pause on exceptions"** ☑
3. Optionnel : Cochez aussi **"Pause on caught exceptions"**

```
☑ Pause on exceptions
☐ Pause on caught exceptions
```

**Résultat :** Dès qu'une erreur se produit, le débogueur se met en pause à la ligne problématique.

**Très utile pour :** Trouver rapidement les erreurs qui cassent votre code.

---

### DOM breakpoints

Vous pouvez mettre en pause quand un élément HTML est **modifié**.

**Comment ajouter :**
1. Dans l'onglet **Elements**, sélectionnez un élément
2. **Clic droit** > **Break on** > Choisissez :
   - **Subtree modifications** : Un enfant est ajouté/supprimé
   - **Attribute modifications** : Un attribut change
   - **Node removal** : L'élément est supprimé

**Exemple :**
```javascript
// Vous ne savez pas où dans votre code cet élément est modifié
document.querySelector('.titre').textContent = "Nouveau titre";
```

Ajoutez un DOM breakpoint sur `.titre`, et le débogueur se mettra en pause quand le texte change !

---

### XHR/Fetch breakpoints

Vous pouvez mettre en pause quand une **requête HTTP** est faite.

**Comment ajouter :**
1. Dans le panneau **XHR/Fetch Breakpoints**
2. Cliquez sur **"+"**
3. Entrez une partie de l'URL : `/api/users`

**Résultat :** Le code se met en pause quand une requête vers cette URL est effectuée.

---

## Debugging de fonctions asynchrones

### Async/Await

Le débogueur fonctionne parfaitement avec `async/await` :

```javascript
async function chargerDonnees() {
  console.log("Début");

  let reponse = await fetch('/api/data');  🔵 Breakpoint
  let data = await reponse.json();

  console.log(data);
}
```

Vous pouvez mettre un breakpoint et utiliser `F10` normalement. Le débogueur attend la résolution de la Promise.

---

### Promises

Avec les Promises classiques :

```javascript
fetch('/api/data')
  .then(response => response.json())  🔵 Breakpoint
  .then(data => {
    console.log(data);  🔵 Breakpoint
  });
```

Les breakpoints fonctionnent dans chaque `.then()`.

---

## Cas d'usage pratiques

### Scénario 1 : "Mon calcul donne un mauvais résultat"

**Problème :** Une fonction de calcul retourne une valeur incorrecte.

**Solution avec le débogueur :**
1. Ajoutez un breakpoint au début de la fonction
2. Exécutez pas à pas (`F10`)
3. Vérifiez la valeur de chaque variable à chaque étape
4. Identifiez où le calcul devient incorrect

---

### Scénario 2 : "Ma boucle ne fonctionne pas comme prévu"

**Problème :** Une boucle s'exécute trop de fois ou pas assez.

**Solution :**
1. Breakpoint au début de la boucle
2. Surveillez la variable de contrôle dans **Scope**
3. Avancez avec `F10` pour voir chaque itération
4. Identifiez où la condition de sortie échoue

---

### Scénario 3 : "Je ne sais pas quelle fonction appelle mon code"

**Problème :** Votre fonction est appelée, mais vous ne savez pas d'où.

**Solution :**
1. Breakpoint dans votre fonction
2. Quand ça se met en pause, regardez la **Call Stack**
3. Vous voyez toute la chaîne d'appels
4. Cliquez sur chaque entrée pour voir le code

---

### Scénario 4 : "Un objet a une valeur inattendue"

**Problème :** Un objet ne contient pas les bonnes données.

**Solution :**
1. Breakpoint juste après la création/modification de l'objet
2. Inspectez l'objet dans **Scope**
3. Dépliez toutes les propriétés
4. Vérifiez que toutes les valeurs sont correctes

---

### Scénario 5 : "Mon code ne passe jamais dans un if"

**Problème :** Une condition `if` n'est jamais vraie.

**Solution :**
1. Breakpoint juste avant le `if`
2. Vérifiez la valeur de la condition dans **Scope** ou **Console**
3. Testez la condition dans la Console : `x > 10`
4. Comprenez pourquoi elle est fausse

---

## Bonnes pratiques

### 1. Commencez par la Console, puis le débogueur

**Workflow recommandé :**
1. Ajoutez des `console.log()` pour comprendre le flux
2. Si ce n'est pas assez, utilisez le débogueur
3. Ajoutez des breakpoints aux endroits clés

Le débogueur est **plus puissant** mais aussi plus lent. Utilisez-le quand la Console ne suffit pas.

---

### 2. Utilisez des breakpoints conditionnels

Au lieu de mettre en pause 1000 fois dans une boucle :

```javascript
// ❌ Mauvais : Se déclenche 1000 fois
for (let i = 0; i < 1000; i++) {
  traiter(i);  🔵 Breakpoint
}

// ✅ Bon : Breakpoint conditionnel (i === 500)
for (let i = 0; i < 1000; i++) {
  traiter(i);  🟠 Se déclenche seulement à i = 500
}
```

---

### 3. Surveillez les expressions clés avec Watch

Ajoutez dans **Watch** les expressions importantes :
- Variables critiques
- Calculs complexes
- État de votre application

```
▼ Watch
  utilisateur.isConnecte
  panier.length
  total * 1.2
```

Elles se mettent à jour automatiquement à chaque étape.

---

### 4. Désactivez les breakpoints au lieu de les supprimer

Si vous avez un breakpoint que vous n'utilisez pas maintenant mais qui pourrait être utile plus tard :
- **Décochez-le** ☐ au lieu de le supprimer
- Vous pouvez le réactiver facilement plus tard

---

### 5. Nettoyez vos breakpoints

Supprimez les breakpoints dont vous n'avez plus besoin :
- Clic droit dans la liste des breakpoints > **"Remove breakpoint"**
- Ou cliquez sur le point bleu dans le code

**Un projet avec 50 breakpoints inutilisés = confusion garantie !**

---

## Raccourcis clavier essentiels

| Action | Windows/Linux | Mac |
|--------|---------------|-----|
| Ajouter/Retirer breakpoint | Clic sur numéro de ligne | Clic sur numéro de ligne |
| Resume (Continuer) | `F8` | `F8` |
| Step Over | `F10` | `F10` |
| Step Into | `F11` | `F11` |
| Step Out | `Shift + F11` | `Shift + F11` |
| Désactiver tous breakpoints | `Ctrl + F8` | `Cmd + F8` |
| Ouvrir fichier | `Ctrl + P` | `Cmd + P` |

---

## Limites et pièges à éviter

### 1. Le code est minifié

**Problème :** Le code de production est souvent minifié (tout sur une ligne).

**Solution :** Cliquez sur **{ }** (Pretty Print) en bas de l'éditeur pour le formater.

---

### 2. Code asynchrone complexe

**Problème :** Avec beaucoup d'async/await ou de Promises, suivre le flux peut être compliqué.

**Solution :** Utilisez la **Call Stack** et les **Watch expressions** pour garder le fil.

---

### 3. Trop de breakpoints

**Problème :** Vous avez mis des breakpoints partout et perdez du temps.

**Solution :**
- Soyez **stratégique** dans vos breakpoints
- Un ou deux breakpoints bien placés valent mieux que 10 partout

---

### 4. Oubli de retirer les breakpoints

**Problème :** Vous laissez des breakpoints actifs et le site se met en pause lors de la navigation normale.

**Solution :** Désactivez tous les breakpoints quand vous avez fini de débugger.

---

## Console vs Débogueur : Quand utiliser quoi ?

### Utilisez la Console quand :

- ✅ Vous voulez voir rapidement des valeurs
- ✅ Le bug est simple à identifier
- ✅ Vous testez du code rapidement
- ✅ Vous débutez avec un problème

### Utilisez le Débogueur quand :

- ✅ Le bug est complexe
- ✅ Vous devez suivre le flux d'exécution
- ✅ Vous avez besoin de voir l'état à chaque étape
- ✅ Les `console.log()` ne suffisent plus

**En pratique :** Commencez par la Console (plus rapide), passez au débogueur si nécessaire (plus puissant).

---

## Résumé

### L'onglet Sources, c'est quoi ?

Un débogueur JavaScript complet pour :
- 🔍 Voir tous vos fichiers
- ⏸️ Mettre en pause l'exécution
- 🐛 Débugger pas à pas
- 👁️ Inspecter les variables
- 🔬 Comprendre le flux d'exécution

### Concepts clés

**Breakpoint** : Point d'arrêt dans le code
**Step Over (F10)** : Ligne suivante
**Step Into (F11)** : Entrer dans une fonction
**Call Stack** : Chaîne des appels de fonctions
**Scope** : Variables accessibles
**Watch** : Expressions surveillées

### Workflow de débogage

1. Identifiez la zone problématique
2. Ajoutez un breakpoint
3. Rafraîchissez la page (`F5`)
4. Le code se met en pause
5. Inspectez les variables
6. Avancez pas à pas (`F10`)
7. Identifiez le problème
8. Corrigez dans votre éditeur
9. Testez à nouveau

---

## Pour aller plus loin

L'onglet Sources est un outil avancé qui demande de la pratique. Plus vous l'utilisez, plus vous devenez efficace !

**Prochaines étapes :**
- **2.4.5 Mode Responsive** : Tester votre site sur mobile et tablette
- **5.12.6 Breakpoints avancés** : Techniques de debugging avancées
- **7.1 Debugging JavaScript avancé** : Maîtriser le débogueur

---

## Conseil final

> 💡 **Le débogueur, c'est comme apprendre à conduire**

Au début, ça semble compliqué : "Je dois faire quoi ? F10 ou F11 ?". Mais avec la pratique, ça devient naturel.

**Commencez simple :**
1. Un breakpoint
2. F10 pour avancer
3. Regardez les valeurs dans Scope

Petit à petit, vous découvrirez toutes les fonctionnalités avancées. L'important est de **pratiquer** !

**Exercice recommandé :**
Prenez un de vos projets JavaScript, ajoutez un breakpoint au début d'une fonction, et suivez son exécution pas à pas. Observez comment les variables changent. C'est la meilleure façon d'apprendre ! 🚀

Le débogueur transformera votre façon de coder. Fini les 50 `console.log()` partout, bonjour le debugging professionnel ! 🐛🔧

⏭️ [Mode responsive et simulation mobile](/02-environnement-de-developpement/04-devtools-du-navigateur/05-mode-responsive.md)
