# Fiche synthèse : Software Craft : TDD, Clean Code et autres pratiques essentielles

Livre - 288 pages - DUNOD - Cyrille MARTRAIRE, Arnaud THIEFAINE, Dorra BARTAGUIZ, Fabien HIEGEL, Houssam FAKIH

![couverture](https://www.dunod.com/sites/default/files/styles/principal_desktop/public/thumbnails/image/9782100825202-001-X.jpeg)

:link: <https://www.dunod.com/sciences-techniques/software-craft-tdd-clean-code-et-autres-pratiques-essentielles>

- [1- Les pratiques incontournables du craft](#partie-1--les-pratiques-incontournables-du-craft)
- [2- Techniques avancées et élargissements](#partie-2--techniques-avanc%C3%A9es-et-%C3%A9largissements)
- [3- Craft et attitudes](partie-3--craft-et-attitudes)

## Avant-propos

Le _Software Craft_ est un ensemble d'attitudes qu'on apprend à adopter pour être plus efficace sur la façon d'utiliser les technologies, quelles qu'elles soient. Ce qui est remarquable avec les attitudes c'est qu'elles sont bien plus pérennes que les technologies sur lesquelles on les applique.

Le vrai enjeu du développement logiciel est de rester évolutif dans la durée.

En insistant sur l'excellence technique, le risque est de dériver vers l'élitisme, mais le _Software Craft_ inclut l'antidote qui est l'importance de la transmission des savoirs-faire.

## PARTIE 1 : Les pratiques incontournables du craft

### Le Développement Dirigé par les Tests (TDD)

Le TDD n'est pas une technique de test mais bien une technique de développement et de conception.

Nommage du test : lorsque la règle de gestion est exprimée avec précision, on peut facilement déterminer la cause de l'échec du test. (formalisme : Should XXX When YYYY).

Écriture du test : il vaut mieux commencer par la vérification.

Étape verte : c'est un peu difficile de se contraindre à écrire une seule ligne de code alors qu'on voit probablement d'avance l'implémentation finale.

"Kata" : _de la répétition de la pratique naît la perfection_.

Les tests deviennent notre harnais de sécurité contre les régressions qui peuvent venir se glisser dans le code par inadvertance.

Le respect scrupuleux du TDD garantit une couverture totale.

### Techniques et principes de propreté de code (Clean Code)

#### Être exemplaire

Michael FEATHERS estime que la qualité majeure du code est de donner l'impression d'être écrit par quelqu'un qui fait attention à la qualité de son travail.

L'être humain a une propension au laisser-aller face à un environnement dégradé, et qu'à l'inverse il éprouve des scrupules à ne pas respecter les règles dans un environnement sain.

- théorie de la vitre brisée
- règle du boy-scout

Il faut appliquer un principe de tolérance zéro : dès qu'on se met à s'autoriser des négligences qu'on estime acceptables, on ouvre la porte à des négligences futures plus graves.

Les tests sont la vitrine du code, et leur qualité se doit d'être exemplaire.

#### Design

D'une manière générale :

- on doit chercher à guider les développeurs qui vont reprendre notre code après nous, à réduite leur charge mentale de façon qu'ils puissent se concentrer sur l'essentiel.
- le code ne devrait pas paraître plus complexe que le problème métier qu'il cherche à résoudre.

Les 4 règles simples pour un design simple :

- passer les tests
- révéler l'intention
- éviter la duplication
- rester petit

Selon J.B. RAINSBERGER les règles essentielles du design simple ne seraient plus que 2 :

- améliorer le nommage
- réduire la duplication

#### Nommage

Il faut faire preuve d'un lâcher-prise dans la recherche de noms parfaits, en gardant à l'esprit qu'un nom n'a rien de définitif.

Les 4 étapes de renommage préconisées par Kent BECK :

- Nonsense (sans signification)
- Accurate but vague (ciblé mais vague)
- Precise (précis)
- Intention revealing (révélant l'intention)

Un nommage erroné ou approximatif peut induire en erreur et engendrer la création de bugs.

#### Structuration

Garder les niveaux d'abstraction en tête et les matérialiser aide à raisonner sur une quantité réduite de code, donc à moindre effort.

Les fonctions :

- Une fonction ne doit faire qu'une seule chose.
- On devrait consider que tous les paramètres d'entrée sont immuables.
- Les fonctions traitant le problème principal devraient se situer en tête du fichier source.
- Aucune fonction ne devrait être définie plus haut qu'une fonction qui l'appelle.

L'aspect visuel du code :

- il est bien formaté.
- le niveau maximum d'indentation est limité.
- les lignes de code ne sont pas très larges.
- il est normé (encodage, retour chariot, formatage, imports)

#### Commentaires ... optionnels

- considérer les commentaire avec méfiance.
- il existe suffisamment de moyens d'exprimer l'intention par le code pour pouvoir se passer des commentaires.
- les commentaires ne sont pas du code, ils souffrent de tous les travers inhérents de la documentation (décalage avec le réel, obsolescence).
- le fait de ne s'autoriser que les commentaires réellement utiles donne à chacun d'entre eux une plus grande valeur.

#### DRY

- Nombre de développeurs adoptent un style de programmation par mimétisme.
- Le démon du copier-coller est une addiction dont vous devez absolument vous débarrasser pour produire du code de bonne qualité.
- Mais ... lorsque l'on assemble plusieurs morceaux de code en apparence semblables en une unique abstraction, on crée un couplage entre eux.
- Plus le périmètre est restreint, et plus il est conseillé de réduire la duplication, parce que la portée du couplage introduit reste limitée.

#### Conclusion

L'écriture de code de qualité ne se fait pas en un seul jet, c'est un processus itératif par la pratique du refactoring.

### Les spécifications agiles avec le développement dirigé par le comportement (BDD)

#### 3 amigos

Co-construction :

- La présence simultanée des 3 rôles permet d'optimiser les échanges dans une posture de co-construction d'égal à égal.
- Il est important de rappeler qu'aucun rôle n'est subordonné à un autre.

Il vaut mieux ne pas dépasser 4 (voire 5) afin d'éviter de compliquer les échanges.

#### Gherkin : Given-When-Then, exécutable sous forme de tests automatisés

- sous forme de critère d'acceptation en phase de développement initial
- sous forme de tests de non-régression ultérieurement
- compréhension partagée par tous
- c'est une documentation vivante et à jour

### BDD

BDD est une pratique qui ne nécessite pour démarrer que de rassembler des personnes de bonne volonté dans un atelier de spécifications.

### Collaborer efficacement avec le pair & mob programming

Adopter une attitude de partage et de don de ses connaissances est important, parce que par mimétisme, les autres personnes de l'équipe auront tendance à faire de même.

Le Mob Programming reste un formidable outil pédagogique lors de formations et ateliers. Son efficacité pour apprendre ou pour aligner les pratiques de code, de conception, d'architecture, de connaissance du métier ou de documentation n'est plus à démonter.

### L’importance des techniques de refactoring

Le _refactoring_ consiste à retravailler un code source sans en modifier le comportement, afin d'en améliorer la lisibilité et de le rendre beaucoup plus facile à maintenir et propice à accueillir des évolutions.

La présence d'une couverture de tests suffisamment solide pour garantir que les améliorations de code se font en toute sécurité : nous sommes capables de vérifier de façon fiable si nous avons cassé quelque chose.

Dette technique : plus l'équipe emprunte, plus elle réduit sa capacité à délivrer de la valeur à l'avenir.

C'est certainement le soin apporté au nommage qui apporte le plus de valeur à une base de code.

Il faut veiller à ne pas pousser les abstractions trop loin : trop de généricité peut, d'une part, rendre le code moins facile à comprendre, et, d'autre part, le rendre moins évolutif parce qu'il devient utilisé par beaucoup trop de monde.

Le soin qui est apporté aux signatures de méthodes est déterminant pour l'évolutivité et la compréhension du code.

Un code qui est écrit comme une fonction pure, c'est à dire que pour chaque ensemble de paramètres en entrée on attend une valeur en sortie bien déterminée, est beaucoup plus facile à tester et donc à réécrire.

Le code de test est ce qui va servir de point d'entrée pour tout nouvel arrivant, et il peut offrir une valeur documentaire élevée.

Pratiquer le _refactoring_ est une forme d'hygiène du code.

### Travailler avec du code legacy

Les projets "legacy" sont la plupart du temps les plus sensibles sur le plan financier : ceux qui ont le plus de valeur pour le métier et donc ceux qui rapportent le plus d'argent.

On essaye de restreindre l'effort à fournir en délimitant soigneusement notre périmètre d'intervention.

Avec du _code legacy_, la sécurisation du parcours s'obtient en écrivant les tests qui manquent.

Il est important de se concentrer sur les réécritures qui apportent une réelle valeur.

Tout nouveau test augmentant le score de couverture se montrera pertinent mais la couverture de test comporte une faiblesse importante : elle mesure seulement les lignes de code qui sont exécutées par les tests, indépendamment du résultat.

La couverture optimale de tests représente un filet de sécurité appréciable qui permet, en libérant l'esprit du risque de régression, d'expérimenter et de tenter des actions de _refactoring_ plus audacieuses.

Michael FEATHERS : notion de "seam" : on cherche à identifier des _coutures_ dans le code, c'est-à-dire des points précis où on peut intervenir sans modifier significativement le code de production.

Une difficulté récurrente lorsqu'on réécrit du _code legacy_ est de s'enfermer dans des optimums locaux, avec des _refactorings_ satisfaisants au premier abord mais qui empêchent de s'aventurer plus loin.

L'idée essentielle est, lorsqu'on souhaite apporter une évolution, de mettre en place les conditions propices au changement, notamment grâce aux techniques de refactoring, et de pouvoir ainsi apporter facilement le changement souhaité.

Une fois que la couverture du code par les tests paraît satisfaisante, nous disposons d'un filet de sécurité qui nous permet de procéder à la phase de refactoring en toute sérénité.

### Étude détaillée du kata Fraction

Mise en oeuvre des 4 règles de design simple.

## PARTIE 2 : Techniques avancées et élargissements

### Principes et outils pour tester efficacement

Caractéristiques F.I.R.S.T. :

- F pour fast : il est important de s'assurer que chaque test est suffisamment véloce, afin de ne pas pénaliser l'ensemble de la suite de tests.
- I pour isolated/independent : on doit pouvoir lancer les tests individuellement, en parallèle et dans n'importe quel ordre d'exécution, et garantir que cela n'a aucun impact sur le résultat.
- R pour repeatable (reproductible) : il doit s'exécuter comme un système fermé sans accès à des ressources extérieures.
- S pour self-verifying (auto-validant) : le résultat doit être outillé et sauter aux yeux, sans requérir une intervention humaine pour comprendre ou interpréter le résultat.
- T pour Timely ou Thorough : opportun et/ou précis : il est préférable de les séparer en se limitant à un test par scénario.

Les doublures de tests :

- Dummy object : variable fantoche
- Test Stub
- Test Spy
- Mock Object
- Fake Object : composant factice, c'est une implémentation réelle mais simplifiée de la vraie classe, une sorte de simulateur. Ils demandent une logique spécifique et font partie des cas pour lesquels il est préférable d'écrire un substitut à la main que de passer par une bibliothèque.

L'utilisation des bibliothèques de substitutions (ex: Mockito) est rarement simple et une utilisation efficace nécessite d'en comprendre les principes, mécanismes et limitations.

Il est plus prudent de ne substituer que les objets qu'on maîtrise  : "ne substituer que le code dont vous êtes propriétaire".

Les niveaux de tests :

- Test unitaire
- Test d'intégration (tests étroits / tests de grande envergure)
- Test de bout en bout (end to end = e2e)
- Test exploratoire

En plus des données utiles pour les tests, on pourrait choisir parfois de prévoir des données qu'on appelle des "données parasites". Les tests n'ont pas besoin de ces données pour être exécutées, mais leur présence permet de simuler au plus près la production.

Chaque type de test apporte son niveau de protection.

### Outils et techniques avancées de TDD

Une _User Story_ doit respecter les caractéristiques I.N.V.E.S.T. :

- Independent / Indépendante
- Negotiable / Négociable
- Valuable / Apporte de la valeur
- Estimable
- Small / Petite
- Testable

Découpage en arbre de fonctionnalités :

- TDD inside-out : approche _Bottom Up_ (Chicago School ou classic approach)
- TDD outside-in : approche _Top Down_ (London School ou mockist approach)

ATDD (_Acceptance Test Driven Development_) : généralement on n'utilise pas de substituts pour ce test ou on minimise leur utilisation aux frontières de notre système.

ATDD = indicateur de fin de développement (quand il passe au vert).

TDD "_as if you meant it_" : commencer par mettre tout le code dans le corps de la méthode de test.

TPP (_Transformation Priority Premise_) : le meilleur moyen pour rester en mode _baby step_ est d'appliquer les transformations priorisées proposées par Robert MARTIN.

### Techniques de conception

- Principes S.O.L.I.D. :
  - Single Responsibility Principle
  - Open-Closed Principle
  - Liskov Substitution Principle
  - Interface Segregation Principle
  - Dependency Inversion Principle
- Composition over inheritance
- Faible couplage et forte cohésion
- Principe de dépendance du spécifique vers le générique : le code le plus stable ne doit pas dépendre de code moins stable (le générique ne doit jamais dépendre du spécifique).
- Loi de Demeter (principe de connaissance minimale) : limiter ce qu'on expose, notamment les détails d'implémentation.
- Principe du "_Tell Don't Ask_" : au lieu de demander les données à un objet pour les manipuler et les modifier, il est préférable de fournir directement les abstractions qui permettent d'effectuer des actions de plus haut niveau. (POJO ou DTO sont juste des structures clef/valeur de luxe).
- Principe d'Hollywood "_Don't call us, we'll call you_" : lié au principe d'inversion de contrôle (IoC) : réaction à des évènements : callback, hook, ... Le style fonctionnel aide à renforcer ce principe.
- Le jeu de contraintes "_Object Calisthenics_" : 9 règles de Jeff BRAY, un code qui applique ces règles tend naturellement à être respectueux de la plupart des autres principes théoriques :
  - _Only one level of indentation per method_ : permet de favoriser le découpage et de réduire l'éparpillement du contexte.
  - _Don't use the 'else' keyword_ : sortir plus tôt de la méthode, _fail-fast_, ...
  - _Wrap all primitives and strings_ : sécurise le code en masquant les détails d'implémentation. En encapsulant les données et en exposant des comportements.
  - _First class collections_ : permet de rapprocher le traitement des données qu'il manipule.
  - _One dot per line_ : on peut facilement substituer le comportement des objets amis ou voisins pour tester unitairement la fonctionnalité voulue.
  - _Don't abbreviate_ : favorise l'expression de l'intention en nommant explicitement les notions métier.
  - _Keep all entities small_ : design plus simple et meilleure lisibilité donc meilleure maintenabilité.
  - _No classes with more than two instance variables_ : renforce l'encapsulation.
  - _No getter/setters_ : on tend vers des objets immuables (simplicité, thread-safe, robustesse).
- Code smells courants :
  - Code complexe ou omniscient
  - Données globales partagées
  - Primitive obsession
  - Commentaire honteux
  - Litanie de paramètres
  - Mutation des paramètres d'une méthode (effet de bord)
  - Données muables
- Design Patterns :
  - Switchs multiples vers le pattern strategy.
  - Boucles visibles vers le pattern composite.
  - Vérification de nullité vers le pattern Null Object.

### Transformation de code à caractère architectural

- Découpler un lien navigable (association) (DDD et notion d'agrégat).
- Architecture hexagonale et inversion de dépendance.
- Style réactif orienté chorégraphie (plutôt que l'orchestration) et pattern Observer.
- Stateful -> stateless.
- Service idempotent.

## PARTIE 3 : Craft et attitudes

### Introduire le craft dans votre contexte

Code retreat : (retraites de code) : évènement sur une journée où les participants répètent six fois le même kata, en TDD et binôme, mais avec à chaque fois des contraintes différentes. C'est une expérience incontournable.

Initier une dynamique consiste à lancer des actions plutôt modestes, mais régulièrement (dont l'effet cumulé suscitera l'intérêt).

Il faut être centré sur la livraison de valeur :

- Se rappeler les objectifs du craft pour recentrer aussi notre attention sur la livraison de valeur.
- Ne pas consacrer une part excessive de temps de travail sur sur l'amélioration du code en négligeant la livraison de valeur.
- Toute initiative d'amélioration doit rester subordonnée à des bénéfices attendus et avérés.

Transférer les compétences fait partie intégrante du craft, mais dans une approche bienveillante avec des collègues qui en ont manifesté l'envie.

### Au-delà des pratiques, un état d’esprit

Tout le monde pourrait devenir expert dans une discipline, à condition de pratiquer régulièrement et intensément. La répétition et la pratique engendre des effets positifs.

Il faut être suffisamment curieux pour maintenir ses connaissances à jour.

L'intérêt des katas :

- réside surtout dans l'opportunité d'acquérir, par la répétition, certains réflexes qui vont s'appliquer naturellement sur un vrai projet.
- réside aussi dans la capacité d'aborder le même problème de plusieurs façons.

La veille : on nous demande de renforcer continuellement nos connaissances et expertises. La veille ne peut se faire qu'en sacrifiant une partie de notre temps personnel, il est donc important de bien cibler les sujets.

La transmission : la majeur partie de notre savoir faire provient des autres,  il apparaît juste et naturel, à notre tour, et en fonction de nos capacités, de transmettre nos compétences aux autres. Avec des bénéfices non négligeables :

- amélioration progressive des conditions de travail avec des bases de code de plus en plus propres et faciles à maintenir.
- construction d'une communauté de bonnes pratiques.
- bénéficier du savoir-faire des autres.
- amélioration personnelle, nous forçant à consolider nos connaissances.
- satisfaction personnelle.

L'accompagnement par l'exemple, en "pairant", en "mobbant" ou en effectuant des revues de code bienveillantes, est beaucoup mieux accepté.

En se cantonnant dans notre zone de confort on perd le sel de ce qui fait notre métier : renouvellement permanent des techniques et pratiques.

L'expérimentation et l'échec font partie de la réussite.

Surconfiance : effet Dunning-Kruger : biais cognitif par lequel les personnes découvrant un domaine pourraient surestimer leur compétence. Corollaire : les personnes les plus expertes auraient tendance à minimiser leurs compétences, en pensant que ce qui est facile pour elles l'est forcément pour les autres.

Le craft se distingue aussi bien par ses savoirs-faire que par ses valeurs éthiques telles que l'humilité, la bienveillance et le partage.

Plus on gagne en expérience et en sagesse et plus on prend conscience de l'étendue de notre ignorance.

L'humilité est un moteur qui va nous inciter à nous améliorer continuellement, à viser l'excellence et à faciliter nos interactions avec les autres.

On peut s'autoriser à féliciter quelqu'un en public mais les _feedbacks_ négatifs ne devraient être délivrés qu'en tête à tête.

Dans un contexte bienveillant, chacun va pouvoir progresser avec l'aide des autres et pouvoir se sentir mieux.

Le rôle de "Tech Lead", s'il peut être attribué explicitement par un manager, s'obtient dans de nombreux cas par la reconnaissance des pairs,  il donne l'exemple en aidant les autres, il préfère convaincre plutôt que d'imposer et il ne craint pas que d'autres tiennent aussi ce rôle.

Être pragmatique revient à savoir faire les bons compromis pour maximiser les chances de réussite d'un projet sur le court, moyen et long terme.

Être développeur, au-delà d'être bon technicien, c'est avant tout être un bon communicant (échanger et collaborer). La communication entre développeurs est essentielle (prodiguer des feedbacks).

### Craft 2.0

Le craft correspond aux pratiques nécessaires pour atteindre la maturité.

---
:point_left: [Retour à l'accueil](../README.md)
