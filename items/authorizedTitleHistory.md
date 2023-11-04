# items.\*.authorizedTitleHistory

Tämä rakenne sisältää teosluettelo-objektin auktorisoidun nimekkeen muutoshistorian, mikäli teosluettelo-objektilla on auktorisoitu nimeke.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `createdAt` | aina | string | Auktorisoidun nimekkeen luomispäivämäärä | `YYYY`-`MM`-`DD` |
| [`authorizedTitle`](#itemsauthorizedtitlehistoryauthorizedtitle) | aina | object | Auktorisoitu nimeke| |

## Esimerkki

```JSON
"authorizedTitleHistory": [
  {
  "createdAt": "2012-11-01",
  "authorizedTitle": {
    "title": "Aallon kehtolaulu",
    "language": {
        "code": "fin",
        "label": [
            {
              "locale": "fi",
              "literal": "suomi"
            }
        ]
    },
    "note": "Poroila 2012",
    "sources": [
        {
          "reference": "Poroila, Heikki (2012). Yhtenäistetty Armas Järnefelt. Yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 134. PDF. ISBN 978-952-5363-68-5. ",
          "id": "source-e674f774-82d7-48a8-ad7d-6bb3834a747e"
        }
      ]
    }
  }
]
```

### items.\*.authorizedTitleHistory.\*.authorizedTitle

Tämä rakenne sisältää muutoshistoriaversion nimekkeen. Rakenne on identtinen rakenteen [`items.*.authorizedTitle`](authorizedTitle.md) kanssa.

| Avain | Läsnä | Tyyppi | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| `title` | aina | string | Auktorisoitu nimeke. |  |
| `offset` | joskus | integer | Ohitettavat merkit. | |
| [`language`](authorizedTitle.md#itemsauthorizedtitlelanguage) | joskus | object | Nimekkeen kieli | |
| [`alphabet`](authorizedTitle.md#itemsauthorizedtitlealphabet) | joskus | object | Nimekkeen merkistö |  |
| [`transliteration`](authorizedTitle.md#itemsauthorizedtitletransliteration) | joskus | string | Nimekkeen translitterointi | `iso9` \| `sfs4900` |
| `note` | joskus | string | Huomautus nimekkeestä | |
| [`publications`](authorizedTitle.md#itemsauthorizedtitlepublications) | joskus | array | Nimekkeeseen liittyvät julkaisut | |
| [`sources`](authorizedTitle.md#itemsauthorizedtitlesources) | joskus | array | Nimekkeen lähteet | |