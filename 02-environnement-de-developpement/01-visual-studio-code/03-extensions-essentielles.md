🔝 Retour au [Sommaire](/SOMMAIRE.md)

# 2.1.3 Extensions essentielles pour le développement web

## Introduction

VS Code est puissant dès son installation, mais les **extensions** le transforment en un outil sur-mesure pour vos besoins. Imaginez les extensions comme des **applications** que vous installez sur votre smartphone : elles ajoutent de nouvelles fonctionnalités à VS Code.

### Qu'est-ce qu'une extension ?

Une extension est un **petit programme** développé par la communauté ou par Microsoft qui ajoute des fonctionnalités à VS Code :
- 🎨 Support de nouveaux langages de programmation
- ✨ Amélioration de l'auto-complétion
- 🔍 Détection d'erreurs plus précise
- 🎭 Nouveaux thèmes visuels
- 🚀 Outils de productivité
- 🤝 Fonctionnalités de collaboration

### Pourquoi utiliser des extensions ?

**Sans extensions** : VS Code est un bon éditeur de texte avec coloration syntaxique basique.

**Avec extensions** : VS Code devient un **environnement de développement complet** qui :
- Détecte vos erreurs avant même de tester votre code
- Formate automatiquement votre code pour qu'il soit propre
- Affiche une prévisualisation en direct de votre page web
- Vous aide à écrire du code plus rapidement
- Vous fait gagner des heures de travail

### ⚠️ Attention : ne pas en abuser !

**Piège du débutant** : installer des dizaines d'extensions "au cas où".

**Problème** :
- VS Code devient lent au démarrage
- Conflits entre extensions
- Interface surchargée et confuse
- Difficulté à identifier ce qui fait quoi

**Notre recommandation** : commencez avec **5-10 extensions essentielles**, puis ajoutez-en progressivement selon vos besoins réels.

---

## Comment installer une extension

### Méthode 1 : Via la barre d'activité (recommandée)

1. Cliquez sur l'icône **Extensions** dans la barre d'activité (icône avec 4 carrés) ou appuyez sur `Ctrl + Shift + X` (Windows/Linux) ou `⌘ + Shift + X` (macOS)

2. Dans la barre de recherche en haut, tapez le nom de l'extension

3. Cliquez sur l'extension dans les résultats

4. Cliquez sur le bouton bleu **"Installer"** (Install)

5. Une fois installée, certaines extensions nécessitent de **recharger VS Code** (un bouton "Recharger" apparaîtra)

### Méthode 2 : Via la palette de commandes

1. Ouvrez la palette : `Ctrl + Shift + P` (Windows/Linux) ou `⌘ + Shift + P` (macOS)

2. Tapez : `Extensions: Install Extensions`

3. Appuyez sur `Entrée`

4. Cherchez et installez l'extension

### Méthode 3 : Via le marketplace en ligne

1. Rendez-vous sur https://marketplace.visualstudio.com/vscode

2. Cherchez l'extension

3. Cliquez sur **"Install"** : cela ouvrira VS Code et lancera l'installation

### Informations sur une extension

Avant d'installer une extension, cliquez dessus pour voir :
- **Description** : ce qu'elle fait
- **Note** : ⭐⭐⭐⭐⭐ (sur 5 étoiles)
- **Nombre de téléchargements** : indicateur de popularité
- **Version** : numéro de version
- **Éditeur** : qui l'a créée
- **Dernière mise à jour** : si elle est maintenue
- **README** : documentation complète

💡 **Conseil** : privilégiez les extensions avec :
- ✅ Plus d'un million de téléchargements
- ✅ Note supérieure à 4 étoiles
- ✅ Mise à jour récente (moins de 6 mois)

---

## Extensions essentielles pour le développement web

Voici la liste des extensions **indispensables** pour bien débuter. Nous les classons par catégorie.

### 🌐 Catégorie : Prévisualisation et serveur local

#### **Live Server** ⭐⭐⭐⭐⭐ (Essentiel)

**Éditeur** : Ritwick Dey
**Téléchargements** : 40+ millions

**Qu'est-ce que c'est ?**
Live Server lance un serveur web local et rafraîchit automatiquement votre navigateur à chaque modification de fichier.

