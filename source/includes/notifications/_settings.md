## Récupération des paramètres de notification d'un utilisateur

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/get-user-settings"
  -H "Authorization: Basic KEY"  
  -F "userId=USER_ID"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "userId": "M0cG+MtX8/Zr+zSMuI+H7yTC7SeEHT/tvYr1BsdqZic=",
    "types": [
        {
            "id": "TYPE_1",
            "name": {
                "fr_FR": "Type de notification 1"
            },
        },
        {
            "id": "TYPE_2",
            "name": {
                "fr_FR": "Type de notification 2"
            },
        }
    ],
    "channels": [
        "EMAIL"
    ]
}
```

Ce endpoint renvoie la liste des types de notifications auxquels l'utilisateur est abonné ainsi que la liste des canaux qu'il a choisi.


### Paramètres

Paramètre | Description
--------- | -----------
userId | Identifiant de l'utilisateur dans la base Publik


