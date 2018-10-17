## Liste des lieux par territoire

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-places-by-territory/territory-id/P_FR"
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

Ce endpoint renvoie la liste des lieux correspondant à l'identifiant SIG du territoire passé en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-places-by-territory/territory-id/<ID_TERRITORY>`

### Paramètres

Paramètre | Description
--------- | -----------
TERRITORY_ID | Identifiant SIG du territoire
