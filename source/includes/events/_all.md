## Tous les événements

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events"
  -H "Authorization: Basic KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    "externalId": "event_1",
    "title": {
      "fr_FR": "Titre de l'événement",
      "en_US": "Event title",
    },
    "subtitle": {
      "fr_FR": "Sous-titre de l'événement",
      "en_US": "Event subtitle"
    },
    "description": {
      "fr_FR": "<p>Description de l'événement</p>",
      "en_US": "<p>Event description</p>"
    },
    "imageURL": "http://URL_DE_L_ILLUSTRATION",
    "imageCopyright": "Copyright de l'image",
    "periods": [
      {
        "endDate": "yyyy-MM-dd",
        "startDate": "yyyy-MM-dd",
        "timeDetail": {
          "fr_FR": "De 16 à 18h",
          "de_DE": "From 4 to 6pm"
        },
      }
    ],
    "place": {
      "name": {
        "fr_FR": "Nom du lieu où l'événement à lieu",
        "en_US": "Event place name",
      },
      "streetNumber": "Numéro de la rue",
      "streetName": "Nom de la rue",
      "zipCode": "Code postal",
      "city": "Ville",
      "accessForBlind": true,
      "accessForWheelchair": true,
      "accessForDeaf": true,
      "accessForDeficient": true,
      "accessForElder": true,
      "access": {
        "fr_FR": "<p>Détails sur les accès au lieu de l'événement</p>",
        "en_US": "<p>Event access details</p>",
      },
      "accessForDisabled": {
        "fr_FR": "<p>Détails sur les accès au lieu de l'événement pour les personnes handicapées</p>",
        "en_US": "<p>Access details for disabled people</p>",
      },
    },
    "freeEntry": 2,
    "price": {
      "fr_FR": "<p>Tarifs de l'événement</p>",
      "en_US": "<p>Event price</p>",
    },
    "types": [
      "83504"
    ],
    "themes": [
      "126203"
    ],
    "territories": [
      "83503"
    ],
    "categories": [
      "83503",
      "83504",
      "126203"
    ],
    "eventURL": "https://www.strasbourg.eu/-/entity/id/000001",
  }, {
    "id": "000002",
    ...
  }
]
```

Ce endpoint renvoie l'ensemble des événements qui ont lieu dans l'Eurométropole de Strasbourg.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events`

### Description des champs

*TODO*