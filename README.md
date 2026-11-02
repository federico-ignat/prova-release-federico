# ISO 27001 Release PDF Generator

### Descrizione
Questo progetto genera automaticamente un scheda di rilascio in formato PDF quando viene pubblicata una Release GitHub.

L'obbiettivo è supportare il processo di conformità ISO 27001 automatizzando la raccolta delle informazioni di rilascio e la generazione della documentazione associata.

---

## Funzionamento

Quando viene creata una nuova Release GitHub:

1. Viene eseguita automaticamente una GitHub Action.
2. La Action recupera le informazioni della Release.
3. Viene generato un PDF tramite ReportLab.
4. Il PDF viene allegato automaticamente alla release.

---

## Informazioni recuperate automaticamente

- Repository
- Versione (Tag)
- Nome Release
- Data Release

---

## Sezioni generate nel PDF

### Informazioni Progetto

- Titolo Progetto
- Sviluppatore Assegnato
- Data Inizio Sviluppo
- Data Fine

### Analisi delle Specifiche

- Data di Apertura
- Data di Completamento
- Note

### Sviluppo 

- Branch
- Data di Apertura
- Data di Chiusura

### Test 

- Bug Riscontrati
- Esito Test

### Validazione

- Approvazione del Rilascio
- Note

### Rilascio in produzione

- Responsabile del Merge
- Data del Rilascio

### Documento di Applicabilità dei Controlli

Controlli del Secure Coding:

- 5.1 Controllo del codice sorgente
- 5.2 Gestione del repository
- 5.3 Revisione del codice
- 5.4 Gestione delle vulnerabilità
- ...
- 5.16 Output Validation

  ...

### Tecnologie Utilizzate

-GitHub Actions
-Python 3.10
-ReportLab
-GitHub Release

---

## Esempio workflow

Release GitHub
|
|
V

GitHub Action 
|
|
V

Generazione PDF 
|
|
V
Allegato automatico alla Release
|
|
V

---

## Possibili Evoluzioni Future

-Recupero automatico delle informazioni dalla descrizione della Release
-Inserimento del logo aziendale
-Generazione automatica delle checklist di sicurezza
-Integrazione con controlli ISO 27001 aggiuntivi
  
