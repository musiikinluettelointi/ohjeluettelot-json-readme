# ohjeluettelot-json-readme

## Dokumentti

Dokumentti sisältää metatiedot rakenteessa `meta` ja teosluettelo-objektit rakenteessa `items`.

| Avain | Läsnä | Tyyppi | Kuvaus |
| --- | --- | --- | --- |
| [`items`](#items) | aina  | array | Sisältää teosluettelo-objektit |
| [`meta`](#meta) | aina | object | Sisältää dokumentin metatiedot |

## meta

Tämä rakenne sisältää dokumentin metatiedot.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`apiVersion`](meta/apiVersion.md) | aina | string |  Dokumentin tuottanut rajapinta |  |
| [`composer`](meta/composer.md) | aina | object | Säveltäjän tiedot |  |
| [`createdBy`](meta/createdBy.md) | aina | string |  Dokumentin tuottaja | email |
| [`createdAt`](meta/createdAt.md) | aina | string |  Dokumentin luomisaika | ISO 8601 |
| [`license`](meta/license.md) | aina | object |  Dokumentin käyttöehdot |  |


## items

Tämä rakenne sisältää teosluettelon teosluettelo-objektit.

### Teosluettelo-objekti

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`alternativeTitle`](items/alternativeTitle.md) | joskus | array | Vaihtoehtoinen nimeke | |
| [`authorizedTitle`](items/authorizedTitle.md) | joskus | array | Auktorisoitu nimeke  | |
| [`authorizedTitleHistory`](items/authorizedTitleHistory.md) | joskus | array | Auktorisoidun nimekkeen muutoshistoria | |
| [`children`](items/children.md) | joskus | array | Teosluettelo-objektin poikaset  | |
| [`commissionedBy`](items/commissionedBy.md) | joskus | array | Tilaaja  | |
| [`composer`](items/composer.md) | joskus | object | Säveltäjä | |
| [`creationYear`](items/creationYear.md) | joskus | array | Luomisaika | |
| [`dedicatedTo`](items/dedicatedTo.md) | joskus | array | Omistus | |
| [`derivativeWork`](items/derivativeWork.md) | joskus | array | Jhdetut teokset | |
| [`firstPerformed`](items/firstPerformed.md) | joskus | array | Ensiesitys | |
| [`firstPublication`](items/firstPublication.md) | joskus | array | Ensijulkaisu | |
| [`genre`](items/genre.md) | joskus | array | Muoto tai lajityyppi | |
| [`id`](items/id.md) | aina  | string | Teosluettelo-objektin tunniste teosluettelossa | {`work` \| `part` \| `arrangement` \| `translation`}-{uuid} |
| [`incipitText`](items/incipitText.md) | joskus | array | Alkusanat | |
| [`itemType`](items/itemType.md) | aina | string | Teosluettelo-objektin tyyppi | `work` \| `part` \| `arrangement` \| `translation`  |
| [`language`](items/language.md) | joskus | array | Esityskieli | |
| [`linkedWork`](items/linkedWork.md) | joskus | array | Liittyvä teos | |
| [`mediumOfPerformance`](items/mediumOfPerformance.md) | joskus | array | Esityskokoonpano | |
| [`misattributedAuthor`](items/misattributedAuthor.md) | joskus | array | Virheellinen tekijä | |
| [`musicKey`](items/musicKey.md) | joskus | array | Sävellaji | |
| [`musicOriginWork`](items/musicOriginWork.md) | joskus | array | Musiikin perustana oleva teos | |
| [`nonAuthorizedTitle`](items/nonAuthorizedTitle.md) | joskus | array | Auktorisoimaton nimeke | |
| [`note`](items/note.md) | joskus | string | Huomautus | |
| [`parent`](items/parent.md) | joskus  | string | Teosluettelo-objektin emon tunniste teosluettelossa | {`work` \| `part` \| `arrangement`}-{uuid} |
| [`publications`](items/publications.md) | joskus  | array | Liittyvä julkaisu | |
| [`secondaryAuthor`](items/secondaryAuthor.md) | joskus | array | Muu tekijä | |
| [`sources`](items/sources.md) | joskus  | array | Lähde | |
| [`textOriginWork`](items/textOriginWork.md) | joskus  | array | Tekstin perustana oleva teos | |
| [`workCategory`](items/workCategory.md) | joskus | array | Teoskategoria | |
| [`workNumber`](items/workNumber.md) | joskus  | array | Numerointi | |