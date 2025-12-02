🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.2.3 Formatage automatique du code

## Introduction

Le **formatage du code** consiste à organiser et présenter votre code de manière lisible, cohérente et professionnelle. Imaginez un livre : même si le contenu est excellent, une mise en page chaotique avec des paragraphes mal alignés et des espaces incohérents rendrait la lecture difficile. C'est pareil avec le code !

### Qu'est-ce qu'un code bien formaté ?

**Code mal formaté** :
```html
<div><h1>Titre</h1><p>Un long paragraphe de texte</p><ul><li>Item 1</li><li>Item 2</li></ul></div>
```

**Code bien formaté** :
```html
<div>
  <h1>Titre</h1>
  <p>Un long paragraphe de texte</p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
</div>
```

**Quelle différence !** Le second est :
- ✅ Plus lisible
- ✅ Plus facile à comprendre
- ✅ Plus facile à maintenir
- ✅ Plus professionnel

### Pourquoi le formatage est crucial ?

#### 1. Lisibilité
Un code bien formaté se lit comme un livre bien mis en page. Vous identifiez immédiatement la structure et les relations entre les éléments.

#### 2. Maintenance
Dans 6 mois, quand vous reviendrez sur votre code, vous comprendrez rapidement ce que vous aviez écrit.

#### 3. Collaboration
Si vous travaillez en équipe, tout le monde doit formater de la même façon. Sinon, c'est le chaos !

#### 4. Professionnalisme
Un code bien formaté montre que vous maîtrisez les standards de l'industrie.

#### 5. Détection d'erreurs
Paradoxalement, un bon formatage aide à repérer les erreurs. Une balise mal fermée devient évidente quand le code est bien indenté.

### Le problème du formatage manuel

**Sans outil automatique**, vous devez :
- ❌ Compter les espaces manuellement
- ❌ Vérifier chaque indentation
- ❌ Aligner les éléments à la main
- ❌ Respecter les conventions (guillemets simples ou doubles ?)
- ❌ Perdre du temps sur la forme plutôt que le fond

**C'est ennuyeux, chronophage et source d'erreurs !**

### La solution : le formatage automatique

Avec VS Code et **Prettier**, le formatage devient :
- ✅ **Automatique** : appuyez sur une touche (ou sauvegardez)
- ✅ **Instantané** : en moins d'une seconde
- ✅ **Cohérent** : toujours les mêmes règles
- ✅ **Sans effort** : vous vous concentrez sur le code, pas la forme

---

## Prettier : l'outil de formatage moderne

### Qu'est-ce que Prettier ?

**Prettier** est un **formateur de code** (code formatter) qui :
- Analyse votre code
- Le réécrit selon des règles cohérentes
- Gère HTML, CSS, JavaScript, JSON, Markdown, et bien plus

**C'est l'outil standard de l'industrie**, utilisé par des millions de développeurs.

### Pourquoi Prettier ?

#### Avantages :
- 🎯 **Opinionated** : des règles déjà définies (pas besoin de choisir)
- ⚡ **Rapide** : formate instantanément
- 🌐 **Multi-langages** : un seul outil pour tout
- 🤝 **Standard** : utilisé partout dans l'industrie
- 🔧 **Configurable** : ajustable si besoin

#### Alternatives :
- **BeautifyJS** : plus ancien, moins utilisé
- **ESLint** avec auto-fix : principalement pour JavaScript
- Formateurs spécifiques par langage

**Notre recommandation** : Prettier pour débuter. C'est simple, efficace et standard.

### Installation de Prettier

Si vous avez suivi la section sur les extensions, vous devriez déjà avoir installé Prettier. Sinon, voici comment faire :

1. **Ouvrir les extensions** : `Ctrl/⌘ + Shift + X`
2. **Chercher** : "Prettier - Code formatter"
3. **Installer** : cliquez sur "Install"
4. **Recharger** VS Code si demandé

**Vérification** : Vous devriez voir Prettier dans votre liste d'extensions installées.

---

## Configuration de base

### Définir Prettier comme formateur par défaut

VS Code peut avoir plusieurs formateurs. Il faut dire à VS Code d'utiliser Prettier.

