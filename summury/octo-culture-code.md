# Fiche synthèse : OCTO - Culture Code - 2016

:link: <https://publication.octo.com/fr/telechargement-livre-blanc-culture-code> : _Software Craftsmanship : Better Places with Better Code_

## Introduction

- Nous sommes convaincus que créer des logiciels de qualité ne coûte pas plus cher, au contraire. Malheureusement, la situation dans de beaucoup d’entreprises est préoccupante.
- On peut avoir l'impression d'obtenir le même logiciel avec ou sans tests automatisés [...] mais c'est dans le temps que l'écart se creusera.
- Le développement de logiciels est un savoir-faire, qui s’acquiert via l’expérience et l’accompagnement de ses pairs, comme dans l’artisanat. Une simple formation n’est pas suffisante.
- Software Craftsmanship (artisanat logiciel) : il ne suffit pas qu’un logiciel fonctionne, il faut également qu’il soit bien conçu.
- La non-qualité du code a également des conséquences économiques concrètes
- L’absence de culture de la qualité explique aussi souvent un piètre degré de satisfaction et un désengagement des développeurs

## Better Places

- Pour réaliser des produits de haute qualité, il faut s’appuyer sur des personnes compétentes, motivées et même passionnées, et qui cherchent à apprendre et à s’améliorer en continu.
- Travailler dans un cadre où la qualité des réalisations est négligée devient vite démotivant, notamment pour les développeurs, au risque de voir les meilleurs partir dans une autre entreprise ; un développeur préfère investir du temps pour des fonctionnalités futures plutôt qu’éponger les bugs du passé...
- c’est une culture, celle de la qualité logicielle
- Pour agir au mieux dans l’équipe, et collaborer efficacement avec chacun, il est utile de comprendre un minimum le métier de chacun
- Adopter les valeurs « Craft » est une bonne première étape mais les partager avec ses collègues et encore plus aux managers, est la clé pour pouvoir produire du code de qualité au sein de votre entreprise.
- Les développeurs sont des professionnels du développement, il est indispensable de leur accorder une certaine autonomie dans leurs pratiques.
- La création de logiciel est un métier passionnant et même plutôt fun, pour peu que l’on puisse l’exercer avec application et professionnalisme dans un environnement favorable.
- la qualité du code que produit votre entreprise est une affaire dont vous (=> les managers) devez vous préoccuper.
- Le code est une source de valeur pour l’entreprise, et cette valeur doit être préservée par la mise en place de pratiques de développement de qualité.
- Le premier principe du manager responsable d’équipes de développement est de considérer le code développé par ses équipes comme un « actif », au même titre que tout autre moyen de produire de la valeur dans l’entreprise.
- Sans une discipline de tests unitaires et de revues de code, le nombre de bugs dans l’application augmente imperceptiblement.
- Le manager d’une équipe de développement devrait être « dur avec les mauvaises pratiques, doux avec les personnes »
- l’impact de la non-qualité sur un projet détériore les performances de son service, mais est de plus préjudiciable à la culture de l’entreprise ainsi qu’à son image
- Aidez les développeurs à diffuser les bonnes pratiques en encourageant la mise en place de communautés de pratiques dans l’entreprise
- Le code logiciel produit est un actif apportant de la valeur à la société qui le produit. À ce titre, il est primordial pour une organisation de tout mettre en oeuvre pour en prendre soin.
- La responsabilité de cette qualité n’incombe pas seulement aux développeurs
- La plupart des équipes ont besoin d’un Tech Lead qui les emmène vers une forte culture de la qualité.
- Le but est de favoriser un fonctionnement collectif, dans lequel l’équipe peut prendre ses propres décisions, au lieu d’attendre simplement les ordres
- Dette technique tactique : un expédient temporaire, un écart ponctuel aux standards de l’équipe, pour lequel une solution de recouvrement est non seulement identifiée, mais en plus planifiée dans le temps
- Dette technique endémique : revient à désigner le code de mauvaise qualité, pour lequel aucune solution n’a été planifiée.
- Vous ne pouvez pas mener un développement logiciel à coups de dettes techniques répétées, et encore moins en vous appuyant sur du code de mauvaise qualité.
- Travailler seulement sur les dégâts sans tenter de changer les facteurs, c’est comme tenter d’écoper sans rechercher les voies d’eau.

## Better Code

### La revue de code

- **l'outillage ne peut en aucun cas remplacer la revue de code**. Même si un grand nombre de défauts potentiels peut être relevé automatiquement, il serait dangereux de penser qu'on peut se reposer intégralement dessus.
- La revue de code est une pratique technique. Donc seules les personnes compétentes techniquement doivent y participer, les animer et suivre les corrections.
- la relecture du code produit est une pratique essentielle pour la qualité de l'ouvrage. Elle permet de **détecter les défauts au plus tôt et à moindre coût, renforce la propriété collective du code, favorise l'apprentissage et améliore la qualité des échanges entre développeurs**.

### Les tests

- Beaucoup d'organisations ont des douleurs dans la mise en place de leur stratégie de tests, allant parfois jusqu'à abandonner les changements initiés.
- Faire participer un testeur ou un analyste métier à l'élaboration des tests unitaires n'a que peu de sens : ils concernent uniquement les développeurs.
- C'est un véritable gâchis d'utiliser l'énergie d'un testeur pour découvrir des défauts évidents, alors qu'il pourrait par exemple se concentrer sur des tests exploratoires.
- Les tests de bout en bout ou d'IHM ne sont quant à eux pas toujours rentables en termes d'automatisation.
- L'automatisation des tests fonctionnels au niveau de l'interface graphique [...] sont très sensibles aux modifications dues aux évolutions fréquentes des interfaces. Ils sont donc victimes de "faux négatifs".
- Il est préférable de se concentrer sur des cas critiques dont le non-fonctionnement pourrait porter atteinte à l'activité de l'organisation.
- tout code qui n'est pas couvert par des test automatisés est du _Legacy_.
- Les tests deviennent une pratique centrale de l'équipe de réalisation du produit.
- Mettre l'accent sur l'automatisation des tests de construction permet aussi de limiter l'effort sur les tests de contrôle, et de concentrer l'énergie des testeurs là où ils apportent le plus de valeur.
- Tout temps utilisé avant le déploiement pour prévenir des défauts est du temps investi judicieusement.
- Le design n'émergeait pas avec les tests, et je n'écrivais que ceux auxquels l'implémentation me faisait penser.

---
:point_left: [Retour à l'accueil](../README.md)
