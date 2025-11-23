## 📝 4 Exercices de SQL Pur

### Exercices de Lecture (SELECT)

1.  **Affichage, Alias, Ordre et Limite :** Affichez les **5 titres de films** (`title` de la table `film`) classés par **ordre alphabétique croissant**, en utilisant un **alias** pour la colonne.
2.  **Agrégation :** Calculez la **moyenne**, le **minimum**, le **maximum**, le **nombre total** et la **somme** du champ `length` (durée en minutes) de tous les films dans la table `film`.

---

### Exercices de Modification (INSERT / UPDATE)

3.  **Insertion (`INSERT`) avec gestion d'ID et de Date :**
    * **Insérez** un nouvel acteur avec le prénom `"JEAN-CLAUDE"`, le nom `"VANDAMME"`, le nouvel ID calculé, et la date/heure actuelle pour le champ **`last_update`**.
      * **Trouvez** l'**`actor_id` maximum** existant dans la table `actor`, puis **calculez le nouvel ID** en ajoutant 1.
      * **Format de date requis pour le `last_update` :** Utilisez le module `datetime` pour générer la chaîne `YYYY-MM-DD HH:MM:SS`.

4.  **Modification (`UPDATE`) par ID :** **Modifiez** l'acteur que vous venez d'insérer (en le ciblant par son **ID unique**) pour changer son prénom de `"JEAN-CLAUDE"` à `"JC"`.