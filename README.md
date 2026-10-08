# Tempotreeni

Selaimessa toimiva harjoitusohjelma rumpalille tai muusikolle, joka haluaa treenata sisäistä tempoaan.

- Tempon voi asettaa liukurilla tai napauttamalla (Naputa tempo -painike tai T-näppäin).
- Klikki soi aluksi asetetussa tempossa valitsemasi määrän iskuja (alkuklikki). Kun soitat tempossa, se hiljenee.
- Ohjelma mittaa tempoasi viimeisten iskujen ajalta. Jos se poikkeaa asetetusta enemmän kuin sallit (esim. +3 / −3 bpm), klikki palaa kuuluviin **sinun senhetkisessä tempossasi**, tarttuu soittoosi ja liukuu sitten hitaasti takaisin asetettuun tempoon.
- Iskut tunnistetaan mikrofonilla. Vaihtoehtoina ovat myös napautus/välilyönti ja äänitiedosto (testaukseen).
- Vertailuruudukko voi olla automaattinen (suorat 1/8- ja 1/16-osat tai triolit/shuffle) tai käsin valittu.

## Käyttö

Avaa `tempotreeni.html` selaimessa. Käytä kuulokkeita, ettei klikki kuulu mikrofoniin. Mikrofoni toimii vain https-osoitteessa tai omalta koneelta avattuna.

Paina ensin **Kalibroi** ja soita tai naputa 16 neljäsosaa klikin mukana, niin ohjelma korjaa laitteen viiveen.

Jos ohjelma toimii oudosti, kytke päälle **Tallenna harjoitus** (Syöte-osiossa). Lopetettuasi voit ladata mikrofonin äänen (WAV) ja lokin ohjelman tulkinnoista. Äänen ja lokin ajat ovat samalla aikajanalla, joten niistä näkee tarkalleen, mitä ohjelma kuuli ja päätteli. Tallenteet jäävät laitteelle, eikä `.gitignore` päästä niitä repositorioon.

## Testiäänet

Kansiossa `testiaanet/` on syntetisoituja rumpunauhoituksia, joiden todellinen tempo tiedetään (`testiaanet.json`):

| Tiedosto | Sisältö |
|---|---|
| `rock_100_tasainen.wav` | rock-komppi, tasainen 100 bpm |
| `funk16_kiihtyy_100_107.wav` | 1/16-funk, kiihtyy 100 → 107 bpm |
| `shuffle_laahaa_100_94.wav` | shuffle, hidastuu 100 → 94 bpm |
| `neljasosat_100_tasainen.wav` | pelkät 1/4-osat, tasainen 100 bpm |
| `neljasosat_kiihtyy_100_115.wav` | pelkät 1/4-osat, kiihtyy 100 → 115 bpm |
| `fillit_80_tasainen.wav` | 1/8-komppi 80 bpm, kuusi erilaista lyhyttä filliä (1/16, 1/16-triolit, 1/32-rulla, kiirehtivä, flamit, 1/8-triolit) |
| `fillit_80_hyppy.wav` | kuten edellä, mutta komppi jatkuu fillin jälkeen 60–120 ms aiemmin tai myöhemmin samassa tempossa |
| `fillit_80_kiihtyy_86.wav` | fillit ja tempo kiihtyy lopussa 80 → 86 bpm |

Valitse syötteeksi **Äänitiedosto (testi)** ja tempoksi tiedoston alkutempo (100 tai 80 bpm). Tiedoston alku soi yhtä aikaa ensimmäisen klikin kanssa.
