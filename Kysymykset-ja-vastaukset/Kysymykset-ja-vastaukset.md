# Ryhti-rajapintakuvauksista esitetyt kysymykset ja vastaukset niihin
Kommentit kronologisessa järjestyksessä vanhimmasta uusimpaan.

## Vuorovaikutus- ja käsittelytapahtuman lisääminen kaava-asialle
Kommentti jätetty 7.7.2023: Vuorovaikutus- ja käsittelytapahtuman lisääminen kaava-asialle jää ehkä hieman epäselväksi:
Vuorovaikutustapahtuma: (POST) /api/InteractionEvent/{landUseCaseId}/LifeCycleStatus/{lifeCycleStatus}
Käsittelytapahtuma: (POST) /api/SpatialPlanHandlingEvent/{landUseCaseId}
Pitäisikö käsittelytapahtuman lisäävässä metodissa olla vastaavat parametrit, eli puuttuuko /LifeCycleStatus/{lifeCycleStatus} -osuus?

**Vastaus 8.9.2023: Tämä osuus tulee muuttumaan merkittävästi seuraavaan julkaistavaan versioon.**

## Epäloogisuus terminologiassa: InteractionEvent ja HandlingEvent
Kommentti jätetty 7.7.2023: Jos vuorovaikutustapahtuma-osio on "InteractionEvent", niin eikö "SpatialPlanHandlingEvent" -osio voisi olla loogisesti vain "HandlingEvent"?

**Vastaus 8.9.2023: Hyvä huomio. Käymme terminologiaa parhaillaan läpi.**

## Metodien kuvaukset englanniksi ja kirjoitusvirhe
Kommentti jätetty 7.7.2023: Rajapinnan kuvaustekstit ovat pääosin suomeksi, mutta LocalMasterPlanidentifier ja RegionalLandUsePlanidentifier metodien kuvaukset englanniksi. Lisäksi, jos oikein tarkkoja ollaan, näiden metodien identifier-sanan pitäisi alkaa isolla kirjaimella kuten skeemassa muuten on (vrt. LocalDetailedPlanIdentifier).

**Vastaus 8.9.2023: Olemme tarkentaneet ja korjanneet kirjoitusvirheitä seuraavaan versioon. Kuvaustekstit tulevat olemaan suomeksi ja tietorakenteet englanniksi.** 

## Koodistojen pitkät merkkijonot
Kommentti jätetty 7.7.2023: Tämä ei liity suoraan tähän rajanpintakuvaukseen tai edes skeemaan, mutta uusi tapa kuvata joidenkin koodistojen koodiarvot merkkijonona on hämmentävä monellakin tapaa:
- Arvojen pituudet, esim. RY_Kaavamääräyslaji-koodiston koodistoarvo: "valtionOmistamienRakennustenSuojelustaAnnetunAsetuksenNojallaSuojeltuRakennus"
- Onko oikeasti hyvä että merkkijonoarvo on jono suomenkielisiä sanoja?
- Mitä jos koodiarvon kuvaus joskus muuttuu - arvo ei enää vastaa kuvausta?

**Vastaus 8.9.2023: Kaavamääräyslajikoodiston arvot on toteutettu yhteentoimivuustyössä sovitusti. Arvo on pitkä jono, mutta toisaalta muoto mahdollistaa, että koodistoon voidaan lisätä väliin uusia arvoja. JSON-sanomassa toimitettava koodiarvo toimitetaan aina URI-muodossa esimerkiksi, http://uri.suomi.fi/codelist/rytj/RY_Kaavamaarayslaji/code/valtionOmistamienRakennustenSuojelustaAnnetunAsetuksenNojallaSuojeltuRakennus.**

**Kuvaukset eivät voi muuttua. Jos lisäyksiä tulee, tehdään uusi koodi ja koodistosta uusi versio. Olemassa oleva URI ei muutu.** 

## Miten versionhallinta toimii Ryhdin päässä?
Kommentti jätetty 28.7.2023: Eli jos vaikka alueidenkäyttöasia on jo olemassa Ryhdissä, ja vie koko asian uudelleen funktiolla "POST/api/LandUseCase/{landUseCaseidentifier}", mitä tapahtuu? Kumoutuuko vanha kokonaan, tehdäänkö merge, jääkö vanha Ryhtiin talteen?

