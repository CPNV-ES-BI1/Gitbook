# Sprint 2 - Mise en place des flux (synchrone)

## Objectif du sprint

<mark style="color:red;">Le sprint précédant a été dédié à l'implémentation de tous les composants nécessaires à la future gestion des flux BI. Il est venu le temps de mettre en place une logique de flux.</mark>\
\ <mark style="color:red;">Il s'agit pour chaque sous-projet de développer une première version du flux. Cela permettra de valider si vos implémentations sont pertinentes et si les mocks et autres stubs ont bien simulés le comportement du flux implémenté.</mark>

<mark style="color:red;">A la fin du sprint, nous devrions avoir les deux flux "ELT" et "ETL":</mark>

* [ ] <mark style="color:red;">Chaque API est devenue un micoservice "dockerisé",</mark>
* [ ] <mark style="color:red;">Une</mark> [<mark style="color:red;">stratégie d'ordonnancement est définie</mark>](https://aws.amazon.com/blogs/big-data/etl-and-elt-design-patterns-for-lake-house-architecture-using-amazon-redshift-part-1/) <mark style="color:red;">et appliquée.</mark>

## Objectifs par équipe

### Sous-Projet : Data Generator / Business Logic

| DevTeams       | Objectif                                                                                                                                                                                                     |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Data Generator | [Internationaliser le flux entrant ](https://github.com/orgs/CPNV-ES-BI1-SBB/projects/11/views/1?pane=issue\&itemId=90286838\&issue=CPNV-ES-BI1-SBB%7CDATA-GENERATOR%7C4)                                    |
| Business logic | [Enrichir le nombre de graphiques que le Dashboard est censé afficher.](https://github.com/orgs/CPNV-ES-BI1-SBB/projects/11/views/1?pane=issue\&itemId=90286838\&issue=CPNV-ES-BI1-SBB%7CDATA-GENERATOR%7C4) |

### Sous-Projet : Internal Source - ETL

| DevTeams  | Objectif                    |
| --------- | --------------------------- |
| Extract   | //objectif global du sprint |
| Transform | //objectif global du sprint |
| Load      | //objectif global du sprint |

### Sous-Projet : External Source - ELT

| DevTeams      | Objectif                    |
| ------------- | --------------------------- |
| Extract       | //objectif global du sprint |
| Load DataLake | //objectif global du sprint |
| Transform     | //objectif global du sprint |
| Load          | //objectif global du sprint |



## Definition of Done

[Lien vers la DoD valable durant tout le projet.](sprint-2-mise-en-place-des-flux-synchrone.md#definition-of-done)

Pour ce premier sprint voici les contraintes de qualité spécifique à respecter:

| Critères                                               | Valeur                                                                                                       | Détails                                                                                                                                                  |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Type de composant                                      | Une api RESTFUL <mark style="color:red;">Dockerisé</mark>                                                    | [Resource naming](https://restfulapi.net/resource-naming/)                                                                                               |
| Réutilisabilité                                        | <mark style="color:red;">Valider ce principe en ajoutant des flux entrants supplémentaires et divers.</mark> | Utiliser de manière adéquate [les interfaces tout comme l'héritage](https://cpnv-es-ngy.gitbook.io/uml-backlog/archive/2023-2024/class-diagram).         |
| Approche BDD                                           | <mark style="color:red;">Tous les nouveaux scenarios doivent être intégrés au BDD.</mark>                    | [Utilisation de stub, mocks en fonction des besoins](../../../../sandbox/semaines-4-6/theorie-et-concepts/bdd-gerer-les-dependences/mocksarentstubs.md). |
| Injection de dépendance et inversion de responsabilité | <mark style="color:red;">Ce principe est appliqué aussi à l'implémentation.</mark>                           | [DI and IoC](../../../../sandbox/semaines-4-6/theorie-et-concepts/bdd-gerer-les-dependences/di-and-ioc.md).                                              |

## Modalités de livraison

{% hint style="info" %}
Délai de livraison fixé au <mark style="color:red;">vendredi  10 janvier</mark> à 18h00
{% endhint %}

* La review sera basée sur la branche "develop". Aucune release ne doit être faite.
* Si des features n'ont pas été terminées, elles restent en l'état sur le "feature branch".
* Chaque équipe livre une issue contenant le commit final du sprint, en faisant un rapide "topo" sur la situation.

## Review et sprint planning

### Travail préparatoire

* [ ] **Enseignant** - récupère vos dépôts et étudie vos propositions d'implémentation.
* [ ] **DevTeams** - écrivent leur stories pour le sprint 2 en sachant que l'objectif et de faire dialoguer tous les composants et de mettre en place les différents flux.

{% hint style="info" %}
<mark style="color:red;">Jeudi 16 et Vendredi 17 janvier</mark>
{% endhint %}

### Déroulement

* [ ] Feedback de l'enseignant sur le travail réalisé
* [ ] Construction -ensemble- du prochain sprint backlog



