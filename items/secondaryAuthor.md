# items.\*.secondaryAuthor

Tämä rakenne sisältää teosluettelo-objektin muut tekijät.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `name` | aina | string | Muun tekijän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `id` | aina | string | Muun tekijän tunniste teosluettelossa. | name-{uuid} |
| `kantoUri` | joskus | string | Muun tekijän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |
| [`role`](#itemssecondaryauthorrole) | joskus | object | Muun tekijän rooli. | |
| `note` | joskus | string | Huomautus muusta tekijästä. | |
| [`publications`](#itemssecondaryauthorpublications) | joskus | array | Muuhun tekijään liittyvät julkaisut. | |
| [`sources`](#itemssecondaryauthorsources) | joskus | array | Muun tekijän lähteet. | |

## Esimerkki

```JSON
"secondaryAuthor": [
    {
        "name": "Heine, Heinrich, 1797-1856",
        "id": "name-d28f56f6-b3cc-4f84-acf7-79cba52e66a2",
        "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000196030",
        "role": {
            "code": "writer",
            "label": [
                {
                    "locale": "fi",
                    "label": "kirjoittaja"
                }
            ]
        },
        "sources": [
            {
                "reference": "Poroila, Heikki (2012). Yhtenäistetty Armas Järnefelt. Yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 134. PDF. ISBN 978-952-5363-68-5. ",
                "id": "source-e674f774-82d7-48a8-ad7d-6bb3834a747e"
            }
        ]
    }
]
```


## items.\*.secondaryAuthor.\*.role

Tämä rakenne sisältää muun tekijän roolin.

```JSON
"role": {
    "code": "writer",
    "label": [
        {
            "locale": "fi",
            "label": "kirjoittaja"
        }
    ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Muun tekijän roolin koodi |  |
| [`label`](#itemssecondaryauthorrolelabel) | aina | array | Muun tekijän roolin otsikon kieliversiot. | |

### items.\*.secondaryAuthor.\*.role.label

Tämä rakenne sisältää muun tekijän roolin otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "kirjoittaja"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Muun tekijän roolin otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Muun tekijän roolin otsikko. | |

## items.\*.secondaryAuthor.\*.publications

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

## items.\*.secondaryAuthor.\*.sources

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