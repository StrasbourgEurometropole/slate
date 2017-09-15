## Tous les lieux

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-places"
```

> La structure JSON renvoyée est la suivante :

```json
[
  {
    "id": "1",
    "idSurfs": "ID_SIG",
    "name": {
      "fr_FR": "Nom du lieu",
      "fr_FR": "Place name"
    },
    "description": {
      "fr_FR": "<p>Description du lieu</p>",
      "fr_FR": "<p>Place description</p>"
    },
    "imageURL": "https://strasbourg.eu/images/cathedrale-1.png",
    "imageCopyright": "Copyright de l'image principale",
    "images": [{
      "imageURL": "https://strasbourg.eu/images/cathedrale-2.png",
      "imageCopyright": "Copyright de l'image secondaire"
    }],
    "serviceAndActivities": {
      "fr_FR": "<p>Services et activités du lieu</p>",
      "fr_FR": "<p>Place services and activities</p>"
    },
    "characteristics": {
      "fr_FR": "<p>Caractéristiques du lieu</p>",
      "fr_FR": "<p>Place characteristics</p>"
    },
    "price": {
      "fr_FR": "<p>Tarifs du lieu</p>",
      "fr_FR": "<p>Place price</p>"
    },
    "address": "Adresse complète"
    "distribution": "Distribution",
    "street": "Rue",
    "complement": "Complément d'adresse",
    "zipCode": "Code postal",
    "districtCode": "Code SIG du quartier",
    "cityCode": "Code SIG de la ville",
    "city": "Ville",
    "country": "Pays",
    "RGF93X": "Coordonnée Y RGF93",
    "RGF93Y": "Coordonnée X RGF93",
    "mercatorX": "Coordonnée X mercator",
    "mercatorY": "Coordonnée Y mercator",
    "types": [
      "TYPE_1",
      "TYPE_2"
    ],
    "mail": "contact@place.eu",
    "phone": "0101010101",
    "facebookName":  {
      "fr_FR": "Nom de la page Facebook",
      "fr_FR": "Facebook page name",
    },
    "facebookURL": {
      "fr_FR": "URL de la page Facebook",
      "fr_FR": "Facebook page URL",
    },
    "websiteName":  {
      "fr_FR": "Nom du site internet",
      "fr_FR": "Website name",
    },
    "websiteURL": {
      "fr_FR": "URL du site internet",
      "fr_FR": "Website URL",
    },
    "access": {
      "fr_FR": "<p>Accès</p>",
      "fr_FR": "<p>Access</p>"
    },
    "accessForDisabled": {
      "fr_FR": "<p>Accès handicapé</p>",
      "fr_FR": "<p>Access for disabled people</p>"
    },
    "accessForBlind": true,
    "accessForWheelchair": true,
    "accessForDeaf": true,
    "accessForElder": true,
    "accessForDeficient": true,
    "periods": [{
      "periodName": {
        "fr_FR": "Nom de la période",
        "fr_FR": "Period name"
      },
      "startDate": "yyyy-MM-dd",
      "endDate": "yyyy-MM-dd",
      "scheduleLinkName": {
        "fr_FR": "Nom du lien vers le détail des horaires pour la période",
        "fr_FR": "Period schedule detail link name"
      },
      "scheduleLinkURL": {
        "fr_FR": "Lien vers le détail des horaires pour la période",
        "fr_FR": "Schedule detail link"
      },
      "alwaysOpen": false,
      "schedules": [{
         "dayOfWeek": 0 à 6,
         "startHour": "hh:mm",
         "endHour": "hh:mm",
      },
      {
        ...
      }]
    },
    {
      ...
    }],
    "exceptions": [{
      "description": {
        "fr_FR": "Description de l'exception",
        "fr_FR": "Exception description"
      },
      "startDate": "yyyy-MM-dd",
      "endDate": "yyyy-MM-dd",
      "closed": false,
      "startHour": "hh:mm",
      "endHour": "hh:mm"
    }],
    "exceptionalSchedule": {
      "fr_FR": "Programme exceptionnel",
      "fr_FR": "Exceptionnal schedule"
    },
    "additionalInformation": {
      "fr_FR": "Informations complémentaires",
      "fr_FR": "Additional information"
    },
    "videos": ["https://youtube.com/AaaAaA", "https://youtube.com/bbBBBb"],
    "documents": ["https://strasbourg.eu/documents/programme.pdf"],
    "friendlyURL": "https://www.strasbourg.eu/-/entity/id/000001",
  }, {
    "id": "000002",
    ...
  }
]
```

Ce endpoint renvoie l'ensemble des lieux de l'Eurométropole de Strasbourg.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-places`

### Description des champs

*TODO*