**Méthode 1 : Via les paramètres**

1. Ouvrez les paramètres : `Ctrl/⌘ + ,`
2. Cherchez : "default formatter"
3. Trouvez : **"Editor: Default Formatter"**
4. Sélectionnez : **"Prettier - Code formatter"** (esbenp.prettier-vscode)

**Méthode 2 : Via le fichier JSON**

1. `Ctrl/⌘ + Shift + P` → "Preferences: Open Settings (JSON)"
2. Ajoutez :
```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

### Activer le formatage à la sauvegarde

**Le plus important** : formater automatiquement quand vous sauvegardez.

**Dans les paramètres** :
1. Ouvrez les paramètres : `Ctrl/⌘ + ,`
2. Cherchez : "format on save"
3. Cochez : **"Editor: Format On Save"**

**Ou dans le JSON** :
```json
{
  "editor.formatOnSave": true
}
```

**Test** :
1. Écrivez du code mal formaté
2. Sauvegardez (`Ctrl/⌘ + S`)
3. Magie ! Le code est reformaté automatiquement 🎉

### Autres options de formatage automatique

**Format On Paste** :
- Formate le code quand vous le collez
- Paramètre : `"editor.formatOnPaste": true`

**Format On Type** :
- Formate pendant que vous tapez
- Paramètre : `"editor.formatOnType": true`
- **Attention** : peut être perturbant, déconseillé pour débuter

**Notre recommandation** : Activez uniquement **Format On Save** au début.

---

## Utiliser Prettier : les bases

### Formater manuellement

Même avec "Format On Save" activé, vous pouvez formater manuellement :

**Raccourci** :
- Windows/Linux : `Shift + Alt + F`
- macOS : `Shift + Option + F`

**Via la palette** :
- `Ctrl/⌘ + Shift + P`
- Tapez "Format Document"
- Appuyez sur `Entrée`

**Clic-droit** :
- Clic-droit dans l'éditeur
- "Format Document" ou "Format Document With..."

### Formater une sélection

Vous pouvez formater seulement une partie du code :

1. **Sélectionnez** le code à formater
2. **Clic-droit** → "Format Selection"
3. Ou raccourci : `Ctrl/⌘ + K, Ctrl/⌘ + F`

**Exemple** :
```javascript
// Sélectionnez seulement la fonction
function calculate(a,b){return a+b;}

// Format Selection
function calculate(a, b) {
  return a + b;
}
```

### Choisir le formateur

Si vous avez plusieurs formateurs installés :

1. **Clic-droit** → "Format Document With..."
2. Choisissez "Prettier - Code formatter"
3. Option : "Configure Default Formatter..." pour changer le défaut

---

## Exemples de formatage

Voyons ce que Prettier fait concrètement sur différents langages.

### HTML

**Avant** :
```html
<div class="container"><h1>Titre</h1><p>Un paragraphe avec <strong>du texte important</strong> dedans.</p><ul><li>Item 1</li><li>Item 2</li></ul></div>
```

**Après Prettier** :
```html
<div class="container">
  <h1>Titre</h1>
  <p>
    Un paragraphe avec <strong>du texte important</strong> dedans.
  </p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