**Pourquoi c'est indispensable ?**
Sans Live Server :
- Vous devez sauvegarder le fichier
- Puis aller dans votre navigateur
- Puis cliquer sur "Actualiser"
- À chaque petite modification !

Avec Live Server :
- Vous sauvegardez (ou l'auto-save le fait)
- La page se rafraîchit automatiquement
- Vous voyez le résultat instantanément

**Comment l'utiliser ?**
1. Installez l'extension
2. Ouvrez un fichier HTML
3. Faites un clic-droit dans l'éditeur
4. Choisissez **"Open with Live Server"**
5. Votre navigateur s'ouvre automatiquement sur `http://127.0.0.1:5500`

**Icône** : Un petit **"Go Live"** apparaît en bas à droite dans la barre d'état

**Paramètres utiles** :
- `Live Server: Custom Browser` : choisir le navigateur par défaut
- `Live Server: Port` : changer le port (5500 par défaut)

---

### ✨ Catégorie : Formatage et qualité du code

#### **Prettier - Code formatter** ⭐⭐⭐⭐⭐ (Essentiel)

**Éditeur** : Prettier
**Téléchargements** : 35+ millions

**Qu'est-ce que c'est ?**
Prettier formate automatiquement votre code pour qu'il soit propre, cohérent et lisible.

**Pourquoi c'est indispensable ?**
- Indentation automatique parfaite
- Respect des conventions de style
- Code professionnel sans effort
- Gain de temps énorme

**Avant Prettier** :
```html
<div><h1>Titre</h1><p>Texte mal indenté</p></div>
```

**Après Prettier** :
```html
<div>
  <h1>Titre</h1>
  <p>Texte mal indenté</p>
</div>
```

**Comment l'utiliser ?**
1. Installez l'extension
2. Activez le formatage automatique à la sauvegarde :
   - Paramètres (`Ctrl + ,`)
   - Cherchez "Format On Save"
   - Cochez la case
3. Définissez Prettier comme formateur par défaut :
   - Paramètres
   - Cherchez "Default Formatter"
   - Choisissez "Prettier - Code formatter"

**Formater manuellement** :
- **Raccourci** : `Shift + Alt + F` (Windows/Linux) ou `Shift + Option + F` (macOS)
- **Palette** : "Format Document"

**Langages supportés** :
- HTML
- CSS / SCSS / Less
- JavaScript / TypeScript
- JSON
- Markdown
- Et bien d'autres !

**Paramètres recommandés** :
```json
"prettier.semi": true,
"prettier.singleQuote": true,
"prettier.tabWidth": 2,
"prettier.trailingComma": "es5"
```

---

#### **ESLint** ⭐⭐⭐⭐⭐ (Très important)

**Éditeur** : Microsoft
**Téléchargements** : 25+ millions

**Qu'est-ce que c'est ?**
ESLint analyse votre code JavaScript et détecte les erreurs, les mauvaises pratiques et les problèmes potentiels.

**Pourquoi c'est très important ?**
- Détecte les bugs **avant** l'exécution
- Apprend les bonnes pratiques JavaScript
- Suggère des améliorations
- Évite les erreurs classiques

**Exemples de détection** :
```javascript
// ❌ ESLint détecte :
let x = 10;  // Variable déclarée mais jamais utilisée

// ❌ ESLint détecte :
if (x = 10) { }  // Utilisation de = au lieu de ==

// ❌ ESLint détecte :
const user = { name: "Jean" };
console.log(user.age);  // Propriété inexistante
```

**Installation et configuration** :
1. Installez l'extension ESLint
2. Dans votre projet, installez ESLint via npm (nous verrons ça plus tard)
3. Créez un fichier `.eslintrc.json` de configuration

**Pour débuter**, vous pouvez l'installer maintenant mais la configurer plus tard quand vous travaillerez avec npm.

**Affichage des erreurs** :
- Soulignement ondulé rouge dans le code
- Messages dans le panneau "Problèmes"
- Suggestions de corrections

---

### 🏷️ Catégorie : Aide à la saisie HTML

#### **Auto Rename Tag** ⭐⭐⭐⭐⭐ (Très utile)

**Éditeur** : Jun Han
**Téléchargements** : 15+ millions

**Qu'est-ce que c'est ?**
Renomme automatiquement la balise de fermeture quand vous renommez la balise d'ouverture (et vice-versa).

**Exemple** :
```html
<!-- Vous modifiez <div> en <section> -->
<div>
  <h1>Titre</h1>
</div>

<!-- Auto Rename Tag met à jour automatiquement : -->
<section>
  <h1>Titre</h1>
</section>
```

**Pourquoi c'est très utile ?**
- Évite les erreurs de balises mal fermées
- Gain de temps énorme
- Moins de frustration

**Configuration** : Aucune nécessaire, fonctionne immédiatement après installation.

---

#### **Auto Close Tag** ⭐⭐⭐⭐ (Utile)

**Éditeur** : Jun Han
**Téléchargements** : 10+ millions

**Qu'est-ce que c'est ?**
Ferme automatiquement les balises HTML et XML.

**Exemple** :
```html
<!-- Vous tapez : -->
<div>

<!-- Auto Close Tag ajoute automatiquement : -->
<div></div>
```

**Note** : VS Code a maintenant cette fonctionnalité intégrée pour HTML, mais l'extension fonctionne aussi pour JSX (React) et autres langages.

**Verdict** : Optionnel si vous travaillez uniquement en HTML, utile pour React.

---

#### **HTML CSS Support** ⭐⭐⭐⭐ (Recommandé)

**Éditeur** : ecmel
**Téléchargements** : 8+ millions

**Qu'est-ce que c'est ?**
Améliore l'auto-complétion pour les classes CSS et les IDs dans les fichiers HTML.

**Exemple** :
```html
<!-- Dans votre CSS : -->
.ma-classe-speciale { color: red; }

<!-- Dans votre HTML : quand vous tapez class=" -->
<div class="ma-">
<!-- L'extension suggère : ma-classe-speciale -->
```

**Pourquoi c'est recommandé ?**
- Évite les fautes de frappe dans les noms de classes
- Vous rappelle les classes existantes
- Gain de temps

**Configuration** : Fonctionne automatiquement si vos fichiers CSS sont dans le projet.

---

### 🎨 Catégorie : Aide CSS

#### **IntelliSense for CSS class names in HTML** ⭐⭐⭐⭐ (Recommandé)

**Éditeur** : Zignd
**Téléchargements** : 6+ millions

**Qu'est-ce que c'est ?**
Auto-complétion intelligente des noms de classes CSS définies dans votre projet.

**Avantage** : Complète "HTML CSS Support" en étant encore plus intelligent pour trouver les classes dans tout le projet, même dans des fichiers externes.

**Configuration** :
```json
"css.enabledLanguages": ["html"]
```

---

### 📁 Catégorie : Navigation et fichiers

#### **Path Intellisense** ⭐⭐⭐⭐ (Très utile)

**Éditeur** : Christian Kohler
**Téléchargements** : 10+ millions

**Qu'est-ce que c'est ?**
Auto-complétion pour les chemins de fichiers.

**Exemple** :
```html
<!-- Quand vous tapez : -->
<img src="./images/">

<!-- L'extension suggère automatiquement les fichiers : -->
<img src="./images/logo.png">
```

**Pourquoi c'est très utile ?**
- Plus d'erreurs de chemin (erreur très fréquente !)
- Gain de temps
- Découverte des fichiers disponibles

**Fonctionne dans** : HTML, CSS, JavaScript, et presque tous les fichiers.

---

#### **Material Icon Theme** ⭐⭐⭐⭐ (Confort visuel)

**Éditeur** : Philipp Kief
**Téléchargements** : 15+ millions

**Qu'est-ce que c'est ?**
Change les icônes des fichiers dans l'explorateur pour les rendre plus jolies et reconnaissables.

**Avant** : Icônes génériques 📄

**Après** : Icônes colorées et spécifiques
- 🌐 HTML en orange
- 🎨 CSS en bleu
- ⚡ JavaScript en jaune
- 📁 Dossiers en couleurs
- 🖼️ Images avec aperçu
- Et bien d'autres !

**Pourquoi c'est utile ?**
- Reconnaissance visuelle immédiate du type de fichier
- Interface plus agréable
- Navigation plus rapide

**Alternatives** :
- **VSCode Icons** (vscode-icons)
- **Atom One Dark Theme** (icons inclus)

**Installation** :
1. Installez l'extension
2. Palette de commandes : "File Icon Theme"
3. Choisissez "Material Icon Theme"

---

### 🐛 Catégorie : Debugging et erreurs

#### **Error Lens** ⭐⭐⭐⭐ (Très pratique)

**Éditeur** : Alexander
**Téléchargements** : 5+ millions

**Qu'est-ce que c'est ?**
Affiche les erreurs et avertissements **directement dans le code**, à côté de la ligne concernée.

**Sans Error Lens** :
```javascript
const x = 10;
// Vous devez regarder le panneau "Problèmes" en bas pour voir l'erreur
```

**Avec Error Lens** :
```javascript
const x = 10; // ❌ 'x' is assigned a value but never used
```

**Pourquoi c'est très pratique ?**
- Erreurs visibles immédiatement
- Pas besoin de chercher dans le panneau "Problèmes"
- Correction plus rapide

**Configuration** :
```json
"errorLens.enabledDiagnosticLevels": ["error", "warning"],
"errorLens.fontSize": "12"
```

**Note** : Peut être visuellement chargé au début, vous pouvez le désactiver temporairement si besoin.

---

### 🎨 Catégorie : Thèmes et apparence

#### **One Dark Pro** ⭐⭐⭐⭐ (Thème populaire)

**Éditeur** : binaryify
**Téléchargements** : 10+ millions

**Qu'est-ce que c'est ?**
Un thème sombre élégant inspiré d'Atom.

**Alternatives populaires** :
- **Dracula Official** : thème sombre violet
- **Night Owl** : thème sombre conçu pour réduire la fatigue oculaire
- **GitHub Theme** : thème clair et sombre comme GitHub
- **Material Theme** : thème avec variantes multiples

**Installation** :
1. Installez le thème de votre choix
2. Palette de commandes : "Preferences: Color Theme"
3. Choisissez votre thème

💡 **Conseil** : Testez plusieurs thèmes et gardez celui où vous vous sentez le mieux. Le confort visuel est important !

---

### 🤝 Catégorie : Collaboration (optionnel pour débuter)

#### **Live Share** ⭐⭐⭐⭐ (Pour travailler à plusieurs)

**Éditeur** : Microsoft
**Téléchargements** : 10+ millions

**Qu'est-ce que c'est ?**
Permet de coder à plusieurs en temps réel sur le même projet, comme Google Docs pour le code.

**Fonctionnalités** :
- Partage de session de codage
- Plusieurs curseurs simultanés
- Chat intégré
- Partage de terminal
- Partage de serveur local

**Quand l'utiliser ?**
- Pair programming (coder à deux)
- Entraide à distance
- Code review en temps réel
- Enseignement / mentorat

**Installation** : Installez le pack **"Live Share Extension Pack"** qui contient Live Share et ses outils.

**Verdict** : Pas indispensable pour débuter seul, mais excellent pour apprendre avec quelqu'un.

---

### 🎯 Catégorie : Git (optionnel pour débuter)

#### **GitLens** ⭐⭐⭐⭐⭐ (Pour Git avancé)

**Éditeur** : GitKraken
**Téléchargements** : 25+ millions

**Qu'est-ce que c'est ?**
Suralimente les capacités Git de VS Code avec des visualisations et informations détaillées.

**Fonctionnalités** :
- Voir qui a modifié chaque ligne (blame annotations)
- Historique des modifications
- Comparaison de versions
- Graphique de branches
- Navigation dans l'historique Git

**Verdict** : Très puissant mais **optionnel pour débuter**. Installez-le plus tard quand vous maîtriserez Git.

---

## Notre sélection : starter pack débutant

### Les 5 extensions à installer ABSOLUMENT

Si vous ne deviez installer que 5 extensions pour commencer :

1. ✅ **Live Server** : prévisualisation en direct
2. ✅ **Prettier** : formatage automatique
3. ✅ **Auto Rename Tag** : renommage de balises
4. ✅ **Path Intellisense** : auto-complétion des chemins
5. ✅ **Material Icon Theme** : meilleure visualisation

### Extensions supplémentaires recommandées (5 de plus)

Quand vous êtes à l'aise avec les 5 premières :

6. ✅ **ESLint** : analyse JavaScript
7. ✅ **HTML CSS Support** : auto-complétion CSS
8. ✅ **Error Lens** : erreurs visibles
9. ✅ **IntelliSense for CSS class names** : aide CSS avancée
10. ✅ **Un thème qui vous plaît** : confort visuel

### Extensions à installer plus tard

Quand vous progresserez :

- **Live Share** : collaboration en temps réel
- **GitLens** : Git avancé
- **REST Client** : tester des APIs
- **Debugger for Chrome** : déboguer JavaScript dans Chrome
- Extensions spécifiques à des frameworks (React, Vue, etc.)

---

## Gérer vos extensions

### Voir les extensions installées

1. Cliquez sur l'icône Extensions (`Ctrl + Shift + X`)
2. Dans la barre de recherche, cliquez sur les **trois points** (•••)
3. Choisissez **"Afficher les extensions installées"**

Ou tapez directement : `@installed` dans la barre de recherche

### Désactiver une extension

**Désactiver temporairement** (sans désinstaller) :
1. Ouvrez la vue Extensions
2. Cherchez l'extension à désactiver
3. Cliquez sur la roue dentée ⚙️ à côté de "Désinstaller"
4. Choisissez **"Désactiver"**

**Pourquoi désactiver ?**
- Extension qui ralentit VS Code
- Extension en conflit avec une autre
- Extension utile seulement dans certains projets

**Réactiver** : même procédure, cliquez sur "Activer"

### Désactiver pour un espace de travail uniquement

Vous pouvez désactiver une extension **seulement pour un projet spécifique** :
1. Roue dentée ⚙️ de l'extension
2. **"Désactiver (Espace de travail)"**

**Exemple d'utilisation** :
- ESLint activé pour les projets JavaScript
- ESLint désactivé pour les projets HTML/CSS purs

### Désinstaller une extension

1. Vue Extensions
2. Cherchez l'extension
3. Cliquez sur **"Désinstaller"**
4. Rechargez VS Code si demandé

### Mettre à jour les extensions

VS Code met à jour les extensions automatiquement par défaut.

**Mettre à jour manuellement** :
1. Vue Extensions
2. Cliquez sur **"Mises à jour disponibles"**
3. Cliquez sur le bouton **"Mettre à jour"** à côté de l'extension

Ou : cliquez sur **"Tout mettre à jour"** dans les trois points (•••)

### Synchroniser les extensions entre plusieurs machines

Si vous utilisez VS Code sur plusieurs ordinateurs :

1. Cliquez sur l'icône **Comptes** (en bas de la barre d'activité)
2. Connectez-vous avec un compte **Microsoft** ou **GitHub**
3. Activez la **synchronisation**
4. Choisissez ce que vous voulez synchroniser (paramètres, extensions, raccourcis...)

