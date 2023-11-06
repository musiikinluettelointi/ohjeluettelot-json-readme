# items.\*.commissionedBy

Tämä rakenne sisältää teosluettelo-objektin tilaajat.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `name` | aina | string | Tilaajan nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `id` | aina | string | Tilaajan tunniste teosluettelossa. | name-{uuid} |
| `kantoUri` | joskus | string | Tilaajan KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |
| `date` | joskus | string  | Tilaajan päivämäärä. |  `YYYY`-`MM`-`DD`  |
| `year` | joskus | integer | Tilaajan vuosiluku. | `YYYY` |
| [`place`](#itemscommissionedbyplace) | joskus | object  | Tilaajan paikka. | |
| `note` | joskus | string | Huomautus tilaajasta. | |
| [`publications`](#itemscommissionedbypublications) | joskus | array | Tilaajaan liittyvät julkaisut. | |
| [`sources`](#itemscommissionedbysources) | joskus | array | Tilaajan lähteet. | |

## Esimerkki

```JSON
"commissionedBy": [
    {
        "name": "Helsingin juhlaviikot",
        "id": "name-5b829f70-0732-4520-a2d9-8c6cdec40001",
        "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000000745",
        "sources": [
            {
                "reference": "Poroila, Heikki (2015). Yhtenäistetty Joonas Kokkonen. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 183. PDF. ISBN 978-952-5363-81-4. ",
                "id": "source-dd51ea2b-2d80-4829-9ce7-0fe99f67ab8f"
            }
        ]
    }
],
```


## items.\*.commissionedBy.\*.place

Tämä rakenne sisältää tilaajan paikan. Paikka on poimittu [YSO-paikat-sanastosta](https://finto.fi/yso-paikat/fi/).

```JSON
"place": {
    "label": [
        {
            "locale": "fi",
            "literal": "Suomi"
        }
    ],
    "ysoUri": "http://www.yso.fi/onto/yso/p94426"
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemscommissionedbyplacelabel) | aina | array | Tilaajan paikan otsikon kieliversiot. | |
| `ysoUri` | aina | string | Tilaajan paikan YSO-paikat-URI | `uri` |

### items.\*.commissionedBy.\*.place.label

Tämä rakenne sisältää tilaajan paikan otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "Suomi"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Tilaajan paikan otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Tilaajan paikan otsikko. | |

## items.\*.commissionedBy.\*.publications

Tämä rakenne sisältää tilaajaan liittyvät julkaisut.

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

## items.\*.commissionedBy.\*.sources

Tämä rakenne sisältää tilaajan lähteet.

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