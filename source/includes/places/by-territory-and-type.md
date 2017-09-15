## Liste des lieux par territoire et type

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-territory-and-type/territory-id/P_FR/type-id/<ID_TYPE>"
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

Ce endpoint renvoie la liste des lieux correspondant à l'identifiant SIG du territoire et à l'identifiant SIG du type de lieu passés en paramètres.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-territory-and-type/territory-id/<ID_TERRITORY>/type-id/<ID_TYPE>`

### Paramètres

Paramètre | Description
--------- | -----------
TERRITORY_ID | Identifiant SIG du territoire
TYPE_ID | Identifiant SIG du type de lieu
