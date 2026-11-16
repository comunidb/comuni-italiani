**Italiano** · [English](#english)

# Comuni italiani: CAP, PEC e codici ISTAT (Veneto, CSV gratuito)

Elenco aggiornato dei comuni del **Veneto** con **CAP** (anche per i comuni con più CAP),
**PEC**, email e indirizzo del municipio, **codice ISTAT**, **codice catastale**, codice fiscale,
provincia e regione. In CSV, pronto da importare.

Dati modificati l'ultima volta il **16 novembre 2026**, verificati sulle fonti ufficiali il **16 novembre 2026**:
559 comuni, 649 coppie comune/CAP, 7 province. Le fonti sono ricontrollate ogni
settimana; i file cambiano solo quando cambiano i dati.

**Tutta Italia (7.894 comuni) in CSV, Excel (XLSX), JSON e SQL: [comunidb.it/database-comuni-italiani](https://comunidb.it/database-comuni-italiani) · [English: comunidb.it/en](https://comunidb.it/en/).**

## File

| File | Contenuto |
|---|---|
| `csv/comuni.csv` | Un comune per riga: codici, provincia, regione, CAP (uno, o più separati da virgola), `multi_cap`, PEC, email, indirizzo e sito del comune |
| `csv/cap.csv` | Tutte le coppie `codice_istat` e `cap`: i comuni con più CAP hanno una riga per CAP |
| `csv/province.csv` | Le province del Veneto, con il numero di comuni |
| `csv/regioni.csv` | La regione, con il numero di province e di comuni |
| `ATTRIBUZIONI.txt` | Fonti e licenze |

Formato: CSV in UTF-8 con BOM (si aprono correttamente in Excel), separati da virgola; il database
completo è disponibile anche in Excel, JSON e SQL. I codici (ISTAT, CAP, provincia, regione) sono testo:
mantengono gli zeri iniziali.

Le schede di ogni comune e di ogni CAP si consultano gratis su [comunidb.it](https://comunidb.it).

## Colonne

### `csv/comuni.csv`

| Colonna | Contenuto | Content |
|---|---|---|
| `codice_istat` | Codice ISTAT del comune (6 cifre, testo) | ISTAT municipality code (6 digits, text) |
| `comune` | Nome del comune | Municipality name |
| `codice_catastale` | Codice catastale (Belfiore) | Cadastral (Belfiore) code, as used in the Italian tax code |
| `codice_fiscale` | Codice fiscale del comune | Tax code of the municipality |
| `sigla_provincia` | Sigla della provincia | Province abbreviation, as written on addresses (MI, VE) |
| `codice_provincia` | Codice ISTAT della provincia | ISTAT province code |
| `provincia` | Nome della provincia | Province name |
| `codice_regione` | Codice ISTAT della regione | ISTAT region code |
| `regione` | Nome della regione | Region name |
| `ripartizione` | Ripartizione geografica ISTAT | ISTAT geographic area (Nord-ovest, Nord-est, Centro, Sud, Isole) |
| `nuts3` | Codice NUTS 3 (Eurostat) | NUTS 3 code (Eurostat) |
| `cap` | CAP del comune: uno, o più separati da virgola (una riga per CAP in cap.csv) | Postal codes (CAP): a list in JSON, comma-separated in CSV, Excel and SQL |
| `multi_cap` | true se il comune ha più CAP (tutti in cap.csv) | true when the municipality has several postal codes (all in table cap) |
| `pec` | PEC del comune (IndicePA) | Certified email address (PEC, from IndicePA) |
| `email` | Email istituzionale del comune | Institutional email address |
| `indirizzo` | Indirizzo del municipio | Town hall address |
| `cap_sede` | CAP dell'indirizzo del municipio | Postal code of the town hall address |
| `sito_web` | Sito web del comune | Municipality website |

### `csv/cap.csv`

| Colonna | Contenuto | Content |
|---|---|---|
| `codice_istat` | Codice ISTAT del comune (6 cifre, testo) | ISTAT municipality code (joins table comuni) |
| `cap` | Un CAP del comune | One postal code of the municipality |

### `csv/province.csv`

| Colonna | Contenuto | Content |
|---|---|---|
| `codice_provincia` | Codice ISTAT della provincia | ISTAT province code |
| `sigla_provincia` | Sigla della provincia | Province abbreviation |
| `provincia` | Nome della provincia | Province name |
| `tipo_uts` | Tipo di unità territoriale sovracomunale (codice ISTAT) | ISTAT type of supra-municipal unit (code) |
| `codice_regione` | Codice ISTAT della regione | ISTAT region code |
| `regione` | Nome della regione | Region name |
| `comuni` | Numero di comuni | Number of municipalities |

### `csv/regioni.csv`

| Colonna | Contenuto | Content |
|---|---|---|
| `codice_regione` | Codice ISTAT della regione | ISTAT region code |
| `regione` | Nome della regione | Region name |
| `ripartizione` | Ripartizione geografica ISTAT | ISTAT geographic area |
| `province` | Numero di province | Number of provinces |
| `comuni` | Numero di comuni | Number of municipalities |

## Fonti e licenze

- **ISTAT** (elenco dei comuni SITUAS): CC BY 4.0.
- **IndicePA** (AgID): PEC, email, indirizzo, sito web. CC BY 4.0.
- **OpenStreetMap**: CAP dei comuni con più CAP. © OpenStreetMap contributors, ODbL 1.0: la
  tabella `cap.csv` resta sotto ODbL e si può ridistribuire alle sue condizioni.

Dettagli in [`ATTRIBUZIONI.txt`](ATTRIBUZIONI.txt). I dati sono forniti così come sono, senza
garanzia di completezza o esattezza.

## English

**Italian municipalities (*comuni*) of the Veneto region: postal codes, PEC, ISTAT and cadastral codes. Free CSV, checked every week.**

The municipalities of the **Veneto** region of Italy with their **postal codes** (CAP, including municipalities with
several), **certified email (PEC)**, email and town hall address, **ISTAT code**, **cadastral (Belfiore) code**, tax
code, province and region. CSV, ready to import.

Data last changed on **16 November 2026**, checked against the official sources on **16 November 2026**: 559
municipalities, 649 municipality/postal code pairs, 7 provinces. The sources are checked every week; the files change
only when the data change.

**All of Italy (7,894 municipalities) in CSV, Excel (XLSX), JSON and SQL, with frazioni, coordinates, population and
street-level postal codes in the higher plans: [comunidb.it/en](https://comunidb.it/en/).**

### Files

| File | Rows | Content |
|---|---|---|
| `csv/comuni.csv` | 559 | One municipality per row: codes, province, region, postal codes, PEC, email, address, website |
| `csv/cap.csv` | 649 | Every municipality/postal code pair: municipalities with several postal codes have one row each |
| `csv/province.csv` | 7 | The provinces, with their number of municipalities |
| `csv/regioni.csv` | 1 | The region, with its number of provinces and municipalities |
| `ATTRIBUZIONI.txt` | | Sources and licences (Italian) |

CSV files are UTF-8 with a BOM (they open correctly in Excel) and comma-separated. Codes (ISTAT, postal code,
province, region) are text and keep their leading zeros. Column names are Italian; the column tables
([Colonne](#colonne)) give each one in English.

### Sources and licences

- **ISTAT** (SITUAS list of municipalities): CC BY 4.0.
- **IndicePA** (AgID): PEC, email, address, website. CC BY 4.0.
- **OpenStreetMap**: postal codes of the municipalities with several. © OpenStreetMap contributors, ODbL 1.0: the
  `csv/cap.csv` table stays under the ODbL and may be redistributed on its terms.

Provided as is, without warranty of completeness or accuracy. The same sample is on GitHub, Hugging Face and Kaggle
(`comunidb/comuni-italiani`).
