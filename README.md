# Tempotreeni

Selaimessa toimiva harjoitusohjelma rumpalille tai muusikolle, joka haluaa treenata sisäistä tempoaan.

- Klikki soi aluksi asetetussa tempossa. Kun soitat tarpeeksi tarkasti, se hiljenee.
- Ohjelma mittaa tempoasi viimeisten iskujen ajalta. Jos se poikkeaa asetetusta enemmän kuin sallit (esim. +3 / −3 bpm), klikki palaa kuuluviin **sinun senhetkisessä tempossasi**, tarttuu soittoosi ja liukuu sitten hitaasti takaisin asetettuun tempoon.
- Iskut tunnistetaan mikrofonilla. Vaihtoehtoina ovat myös napautus/välilyönti ja äänitiedosto (testaukseen).
- Vertailuruudukko voi olla automaattinen (suorat 1/8- ja 1/16-osat tai triolit/shuffle) tai käsin valittu.

## Käyttö

Avaa `tempotreeni.html` selaimessa. Käytä kuulokkeita, ettei klikki kuulu mikrofoniin. Mikrofoni toimii vain https-osoitteessa tai omalta koneelta avattuna.

Paina ensin **Kalibroi** ja soita tai naputa 16 neljäsosaa klikin mukana, niin ohjelma korjaa laitteen viiveen.

## Testiäänet

Kansiossa `testiaanet/` on syntetisoituja rumpunauhoituksia, joiden todellinen tempo tiedetään (`testiaanet.json`):

| Tiedosto | Sisältö |
|---|---|
| `rock_100_tasainen.wav` | rock-komppi, tasainen 100 bpm |
| `funk16_kiihtyy_100_107.wav` | 1/16-funk, kiihtyy 100 → 107 bpm |
| `shuffle_laahaa_100_94.wav` | shuffle, hidastuu 100 → 94 bpm |
| `neljasosat_100_tasainen.wav` | pelkät 1/4-osat, tasainen 100 bpm |
| `neljasosat_kiihtyy_100_115.wav` | pelkät 1/4-osat, kiihtyy 100 → 115 bpm |

Valitse syötteeksi **Äänitiedosto (testi)** ja tempoksi 100 bpm. Tiedoston alku soi yhtä aikaa ensimmäisen klikin kanssa.
