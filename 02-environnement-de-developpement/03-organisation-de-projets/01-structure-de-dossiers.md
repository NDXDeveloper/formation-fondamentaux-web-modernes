🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.3.1 Structure de dossiers recommandée

## Introduction

Lorsque vous commencez un projet web, l'une des premières choses à faire est de créer une structure de dossiers claire et logique. Une bonne organisation vous permettra de :

- **Retrouver facilement vos fichiers** : Plus besoin de chercher pendant 5 minutes où se trouve votre feuille de style !
- **Travailler efficacement** : Une structure claire = moins de temps perdu
- **Collaborer avec d'autres développeurs** : Une organisation standardisée facilite le travail en équipe
- **Maintenir votre projet** : Revenir sur un projet bien organisé, même après plusieurs mois, sera beaucoup plus facile

> 💡 **Analogie** : Imaginez votre cuisine. Si tous vos ustensiles, ingrédients et vaisselle sont mélangés dans un seul placard, cuisiner devient un cauchemar. Une bonne organisation (tiroirs à couverts, placard à épices, etc.) rend tout plus simple !

---

## Pourquoi organiser ses fichiers ?

### Le problème du "tout dans un seul dossier"

Beaucoup de débutants créent leurs premiers projets comme ceci :

```
mon-projet/
├── index.html
├── page2.html
├── style.css
├── script.js
├── photo1.jpg
├── photo2.jpg
├── logo.png
├── style2.css
├── ancien-script.js
└── test.html
```

**Problèmes avec cette approche :**
- Difficile de distinguer les types de fichiers au premier coup d'œil
- Les images se mélangent avec le code
- On ne sait pas quels fichiers sont vraiment utilisés
- Ça devient vite le chaos dès qu'on a plus de 10 fichiers

### La solution : une structure organisée

Une structure bien pensée sépare les fichiers par **type** et par **fonction**. C'est comme ranger ses vêtements : les chaussettes dans un tiroir, les t-shirts dans un autre !

---

## Structure de base recommandée

Voici une structure simple et professionnelle, parfaite pour débuter :

```
mon-projet/
├── index.html
├── css/
│   ├── style.css
│   └── reset.css
├── js/
│   └── script.js
├── images/
│   ├── logo.png
│   ├── photo1.jpg
│   └── photo2.jpg
└── assets/
    ├── fonts/
    └── icons/
```

### Explication détaillée

#### **Fichier `index.html` à la racine**

```
mon-projet/
├── index.html      ← Page d'accueil de votre site
```

- Le fichier `index.html` doit toujours être **à la racine** (au premier niveau) de votre projet
- C'est la convention universelle : quand un serveur web reçoit une requête pour un dossier, il cherche automatiquement un fichier nommé `index.html`
- C'est la porte d'entrée de votre site web

> 📌 **Important** : Si vous avez d'autres pages HTML (comme `contact.html`, `about.html`), vous pouvez aussi les placer à la racine pour les petits projets.

---

#### **Dossier `css/` pour les styles**

```
css/
├── style.css       ← Votre feuille de style principale
└── reset.css       ← (Optionnel) Fichier de normalisation CSS
```

**Pourquoi un dossier séparé ?**
- Tous vos fichiers CSS sont au même endroit
- Facile à retrouver et à modifier
- Séparation claire entre structure (HTML) et apparence (CSS)

**Conventions de nommage :**
- `style.css` : votre feuille de style principale
- `reset.css` ou `normalize.css` : pour réinitialiser les styles par défaut du navigateur
- Pour des projets plus grands, vous pourriez avoir : `header.css`, `footer.css`, `forms.css`, etc.

**Comment lier ces fichiers dans votre HTML :**

```html
<!-- Dans votre index.html -->
<head>
    <link rel="stylesheet" href="css/style.css">
</head>
```

---

#### **Dossier `js/` pour JavaScript**

```
js/
└── script.js       ← Votre fichier JavaScript principal
```

**À quoi sert ce dossier ?**
- Contient tous vos scripts JavaScript
- Sépare la logique et les interactions de la structure HTML

**Exemples de fichiers possibles :**
- `script.js` : script principal
- `utils.js` : fonctions utilitaires réutilisables
- `api.js` : code pour communiquer avec des APIs

**Comment lier ces fichiers dans votre HTML :**

```html
<!-- Juste avant la fermeture de </body> -->
<body>
    <!-- Votre contenu -->

    <script src="js/script.js"></script>
</body>
```

---

#### **Dossier `images/` pour les médias**

```
images/
├── logo.png
├── hero-banner.jpg
├── product-1.jpg
└── icon-menu.svg
```

**Ce qu'on y met :**
- Toutes les images de votre site : photos, illustrations, logos, icônes
- Formats courants : `.jpg`, `.png`, `.svg`, `.gif`, `.webp`

**Bonnes pratiques :**
- Utilisez des noms descriptifs : `logo-entreprise.png` plutôt que `img1.png`
- Pour les grands projets, vous pouvez créer des sous-dossiers :
  ```
  images/
  ├── logos/
  ├── products/
  └── backgrounds/
  ```

**Comment utiliser ces images dans votre HTML :**

```html
<img src="images/logo.png" alt="Logo de l'entreprise">
```

---

#### **Dossier `assets/` pour les autres ressources**

```
assets/
├── fonts/          ← Polices de caractères personnalisées
│   ├── roboto.woff2
│   └── roboto.woff
└── icons/          ← Icônes au format SVG ou fonte d'icônes
    └── sprite.svg
```

