# Ryhti-rajapintakuvaukset
Rakennetun ympäristön tietojärjestelmän rajapintojen kuvaukset, jotka kertovat tietojärjestelmän validointi- ja tallennusrajapintojen toteutustavasta. Kuvaukset päivitettiin joulukuun 2023 alussa, jolloin niihin tuli merkittäviä muutoksia. Ensimmäiset kehitysversiot julkaistiin kesäkuussa 2023.

Rajapintakuvaukset ovat kehitysversioita, joita tullaan täydentämään. Kehitysversiota ei versioida, vaan muutokset näkyvät GitHub-repositoryn muutoshistoriasta. Myös kuvauksiin liittyvä dokumentaatio täydentyy. 

Rajapintakuvauksiin tutustuminen edellyttää aiempaa kokemusta rajapintojen toteutuksesta ja JSON-tiedostoista. Kuvaukset on tarkoitettu erityisesti teknisille järjestelmäkehittäjille yrityksissä, kunnissa ja muissa organisaatioissa.

## Kommentointi
Voit lähettää palautetta ja kysymyksiä rajapintakuvauksista osoitteeseen ryhti@syke.fi.
 
### Ryhti-tiimiä kiinnostaa erityisesti:
* Ovatko rajapintakuvaukset riittävän ymmärrettäviä?
* Tulisiko jotain kuvauksissa selventää?
* Riittävätkö rajapintakuvaukset kuntatietojärjestelmien kehittäjille?

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
* [Rakentamislupa ja rakennuskohde, rajapintojen toiminnallisuudet](https://ryhti.syke.fi/wp-content/uploads/sites/2/2023/12/Rakentamislupa-ja-rakennuskohde.pdf)

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
| LocalDetailedPlanMatter | Hyväksymistestauksessa | 11.12.2023 |
| LocalMasterPlanMatter | Hyväksymistestauksessa | 11.12.2023 |
| RegionalPlanMatter | Hyväksymistestauksessa | 11.12.2023 |

### Yhteiset
| Endpoint  | Status | Status päivitetty |
| ------------- | ------------- | ------------- |
| Document | Valmis | 5.12.2023 |
| Status | Valmis | 5.12.2023 |

### Muut kehitettävät
Tonttijakojen ja maankäyttörajoitusten kehitystyö on kesken. Rajapintakuvaukset valmistuvat Q2/2024. 

### Käyttöliittymät
Kaavatietojen käyttöliittymä on hyväksymistestauksessa (11.12.2023).
