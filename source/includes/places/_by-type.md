## Liste des lieux par type

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-type/type-id/Cat_06_05"
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

Ce endpoint renvoie la liste des lieux correspondant à l'identifiant SIG du type de lieu passé en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-type/type-id/<ID_TYPE>`

### Paramètres

Paramètre | Description
--------- | -----------
TYPE_ID | Identifiant SIG du type de lieu


