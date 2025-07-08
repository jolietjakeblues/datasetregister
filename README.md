# RCE Datasetregister

[![DCAT-AP validator](https://img.shields.io/badge/validate-DCAT--AP-blue)](https://data.vlaanderen.be/validator/dcat-ap/)  
[![SHACL validation](https://img.shields.io/badge/validate-SHACL-green)](https://shacl.org/playground/)  
[![License: CC0](https://img.shields.io/badge/license-CC0--1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)  
[![RCE Website](https://img.shields.io/badge/org-cultureelerfgoed.nl-blue)](https://www.cultureelerfgoed.nl)

Deze repository bevat de datasetcatalogus van de Rijksdienst voor het Cultureel Erfgoed (RCE), gepubliceerd in JSON-LD en TriG. De data voldoet aan [DCAT-AP](https://data.europa.eu/eli/dcat-ap/2.0.1), het Europese profiel voor datacatalogi, en volgt de [vereisten van het Netwerk Digitaal Erfgoed (NDE)](https://docs.nde.nl/requirements-datasets/).

---

## ✅ Doelen

Deze catalogus dient twee functies:

1. **Intern beheer**: als actueel datasetregister van RCE.
2. **Extern hergebruik**: als bron voor harvesting door het NDE Datasetregister of andere DCAT-consumers.

---

## 📁 Bestanden

| Bestand                                         | Beschrijving                                       |
|------------------------------------------------|----------------------------------------------------|
| `datacatalog-rce-v1.trig`                      | Volledige catalogus in TriG (meerdere named graphs) |
| `datacatalog-rce-v1.jsonld`                    | Catalogus in JSON-LD (DCAT-AP NL)                 |
| `datacatalog-rce-cho-v1.jsonld`                | Dataset CHO (Cultuurhistorische Objecten)         |
| `datacatalog-rce-cht-v1.jsonld`                | Dataset CHT (Cultuur-Historische Thesaurus)     |
| `datacatalog-rce-abr-v1.jsonld`                | Dataset ABR (Archeologisch Basisregister)         |
| `datacatalog-rce-beeldbank_ld-v1.jsonld`       | Beeldbank subset als Linked Open Data             |
| `datacatalog-rce-beeldbank_oai-v1.jsonld`      | Beeldbank via OAI-PMH                             |
| `datacatalog-rce-bibliotheek_ld-v1.jsonld`     | Bibliotheek RCE (LOD)                             |
| `datacatalog-rce-bibliotheek_oai-v1.jsonld`    | Bibliotheek via OAI-PMH                           |

Alle bestanden zijn handmatig opgesteld en gevalideerd.

---

## 🧩 URI's en identifiers

| Doel                     | URI                                                                 |
|--------------------------|----------------------------------------------------------------------|
| Datasetcatalogus         | [`https://linkeddata.cultureelerfgoed.nl/catalog`](https://linkeddata.cultureelerfgoed.nl/catalog) |
| Organisatie              | [`https://linkeddata.cultureelerfgoed.nl/id/organisatie/rce`](https://linkeddata.cultureelerfgoed.nl/id/organisatie/rce) |
| ISIL-code                | `NL-AmfRCE`                                                          |

---

## 🛠️ Harvesting en hergebruik

De JSON-LD-bestanden kunnen automatisch worden geharvest door o.a. het datasetregister van het NDE.

Voorbeeldinstructie voor registreren van deze catalogus als bron:

```json
{
  "@id": "https://linkeddata.cultureelerfgoed.nl/catalog",
  "@type": "dcat:Catalog",
  "dct:publisher": {
    "@id": "https://linkeddata.cultureelerfgoed.nl/id/organisatie/rce"
  }
}
