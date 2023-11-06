# items.\*.genre

Tämä rakenne sisältää teosluettelo-objektin muodot tai lajityypit.

Muoto tai lajityyppi on poimittu [Suomalaisesta lajityyppi- ja muotosanastosta (SLM)](https://finto.fi/slm/fi/).

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemsgenrelabel) | aina | array | Muodon tai lajityypin otsikko. |  |
| `slmUri` | joskus | string | Muodon tai lajityypin SLM-URI. | `uri` |
| `note` | joskus | string | Huomautus muodosta tai lajityypistä. | |
| [`publications`](#itemsgenrepublications) | joskus | array | Muotoon tai lajityyppiin liittyvät julkaisut. | |
| [`sources`](#itemsgenresources) | joskus | array | Muodon tai lajityypin lähteet. | |

## Esimerkki

```JSON
"genre": [
    {
        "label": [
            {
                "locale": "fi",
                "literal": "orkesterimusiikki"
            }
        ],
        "slmUri": "http://urn.fi/URN:NBN:fi:au:slm:s1009"
    }
]
```

## items.\*.genre.\*.label

Tämä rakenne sisältää muodon tai lajityypin otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "orkesterimusiikki"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Muodon tai lajityypin otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Muodon tai lajityypin otsikko. | |

## items.\*.genre.\*.publications

Tämä rakenne sisältää muotoon tai lajityyppiin liittyvät julkaisut.

```JSON
"publications": [
    {
        "reference": "Joulupukki [1958].  (1958). Helsinki, Valistus (yhtiö). ",
        "id": "publication-d9cd27f1-dda2-4aec-bd82-31373f2ffa78"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Julkaisun lähdeviite | |
| `id` | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

## items.\*.genre.\*.sources

Tämä rakenne sisältää muodon tai lajityypin lähteet.

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