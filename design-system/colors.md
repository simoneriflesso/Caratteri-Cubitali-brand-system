# Palette colori — Caratteri Cubitali Design System

## Colori ufficiali

| Nome | Hex | Ruolo |
|---|---|---|
| Blu Vibrante | `#434CE0` | Colore Accent principale ★ |
| Giallo Vivo | `#FED74E` | Colore secondario ★ |
| Nero | `#0D0D0D` | Neutro primario |
| Bianco | `#F3F3F3` | Neutro secondario |
| Rosso | `#F24E29` | Uso limitato — urgenza/errore |
| Verde | `#04BF68` | Uso limitato — successo/conferma |

---

## Scale colori estese

### Blu Vibrante — scala completa (50→900)

| Passo | Hex | Uso |
|---|---|---|
| 50 | `#ECEEFF` | Sfondo pastello |
| 100 | `#D4D8FF` | Sfondo pastello |
| 200 | `#A9B1FF` | Sfondo pastello |
| 300 | `#7E8AFF` | Testo su Nero |
| 400 | `#5C67F5` | — |
| **500 ★** | **`#434CE0`** | **Colore brand ufficiale** |
| 600 | `#3239C4` | — |
| 700 | `#2229A8` | Testo su Blu 50/100 |
| 800 | `#141B82` | Testo su Blu 50/100 · sfondo scuro |
| 900 | `#0B105C` | Sfondo scuro |

### Giallo Vivo — scala parziale (50→500)

| Passo | Hex | Uso |
|---|---|---|
| 50 | `#FFFBEC` | Sfondo pastello |
| 100 | `#FFF4C4` | Sfondo pastello |
| 200 | `#FEEA8A` | Sfondo pastello |
| 300 | `#FEDE62` | — |
| **400 ★** | **`#FED74E`** | **Colore brand ufficiale** |
| 500 | `#F5C820` | Più saturo |

> Giallo 600–900 non utilizzati: i valori molto scuri non rientrano nel sistema visivo del brand.

### Nero — scala completa (50→900)

| Passo | Hex | Uso |
|---|---|---|
| 50 | `#F3F3F3` | Bianco brand (sfondo base) |
| 100 | `#E0E0E0` | — |
| 200 | `#C5C5C5` | — |
| 300 | `#ABABAB` | — |
| 400 | `#828282` | — |
| 500 | `#5C5C5C` | — |
| 600 | `#3D3D3D` | — |
| 700 | `#2A2A2A` | — |
| 800 | `#1A1A1A` | Sfondo scuro alternativo |
| **900 ★** | **`#0D0D0D`** | **Colore brand ufficiale** |

### Rosso — scala parziale (50→500)

| Passo | Hex |
|---|---|
| 50 | `#FFF1EE` |
| 100 | `#FFD9D0` |
| 200 | `#FFAB96` |
| 300 | `#FF7F5E` |
| 400 | `#F85E38` |
| **500 ★** | **`#F24E29`** |

### Verde — scala parziale (50→500)

| Passo | Hex |
|---|---|
| 50 | `#EAFBF2` |
| 100 | `#C2F2DA` |
| 200 | `#7EE5B4` |
| 300 | `#3ED490` |
| 400 | `#12C97A` |
| **500 ★** | **`#04BF68`** |

---

## Regole di utilizzo

### Testo su sfondi — combinazioni approvate

#### Regola base: testo Nero su pastello
Testo `#0D0D0D` su qualsiasi sfondo pastello (passo 50–200) dei colori brand.  
Esclusi: Nero 100 (`#E0E0E0`) e Nero 200 (`#C5C5C5`) come sfondi (troppo neutri, poco carattere).

#### Sfondo Bianco
- Testo Nero → 21:1 AAA
- Testo Blu 500 → 5.5:1 AA

#### Sfondo Nero
- Testo Bianco → 21:1 AAA
- Testo Blu 300 (`#7E8AFF`) → AA
- Testo Giallo 400 → 14.7:1 AAA
- Testo Rosso 500 → ~3.5:1 AA Large (solo testo grande ≥18px)
- Testo Verde 500 → AA

#### Eccezioni Blu
- Blu 700/800 su sfondo Blu 50/100 (testo scuro su pastello blu) → AA
- Blu 500 su Bianco → AA

### Cosa non fare
- **Mai colore su stesso colore** (no Giallo su Giallo, no Blu su Blu)
- **Mai colori diversi sullo stesso elemento statistica** (numero e % stessa tinta)
- **Mai pastello come fondino di headline** (solo i 5 colori ufficiali)
- **Mai Rosso o Verde come colore di label sezione** (contrasto insufficiente con bordo sottile)

---

## Accessibilità cromatica

La palette è verificata per daltonismo con simulatore Canva:
- Nessun conflitto colore tra i 4 colori principali
- Adatta a Deuteranopia e Protanopia
- In Tritanopia il Giallo diventa rosa chiaro — usare sempre anche testo/bordo per informazioni critiche

---

## Design tokens CSS

```css
:root {
  /* Colori principali */
  --cc-nero:   #0D0D0D;
  --cc-bianco: #F3F3F3;
  --cc-blu:    #434CE0;
  --cc-giallo: #FED74E;
  --cc-rosso:  #F24E29;
  --cc-verde:  #04BF68;

  /* Scala Blu */
  --cc-blu-50:  #ECEEFF;
  --cc-blu-100: #D4D8FF;
  --cc-blu-200: #A9B1FF;
  --cc-blu-300: #7E8AFF;
  --cc-blu-400: #5C67F5;
  --cc-blu-600: #3239C4;
  --cc-blu-700: #2229A8;
  --cc-blu-800: #141B82;
  --cc-blu-900: #0B105C;

  /* Semantic tokens */
  --cc-accent:     var(--cc-blu);
  --cc-secondary:  var(--cc-giallo);
  --cc-surface:    var(--cc-bianco);
  --cc-on-surface: var(--cc-nero);
}
```
