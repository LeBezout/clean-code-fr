# Les tests

## Règles fondamentales

* :warning: **Tester le plus tôt, le plus possible et le plus souvent possible.**
* :warning: **Les tests sont un pré-requis obligatoire au _refactoring_ car ils permettent de savoir si l’on a cassé ou non des fonctionnalités.**
* :warning: **Le moindre échec dans les tests unitaires / d'intégration doit bloquer obligatoirement la construction de l’application.**
* :warning: **Ce sont les tests unitaires qui permettent d'obtenir un code flexible, maintenable et réutilisable.**
* :warning: **Aucune dépendance externe ne doit être sollicitée : base de données, serveur SMTP, accès réseau (HTTP, NAS, ...) ou bien encore de la date système par exemple.**
* :warning: **S'interdire tout _refactoring_ ou tout déploiement en continu s'il n'y a pas de tests pour valider.**

## Pourquoi faire des tests

Seuls les tests peuvent garantir :

* un bon niveau de qualité.
* un résultat conforme aux attentes.
* la non régression (refactoring, nouvelle fonctionnalité).

Les tests offrent également :

* un retour rapide en cas de problème.
* un aspect documentaire (c’est une documentation vivante et toujours à jour).
* un gain de temps (pas besoin de redéployer entièrement l’application).
* parfois une mise en évidence d'un mauvais design ou une remise en question.

Extraits de la publication d'Octo _Culture DevOps Vol. 3 :_

* Écrire un test c’est faire un investissement en temps.
* Coder consistant essentiellement à prendre une succession de décisions, il est impératif de travailler à avoir une boucle de feed-back la plus rapide possible. Personne ne peut décemment penser déployer en continu du code qui ne
serait pas suffisamment testé.
* Vous assurez également la production d’une documentation via votre code de test. Si l’on se demande quel résultat est censée produire telle ou telle partie, les tests en utilisant des cas et des valeurs concrètes, nous apporterons une réponse plus fiable qu’un document Word ou PDF obsolète.
* Un pipeline qui n’exécute (presque) aucun test perd environ 99 % de son intérêt. **Il permet juste d’envoyer plus vite des bugs en production**. Pas de tests, pas de qualité. Pas de qualité, pas de confiance. Pas de confiance, pas de prod.
* Plus un test est rapide (à développer et à exécuter), plus il sera exécuté souvent, plus il aura de la valeur.

## Comment faire des tests

### Typologie des tests

**Pyramide des tests** : Tests unitaires -> Tests d'intégration / tests d'API -> Tests End to End (bout en bout) -> Tests de charge, tests de sécurité.

Chaque type de test apporte son niveau de protection.

### Structure d'un test : Build-Operate-Check

... ou _Given-When-Then_ ... ou _Arrange-Act-Assert_

1. _Build_ : Construire les données du test.
1. _Operate_ : Exploiter les données du test.
1. _Check_ : Vérifier que l'opération a produit les résultats escomptés.

### Caractéristiques F.I.R.S.T.

1. **F**AST : (Rapide) : les tests doivent être rapides. Un test lent est un test qui risque de ne plus être exécuté.
1. **I**NDEPENDENT (Indépendant) : les tests ne doivent pas dépendre les uns des autres. Un test ne doit pas établir les conditions d'exécution du test suivant. Vous devez être en mesure d'exécuter chaque test indépendamment et dans l'ordre que vous voulez.
1. **R**EPEATABLE (Reproductible) : les tests doivent pouvoir être reproduits dans n'importe quel environnement.
1. **S**ELF-VALIDATING (Auto-validant) : les tests doivent avoir un résultat binaire : ils réussissent ou ils échouent. Vous ne devez pas avoir à consulter un fichier de journalisation ou comparer manuellement 2 fichiers.
1. **T**IMELY (au moment opportun) : les tests doivent être écrits au moment opportun : juste avant le code de production qui permet de les réussir (voir Test First ou TDD) ... ou **T**HOROUGH (approfondis/précis) : les tests doivent explorer l'essentiel des possibilités en utilisant des cas négatifs et positifs.

### Des tests de qualité

* Le code de test est aussi important que le code de production.
* La lisibilité est sans doute encore plus importante dans les tests unitaires qu'elle ne l'est dans le code de production.
* Plus les tests sont négligés plus il est difficile de les modifier.
* Plus le code de test est embrouillé plus le temps nécessaire à l'ajout de nouveaux tests dépassera celui nécessaire à écrire le nouveau code de production.
* Le code doit être pensé et écrit de façon à ce qu’il soit naturellement et unitairement testable.
* Chaque test doit se contenter de valider une et une seule fonctionnalité : un concept par test.
* Chaque test doit avoir un nom clair sur le principe de `should_XXXXX_If_YYYYYYY`.

### Des tests qui testent

* Un test qui ne peut pas échouer est un test qui ne sert à rien.
* Sans les tests chaque modification est un bogue potentiel : les tests permettent le changement. Les systèmes non testables ne sont pas vérifiables. Un système non vérifiable ne doit jamais être déployé.
* Rechercher chaque condition limite et écrivez le test correspondant.
* Les tests restent insuffisants tant qu'il existe des conditions qui n'ont pas été explorées ou des calculs qui n'ont pas été validés.

## Test First & Test Driven Development

Le principe du _développements pilotés par les tests est d'écrire les tests avant le code de production. Test-First est issu des pratiques de l'_eXtreme Programming_, TDD rajoute la notion d'itération et de remise en forme (_refactoring_ : Red->Green->Refactor).

