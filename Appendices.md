---

# Appendices

APPENDIX SCOPE LEGEND
[GB] Global Baseline — applies to all stages.
[SM-#] Stage-Mandatory — required when running Stage #.
[CA] Conditional Aid — consult when helpful; do not inline by default.

---

## [GB-1] CBSA General Guidelines
The Context-Based Significance Assessment (CBSA) method is a holistic, systematic approach to evaluating cultural heritage significance. It integrates both **physical** and **non-physical** aspects of a place and operates across multiple contexts — urban, landscape, historical, social, political, intangible heritage, thematic, and more. Central to CBSA is the **context effect**: values arise from context — the physical, historical, social, or thematic settings bestow meaning and importance on the asset. Conversely, when an asset is valued, its associated context also gains significance through that relationship. This reciprocal process is a key lens for interpreting and weighting values.


Key principles:
- **Holistic approach:** Values are interlinked; consider the place as a whole.
- **Evidence-based:** Always link values, contexts, and significance to tangible or documentary evidence.
- **Multiple perspectives:** Integrate professional, community, and stakeholder viewpoints.
- **Physical & Non-physical evidence:** Include material fabric, setting, and intangible associations.
- **Community involvement:** Engage local/community perspectives where possible.
- **Transparency:** Make reasoning explicit; document how conclusions are reached.
- **Engagement:** Use concise, vivid phrasing that remains evidence-grounded.

---

## [CA-V] Value Types and Definitions
Use plain words in outputs; avoid acronyms. Where relevant, adapt sub-categories.

- **Historical:** Association with past events, periods, people, or functions.  
- **Aesthetic:** Design, style, craftsmanship, materials, setting.  
- **Social:** Community attachment, use, cultural practices.  
- **Technological:** Construction methods or technical innovation embodied in fabric or process.  
- **Symbolic:** Represents identity, belief, collective meaning, emblematic forms.  
- **Landscape:** Contribution to wider visual / spatial / environmental setting.  
- **Scientific:** Potential for research, archaeological or archival study.  
- **Spiritual:** Religious or ritual significance.  
- **Environmental:** Ecological context, biodiversity, natural features.  
- **Urban:** Relationship to urban form, streetscape, spatial coherence.  
- **Mystery & Enigma:** Elements of uncertain origin/meaning that stimulate interpretation and cultural curiosity.  
- **Functional:** Continued or adapted practical use that sustains relevance.  
- **Educational:** Supports learning, interpretation, heritage awareness.  

### [CA-V-MAP] Value Types — Bilingual Mapping (EN ↔ HE)
| EN | HE |
| --- | --- |
| Aesthetic Value | ערך אסתטי |
| Landscape Value | ערך נופי |
| Urban Value | ערך אורבני |
| Historical Value | ערך היסטורי |
| Scientific Value | ערך מדעי |
| Social Value | ערך חברתי |
| Spiritual Value | ערך רוחני |
| Functional Value | ערך פונקציונלי |
| Symbolic Value | ערך סמלי |
| Environmental Value | ערך סביבתי |
| Mystery & Enigma | ערך מסתורין |
| Technological Value | ערך טכנולוגי |
| Educational Value | ערך חינוכי |
---

## [CA-C] Context Types
Geographic • Landscape • Urban • Historical • Social • Political • Technological • Environmental • Intangible Heritage • Thematic  
> Each selected context should be supported by evidence and linked to values.

### [CA-C-MAP] Context Types — Bilingual Mapping (EN ↔ HE)
| EN | HE |
| --- | --- |
| Geographic | הקשר גאוגרפי |
| Landscape | הקשר נופי |
| Urban | הקשר אורבני |
| Historical | הקשר היסטורי |
| Social | הקשר חברתי |
| Political | הקשר פוליטי |
| Technological | הקשר טכנולוגי |
| Environmental | הקשר סביבתי |
| Intangible Heritage | מורשת בלתי מוחשית |
| Thematic | הקשר תמאטי |

---

## [CA-T] Change Types (lexicon)
Fabric • Infrastructure • Use • Setting • Interpretation  
> Use inside the last column of the unified Stage-2 table only when it clarifies the consequence.

---

## [SM-3] Integrity & Nara Grid Guidance
**Template columns:** Aspect | Description | Value Expression | Condition  
**Notes:** Compare current vs. original; cite specific attributes; tie condition back to Stage-2 values; explain briefly how any loss affects the value’s expression; avoid technical prescription.

---

## [CA-E] Examples & Phrasing Aids
**Comparative claims:** “Representative of… / Rare for… / Earliest example of…”  
**Consequence stems:** “Reduces legibility of… / Diminishes landmark presence… / Obscures original volume…”  
**Integrity phrasing:** “Later accretions partially obscure… / Original profile remains legible despite…”

---

## [CA-CS] Comparative Significance Criteria
Use these criteria in Stage 4 (Comparative Evaluation) and Stage 5 (Significance Statement) to support professional judgments.

- **Period:** Represents a significant era or phase in history.  
- **Rarity:** Few comparable examples exist locally, regionally, or nationally.  
- **Documentation:** Well-recorded in archives, plans, photographs, or oral histories.  
- **Connection to Ensemble:** Contributes to a group of related sites or features.  
- **Condition:** Degree of preservation of original fabric or setting.  
- **Selectivity/Diversity:** Contributes to the diversity of heritage types represented.  
- **Research Potential:** Holds potential for further scholarly, scientific, or archaeological study.

---
## [CA‑IMG] Image Analysis Aid (optional)
Purpose: derive contexts, physical features, condition, values, and comparatives from images provided by the user.
Output (when asked to analyze an image):
- Values spotted (with evidence in the image)
- Condition notes (materials, damage, alterations)
- Relevant contexts (time/place/setting)
- Quick comparatives (same type/period)
- Follow‑ups: what extra shot or doc would clarify

---
## [CA-EC] Entity Categories (EN ↔ HE)
Use these for KG node category selection when relevant to the site.

| EN | HE |
| --- | --- |
| Place | מקום |
| Structure / Building | מבנה |
| Architectural Element | אלמנט אדריכלי |
| Person | דמות |
| Event | אירוע |
| Story / Narrative | סיפור / נרטיב |
| Cultural Value | ערך תרבותי |
| Natural Phenomenon | תופעה טבעית |
| Artwork / Artefact | יצירת אמנות / ממצא |
| Tradition / Custom | מסורת / מנהג |
| Social Group | קבוצה חברתית |
| Historical Period | תקופה היסטורית |
| Religion / Belief | דת / אמונה |
| Collective Memory | זיכרון קולקטיבי |

---
# [CA‑KG] Knowledge Graph — EN Scheme with **Value** as Entity (External + Embedded Fallback)

This section defines the **entire KG feature** for the workshop materials, in English, while preserving the **Hebrew color concept**.  
Key change: **Values are first‑class entities**. All nodes of type **“Cultural Value”** (short: **“Value”**) share one color and use the label pattern:  
`Value: <value name> [<value type>]` (e.g., `Value: Pilgrimage [Social]`).

---

## 1) Data Schema (strict)

**DATA = { "nodes": [...], "edges": [...] }**

**Node (required fields):**
- `id` — unique integer or string
- `name` — visible label text in the user’s language
- `type` — **English** category from **[CA‑EC]** (see list below). For value entities use **`"Cultural Value"`** (or `"Value"`; both accepted).
- `meaning` — 5–12 words describing why this node matters (site‑specific)

**Optional node fields (recommended for Value nodes):**
- `value_type` — one of **[CA‑V]**: Historical, Aesthetic, Social, Technological, Symbolic, Landscape, Scientific, Spiritual, Environmental, Urban, Mystery & Enigma, Functional, Educational.
- `color` — overrides palette if needed (object with `background`, `border`).

**Edge (required fields):**
- `from` — source node `id`
- `to` — target node `id`
- `label` — relationship verb (localized to user language). Suggested verbs: `located_in`, `part_of`, `associated_with`, `expresses_value`, `used_by`, `influenced_by`, `commemorates`, `built_by`, `represents`, `related_to`.

**Validation checks before rendering:**
- All `id` values unique.
- Every edge `from`/`to` exists in `nodes`.
- No empty `meaning` fields.
- `type` drawn exactly from **[CA‑EC]** list below (English).  
  For values, use `Cultural Value` (or `Value`); both map to the same styling/logic.
- If localizing fully, keep `type_original` for internal English type (optional).

---

## 2) Localization Rules
- Node `name` and edge `label` mirror the **user’s current language** (EN/HE).  
- Node `type` remains in **English** (controlled vocabulary), even in Hebrew UI.  
- Set `<html lang="en">` for English; add `dir="rtl"` only for Hebrew/Arabic pages.

---

## 3) English Color Palette (Hebrew concept, 1 color for all “Value” nodes)

| Type (EN)               | Background (rgba)      | Border (hex) |
|-------------------------|------------------------|--------------|
| Natural Phenomenon      | rgba(30,144,255,0.7)   | #1E90FF      |
| Structure / Building    | rgba(178,34,34,0.7)    | #B22222      |
| Architectural Element   | rgba(129,199,132,0.7)  | #81C784      |
| Person                  | rgba(255,105,180,0.7)  | #FF69B4      |
| Event                   | rgba(255,160,122,0.7)  | #FFA07A      |
| Story / Narrative       | rgba(255,228,181,0.7)  | #FFE4B5      |
| Social Group            | rgba(255,215,0,0.7)    | #FFD700      |
| **Cultural Value / Value** | **rgba(255,193,7,0.7)** | **#FFC107**  |
| Place                   | rgba(100,149,237,0.7)  | #6495ED      |
| Artwork / Artefact      | rgba(128,0,128,0.7)    | #800080      |
| Tradition / Custom      | rgba(139,69,19,0.7)    | #8B4513      |
| Historical Period       | rgba(0,180,180,0.7)    | #00B4B4      |
| Religion / Belief       | rgba(218,112,214,0.7)  | #DA70D6      |
| Collective Memory       | rgba(75,0,130,0.7)     | #4B0082      |
| General (fallback)      | rgba(200,200,200,0.6)  | #666666      |

> The **Value** color is unified. Non‑value types follow the palette above.

---

## 4) Entity Type List (English) — [CA‑EC]
Place • Structure / Building • Architectural Element • Person • Event • Story / Narrative • Cultural Value (Value) • Natural Phenomenon • Artwork / Artefact • Tradition / Custom • Social Group • Historical Period • Religion / Belief • Collective Memory

---

## 5) LLM Interpretation Notes (MUST)
When interpreting assessment text:
1. **Values are entities** → create nodes with `type: "Cultural Value"` and `value_type: "<one of [CA‑V]>"`.  
2. Prefer concise `name` (≤3 words): e.g., “Pilgrimage”, “Craftsmanship”, “Byzantine Mosaic”.  
3. Put the *why it matters* into `meaning` (5–12 words).  
4. Connect assets to values via `expresses_value` (Structure → Value), communities via `used_by`/`associated_with`, and contexts via `located_in`/`part_of`/`influenced_by`.  
5. If the source text is ambiguous, include the **⚠️ Running with missing data** banner before HTML.

---

## 6) **External** HTML (uses external JS + CSS)
> Save your data JSON into the placeholder `__DATA_JSON__`.  


```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Knowledge Graph</title>
  <link rel="stylesheet"
        href="https://alephplace.com/atar.bot/canvas/knowledge-graph.css"
        crossorigin="anonymous" />
  <script src="https://unpkg.com/vis-network/standalone/umd/vis-network.min.js"></script>
</head>
<body>
  <div id="mynetwork"></div>

  <div id="infowindow" style="display:none;text-align:left;max-width:260px">
    <span id="closeinfo" style="float:right;cursor:pointer;font-weight:bold">✖</span>
    <h3 id="info_name"></h3>
    <p><strong>Type:</strong> <span id="info_type"></span></p>
    <p><strong>Meaning:</strong> <span id="info_meaning"></span></p>
  </div>

  <script>
    const DATA = __DATA_JSON__;
  </script>
  <script src="https://alephplace.com/atar.bot/canvas/knowledge-graph.js"></script>
</body>
</html>
```

---

## 7) **Embedded Fallback** HTML (no external JS required)
> Paste this if the external file cannot be loaded. Same behavior, including unified **Value** color and label format.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Knowledge Graph (Embedded)</title>
  <script src="https://unpkg.com/vis-network/standalone/umd/vis-network.min.js"></script>
  <style>
    body, #mynetwork, #infowindow { font-family: Calibri, system-ui, sans-serif; }
    #mynetwork { width: 100%; height: 600px; border: 1px solid #ddd; }
    #infowindow {
      display:none; position:absolute; background:#fff; border:1px solid #ccc; padding:10px;
      box-shadow:2px 2px 10px rgba(0,0,0,0.15); text-align:left; max-width:260px; z-index:10;
    }
    #closeinfo { float:right; cursor:pointer; font-weight:bold; }
  </style>
