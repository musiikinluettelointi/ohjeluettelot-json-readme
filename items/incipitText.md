# items.\*.incipitText

Tämä rakenne sisältää teosluettelo-objektin alkusanat.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `text` | aina | array | Alkusanat. |  |
| [`language`](#itemsincipittextlanguage) | joskus | object | Alkusanojen kieli | |
| [`alphabet`](#itemsincipittextalphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](#itemsincipittexttransliteration) | joskus | string | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
| `note` | joskus | string | Huomautus alkusanoista. | |
| [`publications`](#itemsincipittextpublications) | joskus | array | Alkusanoihin liittyvät julkaisut. | |
| [`sources`](#itemsincipittextsources) | joskus | array | Alkusanojen lähteet. | |

## Esimerkki

```JSON
"incipitText": [
    {
        "text": "Laulu kaupungin yllä asfaltin",
        "language": {
            "code": "fin",
            "label": [
                {
                    "locale": "fi",
                    "literal": "suomi"
                }
            ]
        }
    }
]
```

## items.\*.incipitText.\*.language

Tämä rakenne sisältää alkusanojen kielen.

```JSON
"language": {
    "code": "fin",
    "label": [
        {
            "locale": "fi",
            "literal": "suomi"
        }
    ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Kielen koodi. | ISO 639-2 |
| [`label`](#itemsincipittextlanguagelabel) | aina | array | Kielen otsikon kieliversiot. | |

### items.\*.incipitText.\*.language.label

Tämä rakenne sisältää kielen otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "suomi"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Kielen otsikon kielikoodi. | ISO 639-2 |
| `literal` | aina | array | Kielen otsikko. | |

## items.\*.incipitText.\*.alphabet

Tämä rakenne sisältää alkusanojen merkistön. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille alkusanoille, mikäli se on saatavilla.

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
| [`label`](#itemsincipittextalphabetlabel) | aina | array | Merkistön otsikon kieliversiot. | |

### items.\*.incipitText.\*.alphabet.label

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
| `locale` | aina | string | Merkistön otsikon kielikoodi. | ISO 639-2 |
| `literal` | aina | array | Merkistön otsikko. | |


## items.\*.incipitText.\*.transliteration

Alkusanojen translitterointi. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille alkusanoille, mikäli se on saatavilla.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


## items.\*.incipitText.\*.publications

Tämä rakenne sisältää alkusanoihin liittyvät julkaisut.

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

## items.\*.incipitText.\*.sources

Tämä rakenne sisältää alkusanojen lähteet.

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