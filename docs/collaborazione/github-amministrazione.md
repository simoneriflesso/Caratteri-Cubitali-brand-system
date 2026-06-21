# Gestione dell'organizzazione su GitHub — Caratteri Cubitali APS ETS

Questa guida è per chi amministra l'organizzazione GitHub di Caratteri Cubitali APS ETS. Spiega come gestire le persone, i ruoli e i permessi.

---

## 🏠 Cos'è l'organizzazione GitHub

L'organizzazione è lo spazio su GitHub intestato a Caratteri Cubitali APS ETS. Tutti i *repository* (archivi di progetto) creati al suo interno appartengono all'associazione, non a una persona singola. Questo vale anche se chi li ha creati lascia l'organizzazione.

---

## 🎭 I ruoli

Ogni persona ha un ruolo. Il ruolo determina cosa può fare.

| Ruolo | Chi è | Cosa può fare |
|---|---|---|
| **Owner** (proprietario) | Chi gestisce l'organizzazione | Tutto: aggiunge e rimuove persone, cambia le impostazioni, gestisce gli archivi di progetto |
| **Maintainer** (responsabile) | Chi coordina il lavoro tecnico su un archivio di progetto | Approva le modifiche, gestisce i *branch*, modifica le impostazioni dell'archivio |
| **Member** (membro) | Chi collabora attivamente | Propone modifiche, apre discussioni, lavora sui propri *branch* |

### Regola pratica

> Assegna sempre il ruolo minimo necessario. Parti da **Member** e promuovi solo se serve.

Tieni il numero di *Owner* al minimo: uno o due al massimo. Più *Owner* ci sono, più è difficile sapere chi ha fatto cosa.

---

## 📬 Come invitare una nuova persona

1. Vai su `github.com/caratteri-cubitali`
2. Clicca su **People** → **Invite member**
3. Inserisci il nome utente GitHub della persona
4. Assegnale il ruolo **Member**
5. Condividi con lei la guida per i collaboratori

Promuovi a **Maintainer** solo chi coordina il lavoro su un archivio di progetto in modo continuativo.

---

## 👋 Come rimuovere una persona

1. Vai su **People**
2. Clicca sul nome della persona
3. Seleziona **Remove from organization**

Gli archivi di progetto rimangono nell'organizzazione. Le modifiche fatte dalla persona rimangono registrate nella cronologia.

---

## 🔒 Come proteggere gli archivi di progetto

GitHub permette di impostare protezioni sui *branch* (versioni di lavoro), così nessuno può fare modifiche accidentali alla versione ufficiale.

### Impostazioni consigliate per la versione ufficiale `main`

1. Vai nell'archivio di progetto → **Settings** → **Branches**
2. Clicca su **Add branch protection rule**
3. Scrivi `main` nel campo del nome
4. Attiva queste opzioni:
   - ✅ **Require a pull request before merging** — nessuno può modificare `main` direttamente
   - ✅ **Require approvals** — almeno 1 approvazione prima di unire
   - ✅ **Do not allow bypassing the above settings** — vale anche per gli *Owner*

### Impostazioni consigliate per il cantiere `develop`

- ✅ **Require a pull request before merging**
- Non serve richiedere approvazioni esplicite

---

## 🤝 Cosa fare quando arriva una nuova persona

1. Invitala come **Member** (vedi sopra)
2. Condividi con lei la guida per i collaboratori
3. Falle creare un *branch* di prova per familiarizzare con il flusso di lavoro

---

*Documento interno — Caratteri Cubitali APS ETS*
*Aggiornato: giugno 2026*
