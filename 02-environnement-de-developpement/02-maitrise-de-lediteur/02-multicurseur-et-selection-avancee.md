🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.2.2 Multicurseur et sélection avancée

## Introduction

Le **multicurseur** (ou multi-cursor en anglais) est l'une des fonctionnalités les plus puissantes et impressionnantes de VS Code. Cette fonction vous permet d'avoir **plusieurs curseurs actifs en même temps**, ce qui signifie que vous pouvez écrire et modifier du code à plusieurs endroits simultanément.

### Qu'est-ce que le multicurseur ?

**Normalement**, quand vous tapez dans un éditeur :
- Vous avez **un seul curseur** (la barre verticale qui clignote)
- Vous tapez à **un seul endroit** à la fois

**Avec le multicurseur** :
- Vous avez **plusieurs curseurs** actifs simultanément
- Ce que vous tapez apparaît à **tous les endroits** en même temps
- Vous pouvez modifier **plusieurs lignes identiques** en une seule fois

### Pourquoi c'est révolutionnaire ?

Imaginez que vous devez modifier ce code HTML :

```html
<li>Élément 1</li>
<li>Élément 2</li>
<li>Élément 3</li>
<li>Élément 4</li>
<li>Élément 5</li>
```

Vous voulez remplacer tous les `<li>` par `<li class="item">`.

**Sans multicurseur** (méthode traditionnelle) :
1. Modifiez la ligne 1
2. Modifiez la ligne 2
3. Modifiez la ligne 3
4. Modifiez la ligne 4
5. Modifiez la ligne 5
→ 5 modifications répétitives = ennuyeux et chronophage

**Avec multicurseur** :
1. Placez un curseur sur chaque ligne
2. Tapez ` class="item"` une seule fois
3. Toutes les lignes sont modifiées simultanément !
→ 1 seule manipulation = rapide et efficace

**Gain de temps** : Des secondes à chaque fois, mais **des heures sur un projet** !

### Ce que vous allez apprendre

Dans cette section, nous allons explorer :
- 🎯 Les différentes méthodes pour créer des multicurseurs
- ✏️ Comment éditer avec plusieurs curseurs
- 🔍 La sélection avancée et intelligente
- 💡 Des cas d'usage concrets et pratiques
- 🚀 Des astuces pour devenir un expert du multicurseur

---

## Créer des multicurseurs : les méthodes essentielles

Il existe plusieurs façons de créer des multicurseurs dans VS Code. Nous allons les voir du plus simple au plus avancé.

### Méthode 1 : Alt/Option + Clic (la plus intuitive)

**Raccourci** :
- Windows/Linux : `Alt + Clic`
- macOS : `Option + Clic`

**Comment ça marche** :
1. Maintenez `Alt` (ou `Option` sur Mac) enfoncé
2. Cliquez à chaque endroit où vous voulez un curseur
3. Relâchez `Alt`/`Option`
4. Commencez à taper : tous les curseurs s'activent !

**Exemple pratique** :

```html
<h1>Titre</h1>
<h2>Sous-titre</h2>
<h3>Section</h3>
```

Vous voulez ajouter `class="heading"` à chaque balise :
1. Maintenez `Alt`/`Option`
2. Cliquez après chaque `<h1`, `<h2`, `<h3`
3. Relâchez `Alt`/`Option`
4. Tapez ` class="heading"`

Résultat :
```html
<h1 class="heading">Titre</h1>
<h2 class="heading">Sous-titre</h2>
<h3 class="heading">Section</h3>
```

**Pourquoi c'est la méthode la plus simple** :
- Très visuelle : vous voyez exactement où vous placez les curseurs
- Intuitive : un clic = un curseur
- Parfaite pour des modifications ponctuelles

---

### Méthode 2 : Ctrl/⌘ + Alt/Option + ↑↓ (ajouter au-dessus/en-dessous)

**Raccourcis** :
- Windows/Linux :
  - `Ctrl + Alt + ↑` : ajouter un curseur au-dessus
  - `Ctrl + Alt + ↓` : ajouter un curseur en dessous
- macOS :
  - `⌘ + Option + ↑` : ajouter un curseur au-dessus
  - `⌘ + Option + ↓` : ajouter un curseur en dessous

