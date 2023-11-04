# ohjeluettelot-json-readme

## In English

To do

## Dokumentti

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

Tämä rakenne sisältää dokumentin metatiedot.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`createdBy`](meta/createdBy.md) | aina | string |  Dokumentin tuottaja | email |
| [`createdAt`](meta/createdAt.md) | aina | string |  Dokumentin luomisaika | ISO 8601 |
| [`license`](meta/license.md) | aina | object |  Dokumentin käyttöehdot |  |
| [`composer`](meta/composer.md) | aina | object | Säveltäjän tiedot |  |
| [`apiVersion`](meta/apiVersion.md) | aina | string |  Dokumentin tuottanut rajapinta |  |


## items

Tämä rakenne sisältää teosluettelon teosluettelo-objektit.

### Teosluettelo-objekti

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`itemType`](items/itemType.md) | aina | string | Teosluettelo-objektin tyyppi | `work` \| `part` \| `arrangement` \| `translation`  |
| [`id`](items/id.md) | aina  | string | Teosluettelo-objektin tunniste teosluettelossa | {`work` \| `part` \| `arrangement` \| `translation`}-{uuid} |
| [`parent`](items/parent.md) | joskus  | string | Teosluettelo-objektin emon tunniste teosluettelossa | {`work` \| `part` \| `arrangement`}-{uuid} |
| [`children`](items/children.md) | joskus | array | Teosluettelo-objektin poikaset  | |
| [`composer`](items/composer.md) | joskus | object | Säveltäjä | |
| [`authorizedTitle`](items/authorizedTitle.md) | joskus | array | Auktorisoitu nimeke  | |
| [`authorizedTitleHistory`](items/authorizedTitleHistory.md) | joskus | array | Auktorisoidun nimekkeen muutoshistoria | |
| [`alternativeTitle`](items/alternativeTitle.md) | joskus | array | Vaihtoehtoinen nimeke | |
| [`workCategory`](items/workCategory.md) | joskus | array | Teoskategoria | |
| [`workNumber`](items/workNumber.md) | joskus  | array | Numerointi | |
| [`creationYear`](items/creationYear.md) | joskus | array | Luomisaika | |
| [`mediumOfPerformance`](items/mediumOfPerformance.md) | joskus | array | Esityskokoonpano | |
| [`genre`](items/genre.md) | joskus | array | Muoto tai lajityyppi | |
| [`language`](items/language.md) | joskus | array | Esityskieli | |
| [`secondaryAuthor`](items/secondaryAuthor.md) | joskus | array | Muu tekijä | |
| [`note`](items/note.md) | joskus | string | Huomautus | |
| [`publications`](items/publications.md) | joskus  | array | Liittyvä julkaisu | |
| [`sources`](items/sources.md) | joskus  | array | Lähde | |