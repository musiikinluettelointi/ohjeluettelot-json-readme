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
| --- | --- | --- | --- | --- |
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
| --- | --- | --- | --- | --- |
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
| --- | --- | --- | --- | --- |
| [`name`](#metacomposername) | aina | string | Säveltäjän nimi  |  |
| [`id`](#metacomposerid) | aina | string | Säveltäjän tunniste teosluettelossa | name-{uuid} |
| [`kantoUri`](#metacomposerkantouri) | joskus | string | Säveltäjän KANTO URI  | uri |
| [`url`](#metacomposerurl) | joskus | string |  Teosluettelon osoite  | url |
| [`introduction`](#metacomposerintroduction) | joskus | array |  Teosluettelon esipuhe  |  |
| [`workCategories`](#metacomposerworkcategories) | joskus | array |  Säveltäjälle määritellyt teoskategoriat  |  |

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
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Esipuheen kieli  | ISO 639-1  |
| `text` | aina | string | Teosluettelon esipuhe | |
| `author` | joskus | string | Esipuheen kirjoittaja | |
| `url` | joskus | string |  Esipuheen osoite  | url |

#### meta.composer.workCategories

Säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

```JSON
"workCategories": [
  {
    "code": "withOpusNumber",
    "label": {

    }
  }
]
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code`  | aina | string | Teoskategorian koodi  |   |
| [`label`](#metacomposerworkcategorieslabel)  | aina | string | Teoskategorian otsikko | |

#### meta.composer.workCategories.label

Teoskategorian otsikko.

```JSON
"label": {
  "locale": "fi",
  "text": "Opusnumeroidut teokset"
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Teoskategorian otsikon kieli | ISO 639-1  |
| `text` | aina | string | Teoskategorian otsikko | |

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

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`itemType`](#itemsitemtype) | aina | string | Teosobjektin tyyppi | `work` \| `part` \| `arrangement` \| `translation`  |
| [`id`](#itemsid) | aina  | string | Teosobjektin tunniste teosluettelossa | {`work` \| `part` \| `arrangement` \| `translation`}-{uuid} |
| [`composer`](#itemscomposer) | joskus | object | Säveltäjä | |
| [`authorizedTitle`](#itemsauthorizedtitle) | joskus | array | Auktorisoitu nimeke  | |
| [`authorizedTitleHistory`](#itemsauthorizedtitlehistory) | joskus | array | Auktorisoidun nimekkeen muutoshistoria | |
| [`alternativeTitle`](#itemsalternativetitle) | joskus | array | Vaihtoehtoiset nimekkeet | |
| [`workCategory`](#itemsworkcategory) | joskus | array | Teoskategoria | |
| [`workNumber`](#itemsworknumber) | joskus  | array | Numerointi | |
| [`creationYear`](#itemscreationyear) | joskus | array | Luomisaika | |
| [`mediumOfPerformance`](#itemsmediumofperformance) | joskus | array | Esityskokoonpano | |
| [`genre`](#itemsgenre) | joskus | array | Muoto tai lajityyppi | |
| [`sources`](#itemssources) | joskus  | array | Lähteet | |

#### items.*.itemType

Teosobjektin tyyppi.

```JSON
"itemType": "work",
```
| Arvo | Kuvaus |
| --- | --- |
| `work`| Teos |
| `part`| Teoksen osa  |
| `arrangement`| Teoksen tai teoksen osan sovitus |
| `translation`| Teoksen, teoksen osan tai sovituksen käännös |

#### items.*.id

Teosobjektin tunniste teosluettelossa.

```JSON
"id": "work-c10de676-0115-474f-895e-26940602371b",
```
#### items.*.composer

Säveltäjä. Anonyymeillä teosobjekteilla ei ole säveltäjää.

```JSON
"composer": {
  "id": ,
  "name": ,
  "kantoUri":
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`id`](#itemscomposerid) | aina | string | Säveltäjän tunniste teosluettelossa | name-{uuid} |
| [`name`](#itemscomposername) | aina | string | Säveltäjän nimi | |
| [`kantoUri`](#itemscomposerkantouri) | joskus | string | Säveltäjän KANTO URI | |

#### items.*.composer.id

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
```

#### items.*.composer.name

Säveltäjän nimi.

```JSON
"name": "Pingoud, Ernest, 1887-1942",
```

#### items.*.composer.kantoUri

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```

#### items.*.authorizedTitle

Auktorisoitu nimeke. Kaikilla teosobjekteilla ei ole auktorisoitua nimekettä.

```JSON
"authorizedTitle": {
  "title": ,
  "offset": ,
  "language": {

  },
  "alphabet": {

  },
  "transliteration": {

  },
  "note": ,
  "publications": [

  ],
  "sources": [

  ]
},
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`title`](#itemsauthorizedtitletitle) | aina | string | Auktorisoitu nimeke |  |
| [`offset`](#itemsauthorizedtitleoffset) | joskus | integer | Ohitettavat merkit | |
| [`language`](#itemsauthorizedtitlelanguage) | joskus | object | Nimekkeen kieli | |
| [`alphabet`](#itemsauthorizedtitlealphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](#itemsauthorizedtitletransliteration) | joskus | object | Nimekkeen translitterointi | |
| [`note`](#itemsauthorizedtitlenote) | joskus | string | Huomautus nimekkeestä | |
| [`publications`](#itemsauthorizedtitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut | |
| [`sources`](#itemsauthorizedtitlesources) | joskus | array | Nimekkeen lähteet | |

#### items.*.authorizedTitle.title

Auktorisoitu nimeke.

```JSON
"title": "Vremena goda, op37a",
```

#### items.*.authorizedTitle.offset

Ohitettavat merkit.

```JSON
"offset": 3,
```

#### items.*.authorizedTitle.language

Nimekkeen kieli.

```JSON
"language": {
  "code": "rus",
  "label": [

  ]
},
```

#### items.*.authorizedTitle.language.code

#### items.*.authorizedTitle.language.label

```JSON
"label": [
  {
    "locale": "fi",
    "literal": "venäjä"
  }
]
```

#### items.*.authorizedTitle.alphabet

Nimekkeen merkistö.

```JSON
"alphabet": {
  "code": "latin",
  "label": [

  ]
},
```
#### items.*.authorizedTitle.alphabet.code

#### items.*.authorizedTitle.alphabet.label


```JSON
"label": [
  {
    "locale": "fi",
    "literal": "latinalainen"
  }
]
```

#### items.*.authorizedTitle.transliteration

Nimekkeen translitterointi.

```JSON
"authorizedTitle": {
    "title": "Vremena goda, op37a",
    "language": {
        "code": "rus",
        "label": [
            {
                "locale": "fi",
                "literal": "venäjä"
            }
        ]
    },
    "transliteration": "sfs4900",
    "note": "Poroila 2013",
```

#### items.*.authorizedTitle.note

Huomautus nimekkeestä.

```JSON
"authorizedTitle": {
    "title": "Vremena goda, op37a",
    "language": {
        "code": "rus",
        "label": [
            {
                "locale": "fi",
                "literal": "venäjä"
            }
        ]
    },
    "transliteration": "sfs4900",
    "note": "Poroila 2013",
```

#### items.*.authorizedTitle.publications

Nimekkeeseen liittyvät julkaisut.

```JSON
"authorizedTitle": {
    "title": "Vremena goda, op37a",
    "language": {
        "code": "rus",
        "label": [
            {
                "locale": "fi",
                "literal": "venäjä"
            }
        ]
    },
    "transliteration": "sfs4900",
    "note": "Poroila 2013",
```

#### items.*.authorizedTitle.sources

Nimekkeen lähteet.

```JSON
"authorizedTitle": {
    "title": "Vremena goda, op37a",
    "language": {
        "code": "rus",
        "label": [
            {
                "locale": "fi",
                "literal": "venäjä"
            }
        ]
    },
    "transliteration": "sfs4900",
    "note": "Poroila 2013",
```

#### items.*.authorizedTitleHistory

Auktorisoidun nimekkeen muutoshistoria, mikäli teosobjektilla on auktorisoitu nimeke.

```JSON

```
#### items.*.alternativeTitle

Vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot.

```JSON

```
#### items.*.workCategory

Teoskategoria. Kaikilla teosobjekteilla ei ole teoskategoriaa.

```JSON

```
#### items.*.workNumber

Numerointi. Kaikilla teosobjekteilla ei ole numerointia.

```JSON

```
#### items.*.creationYear

Luomisaika. Kaikilla teosobjekteilla ei ole luomisaikaa.

```JSON

```
#### items.*.mediumOfPerformance

Esityskokoonpano. Kaikilla teosobjekteilla ei ole esityskokoonpano.

```JSON

```
#### items.*.genre

Muoto tai lajityyppi. Kaikilla teosobjekteilla ei ole muotoa tai lajityyppiä.

```JSON

```
#### items.*.sources

Lähteet. Kaikilla teosobjekteilla ei ole lähteitä.

```JSON

```

```JSON
{
            

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