</head>
<body>
  <div id="mynetwork"></div>

  <div id="infowindow">
    <span id="closeinfo">✖</span>
    <h3 id="info_name"></h3>
    <p><strong>Type:</strong> <span id="info_type"></span></p>
    <p><strong>Meaning:</strong> <span id="info_meaning"></span></p>
  </div>

  <script>
    /* ---------- Provide DATA here ---------- */
    const DATA = __DATA_JSON__;

    /* ---------- Color palette (EN) ---------- */
    const COLOR_BY_TYPE = {
      'Natural Phenomenon':   { background: 'rgba(30,144,255,0.7)',  border: '#1E90FF' },
      'Structure / Building': { background: 'rgba(178,34,34,0.7)',   border: '#B22222' },
      'Architectural Element':{ background: 'rgba(129,199,132,0.7)', border: '#81C784' },
      'Person':               { background: 'rgba(255,105,180,0.7)', border: '#FF69B4' },
      'Event':                { background: 'rgba(255,160,122,0.7)', border: '#FFA07A' },
      'Story / Narrative':    { background: 'rgba(255,228,181,0.7)', border: '#FFE4B5' },
      'Social Group':         { background: 'rgba(255,215,0,0.7)',   border: '#FFD700' },
      'Cultural Value':       { background: 'rgba(255,193,7,0.7)',   border: '#FFC107' },
      'Value':                { background: 'rgba(255,193,7,0.7)',   border: '#FFC107' },
      'Place':                { background: 'rgba(100,149,237,0.7)', border: '#6495ED' },
      'Artwork / Artefact':   { background: 'rgba(128,0,128,0.7)',   border: '#800080' },
      'Tradition / Custom':   { background: 'rgba(139,69,19,0.7)',   border: '#8B4513' },
      'Historical Period':    { background: 'rgba(0,180,180,0.7)',   border: '#00B4B4' },
      'Religion / Belief':    { background: 'rgba(218,112,214,0.7)', border: '#DA70D6' },
      'Collective Memory':    { background: 'rgba(75,0,130,0.7)',    border: '#4B0082' }
    };
    const FALLBACK_COLOR = { background: 'rgba(200,200,200,0.6)', border: '#666666' };

    /* ---------- Normalize node + build label ---------- */
    const normalizeType = t => {
      if (!t) return 'General';
      const s = String(t).trim();
      return (s.toLowerCase() === 'value' || s.toLowerCase() === 'cultural value') ? 'Cultural Value' : s;
    };

    DATA.nodes.forEach(n => {
      n.type = normalizeType(n.type);
      // Label rule: Value nodes use "Value: <name> [<value_type>]"
      if (n.type === 'Cultural Value') {
        const vt = n.value_type ? String(n.value_type) : '—';
        n.label = `Value: ${n.name} [${vt}]`;
      } else {
        n.label = n.name || '';
      }
      const col = COLOR_BY_TYPE[n.type] || FALLBACK_COLOR;
      n.color = n.color || { background: col.background, border: col.border };
      // Small box nodes for legibility
      n.shape = 'box';
    });

    /* ---------- Build vis datasets ---------- */
    const nodes = new vis.DataSet(DATA.nodes);
    const edges = new vis.DataSet(DATA.edges);
    const container = document.getElementById('mynetwork');

    const options = {
      nodes: {
        font: { align: 'center', size: 14, color: '#333' },
        borderWidth: 1,
        margin: { top: 8, right: 10, bottom: 8, left: 10 },
        widthConstraint: { maximum: 180 }
      },
      edges: {
        arrows: { to: { enabled: true, scaleFactor: 0.4 } },
        font: { align: 'middle', size: 11, color: '#555', background: 'white' },
        smooth: { type: 'cubicBezier', forceDirection: 'horizontal', roundness: 0.5 },
        color: { color: '#848484', highlight: '#333', hover: '#555', inherit: false }
      },
      layout: { improvedLayout: true },
      physics: {
        enabled: true,
        solver: 'repulsion',
        repulsion: { nodeDistance: 230, centralGravity: 0.05, springLength: 20, springConstant: 0.005, damping: 0.09 },
        stabilization: { iterations: 2000, fit: true }
      },
      interaction: { hover: true, tooltipDelay: 300 }
    };

    const network = new vis.Network(container, { nodes, edges }, options);

    /* ---------- Info window ---------- */
    const info = document.getElementById('infowindow');
    const closeInfo = () => info.style.display = 'none';
    document.getElementById('closeinfo').addEventListener('click', closeInfo);
    document.addEventListener('keydown', e => { if (e.key === 'Escape') closeInfo(); });

    network.on('click', params => {
      if (params.nodes.length) {
        const node = nodes.get(params.nodes[0]);
        document.getElementById('info_name').innerText = node.name || node.label || '';
        document.getElementById('info_type').innerText = node.type || '';
        document.getElementById('info_meaning').innerText = node.meaning || '';
        info.style.left = params.pointer.DOM.x + 'px';
        info.style.top = params.pointer.DOM.y + 'px';
        info.style.display = 'block';
      } else {
        closeInfo();
      }
    });
  </script>
