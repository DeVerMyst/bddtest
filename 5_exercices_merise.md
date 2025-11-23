## 1. Exercice Simple (1 Fait, 2 Dimensions)

Ce tableau devrait conduire à un **schéma en étoile simple** (1 table de Faits, 2 tables de Dimensions).

| Colonne | Définition / Contenu |
| :--- | :--- |
| **Numéro\_Facture** | Identifiant unique de la transaction. |
| **Date\_Transaction** | Date et heure de l'achat. |
| **Montant\_Total\_HT** | Valeur numérique de la transaction. |
| **Nom\_Client** | Nom complet de l'acheteur. |
| **Email\_Client** | Adresse de contact de l'acheteur. |
| **Nom\_Vendeur** | Nom de l'employé qui a effectué la vente. |
| **Magasin\_Vendeur** | Lieu physique du vendeur (Ville). |

### 🎯 Tables attendues :

* **Faits :** Transactions
* **Dimensions :** Clients, Vendeurs

---

## 2. Exercice Moyen (1 Fait, 1 Association)

Ce tableau introduit une relation **Plusieurs-à-Plusieurs (N,M)** via les détails de la commande, qui nécessite une **Table d'Association** (ou Table de Faits détaillée).

| Colonne | Définition / Contenu |
| :--- | :--- |
| **ID\_Commande** | Identifiant unique de la commande globale. |
| **Date\_Livraison** | Date prévue de livraison. |
| **Quantite\_Commandee** | Nombre d'unités d'un produit spécifique. |
| **Prix\_Unitaire\_Vente** | Prix auquel le produit a été vendu. |
| **Reference\_Produit** | Code du produit commandé. |
| **Nom\_Produit** | Nom commercial de l'article. |
| **Categorie\_Produit** | Type de produit (Ex: Alimentaire, Électronique). |
| **Nom\_Fournisseur** | Société qui a fourni le produit. |

### 🎯 Tables attendues :

* **Faits/Association :** Lignes de Commande (détails)
* **Dimensions :** Commandes (entête), Produits

---

## 3. Exercice Complexe (2 Faits, 2 Associations, 1 Dimension Partagée)

Ce tableau mélange des informations transactionnelles (Ventes) et des informations d'utilisation (Note/Avis), et implique des relations N,M pour les deux processus. Il illustre le concept de **Dimension Partagée** (les utilisateurs).

| Colonne | Définition / Contenu |
| :--- | :--- |
| **Date\_Achat** | Jour où l'article a été acheté. |
| **Montant\_Achat** | Prix de vente final. |
| **Date\_Avis** | Jour où l'utilisateur a laissé une note. |
| **Note\_Avis** | Score (1 à 5 étoiles) donné au produit. |
| **Email\_Utilisateur** | Identifiant de la personne (Client/Rédacteur). |
| **Ville\_Utilisateur** | Localisation géographique de l'utilisateur. |
| **Nom\_Film** | Nom complet du produit (Film/Jeu). |
| **Genre\_Film** | Catégorie du produit (Ex: Action, Comédie). |

### 🎯 Tables attendues :

* **Faits 1 :** Ventes (Transaction)
* **Faits 2 :** Avis/Notes (Évaluation)
* **Dimension Partagée :** Utilisateurs
* **Dimension Annexe :** Produits
* **Associations :** Une Table d'Association sera nécessaire pour relier Utilisateurs/Produits à la table de Faits des Avis (si l'avis est une association N,M entre utilisateur et produit).
