# Mi Laboratorio Digital — Vibe Coding Prompt
**Digital Fluency · DaVinci · Collective Academy**

---

## Lo único que necesitas hacer

1. **Toma screenshots de tu Miro** — una por cada zona (ver abajo)
2. **Abre [bolt.new](https://bolt.new)**
3. **Pega el prompt** en el campo de texto
4. **Adjunta tus screenshots** en el mismo mensaje
5. Espera 1-2 minutos, revisa en **Preview** y haz **Deploy**

Eso es todo. Bolt lee tus imágenes y construye tu sitio con tu información.

---

## Qué screenshots tomar en Miro

Toma una screenshot por cada zona. No importa la calidad exacta,
solo que el texto sea legible.

| # | Zona en Miro | Qué captura |
|---|-------------|-------------|
| 1 | **Zona 1** — Mis Territorios Digitales | Los 3 territorios con estado actual y deseado |
| 2 | **Zona 2** — Mi Framework D.A.T.A. | Tu decisión y las preguntas completadas |
| 3 | **Zona 3** — Mi Board de AI Advisors | Los 3 advisors con su rol y pregunta |
| 4 | **Zona 4** — ARL + VIRA + Decisión | Tus scores y tu recomendación |
| 5 | **Zona 5** — HER + Plan 30-60-90 | Tu H, E, R y primera acción del lunes |

> 💡 Si tienes todo en una sola vista panorámica de Miro, también sirve.

---

## Prompt

```
I'm going to attach screenshots of my personal digital plan built across
5 sessions of a program called Digital Fluency. Please read ALL the images
carefully and extract every piece of information visible in them.

Then build me a single-page personal website using that exact information.

--- READING THE IMAGES ---

Extract from the screenshots:
- My name and role/company (look in headers or participant name fields)
- My 3 digital territories: name, current state, desired state in 90 days
- My D.A.T.A. framework: the decision I evaluated and key questions
- My AI Board of Advisors: name, perspective/role, and key question for each
- My ARL level (the maturity score, 1-5 scale)
- My VIRA scores: V (Valor), I (Implementabilidad), R (Riesgo), A (Adopción)
- My technology/initiative recommendation and the risk I accept
- My HER framework:
    H = my impact hypothesis (the organizational bet I'm making)
    E = my structured experiment (what I'll do and learn in 30/60/90 days)
    R = my demonstrable return (what I deliver to the org at day 90)
- My first action on Monday

If any field is not visible or unclear in the images, use a short
placeholder like "[completar]" so I know what to fill in manually.

--- BUILD THE SITE ---

One index.html file only. Vanilla HTML + CSS + JS. No frameworks, no npm.

DESIGN SYSTEM:
- Background: #0A0A0A | Text: #F5F2ED
- Accents: Magenta #E91E8C | Green #00C851 | Purple #7B2FBE | Amber #F59E0B
- Fonts: Google Fonts — Syne weight 800 (headings) + DM Sans (body)
  Import via single CSS @import in <style> tag
- Dark, executive feel. No white backgrounds.
- CSS variables in :root. No inline style attributes.
- Mobile responsive with CSS Grid + Flexbox.
- IntersectionObserver scroll reveal on cards (fadeUp, stagger 80ms).

SECTIONS (single scrolling page):

1. HERO
   - My name (large Syne 800) and role (smaller, gray)
   - Big display title: "Mi / Laboratorio / Digital" — "Laboratorio" in magenta
   - Subtitle: "Plan 30 · 60 · 90 días"
   - Progress track S1→S5: S1–S4 filled green with checkmark,
     S5 in magenta with glow, connected by horizontal line

2. HER FRAMEWORK — 3 cards side by side (stack on mobile)
   Each card: 3px color top bar (H=magenta, E=green, R=purple)
   Big letter + section name + guiding question + my content + connection footer.
   E card: 3 rows with day badge (30d/60d/90d) + my text for each.

3. TERRITORIES (S1) — 3 cards in grid, green top border
   Each: T1/T2/T3 badge, territory name, two columns:
   "Estado actual" (gray) → arrow → "En 90 días" (green)

4. AI BOARD (S3) — 3 cards, purple accent
   Each: large number watermark (01/02/03), advisor name in purple,
   role/perspective, key question they ask me.

5. TECH DECISION (S4) — two-column layout
   Left card (amber top border): tech name, recommendation, risk block.
   Right: score grid — ARL, V, I, R, A, VIRA Total (Total spans full width).
   Color: V=green, R=magenta, A=amber, Total=magenta.

6. MONDAY ACTION — full-width magenta background
   Small uppercase label + large white bold text with my action.

FOOTER: "Digital Fluency · DaVinci · Collective Academy" left,
"León Ruiz · 2026" right, auto-save indicator center.

FLOATING CONTROLS (bottom-right, column of 3 icon buttons):
- Edit/View toggle: contenteditable on/off, body gets .view-mode
- Export PDF: window.print()
- Copy link: navigator.clipboard + toast "¡Link copiado!"

ALL TEXT FIELDS: contenteditable="true" with data-key attribute.
On focus: magenta border. :empty::before shows placeholder in gray italic.
Single-line fields (name, scores): prevent Enter, blur instead.
View mode: contenteditable=false, transparent borders, pointer-events none.

PERSISTENCE:
- Debounce 700ms save all data-key fields to localStorage on input
- Restore from localStorage on page load
- Show "· guardado" briefly after save

CONSTRAINTS:
- ONE file: index.html (all CSS in <style>, all JS in <script>)
- Google Fonts via @import in CSS only
- No external JS libraries
- localStorage for persistence
- All styling via CSS classes — no inline styles
```

---

## Si algo no se ve bien — qué escribirle a Bolt

No regeneres desde cero. Solo describe el problema en el chat de Bolt:

| Problema | Qué escribir en Bolt |
|----------|---------------------|
| No leyó bien un campo de mi Miro | `You missed [campo] from my screenshots. It says: "[texto exacto]". Please update that field.` |
| Los campos no guardan al recargar | `localStorage save/load isn't working. Fix so all contenteditable fields with data-key persist on reload.` |
| En móvil se ve mal | `Fix mobile layout: all card grids should stack vertically on screens under 768px.` |
| El PDF sale con fondo negro | `Fix print CSS: white background, black text, hide floating controls, no page breaks inside cards.` |
| El toggle de edición no funciona | `Edit/view toggle broken. In view mode set contenteditable=false on all editable fields.` |
| Las fuentes no cargan | `Replace Google Fonts with system fonts: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif.` |

---

*Digital Fluency · DaVinci · Collective Academy · León Ruiz · 2026*
