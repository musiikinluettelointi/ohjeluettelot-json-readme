# ohjeluettelot-json

## In English

To do

## Dokumentti

`object`

Dokumentti sisältää metatiedot rakenteessa `meta` ja teosluettelo-objektit rakenteessa `items`.

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

## meta

`object`

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

## meta.createdBy

`string`

Dokumentin tuottaja.

```JSON
"createdBy": "info@musiikinluettelointi.fi"
```

## meta.createdAt

`string`

Dokumentin luomisaika.

```JSON
"createdAt": "2023-10-31T16:54:50.265847Z"
```

## meta.license

`object`

Tämä rakenne sisältää dokumentin käyttöehdot.

```JSON
"license": {
  "name": ,
  "url":
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`name`](#metalicensename) | aina | string |  Dokumentin lisenssi |  |
| [`url`](#metalicenseurl) | aina | string |  Lisenssin osoite | url |

### meta.license.name

`string`

Dokumentin lisenssi.

```JSON
"name": "CC0 1.0 Universal"
```

### meta.license.url

`string`

Lisenssin osoite.

```JSON
"url": "http://creativecommons.org/publicdomain/zero/1.0"
```
## meta.composer

`object`

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

### meta.composer.name

`string`

Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja.

```JSON
"name": "Pingoud, Ernest, 1887-1942"
```

### meta.composer.id

`string`

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8"
```

### meta.composer.kantoUri

`string`

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```

### meta.composer.url

`string`

Teosluettelon osoite. Kaikilla säveltäjillä ei ole julkista teosluetteloa.

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud"
```

### meta.composer.introduction

`array`

Tämä rakenne sisältää teoksen esipuheen kieliversiot. Kaikille säveltäjille ei ole laadittu esipuhetta.

```JSON
"introduction": [

]
```

#### meta.composer.introduction.\*

`object`

Tämä rakenne sisältää teoksen esipuheen kieliversion.

```JSON
{
  "locale": ,
  "text": ,
  "author": ,
  "url":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Esipuheen kielikoodi  | ISO 639-1  |
| `text` | aina | string | Teosluettelon esipuhe | |
| `author` | joskus | string | Esipuheen kirjoittaja | |
| `url` | joskus | string |  Esipuheen osoite  | url |

#### meta.composer.introduction.\*.locale

`string`

Esipuheen kielikoodi.

```JSON
"locale": "fi"
```

#### meta.composer.introduction.\*.text

`string`

Teosluettelon esipuhe.

```JSON
"text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n"
```

#### meta.composer.introduction.\*.author

`string`

Esipuheen kirjoittaja.

```JSON
"author": "Jaska Järvilehto"
```

#### meta.composer.introduction.\*.url

`string`

Esipuheen osoite.

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe"
```

### meta.composer.workCategories

`array`

Tämä rakenne sisältää säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

```JSON
"workCategories": [

]
```

#### meta.composer.workCategories.\*

`object`

Tämä rakenne sisältää säveltäjälle määritellyn teoskategorian.