**Comment ça marche** :
1. Placez votre curseur sur une ligne
2. Appuyez sur `Ctrl/⌘ + Alt/Option + ↓` pour ajouter un curseur sur la ligne suivante
3. Continuez d'appuyer pour ajouter d'autres curseurs
4. Même chose avec `↑` pour ajouter au-dessus

**Exemple pratique** :

```css
.button { }
.input { }
.label { }
.form { }
```

Vous voulez ajouter `color: blue;` dans chaque classe :
1. Curseur après `{ }` de la première ligne
2. `Ctrl/⌘ + Alt/Option + ↓` trois fois pour créer 4 curseurs
3. Appuyez sur `Entrée` pour créer une nouvelle ligne sur chaque curseur
4. Tapez `  color: blue;`

Résultat :
```css
.button {
  color: blue;
}
.input {
  color: blue;
}
.label {
  color: blue;
}
.form {
  color: blue;
}
```

**Quand utiliser cette méthode** :
- Pour des lignes consécutives
- Quand les modifications sont alignées verticalement
- Plus rapide que de cliquer plusieurs fois

---

### Méthode 3 : Ctrl/⌘ + D (sélectionner l'occurrence suivante)

**Raccourci** : `Ctrl + D` (Windows/Linux) ou `⌘ + D` (macOS)

**Comment ça marche** :
1. Double-cliquez sur un mot (ou placez le curseur sur un mot)
2. Appuyez sur `Ctrl/⌘ + D` : le mot est sélectionné
3. Appuyez à nouveau sur `Ctrl/⌘ + D` : l'occurrence suivante du même mot est sélectionnée avec un nouveau curseur
4. Continuez pour sélectionner plus d'occurrences
5. Tapez pour remplacer toutes les occurrences sélectionnées

**Exemple pratique** :

```javascript
const name = "Jean";
console.log(name);
alert(name);
return name;
```

Vous voulez remplacer tous les `name` par `username` :
1. Double-cliquez sur le premier `name`
2. `Ctrl/⌘ + D` : sélectionne le deuxième `name`
3. `Ctrl/⌘ + D` : sélectionne le troisième `name`
4. `Ctrl/⌘ + D` : sélectionne le quatrième `name`
5. Tapez `username`

Résultat :
```javascript
const username = "Jean";
console.log(username);
alert(username);
return username;
```

**Pourquoi c'est génial** :
- Très rapide pour remplacer plusieurs occurrences d'un mot
- Vous contrôlez exactement quelles occurrences sélectionner
- Évite le rechercher/remplacer classique

**Astuce** : Si vous appuyez une fois de trop sur `Ctrl/⌘ + D`, appuyez sur `Ctrl/⌘ + U` pour revenir en arrière (annuler la dernière sélection).

---

### Méthode 4 : Ctrl/⌘ + Shift + L (sélectionner TOUTES les occurrences)

**Raccourci** : `Ctrl + Shift + L` (Windows/Linux) ou `⌘ + Shift + L` (macOS)

**Comment ça marche** :
1. Sélectionnez un mot (double-clic ou `Ctrl/⌘ + D`)
2. Appuyez sur `Ctrl/⌘ + Shift + L`
3. **TOUTES** les occurrences du mot dans le fichier sont sélectionnées avec des curseurs
4. Tapez pour modifier toutes les occurrences simultanément

**Exemple pratique** :

```css
.container {
  width: 100%;
}

.container p {
  color: blue;
}

.container .item {
  margin: 10px;
}

.container:hover {
  opacity: 0.8;
}
```

Vous voulez remplacer toutes les occurrences de `container` par `wrapper` :
1. Double-cliquez sur le premier `container`
2. `Ctrl/⌘ + Shift + L` : toutes les occurrences sont sélectionnées (4 au total)
3. Tapez `wrapper`

Résultat :
```css
.wrapper {
  width: 100%;
}

.wrapper p {
  color: blue;
}

.wrapper .item {
  margin: 10px;
}

.wrapper:hover {
  opacity: 0.8;
}
```

