🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.3.2 Conventions de nommage

## Introduction

Les conventions de nommage sont comme **les règles de grammaire** en développement web : elles vous aident à écrire du code clair, compréhensible et professionnel. Un bon nom de fichier ou de variable doit être :

- **Descriptif** : On comprend immédiatement à quoi il sert
- **Cohérent** : Suit toujours les mêmes règles
- **Lisible** : Facile à lire et à prononcer
- **Compatible** : Fonctionne sur tous les systèmes (Windows, Mac, Linux)

> 💡 **Analogie** : Imaginez une bibliothèque où les livres seraient classés n'importe comment : "Livre1", "truC", "DOCUMENT final", "test123". Ce serait le chaos ! Les conventions de nommage sont comme le système de classification d'une bibliothèque.

Dans ce chapitre, nous allons voir comment nommer correctement :
- Les fichiers et dossiers
- Les classes et IDs en HTML/CSS
- Les variables et fonctions en JavaScript

---

## Pourquoi c'est important ?

### Les problèmes d'un mauvais nommage

Regardez cet exemple de projet mal nommé :

```
Mon Site/
├── Page 1.html
├── STYLES.css
├── Script final FINAL v2.js
├── Image.jpg
├── image(1).jpg
└── nouveau dossier/
```

**Problèmes :**
- ❌ Les espaces causent des problèmes dans les URLs : `Mon%20Site/Page%201.html`
- ❌ Majuscules incohérentes : impossible de se rappeler si c'est `STYLES.css` ou `styles.css`
- ❌ Noms non descriptifs : "Image.jpg", c'est quoi comme image ?
- ❌ Versions multiples : "final", "FINAL v2"... quelle est la vraie version ?

### Les avantages d'un bon nommage

```
mon-site/
├── index.html
├── contact.html
├── css/
│   └── style.css
├── js/
│   └── navigation.js
└── images/
    ├── logo-entreprise.png
    └── hero-accueil.jpg
```

**Avantages :**
- ✅ Facile à lire et à comprendre
- ✅ Pas de problèmes avec les URLs ou systèmes d'exploitation
- ✅ Cohérence parfaite
- ✅ Professionnel

---

## Règles universelles (valables pour tout)

Ces règles s'appliquent à **tous** vos fichiers, dossiers et noms de code :

### 1. Toujours en minuscules

```
✅ BIEN
index.html
style.css
script.js
logo-entreprise.png

❌ À ÉVITER
Index.html
STYLE.CSS
Script.js
Logo-Entreprise.png
```

**Pourquoi ?**
- Les serveurs Linux (qui hébergent la majorité des sites web) sont **sensibles à la casse** : `Style.css` ≠ `style.css`
- Évite les erreurs bêtes : "Mon fichier ne se charge pas !" → souvent un problème de majuscule/minuscule

**Exception :** Certains fichiers spéciaux comme `README.md`, `LICENSE`, ou `.gitignore` utilisent des majuscules par convention.

---

### 2. Pas d'espaces

```
✅ BIEN
mon-super-projet.html
photo-de-profil.jpg
page-a-propos.html

❌ À ÉVITER
mon super projet.html
photo de profil.jpg
page à propos.html
```

**Pourquoi ?**
- Les espaces deviennent `%20` dans les URLs : `photo%20de%20profil.jpg`
- Cauent des problèmes dans les lignes de commande
- Moins lisibles dans le code

**Comment remplacer les espaces ?**
- Utilisez le **tiret** `-` (recommandé) : `mon-fichier.html`
- Ou le **underscore** `_` : `mon_fichier.html`

> 📌 **Recommandation** : Privilégiez le tiret `-`, c'est la convention la plus répandue en développement web.

---

### 3. Pas d'accents ni de caractères spéciaux

```
✅ BIEN
chateau-de-versailles.jpg
a-propos.html
evenements.html

❌ À ÉVITER
château-de-versailles.jpg
à-propos.html
événements.html
```

**Pourquoi ?**
- Problèmes d'encodage sur certains serveurs
- Peuvent ne pas s'afficher correctement
- Complications potentielles avec les URLs

**Caractères interdits :** `é`, `è`, `ê`, `à`, `ç`, `ù`, etc.

