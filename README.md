# Vude d'ensemble des principes _Clean Code_

_Synthèse des notions de Clean Code de **Robert C. MARTIN**._

## A- SOLID

### SRP : _Single Responsability Principle_

_Il ne doit exister qu'une et une seule raison de modifier une classe ou un module._

### OCP : _Open-Closed Principle_

_Les classes doivent être ouvertes à l'extension mais fermées à la modification._

Dans un système idéal nous incorporons de nouvelles fdonctionnalités en étendant le système, non en modifiant le code existant.

### Liskov Principle

### ISP : _Interface Segregation Principle_

### DIP : _Dependency Inversion Principle_

L'inversion de contrôle déplace les responsabilités secondaires depuis un objet vers d'autres objets qui sont dédiés à chaque responsabilité et respecte ainsi le principe de responsabilité unique.

## B- Lois, règles et autres principes

### DRY : _Don't Repeat Yourself_

_Principe qui consiste à éviter la redondance de code au travers de l’ensemble d’une application afin de faciliter la maintenance, le test, le débogage et les évolutions de cette dernière._

* **La redondance est le principal ennemi d'un système bien conçu.**
* **Une redondance représente en réalité une opportunité d'abstraction maqnuée.**

<https://fr.wikipedia.org/wiki/Ne_vous_r%C3%A9p%C3%A9tez_pas>

### KISS : _Keep It Simple, Stupid_

_Principe dont la ligne directrice de conception qui préconise la simplicité dans la conception et que toute complexité non indispensable devrait être évitée dans toute la mesure du possible._

<https://fr.wikipedia.org/wiki/Principe_KISS>

### Principe de moindre surprise

_Toute fonction ou classe doit implémenter les comportements auquels un autre programmeur peut raisonnablement s'attendre._

**Exemples :**

* Le code doit être placé là où le lecteur s'attend naturellement à la trouver.
* Les noms des fonctions doivent indiquer leur rôle, s'il faut examiner la documentation ou l'implémentation de la fonction pour connaître son rôle cela signifie qu'un meilleur nom doit être trouvé ou que la fonctionnalité doit être déplacée dans des fonctions ayant des noms appropriés.

<https://fr.wikipedia.org/wiki/Principe_de_moindre_surprise>

### Loi de "LeBlanc" 

_"Plus tard signifie jamais"_

Exemples : 

* Commenter ou ignorer un test qui échoue et se dire que l'on fera en sorte qu'il réussisse plus tard

### Règle du Boy-Scout

_"Laisser le code plus propre qu'on ne l'a trouvé"_

### Loi de Déméter

_"Un module ne doit pas connaître les détails internes des objets qu'il manipule"_

<https://fr.wikipedia.org/wiki/Loi_de_D%C3%A9m%C3%A9ter>

Les objets cachent leurs données et exposent des opérations.

Une méthode `f` d'une classe `C` ne doit appeler que les méthodes des éléments suivants : 

* `C`
* un objet créé par `f`
* un objet passé en argument à `f`
* un objet contenu dans une variable d'instance de `C`

### Principe du couplage faible

Lorsqu'un système est suffisamment découplé il est également plus souple et favorise la réutilisation. L'absence de couplage signifie que les éléments du sytème sont mieux isolés les uns des autres et du changement.

En réduisant le couplage nos classes adhèrent à un autre principe de conception appelé principe d'inversion des dépendances (Dependency Inversion Principle).

Un couplage artificiel correspond souvent à un couplage entre deux modules qui n'ont aucun rapport direct. Il résulte du placement d'une variable, d'une constante  ou du'une fonction dans un endroit commode sur le moment, mais finalement inadapté.

### Principe de séparation des préoccupations

> Les systèmes logiciels doivent séparer le processus de d"marrage, lorsque les objets de l'application sont construits et les dépendances sont établies, de la logique d'exécution qui vient ensuite.

### Principe de cohésion

Les classes doivent contenir un nombre réduit de variables d'instance. Lorsque chaque variable d'une classe est employée par chacune de ses méthodes la cohésion est maximale.

## C- Bonnes pratiques

### Envelopper les API tierces

Lorsque nous enveloppons une API tierce nous minimisons nos dépendances avec cette API : nous pouvons décider de changer de bibliothèque sans avoir à payer le prix fort. Par ailleurs, il est également plus facile de simuler les invocations d'une API ou d'un logiciel tiers lorsque nous testons notre propre code.

### Ne pas spéculer sur l'avenir

Notre code doit être pragmatique, non spéculatif. Il ne doit contenir que le nécessaire.

Voir aussi BDUF : _Big Design Up Front_. Pratique qui consiste à tout concevoir à l'avance avant d'implémenter quoi que ce soit : empêche de s'adapter aux changements en raison d'une résistance psychologique à la mise au rebut d'un travail antérieur et de la manière dont les choix architecturaux infuencent les réflexions ultérieures sur la conception.

### Commentaires

_Les commentaires doivent expliquer des choses que le code est incapable d'exprimer par lui-même._

_Si vous envisagez d'ajouter un commentaire, prenez le temps de vous assurer qu'il sagit du **meilleur** commentaire que vous pouvez écrire._