**Ce qu'on y met :**
- **`fonts/`** : Polices de caractères téléchargées (Google Fonts local, polices personnalisées)
- **`icons/`** : Icônes SVG, sprites d'icônes
- Autres ressources comme des fichiers de configuration, données JSON, etc.

> 💡 **Note** : Certains développeurs préfèrent mettre les images dans `assets/images/`. Les deux approches sont valides ! L'important est d'être **cohérent** dans votre choix.

---

## Structure pour un projet plus complexe

Quand votre projet grandit, vous pouvez adapter cette structure :

```
mon-projet/
├── index.html
├── about.html
├── contact.html
├── css/
│   ├── style.css
│   ├── reset.css
│   ├── responsive.css
│   └── components/
│       ├── header.css
│       ├── footer.css
│       └── buttons.css
├── js/
│   ├── main.js
│   ├── utils.js
│   └── modules/
│       ├── slider.js
│       └── form-validation.js
├── images/
│   ├── logos/
│   ├── products/
│   └── backgrounds/
├── assets/
│   ├── fonts/
│   ├── icons/
│   └── documents/
│       └── brochure.pdf
└── pages/
    ├── blog/
    │   ├── article-1.html
    │   └── article-2.html
    └── portfolio/
        └── projet-1.html
```

**Nouveautés :**
- **Sous-dossiers dans `css/`** : Pour organiser vos styles par composants
- **Sous-dossiers dans `js/`** : Pour séparer vos modules JavaScript
- **Dossier `pages/`** : Pour les pages secondaires organisées par section
- **Sous-dossiers dans `images/`** : Pour catégoriser vos images

---

## Ce qu'il faut éviter

### ❌ Mauvaises pratiques

1. **Espaces dans les noms de fichiers ou dossiers**
   ```
   ❌ mes images/photo de vacances.jpg
   ✅ mes-images/photo-vacances.jpg
   ```
   Les espaces peuvent causer des problèmes sur les serveurs web.

2. **Accents et caractères spéciaux**
   ```
   ❌ images/château.jpg
   ✅ images/chateau.jpg
   ```

3. **Majuscules inconsistantes**
   ```
   ❌ Images/Logo.PNG
   ✅ images/logo.png
   ```
   Soyez cohérent : tout en minuscules est la convention standard.

4. **Fichiers de test non supprimés**
   ```
   ❌ test.html, old_script.js, backup.css
   ```
   Supprimez ou archivez les fichiers de test et sauvegardes.

5. **Dossiers trop profondément imbriqués**
   ```
   ❌ assets/images/photos/personnes/famille/portrait.jpg
   ✅ images/portraits/famille-portrait.jpg
   ```

---

## Créer votre structure dans VS Code

### Méthode 1 : Créer les dossiers manuellement

1. **Ouvrez votre projet dans VS Code**
2. **Clic droit dans l'explorateur de fichiers** (barre latérale gauche)
3. Sélectionnez **"New Folder"** (Nouveau dossier)
4. Tapez le nom du dossier (ex: `css`)
5. Répétez pour chaque dossier

### Méthode 2 : Créer plusieurs dossiers d'un coup

Vous pouvez créer un fichier avec un chemin complet, VS Code créera automatiquement les dossiers manquants :

1. Clic droit > **"New File"**
2. Tapez : `css/style.css`
3. VS Code créera le dossier `css` ET le fichier `style.css`

### Méthode 3 : Via le terminal intégré

Si vous êtes à l'aise avec le terminal :

```bash
# Créer tous les dossiers d'un coup
mkdir css js images assets assets/fonts assets/icons
```

---

## Résumé des bonnes pratiques

✅ **À faire :**
- Placer `index.html` à la racine
- Créer des dossiers séparés pour CSS, JS, et images
- Utiliser des noms descriptifs et clairs
- Tout en minuscules, avec des tirets `-` pour séparer les mots
- Être cohérent dans votre organisation

❌ **À éviter :**
- Tout mélanger dans un seul dossier
- Utiliser des espaces ou des accents dans les noms
- Créer des structures trop complexes dès le début
- Garder des fichiers de test dans votre projet final

---

## Exemple pratique : Structure d'un petit site portfolio

Voici à quoi pourrait ressembler la structure d'un site portfolio simple :

```
portfolio-jean-dupont/
├── index.html              ← Page d'accueil
├── projets.html            ← Page portfolio
├── contact.html            ← Page contact
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   ├── photo-profil.jpg
│   ├── projet-1.jpg
│   ├── projet-2.jpg
│   └── projet-3.jpg
└── assets/
    └── documents/
        └── cv-jean-dupont.pdf
```

Simple, clair, et efficace ! 🎯

---

## Évolution de votre structure

Rappelez-vous : **commencez simple** ! La structure présentée au début de ce chapitre est parfaite pour débuter. Au fur et à mesure que vos projets grandissent, vous pourrez :

1. Ajouter de nouveaux dossiers selon vos besoins
2. Créer des sous-dossiers pour mieux organiser
3. Adapter la structure à votre workflow

L'important est de rester **cohérent** et **logique** dans votre organisation. Un autre développeur (ou vous dans 6 mois !) doit pouvoir comprendre rapidement comment votre projet est structuré.

---

## Pour aller plus loin

Dans les prochains chapitres, nous verrons :
- **2.3.2 Conventions de nommage** : Comment nommer vos fichiers de manière professionnelle
- **2.3.3 Introduction à Git** : Comment versionner votre code et collaborer

Une bonne structure de dossiers est la **fondation** d'un projet réussi. Prenez le temps de bien l'organiser dès le début, vous vous remercierez plus tard ! 🚀

⏭️ [Conventions de nommage](/02-environnement-de-developpement/03-organisation-de-projets/02-conventions-de-nommage.md)
