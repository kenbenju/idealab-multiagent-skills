---
name: document-design
version: 3.0.0
description: |
  Expert Information Architect for static and dynamic documents. 
  Designs layouts for PDF, Excel, and PPT with focus on 
  Cognitive Load Reduction and Hierarchical Clarity.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Productivity
trigger_phrases:
  - design the information architecture for a complex PDF
  - build an Excel dashboard logic for [Data Group]
  - create a high-fidelity PowerPoint slide deck map
  - cognitive load reduction bridge (v3.0)
  - document layout and asset specification
license: IDEALAB Partners v3.0
---

# 📄 Document Design & Info-Architecture (v3.0 Layout Engine)

## 🗺️ Ontological Grid Map
```mermaid
graph TD
    A[Content/Data Ingest] --> B{Information Hierarchy}
    B --> C[Page 1: The Executive Summary/Hook]
    B --> D[Page 2+: The Evidence/Logic]
    B --> E[Final Page: The CTA/Action]
    C & D & E --> F[The Visual Grid: F-Pattern vs Z-Pattern]
    F --> G[Data Visualization Strategy: Charts/Graphs]
    G --> H[Color/Typo Token Application]
    H --> I[Final Design Brief for Tool (Canva/InDesign)]
```

---

## 📥 Inputs & 📤 Outputs

### `<document_ingestion_schema>`
```json
{
  "doc_type": "Report / Checklist / Dashboard / Presentation",
  "content_raw": "Bulk text/data",
  "target_audience": "Analytical / Executive / Creative",
  "accessibility_level": "Standard / High-Assistance"
}
```

### `<design_spec_schema>`
```json
{
  "grid_system": "Columnar / Module / Radial",
  "page_by_page_architecture": [
    {"page": 1, "elements": ["Header", "Key Metric", "Summary"], "visual_weight": "Top-Left"}
  ],
  "data_viz_map": {
    "metric_x": "Donut Chart for part-to-whole",
    "metric_y": "Line graph for velocity"
  },
  "font_pairing": ["Head: Bold Sans", "Body: Serif for Readability"]
}
```

---

## 📜 Architecture Standards (10,000% Logic)

### 1. Cognitive Load Reduction
Do not cram information. Use **Negative Space** as a structural element. 
- **Rule:** All pages MUST have at least 20% white space to prevent "Reader Paralysis".
- **Rule:** Use "Information Chunking" (Bullet points of max 7 items).

### 2. Reading Patterns (F/Z Logic)
- **Reports/PDFs:** Use the `F-Pattern`. People scan the top, then the left, then the middle. Critical info must be on those axes.
- **Decks/Slides:** Use the `Z-Pattern`. From top-left to top-right, then diagonal to bottom-left, finishing at bottom-right (The CTA).

### 3. Data Visualization Logic
Do not guess which chart to use.
- **Comparison:** Bar Chart.
- **Relationship:** Scatter Plot.
- **Value Over Time:** Line Chart with confidence intervals.
- **Protocol:** Every chart must include a "So What?" caption that explains the meaning of the data.

### 4. Integration with Brand DNA
The `document-design` agent MUST fetch the `Visual System Token` from Brand DNA. 
- *The Rebel:* Use bold borders, high-impact titles, and high-energy contrasts.
- *The Sage:* Clean lines, subtle borders, and harmonious colors.

---

## 🛠️ Usage for Claude
Use this skill for any work that produces a deliverable (Proposal, Report, Course). It turns "text" into a "product".

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
