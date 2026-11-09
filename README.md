# Comuni italiani: CAP, PEC e codici ISTAT (Veneto, CSV gratuito)

Elenco aggiornato dei comuni del **Veneto** con **CAP** (anche per i comuni con più CAP),
**PEC**, email e indirizzo del municipio, **codice ISTAT**, **codice catastale**, codice fiscale,
provincia e regione. In CSV, pronto da importare.

Dati modificati l'ultima volta il **9 novembre 2026**, verificati sulle fonti ufficiali il **9 novembre 2026**:
559 comuni, 649 coppie comune/CAP, 7 province. Le fonti sono ricontrollate ogni
settimana; i file cambiano solo quando cambiano i dati.

**Tutta Italia (7.894 comuni) in CSV, Excel (XLSX), JSON e SQL: [comunidb.it/database-comuni-italiani](https://comunidb.it/database-comuni-italiani).**

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

## Fonti e licenze

- **ISTAT** (elenco dei comuni SITUAS): CC BY 4.0.
- **IndicePA** (AgID): PEC, email, indirizzo, sito web. CC BY 4.0.
- **OpenStreetMap**: CAP dei comuni con più CAP. © OpenStreetMap contributors, ODbL 1.0: la
  tabella `cap.csv` resta sotto ODbL e si può ridistribuire alle sue condizioni.

Dettagli in [`ATTRIBUZIONI.txt`](ATTRIBUZIONI.txt). I dati sono forniti così come sono, senza
garanzia di completezza o esattezza.

## English

A free, weekly-verified CSV of the municipalities (*comuni*) of the Veneto region of Italy:
postal codes (CAP, including municipalities with several), certified email (PEC), ISTAT and
cadastral codes, province and region. The sources are checked every week and the files change only
when the data change. The complete dataset for all of Italy (7,894 municipalities, in CSV, Excel,
JSON and SQL) is at [comunidb.it/database-comuni-italiani](https://comunidb.it/database-comuni-italiani).
