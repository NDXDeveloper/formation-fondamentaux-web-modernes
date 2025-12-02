🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.2.1 Navigation rapide et raccourcis clavier

## Introduction

Les **raccourcis clavier** sont l'une des clés de la productivité dans VS Code. Au début, il peut sembler plus simple de tout faire à la souris en cliquant dans les menus, mais apprendre les raccourcis vous fera gagner un temps considérable et rendra votre travail beaucoup plus fluide.

### Pourquoi apprendre les raccourcis clavier ?

**Sans raccourcis** :
1. Vous déplacez votre main vers la souris
2. Vous cherchez le menu dans l'interface
3. Vous cliquez plusieurs fois
4. Vous repositionnez vos mains sur le clavier
5. Vous reprenez votre travail

**Avec raccourcis** :
1. Vous appuyez sur une combinaison de touches
2. L'action s'exécute instantanément
3. Vos mains restent sur le clavier

**Gain de temps** : quelques secondes à chaque fois, mais **des heures sur une journée** et **des semaines sur une année** !

### L'approche progressive

⚠️ **Ne tentez pas d'apprendre tous les raccourcis d'un coup !**

**Notre méthode** :
- 📌 **Semaine 1** : Maîtrisez les 5 raccourcis essentiels
- 📌 **Semaine 2** : Ajoutez 5 raccourcis de navigation
- 📌 **Semaine 3** : Ajoutez 5 raccourcis d'édition
- 📌 **Ensuite** : Ajoutez progressivement selon vos besoins

**Astuce** : Imprimez la fiche de raccourcis et gardez-la à côté de votre écran les premières semaines.

### Convention de notation

Dans ce document, nous utiliserons la notation suivante :

**Windows/Linux** :
- `Ctrl + S` : maintenir Ctrl enfoncé, puis appuyer sur S
- `Ctrl + Shift + P` : maintenir Ctrl et Shift, puis appuyer sur P
- `Ctrl + K, Ctrl + S` : appuyer sur Ctrl+K, relâcher, puis appuyer sur Ctrl+S

**macOS** :
- `⌘ + S` : maintenir Cmd (⌘) enfoncé, puis appuyer sur S
- `⌘ + Shift + P` : maintenir Cmd et Shift, puis appuyer sur P
- `⌘ + K, ⌘ + S` : appuyer sur Cmd+K, relâcher, puis appuyer sur Cmd+S

💡 **Note** : Dans la suite de ce document, nous écrirons `Ctrl/⌘` pour indiquer `Ctrl` (Windows/Linux) ou `⌘` (macOS).

---

## Les 5 raccourcis ESSENTIELS (à maîtriser en priorité)

Ces 5 raccourcis sont **absolument indispensables**. Apprenez-les dès maintenant !

### 1. Palette de commandes : `Ctrl/⌘ + Shift + P`

**Le raccourci le plus important de VS Code !**

**À quoi ça sert ?**
Accès instantané à **toutes les commandes** de VS Code. Si vous ne vous souvenez plus d'un raccourci, la palette est là pour vous sauver.

**Comment l'utiliser** :
1. Appuyez sur `Ctrl + Shift + P` (Windows/Linux) ou `⌘ + Shift + P` (macOS)
2. Tapez ce que vous cherchez (ex: "format", "theme", "extension")
3. Sélectionnez avec les flèches ↑↓
4. Appuyez sur `Entrée`

**Exemples d'utilisation** :
```
> Format Document          (formater le code)
> Preferences: Color Theme (changer le thème)
> View: Toggle Terminal    (afficher/masquer le terminal)
> File: Save All          (tout sauvegarder)
```

**Pourquoi c'est essentiel** : Même si vous oubliez tous les autres raccourcis, celui-ci vous permet d'accéder à tout !

---

### 2. Quick Open (ouvrir rapidement un fichier) : `Ctrl/⌘ + P`

**Le deuxième raccourci le plus important !**

**À quoi ça sert ?**
Ouvrir n'importe quel fichier de votre projet en quelques touches, sans naviguer dans l'arborescence.

**Comment l'utiliser** :
1. Appuyez sur `Ctrl/⌘ + P`
2. Tapez une partie du nom du fichier
3. Sélectionnez avec les flèches
4. Appuyez sur `Entrée`