Vos extensions et paramètres seront synchronisés automatiquement ! 🎉

---

## Configurer les extensions

### Accéder aux paramètres d'une extension

**Méthode 1** :
1. Vue Extensions
2. Cliquez sur l'extension
3. Cliquez sur la roue dentée ⚙️
4. Choisissez **"Paramètres de l'extension"**

**Méthode 2** :
1. Ouvrez les paramètres (`Ctrl + ,`)
2. Tapez le nom de l'extension dans la barre de recherche
3. Les paramètres de l'extension s'affichent

### Paramètres importants

#### Pour Prettier :
```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "prettier.semi": true,
  "prettier.singleQuote": true,
  "prettier.tabWidth": 2
}
```

#### Pour Live Server :
```json
{
  "liveServer.settings.donotShowInfoMsg": true,
  "liveServer.settings.port": 5500,
  "liveServer.settings.CustomBrowser": "chrome"
}
```

#### Pour Error Lens :
```json
{
  "errorLens.enabled": true,
  "errorLens.enabledDiagnosticLevels": ["error", "warning"],
  "errorLens.fontSize": "12"
}
```

---

## Recommandations VS Code

VS Code peut vous **recommander des extensions** selon votre projet.

### Voir les recommandations

1. Vue Extensions
2. Dans la barre de recherche, tapez : `@recommended`
3. Vous verrez les extensions recommandées

