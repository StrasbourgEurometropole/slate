# Notifications

## Types de notification

```shell
curl "https://www.strasbourg.eu/api/jsonws/notification.notification/get-types"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
    {
        "name": {
            "en_US": "Type de notification 1"
        },
        "id": "TYPE_1"
    },
    {
        "name": {
            "en_US": "Type de notification 2"
        },
        "id": "TYPE_2"
    }
]
```

Ce endpoint renvoie la liste des types de notification.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/notification.notification/get-types`

## Canaux de notification

```shell
curl "https://www.strasbourg.eu/api/jsonws/notification.notification/get-channels"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
    {
        "name": "email",
        "id": "1"
    },
    {
        "name": "phone",
        "id": "2"
    }
]
```

Ce endpoint renvoie la liste des canaux de notification proposés aux utilisateurs.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/notification.notification/get-channels`


## Réglages utilisateurs

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/get-user-settings"
  -H "Authorization: Basic KEY"  
  -F "userId=USER_ID"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "types": [
        {
            "name": {
                "fr_FR": "Type de notification 1"
            },
            "id": "TYPE_1"
        },
        {
            "name": {
                "fr_FR": "Type de notification 2"
            },
            "id": "TYPE_2"
        }
    ],
    "channels": [
        "EMAIL"
    ],
    "userId": "USER_ID"
}
```

Ce endpoint renvoie la liste des types de notifications auxquels l'utilisateur est abonné ainsi que la liste des canaux qu'il a choisi.


### Paramètres

Paramètre | Description
--------- | -----------
USER_ID | Identifiant de l'utilisateur dans la base Publik


## Mise à jour des réglages d'un utilisateur

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/set-user-settings"
  -F "userId=USER_ID"
  -F "typeIds=TYPE_IDS"
  -F "channelIds=CHANNEL_IDS"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "types": [
        {
            "name": {
                "en_US": "Type de notification 1"
            },
            "id": "TYPE_1"
        }
    ],
    "channels": [
        "PHONE"
    ],
    "userId": "M0cG+MtX8/Zr+zSMuI+H7yTC7SeEHT/tvYr1BsdqZic="
}
```

Ce endpoint permet de mettre à jour les réglages d'un utilisateur.

### Paramètres

Paramètre | Description
--------- | -----------
USER_ID | Identifiant de l'utilisateur dans la base Publik
TYPE_IDS | Liste de tous les types de notification à assigner à l'utilisateur séparés par des virgules (chaîne vide pour supprimer tous les centres d'intérêts de l'utilisateur)
CHANNEL_IDS | Liste de tous les canaux de notification à assigner à l'utilisateur séparés par des virgules (chaîne vide pour supprimer tous les centres d'intérêts de l'utilisateur)


## Notifications utilisateurs

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
            "isRead": false,
            "description": "Notification de type 1",
            "id": "279201",
            "title": "Notification de type 1",
            "type": "Type de notification 1",
            "publicationDate": "Mon Sep 11 13:12:00 GMT 2017",
            "url": "",
            "expirationDate": "Mon Sep 11 13:12:00 GMT 2017"
        },
        {
            "isRead": true,
            "description": "Ma super notif",
            "id": "279801",
            "title": "Ma super notif",
            "type": "Type de notification 1",
            "publicationDate": "Mon Dec 03 10:15:30 GMT 2007",
            "url": "",
            "expirationDate": "Fri Dec 03 10:15:30 GMT 2027"
        }
    ]
}
```

Ce endpoint permet de récupérer la liste des notifications d'un utilisateurs.

## Ajout d'une notification

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/set-user-settings"
  -F "isGlobal=IS_GLOBAL"
  -F "userId=USER_ID"
  -F "typeId=TYPE_IDS"
  -F "title=TITLE"
  -F "description=DESCRIPTION"
  -F "url=URL"
  -F "publicationDate=PUBLICATION_DATE"
  -F "expirationDate=EXPIRATION_DATE"
  -F "url=URL"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "types": [
        {
            "name": {
                "en_US": "Type de notification 1"
            },
            "id": "TYPE_1"
        }
    ],
    "channels": [
        "PHONE"
    ],
    "userId": "M0cG+MtX8/Zr+zSMuI+H7yTC7SeEHT/tvYr1BsdqZic="
}
```

Ce endpoint permet de mettre à jour les réglages d'un utilisateur.

### Paramètres

Paramètre | Description
--------- | -----------
IS_GLOBAL | "true" si la notification doit être envoyée à tous les utilisateurs abonnés au type, false" si la notification s'applique à un utilisateur en particulier
USER_ID | Identifiant de l'utilisateur dans la base Publik, doit être vide si IS_GLOBAL est "true"
TYPE_ID | Type de la notification
TITLE | Titre de la notification
DESCRIPTION | Description de la notification
URL | Si la notification correspond à une page en particulier, URL de cette page, sinon chaîne vide
PUBLICATION_DATE | Date d'envoi de la notification (format YYYY-mm-DDTHH-MM-SS)
EXPIRATION_DATE | Date d'expiration de la notification, forcément ultérieure à la date de publication (format YYYY-mm-DDTHH-MM-SS)
