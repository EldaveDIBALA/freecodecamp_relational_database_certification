## Éditeurs de code vs IDE

* **Éditeur de code :** Application permettant de modifier directement le texte de fichiers de code.
* **IDE (Integrated Development Environment) :** Environnement complet qui permet de compiler, exécuter et déboguer du code en plus de l'éditer.

## Exemples d'IDE locaux

* **Visual Studio (Microsoft) :** Suite complète pour créer, déboguer et déployer des applications.
* **Xcode (Apple) :** Conçu pour le développement d'applications macOS, iOS, watchOS et tvOS.
* **Android Studio (Google) :** Spécialisé pour le développement d'applications Android.

## Exemples d'éditeurs de code locaux

* **Visual Studio Code (Microsoft) :** Éditeur léger, open-source et extensible via un large écosystème d'extensions.
* **Sublime Text :** Éditeur rapide et polyvalent avec coloration syntaxique personnalisable.
* **Notepad++ :** Éditeur léger sous Windows offrant la coloration syntaxique et le repliage de code.

## Éditeurs de code dans le cloud

* Outils en ligne exécutables directement depuis un navigateur web, sans installation locale.
* **Replit :** Plateforme collaborative pour écrire, exécuter et partager du code.
* **GitHub Codespaces :** Environnement de développement complet et prêt à l'emploi directement relié à GitHub.
* **StackBlitz :** Environnement axé sur le développement et le test de projets web.

## Installation de Visual Studio Code

* **Attention lors du téléchargement :** Veillez à bien vous rendre sur le site officiel de **VS Code** et non sur celui de Visual Studio.
* **Installation sous Windows :** Télécharger le fichier d'installation `.exe` et suivre l'assistant d'installation.
* **Installation sous macOS :**
  * Option 1 : Télécharger l'archive `.zip` contenant l'application `.app`.
  * Option 2 : Installer via Homebrew dans le terminal avec la commande `brew install --cask visual-studio-code`.
* **Installation sous Linux :** Télécharger directement le fichier paquet `.deb` ou `.rpm`, puis lancer l'application via le programme ou la commande `code`.

## Créer un projet et exécuter son code localement dans VS Code

* **Notion de Workspace :** VS Code considère tout dossier (répertoire) ouvert dans l'éditeur comme un espace de travail ("workspace").
* **Création d'un dossier de projet via le terminal :**
  * Windows (Command Prompt) : `cd /d %USERPROFILE%` pour aller dans le dossier utilisateur, puis `mkdir mon-projet`.
  * Windows (PowerShell) / macOS / Linux : `cd ~` puis `mkdir mon-projet`.
* **Ouverture de VS Code depuis le terminal :**
  * Commande : `code /chemin/vers/dossier` ou `code .` pour ouvrir le dossier courant.
  * **Sur macOS :** La commande `code` nécessite une activation préalable via la palette de commandes (`Cmd + Shift + P` > `Shell Command: Install 'code' command in PATH`).
* **Création de fichiers :**
  * Passer par le menu `File > New File...`, nommer le fichier (ex. `index.html`) et l'enregistrer dans l'espace de travail.
* **Exécution du code Web avec un serveur local :**
  * Il est déconseillé d'ouvrir un fichier HTML directement dans le navigateur (risque d'erreurs d'affichage du CSS ou de requêtes).
  * **Extension Live Server :** Permet de lancer un serveur web local directement dans VS Code via le bouton *Go Live* dans la barre d'état (ou via l'adresse `http://localhost:5500/`).

## Édition et mise en forme

* **Formater le fichier :** `Shift + Alt + F` (Windows) | `Ctrl + Shift + I` (Linux) | `Shift + Option + F` (macOS)
* **Supprimer la ligne courante :** `Ctrl + Shift + K` (Windows/Linux) | `Cmd + Shift + K` (macOS)
* **Curseurs multiples (lignes adjacentes) :**
  * Windows : `Ctrl + Alt + Haut/Bas`
  * Linux : `Shift + Alt + Haut/Bas`
  * macOS : `Option + Cmd + Haut/Bas`
* **Ajouter un curseur au clic :** `Alt + Clic` (Windows/Linux) | `Option + Clic` (macOS)

## Recherche et navigation

* **Rechercher dans tous les fichiers :** `Ctrl + Shift + F` (Windows/Linux) | `Cmd + Shift + F` (macOS)
* **Rechercher et remplacer :** `Ctrl + Shift + H` (Windows/Linux) | `Cmd + Shift + H` (macOS)
* **Ouvrir la palette de commandes :** `Ctrl + Shift + P` (Windows/Linux) | `Cmd + Shift + P` (macOS)

## Affichage et interface

* **Masquer / Afficher la barre latérale :** `Ctrl + B` (Windows/Linux) | `Cmd + B` (macOS)
* **Agrandir le zoom :** `Ctrl + Plus` (Windows/Linux) | `Cmd + Plus` (macOS)
* **Réduire le zoom :** `Ctrl + Moins` (Windows/Linux) | `Cmd + Moins` (macOS)

## Extensions utiles pour VS Code

* **Lisibilité et correction :**
  * **Better Comments :** Met en valeur certains types de commentaires (ex. TODO, questions, avertissements).
  * **Code Spell Checker :** Vérifie l'orthographe dans le code en prenant en compte la casse (comme le camelCase).
  * **Error Lens :** Surligne toute la ligne et affiche directement le message d'erreur au lieu du simple soulignement.
  * **Indent Rainbow :** Ajoute une couleur à chaque niveau d'indentation pour mieux identifier la portée du code.
  * **Colorize :** Facilite la visualisation des couleurs directement dans les propriétés CSS.
  * **VS Code Great Icons :** Personnalise les icônes de l'arborescence des fichiers pour une meilleure lisibilité.

* **Assistants IA :**
  * **GitHub Copilot / Tabnine :** Proposent des suggestions de code en temps réel pendant la saisie.

* **Spécifiques aux langages :**
  * **ESLint & Prettier :** Pour linter et formater le code JavaScript.
  * **Pretty TypeScript Errors :** Rendu plus clair des messages d'erreur TypeScript.

* **Extensions ludiques :**
  * **VS Code Pets :** Affiche des animaux virtuels dans l'éditeur.
  * **Power Mode :** Ajoute des effets visuels lors d'une saisie rapide de code.
  * **Discord Presence :** Affiche votre activité de codage sur votre profil Discord.
