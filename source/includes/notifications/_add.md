## Ajout d'une notification

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/notification.notification/add-notification"
  -F "isGlobal=IS_GLOBAL"
  -F "userId=USER_ID"
  -F "typeId=TYPE_IDS"
  -F "title=TITLE"
  -F "description=DESCRIPTION"
  -F "url=URL"
  -F "publicationDate=PUBLICATION_DATE"
  -F "expirationDate=EXPIRATION_DATE"
  -H "Authorization: Basic KEY"
```


> La réponse est un des deux objet suivant :

```json
{
    "error": "MESSAGE"
}
```


```json
{
    "success": "MESSAGE"
}
```


Ce endpoint permet d'envoyer une nouvelle notification.

### Paramètres

Paramètre | Description
--------- | -----------
isGlobal | "true" si la notification doit être envoyée à tous les utilisateurs abonnés au type, "false" si la notification s'applique à un utilisateur en particulier
userId | Identifiant de l'utilisateur dans la base Publik, doit être vide si isGlobal est "true"
typeId | Type de la notification
title | Titre de la notification
description | Description de la notification
url | Si la notification correspond à une page en particulier, URL de cette page, sinon chaîne vide
publicationDate | Date d'envoi de la notification (format yyyy-MM-ddThh-mm-ss)
expirationDate | Date d'expiration de la notification, forcément ultérieure à la date de publication (format yyyy-MM-ddThh-mm-ss)

### Messages d'erreurs

Message | Cause
--------|--------
not authorized | L'utilisateur accédant au endpoint n'a pas les droits nécessaires à la réalisation de cette action
isGlobal is true but userId is not empty | Le paramètre isGlobal est "true" mais un userId a été passé passé en paramètre, si isGlobal est "true", userId doit être vide
user does not exist | Le userId ne correspond à aucun utilisateur connu chez nous
title is empty | Le titre est vide
description is empty | La description est vide
publication date is after expiration date | La date de publication est ultérieure à la date de dépublication
wrong date format | Le format de la date n’est pas correct
type does not exist | Le type n’existe pas
unknown error | Erreur inconnue

### Message de succès

Message | Cause
--------|--------
notification sent | Notification envoyée

