# Mise en place de l'environnement

## Intention

Ce laboratoire a pour intention de mettre en place votre environnement de développement afin de rapidement débuter une première implémentation.

Il s'agit égaleemnt de réactiver certaines compétences comme l'UML, les API, la gestion des variables, les pratiques de code tels que les conventional commit et les différents git flow.

## Backlog

### Choix d'un framework

Vous êtes libres dans le choix du langage et du Framework que vous désirez utiliser pour le module. Prenez bien garde à valider les informations suivantes:

* [ ] Framework adapté pour la réalisation d'API (en vue de faire des micro-services)
* [ ] Librairies de test offrant des objets de tests tels que les mocks ou des stubs.
* [ ] Gestion "facilité" injection de dépendences
* [ ] Voici l'architecture à respecter pour vos futurs projets (avec les différences ihérentes à votre langage, bien entendu):

```
└───ms-products
    │   .env
    │   .gitignore
    │   package-lock.json
    │   package.json
    │   products.sqlite
    │   README.md
    │
    ├───docs
    │       class_diagram_micro_services.puml
    │
    └───src
        │   app.js
        │   server.js
        │
        ├───config
        │       database.js
        │       swagger.js
        │
        ├───controllers
        │       product.js
        │
        ├───entities
        │       Product.js
        │
        ├───routes
        │       products.js
        │       router.js
        │
        └───services
                product.js
```

