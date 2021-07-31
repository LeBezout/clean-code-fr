# Fiche synthèse : OCTO - Culture Flow

:link: <https://www.octo.com/publications/culture-flow/>

## Préface

Pour aller plus vite, engagez moins de chantiers en parallèle, vous aurez une meilleure concentration et très probablement une meilleure qualité.

## Les principes à adopter tels quels

### Toute décision est prise en réponse à un évènement et non à une date planifiée

P17 : en décidant par exemple de ne pas mettre tous les risques dans le même panier (business, technique, produit, humain)

P20 : l'ajout de nouvelles personnes dans une équipe a généralement un impact négatif à court terme

### chaque équipe connaît son flux de travail

P26 : Nous sommes surpris car nous ne voyons pas tout de suite les conséquences de nos actes.

P26 : Nous sommes surpris par ce qui dépasse notre limite de compréhension.

P26 : Nous sommes surpris quand la réalité ne correspond pas à notre schéma de pensée.

### une livraison de logiciel est un non-évènement qui peut intervenir n'importe quand

P32 : il est nécessaire qu'à tout moment il soit dans un état stable, c'est à dire, livrable.

P32 : Cela suppose d'automatiser les processus de qualification de l'état et au premier chef les tests dits "de qualification".

P32 : ce qui suppose d'automatiser les processus de packaging et de déploiement du logiciel.

P34 : les organisations les plus rapides sont aussi les plus stables

P36 : Comme chaque modification de code concerne un périmètre restreint, la localisation de la correction sera plus rapide et plus simple.

P38 : (trunk based development) : Lorsque les développeurs effectuent toutes leurs opérations directement sur le trunk plusieurs fois par jour, la base de code se doit d'être livrable à tout moment. Il en résulte une responsabilisation plus forte des développeurs.

P41 : (BDD) : A l'arrivée, ce qui part en production, c'est la compréhension de celui qui le code.

P42 : BDD, TDD, Trunk-Based, CI-CD = facilité à répéter des étapes de production de valeur sans effort et sans risque

### pour résoudre un problème il d'abord le rendre visible

P44 : il est préférable de rendre les problèmes visibles pour générer des discussions et prendre des décisions.

P45 : **lorsque vous traitez des choses sans les rendre visibles vous dissimulez malgré vous le problème au reste de votre écosystème**

P45 : observabilité : Livrer en continu implique d'avoir mis en place
une boucle de rétroaction efficace pour savoir si les changements déployés régulièrement améliorent ou aggravent la stabilité du système dans sa globalité. Surveiller en continu son infrastructure et ses applications permet de détecter et d'être averti instantanément de tout problème survenu sur une plateforme.

P46 : L'observabilité peut se définir comme "_la capacité d'un système à être
appréhendé par un humain afin qu'il puisse le comprendre, le modifier et le corriger_".

### tout le monde connaît le lien entre sa production et la stratégie de l’organisation

P54 : Ce qui a une valeur économique aujourd’hui, ce n’est plus tant le savoir que la capacité à le mettre en œuvre, le contextualiser à un écosystème et se l’approprier.

## Les principes à adapter au contexte

### tout changement pérenne est une modification des habitudes

P66 : la capacité de s'exprimer et de prendre des risques sans crainte est un élément clé.

P68 : _Pair Programming_ : Le grand bénéfice n'est pas la productivité mais le partage de savoir-faire entre les développeurs.Cette pratique est très intéressante lors de l'arrivée d'une nouvelle personne dans l'équipe.

P69 : la revue de code : L'efficacité de la revue de code sur le partage est cependant moindre car les développeurs relisant le code n'ont pas participé aux différentes réflexions ayant amené au résultat produit.

P70 : _Mob Programming_ : Le Mob Programming est l’un des moyens les
plus efficaces, sinon LE moyen le plus efficace, pour :

- Faire émerger des standards dans une équipe qui vient d’être formée,
- Réaligner les standards multiples et/ou implicites d’une équipe déjà formée,
- Diffuser à l'équipe les connaissances acquises par un coéquipier qui reviendrait de formation
- Expérimenter de nouvelles façons de travailler

P70 : _Shifting Left On Security_ : Les experts sécurité, en général peu nombreux dans les organisations, sont souvent sollicités et inclus à la fin du cycle de vie du logiciel lorsqu'il est souvent pénible et coûteux d'effectuer les correctifs nécessaires.

