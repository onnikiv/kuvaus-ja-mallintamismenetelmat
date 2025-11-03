# Assignment 4 - Onni Kivinen

**T1**

Alkuperäinen taulu

| **OpNro** | Sukunimi      | Etunimi | Ins.työn_ohjaaja | Ohjaajan_huone | Kurssi1 | Kurssi2 | Kurssi3 |
| --------: | :------------ | :------ | :--------------- | :------------- | :------ | :------ | :------ |
|       123 | Virta         | Viivi   | Virtanen         | P213           | A13     | A8      |         |
|       214 | Safar         | Farid   | Pavlov           | U414           | B72     | A13     | B4      |
|       413 | Mäkinen       | Jari    | Smith            | V213           | A13     |         |         |
|       517 | van der Merwe | Jan     | Mähönen          | P117           | A8      | A13     |         |

## 1NF - Ensimmäinen normaalimuoto

| **OpNro** | Etunimi | Sukunimi      | Kurssi | Ins. työn_ohjaaja | Ohjaajan_huone |
| --------: | :------ | :------------ | :----: | :---------------- | :------------- |
|       123 | Viivi   | Virta         |   A8   | Virtanen          | P213           |
|       123 | Viivi   | Virta         |  A13   | Virtanen          | P213           |
|       214 | Farid   | Safar         |  A13   | Pavlov            | U414           |
|       214 | Farid   | Safar         |   B4   | Pavlov            | U414           |
|       214 | Farid   | Safar         |  B72   | Pavlov            | U414           |
|       413 | Jari    | Mäkinen       |  A13   | Smith             | V213           |
|       517 | Jan     | van der Merwe |   A8   | Mähönen           | P117           |
|       517 | Jan     | van der Merwe |  A13   | Mähönen           | P117           |

## 2NF - Toinen normaalimuoto

**OPISKELIJA**

| **OpNro** | Etunimi | Sukunimi      |
| --------: | :------ | :------------ |
|       123 | Viivi   | Virta         |
|       214 | Farid   | Safar         |
|       413 | Jari    | Mäkinen       |
|       517 | Jan     | van der Merwe |

**SUORITUS**

| **OpNro** | **Kurssi** | Ins. työn_ohjaaja |
| --------: | :--------: | :---------------- |
|       123 |     A8     | Virtanen          |
|       123 |    A13     | Virtanen          |
|       214 |    A13     | Pavlov            |
|       214 |     B4     | Pavlov            |
|       214 |    B72     | Pavlov            |
|       413 |    A13     | Smith             |
|       517 |     A8     | Mähönen           |
|       517 |    A13     | Mähönen           |

**OHJAAJA**

| **OhjaajanNimi** | Ohjaajan_huone |
| :--------------- | :------------- |
| Virtanen         | P213           |
| Pavlov           | U414           |
| Smith            | V213           |
| Mähönen          | P117           |

## 3NF - Kolmas normaalimuoto

Edellinen on jo käytännössä kolmannessa normaalimuodossa, selkeytyksen suhteen _Ins. työn_ohjaaja_ on nimetty selkeämmin.

**OPISKELIJA**

| **OpNro** | Etunimi | Sukunimi      |
| :-------- | :------ | :------------ |
| 123       | Viivi   | Virta         |
| 214       | Farid   | Safar         |
| 413       | Jari    | Mäkinen       |
| 517       | Jan     | van der Merwe |

**OHJAAJA**

| **OhjaajanNimi** | Ohjaajan_huone |
| :--------------- | :------------- |
| Virtanen         | P213           |
| Pavlov           | U414           |
| Smith            | V213           |
| Mähönen          | P117           |

**SUORITUS**

| **OpNro** | **Kurssi** | **OhjaajaNimi** |
| :-------- | :--------- | :-------------- |
| 123       | A8         | Virtanen        |
| 123       | A13        | Virtanen        |
| 214       | A13        | Pavlov          |
| 214       | B4         | Pavlov          |
| 214       | B72        | Pavlov          |
| 413       | A13        | Smith           |
| 517       | A8         | Mähönen         |
| 517       | A13        | Mähönen         |

## T2

Alkuperäinen taulu

| **Tuotekoodi** | Kuvaus        | Myyjä        | Paikkakunta | Hinta  |
| :------------- | ------------- | ------------ | ----------- | ------ |
| 414            | Robotti-imuri | E-tukku      | Turku       | 249,00 |
|                |               | Sähkötyöt    | Vantaa      | 239,90 |
| 217            | Sähkövatkain  | E-tukku      | Turku       | 84,90  |
|                |               | Sähkötyöt    | Vantaa      | 73,25  |
|                |               | Volttikauppa | Oulu        | 99,90  |

Jaetaan tiedot kolmeen eri tauluihin.

**TUOTE**

| **Tuotekoodi** | TuoteNimi     |
| :------------- | ------------- |
| 414            | Robotti-imuri |
| 217            | Sähkövatkain  |

**YRITYS**

| Myyjä        | Paikkakunta |
| :----------- | ----------- |
| E-tukku      | Turku       |
| Sähkötyöt    | Vantaa      |
| Volttikauppa | Oulu        |

**HINNOITTELU**

| **Tuotekoodi** | Myyjä        | Hinta  |
| :------------- | ------------ | ------ |
| 217            | E-tukku      | 84,90  |
| 414            | E-tukku      | 249,00 |
| 217            | Sähkötyöt    | 73,25  |
| 414            | Sähkötyöt    | 239,00 |
| 217            | Volttikauppa | 99,90  |

## T3
