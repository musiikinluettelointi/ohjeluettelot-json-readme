# items.\*.firstPerformed

Tämä rakenne sisältää teosluettelo-objektin ensiesityksen.

> [!NOTE]
> Teosluettelo-objektilla voi olla useita ensiesityksiä.

| Avain | Läsnä  | Tyyppi  | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemsfirstperformedlabel) | aina   | array   | Ensiesityksen otsikko. | |
| `date` | joskus | string  | Ensiesityksen päivämäärä. |  `YYYY`-`MM`-`DD`  |
| `year` | joskus | integer | Ensiesityksen vuosiluku. | `YYYY` |
| [`place`](#itemsfirstperformedplace) | joskus | object  | Ensiesityksen paikka. | |
| `note` | joskus | string  | Huomautus ensiesityksestä. | |
| [`publications`](#itemsfirstperformedpublications) | joskus | array | Ensiesitykseen liittyvät julkaisut. | |
| [`sources`](#itemsfirstperformedsources) | joskus | array | Ensiesityksen lähteet. | |

## Esimerkki

```JSON
"firstPerformed": [
  {
      "label": [
          {
              "locale": "fi",
              "literal": "Pietari, 1917"
          }
      ],
      "year": 1917,
      "place": {
          "label": [
              {
                  "locale": "fi",
                  "literal": "Pietari"
              }
          ],
          "ysoUri": "http://www.yso.fi/onto/yso/p105354"
      },
      "note": "\"Kantaesitys oli vuonna 1917 Pietarissa, Suomessa 1918\" (Poroila 2014)",
      "sources": [
          {
              "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
              "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
          }
      ]
  },
  {
      "label": [
          {
              "locale": "fi",
              "literal": "Suomi, 1918"
          }
      ],
      "year": 1918,
      "place": {
          "label": [
              {
                  "locale": "fi",
                  "literal": "Suomi"
              }
          ],
          "ysoUri": "http://www.yso.fi/onto/yso/p94426"
      },
      "note": "\"Kantaesitys oli vuonna 1917 Pietarissa, Suomessa 1918\" (Poroila 2014)",
      "sources": [
          {
              "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
              "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
          }
      ]
  }
]
```

## items.\*.firstPerformed.\*.label

Tämä rakenne sisältää ensiesityksen otsikon kieliversiot.

```JSON
"label": [
    {
        "locale": "fi",
        "literal": "Pietari, 1917"
    }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Luomisajan otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Luomisajan otsikko. | |


## items.\*.firstPerformed.\*.place

Tämä rakenne sisältää ensiesityksen paikan. Paikka on poimittu [YSO-paikat-sanastosta](https://finto.fi/yso-paikat/fi/).

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
| [`label`](#itemsfirstperformedplacelabel) | aina | array | Ensiesityksen paikan otsikon kieliversiot. | |
| `ysoUri` | aina | string | Ensiesityksen paikan YSO-paikat-URI | `uri` |

### items.\*.firstPerformed.\*.place.label

Tämä rakenne sisältää ensiesityksen paikan otsikon kieliversiot.

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
| `locale` | aina | string | Ensiesityksen paikan otsikon kielikoodi. | ISO 639-1 |
| `literal` | aina | string | Ensiesityksen paikan otsikko. | |

## items.\*.firstPerformed.\*.publications

Tämä rakenne sisältää ensiesitykseen liittyvät julkaisut.

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

## items.\*.firstPerformed.\*.sources

Tämä rakenne sisältää ensiesityksen lähteet.

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