🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.2.5 Terminal intégré

## Introduction

Le **terminal intégré** de VS Code est l'une de ses fonctionnalités les plus puissantes. Il vous permet d'exécuter des **commandes en ligne de commande** directement dans votre éditeur, sans avoir à jongler entre plusieurs fenêtres. Pour un développeur web moderne, maîtriser le terminal est devenu indispensable.

### Qu'est-ce qu'un terminal ?

Un **terminal** (aussi appelé "invite de commandes", "console" ou "ligne de commande") est une interface **textuelle** qui permet de communiquer avec votre ordinateur en tapant des **commandes**.

**Analogie** : C'est comme parler directement à votre ordinateur dans sa langue, au lieu d'utiliser la souris et les icônes.

**Interface graphique (GUI)** :
```
[📁 Dossier] → Double-clic → Le dossier s'ouvre
[📄 Fichier] → Double-clic → Le fichier s'ouvre
```

**Terminal (CLI - Command Line Interface)** :
```
> cd mon-dossier     (entrer dans le dossier)
> ls                 (lister les fichiers)
> code fichier.html  (ouvrir le fichier dans VS Code)
```

### Pourquoi utiliser un terminal ?

Vous pourriez vous demander : "Pourquoi taper des commandes alors que je peux tout faire avec la souris ?"

**Raisons importantes** :

#### 1. Certaines tâches nécessitent le terminal
En développement web moderne, **vous devez** utiliser le terminal pour :
- 📦 Installer des paquets npm (`npm install`)
- 🚀 Lancer des serveurs de développement (`npm start`)
- 🌿 Utiliser Git pour versionner votre code
- 🏗️ Compiler et construire votre code
- 🧪 Exécuter des tests

**Il n'y a pas d'alternative graphique** pour ces tâches !

#### 2. C'est plus rapide
Une fois que vous connaissez les commandes, c'est **beaucoup plus rapide** que de naviguer avec la souris.

**Exemple** : Créer un dossier et 3 fichiers dedans
- **Avec la souris** : Clic-droit → Nouveau dossier → Nommer → Entrer dans le dossier → Clic-droit → Nouveau fichier → Nommer → Répéter 2 fois
- **Avec le terminal** : `mkdir mon-projet && cd mon-projet && touch index.html style.css script.js` (5 secondes)

#### 3. C'est plus puissant
Le terminal permet d'automatiser des tâches répétitives, de manipuler des centaines de fichiers en une commande, etc.

#### 4. C'est universel
Les commandes du terminal fonctionnent sur tous les systèmes (Windows, macOS, Linux). C'est le langage universel des développeurs.

#### 5. C'est la norme dans l'industrie
Tous les tutoriels, documentations et projets professionnels utilisent le terminal. **Vous devez apprendre à l'utiliser.**

### Le terminal intégré de VS Code

**Avantages du terminal intégré** :
- ✅ S'ouvre **dans VS Code**, pas besoin d'une fenêtre séparée
- ✅ S'ouvre automatiquement dans le **dossier de votre projet**
- ✅ Vous voyez **votre code et le terminal** en même temps
- ✅ Vous pouvez avoir **plusieurs terminaux** ouverts
- ✅ Les liens sont **cliquables** (chemins de fichiers, URLs)
- ✅ **Coloration syntaxique** et auto-complétion

---

## Ouvrir le terminal intégré

### Méthode 1 : Raccourci clavier (recommandé)

**Le plus rapide** :
- **Windows/Linux** : `Ctrl + ù` (ou `Ctrl + `` sur certains claviers)
- **macOS** : `⌘ + ù` (ou `Ctrl + `` sur certains claviers)

