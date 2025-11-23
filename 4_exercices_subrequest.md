**Énoncé :**

Trouvez le **prénom** (`first_name`) et le **nom** (`last_name`) de **tous les clients** de la table `^^customer^^` qui vivent dans la ville de **'London'**.

* **Logique :** Vous devez utiliser une sous-requête pour déterminer la liste de tous les **`address_id`** qui correspondent à la ville 'London' (en joignant `address` et `city` dans la sous-requête), puis utiliser l'opérateur **`IN`** dans la requête principale pour filtrer les clients.