**Exemple** :
```
Votre projet :
src/
  components/
    Header.js
    Footer.js
  pages/
    Home.js

Tapez : "head" → trouve Header.js
Tapez : "home" → trouve Home.js
Tapez : "foot" → trouve Footer.js
```

**Pourquoi c'est essentiel** : Dans un gros projet, chercher un fichier dans l'arborescence prend du temps. Ce raccourci est **ultra-rapide** !

**Bonus** : Modes spéciaux de Quick Open
- `Ctrl/⌘ + P` puis tapez `@` : symboles dans le fichier actuel
- `Ctrl/⌘ + P` puis tapez `#` : symboles dans tout le projet
- `Ctrl/⌘ + P` puis tapez `:42` : aller ligne 42

---

### 3. Sauvegarder : `Ctrl/⌘ + S`

**Le réflexe à avoir !**

**À quoi ça sert ?**
Sauvegarder le fichier actuel.

**Comment l'utiliser** :
Appuyez sur `Ctrl/⌘ + S` régulièrement pendant votre travail.

**Bonne pratique** : Prenez l'habitude de sauvegarder fréquemment, même si vous avez activé l'auto-save (sauvegarde automatique).

**Variantes** :
- `Ctrl/⌘ + K, S` : Sauvegarder tout (tous les fichiers ouverts)
- `Ctrl/⌘ + K, W` : Fermer tout

---

### 4. Basculer la barre latérale : `Ctrl/⌘ + B`

**Pour gagner de l'espace à l'écran !**

**À quoi ça sert ?**
Afficher/masquer la barre latérale (explorateur de fichiers) pour avoir plus d'espace pour votre code.

**Quand l'utiliser** :
- Vous connaissez bien votre fichier et n'avez plus besoin de l'explorateur
- Vous voulez vous concentrer uniquement sur le code
- Vous travaillez sur un petit écran

**Astuce** : Combinez avec le mode Zen (`Ctrl/⌘ + K, Z`) pour une concentration maximale.

---

### 5. Basculer le terminal : `Ctrl/⌘ + ù` (ou `Ctrl/⌘ + `)

**Pour accéder rapidement au terminal !**

**À quoi ça sert ?**
Afficher/masquer le terminal intégré.

**Quand l'utiliser** :
- Vous devez exécuter une commande npm
- Vous voulez utiliser Git en ligne de commande
- Vous testez un script
- Puis vous masquez le terminal pour récupérer de l'espace

**Note** : Sur certains claviers, le raccourci peut varier. Vérifiez dans Fichier → Préférences → Raccourcis clavier.

---

## Récapitulatif : Top 5 à mémoriser cette semaine

| Raccourci | Windows/Linux | macOS | Action |
|-----------|---------------|-------|--------|
| 🏆 Palette | `Ctrl + Shift + P` | `⌘ + Shift + P` | Accès à toutes les commandes |
| 🚀 Quick Open | `Ctrl + P` | `⌘ + P` | Ouvrir un fichier rapidement |
| 💾 Sauvegarder | `Ctrl + S` | `⌘ + S` | Enregistrer le fichier |
| 📂 Barre latérale | `Ctrl + B` | `⌘ + B` | Afficher/masquer explorateur |
| 💻 Terminal | `Ctrl + ù` | `⌘ + ù` | Afficher/masquer terminal |

**Mission** : Utilisez ces 5 raccourcis pendant une semaine jusqu'à ce qu'ils deviennent automatiques !

---

## Raccourcis de navigation (Niveau 2)

Une fois les 5 essentiels maîtrisés, passez à ces raccourcis de navigation.

### Navigation entre fichiers et onglets

#### Changer d'onglet
**Raccourci** : `Ctrl/⌘ + Tab`

**À quoi ça sert ?**
Passer d'un fichier ouvert à l'autre (comme Alt+Tab pour les fenêtres).

**Utilisation** :
- `Ctrl/⌘ + Tab` : onglet suivant
- `Ctrl/⌘ + Shift + Tab` : onglet précédent

**Astuce** : Maintenez `Ctrl/⌘` enfoncé et appuyez plusieurs fois sur `Tab` pour voir tous les fichiers ouverts.

---

#### Fermer l'onglet actuel
**Raccourci** : `Ctrl/⌘ + W`

**À quoi ça sert ?**
Fermer rapidement le fichier actuel.

