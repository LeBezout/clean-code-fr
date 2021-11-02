# Notions de dette technique et de pourriture

:pushpin: Concept introduit par Ward Cunningham en 1992 et qui précise que la dette technique permet de prendre des raccourcis afin d'aller plus vite dans l'élaboration de la solution mais avec une perspective obligatoire de remboursement de celle-ci.

C'est un concept qui est à ne pas confondre avec celui de pourriture (détérioration du code).

* Cette dégradation est **volontaire** ou **intentionnelle** pour une période déterminée et son _remboursement_ est déjà planifié **c'est de la dette technique**.
* Cette dégradation est **assumée** sans intention de la rembourser **ce n'est donc pas de la dette technique, c'est de la pourriture**.
* Cette dégradation est **inconsciente** (dans le pire des cas ou )les intervenants ne mesurent même pas son ampleur) **ce n'est donc pas de la dette technique, c'est de la pourriture**.

La pourriture est donc l'accumulation de risques impliqués par les choix techniques effectués tout au long de la vie d'un projet.
Autrement dit c'est l'ensemble des choix que l'on fait et qui provoqueront des **contraintes** et des **coûts** ultérieurs.

C'est une menace omniprésente qui peut à tout moment mettre en péril un projet, par exemple l'accumulation de risques ou l'absence de respect des bonnes pratiques de conception et de développement.

## Détection de la pourriture

### Quotidiennement

* Peur de modifier une partie du code.
* Des difficultés pour ajouter de nouvelles fonctionnalités.
* Les chiffrages évolutifs anormalement élevés pour une partie du code.
* Les temps de développement sont de plus en plus long (forte baisse de vélocité).
* Les régressions sont en augmentation et les bugs sont de plus en plus fréquents.
* Seules certaines personnes sont capables de maintenir une partie du code ou pire, la connaissance s'est perdue avec le temps ou les changements de personnes.

### Technologiquement

* Utilisation de technologies obsolètes (frameworks, composants applicatifs, ...).
* Absence de montée de version des dépendances et framework.
* Absence de montée de version des serveurs d'applications ou web.
* Absence de montée de version des infrastructures.
* Absence d'outillage et d'automatisation du packaging.
* Absence d'outillage du poste de travail.
* Application Web ne fonctionnant que sur un seul type de Browser Web (exemple IE8).

### Méthodologiquement

* Mauvais choix d'architecture ou architecture obsolète.
* Non-respect des normes et standards.
* Pas ou peu de documentation (techniques et fonctionnelle).
* Pas ou peu d’intégration continue.
* Pas ou peu de contrôles qualité (SonarQube, selenium, ...).
* Pas ou peu de tests unitaires / tests automatisés.
* Pas ou peu de revue de code régulières.
* Duplication de fonctionnalités d'un composant dans un autre ou tout autre duplication.

## Risques identifiés

* Baisse de vélocité avec l'augmentation de la taille de la base de code.
* La pourriture s'accroît tout au long de la vie du projet.
* Des temps de développement de plus en plus long, une augmentation des régressions et des bugs de plus en plus fréquents.
* Le coût de la dette augmente jusqu'à un point où il n'est plus possible de la rembourser intégralement.
* La pourriture s'accroît tout au long de la vie du projet.

## Ressources

* Vidéo : [Software Crafts·wo·manship - Dette technique et entropie du logiciel (Arnaud Lemaire)](https://www.youtube.com/watch?v=VKe9EE4MUxk) - 1h40
* Vidéo : [La dette technique, est-ce une fatalité ? (Mickael Wegerich)](https://www.youtube.com/watch?v=C2COBA4EFrM) - 30min.

---
:point_left: [Retour à l'accueil](../README.md)
