---
title: Strasbourg.eu - Référence de l'API

language_tabs:
  - shell
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Bienvenue sur la documentation des APIs de Strasbourg.eu. Ces APIs vous permettront d'accéder à différentes données de Strasbourg.eu comme les événements et les lieux de la ville de Strasbourg.

# Authentication

L'accès à l'API est protégé par une authentification HTTP. Vous devez posséder un compte utilisateur sur Strasbourg.eu pour y accéder.

Deux méthodes sont possibles pour utiliser l'API :

* Ajoutez le header HTTP suivant à chacune de vos requêtes, où la key est la valeur en base 64 de la chaine de caractères 'username:password' : `Authorization: KEY`, vous pouvez utiliser un encodeur en ligne comme [http://www.motobit.com/util/base64-decoder-encoder.asp](celui-ci) pour effectuer l'encodage

* Ajoutez 'username:password@' devant chaque URL des endpoints de l'API (`https://www.strasbourg.eu/api/...` devient `https://username:password@www.strasbourg.eu/api...`)
  

# Evénements

## Tous les événements


```shell
curl "https://strasbourg.eu/api/jsonws/agenda.event/get-events"
  -H "Authorization: KEY"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
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
      "accessForBlind": false,
      "accessForWheelchair": false,
      "accessForDeaf": false,
      "accessForDeficient": false,
      "accessForElder": false,
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

### Paramètres

*Aucun*

## Un événement spécifique

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-event/id/2"
  -H "Authorization: KEY"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> La structure JSON renvoyée est la suivante

```json
{
  "id": "1",
  ...
}
```

Ce endpoint renvoie un événement spécifique.

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-event/id/<ID>`

### Paramètres

Parameter | Description
--------- | -----------
ID | L'identifiant de l'événement à renvoyer