**Vastaus 8.9.2023: Versionhallinta toimii niin, että sanoma tulee uutena kokonaisuutena ja vanha tieto historioidaan. Kaavan eri elinkaaren vaiheet toimitetaan kokonaisuuksina ja aikaisemmat vaiheet jäävät talteen.**

## Tietorakenteiden kuvaukset, tietojen pakollisuudet, operaatiot ja serialisointi
Kommentti jätetty 28.7.2023. Tietorakenteiden kuvaukset ja tietojen pakollisuudet puuttuvat. Tiedusteltiin sallittujen sanomien serialisointimuodoista, operaatioiden kuvauksista ja operaatioista. Kommentoitiin, että geometrioiden formaattia ei ole vielä määritelty mitenkään.

**Vastaus 8.9.2023: Attribuuttien pakollisuudet näkyvät [kuvaukset-dokumentissa](https://github.com/sykefi/Ryhti-rajapintakuvaukset/blob/8cfab79c1908a404dbbaf4fea7039099ba886076/Dokumentaatio/Kaavoitus/Kuvaukset_kaavatietomalli_v0.3.pdf).
Rajapintakuvauksiin tullaan täydentämään attribuuttien pakollisuuksia ja muotoja. Kaikkia pakollisuuksia ei ole mielekästä kuvata OpenAPI-kuvauksissa, koska pakollisuudet vaihtelevat elinkaarivaiheittain.**

**Operaatioiden kuvaukset ja operaatiot tulevat myöhemmin. Sanomien sallittu serialisointiformaatti on JSON. Geometriat toimitetaan GeoJSON-muodossa osana sanomaa. Tarkempi geometrioiden muoto tullaan päivittämään rajapintakuvauksiin. Geometriatyyppejä (viiva, piste, alue) ei ole erikseen rajapintakuvauksissa määritelty.**

## Kaavayksikön puuttuminen rajapintakuvauksista
Kommentti jätetty 1.8.2023: Kaavayksikkö näyttäisi jääneen tässä vaiheessa pois rajapintamäärittelystä. Ilmeisesti tietoinen valinta. Mitenhän VM:n rahoittamassa KATTI-hankkeessa tähän suhtaudutaan?

**Vastaus 8.9.2023: Kaavayksikkö on jätetty pois, koska kaikki kunnat eivät käytä kaavayksikköä. Kunnat kokivat KAATIO-hankkeessakin kaavayksikköjen toimittamisen hankalaksi. Kaavayksikkö ei perustu lakiin. Kunnat voivat edelleenkin tuottaa kaavayksikköjä ja ratkaista niihin liittyviä kysymyksiä esimerkiksi KATTI-hankkeessa.**

## Vähäinen asemakaavan muutos
Kommentti jätetty 1.8.2023: Vähäinen asemakaavan muutos puuttuu käsitteenä sekä rajapinnasta että validointisäännöistä. Vähäisellä asemakaavan muutoksella ei ole laista tulevia kaikkia samoja pakollisuuksia (esim. OAS:a ei tarvitse laatia, rajatumpi kuuleminen ja valitusoikeus jne.), mitä varsinaisella asemakaavalla on.

Nyt mukana on kaavakohteen osittainen kumoaminen, mikä on hyvä asia. Testit aikanaan osoittavat, miten hallitaan. Kyseessä on kuitenkin ylivertaisesti merkittävin asemakaavoitusta koskeva yksittäinen käyttötapaus.

**Vastaus 8.9.2023: Kiitos kommentista! Tämä on korjattu siten, että OAS ei ole pakollisena asemakaavassa. Tallentaminen onnistuu ilman OASia, mutta käyttäjä saa herätteenä virheilmoituksen, jos OASia ei ole liitetty mukaan.**

## Selvennetäänkö OpenAPI-kuvauksia kaavioilla?
Kommentti jätetty 2.8.2023: En ole toistaiseksi ehtinyt tutustua rajapintakuvausten tietorakenteisiin ja -sisältöihin yksityiskohtaisesti, ja OpenAPI-muodossa niiden läpikäynti vaikuttaa hyvin työläältä. Hyvä kuitenkin, että rajapintakuvauksissa on käytetty OpenAPI-formaattia, joka on nykyään lähes de facto -teollisuusstandandardin asemassa.

1. Pelkät koneluettavat OpenAPI-kuvaukset eivät ole riittäviä Ryhti-rajapintojen ymmärtämiseksi ja arvioimiseksi. Rajapintojen kuvausdokumentissa tulisi olla ainakin seuraavat asiat kuvattuina sanallisesti ja selventävillä kuvilla ja esim. sekvenssi- ja tilakaavioilla täydennettynä:
*	Millä tavoilla Ryhti-järjestelmään voidaan kytkeytyä? Esim. Palveluväylän kautta liityntäpalvelimen kautta, Rest-tyyppisillä HTTPS-rajapinnoilla OData, OpenAPI jne. Onko eri toimijoille rajattu vain tietyt liityntätavat (esim. kunnat, muut viranomaiset, kuntien valtuuttamat yritykset, kuten kaavakonsultit, muut yritykset, kansalaiset)?
Yleiskuva toiminnoista, joita rajapintojen kautta voidaan suorittaa, millaisia käyttäjäoikeuksia niiden suorittamiseen tarvitaan, miten rajapintojen käyttöön tarvittavat käyttäjien, roolien ja valtuutusten hallinta tapahtuu?
*	Yksityiskohtaiset kuvaukset eri käyttäjäryhmien käyttötapausten viemisestä alusta loppuun rajapintaoperaatioiden avulla, sisältäen konkreettisia esimerkkejä kunkin rajapinnan käytöstä todellisuutta vastaavilla tietosisällöillä.
*	Kuvaukset rajapintojen tietoturvakäytännöistä ja palvelutasosta. Miten tietojärjestelmätoimittajien tulisi varautua Ryhti-integraatiossa tapahtuviin erilaisiin virhe- ja ongelmatilanteisiin (esim. operaatioiden atomisuus ja uudelleenyritttäminen)

**Vastaus 8.9.2023: Kiitos kommenteista! OpenApi-kuvausten rinnalle on tulossa erillinen dokumentti, jossa avataan muun muassa yllä mainittuja asioita.**

## GeoJSON vai JSON-FG?
Kommentti jätetty 2.8.2023: En ole löytänyt OpenAPI-kuvauksista mitään vihjettä siitä, että rajapinnoissa käytettäisiin standardimuotoisia paikkatietorakenteita, kuten GeoJSON tai JSON-FG. Olen aiemmasta Ryhti-viestinnästä saanut sen käsityksen, että Ryhti-järjestelmän rajapintojen siirtotiedostojen rakenteiden tuli nimenomaan olla JSON-FG -muotoisia ja erityisesti käyttää OGC- ja ISO -standardeihin perustuvia sijainti- ja geometriatietoja.

**Vastaus 8.9.2023: Sanomien sallittu serialisointiformaatti on JSON. Geometriat toimitetaan GeoJSON-muodossa osana sanomaa. Tarkempi geometrioiden muoto tullaan päivittämään rajapintakuvauksiin. Geometriatyyppejä (viiva, piste, alue) ei ole erikseen rajapintakuvauksissa määritelty.**

## JSOn Schema -tiedostot
Kommentti jätetty 2.8.2023: OpenAPI-kuvauksista on teknisenkin henkilön hyvin hankalaa muodostaa selkeätä kuvaa rajapinnoissa käytettävistä siirtotiedostojen rakenteista, esimerkiksi yhden kaavan tallennusversion tietokokonaisuudesta kaikkine kaavakohteineen, määräyksineen ja muine objektityyppeineen. KAATIOssa käytetyn XML-siirtotiedoston dokumentaatiosta löytyy siirtotiedoston rakennekuvaus esimerkkeineen, ks. https://tietomallit.ymparisto.fi/kehitys/kaatio/xml/esimerkit/ Ryhti-rajapintojen osalta tarvitaan varmasti paljon kattavampi ja yksityiskohtaisempi kuvaus JSON Schema -tiedostoineen, jotta kuntapuolella osataan vaatia järjestelmätoimittajilta oikeita asioita tarjouspyynnöissä. Yhteentoimivuusalustan Tietomallit-työkalun tarjoama tietomallien kuvauksen taso ei ole riittävä teknisen rajapinta-integraation suunnittelun tarpeisiin, eikä Y-alustan luokkien ja OpenAPI-kuvausten JSON-skeemojen vastaavuus ole selkeästi kuvattu.

**Vastaus 8.9.2023: OpenApi-kuvauksissa on mukana schema tietorakenteista. OpenApi-kuvauksissa on pieniä eroja JSON schema -standardiin. Kaikkia JSON-scheman avainsanoja ei ole tuettu sekä, muutamien avainsanojen osalta tuessa pieniä eroja. Esimerkkisanomat ja sanomien tarkat schemat ovat jokaisen api-kuvauksen sisällä.**

## Viittaukset ODataan
Kommentti jätetty 2.8.2023: Näyttäisi, että OpenAPI-rajapintakuvauksissa on viitteitä OData-standardin mukaiseen rajapintaan. Oman kokemukseni perusteella saattaa olla melko vaikeaa saada aikaan hyvin yhteentoimivaa, kattavaa OData-pohjaisten rajapintojen kuvauksia OpenAPI-kuvausten avulla, sillä OData-standardi mahdollistaa hyvin joustavan tavan tehdä tiedonhakuja ja yhdistellä eri objektityyppien (relaatioiden) ominaisuuksien arvoja kyselyparametreina. Lisäksi OData -kyselyt mahdollistavat palautettavan vastauksen muotoilun monin eri tavoin, esimerkiksi $expand- ja  $select-kyselyoptiot (ks. https://www.odata.org/getting-started/basic-tutorial/#queryData). Tällaisten monimuotoisten rajapintojen käyttömahdollisuuksien kuvaaminen staattisilla OpenAPI-kuvauksilla on ymmärtääkseni lähes mahdotonta.
OData on sinänsä varsin toimiva rajapintateknologia silloin, kun kaikki tietomallin relaatioiden avulla yhteen liittyvät tiedot on tallennettu samaan tietokantaan, koska tällöin objektien välisten linkkien yli menevät kyselyt voidaan suorittaa kannassa samalla tietokantakyselyllä. OData-kyselyjen toteuttaminen hajautetusti eri tietokantoihin tallennettuihin tietoaineistoihin on tietääkseni vaikeaa toteuttaa tehokkaasti.

**Vastaus 8.9.2023: Ensimmäisessä julkaistussa versiossa rajapintakuvauksista on viitteitä OData-tuesta. OData-tukea ei kuitenkaan ole tulossa rajapintojen ensimmäisissä versioissa, ja viitteet ODataan on tarkoitus poistaa. OData-viittausten poistamisen yhteydessä tullaan poistamaan myös kaikki muut siirtoformaatit/mediatypet paitsi JSON.**

## Toive UML-malleista
Kommentti jätetty 23.8.2023: Pyysitte palautetta Ryhdin rajapintakuvauksiin liittyen. OpenApi-kuvaukset ovet varsin toimivat kehittäjille, mutta ainakin meillä ja kuntien edustajissa on paljon asian kanssa työskenteleviä joiden asiantuntemus on lähinnä substanssiosaamisen puolella - siis vaikka kaavoituksessa. Tätä silmälläpitäen näkisin että olisi tärkeää että tietomallista ja rajapinnoista olisi olemassa myös UML-kaavioita joista voisi nähdä tiedon rakenteen jatkossakin, kuten vaikka aiemmin tehdyn Kaatio-hankkeen puitteissa oli saatavilla. Nämä kuitenkin avaavat asiaa huomattavasti paremmin maankäytön- ja rakentamisen asiantuntijoille joiden on myös keskeistä ymmärtää tietomallien ja tiedonsiirron sisältö.

**Vastaus 8.9.2023: UML-mallien päivittämisestä on luovuttu, koska pitkälti saman asian ajavat Suomi.fi-yhteentoimivuusalustalta löytyvät mallit. Järjestelmään liittyvät tietomallit kuvaavat tietoja ja niiden välisiä suhteita. 
Olemme koonneet malleista tietoa [tietomallit-verkkosivulle](https://ryhti.syke.fi/ohjeet-ja-tuki/tietomallit/).**






