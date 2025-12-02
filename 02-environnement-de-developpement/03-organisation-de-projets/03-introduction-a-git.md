🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.3.3 Introduction à Git et gestion de versions

## Introduction

Imaginez que vous travaillez sur un projet web depuis plusieurs semaines. Un jour, vous modifiez votre CSS, et soudain... tout se casse ! Impossible de revenir en arrière, vous ne vous souvenez plus de ce que vous avez changé. Ou pire : votre disque dur tombe en panne et vous perdez tout votre travail.

**Git** est là pour résoudre ces problèmes. C'est un **système de gestion de versions** qui :
- 📸 Sauvegarde l'historique complet de votre projet
- ⏮️ Permet de revenir à une version précédente
- 🤝 Facilite la collaboration avec d'autres développeurs
- 🔒 Protège votre code contre les pertes de données

> 💡 **Analogie** : Git est comme une **machine à remonter le temps** pour votre code. Chaque fois que vous sauvegardez votre travail (on dit "commiter"), vous créez un point de restauration auquel vous pouvez revenir à tout moment.

---

## Qu'est-ce que Git ?

### Git vs sauvegarde classique

**Méthode classique (sans Git) :**

```
mon-projet/
├── mon-site-v1.zip
├── mon-site-v2.zip
├── mon-site-v2-final.zip
├── mon-site-v2-final-FINAL.zip
└── mon-site-v2-final-pour-de-vrai.zip
```

**Problèmes :**
- ❌ Prend beaucoup d'espace disque (duplication)
- ❌ Difficile de savoir ce qui a changé entre les versions
- ❌ Impossible de savoir qui a fait quelle modification
- ❌ Cauchemar pour travailler à plusieurs
- ❌ Pas de description des changements

**Avec Git :**

```
mon-projet/
├── index.html
├── style.css
└── script.js

+ Un historique invisible qui enregistre TOUS les changements
```

**Avantages :**
- ✅ Un seul dossier avec les fichiers actuels
- ✅ Historique complet accessible à tout moment
- ✅ Messages descriptifs pour chaque modification
- ✅ Voir qui a changé quoi et quand
- ✅ Travailler à plusieurs sans conflit
- ✅ Léger et efficace

---

## Pourquoi utiliser Git ?

### 1. Historique complet de votre projet

Git enregistre **chaque version** de votre projet avec :
- Quels fichiers ont été modifiés
- Quelles lignes de code ont changé
- Qui a fait la modification
- Quand elle a été faite
- Pourquoi (avec un message descriptif)

**Exemple d'historique :**
```
📌 "Correction du bug du menu responsive" - Jean - 02/12/2024 14:30
📌 "Ajout de la page contact" - Marie - 02/12/2024 10:15
📌 "Amélioration du design de la page d'accueil" - Jean - 01/12/2024 16:45
📌 "Première version du site" - Jean - 01/12/2024 09:00
```

Vous pouvez revenir à n'importe laquelle de ces versions en un clic !

---

### 2. Sécurité et sauvegarde

- Votre code est **sauvegardé** sur votre ordinateur (local)
- Vous pouvez aussi le **synchroniser** sur internet (GitHub, GitLab)
- Si votre ordinateur plante, votre code est en sécurité en ligne
- Impossible de perdre votre travail

---

### 3. Expérimentation sans risque

Vous voulez tester une nouvelle fonctionnalité, mais vous avez peur de tout casser ?

Avec Git, vous pouvez :
1. Créer une **branche** (une copie parallèle de votre projet)
2. Tester vos modifications
3. Si ça marche → fusionner avec le projet principal
4. Si ça ne marche pas → supprimer la branche, aucun impact !

**Schéma de branches :**
```
main (version stable)
│
├─ test-nouveau-menu (expérimentation)
│
└─ correction-bug (correction urgente)
```

---

### 4. Collaboration en équipe

Git permet à plusieurs développeurs de travailler simultanément sur le même projet :

- Chacun travaille sur sa copie locale
- Git fusionne intelligemment les modifications
- Détecte et signale les conflits potentiels
- Historique partagé visible par tous

---

## Concepts fondamentaux

Avant de commencer à utiliser Git, il faut comprendre quelques concepts clés.

### Repository (dépôt)

Un **repository** (ou "dépôt" en français, souvent abrégé "repo") est un projet géré par Git.

```
mon-projet/          ← Votre dossier normal
├── .git/            ← Dossier caché : la base de données Git
├── index.html
├── style.css
└── script.js
```

Le dossier `.git/` contient tout l'historique. **Ne le supprimez jamais !**

