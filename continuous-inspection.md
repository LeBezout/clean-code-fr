# Inspection continue

## Principes et enjeux

Le but de l'inspection continue, initiée par la société [_SonarSource SA_](https://www.sonarsource.com/), est de répondre aux problématiques posées par les revues humaines. Ces revues :

* ne sont pas assez exhaustives
* sont subjectives
* interviennent trop tardivement
* n'impliquent pas assez les acteurs

L'inspection continue (donc outillée) permet :

* d'être exécutée régulièrement (lors d'un _push_ sur le SCM par exemple)
* d'obtenir un _feedback_ très rapide voire immédiat pendant que le code est encore _chaud_ dans les esprits
* d'impliquer les développeurs dans un cercle vertueux d'apprentissage et d'amélioration continue
* d'impliquer les développeurs dans un effort commun
* d'offrir des tableaux de bord et de mesurer l'évolution au fil du temps
* d'obtenir des mesures sur la base de code complète ainsi que sur le nouveau code (différentiel)
* d'être objective car basée sur des règles et bonnes ou mauvaises pratiques connues

:bulb: L'inspection continue est donc à mettre en place **dès le début d'un projet**, ce qui est très facile avec des outils comme _GitLab-CI_.

## Ressources

* [SonarSource White Paper](https://www.sonarsource.com/resources/white-papers/continuous-inspection.html)
* [SonarQube](https://www.sonarqube.org/features/clean-code/)