**Variantes** :
- `Ctrl/⌘ + K, W` : fermer tous les onglets
- `Ctrl/⌘ + K, Ctrl/⌘ + W` : fermer tous les autres onglets (garder seulement celui-ci)

---

#### Rouvrir le fichier fermé
**Raccourci** : `Ctrl/⌘ + Shift + T`

**À quoi ça sert ?**
Rouvrir le dernier fichier fermé (comme dans un navigateur web).

**Utilisation** : Vous avez fermé un fichier par erreur ? Pas de panique, ce raccourci le rouvre !

---

### Navigation dans le code

#### Aller au début/fin du fichier
**Raccourcis** :
- `Ctrl + Home` (Windows/Linux) : début du fichier
- `Ctrl + End` (Windows/Linux) : fin du fichier
- `⌘ + ↑` (macOS) : début du fichier
- `⌘ + ↓` (macOS) : fin du fichier

**À quoi ça sert ?**
Se déplacer instantanément au début ou à la fin d'un long fichier.

---

#### Aller à une ligne spécifique
**Raccourci** : `Ctrl/⌘ + G`

**À quoi ça sert ?**
Aller directement à une ligne numérotée.

**Exemple** : Une erreur vous dit "Erreur ligne 142" → `Ctrl/⌘ + G` → tapez `142` → `Entrée`

**Alternative** : `Ctrl/⌘ + P` puis tapez `:142`

---

#### Aller au symbole (fonction, classe...)
**Raccourci** : `Ctrl/⌘ + Shift + O`

**À quoi ça sert ?**
Afficher la liste de tous les symboles (fonctions, classes, titres HTML) du fichier actuel et naviguer rapidement.

**Exemple en JavaScript** :
```javascript
function calculer() { }
function afficher() { }
function valider() { }
```
Appuyez sur `Ctrl/⌘ + Shift + O` → tapez "afficher" → Entrée → vous êtes à la fonction afficher()

**Alternative** : `Ctrl/⌘ + P` puis tapez `@afficher`

---

#### Naviguer dans l'historique (comme Précédent/Suivant)
**Raccourcis** :
- `Alt + ←` (Windows/Linux) : emplacement précédent
- `Alt + →` (Windows/Linux) : emplacement suivant
- `Ctrl + -` (macOS) : emplacement précédent
- `Ctrl + Shift + -` (macOS) : emplacement suivant

**À quoi ça sert ?**
Revenir à l'endroit où vous étiez avant, comme les boutons Précédent/Suivant d'un navigateur.

**Exemple** :
1. Vous êtes dans `index.html` ligne 50
2. Vous ouvrez `style.css` ligne 100
3. `Alt + ←` vous ramène à `index.html` ligne 50
4. `Alt + →` vous ramène à `style.css` ligne 100

---

### Navigation dans l'interface

#### Afficher/Masquer différentes vues

| Vue | Windows/Linux | macOS | Description |
|-----|---------------|-------|-------------|
| Explorateur | `Ctrl + Shift + E` | `⌘ + Shift + E` | Vue fichiers |
| Recherche | `Ctrl + Shift + F` | `⌘ + Shift + F` | Recherche globale |
| Git | `Ctrl + Shift + G` | `⌘ + Shift + G` | Contrôle de code source |
| Déboguer | `Ctrl + Shift + D` | `⌘ + Shift + D` | Vue déboggage |
| Extensions | `Ctrl + Shift + X` | `⌘ + Shift + X` | Marketplace |

---

#### Basculer le panneau inférieur
**Raccourci** : `Ctrl/⌘ + J`

**À quoi ça sert ?**
Afficher/masquer le panneau du bas (terminal, problèmes, console).

**Complémentaire à** : `Ctrl/⌘ + B` (barre latérale)

---

#### Mode plein écran
**Raccourci** : `F11`

**À quoi ça sert ?**
Passer en mode plein écran pour maximiser l'espace de travail.

**Sortir du plein écran** : Appuyez à nouveau sur `F11`

---

#### Zoom
**Raccourcis** :
- `Ctrl/⌘ + =` : zoomer (agrandir)
- `Ctrl/⌘ + -` : dézoomer (réduire)
- `Ctrl/⌘ + 0` : réinitialiser le zoom

**À quoi ça sert ?**
Ajuster la taille de l'interface pour votre confort visuel.

---

## Raccourcis d'édition (Niveau 3)

