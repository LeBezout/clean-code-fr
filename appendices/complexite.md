# Notions de complexité

On distinguera essentiellement 2 notions de complexité :

* la [complexité essentielle](https://fr.wikipedia.org/wiki/Complexit%C3%A9_essentielle)
* la [complexité accidentelle](https://fr.wikipedia.org/wiki/Complexit%C3%A9_accidentelle)

## Complexité essentielle

> La complexité essentielle relative à un problème, généralement dans le cadre d'un projet informatique, désigne le degré de complexité minimal d'un programme pour résoudre un problème ou appliquer une solution.

C'est sensé être uniquement la complexité du métier sous-jacent. **Celle-ci ne peut en aucun cas être réduite.**

## Complexité accidentelle

> En développement logiciel le terme complexité accidentelle désigne la complexité introduite dans des programmes informatiques non en raison de la complexité du problème, mais de manière accidentelle en raison de choix de développement non pertinents.

## Maîtriser la complexité

Cette complexité doit être réduite et **à défaut il faut la maîtriser** car très coûteuse sur le long terme, par exemple via :

* Décomposition
* Abstractions
* Application de _Design Patterns_
* Application du principe KISS
* Application du principe de couplage faible / modularité
* Application du principe d'orthogonalité
* Pas d'_over-engineering_, d'optimisation prématurée, de fonctionnalités "au cas où"
* _Refactoring_ régulier

---
:point_left: [Retour à l'accueil](README.md)
