# Appendices

APPENDIX SCOPE LEGEND
[GB] Global Baseline — applies to all stages.
[SM‑#] Stage‑Mandatory — required when running Stage #.
[CA] Conditional Aid — consult when helpful; do not inline by default.

## [GB‑1] CBSA General Guidelines
• Use only user‑supplied sources; cite filename + page/para when known.  
• Localization: mirror the user’s language for all visible UI text.  
• HIL: never proceed without explicit approval; show missing‑data banner + 2–4 ways to obtain.  
• Chaining: start each stage with Stage Link; end with Reasoning Brief.  
• DQR footer: Workshop → Stop (approval).  
• Visual aids: include only when they improve clarity for the stage.

## [CA‑V] Value Types (natural words)
Historical • Aesthetic • Social • Technological • Symbolic/Landscape • Scientific • Spiritual • Environmental • Urban • Mystery/Enigma  
Tip: prefer plain words in outputs; avoid acronyms or internal codes.

## [CA‑C] Context Types
Geographic • Landscape • Urban • Historical • Social • Political • Technological • Environmental • Intangible Heritage • Thematic

## [CA‑T] Change Types (lexicon)
Fabric • Infrastructure • Use • Setting • Interpretation  
Use inside the last column of the unified Stage‑2 table only when it clarifies the consequence.

## [SM‑3] Integrity & Nara Grid Guidance
Template columns: Aspect | Description | Value Expression | Condition  
Notes:  
• Compare current vs. original; cite specific attributes.  
• Tie condition back to Stage‑2 values (explain how any loss affects expression).  
• Avoid technical prescriptions unless explicitly requested. Phrase clearly for non‑specialists.

## [CA‑E] Examples & Phrasing Aids
Comparative claims: “Representative of … / Rare for … / Earliest example of …”  
Consequence stems: “Reduces legibility of … / Diminishes landmark presence … / Obscures original volume …”  
Integrity phrasing: “Later accretions partially obscure … / Original profile remains legible despite …”

## [CA‑KG] Knowledge Graph Recipe (optional at Stage 5)
Use this recipe when the user asks for a KG; otherwise only offer it.

### 1) Build DATA (nodes/edges)
Nodes (each): id, name, type, meaning (visible labels mirror user language; internal keys remain English).  
Edges (each): from, to, label.  
Escape rule: run JSON.stringify(DATA) before embedding.

### 2) Embed DATA into the HTML template
Replace __DATA_JSON__ with JSON.stringify(DATA).

### 3) Set locale
Set <html lang> and, for RTL languages, dir="rtl"; otherwise omit dir or set dir="ltr".

### Knowledge Graph — HTML Template (Do Not Modify other than inserting DATA and lang/dir)
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

  <div id="infowindow" style="display:none;">
    <span id="closeinfo" style="float:right;cursor:pointer;font-weight:bold">✖</span>
    <h3 id="info_name"></h3>
    <p><strong>Type:</strong> <span id="info_type"></span></p>
    <p><strong>Meaning:</strong> <span id="info_meaning"></span></p>
  </div>

  <script>
    const DATA = __DATA_JSON__;
    (function () {
      const container = document.getElementById('mynetwork');
      const nodes = new vis.DataSet(DATA.nodes);
      const edges = new vis.DataSet(DATA.edges);
      const network = new vis.Network(container, { nodes, edges }, {
        interaction: { hover: true },
        physics: { stabilization: true }
      });
      const win = document.getElementById('infowindow');
      const closeBtn = document.getElementById('closeinfo');
      const nameEl = document.getElementById('info_name');
      const typeEl = document.getElementById('info_type');
      const meaningEl = document.getElementById('info_meaning');
      network.on('click', function (params) {
        if (params.nodes && params.nodes.length) {
          const n = nodes.get(params.nodes[0]);
          nameEl.textContent = n.name || '';
          typeEl.textContent = n.type || '';
          meaningEl.textContent = n.meaning || '';
          win.style.display = 'block';
        } else {
          win.style.display = 'none';
        }
      });
      closeBtn.onclick = function(){ win.style.display = 'none'; };
    })();
  </script>
</body>
</html>