**Différence avec Ctrl/⌘ + D** :
- `Ctrl/⌘ + D` : sélectionne une par une (contrôle granulaire)
- `Ctrl/⌘ + Shift + L` : sélectionne TOUT d'un coup (action massive)

**Quand utiliser** :
- Quand vous êtes **sûr** de vouloir remplacer TOUTES les occurrences
- Pour des changements globaux dans un fichier
- Gain de temps énorme sur de gros fichiers

**⚠️ Attention** : Vérifiez bien que vous ne modifiez pas accidentellement d'autres mots similaires !

---

### Méthode 5 : Sélection en colonne (Alt/Option + Shift + Glisser)

**Raccourci** :
- Windows/Linux : `Alt + Shift + Glisser` avec la souris
- macOS : `Option + Shift + Glisser` avec la souris

**Comment ça marche** :
1. Maintenez `Alt + Shift` (ou `Option + Shift` sur Mac)
2. Cliquez et glissez verticalement pour créer une sélection rectangulaire
3. Tous les caractères dans le rectangle sont sélectionnés
4. Tapez pour modifier toutes les lignes

**Exemple pratique** :

```
Jean    Dupont    Paris
Marie   Martin    Lyon
Pierre  Bernard   Marseille
Sophie  Dubois    Toulouse
```

Vous voulez sélectionner tous les prénoms (première colonne) :
1. Maintenez `Alt + Shift` (ou `Option + Shift`)
2. Cliquez avant "Jean" et glissez jusqu'après "Sophie"
3. Relâchez
4. Toute la première colonne est sélectionnée

**Alternative au clavier** :
- Windows/Linux : `Ctrl + Shift + Alt + ↑/↓/←/→`
- macOS : `⌘ + Shift + Option + ↑/↓/←/→`

**Quand utiliser** :
- Pour des données alignées en colonnes
- Pour modifier du texte structuré
- Pour créer des multicurseurs sur des colonnes spécifiques

---

### Méthode 6 : Regex avec Rechercher/Remplacer (avancé)

**Raccourci** : `Ctrl/⌘ + H` (Rechercher/Remplacer)

**Comment ça marche** :
1. Ouvrez Rechercher/Remplacer avec `Ctrl/⌘ + H`
2. Activez l'option **"Utiliser une expression régulière"** (icône `.*`)
3. Entrez votre pattern regex
4. Cliquez sur **"Tout remplacer"**

**Exemple pratique** :

```html
<img src="image1.jpg">
<img src="image2.jpg">
<img src="image3.jpg">
```

Vous voulez ajouter `alt="Image X"` (où X est le numéro) :
1. `Ctrl/⌘ + H`
2. Activez regex
3. Rechercher : `<img src="image(\d+).jpg">`
4. Remplacer par : `<img src="image$1.jpg" alt="Image $1">`
5. "Tout remplacer"

Résultat :
```html
<img src="image1.jpg" alt="Image 1">
<img src="image2.jpg" alt="Image 2">
<img src="image3.jpg" alt="Image 3">
```

**Note** : Les regex sont un sujet avancé. Pour l'instant, sachez juste que cette option existe !

---

## Éditer avec des multicurseurs

Une fois que vous avez créé vos multicurseurs, voici ce que vous pouvez faire.

### Taper du texte

**Le plus simple** : Tout ce que vous tapez apparaît à tous les curseurs.

```html
<!-- Avant (3 curseurs après chaque <div) -->
<div>
<div>
<div>

<!-- Tapez " class="box">" -->
<div class="box">
<div class="box">
<div class="box">
```

### Supprimer du texte

**Backspace** et **Delete** fonctionnent sur tous les curseurs.

```html
<!-- Avant (curseurs avant "old-") -->
<div class="old-container">
<div class="old-wrapper">
<div class="old-box">

<!-- Appuyez sur Delete 4 fois pour supprimer "old-" -->
<div class="container">
<div class="wrapper">
<div class="box">
```

### Se déplacer avec les flèches

Les **flèches directionnelles** déplacent tous les curseurs en même temps.

```javascript
// Curseurs au début de chaque ligne
const name = "Jean";
const age = 25;
const city = "Paris";

// Appuyez sur → 6 fois pour aller après "const "
const |name = "Jean";
const |age = 25;
const |city = "Paris";

// Tapez "user" devant chaque variable
const userName = "Jean";
const userAge = 25;
const userCity = "Paris";
```

