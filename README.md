# Ryhti-rajapintakuvaukset
Tutustu rakennetun ympäristön tietojärjestelmän rajapintojen kuvauksiin, jotka kertovat tietojärjestelmän validointi- ja tallennusrajapintojen toteutustavasta.

Main-haarassa on julkaistu tuotantokäyttöön otettujen palveluiden rajapintakuvaukset. Dev-haarasta löydät kehitysversiot kuvauksista. Kehitysversiota ei versioida, vaan muutokset näkyvät GitHub-repositoryn muutoshistoriasta. Myös kuvauksiin liittyvä dokumentaatio täydentyy. 

## Kommentointi
Rajapintakuvauksiin tutustuminen edellyttää aiempaa kokemusta rajapintojen toteutuksesta ja JSON-tiedostoista. Kuvaukset on tarkoitettu erityisesti teknisille järjestelmäkehittäjille yrityksissä, kunnissa ja muissa organisaatioissa.

Voit lähettää palautetta ja kysymyksiä rajapintakuvauksista osoitteeseen ryhti@syke.fi.

## Kaavoituksen rajapintakuvaukset
Kaavoituksen rajapintakuvaukset on julkaistu tuotantokäyttöön. Rajapinnoista kerätään palautetta kehittäjiltä ja kumppanitestaajilta, jonka perusteella rajapintoja voidaan vielä muuttaa.

### Kaavoituksen julkiset rajapinnat
Rakennetun ympäristön tietojärjestelmän ensimmäiset julkiset rajapinnat kaavoituksen kaavasuunnitelmien validointiin on julkistettu osoitteessa https://api-developer.ymparisto.fi/. Rajapinnan käyttö edellyttää rekisteröitymistä ja API avaimen käyttöä.

Lisää tietoa Suomen ympäristökeskuksen sovelluskehittäjäportaalissa https://api-developer.ymparisto.fi/

