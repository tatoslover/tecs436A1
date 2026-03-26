# TECS436 A1 — Design Plan

**Year level:** Year 9 (13–14 year olds)
**Subject:** Financial Literacy / Commerce
**Unit theme:** *Trust & Exchange — from handshake deals to digital transactions*

---

## Unit Narrative Arc

```
Lesson 1                          Bridge                       Lesson 2
Barter, Koha & Utu       ──────────────────────────►   Staying Safe Online
"How did exchange work                                 "The same con artists
 before money, and what            "You've learned      are online now —
 made it fair?"                     to spot what's      can you spot them?"
                                    fake in the
                                    physical world..."
```

The Counterfeit Investigators concept from HW1 becomes a **5–10 min bridge hook** opening Lesson 2: pairs examine 2–3 fictional "fake" digital screenshots using the same investigator framing, then transition into the Look–Check–Pause framework.

---

## Confirmed Decisions

| Decision | Choice |
|----------|--------|
| Lesson 1 | Barter, Koha & Utu |
| Lesson 2 | Staying Safe Online (consumer perspective) |
| Bridge activity | Adapted Counterfeit Investigators — spot the fake screenshot |
| Fake screenshot style | Fictional/stylised (not real scam infrastructure) |
| Year level | Year 9 |
| Karakia | Whakataka te hau (from HW1; may change later) |
| Style | TECS433_A1 (teal/red/blue/purple, sheet-based, print-ready) |

---

## Two Versions — One File

The same `index.html` serves both:

| | Digital version | Physical version |
|---|---|---|
| **What it is** | Hosted HTML site — open in browser on student devices | PDF printed from the same HTML, per sheet |
| **Inputs** | `contenteditable` divs + `<input>` fields for typing | Hidden by `@media print`; replaced by ruled writing lines |
| **Interactivity** | Navigation, interactive inputs, links | All hidden/stripped in print |
| **Buttons** | Per-sheet "↓ Save as PDF" buttons | Hidden in print output |
| **Colours** | Full colour | Preserved with `print-color-adjust: exact` |
| **Barter resource cards** | Displayed on-screen as reference cards | Print-ready, designed to cut up (A6 card size) |
| **Delivery** | GitHub Pages (tatoslover.github.io/...) + submitted HTML | 20-page PDF submitted alongside |

### Screen-only / Print-only pattern (from TECS433_A1)
```css
.screen-only { /* shown on screen */ }
.print-only  { display: none; }          /* shown only in print */

@media print {
  .screen-only { display: none !important; }
  .print-only  { display: inline; }
  /* inputs hidden, writing lines shown */
  input, [contenteditable] { display: none; }
  .write-line { display: block; border-bottom: 1px solid #ccc; }
}
```

---

## Lesson 1 — Barter, Koha & Utu (60 min)

**Kaupapa:** How have people exchanged goods and services across history and cultures — and what made those systems fair?

**Learning focus:**
- Understand barter as a pre-currency exchange system and its practical limitations
- Understand koha as a relational exchange practice grounded in manaakitanga and utu
- Compare these systems to modern currency exchange
- Identify *trust* as the foundation of all exchange (thread to Lesson 2)

**Lesson structure:**

| Time | Phase | Activity |
|------|-------|----------|
| 0–5 min | Karakia + hook | Karakia. Whakataukī: *"Ko tō ringa ki ngā rākau ā tō tīpuna"*. Display a $20 note and a handshake side by side: "What do both have in common?" |
| 5–10 min | Prior knowledge | Discussion: "Has anyone traded something without using money? How did you decide if it was fair?" |
| 10–25 min | Barter simulation | Groups of 5 each get a resource card (e.g., 3 fish / 1 tool / 5 kūmara). Goal: acquire what their card says they need. Debrief: what was hard? what helped? |
| 25–38 min | Koha & utu | Mini-lecture + discussion. What does it mean to give without an invoice? How is that different from barter? |
| 38–50 min | Compare & contrast | Graphic organiser: Barter / Koha / Modern Cash — who benefits? what are the risks? what is required for it to work? |
| 50–57 min | Class discussion | "All three systems need something to work. What is it?" → *trust* |
| 57–60 min | Exit ticket | One written sentence: "What makes an exchange fair?" Collected as formative assessment. |

