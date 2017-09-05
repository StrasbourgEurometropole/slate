# Centres d'intérêt

## Liste des centres d'intérêt

```shell
curl "https://www.strasbourg.eu/api/jsonws/interest.interest/get-interests"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "275305",
    "name": "Centre d'intérêt 2",
    "description": "Centre d'intérêt 2",
    "typeId": "275302",
    "type": "Type de centre d'intérêt 1"
    "categories": [
      "188274"
    ],
  },
  {
    "id": "275303",
    "name": "Centre d'intérêt 1",
    "description": "Centre d'intérêt 1",
    "typeId": "275302",
    "type": "Type de centre d'intérêt 1"
    "categories": [
      "188064",
      "188274"
    ],
  }
]
```

Ce endpoint renvoie la liste de tous les centres d'intérêts publiés.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/interest.interest/get-interests`

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

## Mise à jour des centres d'intérêt d'un utilisateur

```shell
curl -X POST https://www.strasbourg.eu/api/jsonws/interest.interest/set-user-interests"
  -F "userId=USERID"
  -F "interestIds=INTEREST_IDS"
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

### Paramètres

Paramètre | Description
--------- | -----------
USER_ID | Identifiant de l'utilisateur dans la base Publik
INTEREST_IDS | Liste de tous les centres d'intérêt à assigner à l'utilisateur séparés par des virgules (chaîne vide pour supprimer tous les centres d'intérêts de l'utilisateur)