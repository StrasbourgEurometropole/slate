## Mise à jour des paramètres de notification d'un utilisateur

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/set-user-settings"
  -F "userId=USER_ID"
  -F "typeIds=TYPE_IDS"
  -F "channelIds=CHANNEL_IDS"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante en cas de succès :

```json
{
    "types": [
        {
            "name": {
                "fr_FR": "Type de notification 1"
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

> En cas d'erreur, la structure suivante est renvoyée :

```json
{
    "error": "MESSAGE"
}
```

Ce endpoint permet de mettre à jour les réglages d'un utilisateur.

### Paramètres

Paramètre | Description
--------- | -----------
USER_ID | Identifiant de l'utilisateur dans la base Publik
TYPE_IDS | Liste de tous les types de notification à assigner à l'utilisateur séparés par des virgules (chaîne vide pour supprimer tous les centres d'intérêts de l'utilisateur)
CHANNEL_IDS | Liste de tous les canaux de notification à assigner à l'utilisateur séparés par des virgules (chaîne vide pour supprimer tous les centres d'intérêts de l'utilisateur)


### Messages d'erreurs

Message | Cause
--------|--------
not authorized | L'utilisateur accédant au endpoint n'a pas les droits nécessaires à la réalisation de cette action
type does not exist | Le type n’existe pas
incorrect typeIds value | Le format du champ (ids séparés par des virgules) n'est pas respecté
channel does not exist | Le canal n'existe pas
incorrect channelIds value | Le format duc hamp (ids séparés par des virgules) n'est pas respecté