**Caractères à éviter aussi :** `#`, `@`, `%`, `&`, `*`, `(`, `)`, `+`, `=`, etc.

---

### 4. Noms descriptifs et explicites

```
✅ BIEN
logo-entreprise.png
bouton-inscription.css
validation-formulaire.js
banniere-accueil.jpg

❌ À ÉVITER
image1.png
style2.css
script.js
photo.jpg
```

**Principe** : Quelqu'un qui ne connaît pas votre projet doit comprendre ce que contient le fichier juste en lisant son nom.

**Questions à se poser :**
- Dans 6 mois, est-ce que je comprendrai ce qu'est ce fichier ?
- Un collègue peut-il deviner son contenu ?
- Le nom décrit-il précisément son usage ?

---

### 5. Pas de versions dans le nom

```
✅ BIEN
style.css
(Utilisez Git pour gérer les versions)

❌ À ÉVITER
style-v1.css
style-v2.css
style-final.css
style-final-final.css
style-final-pour-de-vrai.css
```

**Pourquoi ?**
- Créé du désordre
- On ne sait jamais quelle est la "vraie" version
- C'est le rôle de Git (que nous verrons au chapitre 2.3.3)

---

## Conventions pour les fichiers et dossiers

### Fichiers HTML

```
✅ Bonnes pratiques
index.html          ← Page d'accueil (obligatoire)
about.html          ← En anglais, court
a-propos.html       ← Ou en français avec tirets
contact.html
mentions-legales.html
page-404.html

❌ À éviter
page1.html
accueil.html        ← On préfère index.html pour la page d'accueil
MesPages.html
à propos.html
```

**Convention :**
- La page d'accueil s'appelle **toujours** `index.html`
- Utilisez soit l'anglais, soit le français, mais soyez **cohérent**
- Séparez les mots avec des tirets `-`

---

### Fichiers CSS

```
✅ Bonnes pratiques
style.css           ← Fichier principal
reset.css           ← Reset des styles
normalize.css
responsive.css
header.css
footer.css
forms.css

❌ À éviter
styles1.css
MesStyles.css
style final.css
```

**Convention :**
- `style.css` pour votre feuille principale
- Noms descriptifs pour les fichiers spécifiques : `header.css`, `forms.css`
- Tout en minuscules, tirets pour séparer

---

### Fichiers JavaScript

```
✅ Bonnes pratiques
script.js           ← Script principal
main.js             ← Alternative au nom principal
navigation.js       ← Descriptif
form-validation.js
slider.js
utils.js            ← Fonctions utilitaires

❌ À éviter
Script.js
script1.js
js.js
test.js
```

**Convention :**
- `script.js` ou `main.js` pour le fichier principal
- Noms descriptifs de la fonctionnalité : `slider.js`, `form-validation.js`
- Séparez les mots avec des tirets

---

### Images

```
✅ Bonnes pratiques
logo-entreprise.png
hero-accueil.jpg
icon-menu.svg
photo-profil-jean-dupont.jpg
product-123.png
background-header.jpg

❌ À éviter
IMG001.jpg
image.png
photo (1).jpg
ma super image.jpg
```

**Convention :**
- **Préfixe du type** (optionnel mais utile) : `logo-`, `icon-`, `bg-`, `photo-`
- **Description claire** : où/comment elle est utilisée
- **Extension appropriée** : `.jpg` pour photos, `.png` pour logos/icônes, `.svg` pour graphiques

**Format du nom :**
```
[type]-[description]-[détails].extension

Exemples :
icon-search.svg
logo-client-total.png
bg-hero-homepage.jpg
photo-product-shoes-red.jpg
```

---

### Dossiers

```
✅ Bonnes pratiques
css/
js/
images/
assets/
fonts/
components/
pages/

❌ À éviter
CSS/
Mes Images/
nouveau dossier/
dossier 1/
```

**Convention :**
- Tout en minuscules
- Noms courts mais descriptifs
- Pluriel recommandé pour les dossiers de contenu : `images/`, `fonts/`, `components/`

---

## Conventions en HTML et CSS

### Classes CSS