### Les 3 lois du TDD

1. Vous ne devez pas écrire un code de production tant que vous n'avez pas écrit un test unitaire d'échec.
1. Vous devez uniquement écrire le test unitaire suffisant pour échouer : l'impossibilité de compiler est un échec.
1. Vous devez uniquement écrire le code de production suffisant pour réussir le test d'échec courant.

### Avantages du TDD

* Réduction du nombre d'anomalies et des régressions.
* Évite la sur-ingénierie.
* C'est une bonne documentation associée au code et toujours à jour.
* Implique de-facto une couverture du code à 100%.

## Dummy, Fake, Stub, Mock, Spy, bouchon, substitut, simulacre

Dans tous les cas ce sont des objets (classes, implémentations, ...) qui ne sont jamais utilisés dans le code de production, des outils pour le code de test. Néanmoins on peut imaginer, en production, des _fallback_ (solution alternative, solution de repli) utilisant des bouchons.

* **Dummy** : Variable ou méthode fantoche :
  * le contenu ou le comportement n'importe pas.
  * le contenu ou le comportement n'influe pas sur le résultat du test.
* **Fake** : Faux-objets
  * Souvent des objets aux capacités limités.
  * Peut être un _stub_ ou _mock_.
* **Stub** : ébauche
  * Permet de remplacer une dépendance existante et non primordiale pour le test.
  * Peut être configuré pour les besoins du test.
  * **_On ne fait aucune assertion sur ces objets_**.
  * Sont utilisés dans la partie _Given_.
* **Mock** : Objet simulé (simulacre)
  * C'est un _stub_ sur lequel on va pouvoir faire des assertions.
  * Sont utilisés dans la partie _When_ et _Then_.
* **Spy** : C'est également un substitut à une implémentation réelle

:gb: [Martin Fowler - Mocks Aren't Stubs](https://www.martinfowler.com/articles/mocksArentStubs.html)

:fr: [Benoît Sautel - Mock ou pas mock ?](https://www.fierdecoder.fr/2015/11/mock-ou-pas-mock/)

:warning: Les définitions peuvent variées il est donc conseillé de définir et de s'accorder sur une définition commune au sein de l'équipe.

## Property Based Testing

Contrairement aux tests basés sur les exemples, le _Property-based Testing_ a pour finalité de tester le comportement du code et non le résultat retourné par celui-ci.
Un test de propriété testera une implémentation avec des valeurs constamment différentes (générées).

Cette technique permet de compléter les tests unitaires, où d'en remplacer certains.

Ressources vidéos :

* :fr: [Devoxx 2021 - Property based testing : de la théorie à la pratique (Nicolas Dubien)](https://www.youtube.com/watch?v=oeaXWvTHyxc) - 30min
* :fr: [Devoxx 2016 - Property-Based Testing, enfin pour tout le monde (Cyrille Martraire - Romeu MOURA)](https://www.youtube.com/watch?v=O-LWbSUaEQU) - 2h24
* :fr: [AFUP Day 2020 - Du test à la preuve: introduction au Property Based Testing (Baptiste Langlade)](https://www.youtube.com/watch?v=uUxGngqsER0) - 22min

## La checklist de validation d'un bon test

Un bon test doit se conformer aux 10 principes suivants :

* [ ] Le test possède un nom évocateur (ou  une description via par exemple `@DisplayName` pour JUnit).
* [ ] Le test est écrit dans le format _Arange/Act/Assert_ (ou _Given/When/Then_) afin d'assurer sa lisibilité et sa maintenabilité.
* [ ] Le test ne valide qu'une seule chose (mais il peut contenir plusieurs assertions).
* [ ] Le test n'est pas un doublon d'un autre (teste la même chose), en d'autres termes il permet d'augmenter la couverture de code.
* [ ] Le test est auto-portant, il n'a besoin d'aucune dépendance externe à son contexte (BDD, service REST, ...) et il ne valide pas inutilement de code externe supposé respecter le comportement qu'on attend de lui.
* [ ] Le test respecte les **caractéristiques FIRST : FAST**, il est rapide à s'exécuter (ou à échouer).
* [ ] Le test respecte les **caractéristiques FIRST : INDEPENDENT**, il ne dépend pas de l'exécution d'un autre test .
* [ ] Le test respecte les **caractéristiques FIRST : REPEATABLE**, il doit pouvoir être exécuté plusieurs fois en retournant toujours le même résultat.
* [ ] Le test respecte les **caractéristiques FIRST : SELF-VALIDATING**, il passe ou échoue de façon automatique, aucune action humaine ne doit être nécessaire pour le valider.
* [ ] Le test respecte les **caractéristiques FIRST : THOROUGH**, il explore toutes les possibilités (ou il fait partie d'un ensemble permettant de traiter tous les cas possibles).

## Pour aller encore plus loin dans la pratique des tests

* [PITest](http://pitest.org/), [Stryker Mutator](https://stryker-mutator.io/) : _Mutation Testing System._
* [Stan4j](http://stan4j.com/download/ide/) : _The dependency graph of packages or components should have no cycles._
* [ArchUnit](https://www.archunit.org/) : _Unit Test your Java Architecture._
* [jQAssistant](https://jqassistant.org/) : _Definition and validation of project specific rules on a structural level._
* [Infinitest](https://infinitest.github.io/) : _Each time you change the code Infinitest runs the relevant tests for you!_

---
:point_left: [Retour à l'accueil](../README.md)
