# Vude d'ensemble des prinicpes de codage propre _Clean Code_

## SOLID

### SRP : _Single Responsability Principle_

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

## Tests
