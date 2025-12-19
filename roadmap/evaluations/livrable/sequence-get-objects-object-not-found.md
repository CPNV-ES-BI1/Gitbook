# Sequence - Get Objects - Object Not Found

## Intention

Ce document présente l'architecture ainsi que la logique à mettre en oeuvre pour la gestion des erreurs.

Le cas qui est décrit est celui d'un "ObjectNotFoundException". La stratégie devra être étendue à toutes les erreurs levées par le SDK.

La classe de test n'est pas mentionnée ici, mais bien entendu il est important d'intégrer les scénarios de tests impliquant des exceptions.

Tout comme pour les cas nominaux (sans exception), vous aurez besoin des interfaces en provenance du _SDK_ spécifique au _provider_ tout comme des classes d'exception.&#x20;

La classe d'implémentation (AWSBucketAdapterImplemention) devra être capable de "catch" les erreurs du _SDK_, mais bien retourner des exceptions découplées du _provider_.

Cette Erreur "métier" (ObjectNotFoundException) remontera jusqu'au _controller_ qui lui appliquera la normes HTTP pour transmettre le bon code.

{% embed url="https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status" %}

## Le diagramme de classe (simplifié)

<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

## La séquence

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

