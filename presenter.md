# SIC
# AI memory that tells your story, as written.
###### storyBASE: Git-native RDF knowledge graphs for narrative-driven AI

storyBASE is an RDF narrative source of truth that steers AI output, making it specific, controllable, and aligned with organizational worldview[^product-overview]. This presentation walks through the system architecture, narrative framework, and proof points that make storyBASE a versionable, collaborative AI memory platform.

[^product-overview]: From storyBASE Product Overview: "RDF narrative source of truth (storyBASE) that steers AI output, making it specific, controllable, aligned with organizational worldview." The system extends software development rigor (versioning, branching, collaboration) into strategy, content, marketing, and organizational operations via RDF narrative source of truth.

---

# storyBASE
## AI memory that tells your story, as written.

---

###### The Problem
## High-quality AI output requires extensive context

Current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory[^opportunity].

[^opportunity]: From storyBASE Market Opportunity: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory." Market context is AI prompt engineering and organizational memory.

---

### The Opportunity

---

###### Convergence of forces
### Timing: 2024–2026 window

Prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory create a window for narrative-driven context management[^timing].

[^timing]: From storyBASE Timing Thesis: "Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management." Timestamp window: 2024-2026.

---

###### Who it's for
### Programming-literate entrepreneurs, designers, developers, consultants

People who manipulate worldview and see perspective changes[^actors].

[^actors]: From storyBASE Primary Actors: "Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes." Related to personas and jobs-to-be-done analysis.

---

### The Strategy

---

###### Positioning
### Extend software development rigor into strategy, content, marketing

Versioning, branching, collaboration via RDF narrative source of truth[^positioning].

[^positioning]: From storyBASE Positioning Thesis: "Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth." Related to moat and leverage concepts.

---

###### Moat
### Git-native, versionable, branchable AI memory

Encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions[^moat].

[^moat]: From storyBASE Moat Leverage: "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions."

---

###### Mission
### Extend software development rigor into strategy, content, marketing

Provide versionable, collaborative, narrative-driven AI memory[^mission].

[^mission]: From storyBASE Mission: "Extend software development rigor into strategy, content, marketing; provide versionable, collaborative, narrative-driven AI memory."

---

### The Product

---

###### What is it?
### RDF narrative source of truth

storyBASE steers AI output, making it specific, controllable, aligned with organizational worldview[^what-is-it].

[^what-is-it]: From storyBASE What Is It: "RDF narrative source of truth (storyBASE) that steers AI output, making it specific, controllable, aligned with organizational worldview."

---

###### Current state
### Initial prototype in n8n

Tools include compile, ontology, extract, diff, tx, commit; MCP server; open WebUI at as written.ai; GitHub Actions for story generation[^product-overview-detail].

[^product-overview-detail]: From storyBASE Product Overview: "Initial prototype in n8n; tools include compile, ontology, extract, diff, tx, commit; MCP server; open WebUI at as written.ai; GitHub Actions for story generation." Related to modules/capabilities and dependencies/integrations.

---

###### Core capabilities
### Compile → Extract → Diff → Tx → Commit

- **Compile**: Replay transactions to Turtle snapshot
- **Extract**: RDF from input
- **Diff**: Semantic comparison
- **Tx**: Propose transaction
- **Commit**: Append-only to Git
- **Story generation**: YAML front matter + prompt to model outputs[^capabilities]

[^capabilities]: From storyBASE Modules Capabilities: "Compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs)."

---

### The Architecture

---

###### System topology
### n8n agent orchestrates tools

MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI); transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean[^topology].

[^topology]: From storyBASE System Topology: "n8n agent orchestrates tools; MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI); transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean."

---

###### Data model
### Append-only transaction log

Immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove[^data-model].

[^data-model]: From storyBASE Data Model Lifecycle: "Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove."

---

###### Integration points
### GitHub, Open Router, Outseta, MCP

- **GitHub**: OAuth, webhooks, Actions
- **Open Router**: API proxy via Helicone
- **Outseta**: OIDC, billing
- **MCP protocol**: Tool exposure
- Future: GitHub Apps with scoped credentials[^integrations]

[^integrations]: From storyBASE Integration Points: "GitHub (OAuth, webhooks, Actions); Open Router (API proxy via Helicone); Outseta (OIDC, billing); MCP protocol (tool exposure); future GitHub Apps with scoped credentials."

---

###### Dependencies
### n8n, MCP, GitHub, Apache Jena/Riot, Docker Compose, Open WebUI, Outseta, Helicone, Open Router

n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access)[^dependencies].

[^dependencies]: From storyBASE Dependencies Integrations: "n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access)."

---

### The Process

---

###### Two modes
### Interactive individuation vs. automated ingestion

**Interactive**: extract → diff → tx → review → commit

**Automated**: file upload → extraction → PR

Story generation triggered by transaction or .story file changes[^process].

[^process]: From storyBASE Process: "Interactive individuation (extract → diff → tx → review → commit) vs. automated ingestion (file upload → extraction → PR); story generation triggered by transaction or .story file changes."

---

###### Role topology
### Programming-literate users

Admin vs. read-write vs. read-only modes; GitHub role-based access; future scoped permissions via GitHub Apps[^roles].