**Note** : Le caractère `` ` `` est la touche en haut à gauche du clavier, sous `Échap`.

**Appuyez une fois** : ouvre le terminal
**Appuyez à nouveau** : ferme le terminal

---

### Méthode 2 : Via le menu

1. **Menu** → **Terminal** → **Nouveau terminal**
2. Ou : **Affichage** → **Terminal**

---

### Méthode 3 : Via la palette de commandes

1. `Ctrl/⌘ + Shift + P`
2. Tapez "Terminal: Create New Terminal"
3. Appuyez sur `Entrée`

---

### Méthode 4 : Raccourci dans la barre d'état

En bas à droite de VS Code, vous pouvez voir des icônes. Cliquez sur l'icône de terminal (ressemble à `>_`).

---

## Interface du terminal

### Les éléments du terminal

Quand vous ouvrez le terminal, vous verrez plusieurs zones :

```
┌─────────────────────────────────────────────────┐
│  TERMINAL ▼  | bash | zsh | PowerShell | + ⚙️   │  ← Onglets et options
├─────────────────────────────────────────────────┤
│                                                 │
│  C:\Users\VotreNom\projets\mon-site>_           │  ← Invite de commande
│                                                 │
│                                                 │
└─────────────────────────────────────────────────┘
```

#### 1. Barre d'onglets du terminal
- **Nom du terminal** : "TERMINAL", "bash", "PowerShell", etc.
- **Menu déroulant** (▼) : liste de tous les terminaux ouverts
- **Bouton +** : créer un nouveau terminal
- **Icône ⚙️** : paramètres du terminal

#### 2. Invite de commande (Prompt)
C'est la ligne où vous tapez vos commandes.

**Exemples selon le système** :

**Windows (PowerShell)** :
```powershell
PS C:\Users\VotreNom\projets\mon-site>
```

**macOS/Linux (bash/zsh)** :
```bash
VotreNom@MacBook mon-site %
```
ou
```bash
user@hostname:~/projets/mon-site$
```

**Signification** :
- Le texte avant `>` ou `$` indique où vous êtes (le dossier actuel)
- Le symbole `>`, `$` ou `%` indique que le terminal attend une commande
- Le curseur clignotant `_` indique où vous pouvez taper

---

## Types de terminaux disponibles

VS Code peut utiliser différents **shells** (interpréteurs de commandes).

### Sur Windows

#### PowerShell (recommandé)
- **Moderne** et puissant
- Installé par défaut sur Windows 10/11
- Syntaxe proche de Unix
- **Notre recommandation** pour Windows

#### Command Prompt (CMD)
- **Ancien** terminal Windows
- Moins de fonctionnalités
- Toujours présent pour compatibilité

#### Git Bash
- Terminal Unix sur Windows
- Installé avec Git for Windows
- Commandes Linux/macOS sur Windows
- **Très utile** pour uniformiser avec macOS/Linux

---

### Sur macOS

#### Zsh (par défaut depuis macOS Catalina)
- Terminal moderne de macOS
- Puissant et avec auto-complétion
- **Recommandé**

#### Bash
- Ancien terminal par défaut de macOS
- Toujours disponible
- Compatible avec Linux

---

### Sur Linux

#### Bash (le plus courant)
- Terminal standard Linux
- Puissant et versatile
- **Recommandé**

#### Zsh
- Alternative moderne à Bash
- Plus de fonctionnalités

---

### Changer le shell par défaut

Pour changer le terminal par défaut dans VS Code :

1. Cliquez sur la **flèche vers le bas** (▼) à côté du **+** dans le terminal
2. Choisissez **"Sélectionner le shell par défaut"**
3. Sélectionnez le shell souhaité dans la liste

**Ou dans les paramètres** :
```json
{
  "terminal.integrated.defaultProfile.windows": "PowerShell",
  "terminal.integrated.defaultProfile.osx": "zsh",
  "terminal.integrated.defaultProfile.linux": "bash"
}
```

---

## Commandes de base du terminal

Maintenant, apprenons les commandes essentielles. Nous les présenterons pour Windows et Unix (macOS/Linux).

### Navigation dans les dossiers

#### Afficher le dossier actuel (Print Working Directory)

**Unix (macOS/Linux)** :
```bash
pwd
```

**Windows (PowerShell/CMD)** :
```powershell
pwd
# ou
cd
```

**Résultat** :
```
C:\Users\VotreNom\projets\mon-site
```

Cela vous montre **où vous êtes** dans l'arborescence des fichiers.

---

#### Lister les fichiers et dossiers (List)

**Unix (macOS/Linux)** :
```bash
ls
```

**Windows (PowerShell)** :
```powershell
ls
# ou
dir
```

**Résultat** :
```
index.html
style.css
script.js
images/
```

**Avec détails** :
```bash
ls -l    # Unix
dir      # Windows CMD
```

**Afficher les fichiers cachés** :
```bash
ls -a    # Unix (montre les fichiers qui commencent par .)
ls -Force  # PowerShell
```

---

#### Changer de dossier (Change Directory)

**Syntaxe universelle** :
```bash
cd nom-du-dossier
```

**Exemples** :

**Entrer dans un sous-dossier** :
```bash
cd images
```

**Remonter d'un niveau (dossier parent)** :
```bash
cd ..
```

**Aller à la racine du disque** :
```bash
cd /          # Unix
cd C:\        # Windows
```

**Aller au dossier personnel** :
```bash
cd ~          # Unix
cd %USERPROFILE%  # Windows CMD
cd $HOME      # PowerShell
```

**Aller directement à un chemin** :
```bash
cd /Users/nom/projets/mon-site     # macOS/Linux
cd C:\Users\nom\projets\mon-site   # Windows
```

**Revenir au dossier précédent** :
```bash
cd -      # Unix
cd -      # PowerShell (peut ne pas fonctionner sur CMD)
```

---

### Manipulation de fichiers et dossiers

#### Créer un dossier (Make Directory)

**Syntaxe universelle** :
```bash
mkdir nom-du-dossier
```

**Exemples** :
```bash
mkdir mon-projet
mkdir images
mkdir css js
```

**Créer plusieurs niveaux** :
```bash
mkdir -p projets/mon-site/css    # Unix
mkdir projets\mon-site\css       # Windows
```

---

#### Créer un fichier vide

**Unix (macOS/Linux)** :
```bash
touch index.html
touch style.css script.js
```

**Windows (PowerShell)** :
```powershell
New-Item index.html
# ou
echo $null > index.html
```

**Windows (CMD)** :
```cmd
type nul > index.html
```

---

#### Copier un fichier (Copy)

**Unix (macOS/Linux)** :
```bash
cp fichier.txt copie.txt
```

**Windows** :
```powershell
copy fichier.txt copie.txt
# ou PowerShell
Copy-Item fichier.txt copie.txt
```

**Copier un dossier** :
```bash
cp -r dossier/ copie-dossier/      # Unix
Copy-Item -Recurse dossier copie   # PowerShell
xcopy dossier copie /E /I          # CMD
```

---

#### Déplacer/Renommer un fichier (Move)

**Unix (macOS/Linux)** :
```bash
mv ancien-nom.txt nouveau-nom.txt
```

**Windows** :
```powershell
move ancien-nom.txt nouveau-nom.txt
# ou PowerShell
Move-Item ancien-nom.txt nouveau-nom.txt
```

---

#### Supprimer un fichier (Remove)

**Unix (macOS/Linux)** :
```bash
rm fichier.txt
```

**Windows** :
```powershell
del fichier.txt
# ou PowerShell
Remove-Item fichier.txt
```

**⚠️ Attention** : La suppression est **définitive** (pas de corbeille) !

**Supprimer un dossier** :
```bash
rm -r dossier/              # Unix
Remove-Item -Recurse dossier  # PowerShell
rmdir /S dossier            # CMD
```

---

#### Afficher le contenu d'un fichier

**Unix (macOS/Linux)** :
```bash
cat fichier.txt      # Affiche tout le fichier
head fichier.txt     # 10 premières lignes
tail fichier.txt     # 10 dernières lignes
```

**Windows (PowerShell)** :
```powershell
type fichier.txt
# ou PowerShell
Get-Content fichier.txt
```

---

### Commandes utiles

#### Effacer l'écran du terminal

**Syntaxe universelle** :
```bash
clear      # Unix
cls        # Windows CMD
clear      # PowerShell (aussi)
```

**Raccourci** : `Ctrl + L` (fonctionne souvent sur tous les systèmes)

---

#### Afficher un message

**Syntaxe universelle** :
```bash
echo "Bonjour le monde"
```

**Résultat** :
```
Bonjour le monde
```

---

#### Afficher l'historique des commandes

**Syntaxe** :
```bash
history    # Unix
Get-History  # PowerShell
doskey /history  # CMD
```

**Naviguer dans l'historique** :
- `↑` : commande précédente
- `↓` : commande suivante

**Rechercher dans l'historique** :
- `Ctrl + R` : recherche inversée (Unix/PowerShell)

---

#### Annuler une commande en cours

**Raccourci universel** : `Ctrl + C`

**Exemple** :
```bash
# Une commande qui prend trop de temps
npm install
# Appuyez sur Ctrl + C pour l'arrêter
^C
```

---

#### Auto-complétion avec Tab

Appuyez sur `Tab` pour **auto-compléter** les noms de fichiers et dossiers.

**Exemple** :
```bash
cd proj<Tab>
# S'auto-complète en :
cd projets/
```

**Double Tab** : Si plusieurs options existent, `Tab` deux fois affiche toutes les options.

---

## Commandes spécifiques au développement web

### Ouvrir VS Code depuis le terminal

**Commande** :
```bash
code .
```

- `code` : lance VS Code
- `.` : ouvre le dossier actuel

**Autres exemples** :
```bash
code index.html        # Ouvre index.html dans VS Code
code mon-projet/       # Ouvre le dossier mon-projet
code .                 # Ouvre le dossier actuel
```

**Si la commande ne fonctionne pas** :
1. Ouvrez VS Code
2. `Ctrl/⌘ + Shift + P`
3. Tapez "Shell Command: Install 'code' command in PATH"
4. Relancez votre terminal

---

### Git (gestion de versions)

**Vérifier si Git est installé** :
```bash
git --version
```

**Commandes Git de base** :
```bash
git init                      # Initialiser un dépôt Git
git add .                     # Ajouter tous les fichiers
git commit -m "Mon message"   # Créer un commit
git status                    # Voir l'état du dépôt
git log                       # Voir l'historique
```

*(Nous verrons Git en détail dans une section ultérieure)*

---

### npm (gestionnaire de paquets JavaScript)

**Vérifier si npm est installé** :
```bash
npm --version
```

**Commandes npm de base** :
```bash
npm init                 # Initialiser un projet npm
npm install              # Installer les dépendances
npm install nom-paquet   # Installer un paquet
npm start                # Lancer le script "start"
npm run build            # Lancer le script "build"
```

*(Nous verrons npm en détail dans une section ultérieure)*

---

### Lancer un serveur local

**Avec Python (si installé)** :
```bash
# Python 3
python -m http.server 8000
# ou Python 2
python -m SimpleHTTPServer 8000
```

**Avec Node.js et http-server** :
```bash
npx http-server
```

**Avec Live Server (extension VS Code)** :
- Pas besoin de commande, utilisez l'extension !

---

## Gérer plusieurs terminaux

### Créer un nouveau terminal

**Méthode 1 : Icône +**
- Cliquez sur le **+** dans la barre du terminal

**Méthode 2 : Raccourci**
- `Ctrl/⌘ + Shift + ù` : nouveau terminal

**Méthode 3 : Palette**
- `Ctrl/⌘ + Shift + P` → "Terminal: Create New Terminal"

---

### Naviguer entre les terminaux

**Avec la souris** :
- Cliquez sur l'onglet du terminal souhaité

**Avec le clavier** :
- Menu déroulant (▼) → Sélectionnez le terminal
- Ou utilisez les raccourcis (selon configuration)

---

### Diviser le terminal (Split)

Vous pouvez avoir **plusieurs terminaux côte à côte**.

**Méthode** :
1. Cliquez sur l'**icône de division** (deux rectangles) dans la barre du terminal
2. Un nouveau terminal s'ouvre à côté

**Raccourci** : `Ctrl/⌘ + \` (dans le terminal)

**Exemple d'utilisation** :
- Terminal 1 : serveur de développement (`npm start`)
- Terminal 2 : commandes Git

---

### Fermer un terminal

**Méthode 1 : Commande**
```bash
exit
```

**Méthode 2 : Icône corbeille**
- Cliquez sur l'icône **poubelle** dans la barre du terminal

**Méthode 3 : Raccourci**
- `Ctrl + D` (Unix)
- Tapez `exit` puis `Entrée` (Windows)

---

### Renommer un terminal

**Utile** quand vous avez plusieurs terminaux ouverts.

**Méthode** :
1. Clic-droit sur l'onglet du terminal
2. Choisissez **"Rename"**
3. Donnez un nom explicite (ex: "Serveur", "Git", "Tests")

---

## Configuration du terminal

### Personnaliser l'apparence

**Taille de la police** :
```json
{
  "terminal.integrated.fontSize": 14
}
```

**Famille de police** :
```json
{
  "terminal.integrated.fontFamily": "Consolas, 'Courier New', monospace"
}
```

**Hauteur de ligne** :
```json
{
  "terminal.integrated.lineHeight": 1.2
}
```

**Curseur** :
```json
{
  "terminal.integrated.cursorStyle": "block",  // ou "line", "underline"
  "terminal.integrated.cursorBlinking": true
}
```

---

### Paramètres utiles

**Démarrage automatique** :
```json
{
  "terminal.integrated.automationProfile.windows": null
}
```

**Nombre de lignes dans l'historique** :
```json
{
  "terminal.integrated.scrollback": 10000
}
```

**Copier lors de la sélection** :
```json
{
  "terminal.integrated.copyOnSelection": true
}
```

---

## Astuces et raccourcis

### Raccourcis clavier essentiels

| Action | Raccourci |
|--------|-----------|
| Ouvrir/Fermer terminal | `Ctrl/⌘ + ù` |
| Nouveau terminal | `Ctrl/⌘ + Shift + ù` |
| Diviser terminal | `Ctrl/⌘ + \` |
| Effacer terminal | `Ctrl + L` ou `clear` |
| Annuler commande | `Ctrl + C` |
| Copier | `Ctrl/⌘ + C` (sélection active) |
| Coller | `Ctrl/⌘ + V` |
| Rechercher | `Ctrl/⌘ + F` |

---

### Navigation rapide

**Début/Fin de ligne** :
- `Home` ou `Ctrl + A` : début de ligne
- `End` ou `Ctrl + E` : fin de ligne

**Mot par mot** :
- `Ctrl + ←/→` : sauter de mot en mot

**Effacer** :
- `Ctrl + U` : effacer toute la ligne
- `Ctrl + K` : effacer depuis le curseur jusqu'à la fin
- `Ctrl + W` : effacer le mot précédent

---

### Liens cliquables

Dans le terminal VS Code, les **chemins de fichiers** et **URLs** sont cliquables.

**Exemple** :
```bash
npm start
# Affiche : Server running at http://localhost:3000
```

`Ctrl + Clic` sur `http://localhost:3000` ouvre l'URL dans votre navigateur !

