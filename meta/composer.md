# meta.composer

`object`

Tämä rakenne sisältää säveltäjän tiedot.

```JSON
"composer": {
  "name": ,
  "id": ,
  "kantoUri": ,
  "url": ,
  "introduction": [

  ],
  "workCategories": [

  ]
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`name`](#metacomposername) | aina | string | Säveltäjän nimi  |  |
| [`id`](#metacomposerid) | aina | string | Säveltäjän tunniste teosluettelossa | name-{uuid} |
| [`kantoUri`](#metacomposerkantouri) | joskus | string | Säveltäjän KANTO URI  | uri |
| [`url`](#metacomposerurl) | joskus | string |  Teosluettelon osoite  | url |
| [`introduction`](#metacomposerintroduction) | joskus | array |  Teosluettelon esipuhe  |  |
| [`workCategories`](#metacomposerworkcategories) | joskus | array |  Säveltäjälle määritellyt teoskategoriat  |  |

## meta.composer.name

`string`

Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja.

```JSON
"name": "Pingoud, Ernest, 1887-1942"
```

## meta.composer.id

`string`

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8"
```

## meta.composer.kantoUri

`string`

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```

## meta.composer.url

`string`

Teosluettelon osoite. Kaikilla säveltäjillä ei ole julkista teosluetteloa.

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud"
```

## meta.composer.introduction

`array`

Tämä rakenne sisältää teoksen esipuheen kieliversiot. Kaikille säveltäjille ei ole laadittu esipuhetta.

```JSON
"introduction": [

]
```

### meta.composer.introduction.\*

`object`

Tämä rakenne sisältää teoksen esipuheen kieliversion.

```JSON
{
  "locale": ,
  "text": ,
  "author": ,
  "url":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Esipuheen kielikoodi  | ISO 639-1  |
| `text` | aina | string | Teosluettelon esipuhe | |
| `author` | joskus | string | Esipuheen kirjoittaja | |
| `url` | joskus | string |  Esipuheen osoite  | url |

#### meta.composer.introduction.\*.locale

`string`

Esipuheen kielikoodi.

```JSON
"locale": "fi"
```

#### meta.composer.introduction.\*.text

`string`

Teosluettelon esipuhe.

```JSON
"text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n"
```

#### meta.composer.introduction.\*.author

`string`

Esipuheen kirjoittaja.

```JSON
"author": "Jaska Järvilehto"
```

#### meta.composer.introduction.\*.url

`string`

Esipuheen osoite.

```JSON
"url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe"
```

## meta.composer.workCategories

`array`

Tämä rakenne sisältää säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

```JSON
"workCategories": [

]
```

### meta.composer.workCategories.\*

`object`

Tämä rakenne sisältää säveltäjälle määritellyn teoskategorian.

```JSON
{
  "code": "withOpusNumber",
  "label": [

  ]
}
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`code`](#metacomposerworkcategoriescode)   | aina | string | Teoskategorian koodi  |   |
| [`label`](#metacomposerworkcategorieslabel)  | aina | array | Teoskategorian otsikko | |

#### meta.composer.workCategories.\*.code

`string`

Teoskategorian koodi

```JSON
"code": "withOpusNumber"
```

#### meta.composer.workCategories.\*.label

`array`

Tämä rakenne sisältää teoskategorian otsikon kieliversiot.

```JSON
{
"label": [

]
}
```

#### meta.composer.workCategories.\*.label.\*

> [!WARNING]
> Avain `literal` oli aiemmin `text`.

`object`

Tämä rakenne sisältää teoskategorian otsikon kieliversion.

```JSON
{
  "locale": ,
  "literal":
}
```
| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`locale`](#metacomposerworkcategorieslabellocale) | aina | string |  Teoskategorian otsikon kielikoodi | ISO 639-1  |
| [`literal`](#metacomposerworkcategorieslabelliteral) | aina | string | Teoskategorian otsikko | |

#### meta.composer.workCategories.\*.label.\*.locale

`string`

Teoskategorian otsikon kielikoodi.

```JSON
"locale": "fi"
```
#### meta.composer.workCategories.\*.label.\*.literal

`string`

> [!WARNING]
> Avain `literal` oli aiemmin `text`.

Teoskategorian otsikko.

```JSON
"literal": "Opusnumeroidut teokset"
```