[^roles]: From storyBASE Role Topology: "Programming-literate users; admin vs. read-write vs. read-only modes; GitHub role-based access; future scoped permissions via GitHub Apps."

---

### The Roadmap

---

###### Next steps
### Move transactions from SPARQL to named graphs (TriG)

- Add SHACL validation
- Implement evolved individuation pipeline (snapshot + message to transaction)
- File ingestion via GitHub
- storyBASE marketplace
- Cost pass-through billing[^roadmap]

[^roadmap]: From storyBASE Narrative-Driven Roadmap: "Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing." Related to core narrative expansion.

---

### Proof

---

###### Planned demo
### Crooked Media podcast transcripts auto-ingested

Stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)[^case-studies].

[^case-studies]: From storyBASE Case Studies: "Planned demo: Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)."

---

### Style & Calibration

---

###### Brand stylization
### CamelCase 'storyBASE' with internal capitalization

Conversational filler 'you know' signals informal register; power verb 'extend' frames value proposition[^style-obs].

[^style-obs]: From Style Observations: "CamelCase 'storyBASE' with internal capitalization" (Brand name stylization); "Conversational filler 'you know' signals informal register" (Idiolect phrasing); "Power verb 'extend' frames value proposition" (Verb choice).

---

###### Rubric assessments
### Strategic alignment: 4/5

- **Register Fit**: 3.5/5 (Conversational, informal; first-person 'I'; fillers; direct but not concise; fits spoken context)
- **Phrasing**: 3/5 (Domain verbs 'compile', 'extract'; some stock phrases; idiolect emerging)
- **Strategic Alignment**: 4/5 (Clear positioning; mission and moat articulated; roadmap detailed; aligns with narrative anchor)[^rubric]

[^rubric]: From Rubric Assessments: Register Fit (3.5/5), Phrasing (3/5), Strategic Alignment (4/5), Audience Tailoring (3.5/5), Resonance (3/5), Flow (3/5), Novelty (3.5/5), Accuracy (4/5). Scores reflect conversational transcript with high jargon and active voice.

---

###### Style metrics
### Average sentence length 35.2, active voice ratio 0.72

Jargon density 0.18, type-token ratio 0.42; conversational transcript with high jargon and active voice[^metrics].

[^metrics]: From Style Metrics: "Average sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42." Note: Conversational transcript with high jargon and active voice.

---

### Narrative Architecture

---

###### Framework
### Opportunity → Strategy → Product → Architecture → Organization → Proof

A Narrative Architecture is the operating system for story-led strategy: it aligns market opportunity, strategy, product, and organization so the same narrative flows from positioning to roadmap to proof[^narrative-arch].

[^narrative-arch]: From Narrative Architecture Concept Scheme: "A Narrative Architecture is the operating system for story-led strategy: it aligns market opportunity, strategy, product, and organization so the same narrative flows from positioning to roadmap to proof."

---

###### Conviction levels
### Notion → Stake → Boulder → Foundation

Degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost[^conviction].

[^conviction]: From Conviction: "Degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost." Levels: Notion (suggestive/observational; open graph edges; exploratory), Stake (proposed; has supporting value and connected nodes; still moveable), Boulder (settled/central; hard to move; requires multi-party consensus to shift), Foundation (underpinning across subgraphs; effectively permanent unless refuted by extraordinary proof).

---

### Current State

---

###### Three transactions
### Sample1 narrative architecture, SIC storyBASE check-in, Conj Talk 2025

1. **Sample1**: Voice memo outlining narrative architecture for identity-as-append-only-log talk; speaker: Scarlet Dame (11,800 chars)
2. **SIC storyBASE check-in**: Spoken transcript with conversational register and technical depth on storyBASE product evolution (18,437 chars)
3. **Conj Talk 2025**: Immutable Selves talk proposal (3,421 chars)[^transactions]

[^transactions]: From Transactions: Three transactions compiled into snapshot: (1) Tx_20251110T184512Z_sample1 (Sample_1, 11,800 chars, voice memo on narrative architecture), (2) Tx_20251109T223928Z_sic-storybase-checkin (18,437 chars, product & strategy check-in), (3) Tx_20251109T223928Z_conj2025 (3,421 chars, Conj Talk 2025 extraction).

---

###### Repository structure
### .storyBASE directory, stories, assets

- **.storyBASE/**: Transaction log (SPARQL files)
- **Stories**: README.story, presenter.story, conj-talk-2025.story
- **Assets**: Ontology (RDF/XML), snapshot (Turtle), compiled graph[^repo]

[^repo]: From Repository Structure: .storyBASE directory contains transaction log (SPARQL files); stories directory contains .story files (YAML front matter + prompt); ontology defines RDF schema; snapshot is compiled Turtle graph.

---

## Next Steps

---

### Explore the storyBASE

Visit **as written.ai** to see the open WebUI in action.

Review the **GitHub repository** to see transactions, ontology, and compiled snapshots.

Try the **MCP server** to integrate storyBASE into your AI workflows.

---

## AI memory that tells your story, as written.

For more, check the [storyBASE repository](https://github.com/synthetic-identity-co/storybase) and [as written.ai](https://as-written.ai).