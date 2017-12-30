# Vude d'ensemble des principes _Clean Code_

## SOLID

### SRP : _Single Responsability Principle_

### OCP : _Open-Closed Principle_

### ISP : _Interface Segregation Principle_

### DIP : _Dependency Inversion Principle_

### Liskov Principle

## Lois, règles et autres principes

### Loi de "LeBlanc" 

_"Plus tard signifie jamais"_

### Règle du Boy-Scout

_"Laisser le code plus propre qu'on ne l'a trouvé"_

### Loi de Déméter

_"Un module ne doit pas connaître les détails internes des objets qu'il manipule"_

Les objets cachent leurs données et exposent des opérations.

Une méthode `f` d'une classe `C` ne doit appeler que les méthodes des éléments suivants : 

* C
* un objet créé par f
* un objet passé en argument à f
* un objet contenu dans une variable d'instance de C

## Bonnes pratiques

### Envelopper les API tierces

Lorsque nous enveloppons une API tierce nous minimisons dos dépendances avec cette API : nous pouvons décider de changer de bibliothèque sans avoir à payer le prix fort. Par ailleurs, il est également plus facile de simuler les invocations d'une API ou d'un logiciel tiers lorsque nous testons notre propre code.

### Ne pas spéculer sur l'avenir

Notre code doit être pragmatique, non spéculatif. Il ne doit contenir que le nécessaire.

## Nommage / Formatage

### Rangement vertical

_"Une fonction appelée doit se trouver en dessous d'une fonction qui l'appelle"_


### Style de formatage

Les développeurs de l'équipe doivent se mettre d'accord sur un même style de formatage et le respecter

## Tests

### 3 lois du TDD _Tests Driven Development_

1. Vous ne devez pas écrire un code de production tant que vous n'avez pas écrit un unitaire d'échec
1. Vous devez uniquement écrire le test unitaire suffisant pour échouer : l'impossibilité de compiler est un échec
1. Vous devez uniquement écrire le code de production suffisant pour réussir le test d'échec courant

### Principes FIRST

1. **F**AST : (Rapide) : les tests doivent être rapides.
1. **I**NDEPENDENT (Indépendant) : les tests ne doivent pas dépendendre les uns des autres. Un test ne doit pas établir les conditions d'exécution du test suivant. Vous devez être en mesure d'exécuter chaque test indépendamment et dans l'ordre que vous voulez.
1. **R**EPEATABLE (Reproductible) : les tests doivent pouvoir être reproduits dans n'importe quel environnement.
1. **S**ELF-VALIDATING (Auto-validant) : les tests doivent avoir un résultat binaire : ils réussisent ou ils échouent. Vous ne devez pas avoir à consulter un fichier de journalisation ou comparer manuellement 2 fichiers.
1. **T**IMELY (au moment opportun) : les tests doivent être écrits au moment opportun : juste avant le code de production qui permet de les réussir.

### Principes généraux

* Le code de test est aussi important que le code de production
* Ce sont les tests unitaires qui permettent d'obtenir un code flexible, maintenable et réutilisable
* Sans les tests chaque modification est un bogue potentiel : les tests permettent le changement
* Plus les tests sont négligés plus il est difficile de les modifier
* Plus le code de test est embrouillé plus le temps nécessaire à l'ajout de nouveaux tests dépassera celui nécessaire à écrire le nouveau code de production
* La lisibilité est sans doute encore plus importante dans les tests unitaires qu'elle ne l'est dans le code de production

### Tests d'apprentissage

Les tests d'apprentissage ne sont pas seulement gratuits, ils ont un retour sur investissement positif. Si de nouvelles versions du paquetage tiers sont publiées nous éx"cutons les tests d'apprentissage pour savoir s'il existe des différences de comportement.

### Structure d'un test : Build-Operate-Check

1. Constuire les données du test
1. Exploiter les données du tests
1. Vérifier que l'opération a produit les résultats escomptés