</div>
```

**Ce que Prettier a fait** :
- ✅ Indenté chaque niveau (2 espaces)
- ✅ Mis chaque élément sur sa ligne
- ✅ Respecté la hiérarchie
- ✅ Gardé les éléments inline (`<strong>`) sur la même ligne que leur parent

---

### CSS

**Avant** :
```css
.button{color:red;background:blue;padding:10px 20px;border:none;font-size:16px;}
```

**Après Prettier** :
```css
.button {
  color: red;
  background: blue;
  padding: 10px 20px;
  border: none;
  font-size: 16px;
}
```

**Ce que Prettier a fait** :
- ✅ Espace après le sélecteur
- ✅ Chaque propriété sur sa ligne
- ✅ Espaces autour des deux-points
- ✅ Point-virgule à la fin de chaque ligne

---

### JavaScript

**Avant** :
```javascript
function calculate(a,b,c){const result=a+b+c;if(result>100){return "Grand nombre";}else{return "Petit nombre";}}
```

**Après Prettier** :
```javascript
function calculate(a, b, c) {
  const result = a + b + c;
  if (result > 100) {
    return "Grand nombre";
  } else {
    return "Petit nombre";
  }
}
```

**Ce que Prettier a fait** :
- ✅ Espaces après les virgules
- ✅ Espaces autour des opérateurs (`+`, `>`, `=`)
- ✅ Indentation des blocs
- ✅ Accolades sur de nouvelles lignes
- ✅ Point-virgule à la fin des instructions

---

### JSON

**Avant** :
```json
{"name":"Jean","age":25,"city":"Paris","hobbies":["lecture","sport","musique"]}
```

**Après Prettier** :
```json
{
  "name": "Jean",
  "age": 25,
  "city": "Paris",
  "hobbies": ["lecture", "sport", "musique"]
}
```

**Ce que Prettier a fait** :
- ✅ Chaque propriété sur sa ligne
- ✅ Indentation cohérente
- ✅ Espaces autour des deux-points
- ✅ Les tableaux courts restent sur une ligne

---

## Configuration de Prettier

Prettier fonctionne très bien avec ses paramètres par défaut, mais vous pouvez le personnaliser.

### Les paramètres principaux

#### 1. Taille de l'indentation (Tab Width)

**Paramètre** : `prettier.tabWidth`
**Valeur par défaut** : `2`
**Valeurs possibles** : `2`, `4`, ou autre nombre

**Exemple avec `2`** :
```html
<div>
  <p>Texte</p>
</div>
```

**Exemple avec `4`** :
```html
<div>
    <p>Texte</p>
</div>
```

**Recommandation** : `2` est le standard pour le développement web moderne.

**Configuration** :
```json
{
  "prettier.tabWidth": 2
}
```

---

#### 2. Point-virgule (Semicolon)

**Paramètre** : `prettier.semi`
**Valeur par défaut** : `true`
**Valeurs possibles** : `true`, `false`

**Avec semicolon (`true`)** :
```javascript
const name = "Jean";
console.log(name);
```

**Sans semicolon (`false`)** :
```javascript
const name = "Jean"
console.log(name)
```

**Recommandation** : `true` (avec point-virgule) pour plus de clarté.

**Configuration** :
```json
{
  "prettier.semi": true
}
```

---

#### 3. Guillemets simples ou doubles (Single Quote)

**Paramètre** : `prettier.singleQuote`
**Valeur par défaut** : `false` (guillemets doubles)
**Valeurs possibles** : `true`, `false`

**Guillemets doubles (`false`)** :
```javascript
const message = "Bonjour";
```

**Guillemets simples (`true`)** :
```javascript
const message = 'Bonjour';
```

**Recommandation** : Question de préférence. Les deux sont valides.
- `false` (doubles) : plus courant en JavaScript
- `true` (simples) : plus courant dans certaines conventions

**Configuration** :
```json
{
  "prettier.singleQuote": true
}
```

---

#### 4. Virgule finale (Trailing Comma)

**Paramètre** : `prettier.trailingComma`
**Valeur par défaut** : `"es5"`
**Valeurs possibles** : `"none"`, `"es5"`, `"all"`

**Exemple avec `"es5"`** :
```javascript
const user = {
  name: "Jean",
  age: 25,  // ← virgule finale
};

const colors = ["red", "blue", "green"]; // ← pas de virgule (tableau sur une ligne)
```

**Exemple avec `"all"`** :
```javascript
function hello(a, b, c,) {  // ← virgule même après le dernier paramètre
  console.log(a, b, c);
}
```

**Recommandation** : `"es5"` (valeur par défaut).

**Configuration** :
```json
{
  "prettier.trailingComma": "es5"
}
```

---

#### 5. Largeur de ligne maximale (Print Width)

**Paramètre** : `prettier.printWidth`
**Valeur par défaut** : `80`
**Valeurs possibles** : n'importe quel nombre (généralement 80, 100, 120)

**À quoi ça sert** :
Prettier essaie de limiter la longueur des lignes pour la lisibilité.

**Exemple avec `printWidth: 40`** :
```javascript
// Ligne trop longue, Prettier la découpe
const message =
  "Un message très long";
