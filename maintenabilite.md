# Maintenabilité

La maintenabilité qui est la capacité du programme à être modifié sans que les fonctions existantes ne soient altérées et sans perte de temps.
On peut parler aussi d'évolutivité. On pourra également rajouter la capacité du logiciel à être testé facilement, la présence, l'ajustement et la qualité de la documentation ou encore le fait d’éviter de mélanger le code métier et le code technique.

:warning: **C'est le critère sur lequel il faut mettre l'accent en priorité**.

## Indicateurs de maintenabilité générale

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

## Indicateurs de maintenabilité du code

* [ ] lisibilité : organisation, indentation et mise en forme générale
* [ ] homogénéité : nommage et uniformisation via le respect des conventions de codage
* [ ] couplage minimum (modules indépendants)
* [ ] complexité cyclomatique minimale
* [ ] présence de documentation, commentaires
* [ ] dette technique maîtrisée

:information_source: Le développeur passe plus de temps à lire du code qu'à en écrire. Il est donc important de rendre celui-ci le plus **lisible** possible, notamment en exprimant clairement les intentions.

## Bonnes pratiques

### L'importance du nommage

* Favoriser toujours le confort de lecture par rapport au confort d'écriture.
* Choisir des noms qui **révèlent les intentions**.
* Évidemment les noms de classes représentent des concepts : on utilise des noms, groupes nominaux.
* Évidemment les noms de méthodes représentent des actions : on utilise des verbes, ou groupes verbaux.
* Évidemment ne pas de mélanger différentes langues dans le même nom.
* Adapter le nommage des variables : plus le _scope_ d'une variable est large plus son nom doit être long et informatif.
* Utiliser plutôt des suffixes (`*DAO` que `DAO*`). Dans tous les cas respecter le choix et ne pas mélanger.
* **Choisir un mot par concept :** statuer et documenter (document de normes, lexique) sur les termes à employer et ne pas employer différents termes pour exprimer la même chose. Exemples :
  * Lire : `query`, `find`, `select`, `fetch`, `retrieve`, ...
  * Mettre à jour : `update`, `modify`, `merge`, `replace`, ...
  * Classe de gestion : `*Helper`, `*Manager`, `*Handler`, ...
  * Outils : `*Tool`, `*Tools`, `*Util`, `*Utils`, ...
  * pire parfois on peut mélanger les concepts : `*Client`, `*Proxy`, `*Stub`, `*Mock`, `*Fake`

### L'importance de la documentation

* Elle permet de poser les normes et lever les ambiguïtés.
* Elle permet d'accompagner les nouveaux arrivants.
* Elle permet de rafraîchir la mémoire des différents acteurs.
* Elle renforce l'autonomie.
* Elle force le développeur à expliquer son programme, ses choix et donc à se poser des questions, et parfois à se remettre en question en levant des par exemple des manques ou des incohérences.
