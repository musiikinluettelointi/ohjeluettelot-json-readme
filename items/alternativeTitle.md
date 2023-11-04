# items.\*.alternativeTitle

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot. |


## Esimerkki

```JSON
 "authorizedTitle": [
  {
    "title": "Kehtolaulu",
    "language": {
      "code": "fin",
      "label": [
        {
          "locale": "fi",
          "literal": "suomi"
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
]
```

## items.\*.alternativeTitle.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoisen nimekkeen. |


```JSON
{
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
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`title`](#itemsalternativetitletitle) | aina | string | Auktorisoitu nimeke |  |
| [`offset`](#itemsalternativetitleoffset) | joskus | integer | Ohitettavat merkit | |
| [`language`](#itemsalternativetitlelanguage) | joskus | object | Nimekkeen kieli | |
| [`alphabet`](#itemsalternativetitlealphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](#itemsalternativetitletransliteration) | joskus | object | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
| [`note`](#itemsalternativetitlenote) | joskus | string | Huomautus nimekkeestä | |
| [`publications`](#itemsalternativetitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut | |
| [`sources`](#itemsalternativetitlesources) | joskus | array | Nimekkeen lähteet | |

### items.\*.alternativeTitle.\*.title

| Tyyppi | Kuvaus |
| --- | --- |
| string | Vaihtoehtoinen nimeke. |

```JSON
"title": ""
```

### items.\*.alternativeTitle.\*.offset

| Tyyppi | Kuvaus |
| --- | --- |
| integer | Ohitettavat merkit. |

```JSON
"offset": 3
```

### items.\*.alternativeTitle.\*.language

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeen kielen. |

```JSON
"language": {
  "code": ,
  "label": [

  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsalternativetitlelanguagecode) | aina | string | Kielen koodi | ISO 639-2 |
| [`label`](#itemsalternativetitlelanguagelabel) | aina | array | Kielen otsikko | |

#### items.\*.alternativeTitle.\*.language.code


| Tyyppi | Kuvaus |
| --- | --- |
| string | Kielen koodi. |

```JSON
"code": "rus"
```

#### items.\*.alternativeTitle.\*.language.label

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää kielen otsikon kieliversiot.|

```JSON
"label": [

]
```

#### items.\*.alternativeTitle.\*.language.label.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää kielen otsikon kieliversion.|


```JSON
{
  "locale": ,
  "literal":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsalternativetitlelanguagelabellocale) | aina | string | Kielen otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsalternativetitlelanguagelabelliteral) | aina | array | Kielen otsikko | |

#### items.\*.alternativeTitle.\*.language.label.\*.locale

| Tyyppi | Kuvaus |
| --- | --- |
| string | Kielen otsikon kielikoodi.|

```JSON
"locale": "fi"
```
#### items.\*.alternativeTitle.\*.language.label.\*.literal

| Tyyppi | Kuvaus |
| --- | --- |
| string | Kielen otsikko.|

```JSON
"literal": "venäjä"
```

### items.\*.alternativeTitle.\*.alphabet

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeen merkistön. Tieto on tallennettu lähinnä kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille.|

```JSON
"alphabet": {
  "code": ,
  "label": [

  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsalternativetitlealphabetcode) | aina | string | Merkistön koodi | `latin` \| `cyrillic` |
| [`label`](#itemsalternativetitlealphabetlabel) | aina | array | Merkistön otsikko | |

#### items.\*.alternativeTitle.\*.alphabet.code

| Tyyppi | Kuvaus |
| --- | --- |
| string | Merkistön koodi.|

```JSON
"code": "latin"
```

#### items.\*.alternativeTitle.\*.alphabet.label

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää merkistön otsikon kieliversiot.|

```JSON
"label": [

]
```

#### items.\*.alternativeTitle.\*.alphabet.label.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää merkistön otsikon kieliversion. |

```JSON
{
  "locale": ,
  "literal":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsalternativetitlealphabetlabellocale) | aina | string | Merkistön otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsalternativetitlealphabetlabelliteral) | aina | array | Merkistön otsikko | |

#### items.\*.alternativeTitle.\*.alphabet.label.\*.locale

| Tyyppi | Kuvaus |
| --- | --- |
| string | Merkistön otsikon kielikoodi. |

```JSON
"locale": "fi"
```

#### items.\*.alternativeTitle.\*.alphabet.label.\*.literal

| Tyyppi | Kuvaus |
| --- | --- |
| string | Merkistön otsikko. |

```JSON
"literal": "latinalainen"
```

### items.\*.alternativeTitle.\*.transliteration

| Tyyppi | Kuvaus |
| --- | --- |
| string | Nimekkeen translitterointi. |

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


### items.\*.alternativeTitle.\*.note

| Tyyppi | Kuvaus |
| --- | --- |
| string | Huomautus nimekkeestä.|

```JSON
 "note": "Poroila 2013"
```

### items.\*.alternativeTitle.\*.publications

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.|

```JSON
"publications": [

]
```

### items.\*.alternativeTitle.\*.publications.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeeseen liittyvän julkaisun.|

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsalternativetitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsalternativetitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.alternativeTitle.\*.publications.\*.reference

| Tyyppi | Kuvaus |
| --- | --- |
| string | Julkaisun lähdeviite. |

```JSON
"reference": ""
```

#### items.\*.alternativeTitle.\*.publications.\*.id

| Tyyppi | Kuvaus |
| --- | --- |
| string | Julkaisun tunniste teosluettelossa. |

```JSON
"id": ""
```

### items.\*.alternativeTitle.\*.sources

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää nimekkeen lähteet. |

```JSON
"sources": [

]
```

### items.\*.alternativeTitle.\*.sources.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeen lähteen. |

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsalternativetitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsalternativetitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.alternativeTitle.\*.sources.\*.reference

| Tyyppi | Kuvaus |
| --- | --- |
| string | Lähteen lähdeviite. |


```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.alternativeTitle.\*.sources.\*.id

| Tyyppi | Kuvaus |
| --- | --- |
| string | Lähteen tunniste teosluettelossa.|

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```