**Chemin de fichier** :
```bash
Error in /Users/nom/projet/index.html:10
```

`Ctrl + Clic` sur le chemin ouvre le fichier à la ligne 10 !

---

### Copier-coller dans le terminal

**Copier** :
1. Sélectionnez le texte avec la souris
2. `Ctrl/⌘ + C` (ou clic-droit → Copier)

**Coller** :
- `Ctrl/⌘ + V`
- Ou clic-droit → Coller

**Astuce Windows** : Dans certains terminaux Windows, clic-droit colle automatiquement.

---

### Rechercher dans le terminal

**Ouvrir la recherche** : `Ctrl/⌘ + F`

**Navigation** :
- `Entrée` ou `F3` : occurrence suivante
- `Shift + Entrée` ou `Shift + F3` : occurrence précédente

**Utile** pour retrouver une commande ou un message d'erreur dans un long historique.

---

## Bonnes pratiques

### 1. Gardez le terminal ouvert

**Habitude à prendre** : Toujours avoir un terminal ouvert dans VS Code pendant que vous codez.

**Pourquoi** :
- Vous êtes prêt à exécuter des commandes rapidement
- Vous voyez les erreurs en temps réel (serveur, compilation)
- Workflow plus fluide

---

### 2. Utilisez plusieurs terminaux

