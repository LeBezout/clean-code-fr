# Les revues de code

## A- Les avantages des revues de code

:pushpin: _La pratique de la revue de code a un coût mais qui est largement amorti plus tard. C'est un investissement rentable et une pratique essentielle à la bonne qualité et à la durabilité du produit développé._

### L'équipe : renforcer la propriété collective

* Le code _n'appartient_ plus qu'à une personne et est maintenable par plusieurs développeurs.
* Implication de tous les développeurs.
* Partager / transmettre la connaissance du sujet.
* Facilite l'apprentissage (nouveau dans l'équipe, nouveau sur la technologie, etc ...).
* Renforce la cohérence et la cohésion (de l'équipe et du code).

### Le produit : assurer une meilleure qualité et moins de bugs

* Détection des défauts au plus tôt (et donc à moindre coût).
* Apporter un regard nouveau, critique.
* Provoquer des échanges, des débats, des analyses (émulation dans l'équipe).
* Éviter la dégradation progressive du code.

## B- Les types de revues

:pushpin: _Différents types de revues peuvent être utilisés._

* Le binômage (_pair-programming_) : _feed-back_ immédiat.
* Les _Merge Requests_ ou _Pull Requests_.
* Les revues par un pair.
* Les revues collectives.

:bulb: Ces techniques peuvent (doivent) être complémentaires.

## C- Les clefs pour réussir les revues de code

:pushpin: _Les revues de code se préparent et doivent respecter quelques pré-requis pour être réellement efficaces. De plus comme toute technique c'est en la pratiquant régulièrement qu'on l'optimise et que l'on s'améliore individuellement et collectivement._

### Le relecteur : être bienveillant

* Critiquer le code, pas le développeur (dissocier le code de la personne).
* Employer "je" ou "on" et pas "tu".
* Valoriser les bons points constatés (montrer les points positifs).

### Le relecteur : apporter des critiques constructives

* Critiquer le fond, pas la forme (pour çà il y a des outils pour automatiser). Attention, la forme n'inclue pas le respect des normes, la lisibilité ou la maintenabilité.
* Être le plus clair, précis et explicite possible (pas d'ironie, d'ambiguïté).
* N'apporter que des commentaires constructifs en proposant des solutions ou des alternatives.
* Ne pas aller trop vite, il faut prendre le temps d'analyser, utiliser une _checklist_ par exemple.
* Ne pas penser que l'on n'est pas forcément légitime, chaque point de vue est bon à prendre et à considérer.
* Favoriser également, en plus des commentaires, les échanges de vive voix.

### Le relu : préparer la revue

Pour faire gagner du temps au relecteur et pour l'orienter :

* Revoir son code avant de soumettre :
  * respect des normes internes
  * respect du style (indentation, nommage, ...)
  * respect des principes SOLID
  * pas de violations Sonarqube
  * code lisible et compréhensible
  * présence de tests...utiles
* Commenter les choix techniques.
* Pointer (et éventuellement décrire) les éléments fondamentaux devant être validés ou partagés
  * expliquer **quoi** et **pourquoi**
  * ... et pas obligatoirement le **comment**

### Le relu : être reconnaissant

* Ne pas prendre les remarques pour soi.
* Considérer les remarques comme des moyens d'amélioration continue, d'apprentissage.
* Se rappeler que la personne qui a commenté le code a pris de son temps dans le but d'améliorer le produit développé.
* Répondre à TOUS les commentaires.
* Expliquer ses choix d'implémentation "à priori" pour orienter le relecteur.
* Ne soumettre à la revue que du code finalisé et fonctionnel ... mais pas forcément complet (ne pas forcément attendre la fin du développement de la fonctionnalité).

### L'équipe : avoir un soutien fort de son management

* Le management doit être convaincu des apports et bénéfices des revues, il doit soutenir et encourager cette pratique.
* Le management ne doit pas intervenir ou participer aux revues, c'est uniquement réservé aux sachants _techniques_.
* Le management ne doit pas utiliser les revues à des fins de _reporting_ ou de contrôle (rappel : on ne s'occupe que du code pas des personnes).

### L'équipe : impliquer tout le monde

* Initier la pratique dès le début du projet, ne pas attendre.
* Rendre les revues systématiques (présente dans les _Definition of Done_ / votre _WorkFlow_ / votre processus de développement)
* Ne pas corriger / modifier à la place du développeur initial (c'est l'auteur qui corrige les défauts relevés, via _pair-programming_ si besoin, permet de le responsabiliser).
* Il faut éviter que cela soit toujours les mêmes personnes qui effectuent les revues (par exemple les _tech lead_ ou les plus expérimentés).
* S'alerter si régulièrement les revues débouchent sur la détection d'aucun défaut : manque d'implication ? de temps ? de confiance ?

## D- Les clefs pour optimiser les revues

### Qui

Les Tech Lead mais aussi tous les développeurs. Un Tech Lead doit revoir le code d'un développeur mais l'inverse est également vrai.

L'aspect partage des connaissances (appropriation collective) et des techniques (montée en compétences en maturité) est un apport majeur de la pratique des revues de code.

### Limiter le périmètre et le champ d'action

* La revue ne doit pas se substituer aux contrôles outillés. On se concentre alors uniquement sur les vérifications qui nécessitent une intervention humaine que l'on pourrait difficilement automatiser.
* Pour les revues collectives limiter la durée et désigner un modérateur et un gardien du temps.
* Limiter la taille des _Merge Requests_ ou _Pull Requests_ ou du code à revoir : trop de code à revoir = risque de louper des choses (découragement, passer trop vite, ...). Petite revue = meilleure efficacité, plus de pertinence.
* Limiter le périmètre : une _Merge Request_ ou _Pull Request_ pour une seule fonctionnalité.
* Les standards / normes / ... doivent être partagés, **validés**, accessibles et connus de tous et maintenus par tous. Ce qui permet :
  * d'éviter de se répéter et donc gagner du temps (de revue et de développement).
  * d'éviter les conflits.
* Consacrer les revues à la détection des défauts, pas à leur correction ni à la génération de débats, qui doivent avoir lieu séparément.

### Contrôler / outiller

* Faire un suivi des défauts constatés pour éviter de les retrouver de revue en revue.
* S'appuyer également sur les rapports des revues outillées (couverture, résultats des tests, ...).

### Combiner les techniques

* Binômage : retour immédiat.
* Tests automatisés, TDD, ...
* Inspection continue avec des outils comme _Sonarqube_.
* Revue collectives : partage de la connaissance.
* Revue par des pairs : regard nouveau.

## E- Les pistes à explorer lors de la revue

* [ ] Le bon nommage (clair, explicite, approprié, ...).
* [ ] Taille des classes et méthodes et nombres de paramètres.
* [ ] Respect des principes SOLID et autres principes _clean code_.
* [ ] Pas d'_Over Design_, _Over Engineering_ et respect du principe YAGNI.
* [ ] Pas de redondance, de copier-coller.
* [ ] Code au bon endroit, où on est sensé s'attendre à le trouver.
* [ ] Présence et pertinence des tests.
* [ ] Présence et pertinence des commentaires et de la Javadoc.
* [ ] Un niveau et des traces de log adaptés et pertinents.
* [ ] Gestion des erreurs et des exceptions.
* [ ] Pas de `switch` ou de blocs `if-elseif ...` abusifs (souvent signe d'un mauvais _design_ où l'héritage et le polymorphisme devraient plutôt être utilisés).
* [ ] Le paramétrage (tout ce qui peut changer : soit en fonction des besoins, soit en fonction des environnements) doit être externalisé.
* [ ] Adaptation au domaine métier (vocabulaire, contexte borné, ...).
* [ ] Les structures de données utilisées sont adaptées au besoin (Ex : pas de `LinkedList` pour des accès direct à un indice donné).

## F- Revue de code _versus_ Audit de code

L'audit de code est généralement réalisé par une personne externe à l'équipe voir parfois externe à l'entreprise.

De plus généralement ce type d'audit intervient souvent trop tard dans le cycle de vie du projet/produit ne permettant pas une remontée rapide et donc une prise en compte rapide des informations par les différents acteurs.

Enfin l'auditeur ne dispose bien souvent que de très peu d'éléments historiques ou de contexte ou des contraintes liés au projet/produit/entreprise pour pouvoir juger des choix techniques ou méthodologiques rencontrés. L'avis exprimé est donc subjectif et basé sur l'expérience et l'avis personnel de l'auteur de la revue.

Cette méthode peut être utilisée dans des cas spécifiques ou des compétences pourraient à manquer :

* audit de sécurité
* tests de performance
* validation d'une solution ou d'un choix technique

:bulb: Le classement par efficacité pourrait ressembler à :

1. Revue collective
1. Pair-Programming
1. Revue par un pair
1. Revue externe (audit)

... d'où l'intérêt de combiner les méthodes.

## G- Annexes

* :fr: Vidéos : [Playlist Youtube](https://www.youtube.com/playlist?list=PLM5oYKLr93VlE4Oq7KrZUGHObWEWV1rRX)
* :gb: Article : [How to Make Your Code Reviewer Fall in Love with You](https://mtlynch.io/code-review-love/)

---
:point_left: [Retour à l'accueil](../README.md)
