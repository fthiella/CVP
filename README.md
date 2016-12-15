# Catalogo Veneto Prescrivibile

Distribuzione non ufficiale del Catalogo Veneto Prescrivibile in formato .SQL per i principali database:

- PostgreSQL
- SQL Server
- MySQL
- SQLite
- Oracle

Sono presenti le versioni 1.0 ed 1.1 del catalogo.

## Definizione della tabella

|campo | tipo | descrizione|
|---|---|---|
|id | TEXT | chiave primaria|
|descrizione | TEXT | descrizione|
|cvp_codice | TEXT | codice CVP|
|progressivo | INTEGER | progressivo prestazione, 0=prestazione senza figli, 1=padre non prescrivibile, n=numero figlio|
|descrizione_padre | TEXT | descrizione padre|
|descrizione_figli | TEXT | descrizione figlio|
|stampa | TEXT | descrizione breve per la stampa|
|ntr_codice | TEXT | codice tariffario nazionale|
|ntr_descrizione | TEXT | descrizione ntr|
|compatibilita | TEXT | compatibilità|
|peso | INTEGER | peso|
|regole_prescrizione | TEXT | regole di prescrizione|
|branca_1 | TEXT | prima branca|
|branca_2 | TEXT | seconda branca|
|branca_3 | TEXT | terza branca|
|branca_4 | TEXT | quarta branca|
|branca_5 | TEXT | quinta branca|
|incompatibilita | TEXT | incompatibilità con altre prestazioni|
|inclusioni | TEXT | include le prestazioni|
|note | TEXT | prestazione unica|
|numero_sedute_ciclo | TEXT | numero sedute ciclo|
|tipo_accesso | INTEGER | 0=controllo, 1=prima visita, NULL=da specificare in ricetta|
|tariffa | NUMERIC(11, 2) | tariffa|
|codice_prima | TEXT | se controllo, codice relativa prima visita|
|codice_controllo | TEXT | se prima visita, codice relativo controllo|
|codice_sx | TEXT | se prestazione DX, codice relativa prestazione SX|
|codice_dx | TEXT | se prestazione SX, codice relativa prestazione DX|

## Catalogo Ufficiale

Il catalogo ufficiale in formato Excel si può scaricare dal seguente percorso:

https://salute.regione.veneto.it/web/fser/catalogo-veneto-prescrivibile

## Note

I campi `codice_prima`, `codice_controllo`, `codice_sx`, `codice_dx` sono stati completati manualmente, tutti gli altri campi sono ricavati dall'Excel originale. Al momento mancano gli accorpamenti.