Une fois à l'aise avec la navigation, ajoutez ces raccourcis d'édition.

### Édition de base

#### Couper, Copier, Coller (toute la ligne)
**Raccourcis** :
- `Ctrl/⌘ + X` : couper la ligne (même sans sélection)
- `Ctrl/⌘ + C` : copier la ligne (même sans sélection)
- `Ctrl/⌘ + V` : coller

**Particularité de VS Code** : Si vous n'avez rien sélectionné, `Ctrl/⌘ + X` ou `Ctrl/⌘ + C` copie/coupe **toute la ligne** !

**Exemple** :
```html
<h1>Titre</h1>
<!-- Curseur sur cette ligne, Ctrl+C, ligne copiée ! -->
```

---

#### Déplacer une ligne vers le haut/bas
**Raccourci** : `Alt + ↑/↓`

**À quoi ça sert ?**
Déplacer la ligne actuelle (ou les lignes sélectionnées) vers le haut ou le bas.

**Exemple** :
```html
<header>...</header>
<nav>...</nav>       ← curseur ici
<main>...</main>
```

Appuyez sur `Alt + ↑` :
```html
<nav>...</nav>       ← ligne déplacée vers le haut
<header>...</header>
<main>...</main>
```

**Utilité** : Réorganiser le code sans couper/coller !

---

#### Dupliquer une ligne
**Raccourci** : `Shift + Alt + ↓` (Windows/Linux) ou `Shift + Option + ↓` (macOS)

**À quoi ça sert ?**
Créer une copie de la ligne actuelle juste en dessous.

**Exemple** :
```html
<li>Item 1</li>  ← curseur ici
```

Appuyez sur `Shift + Alt + ↓` :
```html
<li>Item 1</li>
<li>Item 1</li>  ← ligne dupliquée
```

Modifiez ensuite la deuxième ligne :
```html
<li>Item 1</li>
<li>Item 2</li>
```

**Très utile** pour créer des structures répétitives !

---

#### Supprimer une ligne
**Raccourci** : `Ctrl/⌘ + Shift + K`

**À quoi ça sert ?**
Supprimer toute la ligne où se trouve le curseur.

**Alternative** : `Ctrl/⌘ + X` (coupe la ligne, vous pouvez ensuite la coller ailleurs si besoin)

---

#### Indenter/Désindenter
**Raccourcis** :
- `Tab` : indenter (décaler vers la droite)
- `Shift + Tab` : désindenter (décaler vers la gauche)

**À quoi ça sert ?**
Ajuster l'indentation de votre code.

**Sur plusieurs lignes** :
1. Sélectionnez plusieurs lignes
2. Appuyez sur `Tab` ou `Shift + Tab`
3. Toutes les lignes se décalent ensemble

---

### Sélection avancée

#### Sélectionner tout
**Raccourci** : `Ctrl/⌘ + A`

**À quoi ça sert ?**
Sélectionner tout le contenu du fichier.

---

#### Sélectionner la ligne entière
**Raccourci** : `Ctrl/⌘ + L`

**À quoi ça sert ?**
Sélectionner toute la ligne où se trouve le curseur.

**Appuyez plusieurs fois** : sélectionne les lignes suivantes une par une.

---

#### Sélectionner tous les mots identiques
**Raccourci** : `Ctrl/⌘ + Shift + L`

**À quoi ça sert ?**
Sélectionner toutes les occurrences du mot actuellement sélectionné.

**Exemple** :
```html
<div class="container">
  <div class="item">...</div>
  <div class="item">...</div>
  <div class="item">...</div>
</div>
```

1. Double-cliquez sur "item" (ligne 2)
2. Appuyez sur `Ctrl/⌘ + Shift + L`
3. Tous les "item" sont sélectionnés avec des curseurs multiples
4. Vous pouvez les modifier tous en même temps !

**Nous verrons le multicurseur en détail dans la section suivante.**

---

#### Étendre/réduire la sélection
**Raccourcis** :
- `Shift + Alt + →` : étendre la sélection
- `Shift + Alt + ←` : réduire la sélection

**À quoi ça sert ?**
Sélectionner intelligemment par "niveau" (mot → ligne → bloc → fonction).

**Exemple** :
```html
<div class="container">
  <h1>Titre</h1>
</div>
```

