## Liste des événements par lieu

```shell
curl "https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-place/place-sig-id/885_CUL_36"
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
  }
]
```

Ce endpoint renvoie la liste des événements qui se déroulent dans le lieu passé en paramètre.

<aside class="notice">
  Afin de connaître les différents lieux existant et de récupérer leurs identifiants, référez-vous à la documentation concernant les lieux.
</aside>

### Requête HTTP

`GET https://www.strasbourg.eu/api/jsonws/agenda.event/get-events-by-place/place-sig-id/<ID>`

### Paramètres

Paramètre | Description
--------- | -----------
ID | Identifiant du lieu

