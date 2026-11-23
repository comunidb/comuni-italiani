COMUNIDB: ITALIAN MUNICIPALITIES DATABASE (FREE SAMPLE)

Release of 23 November 2026: 559 municipalities (comuni), 649 municipality/postal code pairs,
7 provinces, 1 regions. https://comunidb.it/en/

The column names and the place names are Italian, as in the official sources. This file says what
each column means. Sources and licences are in ATTRIBUZIONI.txt (Italian); a summary in English is
at the end of this file.


FILES

csv/          one CSV file per table: comuni, cap, province, regioni

CSV files are UTF-8 with a BOM (they open correctly in Excel) and comma-separated. Every code
(ISTAT, cadastral, postal code, province, region) is text, so leading zeros survive: 015146, 00124.


TABLE comuni: one row per municipality

codice_istat       ISTAT municipality code (6 digits, text)
comune             Municipality name
codice_catastale   Cadastral (Belfiore) code, as used in the Italian tax code
codice_fiscale     Tax code of the municipality
sigla_provincia    Province abbreviation, as written on addresses (MI, VE)
codice_provincia   ISTAT province code
provincia          Province name
codice_regione     ISTAT region code
regione            Region name
ripartizione       ISTAT geographic area (Nord-ovest, Nord-est, Centro, Sud, Isole)
nuts3              NUTS 3 code (Eurostat)
cap                Postal codes (CAP): a list in JSON, comma-separated in CSV, Excel and SQL
multi_cap          true when the municipality has several postal codes (all in table cap)
pec                Certified email address (PEC, from IndicePA)
email              Institutional email address
indirizzo          Town hall address
cap_sede           Postal code of the town hall address
sito_web           Municipality website


TABLE cap: one row per municipality and postal code

codice_istat       ISTAT municipality code (joins table comuni)
cap                One postal code of the municipality


TABLE province: one row per province

codice_provincia   ISTAT province code
sigla_provincia    Province abbreviation
provincia          Province name
tipo_uts           ISTAT type of supra-municipal unit (code)
codice_regione     ISTAT region code
regione            Region name
comuni             Number of municipalities


TABLE regioni: one row per region

codice_regione     ISTAT region code
regione            Region name
ripartizione       ISTAT geographic area
province           Number of provinces
comuni             Number of municipalities


SOURCES AND LICENCES (summary of ATTRIBUZIONI.txt)

ISTAT and IndicePA data: CC BY 4.0. Tables derived from OpenStreetMap (table cap): (c) OpenStreetMap
contributors, ODbL 1.0; they stay under the ODbL when redistributed. Provided as is, without
warranty of completeness or accuracy.