Curseur sur "Titre" :
1. `Shift + Alt + →` : sélectionne "Titre"
2. `Shift + Alt + →` : sélectionne `<h1>Titre</h1>`
3. `Shift + Alt + →` : sélectionne tout le contenu de la div
4. `Shift + Alt + ←` : réduit d'un niveau

---

### Recherche et remplacement

#### Rechercher dans le fichier
**Raccourci** : `Ctrl/⌘ + F`

**À quoi ça sert ?**
Ouvrir la boîte de recherche dans le fichier actuel.

**Navigation** :
- `Entrée` ou `F3` : occurrence suivante
- `Shift + Entrée` ou `Shift + F3` : occurrence précédente
- `Échap` : fermer la recherche

---

#### Remplacer dans le fichier
**Raccourci** : `Ctrl/⌘ + H`

**À quoi ça sert ?**
Ouvrir la boîte de recherche/remplacement.

**Boutons** :
- Remplacer une fois
- Remplacer toutes les occurrences

---

#### Rechercher dans tous les fichiers
**Raccourci** : `Ctrl/⌘ + Shift + F`

**À quoi ça sert ?**
Rechercher un texte dans tout votre projet.

**Très utile** pour trouver où une fonction ou une classe est utilisée.

---

#### Rechercher le mot sous le curseur
**Raccourci** : `Ctrl/⌘ + D`

**À quoi ça sert ?**
Sélectionner le mot actuel et trouver l'occurrence suivante.

**Appuyez plusieurs fois** : sélectionne les occurrences suivantes avec des curseurs multiples.

**Exemple** :
```css
.container { width: 100%; }
.container { padding: 20px; }
.container { margin: 0 auto; }
```

1. Curseur sur le premier "container"
2. `Ctrl/⌘ + D` : sélectionne le premier "container"
3. `Ctrl/⌘ + D` : ajoute le deuxième "container"
4. `Ctrl/⌘ + D` : ajoute le troisième "container"
5. Vous pouvez modifier les trois en même temps !

---

### Commentaires

#### Commenter/décommenter une ligne
**Raccourci** : `Ctrl/⌘ + /`

**À quoi ça sert ?**
Ajouter ou retirer le commentaire de ligne.

**Exemple en HTML** :
```html
<h1>Titre</h1>
```
Appuyez sur `Ctrl/⌘ + /` :
```html
<!-- <h1>Titre</h1> -->
```
Appuyez à nouveau pour décommenter.

**Fonctionne avec plusieurs langages** :
- HTML : `<!-- -->`
- CSS : `/* */`
- JavaScript : `//`

---

#### Commenter un bloc
**Raccourci** : `Shift + Alt + A` (Windows/Linux) ou `Shift + Option + A` (macOS)

**À quoi ça sert ?**
Créer un commentaire de bloc (plusieurs lignes).

**Exemple en CSS** :
```css
color: red;
font-size: 16px;
```
Sélectionnez les deux lignes, appuyez sur `Shift + Alt + A` :
```css
/*
color: red;
font-size: 16px;
*/
```

---

### Formatage

#### Formater le document
**Raccourci** : `Shift + Alt + F` (Windows/Linux) ou `Shift + Option + F` (macOS)

**À quoi ça sert ?**
Formater (réindenter) tout le fichier automatiquement.

**Nécessite** : Extension Prettier installée (vue dans la section précédente)

**Avant** :
```html
<div><h1>Titre</h1><p>Texte</p></div>
```

**Après** :
```html
<div>
  <h1>Titre</h1>
  <p>Texte</p>
</div>
```

---

#### Formater la sélection
**Raccourci** : `Ctrl/⌘ + K, Ctrl/⌘ + F`

**À quoi ça sert ?**
Formater seulement le code sélectionné (pas tout le fichier).

---

## Tableau récapitulatif complet

### Navigation

| Action | Windows/Linux | macOS | Priorité |
|--------|---------------|-------|----------|
| Palette de commandes | `Ctrl + Shift + P` | `⌘ + Shift + P` | ⭐⭐⭐ |
| Quick Open | `Ctrl + P` | `⌘ + P` | ⭐⭐⭐ |
| Aller à la ligne | `Ctrl + G` | `⌘ + G` | ⭐⭐ |
| Aller au symbole | `Ctrl + Shift + O` | `⌘ + Shift + O` | ⭐⭐ |
| Changer d'onglet | `Ctrl + Tab` | `⌘ + Tab` | ⭐⭐ |
| Fermer onglet | `Ctrl + W` | `⌘ + W` | ⭐⭐ |
| Historique arrière | `Alt + ←` | `Ctrl + -` | ⭐⭐ |
| Historique avant | `Alt + →` | `Ctrl + Shift + -` | ⭐⭐ |
| Début/Fin fichier | `Ctrl + Home/End` | `⌘ + ↑/↓` | ⭐ |

