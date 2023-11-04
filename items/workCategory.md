# items.\*.workCategory

`array`

Tämä rakenne sisältää teosluettelo-objektin teoskategoriat. Kaikilla teosluettelo-objekteilla ei ole teoskategoriaa.

```JSON
"workCategory": [

]
```

## items.\*.workCategory.\*

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