# Software Craftsmanship

## Historique

:pushpin: [Le Manifeste](http://manifesto.softwarecraftsmanship.org/#/fr-fr)

:information_source: 2009 : mise en place du "Manifesto for Software Craftsmanship" très fortement inspiré du Manifeste Agile et par le livre "The Pragmatic Programmer" publié en 1999 par Andrew Hunt et David Thomas. (avec pour base l'eXtreme Programming).

Synthèse :

* Avec l'orienté objet et DDD, nous pouvons modéliser le métier de nos clients.
* Avec l'agile, nous pouvons faire le minimum de logiciel suffisant pour les satisfaire.
* Avec les pratiques XP, nous garantissons que le logiciel est maintenable et qu'il fonctionne dans tous les cas prévus.

## La culture

Leitmotiv : élever le niveau, atteindre un haut niveau de qualité

* Le _Software Craftsmanship_ est donc plutôt considéré comme une culture qu'une méthode à proprement parler, une culture de la qualité logicielle.
* La non qualité a un coût stratégique, mais aussi financier : une application truffée de défauts sera toujours plus coûteuse à faire évoluer, et les clients qui n'ont plus confiance risquent de ne plus vouloir payer. Il faut donc réduire le périmètre mais pas la qualité.
* Diffuser la culture de la qualité : binômage, Kata, Coding Dojo, Brown Bag Lunch, revues de code, ...  essentiellement tirées de XP (eXtreme Programming).
* Insuffler un état d'esprit dans l'équipe.

## Concepts

* Une solution doit être bien conçue techniquement mais également doit pouvoir d'évoluer rapidement.
* Remettre l'accent sur les pratiques d'ingénierie logicielle et d'excellence technique.
* Tout comme connaître une langue ne fait pas de vous un écrivain à succès, connaître un langage informatique ne fait pas automatiquement de vous un bon développeur.

## L'humain

* La non qualité a un coût humain : travailler dans ce cadre devient vite démotivant, notamment pour les développeurs, au risque de voir les meilleurs partir dans une autre entreprise.
* Certains ont adopté ces valeurs, sont souvent passionnés par leur métier : coder n'est pas qu'un moyen de gagner sa vie mais un moyen de transmettre sa vision, de donner du sens à son métier (envisager son métier comme une passion ou un art).
* Beaucoup d'autres développeurs n'ont que peu ou pas conscience qu'on peut réaliser des logiciels autrement.
* Développeur est une carrière à part entière, à opposer à un changement de carrière en devenant par exemple manager, architecte ou chef de projet.
* Les qualités les plus fréquentes et appréciées étant le savoir-faire, l'engagement et le pragmatisme.
* Le mouvement souhaite que tous les acteurs du métier deviennent professionnels et que cela deviennent la norme.
* Il faut s'appuyer sur un Tech Lead qui va aider l'équipe à progresser jusqu'à ce qu'elle devienne autonome.

## Les valeurs

* Professionnalisme : mettre en œuvre toutes les pratiques connues pour être les meilleures chacune dans leur contexte, pour écrire et entretenir du code.
* Favoriser la collaboration et la communication entre les différents acteurs afin d'assurer la cohérence du projet, c'est une communauté qui partage, s'accompagne, s'entraide.
* Pragmatisme : on ne cherche pas absolument la perfection, on cherche à faire au mieux en tenant compte du contexte.
* Chercher à apprendre, encore et toujours (démarche d'amélioration continue).
* Le logiciel doit être simple, économique et efficace avant tout. Ensuite on peut faire beau bien écrit et bien architecturé.
* Toutes ces valeurs doivent être partagées.

## Les moyens

### Les techniques

* **Test First** : Écriture d'un test unitaire avant l'implémentation
* **Test-Driven Development (TDD)** : basé sur _Test First_ mais ajoute la notion de cycle _Red/Green/Refactor_
* **Continuous Integration**
  * vérifier et remonter rapidement le code produit
  * mesurer la qualité
  * construction du livrable
* **Pair Programming**
  * partage de la connaissance métier et technique
  * plusieurs points de vue confrontés en permanence
  * chacun apprend des techniques et de l'expérience de l'autre
* **Refactoring** : Revoir de manière continue la conception et la lisibilité du code en vue de son amélioration
* **Code review** : par un équipier, par l'ensemble de l'équipe ou bien par un œil externe
  * permet de partager la connaissance avec toute l'équipe, et de faire émerger des critiques constructives afin de retravailler le code en conséquence
  * permet d'obtenir un retour (_feedback_) rapide
* **Behavior Driven Development (BDD)**
  * L'art de rédiger de façon collaborative (métier + développeurs + testeurs) les spécifications d'une application
  * Les scénarios sont illustrés à l'aide de cas précis
  * Permet de favoriser la compréhension des fonctionnalités par tous
  * On utilise généralement le langage _Guerkin_ (exemple avec l'outil _Cucumber_)
* **Domain Driven Design (DDD)** : L'ensemble du code doit être conçu, organisé et écrit, en vue de refléter le domaine pour lequel il existe

### Recevoir

#### Formation

* **Veille technologique**
  * participation à des événements
  * suivi de sites web, blogs, news
  * suivi des leaders d'influence de l'IT (Twitter, ...)
  * mise en oeuvre des _getting started_
* **Mentorat, tutorat**
  * accompagnement par des personnes expérimentées
  * partage des connaissances
* **e-Learning, MOOC (Massive Open Online Courses)**
* **Lecture d'ouvrages**

#### Événements

* Coding games, quizzes
* Hackathon : challenge d'innovation proposant de développer un logiciel en équipe, dans un délai imparti
* [Coding Dojos](coding-dojos.md) (Kata, Randori)
* Brown Bag Lunch
* Meetups
* Conférences (Devoxx, Mix-IT, Breizh Camp, DevFest, ...)

### Partager

* Rédaction d'articles
* Mentorat, tutorat
* Proposer et animer des formations, des Kata ou Coding Dojo

## Liens

* [Blog et Podcast Artisant développeur](http://artisandeveloppeur.fr/)
* [Blog Octo](https://blog.octo.com/software-craftsmanship-une-culture-a-transmettre/)
* [Blog Le Touilleur Express](http://www.touilleur-express.fr/2011/01/20/craftsmanship/)
* [Le Software Craftsmanship, pour la professionnalisation du métier de développeur](http://www.arolla.fr/blog/2014/12/le-software-craftsmanship-pour-la-professionnalisation-du-metier-de-developpeur/)
* [Être Craftsman, c'est un état d'esprit](https://www.novencia.com/craftsman-presentation/)
* [Site d'Arnaud Lemaire / Lilobase](https://www.lilobase.me/)

## Livres

* :gb: Uncle Bob - The Clean Coder
* :gb: [Sandro Mancuso - The Software Craftsman](https://blog.cellenza.com/software-craftsmanship/analyse-the-software-craftsman-sandro-mancuso/)
* :gb: [Andrew Hunt et David Thomas - The Pragmatic Programmer](https://en.wikipedia.org/wiki/The_Pragmatic_Programmer)

---
:point_left: [Retour à l'accueil](README.md)
