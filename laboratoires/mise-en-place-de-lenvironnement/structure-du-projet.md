# Structure du projet

## Structure des répertoires et fichiers

```
`└───ms-products
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

## Diagramme de classes

<figure><img src="../../../.gitbook/assets/class_diagram-microservice-3-Layers.png" alt=""><figcaption></figcaption></figure>

{% file src="../../../.gitbook/assets/class_diagram.puml" %}
