# items.\*.composer

Tämä rakenne sisältää teosluettelo-objektin säveltäjän.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `id` | aina | string | Säveltäjän tunniste teosluettelossa. | name-{uuid} |
| `name` | aina | string | Säveltäjän nimi. Teosluettelossa käytetään ensisijaisesti KANTOon auktorisoituja nimenmuotoja. | |
| `kantoUri` | joskus | string | Säveltäjän KANTO URI, mikäli käytettävä nimenmuoto on poimittu KANTOsta. | |

## Esimerkki

```JSON
"composer": {
    "id": "name-44c8f684-070b-49bd-b0bc-e1d881f07fd8",
    "name": "Pingoud, Ernest, 1887-1942",
    "kantoUri": "http://urn.fi/URN:NBN:fi:au:finaf:000064455"
}
```