# Tipografia — Caratteri Cubitali Design System

## Sistema a tre font

| Ruolo | Font | Quando |
|---|---|---|
| Headline (con o senza fondino) | **Martian Mono** Bold 700 | Titoli slide, dati grandi, numeri |
| Corpo testo | **Atkinson Hyperlegible** Regular 400 / Bold 700 | Corpo, CTA pill, handle |
| Label sezione | **Archivo** Semibold 600 | Solo pillola sezione, uppercase |

**Interlinea universale: 1.2** su tutti gli elementi.  
Unica eccezione: numero statistica, interlinea 1.0 per compattezza visiva.

---

## Scala tipografica (preview HTML → Canva)

| Elemento | px preview | pt Canva approx. | Font | Weight |
|---|---|---|---|---|
| Headline (con/senza fondino) | 26px | ~20pt | Martian Mono | Bold 700 |
| Corpo principale | 15px | ~11pt | Atkinson Hyperlegible | Regular 400 |
| Corpo secondario | 13px | ~10pt | Atkinson Hyperlegible | Regular 400 |
| Enfasi corpo | stesso | — | Atkinson Hyperlegible | Bold 700 |
| Label sezione | 11px | ~8pt | Archivo | Semibold 600 |
| Handle / fonte | 10px | ~7.5pt | Martian Mono | Regular 400 |
| Numero statistica | 58px | ~43pt | Martian Mono | Bold 700 |

> Il preview HTML è calibrato a ~35% della slide reale. Moltiplicatore Canva: ×2.85.

---

## Headline con fondino

Il fondino è la firma visiva di Caratteri Cubitali: testo Martian Mono su box colorato che si adatta a ogni singola riga.

**Implementazione CSS:**
```css
.headline span {
  padding: .08em .22em .12em .22em;
  box-decoration-break: clone;
  -webkit-box-decoration-break: clone;
}
```

### Combinazioni approvate

| Codice | Fondino | Testo | Contrasto | Uso |
|---|---|---|---|---|
| C1 | `#0D0D0D` Nero | `#F3F3F3` Bianco | 21:1 AAA | Primaria, massima leggibilità |
| C2 | `#FED74E` Giallo | `#0D0D0D` Nero | 14.7:1 AAA | Accento energico |
| C3 | `#434CE0` Blu | `#F3F3F3` Bianco | 5.5:1 AA | Colore accent brand |
| C4 | `#F24E29` Rosso | `#0D0D0D` Nero | 4.6:1 AA | **Solo urgenza/errore** |
| C5 | `#04BF68` Verde | `#0D0D0D` Nero | 6.8:1 AA | **Solo successo/conferma** |

### Regole headline

1. **Sentence case** — mai uppercase per le headline.
2. **Fondino e sfondo slide diversi** — il colore del fondino non deve mai replicare il colore dello sfondo (no fondino giallo su slide gialla, no blu su blu).
3. **Una headline per slide** — al massimo un elemento headline dominante per slide.
4. **Fondino si adatta per riga** — `box-decoration-break: clone` garantisce che ogni riga abbia il proprio fondino indipendente.
5. **Coerenza nel carosello** — una sola combinazione colore fondino per tutto il carosello.

---

## Headline Martian Mono senza fondino

Martian Mono può essere usato come testo libero su sfondo, senza fondino, per:
- Titoli di cover su sfondi colorati (Nero, Giallo)
- Numeri grandi nelle slide statistiche
- Slide minimaliste ad alto impatto

---

## Label sezione — neo-brutalist flat shadow

La label sezione è una pillola in Archivo Semibold con ombra flat neo-brutalist.

```css
.label-sezione {
  font-family: 'Archivo', sans-serif;
  font-weight: 600;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  padding: 4px 10px;
  border: 1.5px solid [colore];
  border-radius: 999px;
  background: transparent;
  color: [colore];
  box-shadow: 0 2px 0 [colore];  /* X=0 sempre, opacità 100% sempre */
}
```

### Colori ammessi per la label

| Variante | Colore | Su quale sfondo |
|---|---|---|
| Default | `#0D0D0D` Nero | Sfondi bianchi, pastello, Giallo |
| White | `#F3F3F3` Bianco | Sfondi scuri (Nero, Blu scuro) |
| Giallo | `#FED74E` Giallo | Sfondi scuri (opzione accent) |
| Blu | `#434CE0` Blu | Sfondi bianchi, pastello chiaro |

> **Rosso e Verde esclusi** dalla label: il bordo sottile (1.5px) e la dimensione piccola (11px) non garantiscono contrasto sufficiente per questi colori.

### Regola ombra

- Spostamento **solo verticale**: `box-shadow: 0 2px 0 [colore]`
- Spostamento orizzontale sempre **zero**
- Opacità sempre **100%**, sia su sfondo chiaro che scuro

---

## Statistica

Numero e unità di misura (%, n, ecc.) usano **sempre lo stesso colore**. Il colore viene applicato tramite classe wrapper:

```css
.stat-wrap.c-giallo .stat-number,
.stat-wrap.c-giallo .stat-unit { color: #FED74E; }
```

Vietato usare colori diversi per numero e unità nella stessa slide.

---

## Handle e fonte

- Font: Martian Mono Regular
- Dimensione: 10px (~7.5pt Canva)
- Opacità: 50%
- Posizione: in basso a sinistra, sopra o accanto alla freccia di navigazione
