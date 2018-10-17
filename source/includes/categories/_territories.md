## Liste des territoires

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-territories"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {    
    "id": "1",
    "name": {
      "fr_FR": "Allemagne",
      "en_US": "Germany"
    }
  },
  {
    "id": "2"
    "name": {
      "fr_FR": "France",
      "en_US": "France"
    }
  },
  {
    "id": "3"
    "name": {
      "fr_FR": "Strasbourg",
      "en_US": "Strasbourg"
    },
    "level": 1,
    "parentId": "2"
  },
  {
    "id": "4"
    "name": {
      "fr_FR": "Centre",
      "en_US": "City center"
    },
    "level": 2,
    "parentId": "3"
  }
]
```

Ce endpoint renvoie la liste des territoires pouvant être référencés par d'autres entités, comme les événements où les lieux.

<aside class="notice">Un territoire peut avoir un territoire parent. La profondeur de la catégorie dans l'arbre global est indiqué par la propriété "level" et l'identifiant de la catégorie parente par "parentId"</aside>

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-territories`
