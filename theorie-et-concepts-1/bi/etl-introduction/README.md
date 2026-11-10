# ETL - introduction

{% embed url="https://www.ibm.com/topics/etl?utm_medium=OSocial&utm_source=Youtube&utm_content=SOFWW&utm_id=YTEndCard-101-ETL-Product-Page-ETL" %}

## Définition de l'ETL

L'ETL est un processus d'intégration de données qui permet de collecter des informations provenant de plusieurs sources, de le transformer et de les charger dans une destination commune.

L'objectif est de rendre les données cohérentes, fiables et exploitables pour:

* Le reporting.
* L'analyse de données (_Data Analytics_).
* La _Business Intelligence_ (_BI_).
* Le _Machine Learning_ et l'intelligence artificielle.

L'ETL repose sur trois étapes fondamentales:

| Etape     | Description                                                         |
| --------- | ------------------------------------------------------------------- |
| Extract   | Extraction des données depuis différentes sources.                  |
| Transform | Nettoyage, validation, enrichissement et normalisation des données. |
| Load      | Chargement des données transformées dans un système cible.          |

L'ETL est particulièrement intéressant pour les organisations qui doivent intégrer des systèmes existants (_Legacy Systems_), garantir la qualité des données et protéger les données sensibles.

## Pourquoi l'ETL est-il important ?

L'ETL permet aux entreprises de centraliser des données issues de systèmes hétérogènes et de les convertir en informations fiables.

Son évolution historique peut être résumée en trois grandes périodes:

* Années 1970 : apparition de l'ETL pour intégrer les données et en faciliter l'analyse.
* Années 1990-2000 : développement du Big Data et intégration de nouvelles sources de données, notamment les réseaux sociaux et les objets connectés (_IoT)_.
* Année 2000 à aujourd'hui : développement des infrastructures Cloud et intégration avec des plateformes telles qu'AWS, Microsoft AZURE et Snowflake.

Aujourd'hui, l'ETL évolue vers le traitement en continu (_Streaming ETL_), qui permet d'obtenir des informations presque en temps réel.

## ETL versus ELT

ETL et ELT sont deux approches d'intégration de données. Leur principale différence réside dans l'ordre des opérations.

ETL: les données sont transformées avant leur chargement dans le système cible.

ELT: les données brutes sont d'abord chargées dans le système cible, puis transformées directement dans celui-ci.

| Critère              | ETL                                                                       | ELT                                                  |
| -------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------- |
| Ordre des opérations | Extract → Transform → Load                                                | Extract → Load → Transform                           |
| Transformation       | Avant le chargement                                                       | Après le chargement                                  |
| Type de données      | Principalement structurées                                                | Structurées, semi-structurées et non structurées     |
| Volume               | Adapté aux volumes plus modestes                                          | Adapté au Big Data                                   |
| Performance          | Transformation avant chargement, donc transfert potentiellement plus lent | Chargement initial plus rapide                       |
| Coûts                | Infrastructure et ingénierie initiales plus importantes                   | Infrastructure initiale potentiellement plus simple  |
| Maintenance          | Peut nécessiter davantage de modifications des pipelines                  | Architecture généralement plus flexible              |
| Sécurité             | Possibilité de masquer les données sensibles avant leur chargement        | Nécessite une gouvernance adaptée des données brutes |

A retenir : L'ETL privilégie la préparation et la qualité des données avant leur stockage, tandis que l'ELT privilégie la rapidité d'ingestion et exploite les capacités de traitement du système cible.
