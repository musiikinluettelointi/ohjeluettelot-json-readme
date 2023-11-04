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