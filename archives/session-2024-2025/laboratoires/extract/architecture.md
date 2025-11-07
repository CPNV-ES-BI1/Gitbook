# Architecture

## Backlog

* [ ] Comprendre l'approche "object storage" et son utilité dans un contexte BI.

{% embed url="https://www.ibm.com/topics/object-storage" %}
Introduction à l'Object Storage
{% endembed %}

* [ ] Etudier les documentations officielles de GCP, Azure et AWS concernant leur solution de "Object Storage" adapté au langage Java.

{% embed url="https://learn.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-java?tabs=powershell%2Cmanaged-identity%2Croles-azure-portal%2Csign-in-azure-cli&pivots=blob-storage-quickstart-scratch" %}
Documentation Azure Blob Storage - Java
{% endembed %}

{% embed url="https://cloud.google.com/storage/docs/reference/libraries#client-libraries-usage-java" %}
Documentation GCP Cloud Storage - Java
{% endembed %}

{% embed url="https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/examples-s3.html" %}
Documentation AWS S3 - Java
{% endembed %}

* [ ] Déduire une architecture de code permettant d'avoir un seul même composant qui sera capable de dialoguer avec les trois _providers_, en réduisant la quanité de code à produire et maintenir.

{% embed url="https://cpnv-es-ngy.gitbook.io/uml-backlog/archive/2023-2024/class-diagram/standards" %}
Normes UML à appliquer
{% endembed %}

* [ ] Opter pour un ou plusieurs patrons de conceptions

{% embed url="https://refactoring.guru/design-patterns" %}