## Rakentamisen esimerkki-jsonit
Testatessa voi hyödyntää esimerkki-jsoneita, jotka on julkaistu GitHubiin. 
[Kunnille testi-jsonit](https://github.com/sykefi/Ryhti-rajapintakuvaukset/tree/fffafaaaa89a95e757e73b0d8816404de22fc441/Dokumentaatio/Rakentaminen/Kunnille%20testi-jsonit)

## OpenApi-kuvaukset
Rajapintojen kuvaukset löytyvät kansiosta OpenApi. OpenApi-kuvaukset ovat JSON-muodossa ja niitä voi katsella esim. https://editor.swagger.io/ sivuston avulla kopioimalla JSON-tiedoston sisällön sinne.

Sijanti GitHubissa.
Kuvaukset löytyvät [OpenApi-kansiosta](https://github.com/sykefi/Ryhti-rajapintakuvaukset/tree/main/OpenApi). 

Suomi.fi palveluväylään julkaistut kuvaukset
* [Suomi.fi liityntäkatalogi - testi](https://liityntakatalogi.test.suomi.fi/dataset/ryhti-syke-service)
* [Suomi.fi liityntäkatalogi](https://liityntakatalogi.suomi.fi/organization/suomen-ymparistokeskus)

OpenAPI-spesifikaatio on määrittelykieli APIen kuvaamiseen. OpenAPI-kuvaus on standardoitu tapa määritellä API, mikä auttaa muita ymmärtämään APIn toimintaa ja kyvykkyyksiä. OpenAPI on riippumaton ohjelmointikielestä. 
* [Lue lisää: What is OpenAPI?](https://www.openapis.org/what-is-openapi)

## Rajapintoihin tutustumista tukevat dokumentit
* [Yleiset tietomääritykset ja laatusäännöt](https://ryhti.syke.fi/ohjeet-ja-tuki/tietomallit/tietotyypit/)
* [Rakentamislupa ja rakennuskohde, rajapintojen toiminnallisuudet](https://ryhti.syke.fi/wp-content/uploads/sites/2/2023/12/Rakentamislupa-ja-rakennuskohde.pdf)
* [Rakennustietojen validointisäännöt ja paluuarvot](https://ryhti.syke.fi/wp-content/uploads/sites/2/2023/12/Rakennustietojen-validointisaannot-ja-paluuarvot-Ryhti.pdf)
* [Kaavatietomallin tietomääritykset](https://ryhti.syke.fi/alueidenkaytto/tietomallimuotoinen-kaavoitus/kaavatietomallin-tietomaaritykset/)
* [Kaavatietomallin elinkaari- ja laatusäännöt](https://ryhti.syke.fi/alueidenkaytto/tietomallimuotoinen-kaavoitus/kaavatietomallin-elinkaari-ja-laatusaannot/)
* [Kaavakartan GeoTIFF-vaatimukset](https://ryhti.syke.fi/alueidenkaytto/tietomallimuotoinen-kaavoitus/kaavatietomallin-elinkaari-ja-laatusaannot/kaavakartan-geotiff-vaatimukset/)
* [Tontijaon tietomääritykset](https://ryhti.syke.fi/alueidenkaytto/tietomallimuotoinen-sitova-tonttijako/tonttijaon-tietomaaritykset/)
* [Tonttijaon elinkaari- ja laatusäännöt](https://ryhti.syke.fi/alueidenkaytto/tietomallimuotoinen-sitova-tonttijako/tonttijaon-elinkaari-ja-laatusaannot/)
* [Alueidenkäytön rajoitusten tietomääritykset](https://ryhti.syke.fi/alueidenkaytto/tietomallimuotoiset-alueidenkayton-rajoitukset/ryhti-tietojarjestelman-alueidenkayton-rajoitusten-tietomaaritykset-ja-kuvaukset/)
* [Alueidenkäytön rajoitusten elinkaari- ja laatusäännöt](https://ryhti.syke.fi/ryhti-tietojarjestelman-alueidenkayton-rajoitusten-elinkaari-ja-laatusaannot/)
* [Rakennusjärjestyksen tietomääritykset](https://ryhti.syke.fi/tietomallimuotoinen-rakennusjarjestys/ryhti-tietojarjestelman-rakennusjarjestyksen-tietomaaritykset-ja-kuvaukset/)

## Aikataulu: milloin rajapinnat ja käyttöliittymät ovat testattavissa?
Alla olevan aikataulun avulla pystyt seuraamaan Ryhti-järjestelmän rajapintojen ja käyttöliittymäpalveluiden valmistumista. Taulukko auttaa myös arvioimaan, milloin kehitys- ja testaustyö muissa järjestelmissä kannattaa aloittaa.

### Alueidenkäytön rajapintakäyttö
| Rajapinta |	Endpoint | Ryhti-kehitystiimin status	| Kumppaneiden testattavissa |Status päivitetty |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Asemakaava | LocalDetailedPlanMatter | Tuotantoversio julkaistu | Heti | 20.11.2024 |
| Yleiskaava | LocalMasterPlanMatter | Tuotantoversio julkaistu	| Heti | 20.11.2024 |
| Maakuntakaava | RegionalPlanMatter | Tuotantoversio julkaistu | Heti | 20.11.2024 |
| Tiedostojen lataaminen | UploadedFile | Tuotantoversio julkaistu | Heti	| 20.11.2024 |
| Tonttijako | BindingPlotDivisionMatter | Tuotantoversio julkaistu | Heti	| 11.12.2024 |
| Alueidenkäytön rajoitukset | LandUseRestrictionMatter |	Tuotantoversio julkaistu	| Heti | 24.4.2025 |
| Rakennusjärjestys | BuildingOrdinance |	Tuotantoversio julkaistu	| Heti | 11.12.2024 |
| Kaavojen validointipalvelu | Ryhti Plan Public Validate API | Tuotantoversio julkaistu | Heti |	20.11.2024 |

### Alueidenkäytön käyttöliittymäkäyttö
| Rajapinta |	Ryhti-kehitystiimin status	| Kumppaneiden testattavissa | Status päivitetty |
| ------------- | ------------- | ------------- | ------------- |
| Kaavojen sisääntuontikäyttöliittymä: asemakaava | Tuotantoversio julkaistu | Heti | 20.11.2024 |
| Kaavojen sisääntuontikäyttöliittymä: yleiskaava | Tuotantoversio julkaistu | Heti | 20.11.2024 |
| Kaavojen sisääntuontikäyttöliittymä: maakuntakaava | Tuotantoversio julkaistu | Heti | 20.11.2024 |
| Asemakaavan seurantalomake | Tuotantoversio julkaistu | Heti | 20.11.2024 |
| Tiedostojen lataaminen | Tuotantoversio julkaistu | Heti	| 20.11.2024 |
| Rakennusjärjestys | Tuotantoversio julkaistu |	Heti	| 11.12.2024 |
| Karttapalvelu | Tuotantoversio julkaistu | Heti | 24.4.2025 |
| Kaavojen validointipalvelu | Tuotantoversio julkaistu |	Heti	| 20.11.2024 |

### Rakennusluvituksen rajapintakäyttö
| Rajapinta |	Endpoint | Ryhti-kehitystiimin status	| Kumppaneiden testattavissa |Status päivitetty |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Rakennuskohde | BuildingObject | Hyväksymistestattu | Heti | 22.4.2024 |
| Rakentamislupa | BuildingPermit | Hyväksymistestattu	| Heti | 22.4.2024 |
| Purkamislupa | DemolitionPermit | Hyväksymistestattu | Heti | 22.4.2024 |
| Poikkeamislupa | DeviationPermit | Hyväksymistestattu | Heti	| 22.4.2024 |
| Maisematyölupa | LandscapeWorkPermit | Hyväksymistestattu | Heti	| 22.4.2024 |
| Pysyvät tunnukset | PermanentIdentifiers |	Valmis | Heti | 29.2.2024 |
| Tiedostojen lataaminen | - | - | - |	29.2.2024 |

### Rakennusluvituksen käyttöliittymäkäyttö
| Rajapinta |	Ryhti-kehitystiimin status	| Kumppaneiden testattavissa | Status päivitetty |
| ------------- | ------------- | ------------- | ------------- |
| Karttapalvelu | Tuotantoversio julkaistu | Heti | 24.4.2025 |
| Rakennustietojen muokkauskäyttöliittymä | Ei toteuteta vuonna 2024 | -	| 22.4.2024 |
