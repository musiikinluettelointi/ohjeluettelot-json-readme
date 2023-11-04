# items.\*.authorizedTitle

`object`

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

## items.\*.authorizedTitle.title

`string`

Auktorisoitu nimeke.

```JSON
"title": "Vremena goda, op37a"
```

## items.\*.authorizedTitle.offset

`integer`

Ohitettavat merkit.

```JSON
"offset": 3
```

## items.\*.authorizedTitle.language

`object`

Tämä rakenne sisältää nimekkeen kielen.

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

### items.\*.authorizedTitle.language.code

`string`

Kielen koodi.

```JSON
"code": "rus"
```

### items.\*.authorizedTitle.language.label

`array`

Tämä rakenne sisältää kielen otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.authorizedTitle.language.label.\*

`object`

Tämä rakenne sisältää kielen otsikon kieliversion.

```JSON
{
  "locale": ,
  "literal":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsauthorizedtitlelanguagelabellocale) | aina | string | Kielen otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsauthorizedtitlelanguagelabelliteral) | aina | array | Kielen otsikko | |

#### items.\*.authorizedTitle.language.label.\*.locale

`string`

Kielen otsikon kielikoodi.

```JSON
"locale": "fi"
```

#### items.\*.authorizedTitle.language.label.\*.literal

`string`

Kielen otsikko.

```JSON
"literal": "venäjä"
```

## items.\*.authorizedTitle.alphabet

`object`

Tämä rakenne sisältää nimekkeen merkistön. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"alphabet": {
  "code": ,
  "label": [

  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsauthorizedtitlealphabetcode) | aina | string | Merkistön koodi | `latin` \| `cyrillic` |
| [`label`](#itemsauthorizedtitlealphabetlabel) | aina | array | Merkistön otsikko | |

### items.\*.authorizedTitle.alphabet.code

`string`

Merkistön koodi.

```JSON
"code": "latin"
```

### items.\*.authorizedTitle.alphabet.label

`array`

Tämä rakenne sisältää merkistön otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.authorizedTitle.alphabet.label.\*

`object`

Tämä rakenne sisältää merkistön otsikon kieliversion.

```JSON
{
  "locale": ,
  "literal":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsauthorizedtitlealphabetlabellocale) | aina | string | Merkistön otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsauthorizedtitlealphabetlabelliteral) | aina | array | Merkistön otsikko | |

#### items.\*.authorizedTitle.alphabet.label.\*.locale

`string`

```JSON
"locale": "fi"
```

#### items.\*.authorizedTitle.alphabet.label.\*.literal

`string`

```JSON
"literal": "latinalainen"
```

## items.\*.authorizedTitle.transliteration

`string`

Nimekkeen translitterointi. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


## items.\*.authorizedTitle.note

`string`

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013"
```

## items.\*.authorizedTitle.publications

`array`

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [

]
```

### items.\*.authorizedTitle.publications.\*

`object`

Tämä rakenne sisältää nimekkeeseen liittyvän julkaisun.

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsauthorizedtitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsauthorizedtitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.authorizedTitle.publications.\*.reference

`string`

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.authorizedTitle.publications.\*.id

`string`

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

## items.\*.authorizedTitle.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

### items.\*.authorizedTitle.sources.\*

`object`

Tämä rakenne sisältää nimekkeen lähteen.

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsauthorizedtitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsauthorizedtitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.authorizedTitle.sources.\*.reference

`string`

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.authorizedTitle.sources.\*.id

`string`

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```