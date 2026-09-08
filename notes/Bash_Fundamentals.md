# Notions de base : Ligne de commande, Terminal et Shell

* **Ligne de commande (Command Line) :** Interface textuelle de base permettant de saisir et d'exécuter des commandes (généralement validées par la touche Entrée).
* **Terminal :** Application qui fournit une interface en ligne de commande pour exécuter des commandes au niveau du système.
* **Shell :** Logiciel qui enveloppe la ligne de commande, interprète les saisies de l'utilisateur sous forme de commandes et renvoie le résultat.

## Accès au terminal selon le système d'exploitation

* **Windows :**
  * **Shells intégrés :** PowerShell et Invite de commandes (Command Prompt), chacun disposant de sa propre application terminal.
  * **Microsoft Terminal :** Application moderne permettant d'accéder à la fois à PowerShell, à l'Invite de commandes et aux shells Linux (via WSL) dans un même outil.
* **macOS :**
  * Terminal par défaut : **Terminal** (accessible via Spotlight ou le lanceur d'applications).
  * Emulateurs tiers : iTerm, Ghostty, etc.
* **Linux :**
  * Grande variété d'émulateurs et de shells selon la distribution et l'environnement de bureau (ex. *kitty* sur Arch Linux).
  * Les applications s'installent généralement via le gestionnaire de paquets de la distribution.

## Raccourcis essentiels de la ligne de commande

* **Navigation dans l'historique :**
  * **Flèche Haut :** Remonter dans l'historique des commandes exécutées.
  * **Flèche Bas :** Descendre dans l'historique des commandes.

* **Saisie et autocomplétion :**
  * **Touche Tab :** Complète automatiquement la commande, le fichier ou l'argument en cours de saisie (basé sur l'historique en *nix/zsh ou sur les éléments disponibles dans PowerShell).

* **Gestion du terminal et des processus :**
  * **Effacer l'écran :** `Ctrl + L` (Linux, macOS, PowerShell) ou la commande `cls` sous PowerShell.
  * **Interrompre un processus :** `Ctrl + C` pour arrêter la commande en cours d'exécution (attention sous PowerShell, cela copie aussi le texte sélectionné).
  * **Mettre en arrière-plan (*nix uniquement) :** `Ctrl + Z` suspend le processus courant et le place en tâche de fond (utiliser `fg` pour le faire revenir au premier plan).
  * **Répéter la dernière commande (*nix uniquement) :** Taper `!!` puis `Entrée` pour réexécuter la commande précédente.

## Définition de Bash et commandes de base

* **Définition :** **Bash** signifie *Bourne Again SHell*. C'est le shell le plus répandu dans les environnements de type Unix.
* **Navigation et affichage :**
  * `pwd` : Affiche le chemin du répertoire de travail actuel (*print working directory*).
  * `cd` : Change de répertoire (supporte les chemins absolus avec `/`, relatifs, et `..` pour remonter d'un dossier).
  * `ls` : Liste le contenu du répertoire courant. Accepte des options comme `-a` (fichiers cachés) et `-l` (permissions des fichiers).
  * `cat` / `less` : Affichent le contenu d'un fichier.
* **Gestion des fichiers et dossiers :**
  * `mkdir` : Crée un nouveau dossier/répertoire.
  * `touch` : Crée un nouveau fichier vide (ex. `touch readme.md`).
  * `mv` : Déplace ou renomme un fichier (ex. `mv ancien.txt nouveau.txt`).
  * `cp` : Copie un fichier ou un dossier (utiliser l'option `-r` pour un dossier).
  * `rm` : Supprime un fichier. Utiliser `-r` pour un dossier et `-f` pour forcer la suppression d'un fichier protégé.
* **Redirection de texte et manuel :**
  * `echo` : Affiche du texte dans le terminal.
  * Opérateur `>` : Redirige la sortie pour créer ou écraser un fichier (ex. `echo "Texte" > readme.md`).
  * Opérateur `>>` : Ajoute du texte à la fin d'un fichier existant sans l'écraser.
  * `man` : Affiche la page de manuel/d'aide pour n'importe quelle commande (ex. `man ls`).

## Options et drapeaux (Flags) dans les commandes

* **Définition :** Arguments spéciaux modifiant le comportement d'une commande (souvent utilisés comme des interrupteurs marche/arrêt).
* **Forme longue (Long form) :**
  * Utilisent deux tirets (`--`).
  * Exemples : `--version` (affiche la version), `--help` (affiche le manuel d'aide).
  * Syntaxe avec valeur : utilise un signe égal (ex. `ls --width=50` ou `ls --color=never`).
* **Forme courte (Short form) :**
  * Utilisent un seul tiret (`-`) suivi d'une lettre (ex. `ls -a`).
  * **Avantage :** Possibilité de chaîner plusieurs options en une seule commande (ex. `ls -ahs` au lieu de `ls --all --human-readable --size`).
  * Syntaxe avec valeur : utilise un espace pour séparer l'option de sa valeur (ex. `ls -w 50`).

## Configuration de la langue système et de la disposition du clavier pour Bash et PostgreSQL

* **Importance du clavier anglais (US) :** Les outils de programmation (Bash, SQL/PostgreSQL) s'attendent aux caractères standard d'un clavier américain. Les dispositions non-anglaises (AZERTY, QWERTZ, etc.) peuvent altérer le comportement des symboles (ex. `;`, `/`, `\`, `'`, `"`, `|`) ou utiliser des "touches mortes", provoquant des erreurs de syntaxe.
* **Recommandation :** Passer temporairement le clavier en **English (US)** pendant les cours ou ateliers (cette disposition s'applique aussi à GitHub Codespaces).

* **Changer de disposition selon l'OS :**
  * **Windows :** *Paramètres* > *Heure et langue* > *Langue et région* > Ajouter et sélectionner le clavier *English (US)*.
  * **macOS :** *Réglages système* > *Clavier* > *Sources d'entrée* > Ajouter *English (US)*.
  * **Linux (Terminal) :** 
    * Vérifier la disposition actuelle : `setxkbmap -query`
    * Basculer en clavier US : `setxkbmap us`

* **Vérification :** Tester les caractères `; : / \ | ' " $ { } [ ] ( )` dans le terminal. S'ils s'affichent immédiatement sans attendre d'autre touche (touches mortes), la configuration est correcte.
