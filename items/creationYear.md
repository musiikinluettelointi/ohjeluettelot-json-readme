# items.\*.creationYear

Tämä rakenne sisältää teosluettelo-objektin luomisajat.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemscreationyearlabel) | aina | array | Luomisajan otsikko. |  |
| [`years`](#itemscreationyearyears) | joskus | array | Luomisajan vuosiluku. | |
| [`timespan`](#itemscreationyeartimespan) | joskus | boolean | Luomisajan vuosiluvut muodostavat aikavälin. | |
| [`separateYears`](#itemscreationyearseparateyears) | joskus | boolean | Luomisajan vuosiluvut ovat erillisiä. | |
| `note` | joskus | string | Huomautus luomisajasta. | |
| [`publications`](#itemscreationyearpublications) | joskus | array | Luomisaikaan liittyvät julkaisut. | |
| [`sources`](#itemscreationyearsources) | joskus | array | Luomisajan lähteet. | |

## Esimerkki

```JSON
"creationYear": [
  {
    "label": [
      {
        "locale": "fi",
        "literal": "1915-1916"
      }
    ],
    "years": [
      {
        "year": 1915
      },
      {
        "year": 1916
      }
    ],
    "timespan": true,
    "sources": [
      {
        "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
        "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
      }
    ]
  }
]
```

## items.\*.creationYear.\*.label

Tämä rakenne sisältää luomisajan otsikon kieliversiot.

```JSON
"label": [
  {
    "locale": "fi",
    "literal": "1930?-1939?"
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Luomisajan otsikon kielikoodi. | ISO 639-2 |
| `literal` | aina | array | Luomisajan otsikko. | |

## items.\*.creationYear.\*.years

Tämä rakenne sisältää luomisajan vuosiluvut.

> [!NOTE]
> Rakenne sisältää enintään 2 luomisajan vuosilukua.

```JSON
"years": [
  {
    "year": 1930,
    "yearIsUncertain": true
  },
  {
    "year": 1939,
    "yearIsUncertain": true
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `year` | aina | integer | Luomisajan vuosiluku. |  |
| `yearIsUncertain` | joskus | boolean | Luomisajan vuosiluku on epävarma. | |


## items.\*.creationYear.\*.timespan

Luomisajan vuosiluvut muodostavat aikavälin. Tieto merkitään vain, kun luomisaika koostuu kahdesta vuosiluvusta ja ne muodostavat aikavälin.

```JSON
"timespan": true
```

## items.\*.creationYear.\*.separateYears

Luomisajan vuosiluvut ovat erillisiä. Tieto merkitään vain, kun luomisaika koostuu kahdesta vuosiluvusta ja ne ovat erillisiä.

```JSON
"separateYears": true
```

## items.\*.creationYear.\*.publications

Tämä rakenne sisältää luomisaikaan liittyvät julkaisut.

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

## items.\*.creationYear.\*.sources

Tämä rakenne sisältää luomisajan lähteet.

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