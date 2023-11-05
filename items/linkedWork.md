# items.\*.linkedWork

Tämä rakenne sisältää teosluettelo-objektiin liittyvät saman säveltäjän teokset.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Liittyvän teoksen nimeke. |  |
| `id` | aina | string | Liittyvän teoksen tunniste teosluettelossa. | `work-{uuid}` |
| `note` | joskus | string | Huomautus liittyvästä teoksesta. | |
| [`publications`](#itemslinkedworkpublications) | joskus | array | Esityskieleen liittyvät julkaisut. | |
| [`sources`](#itemslinkedworksources) | joskus | array | Esityskielen lähteet. | |

## Esimerkki

```JSON
"linkedWork": [
    {
        "title": "Tango oriental",
        "id": "work-f328b5a7-d81a-49de-a701-6d2745b7c1d0",
        "note": "\"Kyseessä on sovitus balettimusiikin La face d’une grande ville osasta nro 6 (Vikande hus).\" (Poroila 2014)",
        "sources": [
            {
                "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
            }
        ]
    }
]
```

## items.\*.linkedWork.\*.publications

Tämä rakenne sisältää liittyvään teokseen liittyvät julkaisut.

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

## items.\*.linkedWork.\*.sources

Tämä rakenne sisältää liittyvän teoksen lähteet.

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