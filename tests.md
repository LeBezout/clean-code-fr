# Les tests

## Règles fondamentales

* :warning: **Tester le plus tôt, le plus possible et le plus souvent possible.**
* :warning:  **Les tests sont un pré-requis obligatoire au refactoring car ils permettent de savoir si l’on a cassé ou non des fonctionnalités.**
* :warning:  **Le moindre échec dans les tests unitaires / d'intégration doit bloquer obligatoirement la construction de l’application.**
* :warning:  **Ce sont les tests unitaires qui permettent d'obtenir un code flexible, maintenable et réutilisable.**
* :warning:  **Aucune dépendance externe ne doit être sollicitée : base de données, serveur SMTP, accès réseau (HTTP, NAS, ...) ou bien encore de la date système par exemple.**

## Pourquoi faire des tests

Seuls les tests peuvent garantir :

* un bon niveau de qualité
* un résultat conforme aux attentes
* la non régression (refactoring, nouvelle fonctionnalité)

Les tests offrent également :

* un retour rapide en cas de problème
* un aspect documentaire (c’est une documentation vivante et toujours à jour)
* un gain de temps (pas besoin de redéployer entièrement l’application)

## Structure d'un test : Build-Operate-Check

... ou _Given-When-Then_ ... ou _Arrange-Act-Assert_

1. _Build : Construire les données du test.
1. _Operate_ : Exploiter les données du test.
1. _Check_ : Vérifier que l'opération a produit les résultats escomptés.

## Principes F.I.R.S.T.

1. **F**AST : (Rapide) : les tests doivent être rapides. Un test lent est un test qui risque de ne plus être exécuté.
1. **I**NDEPENDENT (Indépendant) : les tests ne doivent pas dépendre les uns des autres. Un test ne doit pas établir les conditions d'exécution du test suivant. Vous devez être en mesure d'exécuter chaque test indépendamment et dans l'ordre que vous voulez.
1. **R**EPEATABLE (Reproductible) : les tests doivent pouvoir être reproduits dans n'importe quel environnement.
1. **S**ELF-VALIDATING (Auto-validant) : les tests doivent avoir un résultat binaire : ils réussissent ou ils échouent. Vous ne devez pas avoir à consulter un fichier de journalisation ou comparer manuellement 2 fichiers.
1. **T**IMELY (au moment opportun) : les tests doivent être écrits au moment opportun : juste avant le code de production qui permet de les réussir.

## Des tests de qualité

* Le code de test est aussi important que le code de production.
* La lisibilité est sans doute encore plus importante dans les tests unitaires qu'elle ne l'est dans le code de production.
* Plus les tests sont négligés plus il est difficile de les modifier.
* Plus le code de test est embrouillé plus le temps nécessaire à l'ajout de nouveaux tests dépassera celui nécessaire à écrire le nouveau code de production.
* Le code doit être pensé et écrit de façon à ce qu’il soit naturellement et unitairement testable.
* Chaque test doit se contenter de valider une et une seule fonctionnalité : un concept par test.
* Chaque test doit avoir un nom clair sur le principe de `should_XXXXX_If_YYYYYYY`.

## Des tests qui testent

* Un test qui ne peut pas échouer est un test qui ne sert à rien.
* Sans les tests chaque modification est un bogue potentiel : les tests permettent le changement. Les systèmes non testables ne sont pas vérifiables. Un système non vérifiable ne doit jamais être déployé.
* Rechercher chaque condition limite et écrivez le test correspondant.
* Les tests restent insuffisant tant qu'il existe des conditions qui n'ont pas été explorées ou des calculs qui n'ont pas été validés.

---
:point_left: [Retour à l'accueil](README.md)
