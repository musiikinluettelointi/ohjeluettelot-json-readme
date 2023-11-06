# items.\*.derivativeWork

Tämä rakenne sisältää teosluettelo-objektista johdetut muiden säveltäjien teokset.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Johdetun teoksen nimeke. | |
| `id` | aina | string | Johdetun teoksen tunniste teosluettelossa. | work-{uuid} |
| [`composer`](#itemsderivativeworkcomposer) | aina | object | Johdetun teoksen säveltäjä. | |
| `note` | joskus | string | Huomautus johdetusta teoksesta. | |
| [`publications`](#itemsderivativeworkpublications) | joskus | array | Muuhun tekijään liittyvät julkaisut. | |
| [`sources`](#itemsderivativeworksources) | joskus | array | Muun tekijän lähteet. | |

## Esimerkki

```JSON
"derivativeWork": [
    {
        "title": "Konsertot, piano, orkesteri, KV39, B-duuri",
        "id": "work-c0e2c9f6-8f32-421a-b64e-979bd581fe39",
        "composer": {
            "name": "Mozart, Wolfgang Amadeus, 1756-1791",
            "id": "name-fd533d48-19e7-4a24-b6c5-d817a5e64694",
            "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000052618"
        },
        "sources": [
            {
                "reference": "Poroila, Heikki (2020). Yhtenäistetty Wolfgang Amadeus Mozart. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 101. Kuudes korjattu painos, verkkoversio 3.0. ISBN 952-5363-00-7. ",
                "id": "source-58c64e7a-3f38-45e4-81a5-b5e0aa85b594"
            }
        ]
    }
],
```

## items.\*.derivativeWork.\*.composer

## items.\*.derivativeWork.\*.publications

Tämä rakenne sisältää muuhun tekijään liittyvät julkaisut.

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

## items.\*.derivativeWork.\*.sources

Tämä rakenne sisältää muun tekijän lähteet.

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