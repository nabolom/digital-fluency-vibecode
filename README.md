# 🧪 Mi Laboratorio Digital — Vibe Coding Prompt

**Digital Fluency · DaVinci · Collective Academy**  
Usa este prompt en [bolt.new](https://bolt.new) para construir tu sitio personal de plan 30-60-90.

---

## Cómo usarlo

1. Abre [bolt.new](https://bolt.new)
2. Copia el bloque de abajo y pégalo en el campo de prompt
3. Espera 1-2 minutos mientras Bolt genera el sitio
4. Haz clic en **Preview** para verlo
5. Edita los campos directamente en el navegador
6. Cuando esté listo, haz clic en **Deploy** para obtener tu URL pública

---

## Prompt

```
Build a single-page personal digital plan website.
One index.html file only. Vanilla HTML + CSS + JS. No frameworks, no npm.

CONTEXT:
Personal "Digital Lab" page for an executive in pharma / Latin America.
They completed a 5-session program called Digital Fluency and built a
30-60-90 day digital expansion plan using 4 frameworks across sessions.
This page presents that plan so they can share it with their organization.

DESIGN SYSTEM:
- Background: #0A0A0A | Text: #F5F2ED
- Accents: Magenta #E91E8C | Green #00C851 | Purple #7B2FBE | Amber #F59E0B
- Fonts: Google Fonts — Syne (headings, weight 800) + DM Sans (body)
  Import via single CSS @import at top of <style>
- Dark, executive feel. No white backgrounds. No startup aesthetics.
- CSS variables in :root. No inline style attributes.
- Mobile responsive with CSS Grid + Flexbox.
- IntersectionObserver scroll reveal on cards (fadeUp, stagger 80ms).

SECTIONS (single scrolling page):

1. HERO
   - Editable name (large, Syne 800, white)
   - Editable role/company (smaller, gray)
   - Big display title: "Mi / Laboratorio / Digital" — "Laboratorio" in magenta
   - Subtitle: "Plan 30 · 60 · 90 días"
   - Progress nodes: S1 S2 S3 S4 S5 — S1–S4 filled green with checkmark,
     S5 in magenta with glow, connected by a horizontal line

2. HER FRAMEWORK — 3 cards side by side (stack on mobile)
   Each card has a 3px color bar on top (H=magenta, E=green, R=purple)
   H card: big letter "H" + label "Hipótesis de Impacto"
     - Field: "La apuesta que estoy haciendo"
     - Field: "El problema que resuelve"
     - Footer: "Conecta con: Territorio (S1) · Decisión (S4)"
   E card: big letter "E" + label "Experimento Estructurado"
     - 3 rows with colored badge (30d / 60d / 90d) + editable textarea each
     - Footer: "Conecta con: D.A.T.A. (S2) · Board (S3) · ARL/VIRA (S4)"
   R card: big letter "R" + label "Retorno Demostrable"
     - Field: "Lo que entrego al día 90"
     - Field: "Cómo sé que funcionó"
     - Footer: "Conecta con: Score VIRA (S4) · Territorio (S1)"

3. TERRITORIES (S1) — 3 cards in a grid, green top border
   Each: T1/T2/T3 badge, editable territory name, two columns:
   "Estado actual" (gray label) → arrow → "En 90 días" (green label)
   Each state has an editable textarea.

4. AI BOARD (S3) — 3 cards, purple accent
   Each: large number (01/02/03) watermark top-right,
   editable advisor name (purple), editable role/perspective,
   editable "Pregunta que hace"

5. TECH DECISION (S4) — two-column layout
   Left: card with amber top border
     - Editable tech name (large, bold)
     - Editable recommendation textarea
     - Risk block (amber background tint): editable risk text
   Right: score grid 2x3
     - ARL, V, I, R, A, VIRA Total — each a small card with editable number
     - V=green, R=magenta, A=amber, Total=magenta and spans full width

6. MONDAY ACTION — full-width magenta background
   - Label: "⚡ Mi primera acción el lunes"
   - Large editable text (Syne 700, white, underline on focus)

FOOTER: dark background, "Digital Fluency · DaVinci · Collective Academy"
left, "León Ruiz · 2026" right, auto-save indicator center.

FLOATING CONTROLS (bottom-right, column of 3 icon buttons):
- Edit/View toggle: switches contenteditable on/off, body gets .view-mode class
- Export PDF: window.print() — print CSS hides controls, white bg, black text
- Copy link: navigator.clipboard + toast notification

EDITABLE FIELDS:
- All content areas: contenteditable="true"
- data-key attribute on each for localStorage
- :empty::before shows placeholder text (gray italic)
- On focus: magenta border (or accent color of section)
- Single-line fields (name, scores): prevent Enter key, blur instead
- In view mode: contenteditable=false, transparent borders, pointer-events none

PERSISTENCE:
- On any input event: debounce 700ms, save all data-key fields to localStorage
- On page load: restore all saved content
- Show "· guardado" indicator briefly after save

DEFAULT PLACEHOLDER CONTENT (use as initial innerHTML):
- Name: "Ana García"
- Role: "Directora Comercial · Farmacéutica Regional"
- H apuesta: "Si implementamos un sistema de análisis de demanda en los
  próximos 60 días, tomaremos decisiones de forecast con datos en lugar
  de intuición, reduciendo errores de abasto en un 30%."
- H problema: "El equipo toma decisiones de inventario basadas en experiencia
  histórica sin datos actualizados ni criterio estructurado."
- E 30d: "Mapeo de fuentes de datos + configurar advisor escéptico en Gemini.
  Aprendo: ¿qué datos existen y cuáles faltan?"
- E 60d: "Piloto de dashboard en 1 región. Aprendo: ¿funciona con los datos
  actuales o necesito fuentes adicionales?"
- E 90d: "Entrego informe de decisión con recomendación de escalar o pivotar."
- R entrego: "Informe: datos de adopción, costo real vs. estimado,
  recomendación fundamentada para Q4."
- R métrica: "Mi director toma la decisión con el informe — no con mi opinión."
- T1: name="Análisis de demanda" actual="Reportes manuales semanales"
  deseado="Alertas automáticas con dashboard compartido"
- T2: name="Comunicación con equipo" actual="WhatsApp sin estructura"
  deseado="Dashboard con KPIs semanales"
- T3: name="Relación con distribuidores" actual="Llamadas reactivas"
  deseado="Revisión proactiva con datos de tendencia"
- Advisor 1: "El CFO Escéptico · Cuestiona ROI antes de invertir"
- Advisor 2: "La Usuaria Final · ¿Esto cambia mi día a día?"
- Advisor 3: "El Regulador · ¿Qué riesgos estamos ignorando?"
- Tech: "Dashboard BI de demanda" ARL=2.5 V=4 I=3 R=3 A=2 Total=12
- Risk: "Adopción lenta del equipo. Mitigo con capacitación en semanas 1-2."
- Monday: "Agendar reunión con el equipo de datos para mapear qué información
  existe hoy en el sistema."

TECHNICAL CONSTRAINTS:
- ONE file: index.html (all CSS in <style>, all JS in <script>)
- Google Fonts via @import in CSS only
- No external JS libraries
- localStorage for all persistence
- Total under 600 lines
- All CSS as classes, no inline styles
```

---

## Bugs comunes — cómo pedirle a Bolt que los corrija

Si algo no funciona, escribe esto en el chat de Bolt **sin regenerar desde cero**:

| Problema | Qué escribir en Bolt |
|----------|---------------------|
| Los campos no guardan al recargar | `The localStorage save/load isn't working. Fix so all contenteditable fields with data-key persist on page reload.` |
| En móvil las cards se ven mal | `Fix mobile layout: HER cards, territory cards and board cards should stack vertically on screens under 768px.` |
| El PDF sale con fondo negro | `Fix print CSS: white background, black text for all sections, hide floating controls, no page breaks inside cards.` |
| Los placeholders no aparecen | `Add :empty::before CSS for all contenteditable fields showing data-placeholder attribute as gray italic text.` |
| El toggle de edición no funciona | `The edit/view toggle isn't working. In view mode set contenteditable=false on all .editable elements and remove focus styles.` |
| Las fuentes de Google no cargan | `Replace Google Fonts with system fonts: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif. Use font-weight 800 for headings.` |

---

## Después del deploy

Una vez que Bolt genera tu sitio y haces **Deploy**:

- Obtienes una URL tipo `https://[algo].bolt.new/` o en tu GitHub Pages
- Esa URL la puedes compartir con tu director o equipo
- Los datos se guardan en **tu navegador** (localStorage) — si abres en otro dispositivo, verás el contenido por defecto
- Para tener tus datos en cualquier dispositivo, edita el contenido directamente en el HTML antes de hacer deploy

---

*Digital Fluency · DaVinci · Collective Academy · León Ruiz · 2026*