### Interface

| Action | Windows/Linux | macOS | Priorité |
|--------|---------------|-------|----------|
| Barre latérale | `Ctrl + B` | `⌘ + B` | ⭐⭐⭐ |
| Terminal | `Ctrl + ù` | `⌘ + ù` | ⭐⭐⭐ |
| Panneau | `Ctrl + J` | `⌘ + J` | ⭐⭐ |
| Explorateur | `Ctrl + Shift + E` | `⌘ + Shift + E` | ⭐⭐ |
| Recherche | `Ctrl + Shift + F` | `⌘ + Shift + F` | ⭐⭐ |
| Extensions | `Ctrl + Shift + X` | `⌘ + Shift + X` | ⭐ |
| Plein écran | `F11` | `F11` | ⭐ |
| Zoom +/- | `Ctrl + =/-` | `⌘ + =/-` | ⭐ |

### Édition

| Action | Windows/Linux | macOS | Priorité |
|--------|---------------|-------|----------|
| Sauvegarder | `Ctrl + S` | `⌘ + S` | ⭐⭐⭐ |
| Déplacer ligne ↑↓ | `Alt + ↑/↓` | `Option + ↑/↓` | ⭐⭐⭐ |
| Dupliquer ligne | `Shift + Alt + ↓` | `Shift + Option + ↓` | ⭐⭐⭐ |
| Supprimer ligne | `Ctrl + Shift + K` | `⌘ + Shift + K` | ⭐⭐ |
| Commenter ligne | `Ctrl + /` | `⌘ + /` | ⭐⭐⭐ |
| Sélectionner ligne | `Ctrl + L` | `⌘ + L` | ⭐⭐ |
| Indenter | `Tab` | `Tab` | ⭐⭐⭐ |
| Désindenter | `Shift + Tab` | `Shift + Tab` | ⭐⭐⭐ |
| Formater | `Shift + Alt + F` | `Shift + Option + F` | ⭐⭐⭐ |

### Recherche

| Action | Windows/Linux | macOS | Priorité |
|--------|---------------|-------|----------|
| Rechercher | `Ctrl + F` | `⌘ + F` | ⭐⭐⭐ |
| Remplacer | `Ctrl + H` | `⌘ + H` | ⭐⭐⭐ |
| Recherche globale | `Ctrl + Shift + F` | `⌘ + Shift + F` | ⭐⭐⭐ |
| Mot suivant | `Ctrl + D` | `⌘ + D` | ⭐⭐ |
| Tous les mots | `Ctrl + Shift + L` | `⌘ + Shift + L` | ⭐⭐ |

**Légende** :
- ⭐⭐⭐ : Essentiel, à apprendre en priorité
- ⭐⭐ : Très utile, à apprendre ensuite
- ⭐ : Utile, à apprendre progressivement

---

## Comment mémoriser les raccourcis ?

### Méthode 1 : La répétition espacée

**Principe** : Pratiquez chaque raccourci plusieurs fois par jour pendant une semaine.

**Exemple** :
- **Jour 1-7** : Les 5 essentiels uniquement
- **Jour 8-14** : Ajoutez 5 raccourcis de navigation
- **Jour 15-21** : Ajoutez 5 raccourcis d'édition

### Méthode 2 : Forcez-vous à utiliser les raccourcis

**Astuce** : Pendant une semaine, **interdisez-vous** d'utiliser la souris pour certaines actions.

**Exemple** :
- ❌ Ne cliquez plus sur "Fichier → Ouvrir"
- ✅ Utilisez `Ctrl/⌘ + P`

Au bout de quelques jours, ce sera automatique !

### Méthode 3 : Imprimez une aide-mémoire

1. Téléchargez la fiche de raccourcis officielle :
   - Windows : https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
   - macOS : https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf
   - Linux : https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf

2. Imprimez-la

