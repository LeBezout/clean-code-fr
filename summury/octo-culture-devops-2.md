# Fiche synthèse : OCTO - Culture DevOps vol. 2 - 2018

:link: <https://publication.octo.com/fr/telechargement-livre-blanc-culture-devops-vol-2> : _Le nouveau guide de survie des dev', ops et architectes !_

## Chapitre 1 - Une API REST sinon rien

* Une API est un produit avant tout (_API as a Product_) et se conçoit avec des garde-fous.
* Exposer des API devient plus important que l'exposition d'interfaces Web ou le traitement de tickets.
* L'API va permettre aux utilisateurs de créer leurs propres fonctionnalités par dessus l'infrastructure, démultipliant sa richesse.

## Chapitre 2 - L'open source

* Nous ne sommes plus de simples utilisateurs d'une solution mais également des contributeurs en capacité de l'améliorer

## Chapitre 3 - Les architectures distribuées

* Pour atteindre ces 2 objectifs (performance et disponibilité) il faut arrêter de penser scalabilité verticale (_scale-up_) et pivoter à 90° vers la scalabilité horizontale (_scale-out_).

## Chapitre 4 - L'orientation SDx

* Il faut penser programmation, code et configuration pour représenter une architecture.
* Offrir une SDx à vos clients vous impose une rigueur à toute épreuve dans l'automatisation de votre infra, pour être toujours prêt à réagir aux imprévus.

## Chapitre 5 - L'Infrastructure as Code

* Si un DAT (dossier d'architecture technique) est régulièrement faux, pas à jour, incomplet, imprécis, une plateforme fraîchement bâtie par de l'IaC est nécessairement à l'exact image du code qui l'a produite.
* Si l'on commence à modifier les machines à la main, cette assertion ne reste pas vraie très longtemps.
* L'IaC est née bien avant l'apparition du terme _DevOps_.
* Les pratiques _DevOps_ l'ont simplement rendue indispensable.
* Les langages d'IaC sont généralement conçus autour du paradigme de programmation déclarative :
  * Déclaratif : Puppet, Terraform, Chef, CFEngine
  * Impératif : Fabric, Capistrano
  * Hybride : Ansible
* Modes de fonctionnement : push/pull :
  * Mode agent de type _pull_ : Puppet, Chef, CFEngine
  * Mode _push_ à partir d'une machine de contrôle : Ansible, Terraform, Fabric, Capistrano
* Tous les produits ne ciblent pas le même objectif.
* Les outils :
  * Puppet : _la Rolls des IaC_ projet de référence tant au niveau de son fonctionnement qu'au niveau de l'écosystème qu'il draine.
  * Ansible : _le couteau suisse de l'IaC_, à la fois capable d'adresser l'approvisionnement des machines que l'orchestration "futée" du déploiement des applications.
  * Hashicorp Terraform : spécialisé dans l'approvisionnement des infrastructures sur des _clouds_ ou diverses technologies de virtualisation.
* L'IaC atteint un niveau de maturité qui la rend incontournable de nos jours.
* Le risque n'est toutefois pas éliminé à 100% si la manipulation de l'IaC ne s'accompagne pas d'une hygiène irréprochable dans la gestion et la qualité du code.
* Toute l'infrastructure peut être décrite, installée, testée et versionnée.
* Les administrateurs peuvent se concentrer sur l'amélioration du SI plutôt que sur des tâches facilement robotisables, sans valeur ajoutée à l'intelligence humaine.

## Chapitre 6 - La conteneurisation

* Les conteneurs véhiculent des concepts vecteurs de transformations profondes de notre industrie.
* _Docker_ est le fruit de l'assemblage - génial, de plusieurs concepts pré-existants.
* Conteneurs et machines virtuelles permettent _in fine_ d'isoler des applications ou des processus.
* La particularité de _Windows_ est de proposer deux modes de fonctionnement : faire tourner des conteneurs Window Natifs ou démarrer des portions de système Linux virtualisé pour permettre l'exécution de conteneur Linux.
* Puisqu'il se résume au démarrage d'une application le coût de démarrage du conteneur est négligeable.
* Dans l'esprit _Docker_ suit le principe du _rebuild_ plutôt que celui d'_upgrade_.
* Une mise à jour se fait en reconstruisant une nouvelle image et en remplaçant un ancien conteneur par un nouveau basé sur cette image.
* L'intérêt de ce découpage en couches est la possibilité pour 2 images (ou plus) de partager les mêmes couches, réduisant ainsi l'espace de stockage nécessaire.
* Les applications doivent être pensées pour être proprement et fréquemment arrêtées et redémarrées mais  aussi :
  * Applications dite _stateless_.
  * Séparation du code et de la configuration, principe du _build once, run everywhere_.
  * Exposition d'URL de _healthcheck_.
  * Exposition d'URL de métriques.
  * Production de logs sur les sorties standards.
* Il y a une réelle nécessité de repenser les applications et les processus pour utiliser correctement les conteneurs.

## Chapitre 7 - Le cloud

* Il devient très compliqué, voire impossible de conserver des versions obsolètes de logiciels (OS, middlewares, ...)
* La portabilité implique malheureusement  de se contenter du plus petit dénominateur commun.
* Cette propension à utiliser une application ou un services à la limite - voire ne dehors - de son cadre est un frein à son passage sur le _cloud_.
* Infrastructures immuables : le déploiement _blue/green_ permet de déployer une nouvelle version d'un système sans interrompre le bon fonctionnement du service.
* Si vous songez à mettre votre _cloud_ derrière un outil de _ticketing_, sous la responsabilité d'un centre de service, pour en maîtriser ses usages, alors vous ne tirerez jamais parti des réels avantages du _cloud_. Vous n'avez au final, que déplacé vos serveurs dans le _datacenter_ de quelqu'un d'autre.

## Chapitre 8 - Et à part ça ?

* Le mouvement _DevOps_ a remis le génie logiciel au coeur du monde de l'exploitation informatique.
* Conception responsable, empreinte du numérique (_green it_), ...

## Conclusion

* Vouloir absolument mettre en oeuvre tout le catalogue de ces frameworks dans son SI reviendrait à faire du "_Cargo Cult_", c'est à dire à procéder par mimétisme en s'imaginant être  mature sur le sujet _DevOps_ uniquement parce qu'on a choisi tous les outils à la mode.
* Sans une réelle discipline et une recherche perpétuelle de qualité dans leur mise en oeuvre, ces innovations sont vouées à faire de gros dégâts dans nos SI.
* La production et les opérations sont, par nature, des lieux où le conservatisme est de mise. Or, il faut définitivement remettre ne cause ce mythe qui n'a plus lieu d'être à l'heure du numérique.

---
:point_left: [Retour à l'accueil](../README.md)
