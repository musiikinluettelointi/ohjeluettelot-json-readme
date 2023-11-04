## meta

`object`

Tämä rakenne sisältää dokumentin metatiedot.

```JSON
 "meta": {
    "createdBy": ,
    "createdAt": ,
    "license": {

    },
    "composer": {

    },
    "apiVersion":
  },
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`createdBy`](#metacreatedby) | aina | string |  Dokumentin tuottaja | email |
| [`createdAt`](#metacreatedat) | aina | string |  Dokumentin luomisaika | ISO 8601 |
| [`license`](#metalicense) | aina | object |  Dokumentin käyttöehdot |  |
| [`composer`](#metacomposer) | aina | object | Säveltäjän tiedot |  |
| [`apiVersion`](#metaapiversion) | aina | string |  Dokumentin tuottanut rajapinta |  |