# items.\*.workNumber

Tämä rakenne sisältää teosluettelo-objektin teosnumerot.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `number` | aina | string |  Teosnumero. |  |
| [`type`](#itemsworknumbertype) | joskus | object | Teosnumeron tyyppi. | |
| `note` | joskus | string |  Huomautus teosnumerosta. |  |
| [`publications`](#itemsworknumberpublications) | joskus | array | Teosnumeroon liittyvät julkaisut. | |
| [`sources`](#itemsworknumbersources) | joskus | array |  Teosnumeron lähteet. |  |

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
| [`label`](#itemsworknumbertypelabel) | aina | array | Teosnumeron tyypin otsikon kieliversiot | |

### items.\*.workNumber.\*.type.code

Teosnumeron tyypin koodi.

| Arvo | Kuvaus |
| --- | --- |
| `catalogNumber`| Teosluettelonumero |
| `opusNumber`| Opusnumero  |
| `orderNumber`| Järjestysnumero |
| `otherNumber`| Muu numero |


### items.\*.workNumber.\*.type.label

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

Tämä rakenne sisältää teosnumeroon liittyvät julkaisut.

```JSON
"publications": [
  {
    "reference": "",
    "id": ""
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Julkaisun lähdeviite | |
| `id` | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

## items.\*.workNumber.\*.sources

Tämä rakenne sisältää teosnumeron lähteet.

```JSON
"sources": [
  {
    "reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1.",
    "id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Lähteen lähdeviite. | |
| `id` | aina | string | Lähteen tunniste teosluettelossa. | source-{uuid} |