**Organisez vos terminaux** :
- Terminal 1 : serveur de développement (toujours actif)
- Terminal 2 : commandes ponctuelles (Git, npm install, etc.)
- Terminal 3 : tests (si nécessaire)

**Renommez-les** pour vous y retrouver !

---

### 3. Apprenez les commandes progressivement

**Ne tentez pas** d'apprendre toutes les commandes d'un coup.

**Progression recommandée** :
- Semaine 1 : `cd`, `ls`, `pwd`
- Semaine 2 : `mkdir`, `touch`, `rm`
- Semaine 3 : `git` de base
- Semaine 4 : `npm` de base

---

### 4. Utilisez l'auto-complétion (Tab)

**Toujours** appuyez sur `Tab` pour auto-compléter :
- Noms de fichiers
- Noms de dossiers
- Commandes

**C'est plus rapide** et **évite les erreurs de frappe**.

---

### 5. Consultez l'aide des commandes

**Syntaxe** :
```bash
commande --help        # Général
git --help            # Aide Git
npm help              # Aide npm
man commande          # Manuel (Unix)
```

**Exemple** :
```bash
git --help
# Affiche toutes les commandes Git disponibles
```

---

### 6. Sauvegardez vos commandes utiles

**Créez un fichier** avec vos commandes fréquentes :

