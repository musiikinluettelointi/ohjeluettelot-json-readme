# items.\*.alternativeTitle

Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Vaihtoehtoinen nimeke. |  |
| `offset` | joskus | integer | Ohitettavat merkit. | |
| [`language`](#itemsalternativetitlelanguage) | joskus | object | Nimekkeen kieli. | |
| [`alphabet`](#itemsalternativetitlealphabet) | joskus | object | Nimekkeen merkistö. |  |
| [`transliteration`](#itemsalternativetitletransliteration) | joskus | object | Nimekkeen translitterointi. | `iso9` \| `sfs4900` |
| `note` | joskus | string | Huomautus nimekkeestä. | |
| [`publications`](#itemsalternativetitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut. | |
| [`sources`](#itemsalternativetitlesources) | joskus | array | Nimekkeen lähteet. | |


## Esimerkki

```JSON
"alternativeTitle": [
    {
        "title": "15 sånger till dikter av Ernst Josephson",
        "language": {
              "code": "swe",
              "label": [
                  {
                      "locale": "fi",
                      "literal": "ruotsi"
                  }
              ]
          },
          "note": "Poroila 2011",
          "sources": [
              {
                  "reference": "Poroila, Heikki (2011). Yhtenäistetty Yrjö Kilpinen. Yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 144. PDF. ISBN 978-952-5363-43-2. ",
                  "id": "source-0148bad1-5255-4fca-832d-d3813fad7de9"
              }
        ]
    }
]
```


## items.\*.alternativeTitle.\*.language

Tämä rakenne sisältää nimekkeen kielen.

```JSON
"language": {
    "code": "rus",
    "label": [
        {
            "locale": "fi",
            "literal": "venäjä"
        }
    ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Kielen koodi. | ISO 639-3 |
| [`label`](#itemsalternativetitlelanguagelabel) | aina | array | Kielen otsikon kieliversiot. | |

### items.\*.alternativeTitle.\*.language.label

Tämä rakenne sisältää kielen otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "venäjä"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Kielen otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Kielen otsikko. | |

## items.\*.alternativeTitle.\*.alphabet

Tämä rakenne sisältää nimekkeen merkistön. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"alphabet": {
    "code": "latin",
    "label": [
        {
            "locale": "fi",
            "literal": "latinalainen"
        }
    ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Merkistön koodi. | `latin` \| `cyrillic` |
| [`label`](#itemsalternativetitlealphabetlabel) | aina | array | Merkistön otsikon kieliversiot. | |

### items.\*.alternativeTitle.\*.alphabet.label

Tämä rakenne sisältää merkistön otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "latinalainen"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Merkistön otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Merkistön otsikko. | |


## items.\*.alternativeTitle.\*.transliteration

Nimekkeen translitterointi. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |

## items.\*.alternativeTitle.\*.publications

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [
    {
        "reference": "",
        "id": ""
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Julkaisun lähdeviite | |
| `id` | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

## items.\*.alternativeTitle.\*.sources

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [
    {
        "reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1.",
        "id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Lähteen lähdeviite. | |
| `id` | aina | string | Lähteen tunniste teosluettelossa. | source-{uuid} |