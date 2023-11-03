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
| [`meta`](#meta) | aina | object | Sisältää dokumentin metatiedot |
| [`items`](#items) | aina  | array | Sisältää teosobjektit |

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
| [`createdBy`](#metacreatedby) | aina | string |  Dokumentin tuottaja | email |
| [`createdAt`](#metacreatedat) | aina | string |  Dokumentin luomisaika | ISO 8601 |
| [`license`](#metalicense) | aina | object |  Dokumentin käyttöehdot |  |
| [`composer`](#metacomposer) | aina | object | Säveltäjän tiedot |  |
| [`apiVersion`](#metaapiversion) | aina | string |  Dokumentin tuottanut rajapinta |  |

#### meta.createdBy

Dokumentin tuottaja.

```JSON
"createdBy": "info@musiikinluettelointi.fi",
```

#### meta.createdAt

Dokumentin luomisaika.

```JSON
"createdAt": "2023-10-31T16:54:50.265847Z",
```

#### meta.license

Dokumentin käyttöehdot.

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

Säveltäjän tiedot.

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
| `id` | aina | string | Säveltäjän tunniste teosluettelossa | name-{uuid} |
| `kantoUri` | joskus | string | Säveltäjän KANTO URI  | uri |
| `url` | joskus | string |  Teosluettelon osoite  | url |
| `introduction` | joskus | array |  Teosluettelon esipuhe  |  |
| `workCategories` | joskus | array |  Säveltäjälle määritellyt teoskategoriat  |  |

#### meta.composer.name

Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja.

```JSON
"name": "Pingoud, Ernest, 1887-1942",
```

#### meta.composer.id

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
```

#### meta.composer.kantoUri

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455",
```

#### meta.composer.url

Teosluettelon osoite. Kaikilla säveltäjillä ei ole julkista teosluetteloa.

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud",
```

#### meta.composer.introduction

 Teosluettelon esipuhe. Kaikille säveltäjille ei ole laadittu esipuhetta.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | -- | -- | -- |
| `locale` | aina | string |  Esipuheen kieli  | ISO 639-1  |
| `text` | aina | string | Teosluettelon esipuhe | |
| `author` | joskus | string | Esipuheen kirjoittaja | |
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

Säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

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

Teoskategorian otsikko.

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

### items.*

```JSON
"items": [
  {
    "itemType": ,
    "id": ,
    "composer": {
    
    },
    "authorizedTitle": {
    
    },
    "authorizedTitleHistory": [
    
    ],
    "alternativeTitle": [
    
    ],
    "workCategory": [
    
    ],
    "workNumber": [
    
    ],
    "creationYear": [
    
    ],
    "mediumOfPerformance": [
     
    ],
    "genre": [
      
    ],
    "sources": [
    
    ]
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus |
| --- | --- | --- | --- |
| `itemType` | aina | string | |
| `id` | aina  | string | |
| `composer` | joskus | object | |
| `authorizedTitle` | joskus  | array |  |
| `authorizedTitleHistory` | joskus | array |  |
| `alternativeTitle` | joskus  | array |  |
| `workCategory` | joskus | array |  |
| `workNumber` | joskus  | array |  |
| `creationYear` | joskus | array |  |
| `mediumOfPerformance` | joskus  | array |  |
| `genre` | joskus | array |  |
| `sources` | joskus  | array |  |

```JSON
{
            "itemType": "work",
            "id": "work-c10de676-0115-474f-895e-26940602371b",
            "composer": {
                "id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
                "name": "Pingoud, Ernest, 1887-1942",
                "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
            },
            "authorizedTitle": {
                "title": "Prologue, op4",
                "sources": [
                    {
                        "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                        "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                    }
                ]
            },
            "authorizedTitleHistory": [
                {
                    "createdAt": "2014-07-01",
                    "authorizedTitle": {
                        "title": "Prologue, op4",
                        "sources": [
                            {
                                "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                                "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                            }
                        ]
                    }
                }
            ],
            "alternativeTitle": [
                {
                    "title": "Prologue symphonique pour Grand Orchestre",
                    "language": {
                        "code": "fre",
                        "label": [
                            {
                                "locale": "fi",
                                "literal": "ranska"
                            }
                        ]
                    },
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                        }
                    ]
                }
            ],
            "workCategory": [
                {
                    "code": "withOpusNumber",
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "Opusnumeroidut teokset"
                        }
                    ]
                }
            ],
            "workNumber": [
                {
                    "number": "op4",
                    "type": {
                        "code": "opusNumber",
                        "label": [
                            {
                                "locale": "fi",
                                "literal": "opusnumero"
                            }
                        ]
                    },
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                        }
                    ]
                }
            ],
            "creationYear": [
                {
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "1915"
                        }
                    ],
                    "years": [
                        {
                            "year": 1915
                        }
                    ],
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                        }
                    ]
                }
            ],
            "mediumOfPerformance": [
                {
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "orkesteri"
                        }
                    ],
                    "items": [
                        {
                            "label": [
                                {
                                    "locale": "fi",
                                    "literal": "orkesteri"
                                }
                            ],
                            "itemCount": 1,
                            "itemIsGroup": true,
                            "sekoUri": "http://urn.fi/urn:nbn:fi:au:seko:00728"
                        }
                    ],
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                        }
                    ]
                }
            ],
            "genre": [
                {
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "orkesterimusiikki"
                        }
                    ],
                    "slmUri": "http://urn.fi/URN:NBN:fi:au:slm:s1009"
                }
            ],
            "firstPerformed": [
                {
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "1918"
                        }
                    ],
                    "year": 1918,
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                        }
                    ]
                }
            ],
            "sources": [
                {
                    "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                    "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                }
            ]
        },
```
