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
| [`items`](#items) | aina  | array | Sisältää teosluettelo-objektit |

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

Tämä rakenne sisältää dokumentin käyttöehdot.

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

Tämä rakenne sisältää säveltäjän tiedot.

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

#### meta.composer.introduction.*

Tämä rakenne sisältää teoksen esipuheen. Kaikille säveltäjille ei ole laadittu esipuhetta.

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

#### meta.composer.workCategories.*

Tämä rakenne sisältää säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

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

#### meta.composer.workCategories.*.label

> [!WARNING]
> Avain `text` tullaan muuttamaan avaimeksi `literal`.

Tämä rakenne sisältää teoskategorian otsikon.

```JSON
"label": {
  "locale": "fi",
  "text": "Opusnumeroidut teokset"
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Teoskategorian otsikon kielikoodi | ISO 639-1  |
| `text` | aina | string | Teoskategorian otsikko | |

#### meta.composer.workCategories.*.label.locale

Teoskategorian otsikon kielikoodi.

```JSON
"locale": "fi",
```
#### meta.composer.workCategories.*.label.text

> [!WARNING]
> Avain `text` tullaan muuttamaan avaimeksi `literal`.

Teoskategorian otsikko.

```JSON
"text": "Opusnumeroidut teokset"
```

#### meta.apiVersion

Dokumentin tuottanut rajapinta.

```JSON
"apiVersion": "v1"
```

### items.*

Tämä rakenne sisältää teosluettelon teosluettelo-objektit.

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
| [`itemType`](#itemsitemtype) | aina | string | teosluettelo-objektin tyyppi | `work` \| `part` \| `arrangement` \| `translation`  |
| [`id`](#itemsid) | aina  | string | teosluettelo-objektin tunniste teosluettelossa | {`work` \| `part` \| `arrangement` \| `translation`}-{uuid} |
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

teosluettelo-objektin tyyppi.

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

teosluettelo-objektin tunniste teosluettelossa.

```JSON
"id": "work-c10de676-0115-474f-895e-26940602371b",
```
#### items.*.composer

Tämä rakenne sisältää teosluettelo-objektin säveltäjän tiedot. Anonyymeillä teosluettelo-objekteilla ei ole säveltäjää.

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

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen. Kaikilla teosluettelo-objekteilla ei ole auktorisoitua nimekettä.

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
| [`transliteration`](#itemsauthorizedtitletransliteration) | joskus | object | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
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
  "code": ,
  "label": [

  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsauthorizedtitlelanguagecode) | aina | string | Kielen koodi | ISO 639-2 |
| [`label`](#itemsauthorizedtitlelanguagelabel) | aina | array | Kielen otsikko | |

#### items.*.authorizedTitle.language.code

Kielen koodi.

```JSON
"code": "rus",
```

#### items.\*.authorizedTitle.language.label.*

Kielen otsikko.

```JSON
"label": [
  {
    "locale": ,
    "literal": 
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsauthorizedtitlelanguagelabellocale) | aina | string | Kielen koodi | ISO 639-2 |
| [`literal`](#itemsauthorizedtitlelanguagelabelliteral) | aina | array | Kielen otsikko | |

#### items.\*.authorizedTitle.language.label.*.locale

Kielen otsikon kielikoodi.

```JSON
"locale": "fi",
```
#### items.\*.authorizedTitle.language.label.*.literal

Kielen otsikko.

```JSON
"literal": "venäjä"
```
#### items.*.authorizedTitle.alphabet

Nimekkeen merkistö.

```JSON
"alphabet": {
  "code": ,
  "label": [

  ]
},
```
#### items.*.authorizedTitle.alphabet.code

```JSON
"code": "latin",
```

#### items.\*.authorizedTitle.alphabet.label.*

```JSON
"label": [
  {
    "locale": ,
    "literal": 
  }
]
```

#### items.\*.authorizedTitle.alphabet.label.*.locale

```JSON
"locale": "fi",
```

#### items.\*.authorizedTitle.alphabet.label.*.literal

```JSON
"literal": "latinalainen"
```

#### items.*.authorizedTitle.transliteration

Nimekkeen translitterointi.

```JSON
"transliteration": "sfs4900",
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


#### items.*.authorizedTitle.note

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013",
```

#### items.\*.authorizedTitle.publications.*

Nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [
  {
    "reference": ,
    "id":
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsauthorizedtitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsauthorizedtitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.authorizedTitle.publications.*.reference

Julkaisun lähdeviite.

```JSON
"reference": "",
```

#### items.\*.authorizedTitle.publications.*.id

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

#### items.\*.authorizedTitle.sources.*

Nimekkeen lähteet.

```JSON
"sources": [
                {
                    "reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1. ",
                    "id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
                }
            ]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsauthorizedtitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsauthorizedtitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.authorizedTitle.sources.*.reference

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1.",
```

#### items.\*.authorizedTitle.sources.*.id

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```

#### items.*.authorizedTitleHistory

Auktorisoidun nimekkeen muutoshistoria, mikäli teosluettelo-objektilla on auktorisoitu nimeke.

```JSON

```
#### items.*.alternativeTitle

Vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot.

```JSON

```
#### items.*.workCategory

Teoskategoria. Kaikilla teosluettelo-objekteilla ei ole teoskategoriaa.

```JSON

```
#### items.*.workNumber

Numerointi. Kaikilla teosluettelo-objekteilla ei ole numerointia.

```JSON

```
#### items.*.creationYear

Luomisaika. Kaikilla teosluettelo-objekteilla ei ole luomisaikaa.

```JSON

```
#### items.*.mediumOfPerformance

Esityskokoonpano. Kaikilla teosluettelo-objekteilla ei ole esityskokoonpano.

```JSON

```
#### items.*.genre

Muoto tai lajityyppi. Kaikilla teosluettelo-objekteilla ei ole muotoa tai lajityyppiä.

```JSON

```
#### items.*.sources

Lähteet. Kaikilla teosluettelo-objekteilla ei ole lähteitä.

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
