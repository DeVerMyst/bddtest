
## 📝 Énoncés des Exercices de Jointure SQL (Sakila)

### Exercice 1 : Jointure Simple à 2 Tables

**Objectif :** Joindre la table des clients à la table des locations pour trouver les clients les plus actifs récemment.

| Tables Impliquées | Clauses Spécifiques |
| :--- | :--- |
| `customer` et `rental` | Alias, `ORDER BY`, `LIMIT` |

**Énoncé :**

Écrivez une requête SQL pour lister les **10 clients** (`first_name`, `last_name` de la table `customer`) ayant effectué leur location la **plus récente**. Affichez également la date de la location (`rental_date` de la table `rental`).

* **Instructions :**
    * Utilisez des **alias** clairs pour les tables (`c` pour `customer`, `r` pour `rental`).
    * Triez le résultat par la date de location la plus récente (`ORDER BY`).
    * Limitez l'affichage aux 10 premiers résultats (`LIMIT`).

---

### Exercice 2 : Jointure à 3 Tables

**Objectif :** Relier la transaction (`rental`) au contexte du produit (`film`) via la table d'inventaire.

| Tables Impliquées | Clauses Spécifiques |
| :--- | :--- |
| `rental`, `inventory` et `film` | Alias, `ORDER BY`, `LIMIT`, `WHERE` |

**Énoncé :**

Quel est le **titre du film** (`title` de la table `film`) et la **date de location** (`rental_date` de la table `rental`) des **5 dernières locations** ?

* **Filtre :** Incluez uniquement les films dont la classification (`rating`) est `'PG-13'`.
* **Instructions :**
    * Triez par la date de location la plus récente (`ORDER BY`).
    * Limitez l'affichage aux 5 premiers résultats (`LIMIT`).

---

### Exercice 3 : Jointure à 4 Tables (Liaison Many-to-Many)

**Objectif :** Traverser une table de liaison pour relier des entités et ajouter une dimension (langue).

| Tables Impliquées | Clauses Spécifiques |
| :--- | :--- |
| `actor`, `film_actor`, `film` et `language` | Alias, `LIMIT`, `WHERE`, `DISTINCT` |

**Énoncé :**

Listez les **15 premiers acteurs** (`first_name`, `last_name` de la table `actor`) qui ont joué dans des films dont la **langue originale** (`name` de la table `language`) est l'**Anglais** (`'English'`). Affichez uniquement le nom et le prénom de l'acteur.

* **Instructions :**
    * Utilisez **`DISTINCT`** pour garantir que chaque acteur n'apparaisse qu'une seule fois.
    * Triez par le nom de famille de l'acteur (`ORDER BY`).
    * Limitez le résultat à 15 entrées (`LIMIT`).

---

### Exercice 4 : Jointure à 5 Tables (Transaction et Structure)

**Objectif :** Intégrer la dimension humaine (`staff`) et structurelle (`store`) à la transaction (`rental`) et au produit (`film`).

| Tables Impliquées | Clauses Spécifiques |
| :--- | :--- |
| `rental`, `inventory`, `film`, `store` et `staff` | Alias, `ORDER BY`, `LIMIT`, `WHERE` |

**Énoncé :**

Pour le **magasin n°2** (`store_id = 2`), listez les **5 derniers films loués** (`title` de la table `film`), la **date de location** (`rental_date` de la table `rental`) et le **prénom/nom de l'employé** (`first_name`, `last_name` de la table `staff`) qui a géré la transaction.

* **Instructions :**
    * Utilisez la clause `WHERE` pour filtrer sur le magasin n°2.
    * Triez par la date de location la plus récente (`ORDER BY`).
    * Limitez l'affichage aux 5 résultats (`LIMIT`).

---

### Exercice 5 : Jointure de Navigation et Agrégation (6 Tables)

**Objectif :** Naviguer à travers de nombreuses tables de dimensions pour filtrer les clients (par ville) et effectuer une agrégation sur les paiements.

| Tables Impliquées | Clauses Spécifiques |
| :--- | :--- |
| `customer`, `address`, `city`, `country`, `payment` | Alias, `GROUP BY`, `HAVING`, `ORDER BY`, Fonctions d'agrégation (`SUM`) |

**Énoncé :**

Trouvez le **montant total des paiements** (`SUM(amount)` de la table `payment`) effectués par les clients qui vivent dans la ville de **"London"** (`city` de la table `city`). Affichez le prénom et le nom du client.

* **Filtres et Agrégation :**
    * Regroupez les résultats par client (`GROUP BY`).
    * N'incluez que les clients ayant dépensé plus de **100.00** unités monétaires (`HAVING`).
* **Instructions :**
    * Triez le résultat par le montant total dépensé (décroissant) (`ORDER BY`).

---