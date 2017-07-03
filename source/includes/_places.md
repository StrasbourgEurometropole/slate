# Lieux

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
      "en_US": "Place name"
    },
    "description": {
      "fr_FR": "<p>Description du lieu</p>",
      "en_US": "<p>Place description</p>"
    },
    "imageURL": "https://strasbourg.eu/images/cathedrale-1.png",
    "imageCopyright": "Copyright de l'image principale",
    "images": [{
      "imageURL": "https://strasbourg.eu/images/cathedrale-2.png",
      "imageCopyright": "Copyright de l'image secondaire"
    }],
    "serviceAndActivities": {
      "fr_FR": "<p>Services et activités du lieu</p>",
      "en_US": "<p>Place services and activities</p>"
    },
    "characteristics": {
      "fr_FR": "<p>Caractéristiques du lieu</p>",
      "en_US": "<p>Place characteristics</p>"
    },
    "price": {
      "fr_FR": "<p>Tarifs du lieu</p>",
      "en_US": "<p>Place price</p>"
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
      "en_US": "Facebook page name",
    },
    "facebookURL": {
      "fr_FR": "URL de la page Facebook",
      "en_US": "Facebook page URL",
    },
    "websiteName":  {
      "fr_FR": "Nom du site internet",
      "en_US": "Website name",
    },
    "websiteURL": {
      "fr_FR": "URL du site internet",
      "en_US": "Website URL",
    },
    "access": {
      "fr_FR": "<p>Accès</p>",
      "en_US": "<p>Access</p>"
    },
    "accessForDisabled": {
      "fr_FR": "<p>Accès handicapé</p>",
      "en_US": "<p>Access for disabled people</p>"
    },
    "accessForBlind": true,
    "accessForWheelchair": true,
    "accessForDeaf": true,
    "accessForElder": true,
    "accessForDeficient": true,
    "periods": [{
      "periodName": {
        "fr_FR": "Nom de la période",
        "en_US": "Period name"
      },
      "startDate": "yyyy-MM-dd",
      "endDate": "yyyy-MM-dd",
      "scheduleLinkName": {
        "fr_FR": "Nom du lien vers le détail des horaires pour la période",
        "en_US": "Period schedule detail link name"
      },
      "scheduleLinkURL": {
        "fr_FR": "Lien vers le détail des horaires pour la période",
        "en_US": "Schedule detail link"
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
        "en_US": "Exception description"
      },
      "startDate": "yyyy-MM-dd",
      "endDate": "yyyy-MM-dd",
      "closed": false,
      "startHour": "hh:mm",
      "endHour": "hh:mm"
    }],
    "exceptionalSchedule": {
      "fr_FR": "Programme exceptionnel",
      "en_US": "Exceptionnal schedule"
    },
    "additionalInformation": {
      "fr_FR": "Informations complémentaires",
      "en_US": "Additional information"
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

## Lieu par identifiant

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-id/id/<ID>"
```

> La structure JSON renvoyée est la suivante :

```json
{
  "id": "1",
  ...
}
```

Ce endpoint renvoie le lieu correspondant à l'identifiant SIG passé en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-id/id/<ID>`

### Paramètres

Parameter | Description
--------- | -----------
ID | Identifiant du lieu

## Lieu par identifiant SIG

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-sig-id/sig-id/10_ENF_2"
```

> La structure JSON renvoyée est la suivante :

```json
{
  "id": "1",
  ...
}
```

Ce endpoint renvoie le lieu correspondant à l'identifiant SIG passé en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-sig-id/sig-id/Cat_06_01`

### Paramètres

Parameter | Description
--------- | -----------
ID_SIG | Identifiant SIG du lieu


## Liste des lieux par type

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-type/type-id/Cat_06_05"
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

Ce endpoint renvoie la liste des lieux correspondant à l'identifiant SIG du type de lieu passé en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-type/type-id/<ID_TYPE>`

### Paramètres

Parameter | Description
--------- | -----------
TYPE_ID | Identifiant SIG du type de lieu


## Liste des lieux par territoire

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-territory/territory-id/P_FR"
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

Ce endpoint renvoie la liste des lieux correspondant à l'identifiant SIG du territoire passé en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-territory/territory-id/<ID_TERRITORY>`

### Paramètres

Parameter | Description
--------- | -----------
TERRITORY_ID | Identifiant SIG du territoire


## Liste des lieux par territoire et type

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-territory-and-type/territory-id/P_FR/type-id/<ID_TYPE>"
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

Ce endpoint renvoie la liste des lieux correspondant à l'identifiant SIG du territoire et à l'identifiant SIG du type de lieu passés en paramètres.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-territory-and-type/territory-id/<ID_TERRITORY>/type-id/<ID_TYPE>`

### Paramètres

Parameter | Description
--------- | -----------
TERRITORY_ID | Identifiant SIG du territoire
TYPE_ID | Identifiant SIG du type de lieu


## Liste des lieux par nom

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-places-by-name-and-language/name/piscine/-language
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

Ce endpoint renvoie la liste des lieux ayant un nom contenant la chaîne de caractère passée en paramètre.

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-name-and-language/keyword/<KEYWORD>/-language

### Paramètres

Parameter | Description
--------- | -----------
KEYWORD | Mot-clé de recherche