**Types de recommandations** :
- **Pour votre espace de travail** : basées sur les fichiers de votre projet
- **Populaires** : les plus téléchargées

### Créer un fichier de recommandations pour votre projet

Vous pouvez créer un fichier `.vscode/extensions.json` dans votre projet :

```json
{
  "recommendations": [
    "ritwickdey.liveserver",
    "esbenp.prettier-vscode",
    "formulahendry.auto-rename-tag",
    "pkief.material-icon-theme"
  ]
}
```

Quand quelqu'un ouvre votre projet, VS Code lui suggérera automatiquement ces extensions !

---

## Dépannage : problèmes courants

### Une extension ne fonctionne pas

**Solutions** :
1. **Rechargez VS Code** : Palette de commandes → "Reload Window"
2. **Vérifiez que l'extension est activée** : Vue Extensions → vérifier qu'elle n'est pas désactivée
3. **Vérifiez les paramètres** : certaines extensions nécessitent de la configuration
4. **Désinstallez et réinstallez** l'extension
5. **Vérifiez la compatibilité** : regardez la page de l'extension pour les prérequis

### VS Code est lent au démarrage

**Cause probable** : trop d'extensions

**Solutions** :
1. **Désactivez les extensions inutilisées**
2. **Désinstallez les extensions que vous n'utilisez jamais**
3. **Activez les extensions par espace de travail** (seulement pour certains projets)

