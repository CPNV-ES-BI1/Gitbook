# Microservices - Architecture

## INTRODUCTION

L’architecture _microservices_ consiste à structurer une application en un ensemble de services:

* indépendants,&#x20;
* autonomes,&#x20;
* faiblement couplés,&#x20;
* chacun aligné sur un contexte métier commun.&#x20;

Ce modèle offre modularité, autonomie d’équipe, rapidité de déploiement, flexibilité technologique et scalabilité.&#x20;

Mais <mark style="color:orange;">ce gain de souplesse vient avec un coût en complexité</mark> :&#x20;

* gestion des données distribuées,&#x20;
* cohérence,&#x20;
* complexité des opérations réparties,&#x20;
* besoin d’un bon découpage des services.

Source : [microservices.io - introduction](https://microservices.io/patterns/microservices.html)

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<p align="center">Source : <a href="https://aws.amazon.com/microservices/">AWS - Microservices</a></p>



### API GATEWAY

Source : [microservices.io - API Gateway](https://microservices.iohttps/microservices.io/patterns/apigateway.html)

Dans une architecture basée sur des _microservices_, on a souvent plusieurs services backend, chacun exposant des _APIs_ fines, et plusieurs types de clients (web, mobile, applications tierces, etc.).&#x20;



Si chaque client doit appeler directement chaque microservice, cela pose plusieurs problèmes :

* le client doit connaître l’architecture interne (quels services appeler, leurs adresses, versions, etc.)  couplage fort entre client et backend.
* pour une simple vue/écran, on risque plusieurs _round-trips_ (appels successifs) vers différents services, ce qui peut nuire aux performances (latence, surcharge réseau), surtout pour des clients mobiles ou distants. [Microsoft Learn+1](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/direct-client-to-microservice-communication-versus-the-api-gateway-pattern?utm_source=chatgpt.com)
* chaque microservice devrait gérer les préoccupations transverses (_cross-cutting concerns_) comme l’authentification, le routage, la traduction de protocole, les logs, etc. Cela duplique le code et complique la maintenance



<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>



### EVENT-DRIVEN OR ORCHESTRATOR

Source : [microservices.io - Event-driven architecture](https://microservices.io/patterns/data/event-driven-architecture.html)

