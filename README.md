# ohjeluettelot-json

## In English

To do

## Dokumentin rakenne

```JSON
{
  "meta": {

  },
  "items": [

  ]
}
```

| Avain | Pakollinen | Tyyppi | Kuvaus |
| --- | --- | --- | --- |
| `meta` | kyllä | object | Sisältää dokumentin metatiedot |
| `items` | kyllä  | array | Sisältää teosobjektit |

### meta

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

| Avain | Pakollinen | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `createdBy` | kyllä | string |  Identifioi dokumentin tuottajan | email |
| `createdAt` | kyllä | string |  Dokumentin luomisaika | ISO 8601 |
| `license` | kyllä | object |  Dokumentin käyttöehdot |  |
| `composer` | kyllä | object | Dokumentin sisällön kuvaus |  |
| `apiVersion` | kyllä | string |  Dokumentin tuottanut rajapinta |  |

#### meta.createdBy

```JSON
"createdBy": "info@musiikinluettelointi.fi",
```

#### meta.createdAt

```JSON
"createdAt": "2023-10-31T16:54:50.265847Z",
```

#### meta.license

```JSON
"license": {
  "name": "CC0 1.0 Universal",
  "url": "http://creativecommons.org/publicdomain/zero/1.0"
},
```

| Avain | Pakollinen | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `name` | kyllä | string |  Dokumentin lisenssi |  |
| `url` | kyllä | string |  Lisenssin osoite | url |


#### meta.composer

```JSON
    "composer": {
            "name": "Pingoud, Ernest, 1887-1942",
            "id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
            "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455",
            "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud",
            "introduction": [
                {
                    "locale": "fi",
                    "text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n",
                    "author": "Jaska Järvilehto",
                    "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe"
                }
            ],
            "workCategories": [
                {
                    "code": "withOpusNumber",
                    "label": {
                        "locale": "fi",
                        "text": "Opusnumeroidut teokset"
                    }
                },
                {
                    "code": "withoutOpusNumber",
                    "label": {
                        "locale": "fi",
                        "text": "Opusnumerottomat teokset"
                    }
                }
            ]
        },
```

#### meta.apiVersion

```JSON
   "meta": {
        "createdBy": "info@musiikinluettelointi.fi",
        "createdAt": "2023-10-31T16:54:50.265847Z",
        "license": {
            "name": "CC0 1.0 Universal",
            "url": "http://creativecommons.org/publicdomain/zero/1.0"
        },
        "composer": {
            "name": "Pingoud, Ernest, 1887-1942",
            "id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
            "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455",
            "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud",
            "introduction": [
                {
                    "locale": "fi",
                    "text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n",
                    "author": "Jaska Järvilehto",
                    "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe"
                }
            ],
            "workCategories": [
                {
                    "code": "withOpusNumber",
                    "label": {
                        "locale": "fi",
                        "text": "Opusnumeroidut teokset"
                    }
                },
                {
                    "code": "withoutOpusNumber",
                    "label": {
                        "locale": "fi",
                        "text": "Opusnumerottomat teokset"
                    }
                }
            ]
        },
        "apiVersion": "v1"
    },
```

### items

