# Load

La dernière étape consiste à charger les données transformées dans leur destination finale.

Il existe trois principaux types de chargement:

<table><thead><tr><th>Type</th><th width="379">Description</th></tr></thead><tbody><tr><td>Initial Load</td><td>Chargement initial de l'ensemble des données.</td></tr><tr><td>Incremental Load</td><td>Chargement uniquement des nouvelles données ou des données modifiées ou supprimées depuis le dernier traitement.</td></tr><tr><td>Full Load</td><td>Remplacement complet des données existantes par l'ensemble des données disponibles.</td></tr></tbody></table>

Le chargement peut être effectué périodiquement ou en continu dans le cas du _Streaming ETL_.

* Points clés à étudier:
  * Si vous avez un nombre très important de sources de données, optez-vous pour une approche ETL ou au contraire ELT ?
  * Quelles sont les problématiques ("faiblesses") des ELT ?
  * La composante "cloud computing" nous poussera à utiliser quelle approche ?
