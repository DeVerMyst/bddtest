## 📝 Énoncés des Exercices 1 & 2 (SQLA → Pandas → Seaborn)

Ces exercices sont conçus pour mettre en œuvre le pipeline en **trois étapes** : Requête SQL (SQLAlchemy), Chargement en DataFrame (Pandas) et Visualisation (Seaborn).

### Exercice 1 : Distribution des Taux de Location (Taux d'Emprunt)

Cet exercice permet de visualiser la distribution d'une variable numérique simple.

1.  **Requête SQL :** Écrivez une requête SQL pour sélectionner uniquement le champ **`rental_rate`** (taux de location) de la table `^^film^^`.
2.  **Conversion Pandas :** Chargez les résultats de la requête SQL dans un DataFrame Pandas.
3.  **Visualisation (Seaborn) :** Créez un **histogramme** (*histplot*) avec Seaborn pour visualiser la **distribution** de la colonne `rental_rate`.

### Exercice 2 : Durée Moyenne des Films par Classification

Cet exercice utilise une fonction d'agrégation SQL et une visualisation pour la comparaison de catégories.

1.  **Requête SQL :** Écrivez une requête SQL pour calculer la **durée moyenne** (`AVG(length)`) de tous les films pour **chaque classification** (`rating` - ex: G, PG, R) dans la table `^^film^^`.
    * *Indice : Vous devrez utiliser la clause `GROUP BY`.*
2.  **Conversion Pandas :** Chargez les résultats (la classification et sa durée moyenne) dans un DataFrame Pandas.
3.  **Visualisation (Seaborn) :** Créez un **diagramme à barres** (*barplot*) avec Seaborn pour comparer visuellement la durée moyenne (`avg_length`) pour chaque catégorie de classification (`rating`).

---

