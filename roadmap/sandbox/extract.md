# Extract

## Intention

Dans ce laboratoire nous allons entraîner à concevoir et implémenter une première version de notre couche d'extraction. L'intention étant de réaliser une analyse du besoin et de faire ensuite des choix techonlogiques qui peuvent aussi bien toucher le langage de programmation que l'architecture même de la couche d'extraciton.

## Les différentes étapes

### Analyse

Les questions essentielles à étudier avant de partir en conception sont les suivantes:

| Axe                         | Objectif                                                         | Notre ocntexte                                                                                                      |
| --------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Sources de données          | Comprendre d'où viennent les données et comment y accéder.       | DataStorage de différents fournisseurs tels qu'AWS (S3), Azure (BlobStorage) ou GCP (GCPStorage)                    |
| Stratégie d'extraction      | Définir la fréquence, le périmètre                               | L'extraction aura lieu sur demande (trigger manuel). Plusieurs fois par jour.                                       |
| Aspects techniques          | Choisir un langage d'implémentation et une architecture de code. | Liberté total du choix du langage. L'architecture sera identique pour toutes les équipes.                           |
| Qualité et conformité       | Garantir des données fiables et conformes.                       | Pour l'instant il s'agira simplement de récupérer des fichiers plats. Le contenu des fichiers ne sera pas exploité. |
| Maintenance & évolutivité   | Prévoir la robutesse et la facilité d'évolution.                 | L'architecture tiendra compte des aspects évolutif et les tests permettront de valider la non-regression.           |
| Gouvernance & documentation | Assurer la traçabilité et la transparence.                       | Les données ne seront pas exploitées. Il s'agit d'une phase de test.                                                |

##
