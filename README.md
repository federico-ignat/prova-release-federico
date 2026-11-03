# ISO 27001 Release PDF Generator

![Python](https://Img.shields.io/badge/Phython-3.10-blue) 
![GitHub Actions](https://img.shields.io/badge/GitHub-Action-green) 
![ISO27001](https://img.shields.io/badge/ISO-27001-orange) 

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

-GitHub Actions <br>
-Python 3.10 <br>
-ReportLab <br>
-GitHub Release <br>

---

## Esempio workflow

Release GitHub


GitHub Action 


Generazione PDF 


Allegato automatico alla Release


---

## Possibili Evoluzioni Future

-Recupero automatico delle informazioni dalla descrizione della Release <br>
-Inserimento del logo aziendale <br>
-Generazione automatica delle checklist di sicurezza <br>
-Integrazione con controlli ISO 27001 aggiuntivi <br>
  
