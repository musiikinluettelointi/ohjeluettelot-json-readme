# items.\*.misattributedAuthor

Tämä rakenne sisältää teosluettelo-objektin virheellisen tekijän.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `name` | aina | string | Muun tekijän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `id` | aina | string | Virheellisen tekijän tunniste teosluettelossa. | name-{uuid} |
| `kantoUri` | joskus | string | Virheellisen tekijän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |
| `note` | joskus | string | Huomautus virheellisestä tekijästä. | |
| [`publications`](#itemsmisattributedauthorpublications) | joskus | array | Virheelliseen tekijään liittyvät julkaisut. | |
| [`sources`](#itemsmisattributedauthorsources) | joskus | array | Virheellisen tekijän lähteet. | |

## Esimerkki

```JSON
"misattributedAuthor": [
    {
        "name": "Mozart, Wolfgang Amadeus, 1756-1791",
        "id": "name-fd533d48-19e7-4a24-b6c5-d817a5e64694",
        "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000052618",
        "sources": [
            {
                "reference": "Poroila, Heikki (2020). Yhtenäistetty Wolfgang Amadeus Mozart. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 101. Kuudes korjattu painos, verkkoversio 3.0. ISBN 952-5363-00-7. ",
                "id": "source-58c64e7a-3f38-45e4-81a5-b5e0aa85b594"
            }
        ]
    }
]
```

## items.\*.misattributedAuthor.\*.publications

Tämä rakenne sisältää virheelliseen tekijään liittyvät julkaisut.

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

## items.\*.misattributedAuthor.\*.sources

Tämä rakenne sisältää virheellisen tekijän lähteet.

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