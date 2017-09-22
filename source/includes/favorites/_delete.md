## Suppression d'un favoris

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/favorite.favorite/add-favorite"
  -F "userId=USER_ID"
  -F "favoriteId=FAVORITE_ID"
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

Ce endpoint permet de supprimer un favoris.

### Paramètres

Paramètre | Description
--------- | -----------
userId | Identifiant de l'utilisateur dans la base Publik
favoriteId | Identifiant du favoris

### Messages d'erreurs

Message | Cause
--------|--------
not authorized | L'utilisateur accédant au endpoint n'a pas les droits nécessaires à la réalisation de cette action
favorite does not exist | Le favoris n'existe pas
favorite does not belong to user | Le favoris existe mais n'appartient pas à l'utilisateur passé en paramètre
unknown error | Erreur inconnue

### Message de succès

Message | Cause
--------|--------
favorite deleted | Favoris supprimé
