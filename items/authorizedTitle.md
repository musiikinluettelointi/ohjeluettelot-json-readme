# items.\*.authorizedTitle

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen. Kaikilla teosluettelo-objekteilla ei ole auktorisoitua nimekettä, katso [`items.*.nonAuthorizedTitle`](nonAuthorizedTitle.md).

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Auktorisoitu nimeke. |  |
| `offset` | joskus | integer | Ohitettavat merkit. | |
| [`language`](#itemsauthorizedtitlelanguage) | joskus | object | Nimekkeen kieli | |
| [`alphabet`](#itemsauthorizedtitlealphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](#itemsauthorizedtitletransliteration) | joskus | string | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
| `note` | joskus | string | Huomautus nimekkeestä | |
| [`publications`](#itemsauthorizedtitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut | |
| [`sources`](#itemsauthorizedtitlesources) | joskus | array | Nimekkeen lähteet | |


## items.\*.authorizedTitle.language

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
| `code` | aina | string | Kielen koodi. | ISO 639-2 |
| [`label`](#itemsauthorizedtitlelanguagelabel) | aina | array | Kielen otsikko. | |

### items.\*.authorizedTitle.language.label

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
| `locale` | aina | string | Kielen otsikon kielikoodi. | ISO 639-2 |
| `literal` | aina | array | Kielen otsikko. | |

## items.\*.authorizedTitle.alphabet

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
| `code` | aina | string | Merkistön koodi | `latin` \| `cyrillic` |
| [`label`](#itemsauthorizedtitlealphabetlabel) | aina | array | Merkistön otsikko | |

### items.\*.authorizedTitle.alphabet.label

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


## items.\*.authorizedTitle.transliteration

Nimekkeen translitterointi. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |

## items.\*.authorizedTitle.publications

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

## items.\*.authorizedTitle.sources

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
