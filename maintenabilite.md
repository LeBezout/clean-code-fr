# Maintenabilité

La maintenabilité qui est la capacité du programme à être modifié sans que les fonctions existantes ne soient altérées et sans perte de temps.
On peut parler aussi d'évolutivité. On pourra également rajouter la capacité du logiciel à être testé facilement, la présence, l'ajustement et la qualité de la documentation ou encore le fait d’éviter de mélanger le code métier et le code technique.

:warning: **C'est le critère sur lequel il faut mettre l'accent en priorité**.

## Checklist d'évaluation

Imaginons la situation suivante, un nouveau développeur arrive sur le projet pouvons-nous lui apporter :

* [ ] la documentation fonctionnelle du projet
* [ ] la documentation technique du projet (comment installer, configurer, préparer son poste de travail, ...)
* [ ] les normes internes à respecter
* [ ] le dictionnaire des des données ou un glossaire ou une description des acronymes utilisés
* [ ] les moyens de versionner son code (système de gestion de versions : Git)
* [ ] les moyens de tester son code (environnement, jeux de données, cas de test)
* [ ] les moyens de suivre la qualité de son code (IDE, inspection continue, ...)
* [ ] les moyens d'accompagnement et de montée en compétence sur le métier et les techniques
* [ ] du support technique sur les technologies utilisées

## Indicateurs de maintenabilité

* [ ] organisation, lisibilité, indentation et mise en forme générale
* [ ] nommage et uniformisation via le respect des conventions de codage
* [ ] couplage minimum (modules indépendants)
* [ ] complexité cyclomatique minimale
* [ ] présence de documentation, commentaires
* [ ] dette technique maîtrisée
