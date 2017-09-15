## Liste des services gestionnaires

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-services
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante

```json
[
  {    
    "id": "1",
    "name": {
      "fr_FR": "Service 1"
    }
  },
  {
    "id": "2"
    "name": {
      "fr_FR": "Service 2"
    }
  }
]
```

Ce endpoint renvoie la liste des services gestionnaires des événements.

<aside class="notice">Un territoire peut avoir un territoire parent. La profondeur de la catégorie dans l'arbre global est indiqué par la propriété "level" et l'identifiant de la catégorie parente par "parentId"</aside>

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-services`
