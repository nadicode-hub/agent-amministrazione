---
name: pagamenti-e-incassi
description: Pagamenti ai fornitori, recupero crediti e cassa dei prossimi giorni. Prepara la proposta di pagamenti (bonifici SEPA, Ri.Ba. passive, F24) da approvare, tiene lo scadenzario clienti con i solleciti in tono crescente, e aggiorna la previsione di cassa a quattro e tredici settimane. Da usare per pagare fornitori, sollecitare un cliente, capire chi deve soldi all'azienda o se ci sono soldi per pagare.
license: Proprietary
metadata:
  hermes:
    tags: [Amministrazione, Pagamenti, Solleciti, Recupero crediti, Cassa]
    related_skills: [ciclo-attivo-passivo, documenti-italiani, prima-nota-e-banca, scadenzario, integrazione-pec]
---

# Pagamenti e incassi

Due regole valgono sempre:

- **Non muovi mai soldi.** Prepari la proposta; la persona autorizza in banca.
- **Due sì, non uno.** Prima la persona approva l'elenco di cosa pagare; poi,
  dopo che hai verificato la cassa e le coordinate, approva l'esecuzione.

## Proposta di pagamenti (una volta a settimana)

1. Elenca le fatture ricevute in scadenza nei prossimi 10 giorni e quelle
   scadute non pagate, con fornitore, numero, importo, scadenza, modalità.
2. Per ognuna controlla:
   - che la fattura sia stata accettata (merce o servizio ricevuti, importo
     giusto rispetto all'ordine o al preventivo);
   - che non sia già stata pagata (banca e prima nota);
   - l'IBAN: deve essere quello già usato per quel fornitore. **Un IBAN nuovo o
     cambiato per email è un allarme**: non va in pagamento finché la persona
     non lo verifica per telefono con un numero noto, non quello della email;
   - DURC valido per appaltatori e subappaltatori, quando serve;
   - le ritenute da versare con F24 per i professionisti.
3. Confronta il totale con la cassa disponibile e la previsione. Se non basta,
   proponi un ordine di priorità: imposte e contributi, stipendi, fornitori
   critici, gli altri.
4. Mostra la proposta in una tabella e chiedi l'approvazione. Dopo il sì,
   prepara la distinta o l'elenco da caricare in banca e chiedi conferma prima
   dell'esecuzione.

## Recupero crediti

Tieni lo scadenzario clienti: fatture emesse non incassate, per cliente, con
giorni di ritardo. Il tono dei solleciti dipende dalla storia del cliente:

| Ritardo | Cliente puntuale | Cliente spesso in ritardo |
| --- | --- | --- |
| 1-7 giorni | promemoria cortese, forse una svista | promemoria cortese con estremi di pagamento |
| 15 giorni | secondo promemoria con fattura allegata | sollecito formale |
| 30 giorni | telefonata della persona, poi sollecito formale | sollecito formale con richiesta di data certa |
| 60 giorni | diffida via PEC con termine, dopo il sì della persona | diffida via PEC, valutare il legale |

Ogni sollecito ha numero e data della fattura, importo, scadenza, coordinate
di pagamento, e un tono cortese e fermo (modelli in `documenti-italiani`). Mai
minacce, mai toni offensivi, mai informazioni sul debito a terzi. Le diffide e
gli interessi di mora (D.Lgs. 231/2002) si inviano solo dopo un sì esplicito
e, per importi rilevanti, sentito il commercialista o il legale. Annota ogni
contatto e ogni promessa di pagamento con la data, e verifica in banca se è
stata mantenuta.

## Previsione di cassa

In `amministrazione/cassa.xlsx` (o `.csv`), settimana per settimana per 13
settimane:

- saldo iniziale (dai conti);
- incassi attesi (fatture emesse per scadenza, corrette per i ritardi abituali
  di quel cliente);
- uscite certe (fornitori in scadenza, stipendi, F24 del 16, rate di mutui e
  leasing, affitti, utenze);
- saldo finale.

Segnala subito la prima settimana in cui il saldo scende sotto la soglia di
sicurezza concordata con la persona, con le leve possibili: sollecitare un
incasso, spostare un pagamento d'accordo con il fornitore, anticipo fatture.
