# items.\*.alternativeTitle

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoiset nimekkeet. Näitä ovat mm. aiemmat auktorisoidut nimekkeet, nimekkeen eri kieliversiot, lempinimet ja nimekkeen viittausmuodot. |


## Esimerkki

```JSON
 "authorizedTitle": [
  {
    "title": "Kehtolaulu",
    "language": {
      "code": "fin",
      "label": [
        {
          "locale": "fi",
          "literal": "suomi"
        }
      ]
    },
    "sources": [
      {
        "reference": "Poroila, Heikki (2014). Yhtenäistetty Ernest Pingoud. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 169. PDF. ISBN 978-952-5363-68-5. ",
        "id": "source-87511f45-eb6e-414d-832f-eadd88967c4b"
      }
    ]
  }
]
```

## items.\*.alternativeTitle.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää teosluettelo-objektin vaihtoehtoisen nimekkeen. |


```JSON
{
  "title": ,
  "offset": ,
  "language": {

  },
  "alphabet": {

  },
  "transliteration": {

  },
  "note": ,
  "publications": [

  ],
  "sources": [

  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`title`](#itemsalternativetitletitle) | aina | string | Auktorisoitu nimeke. |  |
| [`offset`](#itemsalternativetitleoffset) | joskus | integer | Ohitettavat merkit. | |
| [`language`](#itemsalternativetitlelanguage) | joskus | object | Nimekkeen kieli. | |
| [`alphabet`](#itemsalternativetitlealphabet) | joskus | object | Nimekkeen merkistö. |  |
| [`transliteration`](#itemsalternativetitletransliteration) | joskus | object | Nimekkeen translitterointi. | `iso9` \| `sfs4900` |
| [`note`](#itemsalternativetitlenote) | joskus | string | Huomautus nimekkeestä. | |
| [`publications`](#itemsalternativetitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut. | |
| [`sources`](#itemsalternativetitlesources) | joskus | array | Nimekkeen lähteet. | |

## items.\*.alternativeTitle.\*.title

| Tyyppi | Kuvaus |
| --- | --- |
| string | Vaihtoehtoinen nimeke. |

```JSON
"title": "Kotimaan kaikuja"
```

## items.\*.alternativeTitle.\*.offset

| Tyyppi | Kuvaus |
| --- | --- |
| integer | Ohitettavat merkit. |

```JSON
"offset": 3
```

## items.\*.alternativeTitle.\*.language

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeen kielen. |

```JSON
"language": {
  "code": "rus",
  "label": [
    {
      "locale": "fi",
      "literal": "venäjä"
    }
  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Kielen koodi. | ISO 639-2 |
| [`label`](#itemsalternativetitlelanguagelabel) | aina | array | Tämä rakenne sisältää kielen otsikon kieliversiot. |



### items.\*.alternativeTitle.\*.language.label.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää kielen otsikon kieliversion.|


```JSON
{
  "locale": "fi",
  "literal": "venäjä"
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Kielen otsikon kielikoodi | ISO 639-2 |
| `literal` | aina | array | Kielen otsikko | |

## items.\*.alternativeTitle.\*.alphabet

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeen merkistön. Tieto on tallennettu lähinnä kyrillisestä merkistöstä latinalaiselle merkistölle translitteroiduille nimekkeille.|

```JSON
"alphabet": {
  "code": "latin",
  "label": [
    {
      "locale": "fi",
      "literal": "latinalainen"
    }
  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code` | aina | string | Merkistön koodi | `latin` \| `cyrillic` |
| [`label`](#itemsalternativetitlealphabetlabel) | aina | array | Merkistön otsikko | |

### items.\*.alternativeTitle.\*.alphabet.label.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää merkistön otsikon kieliversion. |

```JSON
{
  "locale": "fi",
  "literal": "latinalainen"
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string | Merkistön otsikon kielikoodi. | ISO 639-2 |
| `literal` | aina | array | Merkistön otsikko. | |

## items.\*.alternativeTitle.\*.transliteration

| Tyyppi | Kuvaus |
| --- | --- |
| string | Nimekkeen translitterointi. |

```JSON
"transliteration": "sfs4900"
```

| Arvo | Kuvaus |
| --- | --- |
| `iso9`| Kansainvälinen standardi |
| `sfs4900`| Kansallinen standardi |


## items.\*.alternativeTitle.\*.note

| Tyyppi | Kuvaus |
| --- | --- |
| string | Huomautus nimekkeestä.|

```JSON
 "note": "Poroila 2013"
```

## items.\*.alternativeTitle.\*.publications

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää nimekkeeseen liittyvät julkaisut.|

```JSON
"publications": [

]
```

## items.\*.alternativeTitle.\*.publications.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeeseen liittyvän julkaisun.|

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Julkaisun lähdeviite | |
| `id` | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

## items.\*.alternativeTitle.\*.sources

| Tyyppi | Kuvaus |
| --- | --- |
| array | Tämä rakenne sisältää nimekkeen lähteet. |

```JSON
"sources": [
  {
    "reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1.",
    "id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
  }
]
```

### items.\*.alternativeTitle.\*.sources.\*

| Tyyppi | Kuvaus |
| --- | --- |
| object | Tämä rakenne sisältää nimekkeen lähteen. |


| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `reference` | aina | string | Lähteen lähdeviite | |
| `id` | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |
