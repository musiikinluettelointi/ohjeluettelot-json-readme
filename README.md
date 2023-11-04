# ohjeluettelot-json

## In English

To do

## Dokumentin rakenne

Dokumentti sisältää dokumentin metatiedot ja teosluettelo-objektit.

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

#### meta.createdBy

`string`

Dokumentin tuottaja.

```JSON
"createdBy": "info@musiikinluettelointi.fi"
```

#### meta.createdAt

`string`

Dokumentin luomisaika.

```JSON
"createdAt": "2023-10-31T16:54:50.265847Z"
```

#### meta.license

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

#### meta.license.name

`string`

Dokumentin lisenssi.

```JSON
"name": "CC0 1.0 Universal"
```

#### meta.license.url

`string`

Lisenssin osoite.

```JSON
"url": "http://creativecommons.org/publicdomain/zero/1.0"
```
#### meta.composer

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

#### meta.composer.name

`string`

Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja.

```JSON
"name": "Pingoud, Ernest, 1887-1942"
```

#### meta.composer.id

`string`

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8"
```

#### meta.composer.kantoUri

`string`

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```

#### meta.composer.url

`string`

Teosluettelon osoite. Kaikilla säveltäjillä ei ole julkista teosluetteloa.

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud"
```

#### meta.composer.introduction.\*

`array`

Tämä rakenne sisältää teoksen esipuheen. Kaikille säveltäjille ei ole laadittu esipuhetta.

```JSON
"introduction": [
 
]
```

#### meta.composer.introduction.\*

`object`

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

#### meta.composer.workCategories

`array`

Tämä rakenne sisältää säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

```JSON
"workCategories": [

]
```

#### meta.composer.workCategories.\*

`object`

```JSON
{
  "code": "withOpusNumber",
  "label": {

  }
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#metacomposerworkcategoriescode)   | aina | string | Teoskategorian koodi  |   |
| [`label`](#metacomposerworkcategorieslabel)  | aina | string | Teoskategorian otsikko | |

#### meta.composer.workCategories.\*.code

`string`

Teoskategorian koodi

```JSON
"code": "withOpusNumber"
```

#### meta.composer.workCategories.\*.label

> [!WARNING]
> Avain `literal` oli aiemmin `text`.

`object`

Tämä rakenne sisältää teoskategorian otsikon.

```JSON
"label": {
  "locale": ,
  "literal": 
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Teoskategorian otsikon kielikoodi | ISO 639-1  |
| `literal` | aina | string | Teoskategorian otsikko | |

#### meta.composer.workCategories.\*.label.locale

`string`

Teoskategorian otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### meta.composer.workCategories.\*.label.literal

`string`

> [!WARNING]
> Avain `literal` oli aiemmin `text`.

Teoskategorian otsikko.

```JSON
"literal": "Opusnumeroidut teokset"
```

#### meta.apiVersion

`string`

Dokumentin tuottanut rajapinta.

```JSON
"apiVersion": "v1"
```

### items\*

`array`

Tämä rakenne sisältää teosluettelon teosluettelo-objektit.

```JSON
"items": [

]
```

### items\*

`object`

Tämä rakenne sisältää teosluettelo-objektin.

```JSON
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

#### items.\*.itemType

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

#### items.\*.id

`string`

Teosluettelo-objektin tunniste teosluettelossa.

```JSON
"id": "work-c10de676-0115-474f-895e-26940602371b"
```
#### items.\*.composer

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

#### items.\*.composer.id

`string`

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8"
```

#### items.\*.composer.name

`string`

Säveltäjän nimi.

```JSON
"name": "Pingoud, Ernest, 1887-1942"
```

#### items.\*.composer.kantoUri

`string`

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```

#### items.\*.authorizedTitle

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

#### items.\*.authorizedTitle.title

`string`

Auktorisoitu nimeke.

```JSON
"title": "Vremena goda, op37a"
```

#### items.\*.authorizedTitle.offset

`integer`

Ohitettavat merkit.

```JSON
"offset": 3
```

#### items.\*.authorizedTitle.language

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

Tämä rakenne sisältää kielen otsikon.

```JSON
"label": [

]
```

#### items.\*.authorizedTitle.language.label.\*

`object`

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
#### items.\*.authorizedTitle.alphabet

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

Tämä rakenne sisältää merkistön otsikon.

```JSON
"label": [

]
```

#### items.\*.authorizedTitle.alphabet.label.\*

`object`

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

#### items.\*.authorizedTitle.transliteration

`string`

Nimekkeen translitterointi.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


#### items.\*.authorizedTitle.note

`string`

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013"
```

#### items.\*.authorizedTitle.publications

`array`

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

```JSON
"publications": [

]
```

#### items.\*.authorizedTitle.publications.\*

`object`

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

#### items.\*.authorizedTitle.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

#### items.\*.authorizedTitle.sources.\*

`object`

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

#### items.\*.authorizedTitleHistory

`array`

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen muutoshistorian, mikäli teosluettelo-objektilla on auktorisoitu nimeke.

```JSON
"authorizedTitleHistory": [

]
```

#### items.\*.authorizedTitleHistory.\*

`object`

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

#### items.\*.authorizedTitleHistory.\*.createdAt

`string`

Auktorisoidun nimekkeen luomispäivämäärä. Mikäli kuukautta tai päivää ei ole tiedossa, on ne merkitty numerolla yksi.
```JSON
"createdAt": "2014-07-01"
```

#### items.\*.authorizedTitleHistory.\*.authorizedTitle

`object`

Tämä rakenne sisältää auktorisoidun nimekkeen. Rakenne on identtinen rakenteen [`items\*.authorizedTitle`](#itemsauthorizedtitle) kanssa.

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


#### items.\*.alternativeTitle

`array`

Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot.

```JSON
"alternativeTitle": [

]

```

#### items.\*.alternativeTitle.\*

`object`

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

#### items.\*.alternativeTitle.\*.title

Vaihtoehtoinen nimeke.

```JSON
"title": ""
```

#### items.\*.alternativeTitle.\*.offset

Ohitettavat merkit.

```JSON
"offset": 3
```

#### items.\*.alternativeTitle.\*.language

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

Kielen koodi.

```JSON
"code": "rus"
```

#### items.\*.alternativeTitle.\*.language.label.\*

Tämä rakenne sisältää kielen otsikon.

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
| [`locale`](#itemsalternativetitlelanguagelabellocale) | aina | string | Kielen otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsalternativetitlelanguagelabelliteral) | aina | array | Kielen otsikko | |

#### items.\*.alternativeTitle.\*.language.label.\*.locale

Kielen otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### items.\*.alternativeTitle.\*.language.label.\*.literal

Kielen otsikko.

```JSON
"literal": "venäjä"
```
#### items.\*.alternativeTitle.\*.alphabet

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

Merkistön koodi.

```JSON
"code": "latin"
```

#### items.\*.alternativeTitle.\*.alphabet.label.\*

Tämä rakenne sisältää merkistön otsikon.

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
| [`locale`](#itemsalternativetitlealphabetlabellocale) | aina | string | Merkistön otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemsalternativetitlealphabetlabelliteral) | aina | array | Merkistön otsikko | |

#### items.\*.alternativeTitle.\*.alphabet.label.\*.locale

```JSON
"locale": "fi"
```

#### items.\*.alternativeTitle.\*.alphabet.label.\*.literal

```JSON
"literal": "latinalainen"
```

#### items.\*.alternativeTitle.\*.transliteration

Nimekkeen translitterointi.

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


#### items.\*.alternativeTitle.\*.note

Huomautus nimekkeestä.

```JSON
 "note": "Poroila 2013"
```

#### items.\*.alternativeTitle.\*.publications.\*

Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.

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
| [`reference`](#itemsalternativetitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsalternativetitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.alternativeTitle.\*.publications.\*.reference

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.alternativeTitle.\*.publications.\*.id

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

#### items.\*.alternativeTitle.\*.sources.\*

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [
  {
    "reference": ,
    "id": 
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsalternativetitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsalternativetitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.alternativeTitle.\*.sources.\*.reference

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.alternativeTitle.\*.sources.\*.id

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```

#### items.\*.workCategory

Tämä rakenne sisältää teosluettelo-objektin teoskategorian. Kaikilla teosluettelo-objekteilla ei ole teoskategoriaa.

```JSON

```
#### items.\*.workNumber

Tämä rakenne sisältää teosluettelo-objektin numeroinnin. Kaikilla teosluettelo-objekteilla ei ole numerointia.

```JSON

```
#### items.\*.creationYear

Tämä rakenne sisältää teosluettelo-objektin luomisajan. Kaikilla teosluettelo-objekteilla ei ole luomisaikaa.

```JSON

```
#### items.\*.mediumOfPerformance

Tämä rakenne sisältää teosluettelo-objektin esityskokoonpanon. Kaikilla teosluettelo-objekteilla ei ole esityskokoonpano.

```JSON

```
#### items.\*.genre

Tämä rakenne sisältää teosluettelo-objektin muodon tai lajityypin. Kaikilla teosluettelo-objekteilla ei ole muotoa tai lajityyppiä.

```JSON

```
#### items.\*.sources

Tämä rakenne sisältää teosluettelo-objektin lähteet. Kaikilla teosluettelo-objekteilla ei ole lähteitä.

```JSON

```

```JSON
{
            

     
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
