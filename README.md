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

## Rakentamisen rajapintakuvaukset
Rakentamisen rajapintakuvauksia kehitetään. Rajapinnoille ei ole vielä määritelty tarkkaa julkaisuajankohtaa.

## OpenApi-kuvaukset
Rajapintojen kuvaukset löytyvät kansiosta OpenApi. OpenApi-kuvaukset ovat JSON-muodossa ja niitä voi katsella esim. https://editor.swagger.io/ sivuston avulla kopioimalla JSON-tiedoston sisällön sinne.

Suorat linkit kuvauksiin Githubissa
* [Kaavoitus OpenApi.json](https://github.com/sykefi/Ryhti-rajapintakuvaukset/blob/main/OpenApi/Kaavoitus/Palveluv%C3%A4yl%C3%A4/Kaavoitus%20OpenApi.json)
* [Rakentaminen OpanApi Beta.json](https://github.com/sykefi/Ryhti-rajapintakuvaukset/blob/Dev/OpenApi/Rakentaminen/Palveluv%C3%A4yl%C3%A4/Rakentaminen%20OpenApi%20Beta.json)

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

## Testirajapintojen aikataulu
Alla olevan aikataulun avulla pystyy seuraamaan testirajapintojen valmistumista ja arvioimaan, milloin kehitystyö muissa järjestelmissä kannattaa aloittaa.

### Rakennustieto
| Endpoint  | Status | Status päivitetty |
| ------------- | ------------- | ------------- |
| BuildingObject | Hyväksymistestauksessa | 5.12.2023 |
| BuildingPermit | Hyväksymistestauksessa | 5.12.2023 |
| DemolitionPermit | Hyväksymistestauksessa | 12.1.2024 |
| DeviationPermit | Hyväksymistestauksessa | 12.1.2024 |
| LandscapeWorkPermit | Hyväksymistestauksessa | 12.1.2024 |
| PermanentIdentifiers | Valmis | 5.12.2023 |

### Alueidenkäytön suunnitelmatieto
| Endpoint  | Status | Status päivitetty |
| ------------- | ------------- | ------------- |
| LocalDetailedPlanMatter | Tuotantovalmius | 30.1.2024 |
| LocalMasterPlanMatter | Tuotantovalmius | 30.1.2024 |
| RegionalPlanMatter | Tuotantovalmius | 30.1.2024 |

### Yhteiset
| Endpoint  | Status | Status päivitetty |
| ------------- | ------------- | ------------- |
| Document | Valmis | 5.12.2023 |
| Status | Valmis | 5.12.2023 |

### Muut kehitettävät
Tonttijakojen ja maankäyttörajoitusten kehitystyö on kesken. Rajapintakuvaukset valmistuvat Q2/2024. 

### Käyttöliittymät
Ensimmäinen versio kaavatietojen käyttöliittymästä on valmistunut. Käyttöliittymän kehitystä jatketaan siten, että ennen kesää julkaistavassa versiossa voi lomakenäkymän kautta tuoda asiakirjoihin ja päätöksiin liittyvät tiedot, jolloin vain kaavasuunnitelma pitää olla JSON-muodossa.
