🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.1.1 Installation et configuration initiale de Visual Studio Code

## Introduction

**Visual Studio Code** (souvent abrégé **VS Code**) est l'éditeur de code le plus populaire au monde pour le développement web. Créé par Microsoft, il est **totalement gratuit**, **open source**, et disponible sur tous les systèmes d'exploitation.

Ne confondez pas VS Code avec "Visual Studio" (sans le "Code") qui est un environnement de développement beaucoup plus lourd et principalement destiné à d'autres types de développement. **VS Code est léger, rapide et parfait pour le web !**

### Pourquoi VS Code ?

Avant de l'installer, voici pourquoi des millions de développeurs l'utilisent :

- ✅ **Gratuit et open source** : accessible à tous, sans limitation
- ✅ **Léger et rapide** : se lance en quelques secondes
- ✅ **Multi-plateforme** : fonctionne sur Windows, macOS et Linux
- ✅ **Intelligent** : auto-complétion, détection d'erreurs, suggestions
- ✅ **Extensible** : des milliers d'extensions pour personnaliser
- ✅ **Terminal intégré** : plus besoin de jongler entre les fenêtres
- ✅ **Git intégré** : gestion de versions directement dans l'éditeur
- ✅ **Communauté énorme** : des millions d'utilisateurs, beaucoup de ressources

### Prérequis

Avant de commencer l'installation, assurez-vous d'avoir :
- Un ordinateur avec **Windows 7+**, **macOS 10.11+** ou **Linux**
- Au moins **200 Mo d'espace disque** disponible
- Une **connexion internet** pour télécharger l'installateur
- Les **droits d'administrateur** sur votre machine (pour l'installation)

---

## Étape 1 : Téléchargement de VS Code

### Accéder au site officiel

1. Ouvrez votre navigateur web (Chrome, Firefox, Edge, Safari...)
2. Rendez-vous sur le site officiel : **https://code.visualstudio.com**
3. Vous verrez un grand bouton de téléchargement

### Choisir la bonne version

Le site détecte automatiquement votre système d'exploitation et vous propose la bonne version. Vous verrez un bouton avec :
- **"Download for Windows"** si vous êtes sur Windows
- **"Download for Mac"** si vous êtes sur macOS
- **"Download for Linux"** si vous êtes sur Linux

**Cliquez sur ce bouton** pour télécharger l'installateur.

