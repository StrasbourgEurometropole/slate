## Liste des thèmes des événements

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-themes
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {    
    "id": "1",
    "name": {
      "fr_FR": "Eté",
      "en_US": "Summer"
    }
  },
  {
    "id": "2"
    "name": {
      "fr_FR": "Noël",
      "en_US": "Christmas"
    }
  },
  {
    "id": "3"
    "name": {
      "fr_FR": "Noël des enfants",
      "en_US": "Christmas for kids"
    },
    "level": 1,
    "parentId": "2"
  }
]
```

Ce endpoint renvoie la liste des thèmes des événements.

<aside class="notice">Un thème peut avoir un thème parent. La profondeur de la catégorie dans l'arbre global est indiqué par la propriété "level" et l'identifiant de la catégorie parente par "parentId"</aside>

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-themes`

