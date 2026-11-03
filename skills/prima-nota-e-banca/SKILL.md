---
name: prima-nota-e-banca
description: Prima nota cassa e banca e riconciliazione bancaria. Legge i movimenti esportati dall'home banking (CSV, Excel, CBI, CAMT.053), abbina ogni movimento a fattura, F24, stipendi, commissioni o giroconto, tiene l'elenco dei movimenti non abbinati e prepara a fine mese il prospetto di riconciliazione tra saldo banca e saldo contabile. Da usare quando arrivano movimenti bancari, per la prima nota, per capire un movimento o per la quadratura di fine mese.
license: Proprietary
metadata:
  hermes:
    tags: [Amministrazione, Banca, Prima nota, Riconciliazione]
    related_skills: [contabilita-base, ciclo-attivo-passivo, pagamenti-e-incassi, chiusura-mensile]
---

# Prima nota e banca

## Dove scrivi

- `amministrazione/banca/<banca>-<anno>-<mese>.csv`: i movimenti come arrivano.
- `amministrazione/prima-nota-<anno>.xlsx` (o `.csv`): data, conto (cassa,
  banca), descrizione, entrata, uscita, documento abbinato, categoria, note.
- `amministrazione/da-abbinare.md`: i movimenti che non sai spiegare.

## Leggere i movimenti

1. Chiedi alla persona l'export del periodo (o leggilo dalla cartella
   concordata). Preferisci CSV o CAMT.053 al PDF.
2. Controlla che il saldo iniziale sia il saldo finale del periodo prima e che
   saldo iniziale più movimenti dia il saldo finale dell'estratto. Se non
   quadra, fermati e dillo: mancano movimenti.
3. Non modificare mai il file originale: lavora su una copia.

## Abbinare

Per ogni movimento cerca, in quest'ordine:

1. **Incassi:** fattura emessa per importo, cliente (nome nella causale o IBAN
   ordinante) e numero di fattura nella causale. Incassi parziali o cumulativi:
   abbina a più fatture e annota il residuo.
2. **Pagamenti a fornitori:** fattura ricevuta, scadenza, Ri.Ba. passiva.
3. **F24:** data e importo della delega; abbina alla quietanza.
4. **Stipendi e contributi:** distinta del consulente del lavoro.
5. **Commissioni, interessi, bolli, canoni:** voce banca.
6. **Giroconti** tra conti dell'azienda: due movimenti opposti, stessa data.
7. **Carte e POS:** accrediti del POS al netto delle commissioni, addebiti
   della carta aziendale con il suo estratto.

Un abbinamento incerto lo segni come "proposto" con il motivo. Quello che non
riesci a spiegare va in `da-abbinare.md` con data, importo, causale, e la
domanda precisa da fare alla persona ("Bonifico di 1.200,00 € del 4/11 da
Rossi Srl: a quale fattura si riferisce?").

Non registri tu in contabilità e non decidi conti o aliquote: prepari la prima
nota e i dati per il commercialista, come dice `contabilita-base`.

## Riconciliazione di fine mese

Per ogni conto prepara un prospetto:

| Voce | Importo |
| --- | --- |
| Saldo da estratto conto al giorno X | |
| meno pagamenti registrati non ancora addebitati | |
| più incassi registrati non ancora accreditati | |
| più o meno altri elementi da spiegare (con descrizione) | |
| = Saldo contabile atteso | |
| Saldo contabile dal gestionale o dalla prima nota | |
| Differenza | deve essere zero |

Una differenza diversa da zero non si "aggiusta": si spiega movimento per
movimento o si segnala. Elementi in sospeso da più di 30 giorni vanno
segnalati alla persona.

## Cosa riferisci

Nel punto settimanale: saldo di ogni conto, incassi e pagamenti della
settimana, quanti movimenti restano da abbinare e le domande aperte. A fine
mese: il prospetto di riconciliazione per ogni conto.
