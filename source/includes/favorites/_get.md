## Liste des favoris d'un utilisateur

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/favorite.favorite/get-user-favorites"
  -H "Authorization: Basic KEY"  
  -F "userId=USER_ID"
```

> La réponse est un des deux objet suivant :

```json
{
    "favorites": [
        {
            "id": "281701",
            "title": "Mon événement",
            "url": "",
            "entityId": "190665",
            "entityTitle": "Le ballet des ombres heureuses",
            "typeId": "2"
        },
        {
            "id": "281702",
            "title": "Mon lieu",
            "url": "",
            "entityId": "153866",
            "entityTitle": "Crèche collective et halte garderie de la Maison de l’enfance",
            "typeId": "1",
        }
    ]
}
```

```json
{
    "error": "MESSAGE"
}
```

Ce endpoint permet de récupérer la liste des favoris d'un utilisateur.

Le champ "entityTitle" n'est retourné que pour les types correspondant à une entité de Strasbourg.eu (actuellement tout sauf les procédures).

### Paramètres

Paramètre | Description
--------- | -----------
userId | Identifiant de l'utilisateur dans la base Publik

### Messages d'erreurs

Message | Cause
--------|--------
not authorized | L'utilisateur accédant au endpoint n'a pas les droits nécessaires à la réalisation de cette action