**commands.md** :
```markdown
# Mes commandes utiles

## Démarrer le projet
npm install
npm start

## Git
git add .
git commit -m "message"
git push

## Etc.
```

---

### 7. Faites attention aux commandes destructrices

**Commandes dangereuses** :
- `rm -rf` : supprime tout (irréversible !)
- `rm *` : supprime tous les fichiers du dossier
- `git reset --hard` : supprime les modifications

**Toujours vérifier** avant d'appuyer sur `Entrée` !

---

## Dépannage : problèmes courants

### Problème 1 : Le terminal ne s'ouvre pas

**Solutions** :
1. Redémarrez VS Code
2. Vérifiez dans Affichage → Terminal
3. Vérifiez les paramètres du shell par défaut

---

### Problème 2 : La commande 'code' n'est pas reconnue

**Cause** : La commande `code` n'est pas dans le PATH.

**Solution** :
1. `Ctrl/⌘ + Shift + P`
2. "Shell Command: Install 'code' command in PATH"
3. Redémarrez votre terminal

---

### Problème 3 : Encodage de caractères incorrect

**Symptôme** : Les accents affichent mal (é → Ã©)

**Solution Windows** :
```powershell
chcp 65001
```

**Ou dans les paramètres** :
```json
{
  "terminal.integrated.defaultProfile.windows": "PowerShell"
}
```

