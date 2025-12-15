# Livrable

## Module BI1 - Objectifs de fin de module

### Intention

Ce document décrit le livrable attendu à la fin du module BI1. Il s'agit d'une confirmation écrite de ce que nous avons discuté en classe à plusieurs reprises. N'hésitez pas à le questionner, à proposer des reformulations pour éviter tout doute sur ce qui est attendu.

### Modalités de livraison

| Critère       | Valeur                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Délai         | Vendredi, 9 janvier 2025, à 17h00                                                                                                                                                                                                                                                                                                                                                                                            |
| Code source   | <p>Repository Github<br>* Partagé avec l'enseignant (droit admin pour que je puisse le transférer dans le projet)<br>* Les fonctionnalités terminées sont présentes sur la branche <em>develop</em><br>* Les fonctionnalités incomplètes restent sur une branche feature dédiée<br>* Wiki précisant les choix technologiques<br>* Les issues décrivent les problèmes détectés (erreur de sécurité, refactor non terminé)</p> |
| GithubProject | <p>Nous offre l'état du projet en utilisant la structure Kaban suivante:<br>* Todo : <em>feature</em> non réalisées, non terminées<br>* In Progress : <em>features</em> en cours de réalisation<br>* In Review : <em>features</em> prêtes pour la review<br>* Done: <em>features</em> validées par l'enseignant - elles pourront être intégrées à la prochaine <em>release</em></p>                                          |
| Livrable      | <p>Une issue est assignée à l'enseignant mentionnant:<br>* Le dernier commit sur la branch <em>develop</em> ainsi que sur les éventuelles branches <em>feature</em><br>* Un lien pointant sur une vidéo présentant le Kaban</p>                                                                                                                                                                                              |

### Description

Votre projet "BucketAdapter" a pour objectif d'être la "base code" pour la suite de l'implémentation qui aura lieu durant le prochain trimestre.

D'un point de vue fonctionnalité, l'idée est d'avoir un composant facilitant le travail asynchrone des micro-services. En déposant leur résultat respectif sur un _bucket,_ les micro-services pourront ainsi travailler à leur rythme.

L'idée est d'avoir un niveau de qualité, un standard que nous pourrons ainsi maintenir pour la suite du développement.

#### Fonctionnalités attendues

Votre solution doit pouvoir dialoguer avec une ressource de type _Object Storage_ de deux providers différents (AWS / GCP / AZURE).

Les fonctionnalités suivantes doivent être implémentées

* Create an object
* Update an object
* Delete an objet
* Share an object (temporaly url)
* List objects
* DoesExist

Note1 : La différence entre un _bucket_ et un _object_ ne doit pas être à la charge de l'utilisateur.

Note2 : Optez une approche permettant à votre composant de dialoguer avec plusieurs _buckets_.

#### Contraintes techniques

Voici les composants minimaux à développer, ainsi que les contraintes à respecter:

***

**API**

| Critère                     | Valeur                                                                                                                                                                                                                                                                                                      |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 3 couches logiques (layers) | <p>* Presentation layer<br>* Business Layer<br>* Persistence layer (dans ce cas, notre <em>Bucket</em> sera considéré comme tel)<br><a href="https://cpnv-es-ngy.gitbook.io/bi1-backlog/roadmap/theorie-et-concepts/technique/api-et-couches-logiques">* Pour vous documenter</a></p>                       |
| Normes HTTP                 | <p>* <a href="https://cpnv-es-ngy.gitbook.io/bi1-backlog/roadmap/theorie-et-concepts/technique/les-methodes-http">Mozilla Foundation - HTTP Verbs</a><br>* <a href="https://cpnv-es-ngy.gitbook.io/bi1-backlog/roadmap/theorie-et-concepts/technique/les-codes-http">Mozilla Foundation - HTTP Code</a></p> |
| Nommage des ressources      | \* [Restfulapi.net - Resource naming](https://restfulapi.net/resource-naming/)                                                                                                                                                                                                                              |
| Documentation               | Un swagger publie la documentation                                                                                                                                                                                                                                                                          |



***

**Service "BucketAdapter"**

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

{% file src="../../.gitbook/assets/class-diagram-v4-bucketAdapter (1).puml" %}

L'architecture minimale suivante doit être respectée:

* Interface
  * Déclare uniquement les signatures des méthodes
  * Aucune trace du provider (argument, type de retour)
* Implémentation _Adapter_
  * Respecte l'interface
  * Est la seule couche qui est spécifique à un _provider_
* Service
  * Ne contient aucune traces d'un _provider_ spécifique
  * S'appui sur une _factory_ pour obtenir le bon _adapter_.
* Design Pattern
  * Une _Factory_ livre le bon adapter au service.

***

* Test
  * Approche BDD (test -> feat -> refactor)
  * Les scénarios de tests suivent la structure "given/when/then"
  * Factorisation du code avec les artefacts du framework de test (Setup/TearDown)
  * L'import du SDK n'est justifié que pour l'utilisation des interfaces livrées par le _Cloud Provider_
  * Un "mock" simule le comportement du _provider client_ afin que les tests soient réalisées sans nécessité d'appel réseau
  * IoC/DI - L'injection de dépendance est implémentée pour permettre le test unitaire de l'implémentation de l'adapter, sans avoir besoin d'instancier un "vrai" client du _sdk_.

***

* Variables d'environnement
  * Un .env centralise les valeurs telles que:\
    \* Le port d'écoute de l'api\
    \* Les _credentials_ et clés d'api\
    \* Toutes les variables intéressantes pour l'_ops_

***

**Readme**

Voici le [_template_](https://github.com/NGY-TEMPLATE/MASTER-README) à utiliser.

***

**Conteneurisation**

La solution offre un déploiement "classique" tout comme via Docker. Pensez-y pour le dév, pour les _Github Actions_ ainsi que le déploiement.

* Le Dockerfile utilise la dernière version de la synthaxe
* Multistage
  * résolution des dépendances
  * exécution et validation des tests
  * image de prod sans dépendances de dev ni test
* Image de prod ne contient que des dépendances de prod (pas de jdk)

***

**Sécurité**

* Conteneur
  * aucune vulnérabilités de type "high" sur l'image de prod
  * seul le port indispensable est publié
* Code
  * aucune vulnérabilités de type "high" sur les dépendances du projet

***

Le dépôt répond aux critères suivants:

| Critère                      | Valeur                                  |
| ---------------------------- | --------------------------------------- |
| Protection de branches       | _main_, _develop_, _release_, _hotfix_  |
| Githubactions activées pour: | <p>* Linter<br>* Tests automatiques</p> |

