# items.\*.musicOriginWork

Tämä rakenne sisältää teosluettelo-objektin musiikin perustana olevat muiden säveltäjien teokset.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Musiikin perustana olevan teoksen nimeke. | |
| `id` | aina | string | Musiikin perustana olevan teoksen tunniste teosluettelossa. | work-{uuid} |
| [`composer`]() | aina | object | Musiikin perustana olevan teoksen säveltäjä. | |
| `note` | joskus | string | Huomautus musiikin perustana olevasta teoksesta. | |
| [`publications`]() | joskus | array | Musiikin perustana olevaan teokseen liittyvät julkaisut. | |
| [`sources`]() | joskus | array | Musiikin perustana olevan teoksen lähteet. | |

## Esimerkki

```JSON
"musicOriginWork": [
    {
        "title": "Sonaatit, viulu, kosketinsoitin, op1",
        "id": "work-8f61a8af-3ba2-4a34-a8ce-1883aa43b516",
        "composer": {
            "name": "Raupach, Hermann Friedrich, 1728-1778",
            "id": "name-31c2da5e-436d-48a4-8d7d-347d461baae2"
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

## items.\*.musicOriginWork.\*.composer

Tämä rakenne sisältää musiikin perustana olevan teoksen säveltäjän.

```JSON
"composer": {
    "name": "Raupach, Hermann Friedrich, 1728-1778",
    "id": "name-31c2da5e-436d-48a4-8d7d-347d461baae2"
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `id` | aina | string | Säveltäjän tunniste teosluettelossa. | name-{uuid} |
| `name` | aina | string | Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `kantoUri` | joskus | string | Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |

## items.\*.musicOriginWork.\*.publications

Tämä rakenne sisältää musiikin perustana olevaan teokseen liittyvät julkaisut.

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

## items.\*.musicOriginWork.\*.sources

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