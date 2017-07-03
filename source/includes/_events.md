# Evénements

## Tous les événements


```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events"
  -H "Authorization: KEY"
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

## Evénement spécifique

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-event/id/2"
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante :

```json
{
  "id": "1",
  ...
}
```

Ce endpoint renvoie un événement spécifique.

## Liste des événements par date

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-date/date/01102018"
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    ...
  }, {
    "id": "2",
    ...
  },
  ...
]
```

Ce endpoint renvoie la liste des événements qui se déroulent un jour donné.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-date/date/<DATE>`

### Paramètres

Parameter | Description
--------- | -----------
DATE | Date au format ddMMyyyy (exemple : 1er octobre 2018 devient 01102018)

## Liste des événements par catégorie

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-category/categoryId/125"
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    ...
  }, {
    "id": "2",
    ...
  },
  ...
]
```

Ce endpoint renvoie la liste des événements qui possèdent une catégorie donnée.

<aside class="notice">
  Les catégories peuvent être des types, des thèmes, des publics ou des territoires. 
  Référez-vous à la documentation concernant les catégories pour savoir comment connaître ces différentes catégories et leurs identifiants.
</aside>

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-category/categoryId/<ID>`

### Paramètres

Parameter | Description
--------- | -----------
ID | Identifiant de la catégorie


## Liste des événements par lieu

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-place/placeSIGId/125"
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    ...
  }, {
    "id": "2",
    ...
  }
]
```

Ce endpoint renvoie la liste des événements qui se déroulent dans le lieu passé en paramètre.

<aside class="notice">
  Afin de connaître les différents lieux existant et de récupérer leurs identifiants, référez-vous à la documentation concernant les lieux.
</aside>

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-place/placeSIGId/<ID>`

### Paramètres

Parameter | Description
--------- | -----------
ID | Identifiant du lieu


## Liste des événements par langue

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-language/language/fr_FR"
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    ...
  }, {
    "id": "2",
    ...
  },
  ...
]
```

Ce endpoint renvoie la liste des événements qui possèdent une traduction dans la langue donnée.

<aside class="notice">
  Sur Strasbourg.eu, les événements peuvent être dispoonbiles en Français ("fr_FR"), anglais ("en_US") et/ou allemand ("de_DE").
</aside>

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-language/language/<LANGUAGE>`

### Paramètres

Parameter | Description
--------- | -----------
LANGUAGE | Langue : "fr_FR" pour le français, "en_US" pour l'anglais, "de_DE" pour l'allemand