```

**Exemple avec `printWidth: 80`** :
```javascript
// La ligne tient, Prettier la garde
const message = "Un message très long";
```

**Recommandation** : `80` ou `100` pour le web.

**Configuration** :
```json
{
  "prettier.printWidth": 80
}
```

---

#### 6. Espaces ou tabulations (Use Tabs)

**Paramètre** : `prettier.useTabs`
**Valeur par défaut** : `false` (utilise des espaces)
**Valeurs possibles** : `true`, `false`

**Avec espaces (`false`)** :
```html
<div>
··<p>Texte</p>  ← 2 espaces
</div>
```

**Avec tabulations (`true`)** :
```html
<div>
→	<p>Texte</p>  ← 1 tabulation
</div>
```

**Recommandation** : `false` (espaces) est le standard web.

**Configuration** :
```json
{
  "prettier.useTabs": false
}
```

---

### Configuration complète recommandée

Voici une configuration Prettier optimale pour le développement web :

**Dans les paramètres VS Code** (`settings.json`) :
```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "prettier.tabWidth": 2,
  "prettier.semi": true,
  "prettier.singleQuote": true,
  "prettier.trailingComma": "es5",
  "prettier.printWidth": 80,
  "prettier.useTabs": false,
  "prettier.arrowParens": "always",
  "prettier.bracketSpacing": true,
  "prettier.endOfLine": "lf"
}
```

**Explication** :
- Indentation de 2 espaces
- Point-virgule activé
- Guillemets simples
- Virgule finale style ES5
- Largeur de ligne 80 caractères
- Espaces (pas de tabulations)

---

## Fichier de configuration Prettier (.prettierrc)

### Pourquoi un fichier de configuration ?

Les paramètres dans VS Code sont **personnels** (sur votre machine uniquement).

Un fichier **.prettierrc** est **partagé** avec votre projet :
- ✅ Toute l'équipe utilise les mêmes règles
- ✅ Fonctionne avec d'autres éditeurs
- ✅ Versionné avec Git
- ✅ Standard de l'industrie

### Créer un fichier .prettierrc

**À la racine de votre projet**, créez un fichier nommé `.prettierrc` (sans extension) :

**Format JSON** :
```json
{
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "es5",
  "printWidth": 80,
  "useTabs": false,
  "arrowParens": "always",
  "bracketSpacing": true
}
```

**Format YAML** (.prettierrc.yml) :
```yaml
tabWidth: 2
semi: true
singleQuote: true
trailingComma: es5
printWidth: 80
useTabs: false
```

**Format JavaScript** (.prettierrc.js) :
```javascript
module.exports = {
  tabWidth: 2,
  semi: true,
  singleQuote: true,
  trailingComma: 'es5',
  printWidth: 80,
  useTabs: false,
};
```

**Notre recommandation** : JSON (le plus simple).

### Priorité des configurations

Prettier cherche la configuration dans cet ordre :
1. **.prettierrc** dans le projet (priorité maximale)
2. **package.json** (section "prettier")
3. Paramètres VS Code
4. Configuration par défaut de Prettier

**En résumé** : le fichier .prettierrc dans votre projet **prime sur tout**.

---

## Ignorer des fichiers avec .prettierignore

Certains fichiers ne doivent **pas** être formatés automatiquement.

### Créer .prettierignore

À la racine du projet, créez `.prettierignore` :

```
# Dépendances
node_modules/
vendor/

# Build
dist/
build/
*.min.js
*.min.css

# Fichiers générés
package-lock.json
yarn.lock

