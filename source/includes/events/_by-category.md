## Liste des événements par catégorie

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-category/category-id/125"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    ...
  }, {
    "id": "2",
    ...
  },
  ...
]
```

Ce endpoint renvoie la liste des événements qui possèdent une catégorie donnée.

<aside class="notice">
  Les catégories peuvent être des types, des thèmes, des publics ou des territoires. 
  Référez-vous à la documentation concernant les catégories pour savoir comment connaître ces différentes catégories et leurs identifiants.
</aside>

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-category/category-id/<ID>`

### Paramètres

Paramètre | Description
--------- | -----------
ID | Identifiant de la catégorie
