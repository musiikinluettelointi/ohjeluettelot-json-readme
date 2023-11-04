# items.\*.composer

`object`

Tämä rakenne sisältää teosluettelo-objektin säveltäjän tiedot. Anonyymeillä teosluettelo-objekteilla ei ole säveltäjää.

```JSON
"composer": {
  "id": ,
  "name": ,
  "kantoUri":
},
```

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`id`](#itemscomposerid) | aina | string | Säveltäjän tunniste teosluettelossa | name-{uuid} |
| [`name`](#itemscomposername) | aina | string | Säveltäjän nimi | |
| [`kantoUri`](#itemscomposerkantouri) | joskus | string | Säveltäjän KANTO URI | |

## items.\*.composer.id

`string`

Säveltäjän tunniste teosluettelossa.

```JSON
"id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8"
```

## items.\*.composer.name

`string`

Säveltäjän nimi.

```JSON
"name": "Pingoud, Ernest, 1887-1942"
```

## items.\*.composer.kantoUri

`string`

Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta.

```JSON
"kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
```