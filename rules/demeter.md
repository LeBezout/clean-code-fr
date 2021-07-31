# Loi de "Déméter"

## Définition

> Un module ne doit pas connaître les détails internes des objets qu'il manipule.

> Les modules ne connaissent que leurs collaborateurs immédiats et ne peuvent pas parcourir l'intégralité du système ou d'un graphe d'objets.

## Détails

Les objets cachent leurs données et exposent des opérations.

Une méthode f d'une classe C ne doit appeler que les méthodes des éléments suivants :

* C
* un objet créé par f
* un objet passé en argument à f
* un objet contenu dans une variable d'instance de C

## Références

* [Wikipédia](https://fr.wikipedia.org/wiki/Loi_de_D%C3%A9m%C3%A9ter)

---
:point_left: [Retour à l'accueil](../README.md)
