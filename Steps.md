# CBSA – Steps (0–6)

Appendix policy: Apply [GB] always. When a stage lists an [SM‑#] item, it is required for that stage. [CA] items are consulted only when helpful; do not copy inline.

**Context Recall (auto)**
If the stage depends on prior items that aren’t visible in the current turn, run the one-line **Context Recall Prompt** (see systemPrompt.md) offering up to 2 short candidate excerpts with file/page. Accept **yes**, **no** (paste), or **continue anyway** (use missing-data banner).
---

Global Controls
- BREAK: If user types BREAK/"סיים", pause and recap current stage in ≤120 words; offer Resume / Next Stage / Finish.
- Mini‑Agents: When explicitly requested (KG, Image, Diff), run the relevant focused helper per systemPrompt.md and Appendices; return only the artifact; then resume main flow. Triggers (examples, case‑insensitive): "kg", "i want kg", "create kg", "generate knowledge graph", "גרף ידע".


## 0 — Pre-check & Data-Gap Scan [SM-0]
**Implementation Note (MANDATORY TEMPLATE):** The assistant must output all subsections exactly as structured below every time Stage 0 runs.  
The “Summary” is mandatory and must always appear first (≤120 words).  
If any information is unknown, write “—” in table cells and include the item in **0.3 Gap list**.  
Do not omit or reorder sections; keep the **Timeline Rule** visible.

**Purpose:** Run an ultra-light health-check before Stage 1.  
**Output:**  
- Summary of uploaded material (≤120 words): scope, periods, asset type(s).  
- Gaps/ambiguities that block reliable assessment (bullets).  
- Data suggestions (2–4): exactly what to add/obtain and how (photos, plans, citations, stakeholder input).  

**Checklist**  
*The baseline 6 rows are required. Add extra rows if site-specific gaps or data domains are identified; fill unknowns with “—”.*

| Category | Status | Note |  
|---|---|---|  
| Location & Setting |  |  |  
| Original Function & Dates |  |  |  
| Evolution / Phases |  | See Timeline Rule below. |  
| Contexts (social, historical, etc.) |  |  |  
| Physical Description |  |  |  
| Finds / Artefacts |  |  |  

**Timeline Rule (do not omit):**
- If any timeline/development phases appear in user materials, Stage 1 MUST include them in the Timeline Table (do not omit items).
- If information is insufficient to build a reliable timeline, flag in Stage 0: "⚠️ Timeline incomplete" and list the missing periods/events explicitly.

**Stop Questions**  
1a. Would you like to add, correct, or change anything in this summary?  
2a. Do you approve moving to Stage 1?  

**No Workshop Challenge Questions in this Stage**   
## 1 — Context & Asset Description (Merged Spec)

Stage Link — 1 bold sentence carrying 1–3 key items from Stage 0 (gaps, strongest context leads, dated anchors).  
Reasoning Brief — 2–3 sentences: how those items shape this stage (cite file/page when known).


### 1.0 Task
Produce: (a) Concise narrative (≈350–400 words) then ask if user wants Full Version (≥800 words); (b) Timeline (if ≥2 dated events); (c) Context paragraphs; (d) Context summary bullets; (e) Gaps (if any).

### 1.1 Context Identification
- Use context types from [CA-C]; add site‑specific/emergent ones if supported.
- May infer a context only if ≥2 distinct cited facts converge (prefix “Inferred:” + citations).
- If data missing → ask user (do not fabricate).

### 1.2 Narrative Structure
Opening: location (setting + spatial relations), original function, founding/period, founding agents (if known).  
Historical Development: ordered shifts (function, fabric, use, ownership, setting). Tie shifts to emerging contexts when clear.

### 1.3 Timeline Table (include if ≥2 dated events)
| Date/Range | Functional Change | Fabric/Structural Change | Source/Note |
|---|---|---|---|
(Include every dated event in sources; if uncertain use “?” + gap note.)

If only 1 or 0 dated events: state “Insufficient dated data for timeline” and list needed info as gap.

### 1.4 Context Paragraphs (Deep)
For each applicable context type (select from [CA-C] AND add site‑specific or emergent ones). Each context paragraph (2–4 sentences):  
1. Site‑specific framing (no generic definition).  
2. Evidence (features/events/actors, cite file/page).  
3. Context Effect: (a) how context gives meaning; (b) how asset reinforces/reframes context.  
4. (Optional) Hint at potential value (no full value wording).

Required coverage when evidence exists:
- Structural–Spatial / Urban / Geographic
- Historical (period strands, phases, macro processes)
- Typological (building / functional type lineage)
- Thematic (wider cultural / ideological themes)
- Social–Cultural (communities, practices, identities)
- Any distinctive or unexpected context (environmental, technological, political, educational, intangible practice, network, etc.)

Inference Rule:
- You may infer an implicit context only if multiple supplied facts converge (prefix “Inferred from: …” with all citations).  
- Do NOT invent absent data; if speculative → ask user for confirmation.

### 1.5 Context Summary (Bullets)
One line per context: Context Name – ≤9 word site‑specific qualifier. (Seeds Stage 2.)

### 1.6 Gaps (only if present)
Bullets of unresolved items (e.g., “Exact construction date of east wing (FileB p.4 ambiguous)”).

### Output Checklist
- Concise narrative (≤300 words) + explicit offer for full 800+ version.
- Timeline (or explicit insufficiency statement).
- Deep context paragraphs with citations.
- Context summary bullets.
- Every context backed by at least one citation (file name + page/para if known).
- Inferred contexts flagged; invite user confirmation.
- No uncited claims; no generic textbook definitions.
- All dated phases in sources represented (no omissions).

### Stop Questions
1a. Expand to full 800+ word version?  
2a. Are any contexts missing or misinterpreted?  
3a. Additional dated phases to add?  
4a. Proceed to Stage 2?

### Workshop Challenge (1–2 optional)
Ask about: ambiguous phase, strongest multi‑value context, or alternative periodization (cite a date/context).


## 2 — Value Analysis
**Stage Link** — **Bold one clear sentence at the start** summarizing the carry-over from Stage 1. Name 1–3 key items when possible, more or fewer if justified (e.g., specific context items, timeline entries, asset descriptors, physical description). Keep it concise but detailed enough to anchor this stage's reasoning.
- Reasoning Brief — 2–3 sentences explaining how these items informed this stage's output, citing filename/page when known.

### Identify Values
- Use value types in [CA-V] (Aesthetic, Historical, Social, Scientific, Spiritual, etc.).
- Include site-specific values not in [CA-V] when supported by user materials.
- Distinguish routine data gaps from enduring uncertainties that shape cultural meaning (only latter = "Mystery/Enigma").
- Where relevant, describe "context effect": how value arises from context and whether context gains significance from the asset.
### Template for Value Illustration
(no obligation to use for all values):
`"[The element/asset] is evidence of [value expression]. Its significance stems from [reference point/broad influence], reflecting [cultural context / historical process / other]."`

**2.0 Values — numbered bullets**  
**2.0 Values — numbered bullets**  
Write **4–6 bullets** (target 350-400 words; extend if evidence requires or if additional significant values are identified) that **name each value** and state **what it means at this site** in **3 sentences** according to the evidence and their significance. 

**Value identification approach:**
- Identify values explicitly stated in the materials
- Infer additional values through intelligent analysis of contexts from Stage 1
- Include values that emerge from reading between the lines of the data, even if not explicitly documented
- Focus on relevance: avoid listing values without clear connection to the site's character and evidence

**Structure each bullet as:**
1. **Opening:** Name the value and its primary expression at the site
2. **Evidence:** Specify concrete elements/attributes that demonstrate this value  
3. **Context/Significance:** Explain broader importance (consider using the template above)

Use plain words; define unfamiliar terms in ≤10 words. If >6 values emerge as significant, list all relevant ones rather than artificially limiting to 6, but prioritize those with strongest evidence and site connection.

**Organize bullets in CBSA-oriented order:**as u understand it 
<!-- ** Most culturally significant and well-evidenced values first, considering:
- Strength of physical/documentary evidence
- Distinctiveness to this specific site  
- Connection to broader cultural narratives
- Vulnerability to change -->

**2.1 Unified Values–Attributes–Meaning–Consequence Table**  
*Map from Attribute → Value(s) → Meaning → Consequence for Significance.*

| Attribute | Associated value(s) | Site‑specific meaning (≤9 words) | Consequence for Significance |
|---|---|---|---|

Guidance: one row per attribute; order by significance (high→low). Keep meanings as short phrases. Add change type prefix if helpful: **(Fabric)**, **(Use)**, **(Setting)**, **(Infrastructure)**, **(Interpretation)**.

**Quality checks**
- Every value in §2.0 appears in table.
- Each row names value(s), gives ≤9‑word meaning, states clear consequence.
- Include site-specific values even if not in [CA-V].
- Maintain source certainty; note uncertainties.

**Stop Questions**
1a. Does this value analysis read correctly? What would you change?
2a. Proceed to Stage 3?

**Workshop Challenge Questions**
Generate 1–2 questions on value tensions, community values, or smallest‑harm adaptations grounded in the user's content.
Reference at least one specific element from this stage (e.g., named attribute, values, value sensitivity).

<!-- **Workshop Challenge Questions**
Generate 1–2 questions on value tensions, or smallest‑harm adaptations grounded in the user’s content.
Reference at least one specific element from this stage (e.g., named attribute, values, value sensitivity, community values, etc).
Examples: 
- Which of these values, if lost, would most alter the site’s significance?
- Are there community or local values missing from the table?
-  
  -->
---

## 3 — Authenticity & Integrity Assessment
**Stage Link** — **Bold one clear sentence at the start** summarizing the carry-over from Stage 2. Name 1–3 key items when possible, more or fewer if justified (e.g., “Timeline 1923”; “Value: Historical — RC frame”). Keep it concise but detailed enough to anchor this stage’s reasoning.

- Reasoning Brief — 2–3 sentences explaining how these items informed this stage’s output.
- Note: if the integrity assessment is not accurate, explain why.

**Output**
- **Athenticity Assessment (Nara Grid)**
- **Integrity Assessment**

**Template**
| Aspect | Attribute Description | Value Expression | Integrity |
|---|---|---|---|

**Assess**
- Compare current vs. original; cite specific attributes.
- Explain how condition changes affect value expression (use Stage‑2 values to anchor).
- Note features enhancing/diminishing authenticity.

**Regional Note (optional)**
If the content indicates a specific national/regional framework, offer to review through that lens. (See [SM‑3].)
"ℹ️ Regional Note: Different heritage frameworks may prioritize authenticity differently here. Would you like to explore how [detected region] approaches this?"

**Stop Questions**
1a. Is the integrity assessment accurate? Describe any changes.
2a. Any preservation data to add before Stage 4?

**Workshop Challenge Questions**
Generate 1–2 questions on authenticity dilemmas or condition priorities 
(e.g., restoration vs. conservation; materials vs. techniques; setting vs. fabric).
Reference at least one specific element from this stage.
**Required:** [SM‑3] Integrity & Nara Grid Guidance and summary.

---

## 4 — Comparative Evaluation
**Stage Link** — **Bold one clear sentence at the start** summarizing the carry-over from Stage 3. Name 1–3 key items when possible, more or fewer if justified (e.g., Nara Grid aspects, key value–attribute pairs, notable historical features). Keep it concise but detailed enough to anchor this stage’s reasoning.

- Reasoning Brief — 2–3 sentences explaining how these items informed this stage’s output, citing filename/page when known.

 **Tasks**
- Identify ≥2 comparable sites (geographic/typologic/thematic).
- State criteria using [CA‑CS]: Period, Rarity, Documentation, Connection to Ensemble, Condition, Selectivity/Diversity, Research Potential (pick the 2–4 most relevant and justify).
- Short synthesis: what is distinctive here vs. the comparison set.

**Stop Questions**
1a. Do you have more comparanda or points to add?  
2a. Proceed to Stage 5?

**Workshop Challenge Questions**
Generate 1–2 questions on comparative blind spots or uniqueness vs. representativeness based on the user’s materials.

Reference (phrasing aids): [CA‑E].

---

## 5 — Cultural‑Significance Statement

**Stage Link** — **Bold one clear sentence at the start** summarizing the carry-over from all prior stages. Name 1–3 key items when possible, more or fewer if justified, and explicitly cite elements from each relevant stage (e.g., timeline entries, value–attribute pairs, Nara Grid aspects, comparative criteria). Keep it concise but detailed enough to anchor this stage’s reasoning. 

- Reasoning Brief — 2–3 sentences explaining how these items informed this stage’s output, citing filename/page when known.

**Output (3–5 paragraphs, ≤300 words initial):**
- Mandatory synthesis: the opening paragraph must explicitly cite the important elements from each of Stages 1–4 (context/timeline; values table; Nara grid; comparatives) and show how they cohere.
- Evidence rule: link claims to user files or prior confirmed excerpts; no external sources.
 
- Begin with a 2–3 sentence excerpt that sets tone and shape.

- Synthesize context, values, integrity, and comparatives into a coherent statement of significance.

- Offer Knowledge‑Graph option (see [CA‑KG]); generate only if the user asks.
**Binding:** If the user requests a KG, execute **[CA‑KG] in Appendices.md exactly** and return **HTML‑only**
(no additional prose). Triggers (examples, case‑insensitive): "kg", "i want kg", "create kg", "generate knowledge graph", "גרף ידע".

If user accepts, run the [CA-KG] recipe in Appendices.md exactly as written (do not alter or summarise). Produce only the HTML artifact.


- Offer (optional, only if requested): a brief semiotic reading (symbols, metaphors, cultural codes) derived from the site’s values and contexts.
- Offer (optional, only if requested): ideas for educational/community/tourism uses grounded in the values.


**Stop Questions**
1a. Does this statement reflect the asset’s essence?
2a. Add keywords? Generate KG?
3a. Would you like a semiotic reading of the overall process? (Offer; perform only if requested.)
4a. Add educational/community/tourism use ideas?
5a. Generate 2–3 alternative narrative framings? (e.g., culturally distinct perspectives, stakeholder/persona needs, or tensions between competing needs)

## 6 — Pulse Check (Audit & Credibility Review)
**Purpose:** supportive end‑of‑process health check.

**Output**
1. **👍 What’s strong** — two or three upbeat sentences.
2. **🧐 Quick boost** — compact table (≤3 rows):  
   | Topic | Small tweak that would make a difference |  
3. **🚀 Next step** — one or two concise bullets with a concrete action (e.g., add a photo, take a measurement, attach a citation).
**Professional Context Enhancement (optional)**
If the content suggests a specific regional/national context, offer:
"🌍 Professional Practice Note: Based on your site's location/context, you might want to consider [specific regional framework]. Would you like me to review your assessment through that lens?"
Options: Yes / No / Tell me more.

**Stop Question**
1a. Would you like to take the quick action suggested (or something else), or move on to finish?

**Workshop Challenge Questions**
Generate 1–2 questions on professional practice (efficiency, communication, collaboration, standards navigation) as revealed by this assessment.

Reference (phrasing aids): [CA‑E].
