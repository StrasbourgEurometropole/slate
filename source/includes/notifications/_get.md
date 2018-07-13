## Liste des notifications d'un utilisateurs

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/get-user-notifications"
  -H "Authorization: Basic KEY"  
  -F "userId=USER_ID"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "notifications": [
        {
            "id": "279201",
            "title": "Notification de type 1",
            "description": "Notification de type 1",
            "url": "",
            "type": "Type de notification 1",
            "typeId": "TYPE_1",
            "isRead": false,
            "publicationDate": "2018-01-01 12:00:00",
            "expirationDate": "2019-01-01 12:00:00"
        },
        {
            "id": "279801",
            "title": "Ma super notif",
            "description": "Ma super notif",
            "url": "",
            "type": "Type de notification 1",
            "typeId": "TYPE_1",
            "isRead": true,
            "publicationDate": "2018-06-01 12:00:00",
            "expirationDate": "2019-06-01 12:00:00"
        }
    ]
}
```

Ce endpoint permet de récupérer la liste des notifications d'un utilisateurs.
