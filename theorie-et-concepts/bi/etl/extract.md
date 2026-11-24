# Extract

## Principe de base

La première étape de l'ETL consiste à récupérer des données de différentes sources.

Source interne: //TODO

Source externe: //TODO

Les données extraites sont généralement copiées dans une zone temporaire appelée _Staging Area_.

Les sources peuvent notamment être:

* Bases de données relationnelles ou NoSQL.
* CRM et ERP.
* API et microservices.
* Fichiers JSON et XML.
* Fichiers plats (CSV, TXT, etc).
* Emails.
* Pages Web.
* Objets connectés (_IoT)._

L'objectif est de récupérer les informations nécessaires tout en conservant les éléments permettant de les identifier et de les relier entre elles.

## Détails techniques

{% embed url="https://www.bmc.com/learn/data-extraction.html" %}

{% hint style="info" %}
**Point important :** l'extraction ne signifie pas nécessairement que les données sont déjà propres, structurées ou exploitables.
{% endhint %}

### Extraction de données vs ingestion de données

| Data Extraction                                         | Data Ingestion                                  |
| ------------------------------------------------------- | ----------------------------------------------- |
| Extraction des données depuis une ou plusieurs sources. | Centralisation et préparation des données.      |
| Récupération des données brutes.                        | Acheminement des données vers un système cible. |
| Première étape du processus.                            | Processus d'intégration des données plus large. |

{% hint style="info" %}
L'extraction est donc une partie du processus global d'ingestion.
{% endhint %}

## 3. Les différentes méthodes d'extraction

| Méthode                            | Résumé                                                                     | Exemple                                                        |
| ---------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------- |
| **Full Extraction**                | Extraire toutes les données disponibles.                                   | Récupérer toutes les factures.                                 |
| **Partial Extraction**             | Extraire uniquement les données sélectionnées.                             | Récupérer les factures de 2026.                                |
| **Incremental Extraction**         | Extraire uniquement les nouvelles données ou celles qui ont été modifiées. | Récupérer les factures ajoutées depuis la dernière extraction. |
| **Manual Extraction**              | Extraire les données manuellement.                                         | Copier les informations d'un PDF vers Excel.                   |
| **Update Notification Extraction** | Déclencher l'extraction lorsqu'une modification est détectée.              | Utiliser un webhook lors de la création d'une facture.         |
| **Physical Extraction**            | Extraire des données depuis des équipements ou supports physiques.         | Récupérer des données provenant de capteurs.                   |

#### À retenir

Les méthodes se distinguent principalement par **la quantité de données récupérées et le déclenchement de l'extraction**.

* **Full / Partial** : quelle quantité de données extraire ?
* **Incremental** : quelles données ont changé ?
* **Manual** : extraction réalisée par un utilisateur.
* **Update Notification** : extraction déclenchée par un événement.
* **Physical** : extraction depuis une source physique.

### Discussion Carfleet

Comment qualifiez-vous l'extraction qui est réalisée ?

Critères:

* Sources internes ou externes ?
* Quelle(s) méthode(s) d'extraction ?
* Déclencheur (trigger) ?



### Les 7 étapes du processus d'extraction de données

1. **Valider et nettoyer** : garantir la qualité et la cohérence des données.
2. **Identifier les données** : déterminer les données à extraire et leurs sources.
3. **Détecter les modifications** : identifier les nouvelles données et les changements.
4. **Définir la destination** : déterminer où stocker les données extraites.
5. **Exécuter l'extraction** : récupérer et transférer les données.
6. **Gérer les données** : intégrer l'extraction dans un processus global ETL ou ELT.
7. **Documenter et contrôler** : tester, auditer et assurer la traçabilité du processus.

### Discussion Carfleet

Comment évaluez-vous les points 1 et les points 7 ?