</body>
</html>
```

---

## 8) Minimal Sample DATA (Tabgha-style, EN, with a Value node)
```json
{
  "nodes": [
    { "id": 1, "name": "Tabgha Site", "type": "Place", "meaning": "Historic lakeside location in northern Israel" },
    { "id": 2, "name": "Church of the Multiplication", "type": "Structure / Building", "meaning": "Modern church over early Byzantine remains" },
    { "id": 3, "name": "Mosaic Floor", "type": "Architectural Element", "meaning": "Fifth-century fish and loaves mosaic panel" },
    { "id": 4, "name": "Christian Pilgrims", "type": "Social Group", "meaning": "Visitors seeking spiritual reflection" },
    { "id": "v1", "name": "Pilgrimage", "type": "Cultural Value", "value_type": "Social", "meaning": "Living devotional practice connecting site and believers" }
  ],
  "edges": [
    { "from": 2, "to": 1, "label": "located_in" },
    { "from": 3, "to": 2, "label": "part_of" },
    { "from": 4, "to": 2, "label": "used_by" },
    { "from": 2, "to": "v1", "label": "expresses_value" }
  ]
}
```

---

### Notes
- The **external** and **embedded** versions are functionally equivalent. Use the external one by default; fall back to the embedded block if hosting the JS is not possible.
- The renderer normalizes `type: "Value"` → `"Cultural Value"` automatically to apply the unified color and label rule.


Authoring Steps (single pass):
1. Collect raw entities & candidate values from user text.
2. Create Cultural Value nodes (dedupe by meaning).
3. Assign expresses_value edges from each entity to ≥1 value.
4. Add structural/context edges (located_in, part_of, etc.).
5. Fill/trim meanings (5–15 words); validate all rules.
6. Generate HTML by injecting JSON.stringify(DATA) into template.

Diff Guidance: When suggesting edits mid‑conversation, show only altered node/edge lines in a fenced diff block (≤40 changed lines).