3. Gardez-la à côté de votre écran

4. Surlignez les raccourcis que vous voulez apprendre

### Méthode 4 : Utilisez l'extension "Learn VS Code"

Il existe des extensions qui vous aident à apprendre les raccourcis progressivement, comme **"Keyboard Shortcuts Practice"**.

### Méthode 5 : Consultez le raccourci quand vous utilisez une commande

Quand vous utilisez une commande via la palette ou un menu, VS Code affiche le raccourci à côté. **Notez-le mentalement** pour l'utiliser directement la prochaine fois.

---

## Personnaliser les raccourcis clavier

### Accéder aux raccourcis clavier

**Via le menu** :
- Fichier → Préférences → Raccourcis clavier (Windows/Linux)
- Code → Préférences → Raccourcis clavier (macOS)

**Via la palette** :
`Ctrl/⌘ + Shift + P` → "Preferences: Open Keyboard Shortcuts"

**Via un raccourci** :
`Ctrl/⌘ + K, Ctrl/⌘ + S`

### Interface des raccourcis

Vous verrez une interface avec :
- **Barre de recherche** : cherchez une commande
- **Liste des raccourcis** : toutes les commandes et leurs raccourcis
- **Icône crayon** : modifier un raccourci

### Modifier un raccourci

1. Cherchez la commande (ex: "Format Document")
2. Cliquez sur l'icône **crayon** à gauche de la commande
3. Appuyez sur votre nouvelle combinaison de touches
4. Appuyez sur `Entrée` pour valider

**Attention** : VS Code vous avertit si le raccourci est déjà utilisé.

### Supprimer un raccourci

1. Clic-droit sur le raccourci
2. Choisissez **"Supprimer la combinaison de touches"**

### Réinitialiser tous les raccourcis

Si vous avez tout changé et voulez revenir aux raccourcis par défaut :
1. Cliquez sur les trois points `...` en haut à droite
2. Choisissez **"Réinitialiser tous les raccourcis clavier"**

### Exporter/Importer vos raccourcis

Vos raccourcis personnalisés sont stockés dans un fichier JSON :
- Windows : `%APPDATA%\Code\User\keybindings.json`
- macOS : `~/Library/Application Support/Code/User/keybindings.json`
- Linux : `~/.config/Code/User/keybindings.json`

Vous pouvez copier ce fichier sur une autre machine pour retrouver vos raccourcis !

---

## Astuces et bonnes pratiques

### 1. Commencez petit

Ne tentez pas d'apprendre tous les raccourcis. Maîtrisez d'abord les 5 essentiels, puis ajoutez-en 2-3 par semaine.

### 2. Utilisez la palette de commandes comme filet de sécurité

Si vous oubliez un raccourci, utilisez `Ctrl/⌘ + Shift + P`. La palette affiche le raccourci à côté de chaque commande.

### 3. Favorisez les raccourcis qui vous font gagner le plus de temps

Priorisez les raccourcis pour les actions que vous faites **des dizaines de fois par jour** :
- Sauvegarder
- Changer de fichier
- Formater le code
- Commenter/décommenter

### 4. Créez des mnémoniques

Pour mémoriser, créez des associations :
- `Ctrl + P` : **P**our ouvrir (Open)
- `Ctrl + F` : **F**ind (trouver)
- `Ctrl + H` : **H**istoriquement pour remplacer (Replace)
- `Ctrl + S` : **S**ave (sauvegarder)

### 5. Gardez vos mains sur le clavier

L'objectif des raccourcis est de **minimiser l'utilisation de la souris**. Plus vous gardez vos mains sur le clavier, plus vous êtes rapide.

### 6. Adaptez à votre workflow

Si vous trouvez qu'un raccourci ne vous convient pas, n'hésitez pas à le modifier ! VS Code est votre outil, personnalisez-le.

### 7. Partagez avec votre équipe

Si vous travaillez en équipe, discutez des raccourcis que vous utilisez. Vous découvrirez peut-être de nouvelles astuces !

---

## Différences Windows/macOS/Linux

### Touches modificatrices

| Nom | Windows/Linux | macOS |
|-----|---------------|-------|
| Contrôle | `Ctrl` | `⌘` (Cmd) |
| Alternative | `Alt` | `Option` (⌥) |
| Majuscule | `Shift` | `Shift` |

### Quelques différences notables

