# Sprint 1 - Composant isolé

## Objectif du sprint

Ce sprint est dédié à l'implémentation de tous les composants nécessaires à la future gestion des flux BI. Le projet a été découpé en différents sous-projet qui se résume à la conception et l'implémentation d'une api.&#x20;

Il s'agit pour chaque sous-projet de développer une première version de leur api, de manière isolée et sans interconnection avec les autres composants. Seuls les Stubs et Mocks permetteront de faire une démonstration fonctionnelle de l'api réalisée.

Chaque équipe reçoit la même story "API v1". Elle intègre un modèle de story à compléter par l'équipe. Les équipes définissent eux-mêmes les critères d'acceptations.

Ce sprint permettra de revoir les principes Scrum.

## Objectifs par équipe

### Sous-Projet : Data Generator / Business Logic

| DevTeams       | Objectif                                                                                                                                          |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Data Generator | Définir les sources de données internes et externes et en offrir l'accès aux teams "Extract".                                                     |
| Business logic | <p>Définir les questions auxquelles le futur Dashboard devra répondre.</p><p><br>Simuler sur Excel les graphiques à obtenir par le Dashboard.</p> |

### Sous-Projet : Internal Source - ETL

| DevTeams  | Objectif                                                                                           |
| --------- | -------------------------------------------------------------------------------------------------- |
| Extract   | Extraction de données en partant d'un pdf afin de "semi-"structurer les données dans un json.      |
| Transform | Appliquer sur le json reçu les opérations de transformation, nettoyage pour valoriser les données. |
| Load      | Injection en sql des données nettoyées et valorisées dans le DataWarehouse.                        |

### Sous-Projet : External Source - ELT

| DevTeams      | Objectif                                                                                                                                                        |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Extract       | Récupérer des données exposées par une ou plusieurs API et les livrer en json.                                                                                  |
| Load DataLake | <mark style="color:red;">Injection des données exploitables sans transformation dans le DataLake. Prévoir différents types de fichiers (json, xml, csv)</mark>. |
| Transform     | Re-traitement des données intégrées dans le DataLake pour nettoyer et valoriser les données.                                                                    |
| Load          | Injection en sql des données valorisées dans le DataWarehouse.                                                                                                  |



## Definition of Done

[Lien vers la DoD valable durant tout le projet.](./#definition-of-done)

Pour ce premier sprint voici les contraintes de qualité spécifique à respecter:

| Critères                                               | Valeur                                                                                                                       | Détails                                                                                                                                               |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Type de composant                                      | Une api RESTFUL                                                                                                              | [Resource naming](https://restfulapi.net/resource-naming/)                                                                                            |
| Réutilisabilité                                        | Les classes développées doivent pouvoir s'adapter facilement à différents domaines autres que les trains.                    | Utiliser de manière adéquate [les interfaces tout comme l'héritage](https://cpnv-es-ngy.gitbook.io/uml-backlog/archive/2023-2024/class-diagram).      |
| Approche BDD                                           | Chaque api doit pouvoir être testée en simulant les dépendances.                                                             | [Utilisation de stub, mocks en fonction des besoins](../../../sandbox/semaines-4-6/theorie-et-concepts/bdd-gerer-les-dependences/mocksarentstubs.md). |
| Injection de dépendance et inversion de responsabilité | L'architecture de vos classes d'implémentation ne doit pas être modifiée/adaptée pour répondre à des problématiques de test. | [DI and IoC](../../../sandbox/semaines-4-6/theorie-et-concepts/bdd-gerer-les-dependences/di-and-ioc.md).                                              |

## Modalités de livraison

{% hint style="info" %}
Délai de livraison fixé au <mark style="color:red;">dimanche 15</mark> à 18h00
{% endhint %}

* La review sera basée sur la branche "develop". Aucune release ne doit être faite.
* Si des features n'ont pas été terminées, elles restent en l'état sur le "feature branch".
* Chaque équipe livre une issue contenant le commit final du sprint, en faisant un rapide "topo" sur la situation.

## Review et sprint planning

### Travail préparatoire

* [ ] **Enseignant** - récupère vos dépôts et étudie vos propositions d'implémentation.
* [ ] **DevTeams** - écrivent leur stories pour le sprint 2 en sachant que l'objectif et de faire dialoguer tous les composants et de mettre en place les différents flux.

{% hint style="info" %}
Jeudi 19 et Vendredi 20 décembre
{% endhint %}

### Déroulement

* [ ] Feedback de l'enseignant sur le travail réalisé
* [ ] Construction -ensemble- du prochain sprint backlog



