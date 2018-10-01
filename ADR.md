# Architectural Decision Records (ADR)

## Généralités

L'idée est de créer **au plus proche** du code source un dossier contenant les décisions prises concernant l'architecture du projet (architecture applicative ou plus générale).

C'est une sorte de journal de toutes les décisions architecturales prisent durant la vie du projet.

Celles-ci doivent donc y être toutes listées et **justifiées**.

## Avantages

* Comme pour un véhicule c'est en quelque sorte le carnet d'entretien de l'application permettant de connaître l'historique des choix techniques
* Apporte des éléments historiques et de contexte dans le cadre de nouveaux arrivants sur projet (facilite le _turn-over_) 
* Apporte des éléments historiques et de contexte pour les auditeurs 

## Quelques règles que l'on peut s'imposer

* Un fichier _Markdown_ par décision, par exemple en respectant un formalisme du type `20181001_decision.md`
* ... et contenant à minima les sections :
  * **Context** : _What is the issue we're seeing that is motivating this decision or change_
  * **Decision** : _What is the change that we're actually doing_
  * **Consequences** : _What becomes easier or more difficult to do because of this change_
* Optionnellement rajouter la date et les personnes ayant prises la décision

## Ressources

* [Homepage of the ADR GitHub organization](https://adr.github.io/)
* [Command-line tools for working with ADR](https://github.com/npryce/adr-tools)
* [Blog : Managing Architecture Decision Records with ADR-Tools](https://www.hascode.com/2018/05/managing-architecture-decision-records-with-adr-tools/)
