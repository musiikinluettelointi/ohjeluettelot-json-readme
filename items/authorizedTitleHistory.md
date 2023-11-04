# items.\*.authorizedTitleHistory

`array`

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen muutoshistorian, mikäli teosluettelo-objektilla on auktorisoitu nimeke.

```JSON
"authorizedTitleHistory": [

]
```

## items.\*.authorizedTitleHistory.\*

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

Tämä rakenne sisältää muutoshistoriaversion nimekkeen. Rakenne on identtinen rakenteen [`items\*.authorizedTitle`](items/authorizedTitle.md) kanssa.

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