Les commentaires suivants ne devraient pas exister :

* commentaire contenant des métadonnées : date dernière modification, ...
* historique des modifications
* ancien code
* commentaire trivial ou redondant
* commentaire faux ou obsolète

### Conception

* Il ne doit pas y avoir plus d'une instruction `switch` pour un type donné de sélection. Les cas de cette instruction `switch` doivent crééer des objets polymorphes qui prennent la place d'autres instructions `switch` dans le reste du système.
* Il est contre-indiqué d'employer directement des nombres (ou chaînes) dans le code. Ils doivent être cachés derrière des constantes aux noms parfaitement évocateurs. Voir notion de [**magic number**](https://fr.wikipedia.org/wiki/Nombre_magique_(programmation)).
* Extrayer des fonctions qui expliques les intentions d'une expression conditionnelle.
* Les expressions conditionnelles doivent être données sous une forme positive (plus facile à lire).
* Interdir le couplage temporel : `fonc1` doit être appelée avant `fonc2` qui elle doit être appelée avant `fonc3` : les arguments de ces fonctions doivent être structurés de manière que leur ordre dans les appels soit évident.

### Classes

* Les classes de base ne doivent roen connaître de leurs classes dérivées.
* En déployant séparément les classes dérivées et les classes de base nous pouvons déployer nos systèmes sous forme de composants autonomes et indépendants : réduction de l'impact d'une modification et de la maintenance.

### Fonctions / Méthodes

* Le nombre d'arguments d'une fonction doit être aussi réduit que possible.
* Les arguments de sortie (entrée-sortie) sont tout sauf intuitifs. Si la fonction doit modifier un état ce doit être celui de l'objet sur lequel elle est invoquée.
* Les arguments bolléens mettent clairement en évidence que la fonction fait plusieurs choses. Ils sont déroutants et doivent être éliminés. Solution : faire plusieurs méthodes nommées correctement.
* Les méthodes qui ne sont jamais appelées doivent être retirées. La concervation du code mort coûte cher.
* Pour qu'une fonction soit lisible l'une des solutions les plus performantes consiste à décomposer les calculs en valeurs intermédiaires représentées par des variables aux noms significatifs.

### Rangement vertical

* Une fonction appelée doit se trouver en dessous d'une fonction qui l'appelle.
* Les variables et les fonctions doivent être définies au plus prês de leur utilisation.

### Style de formatage

Les développeurs de l'équipe doivent se mettre d'accord sur un même style de formatage et le respecter

## D- Projets

Les projets doivent pouvoir :

* être extraits rapidement et simplement (ex: `git clone http://....`)
* être construits rapidement et simplement (ex: `mvn clean install`)
* être testés rapidement et simplement


## E- Tests

### 3 lois du TDD : _Tests Driven Development_

1. Vous ne devez pas écrire un code de production tant que vous n'avez pas écrit un test unitaire d'échec
1. Vous devez uniquement écrire le test unitaire suffisant pour échouer : l'impossibilité de compiler est un échec
1. Vous devez uniquement écrire le code de production suffisant pour réussir le test d'échec courant

### Principes FIRST

1. **F**AST : (Rapide) : les tests doivent être rapides.
1. **I**NDEPENDENT (Indépendant) : les tests ne doivent pas dépendendre les uns des autres. Un test ne doit pas établir les conditions d'exécution du test suivant. Vous devez être en mesure d'exécuter chaque test indépendamment et dans l'ordre que vous voulez.
1. **R**EPEATABLE (Reproductible) : les tests doivent pouvoir être reproduits dans n'importe quel environnement.
1. **S**ELF-VALIDATING (Auto-validant) : les tests doivent avoir un résultat binaire : ils réussisent ou ils échouent. Vous ne devez pas avoir à consulter un fichier de journalisation ou comparer manuellement 2 fichiers.
1. **T**IMELY (au moment opportun) : les tests doivent être écrits au moment opportun : juste avant le code de production qui permet de les réussir.

### Autres grands principes

* Le code de test est aussi important que le code de production.
* Ce sont les tests unitaires qui permettent d'obtenir un code flexible, maintenable et réutilisable.
* Sans les tests chaque modification est un bogue potentiel : les tests permettent le changement. Les systèmes non testables ne sont pas vérifiables. Un système non vérifiable ne doit jamais êter déployé.
* Plus les tests sont négligés plus il est difficile de les modifier
* Plus le code de test est embrouillé plus le temps nécessaire à l'ajout de nouveaux tests dépassera celui nécessaire à écrire le nouveau code de production.
* La lisibilité est sans doute encore plus importante dans les tests unitaires qu'elle ne l'est dans le code de production.
* Rechercher chaque condition limite et écrivez le test correspondant.

### Tests d'apprentissage

Les tests d'apprentissage ne sont pas seulement gratuits, ils ont un retour sur investissement positif. Si de nouvelles versions du paquetage tiers sont publiées nous éx"cutons les tests d'apprentissage pour savoir s'il existe des différences de comportement.

### Structure d'un test : Build-Operate-Check

1. Constuire les données du test
1. Exploiter les données du test
1. Vérifier que l'opération a produit les résultats escomptés
