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

| Avain | Läsnä | Tyyppi | Kuvaus |
| --- | --- | --- | --- |
| `meta` | aina | object | Sisältää dokumentin metatiedot |
| `items` | aina  | array | Sisältää teosobjektit |

### meta

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
| --- | --- | -- | -- | -- |
| `createdBy` | aina | string |  Identifioi dokumentin tuottajan | email |
| `createdAt` | aina | string |  Dokumentin luomisaika | ISO 8601 |
| `license` | aina | object |  Dokumentin käyttöehdot |  |
| `composer` | aina | object | Dokumentin sisällön kuvaus |  |
| `apiVersion` | aina | string |  Dokumentin tuottanut rajapinta |  |

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

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `name` | aina | string |  Dokumentin lisenssi |  |
| `url` | aina | string |  Lisenssin osoite | url |


#### meta.composer

```JSON
"composer": {
  "name": ,
  "id": ,
  "kantoUri": ,
  "url": ,
  "introduction": [

  ],
  "workCategories": [
              
  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `name` | aina | string | Säveltäjän nimi  |  |
| `id` | aina | string | Säveltäjän tunniste | name-{uuid} |
| `kantoUri` | joskus | string | Säveltäjän KANTO URI  | uri |
| `url` | joskus | string |  Teosluettelon osoite  | url |
| `introduction` | joskus | array |  Teosluettelon esipuhe  |  |
| `workCategories` | joskus | array |  Säveltäjälle määritellyt teoskategoriat  |  |

#### meta.composer.name

Säveltäjän nimi 

```JSON
"name": "Pingoud, Ernest, 1887-1942",
```

#### meta.composer.id

Säveltäjän tunniste 

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
```

#### meta.composer.kantoUri

Säveltäjän KANTO URI

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455",
```

#### meta.composer.url

Teosluettelon osoite

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud",
```

#### meta.composer.introduction

 Teosluettelon esipuhe

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `locale` | aina | string |  Esipuheen kieli  | ISO 639-1  |
| `text` | aina | string | Teosluettelon esipuhe | |
| `author` | joskus | string | Eipuheen kirjoittaja | |
| `url` | joskus | string |  Esipuheen osoite  | url |

```JSON
"introduction": [
  {
    "locale": "fi",
    "text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n",
    "author": "Jaska Järvilehto",
    "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe"
  }
],
```

#### meta.composer.workCategories

Säveltäjälle määritellyt teoskategoriat

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `code` | aina | string | Teoskategorian koodi  |   |
| `label` | aina | string | Teoskategorian otsikko | |

```JSON
"workCategories": [
  {
    "code": "withOpusNumber",
    "label": {

    }
  }
]
```

#### meta.composer.workCategories.label

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `locale` | aina | string |  Teoskategorian otsikon kieli | ISO 639-1  |
| `text` | aina | string | Teoskategorian otsikko | |

```JSON
"label": {
  "locale": "fi",
  "text": "Opusnumeroidut teokset"
}
```

#### meta.apiVersion

Dokumentin tuottanut rajapinta

```JSON
"apiVersion": "v1"
```



### items

