# items.\*.musicKey

Tämä rakenne sisältää teosluettelo-objektin sävellajin.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsmusickeycode) | aina | string | Sävellajin koodi. | |
| [`label`](#itemsmusickeylabel) | aina | array | Sävellajin otsikko. |  |
| `note` | joskus | string | Huomautus sävellajista. | |
| [`publications`](#itemsmusickeypublications) | joskus | array | Sävellajiin liittyvät julkaisut. | |
| [`sources`](#itemsmusickeysources) | joskus | array | Sävellajin lähteet. | |

## Esimerkki

```JSON
"musicKey": [
    {
        "code": "eFlatMajor",
        "label": [
            {
                "locale": "fi",
                "literal": "Es-duuri"
            }
        ],
        "sources": [
            {
                "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
            }
        ]
    }
]
```

### items.\*.musicKey.\*.code

Sävellajin koodi.

| Arvo | Sävellaji |
| --- | --- | --- |
| `cFlatMajor`| Ces-duuri |
| `cMajor`| C-duuri  |
| `cSharpMajor`| Cis-duuri |
| `dFlatMajor`| Des-duuri |
| `dMajor`| D-duuri |
| `eFlatMajor`| Es-duuri |
| `eMajor`| E-duuri |
| `fMajor`| F-duuri  |
| `fSharpMajor`| Fis-duuri |
| `gFlatMajor`| Ges-duuri |
| `gMajor`| G-duuri |
| `aFlatMajor`| As-duuri |
| `aMajor`| A-duuri |
| `bFlatMajor`| B-duuri  |
| `bMajor`| H-duuri |
| `cMinor`| c-molli |
| `cSharpMinor`| cis-molli |
| `dMinor`| d-molli |
| `dSharpMinor`| dis-molli |
| `eFlatMinor`| es-molli  |
| `eMinor`| e-molli |
| `fMinor`| f-molli |
| `fSharpMinor`| fis-molli |
| `gMinor`| g-molli |
| `gSharpMinor`| gis-molli |
| `aFlatMinor`| as-molli |
| `aMinor`| a-molli |
| `aSharpMinor`| ais-molli |
| `bFlatMinor`| b-molli |
| `bMinor`| h-molli |

## items.\*.musicKey.\*.label

Tämä rakenne sisältää sävellajin otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "Es-duuri"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Sävellajin otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Sävellajin otsikko. | |

## items.\*.musicKey.\*.publications

Tämä rakenne sisältää sävellajiin liittyvät julkaisut.

```JSON
"publications": [
    {
        "reference": "Joulupukki [1958].  (1958). Helsinki, Valistus (yhtiö). ",
        "id": "publication-d9cd27f1-dda2-4aec-bd82-31373f2ffa78"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Julkaisun lähdeviite | |
| `id` | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

## items.\*.musicKey.\*.sources

Tämä rakenne sisältää sävellajin lähteet.

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