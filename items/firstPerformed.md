# items.\*.firstPerformed

Tämä rakenne sisältää teosluettelo-objektin ensiesityksen.

> [!NOTE]
> Teosluettelo-objektilla voi olla useita ensiesityksiä.

| Avain | Läsnä  | Tyyppi  | Kuvaus | Formaatti |
| --- | --- | --- | --- | --- |
| [`label`](#itemsfirstperformedlabel) | aina   | array   | Ensiesityksen otsikko. | |
| `date` | joskus | string  | Ensiesityksen päivämäärä. | |
| `year` | joskus | integer | Ensiesityksen vuosiluku. | |
| [`place`](#itemsfirstperformedplace) | joskus | object  | Ensiesityksen paikka. | |
| `note` | joskus | string  | Huomautus ensiesityksestä. | |
| [`publications`](#itemsfirstperformedpublications) | joskus | array | Ensiesitykseen liittyvät julkaisut. | |
| [`sources`](#itemsfirstperformedsources) | joskus | array | Ensiesityksen lähteet. | |

## Esimerkki

```JSON
"firstPerformed": [
	[
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
]
```

```JSON
    "firstPerformed": [
                {
                    "label": [
                        {
                            "locale": "fi",
                            "literal": "Helsinki, 09.04.1902"
                        }
                    ],
                    "date": "1902-04-09",
                    "year": 1902,
                    "place": {
                        "label": [
                            {
                                "locale": "fi",
                                "literal": "Helsinki"
                            }
                        ],
                        "ysoUri": "http://www.yso.fi/onto/yso/p94137"
                    },
                    "note": "Kansallisteatteri. \"Tilausteos Kansallisteatterin avajaisiin 9.4.1902.\" (Poroila 2012)",
                    "sources": [
                        {
                            "reference": "Poroila, Heikki (2012). Yhtenäistetty Armas Järnefelt. Yhtenäistettyjen nimekkeiden ohjeluettelo. Helsinki, Suomen musiikkikirjastoyhdistys. Suomen musiikkikirjastoyhdistyksen julkaisusarja, 134. PDF. ISBN 978-952-5363-68-5. ",
                            "id": "source-e674f774-82d7-48a8-ad7d-6bb3834a747e"
                        }
                    ]
                }
            ],
```
