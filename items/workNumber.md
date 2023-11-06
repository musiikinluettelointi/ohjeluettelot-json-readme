# items.\*.workNumber

`array`

Tämä rakenne sisältää teosluettelo-objektin teosnumerot.

## Esimerkki

```JSON
"workNumber": [
    {
        "number": "op5",
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
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `number` | aina | string |  Teosnumero. |  |
| [`type`]() | joskus | object | Teosnumeron tyyppi. | |
| [`note`]() | joskus | string |  Huomautus teosnumerosta. |  |
| [`publications`]() | joskus | array | Teosnumeroon liittyvät julkaisut. | |
| [`sources`]() | joskus | array |  Teosnumeron lähteet. |  |

## items.\*.workNumber.\*.type

Tämä rakenne sisältää teosnumeron tyypin.

```JSON
"type": {
    "code": "opusNumber",
    "label": [
        {
            "locale": "fi",
            "literal": "opusnumero"
        }
    ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#itemsworknumbertypecode) | aina | string |  Teosnumeron tyypin koodi | |
| [`label`](#itemsworknumbertypelabel) | aina | array | teosnumeron tyypin otsikon kieliversiot | |

### items.\*.workNumber.\*.type.code

Teosnumeron tyypin koodi.

| Arvo | Kuvaus |
| --- | --- |
| `catalogNumber`| Teosluettelonumero |
| `opusNumber`| Opusnumero  |
| `orderNumber`| Järjestysnumero |
| `otherNumber`| Muu numero |


### items.\*.workNumber.\*.type.label

`array`

Tämä rakenne sisältää teosnumeron tyypin otsikon kieliversiot.

```JSON
    "label": [
        {
            "locale": "fi",
            "literal": "opusnumero"
        }
    ]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Teosnumeron tyypin otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Teosnumeron tyypin otsikko. | |


## items.\*.workNumber.\*.publications

`array`

Tämä rakenne sisältää teosnumeroon liittyvät julkaisut.

```JSON
"publications": [

]
```

### items.\*.workNumber.\*.publications.\*

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

## items.\*.workNumber.\*.sources

`array`

Tämä rakenne sisältää teosnumeron lähteet.

```JSON
"sources": [

]
```

### items.\*.workNumber.\*.sources.\*

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