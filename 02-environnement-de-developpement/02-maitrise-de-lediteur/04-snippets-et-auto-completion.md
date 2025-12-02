🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.2.4 Snippets et auto-complétion

## Introduction

Imaginez pouvoir écrire des dizaines de lignes de code en tapant seulement quelques lettres. C'est exactement ce que permettent les **snippets** et l'**auto-complétion** dans VS Code. Ces fonctionnalités transforment votre façon de coder et vous font gagner un temps considérable.

### Qu'est-ce que l'auto-complétion ?

L'**auto-complétion** (ou IntelliSense dans VS Code) est une fonctionnalité qui :
- Suggère automatiquement du code pendant que vous tapez
- Affiche des propositions intelligentes basées sur le contexte
- Complète automatiquement les mots, les fonctions, les propriétés

**Exemple simple** :
```javascript
// Vous tapez : cons
// VS Code suggère : console, const, constructor...
// Vous sélectionnez "console" avec les flèches
// Appuyez sur Tab ou Entrée : "console" est inséré
```

**C'est comme la prédiction de texte** sur votre téléphone, mais pour le code !

### Qu'est-ce qu'un snippet ?

Un **snippet** (extrait de code en français) est un **modèle de code pré-écrit** que vous pouvez insérer rapidement.

**Exemple** :
```html
<!-- Vous tapez : ! puis Tab -->
<!-- VS Code génère automatiquement : -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

**En tapant 2 caractères**, vous obtenez 13 lignes de code !

### Pourquoi c'est révolutionnaire ?

**Sans snippets et auto-complétion** :
- ❌ Vous tapez tout manuellement
- ❌ Vous faites des fautes de frappe
- ❌ Vous oubliez la syntaxe exacte
- ❌ Vous perdez du temps sur du code répétitif
- ❌ Vous consultez la documentation constamment

**Avec snippets et auto-complétion** :
- ✅ Vous écrivez 10x plus vite
- ✅ Plus d'erreurs de syntaxe
- ✅ La syntaxe correcte est suggérée automatiquement
- ✅ Concentration sur la logique, pas la forme
- ✅ Code cohérent et professionnel

**Gain de productivité** : Facilement **50% de temps économisé** !

---

## Auto-complétion : IntelliSense

### Comment ça marche ?

VS Code analyse constamment votre code et affiche des suggestions intelligentes pendant que vous tapez.

**Vous verrez apparaître** :
- Une petite fenêtre avec des suggestions
- Des icônes indiquant le type (fonction, propriété, snippet, mot-clé...)
- Une description de l'élément suggéré

### Activer l'auto-complétion

**Normalement**, l'auto-complétion est activée par défaut dans VS Code.

**Si elle ne fonctionne pas**, vérifiez :

**Paramètres à vérifier** :
```json
{
  "editor.quickSuggestions": {
    "other": true,
    "comments": false,
    "strings": false
  },
  "editor.suggestOnTriggerCharacters": true,
  "editor.acceptSuggestionOnEnter": "on",
  "editor.tabCompletion": "on"
}
```

### Déclencher l'auto-complétion manuellement

Parfois, l'auto-complétion ne se déclenche pas automatiquement.

**Raccourci** : `Ctrl + Espace` (Windows/Linux) ou `Ctrl + Espace` (macOS)

**Utilisation** :
1. Tapez quelques lettres
2. Appuyez sur `Ctrl + Espace`
3. Une liste de suggestions apparaît
4. Naviguez avec ↑↓
5. Appuyez sur `Tab` ou `Entrée` pour insérer

**Exemple** :
```css
/* Tapez "bo" puis Ctrl + Espace */
bo
  ↓
