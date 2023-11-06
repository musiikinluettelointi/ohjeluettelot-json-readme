# items.\*.dedicatedTo

Tämä rakenne sisältää teosluettelo-objektin omistukset.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `name` | aina | string | Omistuksen kohteen nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `id` | aina | string | Omistuksen kohteen tunniste teosluettelossa. | name-{uuid} |
| `kantoUri` | joskus | string | Omistuksen kohteen KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |
| `date` | joskus | string  | Omistuksen päivämäärä. |  `YYYY`-`MM`-`DD`  |
| `year` | joskus | integer | Omistuksen vuosiluku. | `YYYY` |
| [`place`](#itemsdedicatedtoplace) | joskus | object  | Omistuksen paikka. | |
| `note` | joskus | string | Huomautus omistuksesta. | |
| [`publications`](#itemsdedicatedtopublications) | joskus | array | Omistukseen liittyvät julkaisut. | |
| [`sources`](#itemsdedicatedtosources) | joskus | array | Omistuksen lähteet. | |

## Esimerkki

```JSON
"dedicatedTo": [
    {
        "name": "Tarvajärvi, Niilo, 1914-2002",
        "id": "name-55bdebdd-785a-485e-8d57-8720cb6d825a",
        "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000060624",
        "sources": [
            {
                "reference": "Poroila, Heikki (2015). Yhtenäistetty Joonas Kokkonen. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 183. PDF. ISBN 978-952-5363-81-4. ",
                "id": "source-dd51ea2b-2d80-4829-9ce7-0fe99f67ab8f"
            }
        ]
    }
]
```

## items.\*.dedicatedTo.\*.place

Tämä rakenne sisältää omistuksen paikan. Paikka on poimittu [YSO-paikat-sanastosta](https://finto.fi/yso-paikat/fi/).

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
| [`label`](#itemsdedicatedtoplacelabel) | aina | array | Tilaajan paikan otsikon kieliversiot. | |
| `ysoUri` | aina | string | Tilaajan paikan YSO-paikat-URI | `uri` |

### items.\*.dedicatedTo.\*.place.label

Tämä rakenne sisältää omistuksen paikan otsikon kieliversiot.

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

## items.\*.dedicatedTo.\*.publications

Tämä rakenne sisältää omistukseen liittyvät julkaisut.

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

## items.\*.dedicatedTo.\*.sources

Tämä rakenne sisältää omistuksen lähteet.

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