### Conflit entre extensions

Parfois, deux extensions font la même chose et entrent en conflit.

**Exemple** : deux extensions de formatage différentes

**Solution** : Désactivez-en une ou définissez laquelle utiliser dans les paramètres.

### Extension en erreur

Si une extension affiche une erreur :
1. Lisez le message d'erreur
2. Vérifiez la **page de l'extension** pour les notes de version
3. **Signalez le problème** sur GitHub (lien dans la page de l'extension)
4. **Utilisez une alternative** en attendant la correction

---

## Bonnes pratiques

### ✅ À FAIRE

- ✅ **Installer progressivement** : commencez avec le strict nécessaire
- ✅ **Lire la description** avant d'installer
- ✅ **Vérifier la popularité** et les notes
- ✅ **Tester une extension** avant d'en installer une autre similaire
- ✅ **Désinstaller** les extensions que vous n'utilisez jamais
- ✅ **Mettre à jour** régulièrement
- ✅ **Lire la documentation** des extensions importantes

### ❌ À ÉVITER

- ❌ **Installer des dizaines d'extensions** d'un coup
- ❌ **Garder des extensions désactivées** : si vous ne l'utilisez pas, désinstallez !
- ❌ **Installer des extensions dupliquées** : une seule extension par fonctionnalité
- ❌ **Ignorer les conflits** entre extensions
- ❌ **Installer sans lire** : certaines extensions nécessitent de la configuration

---

## Découvrir de nouvelles extensions

### Sources de recommandations

1. **Marketplace VS Code** : https://marketplace.visualstudio.com/vscode
2. **GitHub Awesome VS Code** : listes communautaires
3. **Blogs de développement** : articles "Top extensions VS Code"
4. **YouTube** : tutoriels vidéo
5. **Collègues et communauté** : demandez autour de vous !

### Critères pour choisir une extension

Avant d'installer une nouvelle extension, vérifiez :

- ✅ **Popularité** : >1 million de téléchargements
- ✅ **Note** : >4 étoiles
- ✅ **Maintenance** : mise à jour récente (<6 mois)
- ✅ **Documentation** : README complet et clair
- ✅ **Support** : problèmes GitHub actifs et résolus
- ✅ **Taille** : ne pas installer de grosse extension pour une petite fonctionnalité

---

## Extensions par cas d'usage

### Pour HTML/CSS/JavaScript pur (débutant)
```
✅ Live Server
✅ Prettier
✅ Auto Rename Tag
✅ Path Intellisense
✅ Material Icon Theme
✅ HTML CSS Support
```

### Pour JavaScript avancé
```
Ajoutez :
✅ ESLint
✅ Error Lens
✅ JavaScript (ES6) code snippets
```

### Pour travailler avec Git
```
Ajoutez :
✅ GitLens
✅ Git Graph
```

### Pour React (plus tard)
```
Ajoutez :
✅ ES7+ React/Redux/React-Native snippets
✅ Auto Import
✅ Simple React Snippets
```

### Pour Vue.js (plus tard)
```
Ajoutez :
✅ Volar
✅ Vue VSCode Snippets
```

---

## Récapitulatif et checklist d'installation

### Checklist : Extensions essentielles installées

Cochez au fur et à mesure :

**Priorité 1 - À installer maintenant** :
- [ ] Live Server
- [ ] Prettier
- [ ] Auto Rename Tag
- [ ] Path Intellisense
- [ ] Material Icon Theme (ou autre thème d'icônes)

**Priorité 2 - À installer dans les jours suivants** :
- [ ] ESLint (quand vous commencerez sérieusement JavaScript)
- [ ] HTML CSS Support
- [ ] IntelliSense for CSS class names
- [ ] Error Lens
- [ ] Un thème de couleur qui vous plaît

**Priorité 3 - Optionnel / Plus tard** :
- [ ] Live Share (pour collaboration)
- [ ] GitLens (pour Git avancé)
- [ ] Extensions spécifiques à votre projet

### Configuration post-installation

Après installation, vérifiez :

- ✅ **Prettier** est défini comme formateur par défaut
- ✅ **Format On Save** est activé
- ✅ **Live Server** fonctionne (testez avec un fichier HTML)
- ✅ **Thème d'icônes** est appliqué (Palette → File Icon Theme)
- ✅ Toutes les extensions sont **bien activées**

---

## Ce que vous savez faire maintenant

Félicitations ! Vous savez maintenant :

- ✅ Ce qu'est une **extension** et pourquoi c'est utile
- ✅ Comment **installer** une extension
- ✅ Les **5-10 extensions essentielles** pour le développement web
- ✅ Comment **configurer** les extensions importantes
- ✅ Comment **gérer** (activer/désactiver/désinstaller) vos extensions
- ✅ Les **bonnes pratiques** pour ne pas surcharger VS Code
- ✅ Comment **dépanner** les problèmes d'extensions
- ✅ Comment **découvrir** de nouvelles extensions utiles

---

## Pour aller plus loin

### Ressources

**Marketplace officiel** :
- https://marketplace.visualstudio.com/vscode

**Awesome VS Code** (liste communautaire) :
- https://github.com/viatsko/awesome-vscode

**VS Code Can Do That?** (astuces) :
- https://vscodecandothat.com

### Créer ses propres extensions

Vous êtes curieux et voulez créer votre propre extension ?
- Documentation officielle : https://code.visualstudio.com/api
- Tutorial : "Your First Extension"

C'est un projet avancé, mais tout à fait possible une fois que vous maîtrisez JavaScript !

---

## Conseils finaux

### 1. Commencez simple

N'installez pas tout d'un coup. Maîtrisez d'abord les 5 extensions essentielles, puis ajoutez progressivement.

### 2. Expérimentez

N'ayez pas peur de tester des extensions. Vous pouvez toujours les désinstaller si elles ne vous conviennent pas.

### 3. Personnalisez à votre goût

Il n'y a pas de configuration "parfaite". Trouvez ce qui fonctionne pour **vous**.

### 4. Restez raisonnable

Moins d'extensions = VS Code plus rapide et plus stable.

### 5. Lisez la documentation

Les meilleures extensions ont une excellente documentation. Prenez 5 minutes pour la lire, vous gagnerez du temps ensuite.

---

## Navigation


**➡️ Section suivante :** [2.2 Maîtrise de l'éditeur](../02-maitrise-de-lediteur/README.md)

**🏠 Retour au sommaire :** [Table des matières](../../SOMMAIRE.md)

---

*Votre environnement VS Code est maintenant optimisé pour le développement web ! Passons maintenant à la maîtrise des fonctionnalités avancées de l'éditeur.*

⏭️ [Maîtrise de l'éditeur](/02-environnement-de-developpement/02-maitrise-de-lediteur/README.md)
