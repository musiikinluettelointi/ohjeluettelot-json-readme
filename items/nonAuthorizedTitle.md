## items.\*.nonAuthorizedTitle

`object`

Tämä rakenne sisältää teosluettelo-objektin auktorisoimattoman nimekkeen.

```JSON
"nonAuthorizedTitle": {
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
| [`title`](#itemsnonauthorizedtitletitle) | aina | string | Auktorisoitu nimeke |  |
| [`offset`](#itemsnonauthorizedtitleffset) | joskus | integer | Ohitettavat merkit | |
| [`language`](#itemsnonauthorizedtitlelanguage) | joskus | object | Nimekkeen kieli | |
| [`alphabet`](#itemsnonauthorizedtitlealphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](#itemsnonauthorizedtitletransliteration) | joskus | object | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
| [`note`](#itemsnonauthorizedtitlenote) | joskus | string | Huomautus nimekkeestä | |
| [`publications`](#itemsnonauthorizedtitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut | |
| [`sources`](#itemsnonauthorizedtitlesources) | joskus | array | Nimekkeen lähteet | |

### items.\*.nonAuthorizedTitle.title

Auktorisoimaton nimeke.

`string`

```JSON
"title": ""
```

### items.\*.nonAuthorizedTitle.offset

`integer`

Ohitettavat merkit.

```JSON
"offset": 3
```

### items.\*.nonAuthorizedTitle.language

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
| [`code`](#itemsnonauthorizedtitlelanguagecode) | aina | string | Kielen koodi | ISO 639-2 |
| [`label`](#itemsnonauthorizedtitlelanguagelabel) | aina | array | Kielen otsikko | |

#### items.\*.nonAuthorizedTitle.language.code

`string`

Kielen koodi.

```JSON
"code": "rus"
```

#### items.\*.nonAuthorizedTitle.language.label

`array`

Tämä rakenne sisältää kielen otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.nonAuthorizedTitle.language.label.\*

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
| [`locale`](#itemsnonauthorizedtitlelanguagelabellocale) | aina | string | Kielen otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsnonauthorizedtitlelanguagelabelliteral) | aina | array | Kielen otsikko | |

#### items.\*.nonAuthorizedTitle.language.label.\*.locale

`string`

Kielen otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### items.\*.nonAuthorizedTitle.language.label.\*.literal

`string`

Kielen otsikko.

```JSON
"literal": "venäjä"
```

### items.\*.nonAuthorizedTitle.alphabet

`object`

Tämä rakenne sisältää nimekkeen merkistön. Tieto on tallennettu lähinnä kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille.

```JSON
"alphabet": {
  "code": ,
  "label": [

  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsnonauthorizedtitlealphabetcode) | aina | string | Merkistön koodi | `latin` \| `cyrillic` |
| [`label`](#itemsnonauthorizedtitlealphabetlabel) | aina | array | Merkistön otsikko | |

#### items.\*.nonAuthorizedTitle.alphabet.code

`string`

Merkistön koodi.

```JSON
"code": "latin"
```

#### items.\*.nonAuthorizedTitle.alphabet.label

`array`

Tämä rakenne sisältää merkistön otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.nonAuthorizedTitle.alphabet.label.\*

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
| [`locale`](#itemsnonauthorizedtitlealphabetlabellocale) | aina | string | Merkistön otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsnonauthorizedtitlealphabetlabelliteral) | aina | array | Merkistön otsikko | |

#### items.\*.nonAuthorizedTitle.alphabet.label.\*.locale

`string`

```JSON
"locale": "fi"
```

#### items.\*.nonAuthorizedTitle.alphabet.label.\*.literal

`string`

```JSON
"literal": "latinalainen"
```

### items.\*.nonAuthorizedTitle.transliteration

`string`

Nimekkeen translitterointi.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


### items.\*.nonAuthorizedTitle.note

`string`

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013"
```

### items.\*.nonAuthorizedTitle.publications

`array`

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [

]
```

#### items.\*.nonAuthorizedTitle.publications.\*

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
| [`reference`](#itemsnonauthorizedtitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsnonauthorizedtitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.nonAuthorizedTitle.publications.\*.reference

`string`

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.nonAuthorizedTitle.publications.\*.id

`string`

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

### items.\*.nonAuthorizedTitle.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

#### items.\*.nonAuthorizedTitle.sources.\*

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
| [`reference`](#itemsnonauthorizedtitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsnonauthorizedtitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.nonAuthorizedTitle.sources.\*.reference

`string`

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.nonAuthorizedTitle.sources.\*.id

`string`

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```