**Sheets:**
- **Sheet 1 — Context card:** Barter, koha, utu definitions; bilingual te reo / English; whakataukī (reference strip style)
- **Sheet 2 — Barter Simulation:** Resource cards (printable/cut-up) + debrief questions
  - Digital: cards displayed on screen for reference
  - Physical: cut-up A6 cards, one set per group
- **Sheet 3 — Graphic Organiser:** Three-column comparison table, fillable digital / ruled lines print
- **Sheet 4 — Exit ticket:** Half-page, one sentence prompt + writing line

**Formative assessment:** Exit ticket (written sentence) + teacher observation during simulation

---

## Lesson 2 — Staying Safe Online (60 min)

**Kaupapa:** How do we recognise and protect ourselves from digital threats to our money and personal information?

**Learning focus:**
- Connect physical security thinking (from Lesson 1) to digital contexts
- Identify common online financial threats (phishing, scam websites, fake shops)
- Apply Look–Check–Pause framework to evaluate digital interactions
- Know where to get help if something goes wrong (CERT NZ, Netsafe, bank fraud lines)

**Lesson structure:**

| Time | Phase | Activity |
|------|-------|----------|
| 0–5 min | Karakia + bridge | Karakia. "Last lesson we asked what makes exchange fair — today: what makes a digital exchange *safe*?" Show NZ note + phishing email screenshot side by side. |
| 5–15 min | Counterfeit Investigators bridge | Pairs examine 2–3 fictional fake screenshots (dodgy bank site, scam email, fake TradeMe listing). What's wrong? Same investigator framing as the note activity. |
| 15–25 min | Look–Check–Pause framework | Introduce the digital verification framework as parallel to Look–Feel–Tilt. Students complete reference card. |
| 25–45 min | Case study investigation | Groups work through 3 fictional case studies (phishing email, fake shop, "you've won" text). Identify red flags, decide what to do, record reasoning on worksheet. |
| 45–53 min | Report back + debrief | Each group presents one case. Class votes on verdict before explanation. |
| 53–57 min | Where to get help | CERT NZ / Netsafe / bank fraud — students annotate a resource card |
| 57–60 min | Exit ticket | "Name one thing you'll do differently online after today." Peer-share, then collected. |

**Sheets:**
- **Sheet 5 — Bridge:** "Same Game, Different Medium" — fictional note vs. fictional phishing email, side by side (designed as a single visual comparison card)
- **Sheet 6 — Look–Check–Pause reference card:** Parallel to LFT; three-step framework with icon per step; printable pocket card
- **Sheet 7 — Case study worksheets:** 3 fictional scenarios with red-flag recording table; fillable digital / ruled lines print
- **Sheet 8 — Exit ticket + where to get help:** Reflection prompt + annotatable resource list

**Formative assessment:** Case study worksheets (collected) + exit ticket written reflection

---

## Fictional Screenshot Assets (to create)

Three assets needed for Lesson 2. All fictional — no real scam infrastructure, no real URLs:

| Asset | Description |
|-------|-------------|
| `fake-bank.png` | Fictional "PacificBank NZ" login page — subtle errors: wrong padlock, misspelled URL, urgency message |
| `scam-email.png` | Fictional email from "IRD.nz" claiming a tax refund — red flags: generic greeting, suspicious sender, urgent link |
| `fake-trademe.png` | Fictional "TradeYou NZ" listing — too-cheap iPhone, no seller rating, unusual payment method requested |

These are built as HTML mockups and screenshotted, or drawn directly in the HTML as styled divs (simpler, no external images needed).

---

## Site Structure

```
index.html
style.css
assets/
  fake-bank.png         (or inline styled div)
  scam-email.png        (or inline styled div)
  fake-trademe.png      (or inline styled div)

Overview
  ├── Karakia (bilingual — Whakataka te hau)
  ├── Whakataukī: "Ko tō ringa ki ngā rākau ā tō tīpuna" + translation
  ├── Learning Objectives (6, across both lessons)
  ├── Success Criteria (8)
  └── How to use these resources

Lesson 1 — Barter, Koha & Utu  [red theme]
  ├── Sheet 1: Context reference card
  ├── Sheet 2: Barter Simulation resource cards + debrief
  ├── Sheet 3: Graphic organiser
  └── Sheet 4: Exit ticket

Lesson 2 — Staying Safe Online  [blue theme]
  ├── Sheet 5: Bridge — "Same Game, Different Medium"
  ├── Sheet 6: Look–Check–Pause reference card
  ├── Sheet 7: Case study worksheets
  └── Sheet 8: Exit ticket + help resources
```

