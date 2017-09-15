## Lieu par identifiant SIG

```shell
curl "https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-id-sig/sig-id/10_ENF_2"
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

`GET https://www.strasbourg.eu/api/jsonws/place.place/get-place-by-id-sig/sig-id/<ID_SIG>`

### Paramètres

Paramètre | Description
--------- | -----------
ID_SIG | Identifiant SIG du lieu