Les classes CSS suivent généralement la convention **kebab-case** (tout en minuscules avec tirets) :

```html
✅ BIEN (kebab-case)
<div class="header-navigation">
<button class="btn-primary">
<section class="hero-section">
<p class="text-center">

❌ À ÉVITER
<div class="Header_Navigation">
<button class="BTNPRIMARY">
<section class="heroSection">
<p class="Text Center">
```

**Règles pour les classes :**
- Tout en minuscules
- Tirets pour séparer les mots
- Descriptif et sémantique : `btn-primary`, `card-title`, `nav-link`

**Exemples de bonnes classes :**
```css
.container { }
.header-main { }
.nav-menu { }
.btn-primary { }
.btn-secondary { }
.card-product { }
.text-center { }
.text-bold { }
.bg-dark { }
.mb-3 { }  /* margin-bottom: 3 */
```

---

### IDs en HTML

Les IDs suivent aussi la convention **kebab-case** :

```html
✅ BIEN
<header id="main-header">
<nav id="primary-navigation">
<section id="hero-section">
<form id="contact-form">

❌ À ÉVITER
<header id="MainHeader">
<nav id="primary_navigation">
<section id="HeroSection">
<form id="Contact Form">
```

**Important :** Les IDs doivent être **uniques** sur une page. Utilisez les classes pour les styles réutilisables.

---

### Méthodologie BEM (Aperçu)

**BEM** (Block Element Modifier) est une convention de nommage populaire pour les classes CSS :

```html
<!-- Block -->
<div class="card">
    <!-- Element -->
    <h2 class="card__title">Titre</h2>
    <p class="card__description">Description</p>
    <!-- Modifier -->
    <button class="card__button card__button--primary">Cliquer</button>
</div>
```

**Structure :**
- `.block` : Le composant principal
- `.block__element` : Un élément à l'intérieur du bloc (2 underscores)
- `.block--modifier` : Une variation du bloc (2 tirets)

> 📌 **Note** : BEM est une méthodologie avancée. Pour débuter, restez simple avec kebab-case !

---

## Conventions en JavaScript

### Variables

En JavaScript, on utilise le **camelCase** (première lettre minuscule, majuscules pour les mots suivants) :

```javascript
✅ BIEN (camelCase)
let userName = "Jean";
let userAge = 25;
let isLoggedIn = true;
let totalPrice = 99.99;
const maxLoginAttempts = 3;

❌ À ÉVITER
let user_name = "Jean";      // snake_case (utilisé en Python)
let UserName = "Jean";        // PascalCase (réservé aux classes)
let USERNAME = "Jean";        // SCREAMING_SNAKE_CASE (réservé aux constantes)
let nom utilisateur = "Jean"; // Espaces interdits !
```

**Règles :**
- Première lettre en **minuscule**
- Pas d'espaces ni de tirets
- Majuscule pour chaque nouveau mot
- Nom descriptif

**Exemples de bons noms :**
```javascript
let firstName = "Marie";
let lastName = "Dupont";
let emailAddress = "marie@example.com";
let isActive = true;
let productCount = 5;
let backgroundColor = "#ff0000";
```

---

### Constantes

Les constantes importantes utilisent le **SCREAMING_SNAKE_CASE** :

```javascript
✅ BIEN
const API_URL = "https://api.example.com";
const MAX_USERS = 100;
const TAX_RATE = 0.20;
const DEFAULT_COLOR = "#000000";

// Mais pour des constantes "normales", camelCase est OK
const userSettings = { theme: "dark" };
const appConfig = { version: "1.0" };
```

**Quand utiliser SCREAMING_SNAKE_CASE ?**
- Valeurs de configuration importantes
- Constantes mathématiques ou physiques
- URLs d'API
- Clés d'API (bien que celles-ci ne devraient pas être dans le code !)

---

### Fonctions

Les fonctions utilisent aussi le **camelCase**, généralement avec un verbe d'action :

```javascript
✅ BIEN (camelCase avec verbe)
function getUserName() { }
function calculateTotal() { }
function isValidEmail() { }
function displayMessage() { }
function saveUserData() { }

❌ À ÉVITER
function GetUserName() { }     // PascalCase
function user_name() { }        // snake_case
function nom() { }              // Pas descriptif
function calcul() { }           // Pas de verbe
```