P70 : Dans cette logique de flux continu de livraison de fonctionnalités, la
sécurité n'a plus sa place dans une phase aval, complètement déconnectée et réalisée par une autre équipe quand tous les développements sont finalisés

P71 : **Il est plus simple de s'assurer que les personnes qui construisent le logiciel agissent et le font correctement que d'inspecter des systèmes et des fonctionnalités presque terminées.**

P72 : Intégrer les nouveaux : l'importance de travailler sur la capacité d'une organisation à inclure de nouvelles personnes.

P73 : Les modes colocalisé et éclaté sont ceux qui montrent les meilleurs résultats. Nous déconseillons donc tous les modes distribués.

P74 : une organisation composée uniquement d’experts, c’est-à-dire de personnes qui ne maîtrisent qu’une seule activité, finira inévitablement par rencontrer des blocages forts.

### les boucles de feedback

P83 : il faut, dans le temps court comme dans le temps long, avoir toujours en ligne de mire les besoins, sans cesse renouvelés, de l’utilisateur final.

P83 : un persona : une représentation symbolique de nos utilisateurs cibles.

P83 : L’UX design (User Experience Design) a pour principe fondamental d’intégrer les utilisateurs le plus tôt possible dans le cycle de développement du produit, afin de concevoir le produit pour et avec eux.

P84 : _Lean Startup_ : une méthodologie faite de boucles de feedback courtes pour apprendre au fur et à mesure

P85 : C'est bien quand nous avons un besoin, et non juste un problème, que nous cherchons une solution que nous sommes prêts à payer.

### les organisations techniques et humaines sont liées

P91 : favoriser les couplages faibles, les modes d'interaction :

- service : B réalise pour A
- collaboration : A travaille avec B pour l'aider
- facilitation = _inner source_  : A modifie directement dans la base de code de B, B fait la revue

P92 : Le mode facilitation est celui qui permet d’aller le plus vite en diminuant les frottements et permet aussi d'abaisser la probabilité de duplication de fonctionnalités dans deux applications (nous ne pouvons pas attendre, donc nous redéveloppons chez nous).

P97 : architecture applicative : Bien ranger sa chambre, c’est éviter toutes les superpositions techniques qui créent du lien

P97 : **sortir des architectures à découpage technique pour s'abstraire des
systèmes externes (base de données, système de fichiers, serveur de mail...) et que le code métier ne soit plus noyé au milieu du code technique (frameworks, librairies).**

P97 : **La valeur d'une application réside dans ses cas d'utilisation et ses services métiers.** la logique métier ne doit pas se retrouver dispersée dans
plusieurs couches. le modèle métier d'une application (les objets métiers manipulés) n'évolue pas au même rythme que le modèle de stockage ou encore le modèle de présentation.

P97 : Ce type d'architecture applicative prône un couplage faible en supprimant les adhérences aux composants d'infrastructure: il en résulte
une meilleure testabilité, orientée sur le comportement métier.

P97 : Par ricochet, en isolant et en protégeant la valeur métier des éléments techniques connexes, il est possible de faire des mises à jour de dépendances techniques beaucoup plus régulièrement et plus facilement, sans crainte de régressions.

P98 : Clean Architecture / Hexagonale Architecture :

- Une isolation et une protection du code métier,
- Une totale indépendance vis-à-vis des frameworks avec un métier clair et explicite,
- Une séparation claire des problèmes,
- Une meilleure testabilité orientée sur le comportement métier.

P100 : Archi hexagonale : l'important est de co-localiser le code métier et de sortir des architectures à découpage technique.

### les écosystèmes sont organisés en minimisant les frictions vis-à-vis de la stratégie

P103 : **il n'y a rien de plus stable dans le temps que les domaines métiers.**

P104 : aligner par couches techniques : elle n'est orientée ni valeur, ni client, ni métier. Il manque une vision d'ensemble.

P105 : modèles : il vaut mieux les conserver sous forme d’exception plutôt que de les faire rentrer au chausse-pied. **C’est l’exemple de l’équipe appelée Transverse qui regroupe toutes les personnes que nous n’avons pas su placer.**

P106 : l'architecture en continue : Les architectes se doivent donc d'être présents au moment de la mise en œuvre et aux côtés des équipes de réalisation quand les difficultés se présentent.

P107 : Nous prenons les décisions d’architecture au moment où nous
devons les prendre, pas après mais pas avant non plus.

---
:point_left: [Retour à l'accueil](../README.md)
