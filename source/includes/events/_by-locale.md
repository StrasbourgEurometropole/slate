## Liste des événements par langue

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-language/language/fr_FR"
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

Ce endpoint renvoie la liste des événements qui possèdent une traduction dans la langue donnée.

<aside class="notice">
  Sur Strasbourg.eu, les événements peuvent être dispoonbiles en Français ("fr_FR"), anglais ("en_US") et/ou allemand ("de_DE").
</aside>

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-language/language/<LANGUAGE>`

### Paramètres

Paramètre | Description
--------- | -----------
LANGUAGE | Langue : "fr_FR" pour le français, "en_US" pour l'anglais, "de_DE" pour l'allemand

