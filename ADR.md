# Architectural Decision Records (ADR)

## Généralités

L'idée est de créer **au plus proche** du code source un dossier contenant les décisions prises concernant l'architecture du projet (architecture applicative ou plus générale).

C'est une sorte de journal de toutes les décisions architecturales prises durant la vie du projet.

Ces décisions doivent donc y être toutes listées et **justifiées** pour pouvoir s'y référer à tout moment.

La rédaction de ces fiches doit être la plus simple et la plus rapide possible, le format **Markdown** y est donc tout à fait adapté.

## Avantages

* Comme pour un véhicule c'est en quelque sorte le carnet d'entretien de l'application permettant de connaître l'historique des choix fait sur le projet
* Apporte des éléments historiques et de contexte dans le cadre de nouveaux arrivants sur projet (facilite le _turn-over_)
* Apporte des éléments historiques et de contexte pour les auditeurs
* Rédiger la documentation nous force à bien comprendre le sujet et à se poser des questions pouvant parfois remettre en cause la décision prise

## Quelques règles que l'on peut s'imposer

* Un fichier _Markdown_ par décision, par exemple en respectant un formalisme du type `20181001_decision.md`
* ... et contenant à minima les sections :
  * **Context** : _What is the issue we're seeing that is motivating this decision or change_
  * **Decision** : _What is the change that we're actually doing_
  * **Consequences** : _What becomes easier or more difficult to do because of this change_
* Optionnellement rajouter :
  * la date
  * les personnes ayant prises la décision
  * un statut : accepté, remplacé, ...
  * les alternatives non retenues

## Quand rédiger une ADR

Quelques exemples :

* Lors de l'ajout, le remplacement ou la suppression d'une bibliothèque
* Lors de la modification d'un contrat d'interface
* Lors du choix d'une dette technique volontaire

## Un template personnel

```markdown
# DATE : TITRE

## Qui(s)

> Personne(s) en charge de la modification

QUI ?

## Origine

> Origine de la demande / du besoin

* [ ] Issue
* [ ] Ticket Jira
* [ ] Initiative personnelle
* [ ] Autre (détailler)

## Contexte

> Description du besoin impliquant le changement

QUOI ?

## Décision

> Description de ce qui a été mis en place

COMMENT ?

## Conséquences

> Description des impacts que ce changement a impliqués

TODO
```

## Ressources

* :uk: [Homepage of the ADR GitHub organization](https://adr.github.io/)
* :uk: [Command-line tools for working with ADR](https://github.com/npryce/adr-tools)
* :uk: [Blog : Managing Architecture Decision Records with ADR-Tools](https://www.hascode.com/2018/05/managing-architecture-decision-records-with-adr-tools/)
* :fr: [[DevFest Toulouse 2018] Architecture Decision Records: Réconciliez vous avec votre doc - Arnaud Bos](https://www.youtube.com/watch?v=EDYplU1PB5s)

---
:point_left: [Retour à l'accueil](README.md)