> 📌 **Important** : Le dossier `.git/` est caché par défaut. Pour le voir dans VS Code, c'est normal qu'il soit grisé.

---

### Working Directory, Staging Area, Repository

Git fonctionne avec **trois zones** :

```
┌─────────────────────┐
│ Working Directory   │  ← Vos fichiers en cours de modification
│ (Répertoire de      │
│  travail)           │
└─────────────────────┘
         │
         │ git add
         ↓
┌─────────────────────┐
│   Staging Area      │  ← Fichiers prêts à être sauvegardés
│   (Zone de transit) │
└─────────────────────┘
         │
         │ git commit
         ↓
┌─────────────────────┐
│    Repository       │  ← Historique permanent
│    (Dépôt Git)      │
└─────────────────────┘
```

**Explication :**

1. **Working Directory** : Votre dossier de travail normal. Vous modifiez vos fichiers ici.

2. **Staging Area** : Une zone intermédiaire. Vous préparez les fichiers que vous voulez sauvegarder.
   - Commande : `git add fichier.html`

3. **Repository** : L'historique permanent. Une fois "commité", c'est sauvegardé pour toujours.
   - Commande : `git commit -m "Message"`

> 💡 **Analogie** : C'est comme préparer un colis postal :
> 1. **Working Directory** : Vous rassemblez les objets à envoyer
> 2. **Staging Area** : Vous mettez les objets dans le carton
> 3. **Repository** : Vous fermez le carton et l'envoyez (impossible de modifier)

---

### Commit

Un **commit** est un **instantané** (snapshot) de votre projet à un moment donné.

Chaque commit contient :
- L'état de tous vos fichiers à ce moment
- Un message descriptif
- L'auteur et la date
- Un identifiant unique (hash)

**Exemple de commit :**
```
Identifiant : a3f5c9d
Auteur      : Jean Dupont <jean@example.com>
Date        : 02/12/2024 14:30:22
Message     : "Ajout de la page contact avec formulaire"

Fichiers modifiés :
  - contact.html (nouveau)
  - style.css (modifié)
  - index.html (modifié)
```

---

### Branches

Une **branche** est une ligne de développement parallèle.

```
                    ┌─ feature-menu (nouvelle fonctionnalité)
                    │
main ────●────●────●────●
              │
              └─ fix-bug (correction)
```

**Branche par défaut :** `main` (anciennement `master`)

**Utilisation des branches :**
- `main` : Version stable du projet
- `develop` : Version de développement
- `feature-xxx` : Nouvelles fonctionnalités
- `fix-xxx` : Corrections de bugs

> 📌 **Pour débuter** : Vous pouvez rester sur la branche `main`. Les branches deviennent utiles pour des projets plus complexes.

---

## Installation de Git

### Vérifier si Git est installé

Ouvrez un terminal (dans VS Code : `Ctrl + ù` ou `View > Terminal`) et tapez :

```bash
git --version
```

Si vous voyez quelque chose comme `git version 2.42.0`, Git est installé ! ✅

Sinon, vous devez l'installer :

### Installation selon votre système