# Librairies externes
public/libs/
```

**Syntaxe** : comme .gitignore

### Fichiers à ignorer couramment

- ✅ **node_modules/** : dépendances externes
- ✅ **dist/** ou **build/** : code compilé
- ✅ **Fichiers minifiés** (.min.js, .min.css)
- ✅ **Fichiers de lock** (package-lock.json)
- ✅ **Documentation générée**

---

## Formatage spécifique par langage

### HTML : options spéciales

**Prettier peut gérer les spécificités HTML** :

```json
{
  "prettier.htmlWhitespaceSensitivity": "css"
}
```

**Valeurs possibles** :
- `"css"` : suit les règles CSS (recommandé)
- `"strict"` : respecte tous les espaces
- `"ignore"` : ignore les espaces blancs

**Exemple avec `"css"`** :
```html
<!-- Prettier garde l'inline approprié -->
<p>Texte avec <strong>emphase</strong> dedans.</p>
```

**Exemple avec `"strict"`** :
```html
<!-- Prettier sépare tout -->
<p>
  Texte avec
  <strong>emphase</strong>
  dedans.
</p>
```

---

### CSS : Prettier vs ESLint/Stylelint

Pour CSS, Prettier gère le formatage de base.

Pour des **règles de qualité** (ordre des propriétés, conventions de nommage), utilisez :
- **Stylelint** : linter CSS
- **ESLint** avec plugin CSS : alternative

**Division des rôles** :
- **Prettier** : formatage visuel (espaces, indentation)
- **Stylelint** : qualité du code (ordre, bonnes pratiques)

**Les deux sont complémentaires, pas concurrents.**

---

### JavaScript : Prettier vs ESLint

**ESLint** est un linter JavaScript qui détecte les erreurs.

**Prettier** formate le code visuellement.

**Peuvent-ils entrer en conflit ?** Oui, si ESLint a des règles de formatage.

**Solution** : Désactiver les règles de formatage d'ESLint.

**Configuration recommandée** :
```bash
npm install --save-dev eslint-config-prettier
```

Puis dans `.eslintrc.json` :
```json
{
  "extends": ["eslint:recommended", "prettier"]
}
```

**Résultat** :
- ESLint gère la **qualité** (erreurs logiques, bonnes pratiques)
- Prettier gère le **formatage** (espaces, indentation)

---

## Cas particuliers et dépannage

### Prettier ne formate pas

**Problèmes courants et solutions** :

#### 1. Prettier n'est pas le formateur par défaut

**Vérification** :
- Paramètres → "Default Formatter"
- Doit être "Prettier - Code formatter"

**Solution** :
```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

---

#### 2. Format On Save n'est pas activé

**Vérification** :
- Paramètres → "Format On Save"
- Doit être coché

**Solution** :
```json
{
  "editor.formatOnSave": true
}
```

---

#### 3. Le fichier n'est pas reconnu

Prettier ne formate que les **fichiers supportés**.

**Langages supportés** :
- HTML, CSS, SCSS, Less
- JavaScript, TypeScript, JSX, TSX
- JSON, JSONC
- Markdown
- YAML
- GraphQL
- Et bien d'autres

**Si votre fichier a une extension bizarre**, Prettier ne le formatera pas.

---

#### 4. Conflit avec un autre formateur

**Symptôme** : Le formatage ne correspond pas aux règles Prettier.

**Cause** : Un autre formateur est actif.

**Solution** :
1. Désactivez les autres formateurs (Beautify, ESLint auto-fix...)
2. Définissez Prettier comme formateur par défaut

---

#### 5. Erreurs de parsing

**Symptôme** : Message d'erreur "Cannot format document"

**Cause** : Votre code a des **erreurs de syntaxe**.

**Exemple** :
```html
<div>
  <p>Texte non fermé
</div>
```

**Solution** : Corrigez les erreurs de syntaxe d'abord, puis formatez.

---

### Formater un fichier manuellement

Si Format On Save ne fonctionne pas, essayez de formater manuellement :

1. **Ouvrez la palette** : `Ctrl/⌘ + Shift + P`
2. **Tapez** : "Format Document With..."
3. **Sélectionnez** : "Prettier - Code formatter"

**Si ça fonctionne**, le problème vient de la configuration "Format On Save".

**Si ça ne fonctionne pas**, le problème vient de Prettier lui-même.

---

### Désactiver Prettier temporairement

Parfois, vous voulez désactiver Prettier sur une partie du code.

**En HTML/CSS** :
```html
<!-- prettier-ignore -->
<div   class="keep-spaces"     >Content</div>
```

