# Generazione documentazione PDF per i rilasci

![Python 3.10](https://img.shields.io/badge/Python-3.10-blue)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-green)
![Documentazione](https://img.shields.io/badge/Documentazione-PDF-orange)

Questo documento contiene workflow GitHub Actions per generare documentazione PDF a supporto del processo di rilascio software e della raccolta dei controlli di sicurezza.

I documenti sono strumenti di supporto alla documentazione: da soli non garantiscono la conformità a ISO 27001.

## Documenti generati

### Scheda di rilascio

Il workflow **"Genera PDF Release Notes per ISO 27001"** genera una scheda PDF che raccoglie le informazioni principali del rilascio, tra cui:

- informazioni sul progetto e sul rilascio;
- analisi delle specifiche;
- attività di sviluppo;
- test autonomi dello sviluppatore;
- verifica con ICT Manager;
- validazione e rilascio in produzione;
- manutenzioni, aggiornamenti e azioni correttive.

**Generazione automatica:** quando una release GitHub viene pubblicata, la scheda PDF viene creata e allegata alla release. Una copia viene inoltre caricata tra gli artifact dell'esecuzione.

**Generazione manuale:** dalla scheda **Actions**, selezionare il workflow e avviare **Run workflow**. È possibile indicare il tag, il nome e il testo della release. Il PDF generato sarà disponibile tra gli artifact dell'esecuzione.

### Modulo di verifica dei controlli

Il workflow **"Genera modulo PDF compilabile dei controlli"** crea un modulo PDF compilabile con i controlli numerati da 5.1 a 5.16. I campi di implementazione e descrizione possono essere compilati o modificati direttamente nel PDF.

**Generazione automatica:** il modulo viene prodotto anche come parte del workflow di rilascio, insieme alla scheda di rilascio.

**Generazione manuale:** aprire **Actions**, selezionare il workflow e avviare **Run workflow**. Il file sarà disponibile come artifact con nome **"modulo-verifica-controlli"**.

## Sezioni della scheda di rilascio

La scheda include:

- Informazioni sul progetto e sul rilascio
- Analisi delle specifiche
- Attività di sviluppo
- Test autonomi dello sviluppatore
- Verifica con ICT Manager
- Validazione e rilascio in produzione
- Manutenzioni, aggiornamenti e azioni correttive

Alcuni valori e testi della scheda sono preimpostati nel workflow; per modificarli occorre aggiornare il relativo file di workflow.

## Tecnologie

- GitHub Actions
- Python 3.10
- ReportLab
- GitHub Releases e Actions artifacts

## File principali

- `.github/workflows/release-pdf.yml` — generazione e pubblicazione della scheda di rilascio e del modulo dei controlli.
- `.github/workflows/modulo-verifica.yml` — generazione autonoma del modulo compilabile dei controlli.

## Recupero dei PDF

- **PDF della release:** aprire la release GitHub per trovare i file allegati; in alternativa, consultare gli artifact dell'esecuzione in **Actions**.
- **Modulo dei controlli:** consultare gli artifact dell'esecuzione del workflow **"Genera modulo PDF compilabile dei controlli"**.
- **PDF della release e modulo dei controlli generati dal workflow di rilascio:** controllare gli artifact dell'esecuzione del workflow **"Genera PDF Release Notes per ISO 27001"**.

Gli artifact sono associati alle rispettive esecuzioni GitHub Actions e sono soggetti alle impostazioni di conservazione configurate per il repository.

## Note operative

- I workflow sono pensati come supporto alla documentazione del processo di rilascio.
- I contenuti preimpostati nei PDF devono essere verificati e aggiornati prima dell'uso effettivo in un contesto operativo.
- La generazione automatica avviene in risposta a una release pubblicata o tramite esecuzione manuale del workflow.

## Integrazione con il processo di rilascio

I PDF generati sono strumenti di supporto alla documentazione del rilascio software e alla raccolta dei controlli di sicurezza. Possono essere usati come base per la verifica interna e la preparazione delle attività di validazione, ma non sostituiscono le procedure aziendali né garantiscono la conformità a standard come ISO 27001.
