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

Paramètre | Description
--------- | -----------
ID | Identifiant du lieu