**Verbes courants pour nommer les fonctions :**
- `get...` : récupérer une valeur → `getUserAge()`
- `set...` : définir une valeur → `setUserName()`
- `calculate...` : calculer → `calculateTotalPrice()`
- `display...` : afficher → `displayErrorMessage()`
- `save...` : sauvegarder → `saveFormData()`
- `delete...` : supprimer → `deleteUser()`
- `is...` / `has...` : vérifier (retourne true/false) → `isValidEmail()`, `hasAccess()`

---

### Classes ES6

Les classes utilisent le **PascalCase** (première lettre en majuscule) :

```javascript
✅ BIEN (PascalCase)
class User { }
class ProductCard { }
class ShoppingCart { }
class PaymentProcessor { }

❌ À ÉVITER
class user { }          // minuscule
class product_card { }  // snake_case
class shopping-cart { } // kebab-case impossible en JS
```

**Pourquoi PascalCase pour les classes ?**
- Distingue visuellement les classes des fonctions
- Convention universelle en programmation orientée objet
- Utilisé dans tous les frameworks (React, Vue, Angular)

---

## Tableau récapitulatif

| Type | Convention | Exemple |
|------|-----------|---------|
| **Fichiers HTML** | kebab-case | `index.html`, `a-propos.html` |
| **Fichiers CSS** | kebab-case | `style.css`, `responsive.css` |
| **Fichiers JS** | kebab-case | `script.js`, `form-validation.js` |
| **Images** | kebab-case | `logo-entreprise.png` |
| **Dossiers** | kebab-case | `css/`, `images/`, `assets/` |
| **Classes CSS** | kebab-case | `.btn-primary`, `.header-nav` |
| **IDs HTML** | kebab-case | `#main-header`, `#contact-form` |
| **Variables JS** | camelCase | `userName`, `isLoggedIn` |
| **Fonctions JS** | camelCase | `getUserName()`, `calculateTotal()` |
| **Constantes JS** | SCREAMING_SNAKE_CASE ou camelCase | `API_URL` ou `appConfig` |
| **Classes JS** | PascalCase | `User`, `ProductCard` |

---

## Exemples concrets

### Projet de site e-commerce

Structure de fichiers avec un bon nommage :

```
boutique-en-ligne/
├── index.html
├── products.html
├── cart.html
├── checkout.html
├── css/
│   ├── style.css
│   ├── products.css
│   └── cart.css
├── js/
│   ├── main.js
│   ├── cart-manager.js
│   └── product-filter.js
└── images/
    ├── logo-boutique.png
    ├── product-001.jpg
    ├── product-002.jpg
    └── icon-cart.svg
```

Exemple de code avec un bon nommage :

```html
<!-- HTML avec bonnes classes -->
<header class="main-header">
    <nav class="primary-nav">
        <ul class="nav-list">
            <li class="nav-item"><a href="#" class="nav-link">Accueil</a></li>
        </ul>
    </nav>
</header>

<section class="product-grid">
    <div class="product-card">
        <img src="images/product-001.jpg" alt="Produit 1" class="product-image">
        <h2 class="product-title">Super Produit</h2>
        <p class="product-price">29.99€</p>
        <button class="btn btn-primary">Ajouter au panier</button>
    </div>
</section>
```

```css
/* CSS avec bonnes classes */
.main-header {
    background-color: #333;
}

.primary-nav {
    display: flex;
}

.nav-list {
    list-style: none;
}

.product-card {
    border: 1px solid #ddd;
    padding: 1rem;
}

.btn-primary {
    background-color: #007bff;
    color: white;
}
```

```javascript
// JavaScript avec bon nommage
const maxProductsPerPage = 12;
const API_URL = "https://api.boutique.com";

let cartItems = [];
let totalPrice = 0;

function addToCart(productId) {
    // Code...
}

function calculateCartTotal() {
    // Code...
}

function displayProducts(products) {
    // Code...
}

class Product {
    constructor(id, name, price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }
}
```

---

## Cas spéciaux et exceptions

### 1. Fichiers de configuration

