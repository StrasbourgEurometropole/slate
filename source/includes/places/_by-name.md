## Liste des lieux par nom

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-places-by-name-and-language/name/piscine/language/fr_FR
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

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-places-by-name-and-language/name/<NAME>/language/fr_FR`

### Paramètres

Paramètre | Description
--------- | -----------
NAME | Mot-clé de recherche
