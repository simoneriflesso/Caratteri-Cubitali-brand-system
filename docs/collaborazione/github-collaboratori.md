# Come collaborare su GitHub — Caratteri Cubitali APS ETS

Questa guida è per chi collabora ai progetti di Caratteri Cubitali APS ETS su GitHub. Spiega come proporre modifiche senza fare danni accidentali.

---

## 🌐 Cos'è GitHub e come lo usiamo

GitHub è un servizio online dove conserviamo i file dei nostri progetti. Ogni modifica viene registrata: si può sempre vedere chi ha cambiato cosa e quando, e si può tornare indietro se qualcosa va storto.

Non è necessario usare la riga di comando: GitHub ha un'interfaccia web che permette di fare quasi tutto dal browser.

---

## 📦 Gli archivi di progetto

Su GitHub, i file di ogni progetto sono conservati in un *repository* (archivio di progetto). È come una cartella che contiene tutti i file e la loro cronologia completa delle modifiche.

---

## 🌿 Le versioni di lavoro

Un *branch* (letteralmente "ramo", in italiano versione di lavoro) è una copia separata dei file su cui lavorare. Serve per fare modifiche senza toccare la versione ufficiale.

L'immagine del ramo è quella giusta: dal tronco principale si diramano rami separati, ognuno con il proprio percorso. Quando il lavoro è pronto, il ramo viene ricongiunti al tronco.

### Le versioni di lavoro principali

Ogni archivio di progetto ha due versioni di lavoro fisse:

**`main` — la versione ufficiale**
- Contiene solo cose pronte e approvate
- Non si modifica mai direttamente
- Si aggiorna solo dopo una revisione

**`develop` — il cantiere**
- È il punto di partenza per le nuove modifiche
- Raccoglie il lavoro in corso prima che finisca in `main`

---

## 🛠️ Come si lavora nella pratica

Quando vuoi fare una modifica — aggiungere un file, correggere un errore, aggiornare la documentazione:

1. Parti dalla versione di lavoro `develop`
2. Crea una versione di lavoro personale con un nome descrittivo, per esempio:
   - `fix/correzione-nome-file`
   - `feature/nuovo-componente`
   - `docs/aggiornamento-istruzioni`
3. Fai le modifiche sulla tua versione di lavoro
4. Quando hai finito, apri una *pull request* (richiesta di revisione)

---

## 🔍 Le richieste di revisione

Una *pull request* (richiesta di revisione) è il modo con cui proponi le tue modifiche per inserirle nella versione di lavoro condivisa. Stai chiedendo che il tuo lavoro venga revisionato e poi unito al resto.

Funziona così:

1. Hai finito di lavorare sulla tua versione di lavoro
2. Apri una *pull request* su GitHub
3. Scrivi un titolo chiaro e una breve descrizione di cosa hai cambiato e perché
4. Un'altra persona controlla le modifiche e le approva
5. Una volta approvata, le modifiche vengono unite a `develop`

### Cosa scrivere nella descrizione

Non serve scrivere molto. Bastano poche righe:
- Cosa hai cambiato
- Perché l'hai cambiato
- Se c'è qualcosa che chi revisiona dovrebbe sapere

---

## 🗺️ Schema del flusso di lavoro

```
versione personale  →  develop  →  main
(lavoro in corso)      (cantiere)  (versione ufficiale)
```

Ogni freccia rappresenta una *pull request* con almeno un'approvazione.

---

## 📋 Regole essenziali

- Non modificare mai `main` o `develop` direttamente
- Ogni modifica parte da una versione di lavoro personale
- Ogni *pull request* deve avere un titolo descrittivo
- Prima di aprire una *pull request*, rileggi le tue modifiche

---

## 🔙 Se qualcosa va storto

GitHub registra ogni modifica. Se fai un errore, non è un problema: si può sempre tornare indietro. Segnala la situazione a chi amministra l'organizzazione.

---

*Documento interno — Caratteri Cubitali APS ETS*
*Aggiornato: giugno 2026*
