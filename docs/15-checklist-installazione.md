---
title: "Checklist di installazione"
date: "2026-10-28"
version: "1.0"
categoria: software Hyperetail
---

# Checklist di installazione

**TARGET:** tecnico installatore · **DURATA STIMATA:** 5 minuti di consultazione

## Obiettivo

Riassumere in ordine operativo tutto ciò che serve per portare a termine una
prima installazione di Hyperetail. Per ogni punto trovi il rimando alla guida
di dettaglio.

## Le tre aree di configurazione principali

Dopo l'installazione e le configurazioni generali, la configurazione si
concentra su tre ambiti:

1. **Reparti**;
2. **Anagrafica articoli** semplificata;
3. **Parametri di barriera** (gruppo POS) e **operatori** per la schermata di
   vendita.

## Checklist operativa

### Installazione

- [ ] Scaricato **HyperSide** da www.hyperetail.it → [Download di HyperSide](02-download-hyperside.md)
- [ ] HyperSide aggiornato e aperto (schede Licenza, Aggiornamenti, Setup, Store)
- [ ] **Hyperetail** installato dalla scheda Setup nella cartella `C:\Hyperetail` → [Installazione](03-installazione-hyperetail.md)
- [ ] Licenza attiva: abbinata, chiavetta di assistenza oppure **demo a tempo** richiesta → [Licenza](04-licenza-e-attivazione.md)

### Primo avvio

- [ ] Login con **99999** (amministratore) e **12345** (operatore base) verificati → [Operatori](05-operatori-disegnatore-pagine.md)
- [ ] Operatori configurati con pagina d'ingresso e limitazioni
- [ ] Pagine POS importate o personalizzate e associate agli operatori

### Archivi di base

- [ ] **Reparti** creati con IVA corretta; **sconti e promozioni disattivati** sui reparti esclusi (es. tabacchi) → [Reparti](06-reparti.md)
- [ ] **Tipo spesa** impostato per i reparti con spese sanitarie
- [ ] **Articoli** creati con reparto, prezzo, EAN (o AutoEAN) e immagine → [Articoli](07-anagrafica-articoli.md)
- [ ] Informazioni **avanzate** compilate solo se servono (brand, varianti, costi, composizione) → [Articoli avanzati](08-articoli-avanzati.md)
- [ ] **Listini** aggiuntivi creati, se necessari; **maschere EAN** verificate per prodotti a peso e bilance → [Listini e maschere EAN](09-listini-e-maschere-ean.md)
- [ ] **Dati azienda** compilati; parametri generali toccati solo se serve → [Azienda e parametri](10-azienda-parametri-generali.md)

### Cassa

- [ ] **Gruppo POS** configurato: magazzino, gruppo pagine, listino di partenza, SubTotale obbligatorio, operatore automatico → [Parametri di barriera](11-parametri-barriera-gruppo-pos.md)
- [ ] **Casse aggiuntive** create, se presenti più postazioni
- [ ] **Forme di pagamento** verificate (Totale Cassetto, Senza resto) → [Pagamenti e movimenti](12-pagamenti-movimenti-causali.md)
- [ ] Numerazioni, codici movimento e causali di scarico controllati solo se il cliente lo richiede

### Schermata di vendita e dispositivi

- [ ] **Aree dinamiche** di reparti e PLU personalizzate → [Schermata di vendita](13-schermata-di-vendita.md)
- [ ] Tasti per il cliente (**Listino Prodotti**, **Nuovo Prodotto**) attivati, se richiesti
- [ ] **Registratore telematico** collegato in `POS.ini` (seriale o LAN); matricola rilevata → [File INI e dispositivi](14-file-ini-dispositivi.md)
- [ ] **Cassetto elettronico** configurato in `POS.ini` e tasto abilitato in vendita
- [ ] **POS bancario** configurato in `PinPad.ini` e tasto **Scambio importo PinPad** creato
- [ ] Scontrino di prova battuto

## Codici e riferimenti rapidi

| Elemento | Valore |
|---|---|
| Codice operatore base | `12345` |
| Codice amministratore | `99999` |
| Cartella di installazione | `C:\Hyperetail` |
| Disegnatore | doppio clic con il tasto destro, oppure `CTRL+SHIFT+D` |
| Uscita dal Disegnatore | tasto destro → **Salva ed esci dal disegnatore** |
| Logout operatore | tasto funzione **Chiave** |
| Protocollo registratore | Custom (`CashType=CUSTOM`) |
| Protocollo POS | 17, porta terminale `65000` |
| Porta database | `3050` (aprire con esclusioni firewall se il database è su un altro PC) |
| Wiki | www.hyperetail.it/wiki |

## Errori più frequenti

| Sintomo | Dove intervenire |
|---|---|
| Download interrotto con errore **12030** | Ripetere il setup di HyperSide → [Installazione](03-installazione-hyperetail.md) |
| Sconto applicato anche ai tabacchi | Reparto: disattivare Accetta Sconti / Accetta Promozioni → [Reparti](06-reparti.md) |
| Operatore non vede la pagina giusta | Operatori → Ingresso Pagina; uscire e rientrare → [Operatori](05-operatori-disegnatore-pagine.md) |
| In un bar serve sempre il SubTotale | Gruppo POS → disattivare SubTotale Obbligatorio → [Parametri di barriera](11-parametri-barriera-gruppo-pos.md) |
| CashMedic non risponde | Non scrivere l'IP: solo `CashMachineType=CashMedic` → [File INI](14-file-ini-dispositivi.md) |
