# Catégories

## Liste des publics

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-publics
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante

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

## Liste des thèmes des événements

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-themes
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante

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


## Liste des types d'événements

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-types
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante

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

<aside class="notice">Un type peut avoir un type parent. La profondeur de la catégorie dans l'arbre global est indiqué par la propriété "level" et l'identifiant de la catégorie parente par "parentId"</aside>

### HTTP Request

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-types`


## Liste des territoires

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-territories
  -H "Authorization: KEY"
```

> La structure JSON renvoyée est la suivante

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
