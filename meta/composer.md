# meta.composer

Tämä rakenne sisältää säveltäjän tiedot.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `name` | aina | string | Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja.  |  |
| `id` | aina | string | Säveltäjän tunniste teosluettelossa | name-{uuid} |
| `kantoUri` | joskus | string | Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | uri |
| `url` | joskus | string |  Teosluettelon osoite. Kaikilla säveltäjillä ei ole julkista teosluetteloa.  | url |
| [`introduction`](#metacomposerintroduction) | joskus | array |  Teosluettelon esipuhe.  |  |
| [`workCategories`](#metacomposerworkcategories) | joskus | array |  Säveltäjälle määritellyt teoskategoriat.  |  |


## meta.composer.introduction

`array`

Tämä rakenne sisältää teoksen esipuheen kieliversiot. Kaikille säveltäjille ei ole laadittu esipuhetta.

```JSON
"introduction": [
  {
    "locale": "fi",
    "text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n",
    "author": "Jaska Järvilehto",
    "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe",
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Esipuheen kielikoodi  | ISO 639-1  |
| `text` | aina | string | Teosluettelon esipuhe | |
| `author` | joskus | string | Esipuheen kirjoittaja | |
| `url` | joskus | string |  Esipuheen osoite  | url |


## meta.composer.workCategories

`array`

Tämä rakenne sisältää säveltäjälle määritellyt teoskategoriat. Kaikille säveltäjille ei ole määritelty teoskategorioita.

```JSON
"workCategories": [
  {
    "code": "withOpusNumber",
    "label": [
      {
        "locale": "fi",
        "literal": "Opusnumeroidut teokset"
      }
    ]
  }
]
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `code`  | aina | string | Teoskategorian koodi  |   |
| [`label`](#metacomposerworkcategorieslabel)  | aina | array | Teoskategorian otsikko | |


### meta.composer.workCategories.\*.label

Tämä rakenne sisältää teoskategorian otsikon kieliversiot.

```JSON
"label": [
  {
    "locale": "fi",
    "literal": "Opusnumeroidut teokset"
  }
]
```

> [!INFO]
> Avain `literal` oli aiemmin `text`.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `locale` | aina | string |  Teoskategorian otsikon kielikoodi. | ISO 639-1  |
| `literal` | aina | string | Teoskategorian otsikko. | |


## Esimerkki

```JSON
"composer": {
  "name": "Pingoud, Ernest, 1887-1942",
  "id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
  "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455",
  "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud",
  "introduction": [
    {
      "locale": "fi",
      "text": "Opusnumerot\nSeuraavia opusnumeroita ei ole käytetty Pingoudin teosten yhteydessä: opus 1, opus 2, opus 3, opus 16, opus 19, opus 24, opus 25, opus 26 (Poroila 2014).\nPseudonyymit\nTaidemusiikin lisäksi Pingoud sävelsi iskelmiä salanimillä \"Lauri Ilari\" ja \"Jonny Loke\" (Poroila 2014). Nämä salanimet on tässä tietokannassa merkitty \"muiksi tekijöiksi\" tekijäroolilla \"säveltäjä\".\n",
      "author": "Jaska Järvilehto",
      "url": "https://musiikinluettelointi.fi/ohjeluettelot/ernestpingoud/esipuhe"
    }
  ],
  "workCategories": [
    {
      "code": "withOpusNumber",
      "label": {
          "locale": "fi",
          "literal": "Opusnumeroidut teokset"
      }
    },
    {
      "code": "withoutOpusNumber",
      "label": {
          "locale": "fi",
          "literal": "Opusnumerottomat teokset"
      }
    }
  ]
}
```