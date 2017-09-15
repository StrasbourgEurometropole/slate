## Liste des centres d'intérêt d'un utilisateur

```shell
curl -X POST "https://www.strasbourg.eu/api/jsonws/interest.interest/get-user-interests"  
  -F "userId=USER_ID"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
    "userId": "M0cG+MtX8/Zr+zSMuI+H7yTC7SeEHT/tvYr1BsdqZic=",
    "interests": [
        "275303"
    ]
}
```

Ce endpoint renvoie la liste des identifiants des centres d'intérêt d'un utilisateur.


### Paramètres

Paramètre | Description
--------- | -----------
USER_ID | Identifiant de l'utilisateur dans la base Publik
