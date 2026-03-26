# 🧪 Mi Laboratorio Digital — Vibe Coding Prompt
**Digital Fluency · DaVinci · Collective Academy**

---

## Antes de abrir Bolt — llena esta hoja con tu información

> Abre tu Miro, navega zona por zona, y copia tu información aquí.
> Cuando la tengas completa, pega el prompt en [bolt.new](https://bolt.new)
> y reemplaza cada `[...]` con tus datos reales.

---

### 👤 Datos personales

| Campo | Tu información |
|-------|---------------|
| Nombre completo | |
| Rol | |
| Empresa | |

---

### S1 · Tus territorios digitales

| | T1 | T2 | T3 |
|-|----|----|-----|
| **Nombre del territorio** | | | |
| **Estado actual** | | | |
| **Estado deseado en 90 días** | | | |

---

### S3 · Tu Board de AI Advisors

| | Advisor 1 | Advisor 2 | Advisor 3 |
|-|-----------|-----------|-----------|
| **Nombre del advisor** | | | |
| **Perspectiva / rol** | | | |
| **Pregunta que te hace** | | | |

---

### S4 · Tu evaluación ARL + VIRA

| Campo | Tu información |
|-------|---------------|
| Tecnología o iniciativa seleccionada | |
| Nivel ARL (promedio 1–5) | |
| Score V (Valor) | |
| Score I (Implementabilidad) | |
| Score R (Riesgo) | |
| Score A (Adopción) | |
| Total VIRA | |
| Tu recomendación en una frase | |
| Riesgo que aceptas conscientemente | |

---

### S5 · Tu Framework HER

| Campo | Tu información |
|-------|---------------|
| **H** — La apuesta que estoy haciendo | |
| **H** — El problema organizacional que resuelve | |
| **E** — 30 días: haré... y aprenderé si... | |
| **E** — 60 días: ajustaré... y aprenderé si... | |
| **E** — 90 días: entregaré... y habré aprendido que... | |
| **R** — Lo que entrego a mi organización al día 90 | |
| **R** — Cómo sé que funcionó (métrica o evidencia) | |

---

### ⚡ Primera acción el lunes

| Campo | Tu información |
|-------|---------------|
| Una sola acción. Específica. El lunes. | |

---

## Cómo usar el prompt

1. **Llena la hoja de arriba** con tu información del Miro
2. **Copia el prompt de abajo** en [bolt.new](https://bolt.new)
3. **Reemplaza cada `[...]`** con tus datos antes de enviarlo
4. Espera 1-2 minutos mientras Bolt genera tu sitio
5. Revisa en **Preview** — si algo falla, usa la tabla de bugs al final
6. Haz clic en **Deploy** para obtener tu URL pública

---

## Prompt

> ⚠️ Reemplaza todos los `[...]` con tu información antes de pegar en Bolt.

```
Build a single-page personal digital plan website.
One index.html file only. Vanilla HTML + CSS + JS. No frameworks, no npm.

CONTEXT:
Personal "Digital Lab" page for an executive in pharma / Latin America
who completed a 5-session program called Digital Fluency. This page
presents their 30-60-90 day digital plan so they can share it with
their organization.

PARTICIPANT DATA — use exactly as written, as default field content:
- Name: [Tu nombre completo]
- Role: [Tu rol · Tu empresa]

HER FRAMEWORK:
- H apuesta: [Tu hipótesis de impacto]
- H problema: [El problema organizacional que resuelve]
- E 30d: [Acción y aprendizaje en 30 días]
- E 60d: [Acción y aprendizaje en 60 días]
- E 90d: [Acción y aprendizaje en 90 días]
- R entrego: [Lo que entregas al día 90]
- R métrica: [Cómo sabes que funcionó]

TERRITORIES (S1):
- T1: [Nombre T1] | actual: [Estado actual] | deseado: [Estado en 90 días]
- T2: [Nombre T2] | actual: [Estado actual] | deseado: [Estado en 90 días]
- T3: [Nombre T3] | actual: [Estado actual] | deseado: [Estado en 90 días]

AI BOARD (S3):
- Advisor 1: [Nombre] · [Perspectiva] · [Pregunta que hace]
- Advisor 2: [Nombre] · [Perspectiva] · [Pregunta que hace]
- Advisor 3: [Nombre] · [Perspectiva] · [Pregunta que hace]

TECH DECISION (S4):
- Technology: [Nombre de la tecnología o iniciativa]
- ARL: [Nivel ARL] | V: [Score] | I: [Score] | R: [Score] | A: [Score] | Total: [Total VIRA]
- Recommendation: [Tu recomendación en una frase]
- Risk: [El riesgo que aceptas conscientemente]

MONDAY ACTION: [Tu primera acción el lunes]

DESIGN SYSTEM:
- Background: #0A0A0A | Text: #F5F2ED
- Accents: Magenta #E91E8C | Green #00C851 | Purple #7B2FBE | Amber #F59E0B
- Fonts: Google Fonts — Syne weight 800 (headings) + DM Sans (body)
  Import via single CSS @import in <style> tag
- Dark, executive feel. No white backgrounds. No startup aesthetics.
- CSS variables in :root. No inline style attributes.
- Mobile responsive with CSS Grid + Flexbox.
- IntersectionObserver scroll reveal on cards (fadeUp, stagger 80ms).

SECTIONS (single scrolling page):

1. HERO
   - Participant name (large Syne 800) and role (smaller, gray)
   - Big display title: "Mi / Laboratorio / Digital" — "Laboratorio" in magenta
   - Subtitle: "Plan 30 · 60 · 90 días"
   - Progress nodes S1→S5: S1–S4 filled green with checkmark,
     S5 in magenta with glow, all connected by a horizontal line

2. HER FRAMEWORK — 3 cards side by side (stack on mobile)
   Each card: 3px color top bar (H=magenta, E=green, R=purple)
   Big letter + section name + guiding question + editable fields + connection footer.
   E card has 3 rows: 30d / 60d / 90d with colored badge + editable text each.

3. TERRITORIES (S1) — 3 cards in grid, green top border
   Each: T1/T2/T3 badge, territory name, two columns:
   "Estado actual" (gray label) → arrow → "En 90 días" (green label)

4. AI BOARD (S3) — 3 cards, purple accent
   Each: large number watermark (01/02/03), advisor name in purple,
   role/perspective, key question they ask.

5. TECH DECISION (S4) — two-column layout
   Left card (amber top border): tech name, recommendation, risk block.
   Right: score grid — ARL, V, I, R, A, VIRA Total (Total spans full width).
   Color: V=green, R=magenta, A=amber, Total=magenta.

6. MONDAY ACTION — full-width magenta background section
   Small uppercase label + large white bold text.

FOOTER: "Digital Fluency · DaVinci · Collective Academy" left,
"León Ruiz · 2026" right, auto-save indicator center.

FLOATING CONTROLS (bottom-right, column of 3 icon buttons):
- Edit/View toggle: contenteditable on/off, body gets .view-mode class
- Export PDF: window.print()
- Copy link: navigator.clipboard.writeText + toast "¡Link copiado!"

ALL TEXT FIELDS: contenteditable="true" with data-key attribute.
On focus: magenta border (or section accent color).
:empty::before shows placeholder in gray italic using data-placeholder attr.
Single-line fields (name, scores): prevent Enter key, blur instead.
View mode: contenteditable=false, transparent borders, pointer-events none.

PERSISTENCE:
- Debounce 700ms save all data-key fields to localStorage on input
- Restore all from localStorage on page load
- Show "· guardado" text briefly after each save

TECHNICAL CONSTRAINTS:
- ONE file: index.html (all CSS in <style>, all JS in <script>)
- Google Fonts via @import in CSS only — no <link> tags for fonts
- No external JS libraries whatsoever
- localStorage for all data persistence
- All styling via CSS classes — no inline style attributes
- Target under 600 lines total
```

---

## Bugs comunes — qué escribir en Bolt para corregirlos

No regeneres desde cero. Solo escribe en el chat de Bolt:

| Problema | Qué escribir en Bolt |
|----------|---------------------|
| Los campos no guardan al recargar | `The localStorage save/load isn't working. Fix so all contenteditable fields with data-key persist on page reload.` |
| En móvil las cards se ven mal | `Fix mobile layout: HER, territory and board cards should stack vertically on screens under 768px.` |
| El PDF sale con fondo negro | `Fix print CSS: white background, black text, hide floating controls, no page breaks inside cards.` |
| Los placeholders no aparecen | `Add :empty::before CSS for all contenteditable fields using data-placeholder as gray italic text.` |
| El toggle de edición no funciona | `Edit/view toggle broken. In view mode set contenteditable=false on all editable fields and remove focus styles.` |
| Las fuentes no cargan | `Replace Google Fonts with system fonts: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif.` |
| Mi información no aparece | `The participant data I provided in the prompt isn't showing. Use it as default innerHTML for each field, not as placeholder.` |

---

*Digital Fluency · DaVinci · Collective Academy · León Ruiz · 2026*
