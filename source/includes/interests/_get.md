## Liste des centres d'intérêt

```shell
curl "https://www.strasbourg.eu/api/jsonws/interest.interest/get-interests"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "interests": [
        {
            "id": "275305",
            "name": "Centre d'intérêt 2",
            "description": "Centre d'intérêt 2",
            "typeId": "275302",
            "type": "Type de centre d'intérêt 1"
            "categories": [
                "188274"
            ],
        },
        {
            "id": "275303",
            "name": "Centre d'intérêt 1",
            "description": "Centre d'intérêt 1",
            "typeId": "275302",
            "type": "Type de centre d'intérêt 1"
            "categories": [
                "188064",
                "188274"
            ]
        }
    ]
}
```

Ce endpoint renvoie la liste de tous les centres d'intérêts publiés.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/interest.interest/get-interests`
