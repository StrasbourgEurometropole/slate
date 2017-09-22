## Mise à jour des centres d'intérêt d'un utilisateur

```shell
curl -X POST https://www.strasbourg.eu/api/jsonws/interest.interest/set-user-interests"
  -F "userId=USERID"
  -F "interestIds=INTEREST_IDS"
  -H "Authorization: Basic KEY"
```

> La réponse est un des deux objet suivant :

```json
{
    "userId": "M0cG+MtX8/Zr+zSMuI+H7yTC7SeEHT/tvYr1BsdqZic=",
    "interests": [
        "275303"
    ]
}
```

```json
{
    "error": "MESSAGE"
}
```

### Paramètres

Paramètre | Description
--------- | -----------
userId | Identifiant de l'utilisateur dans la base Publik
interestIds | Liste de tous les centres d'intérêt à assigner à l'utilisateur séparés par des virgules (chaîne vide pour supprimer tous les centres d'intérêts de l'utilisateur)

### Messages d'erreurs

Message | Cause
--------|--------
not authorized | L'utilisateur accédant au endpoint n'a pas les droits nécessaires à la réalisation de cette action
invalid format for id of interest | Le format du paramètre "interestIds" n'est pas correct
interest does not exist | Le centre d'intérêt n'existe pas