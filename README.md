# Generazione documentazione PDF per i rilasci

![Python 3.10](https://img.shields.io/badge/Python-3.10-blue)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-green)
![Documentazione](https://img.shields.io/badge/Documentazione-PDF-orange)

Questo documento contiene workflow GitHub Actions per generare documentazione PDF a supporto del processo di rilascio software e della raccolta dei controlli di sicurezza. 

I documenti sono strumenti di supporto alla documentazione:  da soli non garantiscono la conformità a ISO 27001.

## Documenti generati

### Scheda di rilascio 
Il workflow "Genera PDF Release Notes per ISO 27001" crea una scheda PDF con informazioni e sezioni relative al rilascio, tra cui i progetti, le analisi, lo sviluppo, i test, le validazioni e il rilascio in produzione e azione correttive.

**Generazione automatica:** quando una release GitHub viene pubblicata, il PDF viene creato e caricato sulla release. Una copia viene anche caricata tra gli artifact dell'esecuzione.

**Generazione manuale:** Dalla scheda **Actions**, selezionare il workflow e avviare **Run Workflow**. E possibile indicare il tag, il nome e il testo della release. Il PDF generato sarà disponibile tra gli artifact dell'esecuzione.

### Modulo di verifica dei controlli

Il workflow "Genera modulo PDF compilabile dei controlli" crea un modulo PDF compilabile con i controlli numerati da 5.1 a 5.16. I campi di implementazione e descrizione possono essere compilati o modificati direttamente nel PDF.

Per generarlo, aprire **Actions**, selezionare il workflow e avviare **Run workflow**. Il file sarà disponibile come artifact con nome "modulo-verifica-controlli"

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

- `.github/workflows/release-pdf.yml` — generazione e pubblicazione della scheda di rilascio.
- `.github/workflows/modulo-verifica.yml` — generazione del modulo compilabile dei controlli.

## Recupero dei PDF 

- **PDF della release:** aprire la release GitHub per trovare il file allegato; in alternativa, consultare gli artifact dell'esecuzione in **Actions**.

- **Modulo dei controlli:** consultare gli artifact dell'esecuzione del workflow "Genera modulo PDF compilabile dei controlli."

Gli artifact sono associati alle rispettive esecuzioni GitHub Actions e sono soggetti alle impostazioni di conservazione configurate per il repository.

