# Fiche synthèse : OCTO - Culture DevOps vol. 3

:link: <https://www.octo.com/publications/culture-devops-volume-3/>

## Chapitre 1 - L'individu

### TDD : de nouveaux outils de tests d’infrastructure

P22 : Coder consistant essentiellement à prendre une succession de décisions, il est impératif de travailler à avoir une boucle de _feed-back_ la plus rapide possible.

Personne ne peut décemment penser déployer en continu du code qui ne
serait pas suffisamment testé.

P28 : vous assurez également la production d’une documentation via votre code de test. Si l’on se demande quel résultat est censée produire telle ou telle partie, les tests, en utilisant des cas et des valeurs concrètes, nous
apporterons une réponse plus fiable qu’un document Word ou PDF obsolète.

### Limites et stratégie

P38 : Écrire un test, c’est faire un investissement en temps.

Plus un test est rapide (à développer et à exécuter), plus il sera exécuté souvent, plus il aura de la valeur.

Nomenclature des tests logiciels <http://douche.name/blog/nomenclature-des-tests-logiciels/>

## Chapitre 2 - L'Équipe

P49 : La connaissance ne circule jamais à 100 % lorsque chacun est sur son
écran.

### Collective Code Ownership

P50 : Pouvoir modifier le code de n’importe qui, n’importe quand, est un bon
indicateur de la qualité d’un code.

Code Reviews: Just Do It <https://blog.codinghorror.com/code-reviews-just-do-it/>

P52 : <https://blog.codinghorror.com/the-ten-commandments-of-egoless-programming/>

P53 : D'expérience, le mob programming est très bénéfique en début de projet lorsqu’on doit constamment prendre des décisions sur les conventions de l’équipe, les choix de design et les apprentissages fonctionnels et techniques. Il facilite l'amorce des sujets complexes et
structurants, qui nécessitent un alignement des convictions et de l’expertise technique.

### Clean Code

P56: L’architecture d’une stack applicative doit suivre les mêmes règles, et réussir à faire la part entre simplicité et efficacité.

### Continuous Integration

P62 : Un pipeline qui n’exécute (presque) aucun test perd environ 99 % de son intérêt. Il permet juste d’envoyer plus vite des bugs en production. Pas de tests, pas de qualité. Pas de qualité, pas de confiance. Pas de confiance, pas de prod.

## Chapitre 3 - L'Entreprise

P69 : chaque équipe est indépendamment constituée selon les expertises
nécessaires à sa tâche, et est capable de prendre des décisions structurantes sans en référer à 8 étages de management.

...les équipes d’infrastructure sont encore trop dans leur monde : elles gèrent le run comme si c’était de leur unique responsabilité. Tant que l’on reste “dans les clous” de ce qu’ils proposent, tout va bien...

### Continuous Delivery

P72 : Proscrire toute modification manuelle sur les machines.

Si un changement doit être opéré, c’est en reconstruisant une nouvelle capacité (VM, conteneur...) à la place d’une ressource existante et non en modifiant une ressource existante.

### Prod-awareness

P76 : Méthode des six chapeaux <https://fr.wikipedia.org/wiki/M%C3%A9thode_des_six_chapeaux>

* Chapeau blanc : La neutralité
* Chapeau rouge : La critique émotionnelle
* Chapeau noir : La critique négative
* Chapeau jaune : La critique positive
* Chapeau vert : La créativité
* Chapeau bleu : L'organisation

P77 : Avoir conscience de la production, c’est se demander ce qui va casser en premier, et comment le limiter, ainsi que comment aller plus vite pour diagnostiquer et rétablir le service.

P81 : L’observabilité n’est pas un luxe, ni quelque chose qui doit intervenir “juste avant une mise en prod”. Vous devez traiter cela comme un first-class citizen , au fur et à mesure de vos développements.

### Le rôle du management

P88 : **Encouragez l’émergence d’une organisation apprenante : faites du partage des bonnes pratiques une valeur centrale de votre organisation.**

## Conclusion

P99 : Au sein d’une équipe, l'émulation est la meilleure des dynamiques.

---
:point_left: [Retour à l'accueil](../README.md)
