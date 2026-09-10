# SQL & PostgreSQL

## Bases de données relationnelles vs non relationnelles

## 1. Bases de données relationnelles (SQL)

* **Structure :** Données organisées en tables formées de lignes (enregistrements) et de colonnes (attributs/champs).
* **Liaisons :** Les tables sont reliées entre elles via des clés primaires (identifiants uniques) et des clés étrangères.
* **Schéma :** Nécessitent un schéma prédéfini et strict spécifiant la structure, les types de données et les contraintes.
* **Avantages :** Maintien rigoureux de l'intégrité des données et capacité à exécuter des requêtes complexes sur plusieurs tables.

## 2. Bases de données non relationnelles (NoSQL)

* **Structure :** Stockage sous forme de fichiers individuels non connectés ou de structures flexibles (clé-valeur, documents, etc.).
* **Schéma :** Schéma flexible ou absent, permettant d'ajouter, modifier ou supprimer des champs sans contrainte rigide.

## Principales SGBDR & Installation de PostgreSQL

## 1. Principaux systèmes de gestion de bases de données relationnelles (SGBDR)

### SGBD Open Source (Gratuits)

* **MySQL :** Très populaire pour le développement web ; simple, fiable et soutenu par une large communauté.
* **PostgreSQL :** Défini comme le SGBDR open source le plus avancé ; reconnu pour sa fiabilité, l'intégrité des données et son extensibilité (types personnalisés, fonctions sur-mesure).
* **SQLite :** Moteur léger, auto-contenu et sans serveur (*serverless*). Zéro configuration requise, stockage directement dans des fichiers.

### SGBD Propriétaires (Entreprise)

* **Microsoft SQL Server :** Largement utilisé dans les environnements professionnels et l'écosystème Microsoft.
* **Oracle Database :** SGBDR très scalable, optimisé pour les applications d'entreprise nécessitant des performances élevées.

---

## 2. Composants d'installation de PostgreSQL

* **PostgreSQL Server :** Le moteur de base de données principal.
* **pgAdmin 4 :** Interface graphique d'administration et de gestion.
* **Stack Builder :** Outil pour installer des extensions et logiciels complémentaires.
* **Command Line Tools :** Outils en ligne de commande, incluant **`psql`** (le terminal interactif pour exécuter des requêtes SQL).

---

## 3. Configuration par défaut de PostgreSQL (Windows)

* **Port par défaut :** `5432`
* **Compte Administrateur :** Utilisateur `superuser` (requiert la définition d'un mot de passe à l'installation).

---

## 4. Commande d'installation rapide (macOS via Homebrew)

```bash
brew install postgresql@<version>
```

```markdown

## 5. Introduction à SQL et création de bases de données

## Qu'est-ce que SQL ?
* **Définition :** *Structured Query Language* (développé dans les années 1970 sous le nom de SEQUEL).
* **Rôle :** Langage standardisé pour stocker, gérer, rechercher et manipuler les données dans une base de données relationnelle.
* **Conventions :** 
  * Les mots-clés SQL s'écrivent généralement en majuscules (ex: `CREATE DATABASE`).
  * Les instructions SQL se terminent par un point-virgule (`;`).
  * La convention de nommage recommandée pour les tables et colonnes est le **snake_case** (ex: `delivery_orders`).

---

## Connexion via `psql` (PostgreSQL)

* **Depuis le terminal (invite de commande) :**
  ```bash
  psql -U <username> -d <database_name>

```

*(Note : PostgreSQL inclut une base par défaut appelée `postgres`).*

* **Changer de base depuis le shell `psql` :**

```text
\c nom_de_la_base

```

*(Les commandes débutant par `\` sont propres au shell `psql` et ne nécessitent pas de point-virgule).*

---

## Commandes SQL fondamentales

* **Créer une base de données :**

```sql
CREATE DATABASE nom_de_la_base;

```

* **Créer une table :**

```sql
CREATE TABLE produits (
    id SERIAL,
    nom VARCHAR(255)
);
```

```markdown
# [What Are the Basic Data Types in SQL?](https://www.freecodecamp.org/learn/relational-databases-v9/lecture-working-with-relational-databases/what-are-the-basic-data-types-in-sql)

## Définition & Syntaxe
Lors de la création d'une table SQL, il est essentiel de définir le type de données de chaque colonne pour assurer la cohérence des enregistrements.

```sql
CREATE TABLE nom_de_la_table (
  colonne1 type_de_donnees contrainte,
  colonne2 type_de_donnees contrainte,
  colonne3 type_de_donnees contrainte
);

```

---

## Les 6 Catégories Principales de Types de Données

* **1. Numériques**
* `INTEGER` : Entier standard (4 octets, plage de -2 147 483 648 à 2 147 483 647). Choix par défaut recommandé.
* `SMALLINT` / `BIGINT` : Variantes d'entiers avec des plages plus réduites ou plus larges.
* `SERIAL` : Pseudo-type propre à PostgreSQL générant un entier auto-incrémenté unique non `NULL` pour les identifiants (`id SERIAL`).
* *Équivalent MySQL :* `INT AUTO_INCREMENT`.

* `FLOAT` / `DECIMAL` : Stockage de nombres à virgule ou décimaux.

* **2. Chaînes de caractères (Texte)**
* `VARCHAR(n)` : Chaîne de longueur variable avec une limite maximale de $n$ caractères (ex: `VARCHAR(50)`).
* `TEXT` : Chaîne de texte sans limite de longueur prédéfinie.
* `CHAR(n)` : Chaîne de longueur fixe.

* **3. Date et Heure**
* `DATE` : Stocke la date (`YYYY-MM-DD`).
* `TIME` : Stocke l'heure (`HH:MM:SS`).
* `TIMESTAMP` : Combine date et heure.
* `TIMESTAMP WITH TIME ZONE` : Combine date, heure et gestion du fuseau horaire.

* **4. Booléens**
* `BOOLEAN` : Stocke une valeur logique (`TRUE` ou `FALSE`).

* **5. Unicode**
* `NVARCHAR` / `NTEXT` : Garantit la gestion et le stockage corrects de caractères issus de divers alphabets/langues.

* **6. Binaires et Divers**
* **Binaires :** Stockage de fichiers non textuels (images, audio, vidéo).
* **Divers :** Types spécialisés tels que `XML` ou `TABLE`.

---

## Questions & Auto-évaluation

* **Quel type est utilisé pour stocker des entiers dans PostgreSQL ?**
* **Réponse :** `INTEGER`

* **Pour stocker un long document texte ou une très longue chaîne, quel type privilégier ?**
* **Réponse :** `TEXT`

* **Quel type de données permet de stocker la valeur `TRUE` ou `FALSE` ?**
* **Réponse :** `BOOLEAN`

```

```
