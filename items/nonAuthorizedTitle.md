# items.\*.nonAuthorizedTitle

Tämä rakenne sisältää teosluettelo-objektin auktorisoimattoman nimekkeen.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Auktorisoimaton nimeke |  |
| `offset` | joskus | integer | Ohitettavat merkit | |
| [`language`](#itemsnonauthorizedtitlelanguage) | joskus | object | Nimekkeen kieli | |
| [`alphabet`](#itemsnonauthorizedtitlealphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](#itemsnonauthorizedtitletransliteration) | joskus | object | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
| `note` | joskus | string | Huomautus nimekkeestä | |
| [`publications`](#itemsnonauthorizedtitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut | |
| [`sources`](#itemsnonauthorizedtitlesources) | joskus | array | Nimekkeen lähteet | |


## Esimerkki

```JSON
"nonAuthorizedTitle": {
    "title": "Le rival",
    "offset": 3,
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
```

## items.\*.nonAuthorizedTitle.language

Tämä rakenne sisältää nimekkeen kielen.

```JSON
"language": {
    "code": "fre",
    "label": [
        {
            "locale": "fi",
            "literal": "ranska"
        }
    ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Kielen koodi. | ISO 639-3 |
| [`label`](#itemsnonauthorizedtitlelanguagelabel) | aina | array | Kielen otsikon kieliversiot. | |

### items.\*.nonAuthorizedTitle.language.label

Tämä rakenne sisältää kielen otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "ranska"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Kielen otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Kielen otsikko. | |

## items.\*.nonAuthorizedTitle.alphabet

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
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Merkistön koodi. | `latin` \| `cyrillic` |
| [`label`](#itemsnonauthorizedtitlelanguagelabel) | aina | array | Merkistön otsikon kieliversiot. | |

### items.\*.nonAuthorizedTitle.alphabet.label

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


## items.\*.nonAuthorizedTitle.transliteration

Nimekkeen translitterointi. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |

## items.\*.nonAuthorizedTitle.publications

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

## items.\*.nonAuthorizedTitle.sources

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