---

### Problème 4 : Le terminal est trop lent

**Causes possibles** :
- Historique trop long
- Extensions qui ralentissent
- Antivirus qui scanne chaque commande

**Solutions** :
```json
{
  "terminal.integrated.scrollback": 1000  // Réduire l'historique
}
```

---

### Problème 5 : Permissions refusées

**Symptôme** :
```
Error: EACCES: permission denied
```

**Solutions** :
- **Unix** : Utilisez `sudo` (avec précaution)
- **Windows** : Lancez VS Code en administrateur
- Vérifiez les permissions du dossier

---

## Aller plus loin

### Personnaliser votre shell

**Oh My Zsh** (macOS/Linux) :
- Thèmes et plugins pour zsh
- Auto-complétion avancée
- Site : https://ohmyz.sh

**Oh My Posh** (Windows PowerShell) :
- Thèmes pour PowerShell
- Interface moderne
- Site : https://ohmyposh.dev

---

### Extensions VS Code pour le terminal

**Terminal Tabs** :
- Meilleure gestion des onglets de terminal

**Terminal Here** :
- Ouvrir le terminal dans n'importe quel dossier

---

### Commandes avancées (pour plus tard)

**Pipes et redirection** :
```bash
ls | grep ".html"           # Filtrer la sortie
echo "texte" > fichier.txt  # Écrire dans un fichier
```

