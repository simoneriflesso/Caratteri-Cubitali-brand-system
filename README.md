# Caratteri Cubitali — Brand System

Design system ufficiale di **Caratteri Cubitali APS**, associazione per l'accessibilità digitale e i diritti delle persone con disabilità.

---

## Struttura repository

```
/
├── README.md
├── design-system/
│   ├── colors.md          # Palette, scale, token CSS, regole d'uso
│   └── typography.md      # Font, scala, headline fondino, label, statistica
├── assets/
│   ├── cc-color-system.html     # Esplora palette interattiva con WCAG
│   └── cc-typography.html       # Simulazione slide caroselli
└── (in arrivo)
    ├── design-system/brand.md   # Logo, versioni, utilizzi corretti/scorretti
    ├── design-system/tone.md    # Tono di voce e comunicazione
    └── design-system/ai-prompts.md  # Prompt AI per generazione immagini
```

---

## Brand in sintesi

### Identità
Caratteri Cubitali è un'associazione giovane e ribelle, nata nel 2022. Il nome viene da un sogno punk: una scritta gigante a pennello con vernice rossa su un muro. L'approccio al design riflette questa identità: provocatorio, accessibile, irriverente.

### Colori ufficiali
| | Hex | Ruolo |
|---|---|---|
| 🔵 Blu Vibrante | `#434CE0` | Accent primario |
| 🟡 Giallo Vivo | `#FED74E` | Secondario |
| ⬛ Nero | `#0D0D0D` | Neutro primario |
| ⬜ Bianco | `#F3F3F3` | Neutro secondario |
| 🔴 Rosso | `#F24E29` | Uso limitato |
| 🟢 Verde | `#04BF68` | Uso limitato |

### Font
- **Martian Mono** — headline (con e senza fondino), dati, handle
- **Atkinson Hyperlegible** — corpo testo, CTA, tutto il testo di lettura
- **Archivo Semibold** — label sezione (pillola neo-brutalist)

### Logo
Tre versioni disponibili in `/assets/`:
- `CC_logo.svg` — solo simbolo
- `CC_logotipo.svg` — solo wordmark
- `CC_logo_completo.svg` — simbolo + wordmark (**versione preferita**)

Applicazione preferita: logo in **nero su sfondo bianco** o su sfondi colorati con bassa luminosità.

---

## File interattivi

### `cc-color-system.html`
Esplora la palette estesa con scale 50→900 per ogni colore. Include:
- Scale colori con stella sul colore brand ufficiale
- Combinazioni sfondo approvate (con regola: mai colore su colore)
- Matrice contrasti WCAG verificata
- Design tokens CSS pronti da copiare

### `cc-typography.html`
Simulazione slide caroselli in formato 4:5. Include:
- Specifiche tipografiche complete
- Tutte le combinazioni headline/fondino con preview reale
- 4 tipi di template slide (Cover, Testo, Statistica, CTA)
- Scala tipografica con tutti gli elementi

---

## Principi di accessibilità

- Tutti i testi rispettano WCAG 2.1 AA (contrasto ≥ 4.5:1)
- La palette è verificata per daltonismo (nessun conflitto tra i 4 colori primari)
- Font Atkinson Hyperlegible progettato specificamente per bassa visione
- Interlinea 1.2 universale per leggibilità
