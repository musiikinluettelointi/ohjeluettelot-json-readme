# items.\*.textOriginWork

Tämä rakenne sisältää teosluettelo-objektin tekstin perustana olevat teokset.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Tekstin perustana olevan teoksen nimeke. | |
| `id` | aina | string | Tekstin perustana olevan teoksen tunniste teosluettelossa. | work-{uuid} |
| [`author`](#itemstextoriginworkauthor) | aina | object | Tekstin perustana olevan teoksen säveltäjä. | |
| `note` | joskus | string | Huomautus tekstin perustana olevasta teoksesta. | |
| [`publications`](#itemstextoriginworkpublications) | joskus | array | Tekstin perustana olevaan teokseen liittyvät julkaisut. | |
| [`sources`](#itemstextoriginworksources) | joskus | array | Tekstin perustana olevan teoksen lähteet. | |

## Esimerkki

```JSON
"textOriginWork": [
    {
        "title": "Artaserse",
        "id": "work-d255be0b-1a8c-4296-820a-2cf91e2498be",
        "author": {
            "name": "Metastasio, Pietro, 1698-1782",
            "id": "name-09783da2-8ed5-4097-ae77-f076524349f3",
            "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000196817"
        },
        "sources": [
            {
                "reference": "Poroila, Heikki (2020). Yhtenäistetty Wolfgang Amadeus Mozart. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 101. Kuudes korjattu painos, verkkoversio 3.0. ISBN 952-5363-00-7. ",
                "id": "source-58c64e7a-3f38-45e4-81a5-b5e0aa85b594"
            }
        ]
    }
]
```

## items.\*.textOriginWork.\*.author

Tämä rakenne sisältää tekstin perustana olevan teoksen tekijän.

```JSON
"author": {
    "name": "Metastasio, Pietro, 1698-1782",
    "id": "name-09783da2-8ed5-4097-ae77-f076524349f3",
    "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000196817"
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `id` | aina | string | Tekijän tunniste teosluettelossa. | name-{uuid} |
| `name` | aina | string | Tekijän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `kantoUri` | joskus | string | Tekijän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |

## items.\*.textOriginWork.\*.publications

Tämä rakenne sisältää tekstin perustana olevaan teokseen liittyvät julkaisut.

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

## items.\*.textOriginWork.\*.sources

Tämä rakenne sisältää musiikin perustana olevan teoksen lähteet.

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