### Sélectionner avec Shift + Flèches

**Shift + Flèches** sélectionne à tous les curseurs.

```css
/* Curseurs au début de chaque ligne */
color: red;
font-size: 16px;
margin: 10px;

/* Shift + End : sélectionne jusqu'à la fin de chaque ligne */
[color: red;]
[font-size: 16px;]
[margin: 10px;]

/* Tapez pour remplacer */
```

### Copier/Coller avec multicurseur

Vous pouvez copier différents textes et les coller à différents curseurs.

**Exemple** :
```html
<!-- 3 lignes vides avec 3 curseurs -->



<!-- Vous avez copié précédemment 3 lignes différentes -->
<!-- Collez avec Ctrl/⌘ + V -->
<h1>Titre 1</h1>
<h2>Titre 2</h2>
<h3>Titre 3</h3>
```

---

## Sélection avancée

VS Code offre des outils puissants pour sélectionner intelligemment du texte.

### Sélection par expansion (Shift + Alt/Option + →)

**Raccourci** : `Shift + Alt + →` (Windows/Linux) ou `Shift + Option + →` (macOS)

**Comment ça marche** :
VS Code sélectionne intelligemment par "niveaux" :
1. Mot
2. Expression
3. Ligne
4. Bloc
5. Fonction/Section

**Exemple en HTML** :

```html
<div class="container">
  <h1>Titre</h1>
  <p>Paragraphe</p>
</div>
```

Curseur sur "Titre" :
1. `Shift + Alt + →` : sélectionne "Titre"
2. `Shift + Alt + →` : sélectionne `<h1>Titre</h1>`
3. `Shift + Alt + →` : sélectionne tout le contenu de la div
4. `Shift + Alt + →` : sélectionne toute la div

**Pour réduire** : `Shift + Alt + ←`

**Pourquoi c'est utile** : Sélection rapide sans avoir à cliquer-glisser précisément.

---

### Sélection de ligne (Ctrl/⌘ + L)

**Raccourci** : `Ctrl + L` (Windows/Linux) ou `⌘ + L` (macOS)

**Comment ça marche** :
1. Appuyez sur `Ctrl/⌘ + L` : sélectionne la ligne entière
2. Appuyez à nouveau : sélectionne la ligne suivante aussi
3. Continuez pour sélectionner plusieurs lignes consécutives

**Exemple** :

```javascript
function hello() {
  console.log("Hello");    // Curseur ici
  return true;
}
```

1. `Ctrl/⌘ + L` : sélectionne `console.log("Hello");`
2. `Ctrl/⌘ + L` : sélectionne aussi `return true;`

**Alternative avec multicurseur** : Utilisez `Ctrl/⌘ + L` puis créez des curseurs sur les lignes sélectionnées.

---

### Sélectionner jusqu'à un caractère (Shift + Recherche)

**Raccourci** : `Ctrl/⌘ + F` puis `Shift + Entrée`

**Comment ça marche** :
1. Ouvrez la recherche (`Ctrl/⌘ + F`)
2. Tapez le caractère que vous cherchez
3. `Shift + Entrée` : sélectionne du curseur jusqu'à l'occurrence trouvée

**Exemple** :

```javascript
const user = { name: "Jean", age: 25, city: "Paris" };
```

Curseur après `{` :
1. `Ctrl/⌘ + F` → tapez `,`
2. `Shift + Entrée` : sélectionne ` name: "Jean"`

**Utile pour** : Sélectionner rapidement entre deux caractères.

---

### Sélectionner tout entre des balises (HTML)

**Raccourci** : Utilisez `Shift + Alt + →` intelligemment ou Emmet

**En HTML**, VS Code comprend la structure des balises.

```html
<div>
  <p>Texte important</p>
</div>
```

Curseur dans le `<p>` :
1. `Shift + Alt + →` : sélectionne "Texte important"
2. `Shift + Alt + →` : sélectionne `<p>Texte important</p>`
3. `Shift + Alt + →` : sélectionne tout le contenu de `<div>`

---

## Cas d'usage pratiques

Voyons des exemples concrets d'utilisation du multicurseur dans le développement web.

### Cas 1 : Ajouter une classe à plusieurs éléments HTML

**Situation** :
```html
<div>
  <p>Paragraphe 1</p>
  <p>Paragraphe 2</p>
  <p>Paragraphe 3</p>
  <p>Paragraphe 4</p>
</div>
```

**Objectif** : Ajouter `class="text"` à tous les `<p>`

**Solution avec multicurseur** :
1. Double-cliquez sur le premier `p` (dans `<p>`)
2. `Ctrl/⌘ + Shift + L` : sélectionne tous les `p`
3. `→` pour aller après `p`
4. Tapez ` class="text"`

**Résultat** :
```html
<div>
  <p class="text">Paragraphe 1</p>
  <p class="text">Paragraphe 2</p>
  <p class="text">Paragraphe 3</p>
  <p class="text">Paragraphe 4</p>
</div>
```

---

### Cas 2 : Transformer une liste en HTML

**Situation** :
```
Pommes
Bananes
Oranges
Fraises
Kiwis
```

**Objectif** : Transformer en liste HTML `<li>`

**Solution avec multicurseur** :
1. `Ctrl/⌘ + A` : sélectionner tout
2. `Ctrl/⌘ + Shift + L` : curseur sur chaque ligne
3. `Home` : aller au début de chaque ligne
4. Tapez `<li>`
5. `End` : aller à la fin de chaque ligne
6. Tapez `</li>`

**Résultat** :
```html
<li>Pommes</li>
<li>Bananes</li>
<li>Oranges</li>
<li>Fraises</li>
<li>Kiwis</li>
```

---

### Cas 3 : Modifier plusieurs valeurs CSS identiques

**Situation** :
```css
.button {
  padding: 10px;
  margin: 10px;
  border-radius: 10px;
}
```

**Objectif** : Remplacer tous les `10px` par `15px`

**Solution avec multicurseur** :
1. Double-cliquez sur le premier `10`
2. `Ctrl/⌘ + D` deux fois pour sélectionner les autres
3. Tapez `15`

**Résultat** :
```css
.button {
  padding: 15px;
  margin: 15px;
  border-radius: 15px;
}
```

---

### Cas 4 : Ajouter des guillemets autour de mots

**Situation** :
```javascript
const fruits = [Pomme, Banane, Orange, Fraise];
```

**Objectif** : Ajouter des guillemets autour de chaque fruit

**Solution avec multicurseur** :
1. `Alt/Option + Clic` avant chaque mot (Pomme, Banane, etc.)
2. Tapez `"`
3. `Ctrl/⌘ + →` pour aller à la fin de chaque mot
4. Tapez `"`

**Résultat** :
```javascript
const fruits = ["Pomme", "Banane", "Orange", "Fraise"];
```

---

### Cas 5 : Créer des constantes JavaScript

**Situation** :
```
userName
userAge
userCity
userEmail
```

**Objectif** : Transformer en déclarations `const`

**Solution avec multicurseur** :
1. Sélectionnez toutes les lignes
2. `Ctrl/⌘ + Shift + L` : curseur sur chaque ligne
3. `Home` : début de ligne
4. Tapez `const `
5. `End` : fin de ligne
6. Tapez ` = "";`

**Résultat** :
```javascript
const userName = "";
const userAge = "";
const userCity = "";
const userEmail = "";
```

---

### Cas 6 : Incrémenter des nombres

**Situation** :
```html
<div id="item-1"></div>
<div id="item-1"></div>
<div id="item-1"></div>
<div id="item-1"></div>
```

**Objectif** : Incrémenter les numéros (1, 2, 3, 4)

**Solution** :
Malheureusement, VS Code n'a pas de fonction d'incrémentation automatique native. Vous devez :
1. Utiliser l'extension **"Increment Selection"**
2. Ou modifier manuellement chaque numéro

**Alternative** : Utilisez la recherche/remplacement avec regex.

---

### Cas 7 : Commenter plusieurs lignes différentes

**Situation** :
```javascript
function calculate() {
  const a = 10;
  const b = 20;
  const c = 30;
  return a + b + c;
}
```

