# Assignment 3 - Group task

**T1** . ER-Diagram

![ER-Diagram](../images/03-assignment/ER-diagram.png)

---

**T2** Relational Schema:
![Relational Schema](../images/03-assignment/Relational-Schema.png)

---

**T3** Yksilötyypit ja yhteystyypit

| Nimi          | Kuvaus                                                                | Attribuutit                                                                                     |
| :------------ | :-------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------- |
| Asiakas       | Yksittäinen vieras                                                    | **AsiakasID**, Etunimi, Sukunimi, Puhelinnumero, Sähköposti, Henkilötunnus, SeurueID,RannekeID  |
| Ranneke       | Asiakkaan käytössä oleva ranneke                                      | **RannekeID**, Käyttöönotto pvm, Päättymis pvm, Allinclusive                                    |
| Hotellihuone  | Hotellihuone, jossa seurue majoittuu                                  | **HuoneID**, Huonenumero, Huonetyyppi, Sänkyjen määrä, Luovutusaika, Käyttöönottoaika, SeurueID |
| Asiakasseurue | Kokoelma asiakkaista, esim perhetilanne                               | **SeurueID**, Asiakasmäärä, Saldo, LaskuID                                                      |
| Tuote         | Hotellin myynpisteissä olevat tuotteet                                | **TuoteID**, Tuotenimi, Kappalemäärä, Hinta                                                     |
| Myyntipiste   | Myyntipiste hotellialueella                                           | **MyyntipisteID**, Myyntipistenimi                                                              |
| Varasto       | Hotellin yhteinen varasto, jossa säilytetään myyntipisteiden tuotteet | **VarastoID**                                                                                   |
| Lasku         | Asiakasseurueen ostot sisältävä lasku                                 | **LaskuID**, Maksettu, Valuutta                                                                 |
| Ostotapahtuma | Yksittäinen ostotapahtuma                                             | **OstosID**, Ostohetki, RannekeID,LaskuID,MyyntipisteID                                         |

| Nimi                                   | Kuvaus                                             | Tärkeimmät attribuutit |
| -------------------------------------- | -------------------------------------------------- | ---------------------- |
| Osana                                  | Liittää ostotapahtuman ja tuotteet                 | OstosID, TuoteID       |
| Hyllyssä                               | Yhdistää myyntipisteen ja siellä myytävät tuotteet | MyyntipisteID, TuoteID |
| Varastossa                             | Yhdistää varaston ja siellä olevat tuotteet        | VarastoID, TuoteID     |
| Käytössä (Ranneke–Asiakas)             | Liittää rannekkeen yksittäiseen asiakkaaseen       | RannekeID, AsiakasID   |
| Käytössä (Asiakassereure–Hotellihuone) | Yhdistää seurueen huoneeseen                       | SeuruelID, HuoneID     |
| Laskutettavana (Asiakassereure–Lasku)  | Yhdistää seurueen laskuun                          | SeuruelID, LaskulID    |
| Veloitettava (Ostotapahtuma–Ranneke)   | Liittää ostot rannekkeeseen                        | OstosID, RannekeID     |
| Ostettu (Ostotapahtuma–Myyntipiste)    | Liittää ostot myyntipisteeseen                     | OstosID, MyyntipisteID |
| Sisältyy (Ostotapahtuma–Lasku)         | Liittää ostos laskuun                              | OstosID, LaskulID      |
| Osana (Asiakas–Asiakassereure)         | Yhdistää asiakkaan asiakassereureeseen             | AsiakasID, SeuruelID   |

---

**T4** Mallidata

- Ranneke(1, '2025-06-01', '2025-06-10', TRUE)
- Tuote(1, 'Olut', 50, 5)
- Varasto(1)
- Myyntipiste(1, 'Allasbaari')
- Lasku(1, FALSE, 'EUR')
- Asiakasseurue(1, 4, 100, 1)
- Hotellihuone(1, 101, 'Kahden hengen', 4, '2025-010-01 14:00:00', '2025-10-10 12:00:00', 1)
- Asiakas(1, 'Matti', 'Meikäläinen', '0401234567', 'matti@example.com', '010101A1234', 1, 1),
- Ostotapahtuma(1, '2025-06-02', 1, 1, 1)
- Osana(1, 1)
- Hyllyssä(1, 1)
- Varastossa(1, 1)

---
