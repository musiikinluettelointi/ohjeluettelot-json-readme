# items.\*.creationYear

`array`

Tämä rakenne sisältää teosluettelo-objektin luomisajat. Kaikilla teosluettelo-objekteilla ei ole luomisaikaa.


```JSON
"creationYear": [

]
```

## items.\*.creationYear.\*

`object`

Tämä rakenne sisältää teosluettelo-objektin luomisajat.

> [!NOTE]
> Rakenne sisältää enintään 2 luomisajan vuosilukua.

```JSON
{
    "years": [

    ],
    "timespan": ,
    "separateYears": ,
    "note": ,
    "publications": [

    ],
    "sources": [

    ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemscreationyearlabel) | aina | array | Luomisajan otsikko |  |
| [`years`](#itemscreationyearyears) | joskus | array | Luomisajan vuosiluvut | |
| [`timespan`](#itemscreationyeartimespan) | joskus | boolean | Luomisajan vuosiluvut muodostavat aikavälin | |
| [`separateYears`](#itemscreationyearseparateyears) | joskus | boolean | Luomisajan vuosiluvut ovat erillisiä| |
| [`note`](#itemscreationyearnote) | joskus | string | Huomautus luomisajasta | |
| [`publications`](#itemscreationyearpublications) | joskus | array | Luomisaikaan liittyvät julkaisut | |
| [`sources`](#itemscreationyearsources) | joskus | array | Luomisajan lähteet | |

## items.\*.creationYear.\*.label

Tämä rakenne sisältää luomisajan otsikon kieliversiot.

`array`

```JSON
"label": [

]
```

### items.\*.creationYear.\*.label.\*


Tämä rakenne sisältää luomisajan otsikon kieliversion.

`object`

```JSON
{
  "locale": ,
  "literal":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#itemscreationyearlabellocale) | aina | string | Luomisajan otsikon kielikoodi | ISO 639-2 |
| [`literal`](#itemscreationyearlabelliteral) | aina | array | Luomisajan otsikko | |

#### items.\*.creationYear.\*.label.\*.locale

`string`

Luomisajan otsikon kielikoodi.

```JSON
"locale": "fi"
```

#### items.\*.creationYear.\*.label.\*.literal

`string`

Luomisajan otsikko.

```JSON
"literal": "1930?-1939?"
```


## items.\*.creationYear.\*.years

`array`

Tämä rakenne sisältää luomisajan vuosiluvut.

> [!NOTE]
> Rakenne sisältää enintään 2 luomisajan vuosilukua.

```JSON
"years": [

]
```

### items.\*.creationYear.\*.years.\*

`object`

Tämä rakenne sisältää luomisajan vuosiluvun.

```JSON
{
    "year": ,
    "yearIsUncertain":
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`year`](#itemscreationyearyearsyear) | aina | integer | Luomisajan vuosiluku |  |
| [`yearIsUncertain`](#itemscreationyearyearsyearisuncertain) | joskus | boolean | Luomisajan vuosiluku epävarma | |


### items.\*.creationYear.\*.years.\*.year

`integer`

Luomisajan vuosiluku.

```JSON
"year": 1930,
```

### items.\*.creationYear.\*.years.\*.yearIsUncertain

`boolean`

Luomisajan vuosiluku on epävarma.

```JSON
"yearIsUncertain": true
```

## items.\*.creationYear.\*.timespan

`boolean`

Luomisajan vuosiluvut muodostavat aikavälin. Tieto merkitään vain, kun luomisaika koostuu kahdesta vuosiluvusta ja ne muodostavat aikavälin.

```JSON
"timespan": true
```

## items.\*.creationYear.\*.separateYears

`boolean`

Luomisajan vuosiluvut ovat erillisiä. Tieto merkitään vain, kun luomisaika koostuu kahdesta vuosiluvusta ja ne ovat erillisiä.

```JSON
"separateYears": true
```

## items.\*.creationYear.\*.note

`string`

Huomautus luomisajasta.

```JSON
"note": "\"1930-luku?\" (Poroila 2012)",
```

## items.\*.creationYear.\*.publications

`array`

Tämä rakenne sisältää luomisaikaan liittyvät julkaisut.

```JSON
"publications": [

]
```

### items.\*.creationYear.\*.publications.\*

`object`

Tämä rakenne sisältää luomisaikaan liittyvän julkaisun.

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsnonauthorizedtitlepublicationsreference) | aina | string | Julkaisun lähdeviite | |
| [`id`](#itemsnonauthorizedtitlepublicationsid) | aina | string | Julkaisun tunniste teosluettelossa | publication-{uuid} |

#### items.\*.creationYear.\*.publications.\*.reference

`string`

Julkaisun lähdeviite.

```JSON
"reference": ""
```

#### items.\*.creationYear.\*.publications.\*.id

`string`

Julkaisun tunniste teosluettelossa.

```JSON
"id": ""
```

## items.\*.creationYear.\*.sources

`array`

Tämä rakenne sisältää nimekkeen lähteet.

```JSON
"sources": [

]
```

### items.\*.creationYear.\*.sources.\*

`object`

Tämä rakenne sisältää nimekkeen lähteen.

```JSON
{
  "reference": ,
  "id":
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`reference`](#itemsnonauthorizedtitlesourcesreference) | aina | string | Lähteen lähdeviite | |
| [`id`](#itemsnonauthorizedtitlesourcesid) | aina | string | Lähteen tunniste teosluettelossa | source-{uuid} |

#### items.\*.creationYear.\*.sources.\*.reference

`string`

Lähteen lähdeviite.

```JSON
"reference": "Poroila, Heikki (2013). Yhtenäistetty Toivo Kuula. Teosten yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 154. Toinen laitos, verkkoversio 1.0. ISBN 978-952-5363-53-1."
```

#### items.\*.creationYear.\*.sources.\*.id

`string`

Lähteen tunniste teosluettelossa.

```JSON
"id": "source-165ed660-ccbe-43da-852c-3f5f58c03826"
```