**Objectif** : Commenter les lignes de constantes seulement

**Solution avec multicurseur** :
1. `Alt/Option + Clic` au début de chaque ligne `const`
2. `Ctrl/⌘ + /` : commente toutes les lignes sélectionnées

**Résultat** :
```javascript
function calculate() {
  // const a = 10;
  // const b = 20;
  // const c = 30;
  return a + b + c;
}
```

---

### Cas 8 : Ajouter des virgules en fin de ligne

**Situation** :
```javascript
const colors = [
  "red"
  "blue"
  "green"
  "yellow"
];
```

**Objectif** : Ajouter une virgule à la fin de chaque ligne (sauf la dernière)

**Solution avec multicurseur** :
1. `Ctrl/⌘ + Alt/Option + ↓` depuis "red" jusqu'à "green"
2. `End` : aller à la fin de chaque ligne
3. Tapez `,`

**Résultat** :
```javascript
const colors = [
  "red",
  "blue",
  "green",
  "yellow"
];
```

---

## Astuces et bonnes pratiques

### 1. Combiner multicurseur avec les raccourcis d'édition

Tous les raccourcis que vous connaissez fonctionnent avec le multicurseur :
- `Ctrl/⌘ + D` : dupliquer
- `Alt/Option + ↑↓` : déplacer les lignes
- `Ctrl/⌘ + /` : commenter
- `Tab` / `Shift + Tab` : indenter / désindenter

**Exemple** :
```html
<p>Texte 1</p>
<p>Texte 2</p>
<p>Texte 3</p>
```

1. Sélectionnez les 3 lignes
2. `Ctrl/⌘ + Shift + L` : curseur sur chaque ligne
3. `Tab` : indente toutes les lignes
4. `Home` : début de ligne
5. Tapez `<li>` sur toutes les lignes
6. `End` puis Backspace 4 fois : supprime `</p>`
7. Tapez `</li>`

---

### 2. Annuler la dernière sélection avec Ctrl/⌘ + U

Si vous avez sélectionné une occurrence de trop avec `Ctrl/⌘ + D`, utilisez **`Ctrl/⌘ + U`** pour annuler la dernière sélection.

**Exemple** :
```javascript
const name = "Jean";
const name = "Marie";
const name = "Pierre";
const age = 25;  // Oups, "name" dans un commentaire !
```

1. Double-cliquez sur le premier `name`
2. `Ctrl/⌘ + D` trois fois
3. Le 4ème "name" (dans le commentaire) est sélectionné par erreur
4. `Ctrl/⌘ + U` : annule la dernière sélection
5. Maintenant, seuls les 3 premiers "name" sont sélectionnés

---

### 3. Échapper du multicurseur avec Échap

Pour quitter le mode multicurseur et revenir à un seul curseur, appuyez sur **`Échap`** (Escape).

---

### 4. Utiliser le multicurseur avec la recherche

La recherche (`Ctrl/⌘ + F`) fonctionne très bien avec le multicurseur.

**Astuce** :
1. Recherchez un mot avec `Ctrl/⌘ + F`
2. `Alt/Option + Entrée` : crée un curseur sur **chaque occurrence** trouvée !
3. Fermez la recherche et éditez toutes les occurrences

---

### 5. Visualiser tous les curseurs

Quand vous avez beaucoup de curseurs, il peut être difficile de tous les voir. VS Code affiche le **nombre de curseurs** dans la barre d'état en bas :

```
Ln 15, Col 8    (3 sélections)
```

Cela vous indique que vous avez 3 curseurs actifs.

---

### 6. Savoir quand utiliser le multicurseur

**Utilisez le multicurseur quand** :
- ✅ Vous devez faire la **même modification** à plusieurs endroits
- ✅ Les modifications sont **similaires** mais pas identiques
- ✅ Vous voulez gagner du temps sur des tâches répétitives

**N'utilisez PAS le multicurseur quand** :
- ❌ Une recherche/remplacement simple suffit
- ❌ Les modifications sont trop différentes d'une ligne à l'autre
- ❌ Vous n'êtes pas sûr des endroits à modifier (risque d'erreurs)

---

### 7. Pratiquer avec des exemples simples

