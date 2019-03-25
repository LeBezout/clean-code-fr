# Les revues de code

## Les avantages des revues de code

_La pratique de la revue de code a un coût mais qui est largement amorti plus tard. C'est un investissement rentable._

### Renforcer la propriété collective

* Le code _n'appartient_ plus qu'à une personne et est maintenable par plusieurs développeurs
* Implication de tous les développeurs
* Partager / transmettre la connaissance du sujet
* Facilite l'apprentissage (nouveau dans l'équipe, nouveau sur la technologie, etc ...)
* Renforce la cohérence et la cohésion (de l'équipe et du code)

### Assurer une meilleure qualité et moins de bugs

* Détection des défauts au plus tôt
* Apporter un regard nouveau, critique
* Provoquer des échanges, des débats, des analyses
* Evite la dégradation progressive du code

## Les techniques

_Différents types de revues peuvent être utilisés_

* Le binômage (_pair-programming_) : _feed-back_ immédiat
* Les _Merge Requests_ ou _Pull Requests_
* Les revues par un pair
* Les revues collectives

:bulb: Ces techniques peuvent être complémentaires.

## Les clefs pour réussir les revues de code

_Les revues de code se préparent et doivent respecter quelques pré-requis pour être réellement efficaces._

### Côté relecteur : être bienveillant

* Critiquer le code, pas le développeur
* Employer "je" ou "on" et pas "tu"
* Valoriser les bons points constatés (montrer les points positifs)

### Côté relecteur : apporter des critiques constructives

* Critiquer le fond, pas la forme (pour çà il y a des outils pour automatiser). Attention, la forme n'inclue pas le respect des normes, la lisibilité ou la maintenabilité
* Etre le plus clair, précis et explicite possible (pas d'ironie, d'ambiguïté)
* N'apporter que des commentaires constructifs en proposant des solutions ou des alternatives
* Ne pas aller trop vite, il faut prendre le temps d'analyser, utiliser une _checklist_ par exemple
* Favoriser également, en plus des commentaires, les échanges de vive voix

### Côté relu : être reconnaissant

* Ne pas prendre les remarques pour soi
* Considérer les remarques comme des moyens d'amélioration continue, d'apprentissage
* Se rappeler que la personne qui a commenté le code a pris de son temps dans le but d'améliorer le produit développé
* Répondre à TOUS les commentaires
* Expliquer ces choix d'implémentation "à priori" pour orienter le relecteur
* Ne soumettre à la revue que du code finalisé et fonctionnel

### Impliquer l'équipe

* Initier la pratique dès le début du projet, ne pas attendre
* Rendre les revues systématiques (présente dans les _Definition of Done_ / votre _WorkFlow_)
* Ne pas corriger / modifier à la place du développeur initial

### Optimiser les revues

* Limiter la taille des _Merge Requests_ ou _Pull Requests_ ou du code à revoir : trop de code à revoir = risque de louper des choses (découragement, passer trop vite, ...). Petite revue = meilleure efficacité, plus de pertinence
* Les standards / normes / ... doivent être partagés, **validés** et connus de tous et maintenus par tous. Ce qui permet :
  * d'éviter de se répéter et donc gagner du temps (de revue et de développement)
  * d'éviter les conflits

### Combiner les techniques

* Tests automatisés
* Inspection continue avec des outils comme _Sonarqube_
* Revue collectives : partage de la connaissance
* Revue par des pairs : regard nouveau

## Revue de code VS Audit de code

L'audit de code est généralement réalisé par une personne externe à l'équipe voir parfois externe à l'entreprise.

De plus généralement ce type d’audit intervient souvent trop tard dans le cycle de vie du projet/produit ne permettant pas une remontée rapide et donc une prise en compte rapide des informations par les différents acteurs.

Enfin l'auditeur ne dispose bien souvent que de très peu d’éléments historiques ou de contexte ou des contraintes liés au projet/produit/entreprise pour pouvoir juger des choix techniques ou méthodologiques rencontrés. L'avis exprimé est donc subjectif et basé sur l'expérience et l'avis personnel de l'auteur de la revue.
