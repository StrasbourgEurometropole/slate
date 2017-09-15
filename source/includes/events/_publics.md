## Liste des publics

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-publics
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {    
    "id": "1",
    "name": {
      "fr_FR": "Moins de 14 ans",
      "en_US": "Under 14 years old"
    }
  },
  {
    "id": "2"
    "name": {
      "fr_FR": "De 14 à 18 ans",
      "en_US": "From 14 to 18 years old"
    }
  }
]
```

Ce endpoint renvoie la liste des types de publics susceptibles d'assister à un événement.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-publics`
