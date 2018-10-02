# Vue d'ensemble des principes _Clean Code_

_Synthèse des notions de Clean Code de [**Robert C. MARTIN**](https://fr.slideshare.net/MarwenMhamdi/coder-proprement) et autres recommandations._

## A- Principes S.O.L.I.D.

### SRP : _Single Responsibility Principle_

> Il ne doit exister qu'une et une seule raison de modifier une classe ou un module.

:link: [SRP](SRP.md)

### OCP : _Open-Closed Principle_

> Les classes doivent être ouvertes à l'extension mais fermées à la modification.

:link: [OCP](OCP.md)

Dans un système idéal nous incorporons de nouvelles fonctionnalités en étendant le système, non en modifiant le code existant.

### LSP : _Liskov Substitution Principle_

> Si **S** est un sous-type de **T**, alors tout objet de type **T** peut être remplacé par un objet de type **S** sans altérer les propriétés désirables du programme concerné.

:link: [LSP](LSP.md)

### ISP : _Interface Segregation Principle_

> Ne pas dépendre de fonctionnalités dont on n’a pas l’utilité.

:link: [ISP](ISP.md)

Respecter ce principe permet de réduire efficacement le couplage des classes entre elles.

### DIP : _Dependency Inversion Principle_

> L'inversion de contrôle déplace les responsabilités secondaires depuis un objet vers d'autres objets qui sont dédiés à chaque responsabilité et respecte ainsi le principe de responsabilité unique.

:link: [DIP](DIP.md)

## B- Lois, règles et autres principes

### DRY : _Don't Repeat Yourself_

> Principe qui consiste à éviter la redondance de code au travers de l’ensemble d’une application afin de faciliter la maintenance, le test, le débogage et les évolutions de cette dernière.

:link: [DRY](DRY.md)

### KISS : _Keep It Simple, Stupid_

> Principe dont la ligne directrice de conception qui préconise la simplicité dans la conception et que toute complexité non indispensable devrait être évitée dans toute la mesure du possible.

:link: [KISS](KISS.md)

### YAGNI : _You Ain't Gonna Need It_

> Ce principe indique de ne pas se baser sur d'hypothétiques évolutions futures pour faire les choix du présent.

:link: [YAGNI](YAGNI.md)

### Principe _Fail-Fast_

> Un système "Fail-Fast" a pour propriété de signaler le plus rapidement possible une erreur : s'il faut échouer, autant le faire le plus vite possible.

:link: <https://en.wikipedia.org/wiki/Fail-fast>

Avantages :

* Erreur d'origine non masquée ou perdue au milieu d'autres et permet la mise en évidence du responsable.
* Facilite l'analyse du problème.
* Evite les effets de bord et les problèmes d'incohérence.

### Principe de moindre surprise

> Toute fonction ou classe doit implémenter les comportements auxquels un autre programmeur peut raisonnablement s'attendre.

:link: <https://fr.wikipedia.org/wiki/Principe_de_moindre_surprise>

Exemples :

* Le code doit être placé là où le lecteur s'attend naturellement à la trouver.
* Les noms des fonctions doivent indiquer leur rôle, s'il faut examiner la documentation ou l'implémentation de la fonction pour connaître son rôle cela signifie qu'un meilleur nom doit être trouvé ou que la fonctionnalité doit être déplacée dans des fonctions ayant des noms appropriés.

### Loi de "LeBlanc" 

> Plus tard signifie jamais.

Exemples : 

* Commenter ou ignorer un test qui échoue et se dire que l'on fera en sorte qu'il réussisse plus tard.
* Remettre à plus tard l'écriture d'un test.
* Remettre à plus tard l'écriture de la documentation.

### Loi de "Déméter"

> Un module ne doit pas connaître les détails internes des objets qu'il manipule.

:link: [demeter](demeter.md)

### Règle du Boy-Scout

> Laisser le code plus propre qu'on ne l'a trouvé.

Exemples :

* Refactoring complet.
* Renommage simple d'une variable peu explicite.
* Amélioration d'un commentaire.
* Suppression d'un code mort ou commenté.
* ...

### Principe du couplage faible

> On parle de couplage faible, couplage léger ou couplage lâche si les composants échangent peu d'information.

Lorsqu'un système est suffisamment découplé il est également plus souple et favorise la réutilisation. L'absence de couplage signifie que les éléments du système sont mieux isolés les uns des autres et du changement.

En réduisant le couplage nos classes adhèrent à un autre principe de conception appelé principe d'inversion des dépendances (_Dependency Inversion Principle_).

Un couplage artificiel correspond souvent à un couplage entre deux modules qui n'ont aucun rapport direct. Il résulte du placement d'une variable, d'une constante  ou d'une fonction dans un endroit commode sur le moment, mais finalement inadapté.

### Principe de séparation des préoccupations (_Separation Of Concerns_)

> Des éléments n'ayant aucune relation conceptuelle dans un système n'ont pas à être modifiés en même temps.

> Les systèmes logiciels doivent séparer le processus de démarrage, lorsque les objets de l'application sont construits et les dépendances sont établies, de la logique d'exécution qui vient ensuite.

:link: [SOC](SOC.md)

### Principe de forte cohésion

> Les classes doivent contenir un nombre réduit de variables d'instance. Lorsque chaque variable d'une classe est employée par chacune de ses méthodes la cohésion est maximale.

:link: <https://fr.wikipedia.org/wiki/Coh%C3%A9sion_(informatique)>

:thumbsup: Une classe fortement cohésive a un nombre de méthodes relativement limitées, fortement liées d'un point de vue fonctionnel.

:thumbsdown: Une classe faiblement cohésive a un grand nombre de responsabilités dans différents domaines fonctionnels (voir ausi SRP).

## C- Bonnes pratiques

### Rangement vertical

* Une fonction appelée doit se trouver en dessous d'une fonction qui l'appelle.
* Les variables et les fonctions doivent être définies au plus près de leur utilisation.

### Style de formatage

Les développeurs de l'équipe doivent se mettre d'accord sur un même style de formatage et le respecter. Idéalement il est documenté et cette documentation facilement accessible. Par exemple : fichier `README.md` à la racine du dépôt GIT.

### Nommage

* Choisir des noms descriptifs : les noms représentent 90% de la lisibilité du code. Les noms doivent révéler les intentions.
* Les noms bien choisis doivent indiquer de manière non ambiguë le rôle d'une fonction ou d'une variable.
* Les noms bien choisis ont le pouvoir d'ajouter une description à la structure du code.
* Les noms doivent décrire les effets secondaires.
* Les noms sont plus faciles à comprendre lorsqu'ils se fondent sur une convention ou un usage établi. Par exemple un _Design Pattern_.
* La longueur d'un nom doit être liée à sa portée. Les variables et les fonctions dont les noms sont courts perdent leur signification avec l'éloignement. Par conséquent plus la portée d'un nom est étendue plus ce nom doit être long et précis.
* Eviter la codification ou notification hongroise (utilisation de préfixes par exemple).
* Choisir un mot par concept : établir un lexique et s’y tenir pour conserver une cohérence sur l'ensemble de application.
* Eviter de mélanger différentes langues dans le même nom de classe, méthode ou variable. Exemples : readFichier, countLignes.

### Commentaires

_Les commentaires doivent expliquer des choses que le code est incapable d'exprimer par lui-même._

_Si vous envisagez d'ajouter un commentaire, prenez le temps de vous assurer qu'il sagit du **meilleur** commentaire que vous pouvez écrire._

_Les commentaires mentent, vieillissent très mal, ne sont pas refactorables, ... : ce sont des aveux de faiblesses, à utiliser un bon nom correct, à faire un découpage, etc ..._

Les commentaires suivants ne devraient pas exister :

* commentaire contenant des métadonnées : date dernière modification, ...
* historique des modifications
* ancien code
* commentaire trivial ou redondant
* commentaire faux ou obsolète
* commentaire mal placé (déplacement avec le temps et donc n'ayant plus aucun sens la où il se trouve)

### Documentation

La documentation doit vivre avec le produit. La première documentation, et de fait toujours à jour, est les tests.

### Conception

* Il ne doit pas y avoir plus d'une instruction `switch` pour un type donné de sélection. Les cas de cette instruction `switch` doivent créer des objets polymorphes qui prennent la place d'autres instructions `switch` dans le reste du système.
* Il est contre-indiqué d'employer directement des nombres (ou chaînes) dans le code. Ils doivent être cachés derrière des constantes aux noms parfaitement évocateurs. Voir notion de [**magic number**](https://fr.wikipedia.org/wiki/Nombre_magique_(programmation)).
* Extrayez des fonctions qui expliquent les intentions d'une expression conditionnelle.
* Les expressions conditionnelles doivent être données sous une forme positive (plus facile à lire).
* Interdir le couplage temporel : `fonc1` doit être appelée avant `fonc2` qui elle doit être appelée avant `fonc3` : les arguments de ces fonctions doivent être structurés de manière que leur ordre dans les appels soit évident.
* _Big Design Up Front_. Pratique à éviter qui consiste à tout concevoir à l'avance avant d'implémenter quoi que ce soit : empêche de s'adapter aux changements en raison d'une résistance psychologique à la mise au rebut d'un travail antérieur et de la manière dont les choix architecturaux influencent les réflexions ultérieures sur la conception.

### Classes

* Les classes de base ne doivent rien connaître de leurs classes dérivées.
* En déployant séparément les classes dérivées et les classes de base nous pouvons déployer nos systèmes sous forme de composants autonomes et indépendants : réduction de l'impact d'une modification et de la maintenance.
* Les classes ne doivent pas hériter des constantes (Interface regroupant des constantes).

### Fonctions / Méthodes

* Le nombre d'arguments d'une fonction doit être aussi réduit que possible.
* Les arguments de sortie (entrée-sortie) sont tout sauf intuitifs. Si la fonction doit modifier un état ce doit être celui de l'objet sur lequel elle est invoquée.
* Les arguments booléens mettent clairement en évidence que la fonction fait plusieurs choses. Ils sont déroutants et doivent être éliminés. Solution : faire plusieurs méthodes nommées correctement.
* Les méthodes qui ne sont jamais appelées doivent être retirées. La conservation du code mort coûte cher.
* Pour qu'une fonction soit lisible l'une des solutions les plus performantes consiste à décomposer les calculs en valeurs intermédiaires représentées par des variables aux noms significatifs.

### Exceptions

* Bien sur les fonctions ne doivent pas utilsier de codes retour, mais des exceptions typées en cas d'erreur.
* Les exceptions doivent être traitées au niveau de la couche la plus haute.
* Eviter de retourner `null`.
* Log : on ne trace pas à la création de l'exception, ni en plein milieu du code.
* Sécurité : ne pas afficher de contexte ou de stacktrace à un utilisateur final.

### Envelopper les API tierces

Lorsque nous enveloppons une API tierce nous minimisons nos dépendances avec cette API : nous pouvons décider de changer de bibliothèque sans avoir à payer le prix fort. Par ailleurs, il est également plus facile de simuler les invocations d'une API ou d'un logiciel tiers lorsque nous testons notre propre code.

## D- Projets

Les projets doivent pouvoir :

* être extraits rapidement et simplement (ex: `git clone http://....`)
* être construits rapidement et simplement (ex: `mvn clean install`)
* être testés rapidement et simplement

## E- Tests

### 3 lois du TDD : _Tests Driven Development_

1. Vous ne devez pas écrire un code de production tant que vous n'avez pas écrit un test unitaire d'échec.
1. Vous devez uniquement écrire le test unitaire suffisant pour échouer : l'impossibilité de compiler est un échec.
1. Vous devez uniquement écrire le code de production suffisant pour réussir le test d'échec courant.

### Principes F.I.R.S.T.

1. **F**AST : (Rapide) : les tests doivent être rapides. Un test lent est un test qui risque de ne plus être exécuté.
1. **I**NDEPENDENT (Indépendant) : les tests ne doivent pas dépendre les uns des autres. Un test ne doit pas établir les conditions d'exécution du test suivant. Vous devez être en mesure d'exécuter chaque test indépendamment et dans l'ordre que vous voulez.
1. **R**EPEATABLE (Reproductible) : les tests doivent pouvoir être reproduits dans n'importe quel environnement.
1. **S**ELF-VALIDATING (Auto-validant) : les tests doivent avoir un résultat binaire : ils réussisent ou ils échouent. Vous ne devez pas avoir à consulter un fichier de journalisation ou comparer manuellement 2 fichiers.
1. **T**IMELY (au moment opportun) : les tests doivent être écrits au moment opportun : juste avant le code de production qui permet de les réussir.

### Autres grands principes

* Le code de test est aussi important que le code de production.
* Ce sont les tests unitaires qui permettent d'obtenir un code flexible, maintenable et réutilisable.
* Sans les tests chaque modification est un bogue potentiel : les tests permettent le changement. Les systèmes non testables ne sont pas vérifiables. Un système non vérifiable ne doit jamais être déployé.
* Plus les tests sont négligés plus il est difficile de les modifier.
* Plus le code de test est embrouillé plus le temps nécessaire à l'ajout de nouveaux tests dépassera celui nécessaire à écrire le nouveau code de production.
* La lisibilité est sans doute encore plus importante dans les tests unitaires qu'elle ne l'est dans le code de production.
* Rechercher chaque condition limite et écrivez le test correspondant.
* Les tests restent insuffisant tant qu'il existe des conditions qui n'ont pas été explorées ou des calculs qui n'ont pas été validés.
* Chaque test doit se contenter de valider une et une seule fonctionnalité : un concept par test.
* Un test qui ne peut pas échouer est un test qui ne sert à rien.

### Tests d'apprentissage

Les tests d'apprentissage ne sont pas seulement gratuits, ils ont un retour sur investissement positif. Si de nouvelles versions du paquetage tiers sont publiées nous exécutons les tests d'apprentissage pour savoir s'il existe des différences de comportement.

### Structure d'un test : Build-Operate-Check (ou Given-When-Then)

1. Construire les données du test.
1. Exploiter les données du test.
1. Vérifier que l'opération a produit les résultats escomptés.
