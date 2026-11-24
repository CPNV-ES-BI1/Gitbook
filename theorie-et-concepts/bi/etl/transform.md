# Transform

## Principe de base

La transformation constitue une étape essentielle de l'ETL.

Elle consiste à convertir les données brutes en données cohérentes et exploitables, conformément aux règles métier définies.

Les opérations possibles sont notamment:

* Nettoyage: suppression des données incorrectes ou inutiles
* Filtrage: conservation uniquement des informations pertinentes.
* Agrégation: regroupement et calcul de données.
* Déduplication: suppression des doublons.
* Validation: vérification de la conformité des données.
* Normalisation: harmonisation des formats et des structures
* Enrichissement: ajout d'informations complémentaires
* Conversion: changement de formats, de devises ou d'unités.
* Sécurisation: suppression, chiffrement ou masquage des données sensibles.

Les données sont ensuite organisées selon le schéma attendu par le système cible.

## En détail

{% embed url="https://aws.amazon.com/what-is/etl/#amsc7--32b7yl" %}

**Transformations de base** : elles améliorent la qualité des données en corrigeant les erreurs, en traitant les champs vides ou en simplifiant les données.

* **Nettoyage (**_**cleansing**_**)** : suppression des erreurs et mise en correspondance des données sources avec le format cible. Par exemple, remplacer un champ vide par 0, ou « Parent » par « P » et « Child » par « C ».
* **Déduplication** : identification et suppression des enregistrements en double.
* **Révision de format** : uniformisation des jeux de caractères, des unités de mesure et des dates/heures. Exemple : un fabricant alimentaire dont certaines recettes sont en kilogrammes et d'autres en livres convertit tout en livres.

**Transformations avancées** : elles appliquent des règles métier pour optimiser les données en vue de l'analyse.

* **Dérivation** : calcul de nouvelles valeurs à partir de valeurs existantes (par exemple, profit = revenu − dépenses, ou coût total = prix unitaire × quantité).
* **Jointure (**_**joining**_**)** : rapprochement de données identiques provenant de différentes sources, par exemple additionner les montants d'achat d'un même article chez plusieurs fournisseurs et ne stocker que le total.
* **Séparation (**_**splitting**_**)** : découpage d'une colonne en plusieurs, comme un nom complet « Jane John Doe » en prénom, deuxième prénom et nom de famille.
* **Agrégation (**_**summarization**_**)** : réduction d'un grand nombre de valeurs en un jeu plus petit, par exemple additionner de nombreuses petites factures sur une période pour calculer la valeur vie client (CLV).
* **Chiffrement** : protection des données sensibles avant leur envoi vers la base cible, pour respecter les lois sur les données et la confidentialité.
