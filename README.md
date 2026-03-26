# 🧪 Mi Laboratorio Digital — Framework HER
**Digital Fluency · DaVinci · Collective Academy**

---

## Lo único que necesitas hacer

1. **Toma un screenshot de tu Zona 5 en Miro** — el frame naranja con tu HER completo
2. **Abre [bolt.new](https://bolt.new)**
3. **Pega el prompt de abajo** y **adjunta tu screenshot** en el mismo mensaje
4. Espera 1-2 minutos, revisa en **Preview** y haz **Deploy**

---

## Prompt

```
I'm going to attach a screenshot of my HER framework from a program
called Digital Fluency. Read the image carefully and extract every
piece of text visible in it.

Then build me a single-page website that presents my HER framework.

--- READING THE IMAGE ---

Extract from the screenshot:
- My name (look in the frame header or participant name field)
- H: my impact hypothesis ("la apuesta que estoy haciendo")
- H: the organizational problem it solves
- E: what I'll do and learn at 30 days
- E: what I'll do and learn at 60 days
- E: what I'll do and learn at 90 days
- R: what I deliver to my organization at day 90
- R: how I know it worked
- My first action on Monday (the last field at the bottom)

If any field is unclear in the image, use "[completar]" as placeholder.

--- BUILD THE SITE ---

One index.html file only. Vanilla HTML + CSS + JS. No npm, no frameworks.

DESIGN:
- Background: #0A0A0A | Text: #F5F2ED
- H accent: #E91E8C (magenta) | E accent: #00C851 (green) | R accent: #7B2FBE (purple)
- Fonts: Google Fonts — Syne 800 (headings) + DM Sans (body) via CSS @import
- Dark executive feel. No white backgrounds. CSS variables in :root.
- Mobile responsive. Subtle fadeUp animation on load.

LAYOUT (single scrolling page):

1. HEADER
   - My name (large, Syne 800)
   - Small badge: "Framework HER · Mi Laboratorio Digital"
   - Tagline: "Mi apuesta. Mi experimento. Mi retorno."

2. HER — 3 cards side by side (stack on mobile)

   H card (magenta top bar):
   - Big letter "H" in magenta
   - Label: "Hipótesis de Impacto"
   - Question: "¿Qué problema organizacional estás apostando a resolver?"
   - My content: apuesta + problema (editable fields)
   - Footer note: "Conecta con: Territorio (S1) · Decisión (S4)"

   E card (green top bar):
   - Big letter "E" in green
   - Label: "Experimento Estructurado"
   - Question: "¿Qué harás y qué aprenderás en 30-60-90 días?"
   - 3 rows: badge (30d / 60d / 90d) + editable text each
   - Footer note: "Conecta con: D.A.T.A. (S2) · Board (S3) · ARL/VIRA (S4)"

   R card (purple top bar):
   - Big letter "R" in purple
   - Label: "Retorno Demostrable"
   - Question: "¿Qué le entregas a tu organización al día 90?"
   - My content: entrego + métrica (editable fields)
   - Footer note: "Conecta con: Score VIRA (S4) · Territorio (S1)"

3. MONDAY ACTION — full-width magenta bar
   - Label: "⚡ Mi primera acción el lunes"
   - My action text (large, white, bold, editable)

FOOTER: "Digital Fluency · DaVinci · Collective Academy · León Ruiz · 2026"

FLOATING CONTROLS (bottom-right, 3 icon buttons):
- Edit/View toggle: contenteditable on/off
- Export PDF: window.print()
- Copy link: navigator.clipboard + toast "¡Link copiado!"

EDITABLE FIELDS:
- All text areas: contenteditable="true" with data-key
- On focus: border in card's accent color
- :empty::before shows placeholder in gray italic
- Single-line fields: prevent Enter key, blur instead
- View mode: contenteditable=false, borders transparent

PERSISTENCE:
- Debounce 700ms save to localStorage on input
- Restore from localStorage on load
- Show "· guardado" briefly after save

PRINT CSS:
- White background, black text
- Hide floating controls
- No page breaks inside cards

CONSTRAINTS:
- ONE file: index.html
- Google Fonts via CSS @import only
- No external JS libraries
- Under 400 lines total
```

---

## Si algo no quedó bien — qué escribirle a Bolt

| Problema | Qué escribir en Bolt |
|----------|---------------------|
| No leyó bien un campo | `You missed [campo]. It says: "[texto exacto]". Please update it.` |
| Los datos no guardan | `localStorage isn't working. Fix save/load for all data-key fields.` |
| En móvil se ve mal | `Fix mobile: HER cards should stack vertically under 768px.` |
| PDF con fondo negro | `Fix print CSS: white bg, black text, hide controls, no breaks inside cards.` |

---

*Digital Fluency · DaVinci · Collective Academy · León Ruiz · 2026*
