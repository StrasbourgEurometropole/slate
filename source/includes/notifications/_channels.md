## Liste des canaux de diffusion de notification

```shell
curl "https://www.strasbourg.eu/api/jsonws/notification.notification/get-channels"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "channels": [
        {
            "id": "1",
            "name": "email"
        },
        {
            "id": "2",
            "name": "phone"
        }
    ]
}
```

Ce endpoint renvoie la liste des canaux de notification proposés aux utilisateurs.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/notification.notification/get-channels`