> **💡 Astuce :** Si vous souhaitez une version portable (qui ne nécessite pas d'installation), cliquez sur la petite flèche à côté du bouton de téléchargement et choisissez "Download .zip" (Windows) ou la version portable correspondante.

### Versions disponibles

VS Code propose plusieurs versions :
- **Stable** : la version recommandée, testée et fiable (c'est celle que nous utiliserons)
- **Insiders** : version de développement avec les dernières fonctionnalités (pour utilisateurs avancés)

**Pour débuter, téléchargez toujours la version Stable.**

---

## Étape 2 : Installation sur Windows

### Lancer l'installateur

1. Une fois le téléchargement terminé, ouvrez le fichier **VSCodeUserSetup-{version}.exe**
2. Windows peut afficher un avertissement de sécurité : cliquez sur **"Exécuter"**
3. Acceptez la licence d'utilisation (cochez "J'accepte l'accord" puis cliquez sur **"Suivant"**)

### Choisir le dossier d'installation

1. L'installateur propose un dossier par défaut (généralement `C:\Users\VotreNom\AppData\Local\Programs\Microsoft VS Code`)
2. **Gardez le dossier par défaut** sauf si vous avez une raison spécifique de le changer
3. Cliquez sur **"Suivant"**

### Options d'installation importantes

Vous verrez une fenêtre avec plusieurs cases à cocher. **Voici ce que nous recommandons pour débuter :**

✅ **Cochez ces options :**
- ☑️ **"Créer une icône sur le Bureau"** : pour lancer VS Code facilement
- ☑️ **"Ajouter à PATH"** : permet de lancer VS Code depuis le terminal (très utile !)
- ☑️ **"Ajouter l'action 'Ouvrir avec Code' au menu contextuel des fichiers"** : clic-droit sur un fichier pour l'ouvrir dans VS Code
- ☑️ **"Ajouter l'action 'Ouvrir avec Code' au menu contextuel des dossiers"** : clic-droit sur un dossier pour l'ouvrir dans VS Code
- ☑️ **"Enregistrer Code en tant qu'éditeur pris en charge pour les types de fichiers"** : VS Code sera proposé pour ouvrir les fichiers de code

Ces options vous faciliteront grandement la vie au quotidien !

### Finaliser l'installation

1. Cliquez sur **"Suivant"**
2. Vérifiez le résumé des options
3. Cliquez sur **"Installer"**
4. L'installation prend généralement moins d'une minute
5. Une fois terminé, **cochez "Lancer Visual Studio Code"**
6. Cliquez sur **"Terminer"**

VS Code se lance pour la première fois ! 🎉

---

## Étape 2 : Installation sur macOS

### Lancer l'installateur

1. Une fois le téléchargement terminé, ouvrez le fichier **VSCode-darwin-universal.zip**
2. Le fichier se décompresse automatiquement, créant une application **Visual Studio Code.app**
3. **Glissez-déposez** cette application dans votre dossier **Applications**

> **💡 Astuce :** Vous pouvez aussi laisser l'application dans le dossier Téléchargements, mais il est préférable de la ranger dans Applications pour une meilleure organisation.

### Premier lancement

1. Ouvrez le dossier **Applications** (⌘ + Shift + A depuis le Finder)
2. Double-cliquez sur **Visual Studio Code**
3. macOS peut afficher un message : "Visual Studio Code ne peut pas être ouvert car il provient d'un développeur non identifié"

**Si ce message apparaît :**
1. Ouvrez **Préférences Système** → **Sécurité et confidentialité**
2. En bas de la fenêtre, vous verrez un message concernant VS Code
3. Cliquez sur **"Ouvrir quand même"**
4. Confirmez en cliquant sur **"Ouvrir"**

### Ajouter VS Code au Dock

Pour un accès rapide :
1. Faites un clic-droit sur l'icône VS Code dans le Dock
2. Choisissez **Options** → **Garder dans le Dock**

### Installer la commande "code" dans le terminal (optionnel mais recommandé)

Pour pouvoir lancer VS Code depuis le terminal :
1. Ouvrez VS Code
2. Appuyez sur **⌘ + Shift + P** pour ouvrir la palette de commandes
3. Tapez "shell command"
4. Sélectionnez **"Shell Command: Install 'code' command in PATH"**
5. Un message de confirmation apparaît

Vous pourrez maintenant taper `code .` dans le terminal pour ouvrir le dossier courant dans VS Code !

---

## Étape 2 : Installation sur Linux

L'installation sur Linux varie selon votre distribution. Voici les méthodes pour les distributions les plus courantes.

### Ubuntu / Debian

**Méthode 1 : Avec le fichier .deb (recommandé)**

1. Téléchargez le fichier **.deb** depuis le site de VS Code
2. Ouvrez un terminal dans le dossier de téléchargement
3. Installez avec la commande :
```bash
sudo apt install ./code_*.deb
```
4. Entrez votre mot de passe administrateur
5. L'installation démarre automatiquement

**Méthode 2 : Via le dépôt officiel**

```bash
# Installer les dépendances
sudo apt-get install wget gpg

# Ajouter la clé GPG de Microsoft
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg

# Ajouter le dépôt
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'

# Installer VS Code
sudo apt update
sudo apt install code
```

### Fedora / Red Hat / CentOS

1. Téléchargez le fichier **.rpm**
2. Installez avec :
```bash
sudo rpm -i code-*.rpm
```

Ou via dnf :
```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update
sudo dnf install code
```

### Arch Linux / Manjaro

VS Code est disponible dans l'AUR :
```bash
yay -S visual-studio-code-bin
```

Ou avec pacman pour la version open source :
```bash
sudo pacman -S code
```

### Lancer VS Code sur Linux

Une fois installé, lancez VS Code :
- Depuis le menu des applications (cherchez "Visual Studio Code")
- Depuis le terminal : tapez simplement `code`
- Pour ouvrir un dossier spécifique : `code /chemin/vers/dossier`

---

## Étape 3 : Premier lancement et découverte

### Écran d'accueil

Au premier lancement de VS Code, vous verrez un **écran d'accueil** (Welcome page) avec plusieurs sections :

- **Start** : actions rapides pour commencer
- **Recent** : vos projets récents (vide pour l'instant)
- **Help** : liens vers la documentation et tutoriels
- **Customize** : options de personnalisation

**Ne vous inquiétez pas si cela semble vide ou intimidant**, c'est normal ! Nous allons tout configurer ensemble.

### Choisir la langue de l'interface

Par défaut, VS Code est en anglais. Pour le mettre en français :

1. Appuyez sur **Ctrl + Shift + X** (Windows/Linux) ou **⌘ + Shift + X** (macOS) pour ouvrir les extensions
2. Dans la barre de recherche, tapez : **French Language Pack**
3. Cliquez sur le premier résultat "French Language Pack for Visual Studio Code"
4. Cliquez sur le bouton bleu **"Install"** (Installer)
5. Une fois installé, un message apparaît en bas à droite
6. Cliquez sur **"Restart"** (Redémarrer) pour appliquer les changements

VS Code redémarre et l'interface est maintenant en français ! 🇫🇷

> **💡 Note :** Dans cette formation, nous utiliserons les termes français, mais vous verrez souvent les termes anglais dans la documentation en ligne. Nous indiquerons les deux quand nécessaire.

---

## Étape 4 : Configuration initiale de base

### Accéder aux paramètres

Les paramètres de VS Code se trouvent dans :
- **Windows/Linux** : Fichier → Préférences → Paramètres (ou **Ctrl + ,**)
- **macOS** : Code → Préférences → Paramètres (ou **⌘ + ,**)

Vous pouvez aussi ouvrir les paramètres avec la palette de commandes (**Ctrl/⌘ + Shift + P**) puis taper "settings".

### Interface des paramètres

Vous verrez deux onglets :
- **Interface utilisateur** : interface graphique avec cases à cocher et menus déroulants (recommandé pour débuter)
- **JSON** : fichier de configuration avancé (pour utilisateurs expérimentés)

**Utilisez l'interface utilisateur** pour l'instant, c'est beaucoup plus simple !

### Paramètres recommandés pour débuter

Voici les paramètres que nous vous conseillons de configurer dès maintenant. Dans la barre de recherche des paramètres, tapez le nom du paramètre et modifiez sa valeur :

#### 1. Taille de la police (Font Size)
- **Paramètre** : `Editor: Font Size`
- **Valeur recommandée** : `14` (ou `16` si vous avez un grand écran)
- **Pourquoi** : une police lisible évite la fatigue visuelle

#### 2. Famille de police (Font Family)
- **Paramètre** : `Editor: Font Family`
- **Valeur recommandée** : gardez la valeur par défaut ou utilisez `'Fira Code', 'Consolas', monospace`
- **Pourquoi** : les polices monospace (à chasse fixe) sont plus lisibles pour le code

#### 3. Activer les ligatures (Font Ligatures) - optionnel
- **Paramètre** : `Editor: Font Ligatures`
- **Valeur** : cochez la case (si vous utilisez Fira Code)
- **Pourquoi** : rend certains symboles de code plus élégants (=>, ===, !=)

#### 4. Sauvegarde automatique (Auto Save)
- **Paramètre** : `Files: Auto Save`
- **Valeur recommandée** : `afterDelay` (sauvegarde après un délai)
- **Pourquoi** : évite de perdre votre travail si vous oubliez de sauvegarder

#### 5. Délai de sauvegarde automatique (Auto Save Delay)
- **Paramètre** : `Files: Auto Save Delay`
- **Valeur recommandée** : `1000` (1 seconde)
- **Pourquoi** : sauvegarde rapidement sans être trop agressif

#### 6. Formatage à la sauvegarde (Format On Save)
- **Paramètre** : `Editor: Format On Save`
- **Valeur** : cochez la case
- **Pourquoi** : votre code sera toujours propre et bien indenté automatiquement

#### 7. Taille de la tabulation (Tab Size)
- **Paramètre** : `Editor: Tab Size`
- **Valeur recommandée** : `2` (pour HTML/CSS/JS moderne)
- **Pourquoi** : convention standard dans le développement web moderne

#### 8. Insertion d'espaces (Insert Spaces)
- **Paramètre** : `Editor: Insert Spaces`
- **Valeur** : cochez la case
- **Pourquoi** : utilise des espaces au lieu de tabulations (standard web)

#### 9. Minimap (petite carte du code)
- **Paramètre** : `Editor: Minimap Enabled`
- **Valeur** : décochez la case si vous débutez
- **Pourquoi** : la minimap peut être distrayante au début, vous pourrez la réactiver plus tard

#### 10. Numéros de ligne (Line Numbers)
- **Paramètre** : `Editor: Line Numbers`
- **Valeur** : `on`
- **Pourquoi** : essentiel pour se repérer dans le code et les messages d'erreur

#### 11. Largeur de rendu (Render Whitespace)
- **Paramètre** : `Editor: Render Whitespace`
- **Valeur recommandée** : `selection` ou `boundary`
- **Pourquoi** : visualise les espaces et tabulations pour mieux comprendre l'indentation

#### 12. Zoom (Window: Zoom Level)
- **Paramètre** : `Window: Zoom Level`
- **Valeur** : `0` (par défaut) ou ajustez selon votre confort
- **Pourquoi** : adaptez la taille globale de l'interface à votre écran

#### 13. Thème de couleur (Color Theme)
- **Paramètre** : Apparence → Thème de couleur
- **Valeur recommandée** :
  - `Dark+ (default dark)` : thème sombre, reposant pour les yeux
  - `Light+ (default light)` : thème clair si vous préférez
- **Pourquoi** : le confort visuel est important pour coder des heures

### Récapitulatif rapide des paramètres

Voici un tableau récapitulatif pour les retrouver facilement :

| Paramètre | Valeur recommandée | Importance |
|-----------|-------------------|------------|
| Font Size | 14-16 | ⭐⭐⭐ |
| Auto Save | afterDelay | ⭐⭐⭐ |
| Format On Save | Activé | ⭐⭐⭐ |
| Tab Size | 2 | ⭐⭐⭐ |
| Insert Spaces | Activé | ⭐⭐⭐ |
| Line Numbers | on | ⭐⭐⭐ |
| Minimap | Désactivé (au début) | ⭐⭐ |
| Color Theme | Dark+ ou Light+ | ⭐⭐ |

---

## Étape 5 : Vérifier l'installation

### Créer un dossier de test

Pour vérifier que tout fonctionne correctement, créons un petit projet de test :

1. Créez un dossier sur votre ordinateur, par exemple : `C:\Users\VotreNom\Documents\test-vscode` (Windows) ou `~/Documents/test-vscode` (macOS/Linux)

### Ouvrir le dossier dans VS Code

**Méthode 1 : Depuis VS Code**
1. Dans VS Code, allez dans **Fichier → Ouvrir le dossier** (File → Open Folder)
2. Naviguez jusqu'à votre dossier `test-vscode`
3. Cliquez sur **Sélectionner un dossier**

**Méthode 2 : Clic-droit (si vous avez coché l'option à l'installation)**
1. Faites un clic-droit sur le dossier `test-vscode`
2. Choisissez **"Ouvrir avec Code"**

**Méthode 3 : Terminal (si vous avez installé la commande)**
1. Ouvrez un terminal
2. Naviguez jusqu'au dossier : `cd ~/Documents/test-vscode`
3. Tapez : `code .`

### Créer un fichier de test

1. Dans VS Code, dans l'explorateur de fichiers (barre latérale gauche), cliquez sur l'icône **"Nouveau fichier"** (feuille avec un +)
2. Nommez le fichier : `test.html`
3. Appuyez sur **Entrée**
4. Le fichier s'ouvre dans l'éditeur

### Écrire du code de test

Tapez le code suivant dans votre fichier `test.html` :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Test VS Code</title>
</head>
<body>
    <h1>Bonjour VS Code !</h1>
    <p>Si vous voyez ceci, tout fonctionne parfaitement !</p>
</body>
</html>
```

### Vérifier les fonctionnalités

**1. Coloration syntaxique**
- Le code doit être coloré : les balises HTML en couleur, les attributs différents, etc.
- ✅ Si c'est le cas, la coloration fonctionne !

**2. Auto-complétion**
- Commencez à taper `<di` et vous devriez voir apparaître des suggestions (`<div>`, etc.)
- ✅ Si des suggestions apparaissent, l'auto-complétion fonctionne !

**3. Fermeture automatique des balises**
- Tapez `<div>` et VS Code devrait automatiquement ajouter `</div>`
- ✅ Si c'est le cas, l'aide à la saisie fonctionne !

**4. Sauvegarde automatique**
- Attendez 1-2 secondes après avoir modifié le fichier
- Le point blanc à côté du nom du fichier (indiquant les modifications non sauvegardées) devrait disparaître
- ✅ Si le fichier se sauvegarde tout seul, l'auto-save fonctionne !

**5. Formatage**
- Désindentez volontairement une ligne (supprimez les espaces devant)
- Sauvegardez avec **Ctrl + S** (Windows/Linux) ou **⌘ + S** (macOS)
- La ligne devrait se réindenter automatiquement
- ✅ Si l'indentation se corrige, le formatage automatique fonctionne !

### Ouvrir le fichier dans le navigateur

Pour voir le résultat dans un navigateur :
1. Faites un clic-droit sur le fichier `test.html` dans l'explorateur de VS Code
2. Choisissez **"Révéler dans l'Explorateur de fichiers"** (Windows) ou **"Reveal in Finder"** (macOS)
3. Double-cliquez sur le fichier pour l'ouvrir dans votre navigateur par défaut

Vous devriez voir votre page HTML s'afficher ! 🎉

---

## Étape 6 : Configurer le terminal intégré (optionnel)

VS Code dispose d'un terminal intégré très pratique. Vérifions qu'il fonctionne :

### Ouvrir le terminal

- **Raccourci** : **Ctrl + ù** (Windows/Linux) ou **Ctrl + `** (macOS)
- **Ou** : Menu **Terminal → Nouveau terminal**

Un panneau s'ouvre en bas de VS Code avec un terminal.

### Sous Windows : choisir PowerShell ou CMD

Par défaut, Windows peut utiliser PowerShell ou l'ancien CMD. PowerShell est recommandé.

Pour changer le terminal par défaut :
1. Dans le terminal, cliquez sur la petite flèche vers le bas à côté du **+**
2. Choisissez **"Sélectionner le shell par défaut"**
3. Choisissez **"PowerShell"** ou **"Command Prompt"** selon votre préférence

### Tester le terminal

Tapez une commande simple pour vérifier que tout fonctionne :

**Windows :**
```powershell
dir
```

**macOS / Linux :**
```bash
ls
```

Vous devriez voir la liste des fichiers de votre dossier `test-vscode`.

---

## Dépannage : problèmes courants

### VS Code ne se lance pas

**Sur Windows :**
- Vérifiez que vous avez les droits d'administrateur
- Essayez de désactiver temporairement votre antivirus
- Réinstallez VS Code en tant qu'administrateur

**Sur macOS :**
- Vérifiez les permissions dans Sécurité et confidentialité
- Essayez de déplacer l'application hors du dossier Applications puis de la remettre

**Sur Linux :**
- Vérifiez les dépendances : `sudo apt install libgtk-3-0 libxss1 libasound2`
- Vérifiez les permissions : `chmod +x /usr/bin/code`

### L'auto-complétion ne fonctionne pas

- Vérifiez que vous avez bien ouvert un **dossier** et pas juste un fichier
- Fermez et rouvrez VS Code
- Vérifiez que le paramètre `Editor: Quick Suggestions` est activé

### Le formatage automatique ne fonctionne pas

- Vérifiez que `Format On Save` est bien coché
- Installez un formateur pour votre langage (nous verrons ça dans la section suivante sur les extensions)
- Essayez de formater manuellement avec **Shift + Alt + F** (Windows/Linux) ou **Shift + Option + F** (macOS)

### Le terminal ne s'ouvre pas

- Essayez de changer le shell par défaut (voir section Terminal ci-dessus)
- Fermez et rouvrez VS Code
- Vérifiez que votre système a bien un shell installé

### VS Code est en anglais malgré l'installation du pack français

- Ouvrez la palette de commandes (**Ctrl/⌘ + Shift + P**)
- Tapez "Configure Display Language"
- Choisissez "fr" (français)
- Redémarrez VS Code

---

## Récapitulatif de la configuration

Félicitations ! 🎉 Vous avez maintenant :

- ✅ **Installé Visual Studio Code** sur votre système
- ✅ **Configuré l'interface en français** (optionnel)
- ✅ **Ajusté les paramètres de base** pour un confort optimal
- ✅ **Créé et testé votre premier fichier** dans VS Code
- ✅ **Vérifié que les fonctionnalités essentielles** fonctionnent correctement
- ✅ **Configuré le terminal intégré** pour les commandes

### Ce que vous savez faire maintenant

- Lancer VS Code de différentes manières
- Ouvrir un dossier de projet
- Créer et éditer des fichiers
- Accéder aux paramètres et les modifier
- Utiliser le terminal intégré
- Ouvrir vos fichiers HTML dans un navigateur

### Prochaines étapes

Dans les sections suivantes, nous allons :
- **Découvrir l'interface complète** de VS Code en détail
- **Installer des extensions essentielles** pour le développement web
- **Apprendre les raccourcis clavier** pour gagner en productivité
- **Maîtriser les fonctionnalités avancées** comme le multicurseur et les snippets

---

## Conseils pour bien débuter

### 1. Prenez le temps de vous familiariser

Ne vous précipitez pas ! Passez quelques minutes chaque jour à explorer l'interface, tester des fonctionnalités. VS Code est riche et vous découvrirez constamment de nouvelles choses.

### 2. Personnalisez selon vos goûts

Les paramètres que nous avons configurés sont des recommandations. N'hésitez pas à les ajuster selon vos préférences :
- Changez le thème de couleurs
- Ajustez la taille de la police
- Testez différentes configurations

### 3. Ne sur-customisez pas au début

Il peut être tentant d'installer des dizaines d'extensions et de modifier tous les paramètres. **Résistez à cette tentation !** Maîtrisez d'abord les bases, vous personnaliserez progressivement au fil de vos besoins.

### 4. Utilisez VS Code tous les jours

Même pour de petites modifications, ouvrez VS Code plutôt que le Bloc-notes. C'est en l'utilisant régulièrement que vous développerez vos automatismes.

### 5. Explorez la documentation

VS Code a une excellente documentation en ligne. La page d'accueil propose des liens vers des tutoriels interactifs.

---

## Ressources complémentaires

### Documentation officielle
- **Site officiel** : https://code.visualstudio.com
- **Documentation** : https://code.visualstudio.com/docs
- **Tutoriels interactifs** : disponibles dans la page d'accueil de VS Code

### Communauté
- **Forum officiel** : https://github.com/microsoft/vscode/discussions
- **Stack Overflow** : tag `visual-studio-code`
- **Reddit** : r/vscode

### Astuces et tutoriels vidéo
- Cherchez "Visual Studio Code tutoriel français" sur YouTube
- La chaîne officielle "Visual Studio Code" propose des vidéos (en anglais)

---

## Navigation


**➡️ Section suivante :** [2.1.2 Découverte de l'interface](./02-decouverte-de-linterface.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Vous avez posé les fondations de votre environnement de développement ! La prochaine étape est de découvrir en détail l'interface de VS Code pour devenir plus efficace.*

⏭️ [Découverte de l'interface](/02-environnement-de-developpement/01-visual-studio-code/02-decouverte-de-linterface.md)
