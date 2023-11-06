# items.\*.workCategory

Tämä rakenne sisältää teosluettelo-objektin teoskategoriat.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Teoskategorian koodi  |   |
| [`label`](#itemsworkcategorylabel)  | aina | array | Teoskategorian otsikko | |
| `note` | joskus | string | Huomautus teoskategoriasta. | |
| [`publications`](#itemsworkcategorypublications) | joskus | array | Teoskategoriaan liittyvät julkaisut. | |
| [`sources`](#itemsworkcategorysources) | joskus | array | Teoskategorian lähteet. | |

## Esimerkki

```JSON
"workCategory": [
    {
        "code": "withOpusNumber",
        "label": [
            {
                "locale": "fi",
                "literal": "Opusnumeroidut teokset"
            }
        ]
    }
]
```

### items.\*.workCategory.\*.label

Tämä rakenne sisältää teoskategorian otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "Opusnumeroidut teokset"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Teoskategorian otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Teoskategorian otsikko. | |

## items.\*.workCategory.\*.publications

Tämä rakenne sisältää teoskategoriaan liittyvät julkaisut.

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

## items.\*.workCategory.\*.sources

Tämä rakenne sisältää teoskategorian lähteet.

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