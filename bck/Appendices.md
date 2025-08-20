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

## [CA-KG] Knowledge Graph Recipe (optional at Stage 5)
Use this recipe when the user asks for a KG; otherwise only offer it. Visible labels mirror the user’s language; internal JSON keys remain in English.

Purpose: Generate an evidence-based Knowledge Graph (KG) from user‑supplied entities and relationships. Output = standalone HTML only (no extra prose).

Triggers:
- User explicit request: “Create KG / Generate knowledge graph / צור גרף ידע”.
- Mini-Agent invocation (see System Prompt).
Otherwise: at Stage 5 only OFFER (do not auto-generate).

Human-in-the-Loop (recommended):
1. List candidate nodes & edges (plain JSON) for approval.
2. After user confirms (or says “continue anyway”), produce final HTML.

Data Schema:
- DATA = { "nodes": [...], "edges": [...] }
- Node fields (all required): id (unique), name, type, meaning (5–12 words).
- Edge fields (all required): from (node id), to (node id), label (relationship verb).
- Escape rule: const DATA = __DATA_JSON__; where __DATA_JSON__ is JSON.stringify(DATA).

Localization Rule (IMPORTANT):
- Node name: user’s current language (local).
- Edge label: user’s current language (local).
- Node type: ALWAYS in English (controlled vocabulary from [CA-EC]) for consistency & downstream tooling.
- Internal JSON keys: English.
- HTML tag: <html lang="xx">; add dir="rtl" when language is Hebrew/Arabic.
- If user explicitly requests fully localized types, provide bilingual “Type (סוג)” but keep an English version inside type_original (optional extension).

Common Relationship Verbs (use those that fit; localize labels): located_in, part_of, associated_with, expresses_value, used_by, influenced_by, commemorates, built_by, represents, related_to.

Validation Checklist BEFORE HTML:
- All ids unique.
- Every edge references existing node ids.
- No empty meaning fields.
- Types drawn from [CA-EC] exactly (English).
- User approval obtained OR user explicitly waived.

Missing Data Handling:
If critical elements absent (e.g., <2 nodes, no edges, or missing meanings) show banner “⚠️ Running with missing data.” Ask for:
- List of core entities (name + type + meaning).
- At least one relationship verb connecting them.

Sample DATA Object (Tabgha example):
```json
{
  "nodes": [
    { "id": 1, "name": "Tabgha Site", "type": "Place", "meaning": "Historic lakeside location in northern Israel" },
    { "id": 2, "name": "Church of the Multiplication", "type": "Structure / Building", "meaning": "Modern church over early Byzantine remains" },
    { "id": 3, "name": "Mosaic Floor", "type": "Architectural Element", "meaning": "Fifth-century fish and loaves mosaic panel" },
    { "id": 4, "name": "Christian Pilgrims", "type": "Social Group", "meaning": "Visitors seeking spiritual reflection" }
  ],
  "edges": [
    { "from": 2, "to": 1, "label": "located_in" },
    { "from": 3, "to": 2, "label": "part_of" },
    { "from": 4, "to": 2, "label": "used_by" }
  ]
}
```

Master HTML Template (Do Not Modify):
```html
<!DOCTYPE html>
<html lang="he" dir="rtl">
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

  <div id="infowindow" style="display:none;direction:rtl;text-align:right">
    <span id="closeinfo" style="float:left;cursor:pointer;font-weight:bold">✖</span>
    <h3 id="info_name"></h3>
    <p><strong>סוג:</strong> <span id="info_type"></span></p>
    <p><strong>משמעות:</strong> <span id="info_meaning"></span></p>
  </div>

  <script>
    const DATA = __DATA_JSON__;
  </script>
  <script src="https://alephplace.com/atar.bot/canvas/knowledge-graph.js"></script>
</body>
</html>
```
