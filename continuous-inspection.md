# Inspection continue

Les contrôles qualité ont pour principal intérêt de pouvoir remonter le plus rapidement possible des informations sur le produit en cours de développement afin de permettre à l’équipe de réagir tout aussi rapidement afin de minimiser les impacts. Un problème découvert trop tard peut avoir des conséquences en termes de budget, de délai ou d’image vis à vis des clients. Le coût peut en effet être multiplié par 5 si le défaut est détecté après la mise en production du produit.

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

:warning: Il est également évidemment dangereux de considérer que l'on peut se reposer uniquement sur cette pratique. Il faut bien sur la compléter avec les techniques de revue de code "humaines" : collectives et par des pairs.

## Outillage

Nombre d'outils sont disponibles (directement ou non) pour remonter rapidement aux développeurs des indicateurs sur la qualité du code produit :

* Les remontées d'informations directement dans l'IDE (soit nativement soit via des plugins type _SonarLint_ ou _FindBugs_).
* Les contrôles de compilation et de succès des tests lors d'un _push_ (via _Jenkins_, _GitLab CI_, ...).
* Les contrôles outillés quotidiens via _SonarQube_ (qui ajoutent en plus un suivi temporel grâce aux _Dashboards_).
* Les analyses via des outils d'APM : l’_Application Performance Monitoring_ suit les transactions de bout en bout permettant la remontée d'informations et de métriques de toutes sortes.

### Les outils SonarQube et SonarLint

#### SonarQube

_SonarQube_ (anciennement _sonar_ et à ne pas confondre avec _SonarJ_) édité par la société _SonarSource SA_ est le standard du marché dans le domaine de l'analyse de la qualité du code d'une application et supporte plus d'une vingtaine de langages.
_SonarQube_ définit 3 catégories de violations :

* *Bugs :* Bug avéré ou du code manifestement erroné ou très susceptible de générer un comportement inattendu.
* *Vulnérabilités :* provenant de code potentiellement vulnérable à l'exploitation par les pirates.
* *Mauvaises pratiques (_Code Smells_) :* provenant de code qui va dégrader la maintenabilité, la robustesse ou la performance. Elles sont mesurées et affichées principalement en termes de temps qu'elles prendront pour être corriger.

_SonarQube_ définit également pour chaque anomalie relevée un niveau de criticité parmi 5, du plus au moins important :

* *Bloquant*  (_blocker_) : anomalie à corriger immédiatement.
* *Critique* (_critical_) : anomalie à corriger rapidement.
* *Majeur* (_major_) : anomalie à étudier, une correction planifiée est souhaitable.
* *Mineur* (_minor_) : anomalie à prendre en compte si possible (souvent facile à corriger).
* *Informatif* (_info_) : anomalie à prendre en compte si possible (souvent facile à corriger).

Enfin l'outil peut même amender automatiquement les _merge request_ (via [un plugin](https://github.com/gabrie-allaigre/sonar-gitlab-plugin)), les violations étant visibles dès lors directement dans GitLab.

#### Sonarlint

_SonarLint_ du même éditeur est un _plugin_ disponible pour différents IDE (Eclipse, IntelliJ IDEA, VS Code, ...) permettant d'avoir un retour immédiat (_Fix issues before they exist_) lors de l'écriture du code (donc avant le commit) sans devoir attendre de lancer une analyse _SonarQube_.

:warning: Comme tout outil, ils peuvent produire des faux-positifs, il conviendra d'analyser les rapports et anomalies relevées avec un esprit critique et ne pas se _jeter_ forcément sur tout. Dans le doute vous pouvez solliciter les équipes support.

#### Tableau comparatif

| Langage | Feedback immédiat dans l'IDE | Feedback asynchrone via l'inspection continue |
| ------- | ---------------------------- | --------------------------------------------- |
| Java | SonarLint (Eclipse,  IntelliJ, VS Code) | SonarQube |
| Java | EclEmma (Eclipse) | JaCoco |
| Java | Snyk Vulnerabilities Scanning (InteliJ) | OWASP Dependency Check |
| Shell | ShellCheck (extension VS Code) | ShellCheck + SonarQube |
| Javascript | JSHint (extension VS Code) | SonarQube |
| Typescript | TSLint (extension VS Code) | ? |

## Ressources

* :gb: [SonarSource White Paper](https://www.sonarsource.com/resources/white-papers/continuous-inspection.html)
* :gb: [SonarQube](https://www.sonarqube.org/features/clean-code/)
