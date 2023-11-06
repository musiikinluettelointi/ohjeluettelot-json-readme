# items.\*.firstPublication

Tämä rakenne sisältää teosluettelo-objektin ensijulkaisut.

| Avain | Läsnä  | Tyyppi  | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemsfirstpublicationlabel) | aina   | array   | Ensijulkaisun otsikko. | |
| `note` | joskus | string  | Huomautus ensijulkaisusta. | |
| [`publications`](#itemsfirstpublicationpublications) | joskus | array | Ensijulkaisuun liittyvät julkaisut. | |
| [`sources`](#itemsfirstpublicationsources) | joskus | array | Ensijulkaisun lähteet. | |

## Esimerkki

```JSON
"firstPublication": [
    {
        "label": [
            {
                "locale": "fi",
                "literal": "Joulupukki [1958].  (1958). Helsinki, Valistus (yhtiö). "
            }
        ],
        "publications": [
            {
                "reference": "Joulupukki [1958].  (1958). Helsinki, Valistus (yhtiö). ",
                "id": "publication-d9cd27f1-dda2-4aec-bd82-31373f2ffa78"
            }
        ],
        "sources": [
            {
                "reference": "Poroila, Heikki (2015). Yhtenäistetty Joonas Kokkonen. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 183. PDF. ISBN 978-952-5363-81-4. ",
                "id": "source-dd51ea2b-2d80-4829-9ce7-0fe99f67ab8f"
            }
        ]
    }
]
```

## items.\*.firstPublication.\*.label

Tämä rakenne sisältää ensijulkaisun otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "Joulupukki [1958].  (1958). Helsinki, Valistus (yhtiö). "
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Luomisajan otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Luomisajan otsikko. | |

## items.\*.firstPublication.\*.publications

Tämä rakenne sisältää ensijulkaisuun liittyvät julkaisut.

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

## items.\*.firstPublication.\*.sources

Tämä rakenne sisältää ensijulkaisun lähteet.

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