Le multicurseur peut sembler déroutant au début. **Pratiquez sur des exemples simples** :

```html
<!-- Exercice simple -->
<div>A</div>
<div>B</div>
<div>C</div>

<!-- Transformez en : -->
<div class="box">A</div>
<div class="box">B</div>
<div class="box">C</div>
```

Une fois à l'aise, passez à des cas plus complexes.

---

### 8. Combiner avec Emmet (HTML/CSS)

Le multicurseur fonctionne avec **Emmet** (nous verrons Emmet plus tard).

**Exemple** :
```
div.item*3
```
Tapez `Tab` et Emmet génère :
```html
<div class="item"></div>
<div class="item"></div>
<div class="item"></div>
```

Vous pouvez ensuite utiliser le multicurseur pour personnaliser chaque div.

---

### 9. Méfiez-vous des modifications globales

Quand vous utilisez `Ctrl/⌘ + Shift + L` (tout sélectionner), **vérifiez bien** que vous ne modifiez pas accidentellement d'autres mots.

**Exemple à éviter** :
```javascript
const container = document.getElementById("container");
// container est un élément DOM

function showContainer() {
  container.style.display = "block";
}
```

Si vous sélectionnez tous les "container" et les remplacez aveuglément, vous pourriez casser votre code.

**Solution** : Utilisez `Ctrl/⌘ + D` pour sélectionner individuellement et contrôler ce que vous modifiez.

---

## Comparaison : Multicurseur vs Rechercher/Remplacer

### Quand utiliser le multicurseur

**Avantages** :
- ✅ Modifications visuelles et interactives
- ✅ Contrôle précis (vous voyez ce que vous modifiez)
- ✅ Idéal pour des patterns complexes
- ✅ Modifications contextuelles

**Exemple** : Transformer une structure de données

### Quand utiliser Rechercher/Remplacer

**Avantages** :
- ✅ Plus rapide pour des remplacements simples
- ✅ Fonctionne sur plusieurs fichiers
- ✅ Support des regex avancées

**Exemple** : Remplacer toutes les occurrences d'un mot dans tout le projet

**En résumé** :
- **Multicurseur** : modifications visuelles et contextuelles
- **Rechercher/Remplacer** : modifications massives et simples

---

## Extensions utiles pour le multicurseur

### 1. Increment Selection

**Nom** : Increment Selection

**À quoi ça sert** :
Incrémenter automatiquement des nombres ou des lettres avec le multicurseur.

**Exemple** :
```html
<div id="item-1"></div>
<div id="item-1"></div>
<div id="item-1"></div>
```

Avec l'extension, vous pouvez incrémenter automatiquement pour obtenir :
```html
<div id="item-1"></div>
<div id="item-2"></div>
<div id="item-3"></div>
```

---

### 2. Multiple Cursor Case Preserve

**Nom** : Multiple Cursor Case Preserve

**À quoi ça sert** :
Préserver la casse (majuscules/minuscules) lors du remplacement avec multicurseur.

**Exemple** :
```javascript
const userName = "Jean";
const UserName = "Marie";
```

Remplacer `Name` en préservant la casse pour obtenir `userEmail` et `UserEmail`.

---

## Dépannage : problèmes courants

### Problème 1 : Les curseurs disparaissent

**Cause** : Vous avez appuyé sur `Échap` ou cliqué quelque part.

**Solution** : Recommencez la création des curseurs.

---

### Problème 2 : Trop de curseurs créés

**Cause** : Vous avez utilisé `Ctrl/⌘ + Shift + L` sur un mot très courant.

**Solution** :
- Appuyez sur `Échap` pour annuler
- Utilisez `Ctrl/⌘ + D` pour sélectionner progressivement
- Ou utilisez Rechercher/Remplacer avec plus de spécificité

---

### Problème 3 : Les curseurs ne sont pas alignés

**Cause** : Utilisation incorrecte de la méthode `Ctrl/⌘ + Alt/Option + ↑↓`.

**Solution** : Utilisez plutôt `Alt/Option + Clic` pour placer manuellement les curseurs exactement où vous voulez.

---

### Problème 4 : Modification accidentelle de code

