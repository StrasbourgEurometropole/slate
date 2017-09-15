## Ajout d'un favoris

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/favorite.favorite/add-favorite"
  -F "userId=USER_ID"
  -F "typeId=TYPE_ID"
  -F "title=TITLE"
  -F "url=URL"
  -F "entityId=ENTITY_ID"
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

Ce endpoint permet de créer un nouveau favoris.

### Paramètres

Paramètre | Description
--------- | -----------
USER_ID | Identifiant de l'utilisateur dans la base Publik
TYPE_ID | Type du favoris
TITLE | Titre du favoris
URL | URL cible du favoris
ENTITY_ID | Identifiant de l'entité mise en favoris - s'il ne s'agit pas d'une entité de Strasbourg.eu, passer la valeur 0 en paramètre

### Messages d'erreurs

Message | Cause
--------|--------
not authorized | L'utilisateur accédant au endpoint n'a pas les droits nécessaires à la réalisation de cette action
type does not exist | Le type n’existe pas
entity does not exist | L'entité n'existe pas
unknown error | Erreur inconnue

### Message de succès

Message | Cause
--------|--------
favorite added | Favoris ajouté
