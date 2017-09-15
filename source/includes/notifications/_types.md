## Liste des types de notification

```shell
curl "https://www.strasbourg.eu/api/jsonws/notification.notification/get-types"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "types": [
        {
            "id": "TYPE_1",
            "name": {
                "fr_FR": "Type de notification 1"
            }
        },
        {
            "id": "TYPE_2",
            "name": {
                "fr_FR": "Type de notification 2"
            }
        }
    ]
}
```

Ce endpoint renvoie la liste des types de notification.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/notification.notification/get-types`