**Cause** : Multicurseur créé sur des zones non voulues.

**Solution** :
- `Ctrl/⌘ + Z` : annuler
- Soyez plus sélectif avec `Ctrl/⌘ + D` plutôt que `Ctrl/⌘ + Shift + L`

---

## Exercices de pratique (pour chez vous)

Voici quelques exercices pour vous entraîner au multicurseur :

### Exercice 1 : Ajouter des classes
```html
<div>Contenu 1</div>
<div>Contenu 2</div>
<div>Contenu 3</div>
```
Transformez en : `<div class="box">Contenu X</div>`

### Exercice 2 : Créer des variables
```
nom
prenom
email
telephone
```
Transformez en : `const nom = "";` (pour chaque ligne)

### Exercice 3 : Modifier des valeurs CSS
```css
.element {
  width: 100px;
  height: 100px;
  margin: 100px;
  padding: 100px;
}
```
Remplacez tous les `100px` par `150px`

### Exercice 4 : Formater une liste
```
Pommes
Bananes
Oranges
Fraises
```
Transformez en liste HTML `<ul><li>...</li></ul>`

---

## Récapitulatif

### Les 6 méthodes de création de multicurseurs

| Méthode | Raccourci | Quand l'utiliser |
|---------|-----------|------------------|
| Clic | `Alt/Option + Clic` | Précision, emplacements spécifiques |
| Lignes ↑↓ | `Ctrl/⌘ + Alt/Option + ↑↓` | Lignes consécutives |
| Occurrence suivante | `Ctrl/⌘ + D` | Mot par mot, contrôle granulaire |
| Toutes les occurrences | `Ctrl/⌘ + Shift + L` | Remplacement massif d'un mot |
| Colonne | `Alt/Option + Shift + Glisser` | Sélection rectangulaire |
| Recherche | `Ctrl/⌘ + F` puis `Alt/Option + Entrée` | Avec pattern de recherche |

### Actions possibles avec multicurseur

- ✅ Taper du texte
- ✅ Supprimer du texte
- ✅ Se déplacer avec les flèches
- ✅ Sélectionner avec Shift + Flèches
- ✅ Copier/Coller
- ✅ Utiliser tous les raccourcis d'édition
- ✅ Indenter/Désindenter
- ✅ Commenter/Décommenter

### Raccourcis importants

- `Échap` : quitter le multicurseur
- `Ctrl/⌘ + U` : annuler la dernière sélection
- `Shift + Alt/Option + →` : sélection intelligente
- `Ctrl/⌘ + L` : sélectionner la ligne

---

## Ce que vous savez faire maintenant

Félicitations ! Vous maîtrisez maintenant :

- ✅ Le **concept de multicurseur** et son utilité
- ✅ Les **6 méthodes** pour créer des multicurseurs
- ✅ Comment **éditer** avec plusieurs curseurs simultanés
- ✅ La **sélection avancée** et intelligente
- ✅ Des **cas d'usage pratiques** du monde réel
- ✅ Les **astuces et bonnes pratiques**
- ✅ Comment **éviter les erreurs** courantes

Le multicurseur est une compétence qui **s'améliore avec la pratique**. Plus vous l'utiliserez, plus il deviendra naturel et vous gagnerez en rapidité !

---

## Pour aller plus loin

### Vidéos recommandées
- Cherchez "VS Code multiple cursors tutorial" sur YouTube
- Vidéos officielles sur la chaîne "Visual Studio Code"

### Articles
- Documentation officielle : https://code.visualstudio.com/docs/editor/codebasics#_multiple-selections-multicursor
- Blog posts sur les techniques avancées

### Pratiquez quotidiennement
Essayez d'utiliser le multicurseur **au moins une fois par jour** sur votre code. Vous verrez rapidement des opportunités de l'utiliser !

---

## Navigation


**➡️ Section suivante :** [2.2.3 Formatage automatique du code](./03-formatage-automatique.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Le multicurseur est une superpuissance de VS Code. Une fois maîtrisé, vous ne pourrez plus vous en passer !* ⚡✨

⏭️ [Formatage automatique du code](/02-environnement-de-developpement/02-maitrise-de-lediteur/03-formatage-automatique.md)
