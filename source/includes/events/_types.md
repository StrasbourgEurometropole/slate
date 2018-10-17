## Liste des types d'événements

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-types"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {    
    "id": "1",
    "name": {
      "fr_FR": "Concert",
      "en_US": "Concert"
    }
  },
  {
    "id": "2"
    "name": {
      "fr_FR": "Exposition",
      "en_US": "Exhibition"
    }
  },
  {
    "id": "3"
    "name": {
      "fr_FR": "Exposition d'art contemporain",
      "en_US": "Modern art exhibition"
    },
    "level": 1,
    "parentId": "2"
  }
]
```

Ce endpoint renvoie la liste des types d'événements.

<aside class="notice">Un type peut avoir un type parent. La profondeur de la catégorie dans l'arbre global est indiqué par la propriété "level" et l'identifiant de la catégorie parente par "parentId". Une catégorie racine n'a pas de propriété "level", une catégorie ayant un parent possède un level de 1, deux parents 2, etc.</aside>

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-types`