Certains fichiers ont des noms conventionnels spécifiques :

```
✅ Noms standards
README.md           ← Documentation du projet
LICENSE             ← Licence du projet
.gitignore          ← Fichiers ignorés par Git
package.json        ← Configuration npm
.env                ← Variables d'environnement
```

**Ne les renommez pas !** Ces noms sont des conventions universelles.

---

### 2. Frameworks et librairies

Certains frameworks imposent leurs propres conventions :

**React :**
```javascript
// Composants React en PascalCase
function UserProfile() { }
function ProductCard() { }
```

**Vue.js :**
```javascript
// Composants Vue en PascalCase
export default {
    name: 'UserProfile'
}
```

Vous apprendrez ces conventions spécifiques quand vous étudierez ces frameworks.

---

## Checklist avant de nommer

Avant de nommer un fichier, dossier ou variable, posez-vous ces questions :

- [ ] Est-ce en minuscules ? (sauf classes JS)
- [ ] Y a-t-il des espaces ? (à remplacer par des tirets)
- [ ] Y a-t-il des accents ou caractères spéciaux ? (à supprimer)
- [ ] Le nom est-il descriptif et clair ?
- [ ] Est-ce cohérent avec le reste de mon projet ?
- [ ] Quelqu'un d'autre peut-il comprendre ce nom ?
- [ ] Ai-je utilisé la bonne convention (kebab-case, camelCase, PascalCase) ?

---

## Conseils pratiques

### 1. Choisissez une langue et tenez-vous y

```
✅ BIEN - Tout en anglais
button-primary
user-profile
shopping-cart

✅ BIEN - Tout en français
bouton-principal
profil-utilisateur
panier-achat

❌ INCOHÉRENT - Mélange
button-principal
profil-user
shopping-panier
```

**Recommandation :** L'anglais est la langue universelle du code. Cependant, pour débuter, le français est acceptable. L'important est d'être **cohérent**.

---

### 2. Soyez cohérent dans tout le projet

Si vous commencez avec une convention, gardez-la partout :

```
✅ Cohérent
header-navigation.html
footer-navigation.html
sidebar-navigation.html

❌ Incohérent
header-navigation.html
FooterNav.html
sidebar_navigation.html
```

---

### 3. Plus descriptif vaut mieux que plus court

```
✅ Descriptif
let userRegistrationDate = "2024-12-02";
function validateEmailAddress(email) { }

❌ Trop court
let d = "2024-12-02";
function val(e) { }
```

**Exception :** Dans les boucles, les variables courtes sont acceptées :
```javascript
// OK dans une boucle
for (let i = 0; i < 10; i++) { }

// OK pour des variables temporaires
let x, y;
```

---

## Résumé

### Règles d'or du nommage

1. **Minuscules** pour les fichiers et dossiers
2. **Pas d'espaces** → utilisez des tirets `-`
3. **Pas d'accents** ni caractères spéciaux
4. **Descriptif** et explicite
5. **Cohérent** dans tout le projet

### Conventions par contexte

- **Fichiers/dossiers** : kebab-case (`mon-fichier.html`)
- **Classes CSS** : kebab-case (`.mon-style`)
- **Variables JS** : camelCase (`monVariable`)
- **Fonctions JS** : camelCase avec verbe (`getUserName()`)
- **Classes JS** : PascalCase (`MaClasse`)
- **Constantes JS** : SCREAMING_SNAKE_CASE (`MAX_VALUE`)

---

## Pour aller plus loin

Les conventions de nommage sont votre **signature professionnelle**. Un code bien nommé est :
- Plus facile à lire
- Plus facile à maintenir
- Plus facile à partager

Dans le prochain chapitre **2.3.3 Introduction à Git**, vous verrez comment versionner votre code et collaborer avec d'autres développeurs. Des conventions de nommage claires seront essentielles pour travailler en équipe !

> 💡 **Astuce finale** : Au début, prenez le temps de bien réfléchir à vos noms. Avec l'expérience, cela deviendra naturel et automatique ! 🚀

⏭️ [Introduction à Git et gestion de versions](/02-environnement-de-developpement/03-organisation-de-projets/03-introduction-a-git.md)
