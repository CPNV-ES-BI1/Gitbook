# Vision

## Intention

Ce projet est une magnifique occasion de revisiter tous les concepts vus durant votre formation et de l'appliquer sur un projet d'une ampleur un peu plus "croustillante" qu'un simple laboratoire.

L'idée est de partir des concepts de la BI vus durant les 4 premières semaines du module pour construire un thème global, le découper ensemble en phase et répartir nos forces sur sa réalisation.

Voici le briefing dessiné au tableau lors du Kickoff:

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption><p>Vision du projet - schéma</p></figcaption></figure>

## Explications

Partant de deux flux, le premier interne et l'autre externe, il s'agira d'implémenter aussi bien un ELT qu'un ETL.

Le schéma initial prévoyait d'exploiter pour les deux flux le même Datawarehouse, mais la répartition des équipes ainsi que le fait que les deux flux traiteront les mêmes informations, implique un DataWahrehouse pour chacun des flux.

## Aspects organisationnels

La répartition en sous-projets/dev teamps a été à la discrétion des développeurs.

Nous aurons donc:

* un projet spécifique basé sur une source interne, pour l'ELT
* un projet spécifique basé sur une source externe, pour l'ETL
* un projet spécifique pour la mise en oeuvre des sources de données.

## Github

Une seule organisation a été ouverte, contenant tous les sous-projets. Les voici:

{% embed url="https://github.com/orgs/CPNV-ES-BI1-SBB/repositories" %}

La gestion des tâches se fera au sein de l'organisation, à l'aide des Github Projects.