**Windows :**
- Téléchargez depuis [git-scm.com](https://git-scm.com/)
- Exécutez l'installateur
- Laissez les options par défaut

**Mac :**
```bash
# Via Homebrew (recommandé)
brew install git

# Ou installez Xcode Command Line Tools
xcode-select --install
```

**Linux (Ubuntu/Debian) :**
```bash
sudo apt update
sudo apt install git
```

---

## Configuration initiale

Une fois Git installé, vous devez le configurer **une seule fois** :

```bash
# Votre nom (tel qu'il apparaîtra dans l'historique)
git config --global user.name "Jean Dupont"

# Votre email
git config --global user.email "jean.dupont@example.com"

# Vérifier la configuration
git config --list
```

> 💡 **Conseil** : Utilisez le même email que votre compte GitHub si vous comptez l'utiliser.

---

## Commandes de base

Voici les commandes essentielles pour débuter avec Git.

### 1. Initialiser un dépôt Git

Pour transformer un dossier normal en dépôt Git :

```bash
# Se placer dans votre dossier de projet
cd mon-projet

# Initialiser Git
git init
```

**Résultat :**
```
Initialized empty Git repository in /chemin/vers/mon-projet/.git/
```

Un dossier `.git/` est créé. Votre projet est maintenant géré par Git !

---

### 2. Vérifier l'état du dépôt

La commande la plus utilisée :

```bash
git status
```

**Exemple de résultat :**
```
On branch main

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        style.css
        script.js

nothing added to commit but untracked files present
```

**Interprétation :**
- Vous êtes sur la branche `main`
- Vous avez 3 fichiers non suivis (untracked)
- Ces fichiers existent mais ne sont pas encore dans Git

> 💡 **Conseil** : Utilisez `git status` souvent ! C'est votre boussole.

---

### 3. Ajouter des fichiers à la staging area

```bash
# Ajouter un fichier spécifique
git add index.html

# Ajouter plusieurs fichiers
git add style.css script.js

# Ajouter TOUS les fichiers modifiés
git add .
```

**Après `git add .` et `git status` :**
```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   index.html
        new file:   style.css
        new file:   script.js
```

Les fichiers sont maintenant dans la **staging area**, prêts à être commités.

---

### 4. Créer un commit

```bash
git commit -m "Premier commit : structure de base du site"
```

**Résultat :**
```
[main (root-commit) a3f5c9d] Premier commit : structure de base du site
 3 files changed, 150 insertions(+)
 create mode 100644 index.html
 create mode 100644 style.css
 create mode 100644 script.js
```

**Le message du commit (-m) :**
- Doit être **descriptif** : qu'est-ce qui a changé ?
- Écrit au **présent** : "Ajoute la page contact" (pas "Ajouté")
- Court mais clair : 50-70 caractères idéalement

**Exemples de bons messages :**
```bash
git commit -m "Ajoute la page contact avec formulaire"
git commit -m "Corrige le bug du menu responsive"
git commit -m "Améliore le design du header"
git commit -m "Supprime les fichiers inutilisés"
```

**Exemples de mauvais messages :**
```bash
git commit -m "modif"           ❌ Pas descriptif
git commit -m "corrections"     ❌ Trop vague
git commit -m "test"            ❌ Pas informatif
git commit -m "aaaaa"           ❌ Non professionnel
```

---

### 5. Voir l'historique des commits

```bash
git log
```

**Résultat :**
```
commit a3f5c9d8f2e1b4a7c6d5e8f9a0b1c2d3e4f5a6b7
Author: Jean Dupont <jean@example.com>
Date:   Mon Dec 2 14:30:22 2024 +0100

    Premier commit : structure de base du site
```

**Version plus courte et lisible :**
```bash
git log --oneline
```

**Résultat :**
```
a3f5c9d Premier commit : structure de base du site
```

**Avec un graphique des branches :**
```bash
git log --oneline --graph --all
```

---

### 6. Voir les modifications avant de commiter

```bash
# Voir les modifications non ajoutées (working directory)
git diff

# Voir les modifications ajoutées (staging area)
git diff --staged
```

Utile pour vérifier exactement ce qui va être commité !

---

## Workflow Git typique

Voici le cycle de travail classique avec Git :

```
1. Modifier vos fichiers
   ↓
2. Vérifier l'état
   git status
   ↓
3. Ajouter les fichiers à la staging area
   git add .
   ↓
4. Vérifier ce qui va être commité
   git status
   ↓
5. Créer un commit
   git commit -m "Description des changements"
   ↓
6. Répéter !
```

**Exemple concret :**

```bash
# 1. Vous modifiez index.html et style.css

# 2. Vérifier ce qui a changé
git status

# 3. Ajouter les fichiers modifiés
git add index.html style.css
# ou simplement : git add .

# 4. Vérifier avant de commiter
git status

# 5. Créer le commit
git commit -m "Améliore le design du header"

# 6. Continuer à travailler...
```

---

## Commandes utiles pour débuter

### Annuler des modifications

```bash
# Annuler les modifications d'un fichier (avant git add)
git restore fichier.html

# Retirer un fichier de la staging area (après git add, avant commit)
git restore --staged fichier.html

# Voir un fichier tel qu'il était au dernier commit
git show HEAD:fichier.html
```

---

### Ignorer des fichiers avec .gitignore

Certains fichiers ne doivent **pas** être versionnés :
- Fichiers temporaires
- Dossiers de dépendances (`node_modules/`)
- Fichiers de configuration locale
- Fichiers sensibles (mots de passe, clés API)

**Créez un fichier `.gitignore` à la racine :**

```
# Fichiers à ignorer

# Dossiers
node_modules/
dist/
.cache/

# Fichiers système
.DS_Store
Thumbs.db
desktop.ini

# Éditeurs
.vscode/
.idea/
*.swp

# Fichiers de configuration locale
.env
config.local.js

# Fichiers temporaires
*.log
*.tmp
```

Git ignorera automatiquement tous ces fichiers !

---

## GitHub / GitLab / Bitbucket

### Qu'est-ce que GitHub ?

**Git ≠ GitHub**

- **Git** : Logiciel de gestion de versions (local sur votre ordinateur)
- **GitHub** : Plateforme en ligne pour héberger vos dépôts Git

**Autres plateformes similaires :**
- **GitLab** : Alternative à GitHub, open-source
- **Bitbucket** : Alternative populaire en entreprise

### Pourquoi utiliser GitHub ?

1. **Sauvegarde en ligne** : Votre code est sécurisé sur internet
2. **Collaboration** : Travaillez facilement avec d'autres développeurs
3. **Portfolio** : Montrez vos projets aux recruteurs
4. **Open source** : Contribuez à des projets existants
5. **Gratuit** : Dépôts publics et privés gratuits

---

### Créer un compte GitHub

1. Allez sur [github.com](https://github.com)
2. Cliquez sur "Sign up" (S'inscrire)
3. Créez votre compte avec un **email professionnel**
4. Choisissez un **nom d'utilisateur professionnel** : `jean-dupont` plutôt que `xXDarkLord666Xx`

> 💡 **Conseil** : Votre profil GitHub est souvent consulté par les recruteurs. Soignez-le !

---

### Connecter un dépôt local à GitHub

**Étape 1 : Créer un dépôt sur GitHub**

1. Cliquez sur "New repository"
2. Nommez votre dépôt : `mon-premier-site`
3. Laissez les autres options par défaut
4. Cliquez sur "Create repository"

**Étape 2 : Connecter votre dépôt local**

GitHub vous donne les commandes à exécuter :

```bash
# Ajouter l'URL du dépôt distant
git remote add origin https://github.com/votre-username/mon-premier-site.git

# Renommer la branche en main (si nécessaire)
git branch -M main

# Envoyer vos commits sur GitHub
git push -u origin main
```

**Explication :**
- `origin` : Nom conventionnel du dépôt distant
- `push` : Envoyer vos commits locaux vers GitHub
- `-u origin main` : Définir `origin/main` comme branche de suivi par défaut

---

### Commandes pour synchroniser avec GitHub

```bash
# Envoyer vos commits locaux vers GitHub
git push

# Récupérer les modifications depuis GitHub
git pull

# Voir les dépôts distants configurés
git remote -v
```

**Workflow avec GitHub :**

```
Votre ordinateur                    GitHub
     (local)                        (distant)
        │                               │
        │     git push                  │
        ├──────────────────────────────>│
        │                               │
        │     git pull                  │
        │<──────────────────────────────┤
        │                               │
```

---

## Commandes Git essentielles - Récapitulatif

| Commande | Description |
|----------|-------------|
| `git init` | Initialiser un dépôt Git |
| `git status` | Voir l'état du dépôt |
| `git add fichier` | Ajouter un fichier à la staging area |
| `git add .` | Ajouter tous les fichiers modifiés |
| `git commit -m "message"` | Créer un commit |
| `git log` | Voir l'historique |
| `git log --oneline` | Historique condensé |
| `git diff` | Voir les modifications |
| `git restore fichier` | Annuler les modifications |
| `git restore --staged fichier` | Retirer de la staging area |
| `git remote add origin URL` | Connecter à un dépôt distant |
| `git push` | Envoyer les commits vers GitHub |
| `git pull` | Récupérer les modifications depuis GitHub |
| `git clone URL` | Cloner un dépôt existant |

---

## Bonnes pratiques

### 1. Commitez régulièrement

```
✅ Bon : Petits commits fréquents
- "Ajoute la structure HTML de la page d'accueil"
- "Style le header avec CSS"
- "Ajoute le menu de navigation"

❌ Mauvais : Un gros commit à la fin de la journée
- "Modifications de la journée"
```

**Principe :** Un commit = Une fonctionnalité ou correction logique

---

### 2. Écrivez des messages de commit clairs

**Format recommandé :**
```
Type: Description courte

Type : feat, fix, style, docs, refactor
```

**Exemples :**
```bash
git commit -m "feat: Ajoute la page contact"
git commit -m "fix: Corrige le bug du menu mobile"
git commit -m "style: Améliore le design du footer"
git commit -m "docs: Met à jour le README"
```

---

### 3. Ne commitez jamais de fichiers sensibles

```
❌ JAMAIS dans Git :
- Mots de passe
- Clés API
- Tokens d'authentification
- Fichiers .env avec des secrets
```

Utilisez `.gitignore` pour les exclure automatiquement !

---

### 4. Synchronisez régulièrement avec GitHub

```bash
# À la fin de chaque session de travail
git push

# Au début de chaque session
git pull
```

---

## Cas d'usage courants

### Scénario 1 : Démarrer un nouveau projet

```bash
# 1. Créer le dossier
mkdir mon-nouveau-projet
cd mon-nouveau-projet

# 2. Initialiser Git
git init

# 3. Créer vos fichiers
touch index.html style.css script.js

# 4. Faire le premier commit
git add .
git commit -m "Initial commit : structure de base"

# 5. (Optionnel) Connecter à GitHub
git remote add origin https://github.com/username/mon-nouveau-projet.git
git push -u origin main
```

---

### Scénario 2 : Cloner un projet existant

```bash
# Cloner depuis GitHub
git clone https://github.com/username/projet-existant.git

# Entrer dans le dossier
cd projet-existant

# Vous avez maintenant tout l'historique du projet !
```

---

### Scénario 3 : Travailler sur votre projet

```bash
# Modifier vos fichiers...

# Voir ce qui a changé
git status

# Ajouter et commiter
git add .
git commit -m "feat: Ajoute la fonctionnalité X"

# Envoyer sur GitHub
git push
```

---

## Intégration Git dans VS Code

VS Code a Git intégré ! Vous n'avez pas besoin du terminal pour les opérations de base.

### Panneau Source Control

1. Cliquez sur l'icône de "Source Control" dans la barre latérale (ou `Ctrl + Shift + G`)
2. Vous voyez tous vos fichiers modifiés
3. Cliquez sur le `+` à côté d'un fichier pour faire `git add`
4. Écrivez votre message de commit en haut
5. Cliquez sur le ✓ pour commiter

### Indicateurs visuels

VS Code montre des indicateurs dans les fichiers :
- **M** (Modified) : Fichier modifié
- **A** (Added) : Nouveau fichier
- **D** (Deleted) : Fichier supprimé
- **U** (Untracked) : Fichier non suivi par Git

---

## Ressources pour aller plus loin

### Documentation officielle
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)

### Tutoriels interactifs
- [Learn Git Branching](https://learngitbranching.js.org/) : Apprendre Git en s'amusant
- [Git Immersion](https://gitimmersion.com/) : Tutoriel pratique étape par étape

### Aide-mémoire (Cheat Sheet)
- [Git Cheat Sheet GitHub](https://education.github.com/git-cheat-sheet-education.pdf)

---

## Que retenir pour débuter ?

### Les 5 commandes essentielles

```bash
1. git status     # Où j'en suis ?
2. git add .      # Préparer mes fichiers
3. git commit -m  # Sauvegarder
4. git push       # Envoyer sur GitHub
5. git pull       # Récupérer depuis GitHub
```

### Les concepts clés

1. **Git** = machine à remonter le temps pour votre code
2. **Commit** = point de sauvegarde avec description
3. **GitHub** = sauvegarde en ligne + collaboration
4. **Commitez souvent** avec des messages clairs
5. **Utilisez .gitignore** pour les fichiers à exclure

---

## Pour aller plus loin

Dans les prochains chapitres et au fil de votre apprentissage, vous découvrirez :

- **Branches** : Travailler sur plusieurs fonctionnalités en parallèle
- **Merge** : Fusionner des branches
- **Conflits** : Les résoudre quand deux personnes modifient le même fichier
- **Pull Requests** : Proposer des modifications sur GitHub
- **Issues** : Gérer les bugs et fonctionnalités
- **Git Flow** : Workflow avancé pour les grandes équipes

Mais pour l'instant, maîtriser les bases (`add`, `commit`, `push`, `pull`) est largement suffisant ! 🚀

---

## Conclusion

Git est un outil **essentiel** pour tout développeur web. Au début, cela peut sembler complexe, mais avec la pratique, cela devient une seconde nature.

**Commencez simple :**
1. Initialisez Git dans vos projets
2. Commitez régulièrement
3. Synchronisez avec GitHub

Petit à petit, vous découvrirez des fonctionnalités plus avancées. L'important est de **prendre l'habitude** d'utiliser Git dès maintenant dans tous vos projets !

> 💡 **Conseil final** : Même pour de petits projets personnels, utilisez Git. C'est comme ça qu'on apprend et qu'on développe de bonnes habitudes professionnelles.

Bienvenue dans le monde de la gestion de versions ! 🎉

⏭️ [Outils de développement du navigateur (DevTools)](/02-environnement-de-developpement/04-devtools-du-navigateur/README.md)
