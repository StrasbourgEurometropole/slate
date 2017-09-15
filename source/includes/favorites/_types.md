## Liste des types de favoris

```shell
curl "https://www.strasbourg.eu/api/jsonws/favorite.favorite/get-types"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "types": [
        {
            "id": "1",
            "name": "PLACE"
        },
        {
            "id": "2",
            "name": "EVENT"
        },
        {
            "id": "3",
            "name": "VIDEO"
        },
        {
            "id": "4",
            "name": "EDITION"
        },
        {
            "id": "5",
            "name": "IMAGE"
        },
        {
            "id": "6",
            "name": "NEWS"
        },
        {
            "id": "7",
            "name": "ARTICLE"
        },
        {
            "id": "8",
            "name": "PROCEDURE",
        }
    ]
}
```

Ce endpoint renvoie la liste des types de favoris.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/favorite.favorite/get-types`