**En JavaScript** :
```javascript
// prettier-ignore
const matrix = [
  1, 0, 0,
  0, 1, 0,
  0, 0, 1
];
```

**En CSS** :
```css
/* prettier-ignore */
.selector { color:red;background:blue; }
```

**Pour un bloc entier** :
```javascript
// prettier-ignore-start
const a = "non formaté";
const b="aussi non formaté";
// prettier-ignore-end
```

**Utilisez avec parcimonie** : la cohérence est importante !

---

## Formatage dans différentes situations

### Formatage de code copié

Quand vous copiez du code d'internet ou d'un autre projet :

**Option 1 : Format On Paste**
```json
{
  "editor.formatOnPaste": true
}
```
Le code est formaté automatiquement quand vous le collez.

**Option 2 : Format après collage**
1. Collez le code
2. Sélectionnez-le
3. `Shift + Alt/Option + F` (formater)

---

### Formater tout le projet

Vous pouvez formater **tous les fichiers** d'un projet en une seule commande.

**Avec Prettier en ligne de commande** :
```bash
npx prettier --write "**/*.{js,html,css}"
```

**Explication** :
- `npx prettier` : lance Prettier
- `--write` : écrit les changements dans les fichiers
- `"**/*.{js,html,css}"` : tous les fichiers JS, HTML, CSS

**Attention** : Testez d'abord sans `--write` :
```bash
npx prettier --check "**/*.{js,html,css}"
```

Cela vérifie quels fichiers seraient modifiés sans les modifier.

---

### Formater avant un commit Git

**Bonne pratique** : formater automatiquement avant chaque commit.

**Avec Husky et lint-staged** (avancé) :
```bash
npm install --save-dev husky lint-staged
```

Configuration dans `package.json` :
```json
{
  "lint-staged": {
    "*.{js,html,css}": ["prettier --write"]
  }
}
```

**Résultat** : Tous les fichiers modifiés sont formatés automatiquement avant le commit.

**Note** : C'est un sujet avancé, nous y reviendrons dans la section Git.

---

## Bonnes pratiques

### 1. Activez Format On Save dès le début

**Le plus tôt possible** dans votre apprentissage, activez :
```json
{
  "editor.formatOnSave": true
}
```

**Avantage** : Vous prenez de bonnes habitudes immédiatement.

---

### 2. Utilisez la configuration par défaut

Ne modifiez pas tous les paramètres dès le début.

**Commencez avec** :
- `tabWidth: 2`
- `semi: true`
- `singleQuote: true` (optionnel)

**Ajustez ensuite** selon vos préférences ou celles de votre équipe.

---

### 3. Créez un .prettierrc dans vos projets

Pour chaque nouveau projet :
1. Créez `.prettierrc` à la racine
2. Définissez les règles pour le projet
3. Commitez le fichier dans Git

**Avantage** : Toute personne qui travaille sur le projet utilisera les mêmes règles.

---

### 4. Ne luttez pas contre Prettier

Prettier a des opinions fortes sur le formatage.

**Mauvaise approche** : "Je veux que mes objets soient formatés différemment !"

**Bonne approche** : "Prettier gère le formatage, je me concentre sur la logique."

**L'uniformité** est plus importante que vos préférences personnelles.

---

### 5. Formatez avant de partager

Avant de :
- Commiter du code
- Envoyer du code à un collègue
- Publier un projet

**Assurez-vous** que tout est bien formaté !

---

### 6. Combinez avec ESLint/Stylelint

**Prettier** : formatage visuel
**ESLint/Stylelint** : qualité et bonnes pratiques

**Les deux ensemble** = code parfait ! 🎯

---

## Comparaison : Formatage manuel vs automatique

### Scénario : Formater 10 fichiers HTML

**Manuellement** :
1. Ouvrir le premier fichier
2. Vérifier l'indentation ligne par ligne
3. Corriger les espaces
4. Aligner les balises
5. Répéter pour les 10 fichiers
⏱️ **Temps** : 30-60 minutes

**Avec Prettier** :
1. Sélectionner les 10 fichiers
2. Formater (`Shift + Alt/Option + F`)
⏱️ **Temps** : 5 secondes