**Navigation**:
- Début/fin de ligne : `Home/End` (Windows) vs `⌘ + ←/→` (macOS)
- Début/fin de fichier : `Ctrl + Home/End` (Windows) vs `⌘ + ↑/↓` (macOS)

**Suppression** :
- Supprimer le mot : `Ctrl + Delete` (Windows) vs `Option + Delete` (macOS)

**La plupart des raccourcis sont identiques**, seule la touche modificatrice change (`Ctrl` vs `⌘`).

---

## Exercice de mémorisation (optionnel)

Pour tester vos connaissances, essayez de répondre sans regarder :

**Questions** :
1. Quel raccourci pour ouvrir la palette de commandes ?
2. Quel raccourci pour ouvrir rapidement un fichier ?
3. Quel raccourci pour sauvegarder ?
4. Quel raccourci pour afficher/masquer la barre latérale ?
5. Quel raccourci pour afficher/masquer le terminal ?
6. Quel raccourci pour déplacer une ligne vers le bas ?
7. Quel raccourci pour dupliquer une ligne ?
8. Quel raccourci pour commenter une ligne ?
9. Quel raccourci pour formater le document ?
10. Quel raccourci pour rechercher dans le fichier ?

**Réponses** :
1. `Ctrl/⌘ + Shift + P`
2. `Ctrl/⌘ + P`
3. `Ctrl/⌘ + S`
4. `Ctrl/⌘ + B`
5. `Ctrl/⌘ + ù`
6. `Alt/Option + ↓`
7. `Shift + Alt/Option + ↓`
8. `Ctrl/⌘ + /`
9. `Shift + Alt/Option + F`
10. `Ctrl/⌘ + F`

**Score** :
- 10/10 : Excellent ! 🏆
- 7-9/10 : Très bien ! 👍
- 5-6/10 : Bon début, continuez !
- 0-4/10 : Revoyez les 5 essentiels et pratiquez

---

## Ressources complémentaires

### Documentation officielle
- **Raccourcis clavier Windows** : https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
- **Raccourcis clavier macOS** : https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf
- **Raccourcis clavier Linux** : https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf

### Extensions utiles
- **Keyboard Shortcuts Practice** : pour pratiquer les raccourcis
- **Learn VS Code** : tutoriels interactifs

### Vidéos et tutoriels
- Chaîne YouTube "Visual Studio Code" : vidéos courtes sur les raccourcis
- Recherchez "VS Code keyboard shortcuts tutorial" sur YouTube

---

## Récapitulatif et prochaines étapes

### Ce que vous savez maintenant

Félicitations ! Vous connaissez maintenant :

- ✅ L'importance des **raccourcis clavier** pour la productivité
- ✅ Les **5 raccourcis essentiels** à maîtriser en priorité
- ✅ Les raccourcis de **navigation** dans les fichiers et le code
- ✅ Les raccourcis d'**édition** pour manipuler le code rapidement
- ✅ Les raccourcis de **recherche et remplacement**
- ✅ Comment **personnaliser** les raccourcis selon vos besoins
- ✅ Des **méthodes pour mémoriser** les raccourcis efficacement

### Votre plan d'action

**Cette semaine** :
- Maîtrisez les 5 raccourcis essentiels
- Forcez-vous à les utiliser systématiquement
- Imprimez la fiche de raccourcis

**Semaine prochaine** :
- Ajoutez 5 raccourcis de navigation
- Continuez à utiliser les 5 essentiels

**Dans deux semaines** :
- Ajoutez 5 raccourcis d'édition
- Vous devriez maintenant être beaucoup plus rapide !

### Prochaine section

Dans la section suivante, nous allons découvrir le **multicurseur**, une fonctionnalité incroyablement puissante de VS Code qui vous permettra de modifier plusieurs endroits du code simultanément. C'est un game-changer pour la productivité !

---

## Navigation


**➡️ Section suivante :** [2.2.2 Multicurseur et sélection avancée](./02-multicurseur-et-selection-avancee.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Les raccourcis clavier sont un investissement qui rapporte tous les jours. Prenez le temps de les apprendre, votre futur vous-même vous remerciera !* ⌨️✨

⏭️ [Multicurseur et sélection avancée](/02-environnement-de-developpement/02-maitrise-de-lediteur/02-multicurseur-et-selection-avancee.md)
