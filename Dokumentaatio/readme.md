# Yleistä käännöstiedostoista

Ryhdin käännetyistä virheteksteistä on tarjolla kaksi tiedostoa:

1. `Ryhti-virhetekstit-ja-käännökset.csv`
2. `Ryhti-virhetekstit-ja-käännökset_[pvm].xlsx`

## CSV-tiedosto

`CSV`-tiedosto mahdollistaa tekstimuutosten vertaamisen tulevaisuudessa versionhallinnan avulla. Tiedosto on puolipiste-eroteltu ja `UTF-8`-enkoodattu. Tiedot on järjestetty aakkosjärjestykseen `Area`- ja `Key`-sarakkeiden mukaan.

## XLSX-tiedosto

Koska sisällössä on rivinvaihtoja, tarjotaan myös Excel-muotoinen `.xlsx`-dokumentti, jotta sisällön oikea näkyvyys voidaan varmistaa.

# Sarakkeiden kuvaus

| Sarake          | Kuvaus                                                                 |
|------------------|------------------------------------------------------------------------|
| `Area`          | Kertoo, liittyykö käännösteksti ensisijaisesti alueidenkäyttöön (`Plan`), rakennustietoihin (`Building`) vai onko käännös yhteinen (`Common`). |
| `Key`           | Käännöksen avain.                                                     |
| `Comment`       | Käännökseen tai sen käyttöön liittyvä kommentti tai ohje englanniksi. |
| `Default language` | Teksti englannin kielellä.                                           |
| `Comment.fi-FI` | Käännökseen tai sen käyttöön liittyvä kommentti tai ohje suomeksi.    |
| `.fi-FI`        | Teksti suomen kielellä.                                               |
| `Comment.sv-SE` | Käännökseen tai sen käyttöön liittyvä kommentti tai ohje ruotsiksi.   |
| `.sv-SE`        | Teksti ruotsin kielellä.                                              |