**Gain** : Des dizaines de minutes, aucune erreur, cohérence parfaite !

---

## Extensions complémentaires

### 1. Prettier ESLint

**Nom** : Prettier ESLint

**À quoi ça sert** :
Combine Prettier (formatage) et ESLint (qualité) en une seule extension.

**Installation** :
Extensions → "Prettier ESLint"

**Avantage** : Un seul outil pour tout.

---

### 2. Format All Files

**Nom** : Format All Files

**À quoi ça sert** :
Formater tous les fichiers d'un projet en un clic.

**Utilisation** :
1. `Ctrl/⌘ + Shift + P`
2. "Start Format All Files"

---

## Résumé visuel : Avant/Après

### Exemple complet : Page HTML

**Avant** :
```html
<!DOCTYPE html><html><head><meta charset="UTF-8"><title>Page</title><style>.container{width:100%;padding:20px;}.box{color:red;}</style></head><body><div class="container"><h1>Titre principal</h1><p>Un paragraphe avec du <strong>texte important</strong> dedans.</p><ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul></div><script>function hello(){console.log("Hello");}</script></body></html>
```

**Après Prettier** :
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Page</title>
    <style>
      .container {
        width: 100%;
        padding: 20px;
      }
      .box {
        color: red;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <h1>Titre principal</h1>
      <p>
        Un paragraphe avec du <strong>texte important</strong> dedans.
      </p>
      <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
      </ul>
    </div>
    <script>
      function hello() {
        console.log("Hello");
      }
    </script>
  </body>
</html>
```

**Différence** : Comme le jour et la nuit ! 🌟

---

## Récapitulatif

### Ce que vous savez maintenant

Félicitations ! Vous maîtrisez maintenant :

- ✅ L'importance du **formatage du code**
- ✅ **Prettier** : l'outil de formatage moderne
- ✅ Comment **installer et configurer** Prettier
- ✅ Comment **formater automatiquement** à la sauvegarde
- ✅ Les **paramètres principaux** de Prettier
- ✅ Comment créer un fichier **.prettierrc**
- ✅ Comment **ignorer des fichiers** avec .prettierignore
- ✅ Le formatage dans **HTML, CSS, JavaScript**
- ✅ Comment **dépanner** les problèmes courants
- ✅ Les **bonnes pratiques** de formatage

### Configuration minimale recommandée

Pour commencer immédiatement :

**Dans VS Code (settings.json)** :
```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "prettier.tabWidth": 2,
  "prettier.semi": true,
  "prettier.singleQuote": true
}
```

**C'est tout !** Vous êtes prêt.

### Les 3 règles d'or

1. ⚙️ **Activez Format On Save** dès maintenant
2. 📄 **Créez un .prettierrc** dans chaque projet
3. 🎯 **Laissez Prettier faire son travail**, ne luttez pas contre lui

---

## Pour aller plus loin

### Documentation officielle

**Prettier** :
- Site officiel : https://prettier.io
- Documentation : https://prettier.io/docs/en/
- Playground : https://prettier.io/playground/ (testez en ligne !)

**VS Code** :
- Formatage : https://code.visualstudio.com/docs/editor/codebasics#_formatting

### Ressources complémentaires

**Articles** :
- "Why Prettier?" sur le site officiel
- Comparaisons Prettier vs autres formateurs

**Vidéos** :
- Cherchez "Prettier tutorial" sur YouTube
- Vidéos officielles VS Code sur le formatage

### Prochaines étapes

Maintenant que votre code est toujours bien formaté, passons à la section suivante où nous découvrirons les **Snippets et l'auto-complétion**, des outils qui vous feront écrire du code encore plus rapidement !

---

## Navigation


**➡️ Section suivante :** [2.2.4 Snippets et auto-complétion](./04-snippets-et-auto-completion.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Un code bien formaté est un code qui respire la qualité professionnelle. Avec Prettier, c'est automatique !* ✨🎨

⏭️ [Snippets et auto-complétion](/02-environnement-de-developpement/02-maitrise-de-lediteur/04-snippets-et-auto-completion.md)