**Scripts** :
- Automatisez des tâches répétitives avec des scripts bash/PowerShell

---

## Récapitulatif

### Ce que vous savez maintenant

Félicitations ! Vous maîtrisez maintenant :

- ✅ Ce qu'est un **terminal** et pourquoi c'est important
- ✅ Comment **ouvrir** le terminal intégré de VS Code
- ✅ Les **commandes de base** pour naviguer et manipuler fichiers
- ✅ Les **différents shells** (PowerShell, bash, zsh)
- ✅ Comment **gérer plusieurs terminaux** simultanément
- ✅ Les **raccourcis clavier** essentiels
- ✅ Les **bonnes pratiques** d'utilisation
- ✅ Comment **dépanner** les problèmes courants

### Commandes essentielles à retenir

**Navigation** :
- `pwd` : où suis-je ?
- `ls` : que contient ce dossier ?
- `cd dossier` : entrer dans un dossier
- `cd ..` : remonter d'un niveau

**Manipulation** :
- `mkdir nom` : créer un dossier
- `touch fichier` : créer un fichier (Unix)
- `rm fichier` : supprimer un fichier

**Développement** :
- `code .` : ouvrir VS Code
- `npm install` : installer les dépendances
- `git status` : état du dépôt Git

### Les 3 règles d'or

1. 💻 **Gardez un terminal ouvert** pendant que vous codez
2. 📚 **Apprenez progressivement** les commandes
3. 🔄 **Pratiquez quotidiennement** pour que ça devienne naturel

---

## Pour aller plus loin

### Documentation officielle

**VS Code Terminal** :
- https://code.visualstudio.com/docs/terminal/basics

**Ligne de commande** :
- Windows : https://docs.microsoft.com/powershell
- macOS : https://support.apple.com/guide/terminal
- Linux : https://ubuntu.com/tutorials/command-line-for-beginners

### Ressources complémentaires

**Tutoriels interactifs** :
- Learn the Command Line (Codecademy)
- Command Line Crash Course

**Cheat sheets** :
- Recherchez "bash cheat sheet" ou "powershell cheat sheet"
- Imprimez-les et gardez-les à portée de main

---

## Navigation


**➡️ Section suivante :** [2.3 Organisation de projets](../03-organisation-de-projets/README.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Le terminal peut sembler intimidant au début, mais c'est un outil indispensable. Avec de la pratique, vous deviendrez un ninja de la ligne de commande !* 💻⚡

⏭️ [Organisation de projets](/02-environnement-de-developpement/03-organisation-de-projets/README.md)
