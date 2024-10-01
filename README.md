### Système de gestion de comptes bancaires

Vous êtes chargé de développer un système de gestion de comptes bancaires pour une banque. La banque propose différents types de comptes, notamment :

-  **Compte courant** : Le client peut déposer et retirer de l'argent librement.
-  **Compte d'épargne** : Le client peut déposer de l'argent, mais il ne peut pas effectuer de retraits directement depuis ce compte.

L'objectif de cet exercice est de respecter le **principe de substitution de Liskov (LSP)**. Cela signifie que toute sous-classe de `BankAccount` (comme `SavingsAccount`) doit pouvoir être utilisée à la place de `BankAccount` **sans provoquer de comportement inattendu**.

#### Contraintes :

1.  **Classe de base** : Créez une classe concrète `BankAccount` avec des méthodes génériques pour déposer (`deposit()`) et retirer (`withdraw()`) de l'argent.

2.  **Sous-classes** :

    -   **CurrentAccount** (Compte courant) : Les clients peuvent déposer et retirer de l'argent librement.
    -   **SavingsAccount** (Compte d'épargne) : Les clients peuvent déposer de l'argent, mais pas en retirer.
3.  **Problème à éviter** : Le principe de substitution de Liskov (LSP) stipule que les sous-classes doivent pouvoir être utilisées de manière interchangeable avec la classe de base sans provoquer d'erreurs ou de comportements imprévu. Pour ce faire, vous devrez donc contrevenir à la structure de l'héritage pour que SavingsAccount ne puisse jamais exécuter une méthode qui ne lui est pas accessible.
