# 🧪 Vibecoding — Framework HER
**Digital Fluency · DaVinci · Collective Academy**

---

## Lo único que necesitas hacer

1. **Toma dos screenshots:**
   - Tu **Zona 5 de Miro** con tu HER ya completado
   - La **imagen de referencia de diseño** que te compartió León
     (el formulario oscuro con las tres columnas H · E · R)
2. **Abre [bolt.new](https://bolt.new)**
3. **Pega el prompt de abajo**, adjunta **las dos imágenes** y envía
4. Revisa en **Preview**, haz **Deploy** y comparte tu URL

---

## Prompt

```
I'm attaching two images:
1. A DESIGN REFERENCE — the exact layout and visual style to replicate
2. MY MIRO DATA — my completed HER framework with my actual content

Read both images carefully.
Extract all my personal content from image 2.
Replicate the visual design from image 1 exactly.
Build it as a single index.html file.

--- DESIGN (replicate from reference image) ---

Dark background (#0A0A0A). Off-white text (#F5F2ED).
Three-column layout for H · E · R cards (stack on mobile).

H card — magenta (#E91E8C) top bar, 3px:
  - Label: "HIPÓTESIS DE IMPACTO" in magenta caps
  - Big letter "H" in magenta (large, faint ghost letter behind)
  - Italic question: "¿Qué problema organizacional estás apostando a resolver?"
  - Field label: "La apuesta que estoy haciendo:"
  - Dark input box with my content
  - Field label: "El problema que resuelve (no la solución):"
  - Dark input box with my content
  - Footer: "Conecta con: Territorio (S1) · Decisión (S4)"

E card — green (#00C851) top bar, 3px:
  - Label: "EXPERIMENTO ESTRUCTURADO" in green caps
  - Big letter "E" in green
  - Italic question: "¿Qué harás y qué aprenderás en 30-60-90 días?"
  - Three rows, each with field label + dark input box:
      "30 días — Haré... y aprenderé si..."
      "60 días — Ajustaré... y aprenderé si..."
      "90 días — Entregaré... y habré aprendido que..."
  - Footer: "Conecta con: D.A.T.A. (S2) · Board (S3) · ARL/VIRA (S4)"

R card — purple (#7B2FBE) top bar, 3px:
  - Label: "RETORNO DEMOSTRABLE" in purple caps
  - Big letter "R" in purple
  - Italic question: "¿Qué le entregas a tu organización al día 90?"
  - Field label: "Lo que entrego al día 90:"
  - Dark input box with my content
  - Field label: "Cómo sé que funcionó:"
  - Dark input box with my content
  - Footer: "Conecta con: Score VIRA (S4) · Territorio (S1)"

Below the three cards — two boxes side by side (full width):
  Left box: label "LO QUE APRENDÍ DE MI BOARD EN ESTE PROCESO" + dark input
  Right box: label "LA PARTE MÁS FRÁGIL DE MI PLAN — Y CÓMO LA FORTALEZCO" + dark input

Bottom — full-width magenta bar (#E91E8C):
  - ">" arrow icon on left
  - Label: "MI PRIMERA ACCIÓN EL LUNES" in white caps
  - White underline input field with my action text

--- FUNCTIONALITY ---

All input boxes: contenteditable="true" with data-key attribute.
On focus: subtle border glow in the card's accent color.
Debounce 700ms save to localStorage. Restore on page load.
Show "· guardado" briefly after save.

Three floating icon buttons bottom-right:
  - Edit/View toggle (pencil): contenteditable on/off
  - Export PDF (download): window.print()
  - Copy link (chain): navigator.clipboard + toast "¡Link copiado!"

Print CSS: white background, black text, hide buttons.

--- CONSTRAINTS ---

One index.html file. All CSS in <style>. All JS in <script>.
Google Fonts: DM Sans via CSS @import only.
No frameworks. No npm. No external JS.
CSS variables in :root. No inline styles.
```

---

## Si algo no quedó bien

| Problema | Qué escribirle a Bolt |
|----------|----------------------|
| No leyó bien un campo | `You missed [campo]. It says: "[texto]". Please update it.` |
| Los datos no guardan | `Fix localStorage: save/load all data-key fields on input and page load.` |
| En móvil se ve mal | `Fix mobile: stack all cards vertically under 768px.` |
| PDF con fondo negro | `Fix print CSS: white background, black text, hide floating buttons.` |

---

*Digital Fluency · DaVinci · Collective Academy · León Ruiz · 2026*
