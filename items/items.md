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