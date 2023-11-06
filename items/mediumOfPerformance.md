# items.\*.mediumOfPerformance

Tämä rakenne sisältää teosluettelo-objektin esityskokoonpanot.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemsmediumofperformancelabel) | aina | array | Esityskokoonpanon otsikko. |  |
| [`items`](#itemsmediumofperformanceitems) | aina | array | Esityskokoonpanon esittäjät. |  |
| `note` | joskus | string | Huomautus esityskokoonpanosta. | |
| [`publications`](#itemsmediumofperformancepublications) | joskus | array | Esityskokoonpanoon liittyvät julkaisut. | |
| [`sources`](#itemsmediumofperformancesources) | joskus | array | Esityskokoonpanon teoksen lähteet. | |

## Esimerkki

```JSON
"mediumOfPerformance": [
    {
        "label": [
            {
                "locale": "fi",
                "literal": "lauluääni, piano"
            }
        ],
        "items": [
            {
                "label": [
                    {
                        "locale": "fi",
                        "literal": "lauluääni"
                    }
                ],
                "itemCount": 1,
                "itemIsVocal": true,
                "sekoUri": "http://urn.fi/urn:nbn:fi:au:seko:00583"
            },
            {
                "label": [
                    {
                        "locale": "fi",
                        "literal": "piano"
                    }
                ],
                "itemCount": 1,
                "sekoUri": "http://urn.fi/urn:nbn:fi:au:seko:00763"
            }
        ],
        "sources": [
            {
                "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
                "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
            }
        ]
    }
]
```

## items.\*.mediumOfPerformance.\*.label

Tämä rakenne sisältää esityskokoonpanon otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "lauluääni, piano"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Esityskokoonpanon otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Esityskokoonpanon otsikko. | |

## items.\*.mediumOfPerformance.\*.items

Tämä rakenne sisältää esityskokoonpanon esittäjät.

Esittäjät on poimittu [Suomalaisesta esityskokoonpanosanastosta (SEKO)](https://finto.fi/seko/fi/).

> [!NOTE]
> Avaimia `itemCount`, `itemIsVocal`, `itemIsGroup` ja `itemIsContinuo` voidaan hyödyntää [Marc-kentän 382 muodostamisessa](https://wiki.helsinki.fi/pages/viewpage.action?pageId=400875418#id-6.Fyysisenkuvailunjne.kent%C3%A4t(3XX)-382382ESITYSKOKOONPANO(T)).

```JSON
"items": [
    {
        "label": [
            {
                "locale": "fi",
                "literal": "lauluääni"
            }
        ],
        "itemCount": 1,
        "itemIsVocal": true,
        "sekoUri": "http://urn.fi/urn:nbn:fi:au:seko:00583"
    },
    {
        "label": [
            {
                "locale": "fi",
                "literal": "piano"
            }
        ],
        "itemCount": 1,
        "sekoUri": "http://urn.fi/urn:nbn:fi:au:seko:00763"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemsmediumofperformanceitemslabel) | aina | array | Esittäjän otsikko. | |
| `itemCount` | joskus | integer | Esittäjien lukumäärä. | |
| `itemIsVocal` | joskus | boolean | Esittäjä on vokaaliesittäjä. Avain on läsnä vain, jos esittäjä on vokaaliesittäjä. | |
| `itemIsGroup` | joskus | boolean | Esittäjä on esittäjäryhmä. Avain on läsnä vain, jos esittäjä on esittäjäryhmä. | |
| `itemIsContinuo` | joskus | boolean | Esittäjä on continuo. Avain on läsnä vain, jos esittäjä on continuo. | |
| `note` | joskus | string | Huomautus esittäjästä. | |
| `sekoUri` | aina | string | Esittäjän SEKO URI. | `uri` |

### items.\*.mediumOfPerformance.\*.items.\*.label

Tämä rakenne sisältää esittäjän otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "lauluääni"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Esittäjän otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Esittäjän otsikko. | |

## items.\*.mediumOfPerformance.\*.publications

Tämä rakenne sisältää esityskokoonpanoon liittyvät julkaisut.

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

## items.\*.mediumOfPerformance.\*.sources

Tämä rakenne sisältää esityskokoonpanon lähteet.

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