```JSON
{
  "code": "withOpusNumber",
  "label": [

  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#metacomposerworkcategoriescode)   | aina | string | Teoskategorian koodi  |   |
| [`label`](#metacomposerworkcategorieslabel)  | aina | array | Teoskategorian otsikko | |

#### meta.composer.workCategories.\*.code

`string`

Teoskategorian koodi

```JSON
"code": "withOpusNumber"
```

#### meta.composer.workCategories.\*.label

`array`

Tämä rakenne sisältää teoskategorian otsikon kieliversiot.

```JSON
{
"label": [

]
}
```

#### meta.composer.workCategories.\*.label.\*

> [!WARNING]
> Avain `literal` oli aiemmin `text`.

`object`

Tämä rakenne sisältää teoskategorian otsikon kieliversion.

```JSON
{
  "locale": ,
  "literal":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#metacomposerworkcategorieslabellocale) | aina | string |  Teoskategorian otsikon kielikoodi | ISO 639-1  |
| [`literal`](#metacomposerworkcategorieslabelliteral) | aina | string | Teoskategorian otsikko | |

#### meta.composer.workCategories.\*.label.\*.locale

`string`

Teoskategorian otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### meta.composer.workCategories.\*.label.\*.literal

`string`

> [!WARNING]
> Avain `literal` oli aiemmin `text`.

Teoskategorian otsikko.

```JSON
"literal": "Opusnumeroidut teokset"
```

## meta.apiVersion

`string`

Dokumentin tuottanut rajapinta.

```JSON
"apiVersion": "v1"
```

## items

`array`

Tämä rakenne sisältää teosluettelon teosluettelo-objektit.

```JSON
"items": [

]
```

## items.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin.

```JSON
{
  "itemType": ,
  "id": ,
  "parent": ,
  "children": [

  ],
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
  "language": [

  ],
  "secondaryAuthor": [

  ],
  "note": [

  ],
  "publications": [

  ],
  "sources": [

  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`itemType`](#itemsitemtype) | aina | string | Teosluettelo-objektin tyyppi | `work` \| `part` \| `arrangement` \| `translation`  |
| [`id`](#itemsid) | aina  | string | Teosluettelo-objektin tunniste teosluettelossa | {`work` \| `part` \| `arrangement` \| `translation`}-{uuid} |
| [`parent`](#itemsparent) | joskus  | string | Teosluettelo-objektin emon tunniste teosluettelossa | {`work` \| `part` \| `arrangement`}-{uuid} |
| [`children`](#itemschildren) | joskus | array | Teosluettelo-objektin poikaset  | |
| [`composer`](#itemscomposer) | joskus | object | Säveltäjä | |
| [`authorizedTitle`](#itemsauthorizedtitle) | joskus | array | Auktorisoitu nimeke  | |
| [`authorizedTitleHistory`](#itemsauthorizedtitlehistory) | joskus | array | Auktorisoidun nimekkeen muutoshistoria | |
| [`alternativeTitle`](#itemsalternativetitle) | joskus | array | Vaihtoehtoinen nimeke | |
| [`workCategory`](#itemsworkcategory) | joskus | array | Teoskategoria | |
| [`workNumber`](#itemsworknumber) | joskus  | array | Numerointi | |
| [`creationYear`](#itemscreationyear) | joskus | array | Luomisaika | |
| [`mediumOfPerformance`](#itemsmediumofperformance) | joskus | array | Esityskokoonpano | |
| [`genre`](#itemsgenre) | joskus | array | Muoto tai lajityyppi | |
| [`language`](#itemslanguage) | joskus | array | Esityskieli | |
| [`secondaryAuthor`](#itemssecondaryauthor) | joskus | array | Muu tekijä | |
| [`note`](#itemsnote) | joskus | string | Huomautus | |
| [`publications`](#itemspublications) | joskus  | array | Liittyvä julkaisu | |
| [`sources`](#itemssources) | joskus  | array | Lähde | |

## items.\*.itemType

Teosluettelo-objektin tyyppi.

`string`

```JSON
"itemType": "work"

```
| Arvo | Kuvaus |
| --- | --- |
| `work`| Teos |
| `part`| Teoksen osa  |
| `arrangement`| Teoksen tai teoksen osan sovitus |
| `translation`| Teoksen, teoksen osan tai sovituksen käännös |

## items.\*.id

`string`

Teosluettelo-objektin tunniste teosluettelossa.

```JSON
"id": "work-c10de676-0115-474f-895e-26940602371b"
```

## items.\*.parent

`string`


```JSON
"parent": "work-2b16c991-c62b-4baa-86c4-cb8b13b77fae",
```

## items.\*.children

`array`


```JSON
"children": [
    "part-42e96681-d3c4-44b4-8a6f-8aa7d4638ef6",
    "part-0443f5dc-42da-48ab-974e-c6bbed7cde9e",
    "part-8d576355-9dc7-4d09-aff2-0ca1f231ac7f",
    "part-3067a3bc-a7f5-4495-a2e2-2514ef3228fd"
],
```



## items.\*.composer

`object`

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

### items.\*.composer.id

`string`

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8"
```

### items.\*.composer.name

`string`

Säveltäjän nimi.

```JSON
"name": "Pingoud, Ernest, 1887-1942"
```

### items.\*.composer.kantoUri

`string`

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```

## items.\*.authorizedTitle

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

### items.\*.authorizedTitle.title

`string`

Auktorisoitu nimeke.

```JSON
"title": "Vremena goda, op37a"
```

### items.\*.authorizedTitle.offset

`integer`

Ohitettavat merkit.

```JSON
"offset": 3
```

### items.\*.authorizedTitle.language

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

#### items.\*.authorizedTitle.language.code

`string`

Kielen koodi.

```JSON
"code": "rus"
```

#### items.\*.authorizedTitle.language.label

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

### items.\*.authorizedTitle.alphabet

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

#### items.\*.authorizedTitle.alphabet.code

`string`

Merkistön koodi.

```JSON
"code": "latin"
```

#### items.\*.authorizedTitle.alphabet.label

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

### items.\*.authorizedTitle.transliteration

`string`

Nimekkeen translitterointi. Tieto on tallennettu kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille, mikäli se on saatavilla.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


### items.\*.authorizedTitle.note

`string`

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013"
```

### items.\*.authorizedTitle.publications

`array`

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [

]
```

#### items.\*.authorizedTitle.publications.\*

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

### items.\*.authorizedTitle.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

#### items.\*.authorizedTitle.sources.\*

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

## items.\*.authorizedTitleHistory

`array`

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen muutoshistorian, mikäli teosluettelo-objektilla on auktorisoitu nimeke.

```JSON
"authorizedTitleHistory": [

]
```

### items.\*.authorizedTitleHistory.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen muutoshistoriaversion.

```JSON
{
  "createdAt": ,
  "authorizedTitle": {

  }
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`createdAt`](#itemsauthorizedtitlehistorycreatedat) | aina | string | Auktorisoidun nimekkeen luomispäivämäärä | `YYYY`-`MM`-`DD` |
| [`authorizedTitle`](#itemsauthorizedtitlehistoryauthorizedtitle) | aina | object | Auktorisoitu nimeke| |

### items.\*.authorizedTitleHistory.\*.createdAt

`string`

Auktorisoidun nimekkeen luomispäivämäärä. Mikäli kuukautta tai päivää ei ole tiedossa, on ne merkitty numerolla yksi.
```JSON
"createdAt": "2014-07-01"
```

### items.\*.authorizedTitleHistory.\*.authorizedTitle

`object`

Tämä rakenne sisältää muutoshistoriaversion nimekkeen. Rakenne on identtinen rakenteen [`items\*.authorizedTitle`](#itemsauthorizedtitle) kanssa.

#### items.\*.authorizedTitleHistory.\*.authorizedTitle.title
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.offset
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.language
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.language.code
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.language.label.\*
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.label.\*.locale
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.label.\*.literal
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.alphabet.code
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.alphabet.label.\*
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.alphabet.label.\*.locale
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.alphabet.label.\*.literal
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.transliteration
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.note
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.publications.\*
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.publications.\*.reference
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.publications.\*.id
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.sources.\*
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.sources.\*.reference
#### items.\*.authorizedTitleHistory.\*.authorizedTitle.sources.\*.id

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



## items.\*.alternativeTitle

`array`

Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot.

```JSON
"alternativeTitle": [

]

```

### items.\*.alternativeTitle.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoisen nimekkeen.

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

Vaihtoehtoinen nimeke.

`string`

```JSON
"title": ""
```

### items.\*.alternativeTitle.\*.offset

`integer`

Ohitettavat merkit.

```JSON
"offset": 3
```

### items.\*.alternativeTitle.\*.language

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
| [`code`](#itemsalternativetitlelanguagecode) | aina | string | Kielen koodi | ISO 639-2 |
| [`label`](#itemsalternativetitlelanguagelabel) | aina | array | Kielen otsikko | |

#### items.\*.alternativeTitle.\*.language.code

`string`

Kielen koodi.

```JSON
"code": "rus"
```

#### items.\*.alternativeTitle.\*.language.label

`array`

Tämä rakenne sisältää kielen otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.alternativeTitle.\*.language.label.\*

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
| [`locale`](#itemsalternativetitlelanguagelabellocale) | aina | string | Kielen otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsalternativetitlelanguagelabelliteral) | aina | array | Kielen otsikko | |

#### items.\*.alternativeTitle.\*.language.label.\*.locale

`string`

Kielen otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### items.\*.alternativeTitle.\*.language.label.\*.literal

`string`

Kielen otsikko.

```JSON
"literal": "venäjä"
```

### items.\*.alternativeTitle.\*.alphabet

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
| [`code`](#itemsalternativetitlealphabetcode) | aina | string | Merkistön koodi | `latin` \| `cyrillic` |
| [`label`](#itemsalternativetitlealphabetlabel) | aina | array | Merkistön otsikko | |

#### items.\*.alternativeTitle.\*.alphabet.code

`string`

Merkistön koodi.

```JSON
"code": "latin"
```

#### items.\*.alternativeTitle.\*.alphabet.label

`array`

Tämä rakenne sisältää merkistön otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.alternativeTitle.\*.alphabet.label.\*

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
| [`locale`](#itemsalternativetitlealphabetlabellocale) | aina | string | Merkistön otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsalternativetitlealphabetlabelliteral) | aina | array | Merkistön otsikko | |

#### items.\*.alternativeTitle.\*.alphabet.label.\*.locale

`string`

```JSON
"locale": "fi"
```

#### items.\*.alternativeTitle.\*.alphabet.label.\*.literal

`string`

```JSON
"literal": "latinalainen"
```

### items.\*.alternativeTitle.\*.transliteration

`string`

Nimekkeen translitterointi.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


### items.\*.alternativeTitle.\*.note

`string`

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013"
```

### items.\*.alternativeTitle.\*.publications

`array`

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [

]
```

### items.\*.alternativeTitle.\*.publications.\*

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
| [`reference`](#itemsalternativetitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsalternativetitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.alternativeTitle.\*.publications.\*.reference

`string`

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.alternativeTitle.\*.publications.\*.id

`string`

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

### items.\*.alternativeTitle.\*.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

### items.\*.alternativeTitle.\*.sources.\*

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
| [`reference`](#itemsalternativetitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsalternativetitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.alternativeTitle.\*.sources.\*.reference

`string`

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.alternativeTitle.\*.sources.\*.id

`string`

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```

## items.\*.workCategory

`array`

Tämä rakenne sisältää teosluettelo-objektin teoskategoriat. Kaikilla teosluettelo-objekteilla ei ole teoskategoriaa.

```JSON
"workCategory": [

]
```

### items.\*.workCategory.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin teoskategorian.

```JSON
{
  "code": "withOpusNumber",
  "label": [

  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsworkcategorycode)   | aina | string | Teoskategorian koodi  |   |
| [`label`](#itemsworkcategorylabel)  | aina | array | Teoskategorian otsikko | |


### items.\*.workCategory.\*.code

`string`

Tämä rakenne sisältää teoskategorian koodin.

```JSON
  "code": "withOpusNumber",
```

### items.\*.workCategory.\*.label

`array`

Tämä rakenne sisältää teoskategorian otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.workCategory.\*.label.\*

`object`

Tämä rakenne sisältää teoskategorian otsikon kieliversion.

```JSON
{
  "locale": ,
  "literal":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsworkcategorylabellocale) | aina | string |  Teoskategorian otsikon kielikoodi | ISO 639-1  |
| [`literal`](#itemsworkcategorylabelliteral) | aina | string | Teoskategorian otsikko | |

#### items.\*.workCategory.\*.label.\*.locale

`string`

Teoskategorian otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### items.\*.workCategory.\*.label.\*.literal

`string`

Teoskategorian otsikko.

```JSON
"literal": "Opusnumeroidut teokset"
```


## items.\*.workNumber

`array`

Tämä rakenne sisältää teosluettelo-objektin teosnumerot. Kaikilla teosluettelo-objekteilla ei ole numerointia.

```JSON
"workNumber": [

]
```

### items.\*.workNumber.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin teosnumeron.

```JSON
{
  "number": ,
  "type": {

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
| [`number`](#itemsworknumbernumber) | aina | string |  Teosnumero |  |
| [`type`](#itemsworknumbernumbertype) | joskus | object | Teosnumeron tyyppi | |
| [`note`](#itemsworknumbernumbernote) | joskus | string |  Huomautus teosnumerosta |  |
| [`publications`](#itemsworknumbernumberpublications) | joskus | array | Teosnumeroon liittyvät julkaisut | |
| [`sources`](#itemsworknumbersources) | joskus | array |  Teosnumeron lähteet |  |

### items.\*.workNumber.\*.number

`string`

Teosnumero.

```JSON
"number": "op4",
```


### items.\*.workNumber.\*.type

`object`

Tämä rakenne sisältää teosnumeron tyypin.

```JSON
"type": {
  "code": "opusNumber",
  "label": [

  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsworknumbertypecode) | aina | string |  Teosnumeron tyypin koodi | ISO 639-1  |
| [`label`](#itemsworknumbertypelabel) | aina | array | teosnumeron tyypin otsikon kieliversiot | |

#### items.\*.workNumber.\*.type.code

`string`

Teosnumeron tyypin koodi.

```JSON
"code": "opusNumber",
```
#### items.\*.workNumber.\*.type.label

`array`

Tämä rakenne sisältää teosnumeron tyypin otsikon kieliversiot.

```JSON
"label": [

]
```

#### items.\*.workNumber.\*.type.label.\*

`object`

Tämä rakenne sisältää teosnumeron tyypin otsikon kieliversion.

```JSON
{
  "locale": ,
  "literal":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemsworknumbertypelabellocale) | aina | string |  Teosnumeron tyypin otsikon kielikoodi | ISO 639-1  |
| [`literal`](#itemsworknumbertypelabelliteral) | aina | string | Teosnumeron tyypin otsikko | |

#### items.\*.workNumber.\*.type.label.\*.locale

`string`

Teosnumeron tyypin otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### items.\*.workNumber.\*.type.label.\*.literal

`string`

Teosnumeron tyypin otsikko.

```JSON
"literal": "opusnumero"
```

#### items.\*.workNumber.\*.note

`string`

Huomautus teosnumerosta.

```JSON
 "note": "Poroila 2013"
```

#### items.\*.workNumber.\*.publications

`array`

Tämä rakenne sisältää teosnumeroon liittyvät julkaisut.

```JSON
"publications": [

]
```

#### items.\*.workNumber.\*.publications.\*

`object`

Tämä rakenne sisältää teosnumeroon liittyvän julkaisun.

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsworknumberpublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsworknumberpublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.workNumber.\*.publications.\*.reference

`string`

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.workNumber.\*.publications.\*.id

`string`

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

#### items.\*.workNumber.\*.sources

`array`

Tämä rakenne sisältää teosnumeron lähteet.

```JSON
"sources": [

]
```

#### items.\*.workNumber.\*.sources.\*

`object`

Tämä rakenne sisältää teosnumeron lähteen.

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsworknumbersourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsworknumbersourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.workNumber.\*.sources.\*.reference

`string`

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.workNumber.\*.sources.\*.id

`string`

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```
## items.\*.creationYear

`array`

Tämä rakenne sisältää teosluettelo-objektin luomisajat. Kaikilla teosluettelo-objekteilla ei ole luomisaikaa.


```JSON
"creationYear": [

]
```

### items.\*.creationYear.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin luomisajat.

> [!NOTE]
> Rakenne sisältää enintään 2 luomisajan vuosilukua.

```JSON
{
    "years": [

    ],
    "timespan": ,
    "separateYears": ,
    "note": ,
    "publications": [

    ],
    "sources": [

    ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemscreationyearlabel) | aina | array | Luomisajan otsikko |  |
| [`years`](#itemscreationyearyears) | joskus | array | Luomisajan vuosiluvut | |
| [`timespan`](#itemscreationyeartimespan) | joskus | boolean | Luomisajan vuosiluvut muodostavat aikavälin | |
| [`separateYears`](#itemscreationyearseparateyears) | joskus | boolean | Luomisajan vuosiluvut ovat erillisiä| |
| [`note`](#itemscreationyearnote) | joskus | string | Huomautus luomisajasta | |
| [`publications`](#itemscreationyearpublications) | joskus | array | Luomisaikaan liittyvät julkaisut | |
| [`sources`](#itemscreationyearsources) | joskus | array | Luomisajan lähteet | |

#### items.\*.creationYear.\*.label

Tämä rakenne sisältää luomisajan otsikon kieliversiot.

`array`

```JSON
"label": [

]
```

#### items.\*.creationYear.\*.label.\*


Tämä rakenne sisältää luomisajan otsikon kieliversion.

`object`

```JSON
{
  "locale": ,
  "literal":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemscreationyearlabellocale) | aina | string | Luomisajan otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemscreationyearlabelliteral) | aina | array | Luomisajan otsikko | |

#### items.\*.creationYear.\*.label.\*.locale

`string`

Luomisajan otsikon kielikoodi.

```JSON
"locale": "fi"
```

#### items.\*.creationYear.\*.label.\*.literal

`string`

Luomisajan otsikko.

```JSON
"literal": "1930?-1939?"
```


### items.\*.creationYear.\*.years

`array`

Tämä rakenne sisältää luomisajan vuosiluvut.

> [!NOTE]
> Rakenne sisältää enintään 2 luomisajan vuosilukua.

```JSON
"years": [

]
```

### items.\*.creationYear.\*.years.\*

`object`

Tämä rakenne sisältää luomisajan vuosiluvun.

```JSON
{
    "year": ,
    "yearIsUncertain":
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemscreationyearyearsyear) | aina | integer | Luomisajan vuosiluku |  |
| [`years`](#itemscreationyearyearsyearisuncertain) | joskus | boolean | Luomisajan vuosiluku epävarma | |


### items.\*.creationYear.\*.years.\*.year

`integer`

Luomisajan vuosiluku.

```JSON
"year": 1930,
```

### items.\*.creationYear.\*.years.\*.yearIsUncertain

`boolean`

Luomisajan vuosiluku on epävarma.

```JSON
"yearIsUncertain": true
```

### items.\*.creationYear.\*.timespan

`boolean`

Luomisajan vuosiluvut muodostavat aikavälin. Tieto merkitään vain, kun luomisaika koostuu kahdesta vuosiluvusta ja ne muodostavat aikavälin.

```JSON
"timespan": true
```

### items.\*.creationYear.\*.separateYears

`boolean`

Luomisajan vuosiluvut ovat erillisiä. Tieto merkitään vain, kun luomisaika koostuu kahdesta vuosiluvusta ja ne ovat erillisiä.

```JSON
"separateYears": true
```

### items.\*.creationYear.\*.note

`string`

Huomautus luomisajasta.

```JSON
"note": "\"1930-luku?\" (Poroila 2012)",
```

### items.\*.creationYear.\*.publications

`array`

Tämä rakenne sisältää luomisaikaan liittyvät julkaisut.

```JSON
"publications": [

]
```

#### items.\*.creationYear.\*.publications.\*

`object`

Tämä rakenne sisältää luomisaikaan liittyvän julkaisun.

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

#### items.\*.creationYear.\*.publications.\*.reference

`string`

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.creationYear.\*.publications.\*.id

`string`

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

#### items.\*.creationYear.\*.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

#### items.\*.creationYear.\*.sources.\*

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

#### items.\*.creationYear.\*.sources.\*.reference

`string`

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.creationYear.\*.sources.\*.id

`string`

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```

## items.\*.mediumOfPerformance

`array`

Tämä rakenne sisältää teosluettelo-objektin esityskokoonpanon. Kaikilla teosluettelo-objekteilla ei ole esityskokoonpanoa.

```JSON
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
]
```

## items.\*.genre

`array`

Tämä rakenne sisältää teosluettelo-objektin muodon tai lajityypin. Kaikilla teosluettelo-objekteilla ei ole muotoa tai lajityyppiä.

```JSON
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
]
```


## items.\*.language

`array`

Tämä rakenne sisältää teosluettelo-objektin esityskielen.

```JSON
"language": [
                {
                    "code": "swe",
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "ruotsi"
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
```



## items.\*.incipitText

`array`

Tämä rakenne sisältää teosluettelo-objektin alkusanat.

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
            ],
```


## items.\*.firstPerformed

`array`

Tämä rakenne sisältää teosluettelo-objektin

```JSON
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
]
```


## items.\*.linkedWork

`array`

Tämä rakenne sisältää teosluettelo-objektin

```JSON
            "linkedWork": [
                {
                    "title": "Tango oriental",
                    "id": "work-f328b5a7-d81a-49de-a701-6d2745b7c1d0",
                    "note": "\"Kyseessä on sovitus balettimusiikin La face d’une grande ville osasta nro 6 (Vikande hus).\" (Poroila 2014)",
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
                        }
                    ]
                }
            ],
```



## items.\*.secondaryAuthor

`array`

Tämä rakenne sisältää teosluettelo-objektin

```JSON

 "secondaryAuthor": [

{
    "name": "Siikaniemi, Väinö, 1887-1932",
    "id": "name-82218f56-6189-4c86-a531-48ef060ba704",
    "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000113189",
    "role": {
        "code": "lyricist",
        "label": [
            {
                "locale": "fi",
                "label": "sanoittaja"
            }
        ]
    }
}
 ]
```

## items.\*.note

`string`

Tämä rakenne sisältää huomautuksen teosluettelo-objektista.

```JSON
"note": "\"Alkuperäiset sanat Leo Tolstoi, ruotsintajaa ei tiedetä.\" (Poroila 2014)",
```



## items.\*.publications

`array`

Tämä rakenne sisältää teosluettelo-objektiin liittyvät julkaisut. Kaikilla teosluettelo-objekteilla ei ole liittyviä julkaisuja.

```JSON
  "sources": [
      {
          "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
          "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
      }
  ]
```

## items.\*.sources

`array`

Tämä rakenne sisältää teosluettelo-objektin lähteet. Kaikilla teosluettelo-objekteilla ei ole lähteitä.

```JSON
  "sources": [
      {
          "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
          "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
      }
  ]
```
