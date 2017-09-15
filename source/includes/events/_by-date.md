## Liste des événements par date

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-date/date/01102018"
  -H "Authorization: Basic KEY"
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

Paramètre | Description
--------- | -----------
DATE | Date au format ddMMyyyy (exemple : 1er octobre 2018 devient 01102018)