---

## Style Reference (TECS433_A1)

```css
--overview:       #1e4d5c   /* teal   — overview/context sections */
--lesson1:        #c0392b   /* red    — Lesson 1 (Barter, Koha & Utu) */
--lesson2:        #1a6b9a   /* blue   — Lesson 2 (Staying Safe Online) */
--support:        #7d3c98   /* purple — reference/support strips */
--bg:             #f8f8f6
--text:           #1a1a1a
```

Font: system font stack (no Google Fonts)
Layout: max-width 900px, centered
Components to carry over: sheet cards, reference strips (purple), key-question boxes (yellow/orange), karakia box (bilingual columns), per-sheet print buttons, `screen-only`/`print-only` classes, `contenteditable` inputs → ruled print lines

---

## Professional Commentary Plan (1000–1200 words)

### 1. Cultural Responsiveness (~250 words)
- Lesson 1 centres koha, utu, manaakitanga as primary lenses — not cultural add-ons
- Whakataukī *"Ko tō ringa ki ngā rākau ā tō tīpuna"* used meaningfully (connects ancestors' tools → today's digital tools)
- Barter simulation surfaces diverse student exchange experiences (Pacific, Asian, Middle Eastern, Māori, Pākehā)
- Lesson 2 digital safety framed around protecting whānau, not just individual transactions
- Reference: Bishop & Berryman (2009) Te Kotahitanga; Penetito (2010) on place-based culturally responsive pedagogy

### 2. Literacy Challenge (~200 words)
- Challenge: **subject vocabulary** — koha, utu, manaakitanga (Lesson 1); phishing, two-factor authentication, verification (Lesson 2)
- Support strategy: bilingual reference card Sheet 1; Look–Check–Pause as a vocabulary anchor; graphic organiser scaffolds structured comparison
- ELL and specialist literacy students: visual reference cards available throughout both lessons; group work reduces solo output pressure

### 3. Curriculum & Pedagogy (~350 words)
- **Culturally responsive pedagogy:** Lesson 1 structure, whakataukī, koha/utu as primary content
- **UDL:** Multiple representation (visual cards, text, simulation, discussion, case studies); multiple expression (graphic organiser, verbal debrief, written exit ticket); multiple engagement (competitive-collaborative simulation, investigation activity)
- **Cooperative learning:** Resource card simulation (group negotiation), case study groups (structured roles)
- **Inquiry / investigative learning:** Investigator framing in both lessons; students construct understanding through discovery before formalisation
- **Assessment for learning:** Exit tickets each lesson; teacher circulates and observes during simulation/case study; peer-share before collection

### 4. Critical Thinking (~300 words)
- Tension: financial literacy risks being purely transactional (better consumers) vs. critical (interrogating systems of power)
- Koha/utu discussion invites students to ask "who benefits from this exchange system?" — challenges purely capitalist framing
- Online safety raises the question of individual vs. platform vs. government responsibility for protection
- Both lessons position students as agents with tools, not passive recipients of rules
- Reference: Hung (2012) on critical financial literacy pedagogy; Kaupapa Māori theory (Smith, 1999)

---

## Build Order

1. `style.css` — copy TECS433_A1 CSS, update any fraction-specific components, keep all variables and print patterns unchanged
2. `index.html` — Overview section (karakia, whakataukī, objectives, criteria)
3. Lesson 1 sheets (Sheets 1–4)
4. Lesson 2 sheets (Sheets 5–8)
5. Fictional screenshot assets — build as inline styled HTML mockups within the page (avoids external images)
6. Print test each sheet — check `@media print` output
7. Host on GitHub Pages
8. Export full PDF (physical version) via browser print
9. Professional commentary (Word/Pages doc — separate from HTML)