border
border-radius
border-color
border-width
...
```

### Naviguer dans les suggestions

**Avec le clavier** (recommandé) :
- `↑` / `↓` : Naviguer dans la liste
- `Tab` ou `Entrée` : Accepter la suggestion
- `Échap` : Fermer les suggestions

**Avec la souris** :
- Cliquez sur la suggestion souhaitée

**Astuce** : Utilisez le clavier pour rester rapide !

### Types de suggestions

VS Code affiche différents types de suggestions avec des icônes :

| Icône | Type | Exemple |
|-------|------|---------|
| 📘 | Mot-clé | `const`, `if`, `function` |
| 📦 | Variable | `userName`, `count` |
| 🔧 | Fonction | `console.log()`, `alert()` |
| 📄 | Propriété | `style`, `innerHTML` |
| 🏷️ | Balise HTML | `<div>`, `<span>` |
| ⚡ | Snippet | `for`, `while`, `!` |
| 🎨 | Classe CSS | `.container`, `.button` |

---

## Snippets natifs de VS Code

VS Code inclut des snippets par défaut pour HTML, CSS et JavaScript.

### Snippets HTML

#### Snippet `!` : Structure HTML complète

**Tapez** : `!` puis `Tab`

**Résultat** :
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  |
</body>
</html>
```

Le curseur `|` est positionné dans le `<body>`.

**C'est le snippet le plus utilisé !**

---

#### Snippet `link` : Lien vers CSS

**Tapez** : `link` puis `Tab`

**Résultat** :
```html
<link rel="stylesheet" href="|">
```

Ensuite, tapez le chemin de votre fichier CSS.

---

#### Snippet `script` : Balise script

**Tapez** : `script:src` puis `Tab`

**Résultat** :
```html
<script src="|"></script>
```

---

#### Snippet `meta` : Balises meta

**Tapez** : `meta:vp` puis `Tab`

**Résultat** :
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

### Snippets CSS

#### Snippet `m` : Margin

**Tapez** : `m` puis `Tab`

**Résultat** :
```css
margin: |;
```

Ensuite, tapez la valeur (ex: `10px`).

**Variantes** :
- `mt` : margin-top
- `mr` : margin-right
- `mb` : margin-bottom
- `ml` : margin-left

---

#### Snippet `p` : Padding

**Tapez** : `p` puis `Tab`

**Résultat** :
```css
padding: |;
```

**Variantes** :
- `pt` : padding-top
- `pr` : padding-right
- `pb` : padding-bottom
- `pl` : padding-left

---

#### Snippet `d` : Display

**Tapez** : `df` puis `Tab`

**Résultat** :
```css
display: flex;
```

**Variantes** :
- `db` : display: block;
- `di` : display: inline;
- `dib` : display: inline-block;
- `dn` : display: none;

---

### Snippets JavaScript

#### Snippet `log` : console.log()

**Tapez** : `log` puis `Tab`

**Résultat** :
```javascript
console.log(|);
```

Le curseur est à l'intérieur des parenthèses.

---

#### Snippet `for` : Boucle for

**Tapez** : `for` puis `Tab`

**Résultat** :
```javascript
for (let index = 0; index < array.length; index++) {
  const element = array[index];
  |
}
```

