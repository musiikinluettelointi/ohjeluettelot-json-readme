# items.\*.language

Tämä rakenne sisältää teosluettelo-objektin esityskielen.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Esityskielen koodi. | `ISO 639-3` |
| [`label`](#itemslanguagelabel) | aina | array | Esityskielen otsikko. |  |
| `note` | joskus | string | Huomautus esityskielestä. | |
| [`publications`](#itemslanguagepublications) | joskus | array | Esityskieleen liittyvät julkaisut. | |
| [`sources`](#itemslanguagesources) | joskus | array | Esityskielen lähteet. | |

## Esimerkki

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
]
```

### items.\*.language.\*.label

Tämä rakenne sisältää esityskielen otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "ruotsi"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Kielen otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Kielen otsikko. | |

## items.\*.language.\*.publications

Tämä rakenne sisältää esityskieleen liittyvät julkaisut.

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

## items.\*.language.\*.sources

Tämä rakenne sisältää esityskielen lähteet.

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