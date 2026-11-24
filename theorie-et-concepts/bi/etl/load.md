# Load

## Principe de base

La dernière étape consiste à charger les données transformées dans leur destination finale.

Il existe trois principaux types de chargement:

<table><thead><tr><th>Type</th><th width="379">Description</th></tr></thead><tbody><tr><td>Initial Load</td><td>Chargement initial de l'ensemble des données.</td></tr><tr><td>Incremental Load</td><td>Chargement uniquement des nouvelles données ou des données modifiées ou supprimées depuis le dernier traitement.</td></tr><tr><td>Full Load</td><td>Remplacement complet des données existantes par l'ensemble des données disponibles.</td></tr></tbody></table>

## En détails

{% embed url="https://aws.amazon.com/what-is/etl/#amsc8--32b7yl" %}

Lors du chargement, les outils ETL déplacent les données transformées de la zone de transit (_staging area_) vers l'entrepôt de données cible. Dans la plupart des organisations, ce processus est automatisé, bien défini, continu et piloté par lots (_batch_). AWS décrit deux méthodes de chargement.

**Chargement complet (**_**full load**_**)** : la totalité des données de la source est transformée puis transférée vers l'entrepôt. Il a généralement lieu lors du premier chargement depuis un système source.

**Chargement incrémentiel (**_**incremental load**_**)** : l'outil ETL charge à intervalles réguliers le « delta », c'est-à-dire la différence entre la cible et la source. Il conserve la date de la dernière extraction pour ne charger que les enregistrements ajoutés après cette date. Il existe deux manières de le mettre en œuvre :

* **Incrémentiel en flux (**_**streaming**_**)** : adapté aux petits volumes, il envoie en continu les modifications vers l'entrepôt via des pipelines de données. Quand la vitesse atteint des millions d'événements par seconde, on peut recourir au traitement de flux d'événements (_event stream processing_) pour surveiller et traiter les données afin de prendre des décisions plus rapidement.
* **Incrémentiel par lots (**_**batch**_**)** : adapté aux gros volumes, il regroupe périodiquement les changements en lots. Pendant cette période de synchronisation, aucune action ne peut avoir lieu sur le système source ni sur le système cible.
