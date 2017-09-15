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
            "publicationDate": "Mon Sep 11 13:12:00 GMT 2017",
            "expirationDate": "Mon Sep 11 13:12:00 GMT 2017"
        },
        {
            "id": "279801",
            "title": "Ma super notif",
            "description": "Ma super notif",
            "url": "",
            "type": "Type de notification 1",
            "typeId": "TYPE_1",
            "isRead": true,
            "publicationDate": "Mon Dec 03 10:15:30 GMT 2007",
            "expirationDate": "Fri Dec 03 10:15:30 GMT 2027"
        }
    ]
}
```

Ce endpoint permet de récupérer la liste des notifications d'un utilisateurs.