**Vous pouvez ensuite** :
- Modifier `array` (nom du tableau)
- Modifier `element` (nom de l'élément)
- Écrire le code dans la boucle

---

#### Snippet `fori` : Boucle for inversée

**Tapez** : `fori` puis `Tab`

**Résultat** :
```javascript
for (let index = array.length - 1; index >= 0; index--) {
  const element = array[index];
  |
}
```

Boucle qui parcourt le tableau à l'envers.

---

#### Snippet `if` : Condition if

**Tapez** : `if` puis `Tab`

**Résultat** :
```javascript
if (condition) {
  |
}
```

---

#### Snippet `ife` : If-else

**Tapez** : `ife` puis `Tab`

**Résultat** :
```javascript
if (condition) {
  |
} else {

}
```

---

#### Snippet `fn` : Fonction

**Tapez** : `fn` puis `Tab`

**Résultat** :
```javascript
function name(params) {
  |
}
```

---

#### Snippet `afn` : Arrow function

**Tapez** : `afn` puis `Tab`

**Résultat** :
```javascript
const name = (params) => {
  |
}
```

---

## Emmet : Le super-pouvoir HTML/CSS

### Qu'est-ce qu'Emmet ?

**Emmet** est un plugin intégré à VS Code qui permet de créer du **HTML et CSS à vitesse supersonique** avec des abréviations.

**Exemple magique** :
```
div.container>h1+p*3
```
Appuyez sur `Tab`, et cela génère :
```html
<div class="container">
  <h1></h1>
  <p></p>
  <p></p>
  <p></p>
</div>
```

**En une seule ligne**, vous créez une structure complète !

### Syntaxe de base Emmet

#### Créer un élément

**Tapez** : `div` puis `Tab`
**Résultat** :
```html
<div></div>
```

**Fonctionne avec toutes les balises** : `p`, `h1`, `ul`, `section`, etc.

---

#### Ajouter une classe

**Tapez** : `div.container` puis `Tab`
**Résultat** :
```html
<div class="container"></div>
```

**Plusieurs classes** :
**Tapez** : `div.container.main.active` puis `Tab`
**Résultat** :
```html
<div class="container main active"></div>
```

---

#### Ajouter un ID

**Tapez** : `div#header` puis `Tab`
**Résultat** :
```html
<div id="header"></div>
```

---

#### Combiner classe et ID

**Tapez** : `div#header.container` puis `Tab`
**Résultat** :
```html
<div id="header" class="container"></div>
```

---

#### Ajouter des attributs

**Tapez** : `a[href="https://google.com"]` puis `Tab`
**Résultat** :
```html
<a href="https://google.com"></a>
```

**Plusieurs attributs** :
**Tapez** : `img[src="logo.png" alt="Logo"]` puis `Tab`
**Résultat** :
```html
<img src="logo.png" alt="Logo">
```

---

#### Ajouter du texte

**Tapez** : `p{Bonjour le monde}` puis `Tab`
**Résultat** :
```html
<p>Bonjour le monde</p>
```

---

### Opérateurs Emmet

#### Opérateur `>` : Enfant

**Tapez** : `div>p` puis `Tab`
**Résultat** :
```html
<div>
  <p></p>
</div>
```

**Plusieurs niveaux** :
**Tapez** : `div>ul>li` puis `Tab`
**Résultat** :
```html
<div>
  <ul>
    <li></li>
  </ul>
</div>
```

---

#### Opérateur `+` : Frère

**Tapez** : `h1+p` puis `Tab`
**Résultat** :
```html
<h1></h1>
<p></p>
```

**Plusieurs frères** :
**Tapez** : `h1+p+p+ul` puis `Tab`
**Résultat** :
```html
<h1></h1>
<p></p>
<p></p>
<ul></ul>
```

---

#### Opérateur `^` : Remonter d'un niveau

**Tapez** : `div>p>span^p` puis `Tab`
**Résultat** :
```html
<div>
  <p><span></span></p>
  <p></p>
</div>
```

Le `^` remonte d'un niveau (sort du `<p>`).

**Remonter de deux niveaux** : `^^`

---

#### Opérateur `*` : Multiplication

**Tapez** : `li*5` puis `Tab`
**Résultat** :
```html
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
```

**Avec structure** :
**Tapez** : `ul>li*3` puis `Tab`
**Résultat** :
```html
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

---

#### Opérateur `()` : Groupement

**Tapez** : `div>(header>h1)+footer` puis `Tab`
**Résultat** :
```html
<div>
  <header>
    <h1></h1>
  </header>
  <footer></footer>
</div>
```

Les parenthèses permettent de **grouper des éléments**.

---

#### Opérateur `$` : Numérotation

**Tapez** : `ul>li.item$*3` puis `Tab`
**Résultat** :
```html
<ul>
  <li class="item1"></li>
  <li class="item2"></li>
  <li class="item3"></li>
</ul>
```

Le `$` est remplacé par le numéro.

**Commencer à 0** : `$@0`
**Tapez** : `ul>li.item$@0*3` puis `Tab`
**Résultat** :
```html
<ul>
  <li class="item0"></li>
  <li class="item1"></li>
  <li class="item2"></li>
</ul>
```

**Numérotation inversée** : `$@-`
**Tapez** : `ul>li.item$@-*3` puis `Tab`
**Résultat** :
```html
<ul>
  <li class="item3"></li>
  <li class="item2"></li>
  <li class="item1"></li>
</ul>
```

---

### Exemples Emmet avancés

#### Exemple 1 : Navigation complète

**Tapez** :
```
nav>ul>li*4>a[href="#"]{Menu $}
```

**Résultat** :
```html
<nav>
  <ul>
    <li><a href="#">Menu 1</a></li>
    <li><a href="#">Menu 2</a></li>
    <li><a href="#">Menu 3</a></li>
    <li><a href="#">Menu 4</a></li>
  </ul>
</nav>
```

---

#### Exemple 2 : Grille de cartes

**Tapez** :
```
div.container>div.card*6>h3.title{Titre $}+p.text{Description}
```

**Résultat** :
```html
<div class="container">
  <div class="card">
    <h3 class="title">Titre 1</h3>
    <p class="text">Description</p>
  </div>
  <div class="card">
    <h3 class="title">Titre 2</h3>
    <p class="text">Description</p>
  </div>
  <!-- ... 4 autres cartes ... -->
</div>
```

---

#### Exemple 3 : Formulaire

**Tapez** :
```
form>div.form-group*3>label+input:text
```

**Résultat** :
```html
<form>
  <div class="form-group">
    <label for=""></label>
    <input type="text" name="" id="">
  </div>
  <div class="form-group">
    <label for=""></label>
    <input type="text" name="" id="">
  </div>
  <div class="form-group">
    <label for=""></label>
    <input type="text" name="" id="">
  </div>
</form>
```

---

### Emmet en CSS

Emmet fonctionne aussi en CSS !

**Exemple 1** :
**Tapez** : `m10` puis `Tab`
**Résultat** :
```css
margin: 10px;
```

**Exemple 2** :
**Tapez** : `w100p` puis `Tab`
**Résultat** :
```css
width: 100%;
```

**Exemple 3** :
**Tapez** : `df` puis `Tab`
**Résultat** :
```css
display: flex;
```

**Exemple 4** :
**Tapez** : `bgc#fff` puis `Tab`
**Résultat** :
```css
background-color: #fff;
```

**Liste des abréviations CSS** :
- `m` : margin
- `p` : padding
- `w` : width
- `h` : height
- `d` : display
- `pos` : position
- `t`, `r`, `b`, `l` : top, right, bottom, left
- `c` : color
- `bg` : background
- `bd` : border
- `fs` : font-size

---

### Configuration Emmet

#### Activer Emmet

Normalement, Emmet est activé par défaut dans VS Code.

**Si ce n'est pas le cas**, vérifiez dans les paramètres :

```json
{
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "vue-html": "html"
  }
}
```

---

#### Changer la touche de déclenchement

Par défaut, Emmet se déclenche avec `Tab`.

**Si vous préférez `Entrée`** :
```json
{
  "emmet.triggerExpansionOnTab": false
}
```

Puis utilisez `Ctrl/⌘ + E` pour déclencher Emmet.

---

## Créer vos propres snippets

Vous pouvez créer des snippets personnalisés pour votre code fréquemment utilisé.

### Accéder aux snippets utilisateur

**Méthode 1 : Via le menu**
1. Fichier → Préférences → Snippets Utilisateur (Windows/Linux)
2. Code → Préférences → Snippets Utilisateur (macOS)

**Méthode 2 : Via la palette**
1. `Ctrl/⌘ + Shift + P`
2. Tapez "Snippets: Configure User Snippets"
3. Choisissez le langage (HTML, CSS, JavaScript, etc.)

**Méthode 3 : Snippet global**
- Choisissez "New Global Snippets file..."
- Nommez votre fichier (ex: `my-snippets.code-snippets`)

---

### Structure d'un snippet

Les snippets sont écrits en **JSON**.

**Structure de base** :
```json
{
  "Nom du snippet": {
    "prefix": "déclencheur",
    "body": [
      "ligne 1 du code",
      "ligne 2 du code"
    ],
    "description": "Description du snippet"
  }
}
```

**Explication** :
- **Nom du snippet** : nom interne (vous pouvez mettre ce que vous voulez)
- **prefix** : ce que vous tapez pour déclencher le snippet
- **body** : le code à insérer (tableau de lignes)
- **description** : description affichée dans l'auto-complétion

---

### Exemple 1 : Console.log avec nom de variable

**Snippet** :
```json
{
  "Console Log with Variable Name": {
    "prefix": "clg",
    "body": [
      "console.log('$1:', $1);"
    ],
    "description": "Log a variable with its name"
  }
}
```

**Utilisation** :
1. Tapez `clg` puis `Tab`
2. Résultat : `console.log('|:', |);`
3. Tapez le nom de la variable (ex: `userName`)
4. Résultat : `console.log('userName:', userName);`

**Explication du `$1`** :
- `$1` est un **tabstop** (point d'arrêt)
- Le curseur s'arrête à cet endroit
- Vous pouvez avoir `$1`, `$2`, `$3`... pour plusieurs arrêts
- Appuyez sur `Tab` pour passer d'un tabstop à l'autre

---

### Exemple 2 : Commentaire d'en-tête

**Snippet** :
```json
{
  "File Header Comment": {
    "prefix": "header",
    "body": [
      "/**",
      " * Fichier: $TM_FILENAME",
      " * Auteur: $1",
      " * Date: $CURRENT_DATE/$CURRENT_MONTH/$CURRENT_YEAR",
      " * Description: $2",
      " */"
    ],
    "description": "Add file header comment"
  }
}
```

**Variables disponibles** :
- `$TM_FILENAME` : nom du fichier
- `$CURRENT_YEAR` : année actuelle
- `$CURRENT_MONTH` : mois actuel
- `$CURRENT_DATE` : jour actuel
- `$CLIPBOARD` : contenu du presse-papier

---

### Exemple 3 : Structure HTML de composant

**Snippet** :
```json
{
  "HTML Component Structure": {
    "prefix": "comp",
    "body": [
      "<div class=\"$1\">",
      "  <h2 class=\"$1__title\">$2</h2>",
      "  <p class=\"$1__text\">$3</p>",
      "</div>"
    ],
    "description": "Create HTML component with BEM naming"
  }
}
```

**Utilisation** :
1. Tapez `comp` puis `Tab`
2. Tapez le nom du composant (ex: `card`)
3. `Tab` : tapez le titre
4. `Tab` : tapez le texte

**Résultat** :
```html
<div class="card">
  <h2 class="card__title">Mon titre</h2>
  <p class="card__text">Mon texte</p>
</div>
```

---

### Exemple 4 : Fonction JavaScript documentée

**Snippet** :
```json
{
  "Documented Function": {
    "prefix": "fndoc",
    "body": [
      "/**",
      " * $1",
      " * @param {$2} $3 - $4",
      " * @returns {$5} $6",
      " */",
      "function $7($3) {",
      "  $0",
      "}"
    ],
    "description": "Function with JSDoc documentation"
  }
}
```

**Tabstops expliqués** :
- `$1` : description de la fonction
- `$2` : type du paramètre
- `$3` : nom du paramètre
- `$4` : description du paramètre
- `$5` : type de retour
- `$6` : description du retour
- `$7` : nom de la fonction
- `$0` : position finale du curseur

---

### Exemple 5 : Snippet CSS avec choix

**Snippet** :
```json
{
  "Flexbox Container": {
    "prefix": "flex",
    "body": [
      "display: flex;",
      "justify-content: ${1|flex-start,center,flex-end,space-between,space-around|};",
      "align-items: ${2|stretch,flex-start,center,flex-end|};",
      "flex-direction: ${3|row,column,row-reverse,column-reverse|};"
    ],
    "description": "Flexbox container with common properties"
  }
}
```

**Explication du `${1|option1,option2,...|}`** :
- Liste de choix pour le tabstop
- Appuyez sur `Tab` et choisissez avec ↑↓
- Appuyez sur `Entrée` pour valider

---

### Snippet avec valeur par défaut

**Snippet** :
```json
{
  "Import React": {
    "prefix": "imr",
    "body": [
      "import React${1:, { useState \\}} from 'react';"
    ],
    "description": "Import React with optional hooks"
  }
}
```

**Explication du `${1:valeur par défaut}`** :
- Si vous appuyez sur `Tab` sans rien taper, la valeur par défaut est gardée
- Si vous tapez quelque chose, cela remplace la valeur par défaut

---

## Extensions de snippets

Il existe de nombreuses extensions qui ajoutent des snippets pour différents frameworks et librairies.

### Extensions populaires

#### 1. JavaScript (ES6) code snippets

**Nom** : JavaScript (ES6) code snippets
**Éditeur** : charalampos karypidis

**Snippets inclus** :
- `imp` : import
- `imd` : import destructured
- `exp` : export
- `clg` : console.log
- `clo` : console.log object
- `dob` : destructuring object
- `dar` : destructuring array
- Et bien plus !

---

#### 2. HTML Snippets

**Nom** : HTML Snippets
**Éditeur** : Mohamed Abusaid

**Snippets inclus** :
- Snippets pour toutes les balises HTML5
- Attributs communs
- Structures courantes

---

#### 3. CSS Snippets

**Nom** : CSS Snippets
**Éditeur** : joy-yu

**Snippets inclus** :
- Propriétés CSS courantes
- Raccourcis pour valeurs communes
- Media queries

---

#### 4. ES7+ React/Redux/React-Native snippets

**Nom** : ES7+ React/Redux/React-Native snippets
**Éditeur** : dsznajder

**Pour plus tard** (quand vous apprendrez React) :
- `rafce` : React Arrow Function Component Export
- `rfc` : React Functional Component
- `useState` : useState Hook
- Et bien plus !

---

## Astuces et bonnes pratiques

### 1. Apprenez progressivement

**Ne tentez pas** de mémoriser tous les snippets d'un coup.

**Méthode recommandée** :
- Semaine 1 : `!` (HTML), `log` (JS), Emmet de base
- Semaine 2 : Snippets CSS, Emmet avancé
- Semaine 3 : Créez vos propres snippets
- Semaine 4+ : Explorez les extensions de snippets

---

### 2. Explorez les snippets disponibles

**Pour voir tous les snippets disponibles** :
1. Tapez quelques lettres
2. `Ctrl + Espace` pour voir les suggestions
3. Les snippets ont une icône ⚡
4. Lisez les descriptions

---

### 3. Utilisez Tab vs Entrée

**Tab** : Accepte la suggestion et se déplace au tabstop suivant
**Entrée** : Accepte la suggestion et crée une nouvelle ligne

**Recommandation** : Utilisez `Tab` pour les snippets (c'est plus intuitif).

---

### 4. Créez des snippets pour votre code répétitif

**Identifiez** le code que vous écrivez souvent :
- Structures HTML répétitives
- Fonctions JavaScript similaires
- Styles CSS récurrents

**Créez un snippet** pour gagner du temps !

---

### 5. Partagez vos snippets avec votre équipe

Si vous travaillez en équipe, partagez vos snippets :

**Méthode** :
1. Créez un fichier `.code-snippets` dans votre projet
2. Commitez-le dans Git
3. Toute l'équipe a accès aux mêmes snippets

---

### 6. Documentez vos snippets personnalisés

Ajoutez toujours une **description** claire à vos snippets :

```json
{
  "Mon Snippet": {
    "prefix": "monsnip",
    "body": ["..."],
    "description": "⭐ Description claire de ce que fait le snippet"
  }
}
```

Dans 6 mois, vous serez content de savoir ce que fait le snippet !

---

### 7. Utilisez des préfixes courts mais mémorables

**Bons préfixes** :
- `clg` : console.log (court, logique)
- `imp` : import (court, clair)
- `comp` : component (court, mémorable)

**Mauvais préfixes** :
- `x` : trop court, pas clair
- `consolelog` : trop long
- `mycustomsnippetforlogging` : beaucoup trop long !

**Recommandation** : 2-5 caractères

---

### 8. Testez Emmet dans l'onglet "Emmet Preview"

VS Code a un **mode aperçu Emmet** :

1. `Ctrl/⌘ + Shift + P`
2. Tapez "Emmet: Wrap with Abbreviation"
3. Entrez votre abréviation Emmet
4. Voyez le résultat avant de valider

**Très utile** pour tester des abréviations complexes !

---

## Dépannage : problèmes courants

### Problème 1 : L'auto-complétion ne fonctionne pas

**Causes possibles** :
1. Paramètre `editor.quickSuggestions` désactivé
2. Vous êtes dans un fichier non reconnu

**Solution** :
```json
{
  "editor.quickSuggestions": {
    "other": true,
    "comments": false,
    "strings": false
  }
}
```

---

### Problème 2 : Emmet ne se déclenche pas

**Causes possibles** :
1. `emmet.triggerExpansionOnTab` désactivé
2. Vous êtes dans un type de fichier non supporté

**Solution** :
```json
{
  "emmet.triggerExpansionOnTab": true
}
```

---

### Problème 3 : Les snippets personnalisés n'apparaissent pas

**Causes possibles** :
1. Erreur de syntaxe JSON dans le fichier de snippets
2. Mauvais nom de fichier ou emplacement

**Solution** :
1. Vérifiez la syntaxe JSON (virgules, guillemets)
2. Rechargez VS Code
3. Vérifiez que vous êtes dans le bon type de fichier

---

### Problème 4 : Conflit entre snippets

Si plusieurs snippets ont le même `prefix`, ils entreront en conflit.

**Solution** :
- Utilisez des préfixes uniques
- Ou désactivez les snippets d'extensions non utilisées

---

## Comparaison : Avec vs Sans snippets

### Scénario : Créer une page HTML de base

**Sans snippets** :
```
Temps : 2-3 minutes
Risque d'erreur : Élevé (oubli de balises, typos)
```

**Avec snippet `!`** :
```
Temps : 5 secondes (! + Tab)
Risque d'erreur : Aucun
```

**Gain** : **95% de temps économisé !**

---

### Scénario : Créer une navigation avec 5 liens

**Sans Emmet** :
```html
<nav>
  <ul>
    <li><a href="#">Lien 1</a></li>
    <li><a href="#">Lien 2</a></li>
    <li><a href="#">Lien 3</a></li>
    <li><a href="#">Lien 4</a></li>
    <li><a href="#">Lien 5</a></li>
  </ul>
</nav>
```
Temps : 3-5 minutes de frappe

**Avec Emmet** :
```
nav>ul>li*5>a[href="#"]{Lien $}
```
Temps : 10 secondes

**Gain** : **90% de temps économisé !**

---

## Récapitulatif

### Ce que vous savez maintenant

Félicitations ! Vous maîtrisez maintenant :

- ✅ L'**auto-complétion** (IntelliSense) dans VS Code
- ✅ Les **snippets natifs** de HTML, CSS, JavaScript
- ✅ **Emmet** : le super-pouvoir HTML/CSS
- ✅ La **syntaxe Emmet** complète (opérateurs, numérotation)
- ✅ Comment **créer vos propres snippets**
- ✅ Les **extensions de snippets** populaires
- ✅ Les **astuces et bonnes pratiques**
- ✅ Comment **dépanner** les problèmes courants

### Snippets essentiels à retenir

**HTML** :
- `!` : structure HTML complète
- `link` : lien vers CSS
- `script:src` : balise script

**Emmet** :
- `div.class` : div avec classe
- `div>p*3` : structure avec enfants
- `ul>li*5` : liste avec 5 items

**JavaScript** :
- `log` : console.log()
- `for` : boucle for
- `fn` : fonction

**CSS** :
- `m10` : margin: 10px;
- `df` : display: flex;
- `w100p` : width: 100%;

### Les 3 règles d'or

1. 🎯 **Utilisez les snippets quotidiennement** pour qu'ils deviennent naturels
2. ⚡ **Maîtrisez Emmet** pour HTML/CSS (gain de temps énorme)
3. 🛠️ **Créez vos propres snippets** pour votre code répétitif

---

## Pour aller plus loin

### Documentation officielle

**VS Code Snippets** :
- https://code.visualstudio.com/docs/editor/userdefinedsnippets

**Emmet** :
- Site officiel : https://emmet.io
- Cheat Sheet : https://docs.emmet.io/cheat-sheet/
- Documentation : https://docs.emmet.io

### Ressources complémentaires

**Emmet Playground** :
- https://emmet.io/demo/
- Testez vos abréviations Emmet en ligne

**Snippet Generator** :
- https://snippet-generator.app
- Créez des snippets facilement avec une interface visuelle

### Vidéos recommandées

- "Emmet Tutorial" sur YouTube
- "VS Code Snippets" sur la chaîne officielle VS Code

---

## Navigation


**➡️ Section suivante :** [2.2.5 Terminal intégré](./05-terminal-integre.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Avec les snippets et Emmet, vous écrivez du code à la vitesse de la pensée !* ⚡✨

⏭️ [Terminal intégré](/02-environnement-de-developpement/02-maitrise-de-lediteur/05-terminal-integre.md)
