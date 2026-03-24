# 📋 Mod. FN – Foglio Notizie · Assunzione in Servizio
![Version](https://img.shields.io/badge/Versione-4.0-orange)
![License](https://img.shields.io/badge/Licenza-CC%20BY--NC--SA%204.0-blue)
![HTML](https://img.shields.io/badge/HTML-Single%20File-red?logo=html5)
![GitHub stars](https://img.shields.io/github/stars/sebastianobasile/presa-servizio)
![GitHub forks](https://img.shields.io/github/forks/sebastianobasile/presa-servizio)

**Generatore di moduli per la presa di servizio del personale scolastico**

> **Utilizzo e dimostrativo:** [superscuola.com/assunzione](https://superscuola.com/assunzione)

> Autore: **Sebastiano BASILE** Avola (SR) · [superscuola.com](https://superscuola.com)  
> Licenza: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.it)  
> Progetto: [GitHub – sebastianobasile](https://github.com/sebastianobasile?tab=repositories)

Se ti piace questo strumento [![Contributo volontario](https://img.shields.io/badge/Offrimi_un_caffè_☕-PayPal-blue)](https://paypal.me/superscuola)
---

## 📌 Descrizione

**Mod. FN** è uno strumento web completamente lato client (nessun server, nessuna installazione) che genera in un unico file tre documenti ufficiali A4 necessari alla presa di servizio del personale scolastico, sia al 1° settembre che in corso d'anno:

| Pagina | Documento |
|--------|-----------|
| **Pagina 1** | Assunzione in Servizio e Foglio Notizie *(Dichiarazione Sostitutiva di Certificazione – art. 46 DPR 445/2000)* |
| **Pagina 2** | Dichiarazione Iscrizione Fondo Espero e Incompatibilità |
| **Pagina 3** | Dichiarazione di Autocertificazione *(art. 47 D.P.R. 445/2000)* |

L'anteprima si aggiorna in tempo reale ad ogni modifica. La stampa / esportazione PDF avviene direttamente dal browser.

---

## 🚀 Come si usa

1. Aprire `index.html` in qualsiasi browser moderno (Chrome, Firefox, Edge, Safari)
2. Compilare l'intestazione istituto nel pannello **🏫 INTESTAZIONE ISTITUTO** *(si configura una volta sola)*
3. Navigare tra le tre tab della sidebar (**1·Notizie**, **2·Espero**, **3·Dichiar.**) e compilare i campi
4. Verificare l'anteprima in tempo reale nel pannello destro
5. Cliccare **STAMPA / SALVA PDF** per stampare o salvare i tre documenti

> Non richiede connessione internet dopo il primo caricamento della pagina.

---

## 🖥️ Struttura dell'interfaccia

L'interfaccia è divisa in due colonne:

- **Barra laterale sinistra** – pannelli di input organizzati in sezioni e tab
- **Anteprima destra** – tre fogli A4 in sequenza, aggiornati in tempo reale

---

## 🏫 Intestazione Istituto *(pannello collassabile)*

Configurazione comune a tutti e tre i documenti. Si salva automaticamente in `localStorage`.

| Campo | Descrizione |
|-------|-------------|
| **Titolo istituto** (riga 1) | Nome in grassetto nell'intestazione |
| **Sottotitolo / Indirizzo** (riga 2) | Tipologia scolastica, indirizzo, telefono |
| **Anno Scolastico (A.S.)** | Es. `2025/2026` |
| **Luogo firma** | Comune da cui vengono emessi i documenti |
| **Data firma** | Applicata a tutte le sezioni firma dei tre documenti |

---

## 📄 Tab 1 · Notizie — Assunzione in Servizio

### Dati Anagrafici

| Campo | Note |
|-------|------|
| Cognome / Nome | — |
| **Genere del dichiarante** | `Maschile` / `Femminile` – gestisce la concordanza automatica (*il sottoscritto / la sottoscritta*, *nato / nata*) in tutti e tre i documenti |
| Data di Nascita | Formattata automaticamente in GG/MM/AAAA |
| Luogo Nascita + Prov. | — |
| Indirizzo residenza + Città + Prov. | Composti automaticamente nel testo |
| Tel. / Email | Campo contatti libero |
| Codice Fiscale | Reso in maiuscolo automaticamente |
| N. Partita (opzionale) | — |

### Allegati *(riquadro Pagina 1)*

Caselle di spunta che attivano il segno ✓ e il grassetto nel riquadro allegati del documento:

- Cedolino dello stipendio
- Documento di riconoscimento valido
- Codice Fiscale
- Documenti già in possesso dell'Istituto

### Incarico

| Campo | Valori / Note |
|-------|---------------|
| **Tipo di assunzione** | `Supplenza Lunga` · `Passaggio di Ruolo` · `Trasferimento` · `Assegnazione Provvisoria` · `Utilizzazione` · `Altro (personalizza...)` |
| **Qualifica** | `Docente a Tempo Determinato` · `Docente a Tempo Indeterminato` · `Personale ATA` · `Altro (personalizza...)` |
| **Ordine di Scuola** | `Secondaria di 1° Grado` · `Primaria` · `Infanzia` · `Secondaria di 2° Grado` |
| Data assunzione | — |
| Ore settimanali | — |
| Fino al | Data fine incarico |
| Classe di concorso / Disciplina | — |
| Completa in altra scuola per ore | Ore di completamento in sede diversa |
| Sede ore completamento | — |
| Titolo di studio principale | — |
| Data immissione in ruolo | — |
| Sede di titolarità | — |
| Ultima sede di servizio | — |

> I campi *Tipo di assunzione* e *Qualifica* supportano l'opzione **Altro**: selezionandola compare un campo testo libero per una dicitura personalizzata.

### Stato Civile e Famiglia

| Campo | Valori |
|-------|--------|
| **Stato Civile** | `Celibe` · `Nubile` · `Coniugato/a` · `Divorziato/a` · `Vedovo/a` |
| Comune di cittadinanza | — |

### Nucleo Familiare

Tabella dinamica dei componenti conviventi (escluso il dichiarante). Per ogni componente:

- Cognome e Nome
- Luogo e Data di nascita
- Rapporto di parentela

Il pulsante **+ Aggiungi componente** inserisce una nuova riga; ogni riga ha il pulsante ✕ per la rimozione. La tabella nel documento si aggiorna in tempo reale e mostra sempre almeno 2 righe vuote.

---

## 📄 Tab 2 · Espero — Fondo Espero e Incompatibilità

### Fondo Espero

Selezione della posizione previdenziale complementare. Nel documento viene spuntata (✓) e resa in grassetto la voce corrispondente:

| Valore | Dicitura nel documento |
|--------|------------------------|
| `Non iscritto` | di NON essere iscritto al Fondo Scuola Espero |
| `Già iscritto` | di essere già iscritto al Fondo Scuola Espero |
| `Ha optato per il riscatto` | di aver optato per il riscatto della posizione maturata |

### Incompatibilità

| Valore | Dicitura nel documento |
|--------|------------------------|
| `Nessuna incompatibilità` | di non trovarsi in nessuna delle situazioni di incompatibilità *(art. 508 D.L.vo 297/1994 e art. 53 D.L.vo 165/2001)* |
| `Incompatibilità - opta per nuovo rapporto` | di trovarsi in una delle suddette situazioni e di optare per il nuovo rapporto di lavoro |

La pagina 2 contiene anche la sezione **AUTORIZZA** per il trattamento dei dati personali ai sensi del D.Lgs. 196/2003, con relativo blocco firma.

---

## 📄 Tab 3 · Dichiar. — Dichiarazione di Autocertificazione

Editor di testo libero per la dichiarazione dei titoli di studio e delle posizioni professionali (ai sensi dell'art. 47 D.P.R. 445/2000).

| Funzione | Come si usa |
|----------|-------------|
| **Testo libero** | Campo `contenteditable` con a-capo semplice (Invio → `<br>`) |
| **Grassetto** | Selezionare il testo e premere il pulsante **G** oppure `Ctrl+B` |
| **Incolla pulito** | Il testo incollato viene privato di qualsiasi formattazione HTML esterna |

Il testo viene visualizzato nella Pagina 3 all'interno di un riquadro con bordo.

---

## 💾 Salvataggio e Persistenza dei Dati

Tutti i dati vengono salvati automaticamente nel `localStorage` del browser ad ogni modifica. Un indicatore **✓ Salvato in memoria browser** appare brevemente ad ogni aggiornamento.

Al riavvio della pagina i dati vengono ripristinati automaticamente.

### Esporta / Importa JSON

Per conservare i dati al di fuori del browser o spostarli su un altro dispositivo:

| Pulsante | Funzione |
|----------|----------|
| **ESPORTA DATI (.json)** | Scarica tutti i campi in un file `foglio_notizie_cognome_nome.json` |
| **IMPORTA DATI (.json)** | Carica un file `.json` precedentemente esportato e ripopola tutti i campi |

---

## 🖨️ Stampa / Salvataggio PDF

Il pulsante **STAMPA / SALVA PDF** richiama il dialogo di stampa nativo del browser. Per salvare un PDF:

- **Chrome / Edge**: selezionare *Salva come PDF* come destinazione
- **Firefox**: selezionare *Stampa su file PDF*
- **Safari**: File → Stampa → Salva come PDF

I tre fogli A4 vengono stampati in sequenza su pagine separate (`page-break-after: always`). La sidebar è nascosta automaticamente in fase di stampa.

---

## 🔄 Reset

Il pulsante **Pulisci tutti i campi** cancella tutti i dati inseriti e il salvataggio in `localStorage`, ripristinando i valori di default della configurazione (nome scuola, anno scolastico, luogo firma).

---

## ⚙️ Configurazione predefinita

I valori di default sono definiti nel blocco `CONFIG` in fondo al file HTML e possono essere modificati direttamente nel sorgente per adattare lo strumento al proprio istituto:

```javascript
const CONFIG = {
    nome_scuola:        "3° ISTITUTO COMPRENSIVO CAPUANA-DE AMICIS DI AVOLA",
    sottotitolo_scuola: "Scuola dell'Infanzia, Primaria e Secondaria di primo grado ...",
    anno_scolastico:    "2025/2026",
    luogo_default:      "Avola",
    crediti:            "Mod. «Assunzione in servizio...» • credit: S. Basile • ..."
};
```

---

## 🔧 Tecnologie utilizzate

| Libreria | Versione | Uso |
|----------|----------|-----|
| [Bootstrap](https://getbootstrap.com/) | 5.3.0 | Layout e componenti UI della sidebar |
| JavaScript vanilla | ES6+ | Sync in tempo reale, localStorage, export/import JSON |
| CSS `@media print` | — | Nasconde la sidebar e formatta le pagine A4 per la stampa |

Nessuna dipendenza lato server. Il file `index.html` è completamente autonomo e autocontenuto.

---

## 📝 Riferimenti normativi

- **Dichiarazione Sostitutiva di Certificazione** – art. 46 DPR 445 del 2.12.2000
- **Dichiarazione di Autocertificazione** – art. 47 D.P.R. 28 dicembre 2000, n. 445 e s.m.i.
- **Fondo Espero** – previdenza complementare del comparto scuola, accordo ARAN del 14 marzo 2001
- **Incompatibilità** – art. 508 D.L.vo n. 297/1994 e art. 53 D.L.vo n. 165/2001
- **Privacy** – autorizzazione al trattamento dati ai sensi del D.Lgs. n. 196 del 30/06/2003

---

## ⚠️ Disclaimer

Lo strumento è fornito a titolo gratuito per uso personale e non commerciale. L'autore non si assume responsabilità per eventuali errori nei documenti generati. Si raccomanda di verificare sempre la correttezza dei dati prima della consegna ufficiale.

---

*Mod. FN · Autore: Seb.no BASILE · [superscuola.com](https://superscuola.com) · Licenza CC BY-NC-SA 4.0*
