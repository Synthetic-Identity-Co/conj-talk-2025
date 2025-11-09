# storyBASE Repository

**AI memory that tells your story, as written.**

---

## State

The storyBASE currently holds two major narrative threads:

1. **storyBASE Product & Strategy** – A comprehensive product architecture extracted from a conversational transcript, capturing the market opportunity, technical implementation, roadmap, and organizational design for storyBASE as an RDF-native, Git-backed AI memory system.[^1]

2. **Immutable Selves: Clojure Talk Proposal** – A conference talk framework applying functional programming principles (immutability, explicit state, data-first design) to identity systems, bridging past work at Vouch.io with current work at Sic.[^2]

Both narratives share a common thesis: **trustworthy systems require immutable, versionable, provenance-tracked foundations**—whether for organizational memory or individual identity.

---

## Stories

### `/README.story`
**Intent:** Maintain a living, auto-generated repository README that tracks the evolving state of storyBASE.

**Relationship to Whole:** Acts as the narrative entry point and changelog, synthesizing transactions and assets into a coherent overview.

**Approach:** Compiles the snapshot to extract current state, stories, assets, and transactions; renders them as a structured Markdown document with citations back to the RDF graph.[^3]

---

### `/presenter.story`
**Intent:** Draft the "Immutable Selves" conference talk using the iA Presenter format, with citations to storyBASE for provenance.

**Relationship to Whole:** Demonstrates storyBASE's capacity to scaffold narrative artifacts (talks, decks, documentation) from structured knowledge graphs.

**Approach:** Maps the Conj Talk 2025 extraction (Opportunity, Strategy, Product, Proof, Architecture) onto the iA Presenter slide format; uses footnotes to cite supporting nodes in the graph (e.g., `#Opportunity`, `#Strategy`, `#Architecture`).[^4]

---

## Assets

### Repository Structure

```
.storyBASE/
├── 1762728019add_conj_talk_2025_extraction.sparql  # Conj Talk 2025 narrative
└── 1762731465sic-storybase-checkin.sparql          # storyBASE product extraction

README.story                                         # This document generator
presenter.story                                      # Talk scaffolding template
```

#### Transaction Files (`.sparql`)
Append-only SPARQL `INSERT DATA` statements that populate the RDF graph. Each transaction is timestamped, attributed to a user and agent, and captures:
- **Narrative Architecture** nodes (Opportunity, Strategy, Product, Architecture, Organization, Proof)
- **Style Observations** (brand names, rhetorical devices, tone)
- **Rubric Assessments** (scores for clarity, technical depth, coherence, engagement)
- **Metrics** (sentence length, active voice ratio, technical density)[^5]

#### Story Files (`.story`)
YAML front matter + Markdown prompts. The front matter declares destination, model, and metadata; the body provides instructions for narrative generation.[^6]

#### Compiled Snapshot (`ttl`)
A Turtle-serialized RDF graph replaying all transactions in sorted order. This snapshot serves as the canonical source of truth for story generation.[^7]

---

### Mermaid: Data Flow

```mermaid
graph LR
    A[Input: Transcripts, Docs] -->|extract| B[Transaction .sparql]
    B -->|compile| C[Snapshot .ttl]
    C -->|story generation| D[.story templates]
    D -->|model inference| E[Output: README, Decks, Docs]
    E -->|commit| F[Git repository]
    F -->|GitHub Actions| G[Auto-update artifacts]
```

---

## Transactions

### `1762728019add_conj_talk_2025_extraction.sparql`
**Timestamp:** 2025-11-09T22:39:28.133Z  
**Significance:** First extraction for the Conj 2025 talk proposal.

- **Opportunity:** Identity vulnerability crisis (deepfakes, synthetic identities, impersonation fraud)[^8]
- **Strategy:** Functional immutable identity architecture (immutability, explicit state, knowledge graphs)[^9]
- **Products:** Vouch.io (past), Sic (current)[^10]
- **Proof:** Conference talk with threaded diagrams and optional demo[^11]
- **Architecture:** Append-only event logs, authentication as pure functions, delegation chains, graph resolution[^12]
- **Style Observations:** Brand stylization (Vouch.io, Sic), technical reframings (identity as log, trust as computable provenance), triadic enumeration[^13]
- **Rubric Scores:** Clarity 4.5/5, Technical Depth 4.8/5, Narrative Coherence 4.6/5, Audience Engagement 4.3/5[^14]
- **Metrics:** Avg sentence length 22.4, technical density 0.68, active voice 0.71[^15]

---

### `1762731465sic-storybase-checkin.sparql`
**Timestamp:** 2025-11-09T23:37:05.079Z  
**Significance:** Comprehensive product and strategy extraction for storyBASE/Sic.

- **Market Opportunity:** AI needs extensive context; RDF-based narrative source of truth enables specific, controllable, versionable AI memory[^16]
- **Timing Thesis:** Convergence of prompt engineering maturity, multi-agent workflows, organizational AI memory demand (2024–2026)[^17]
- **Positioning:** Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing[^18]
- **Moat:** Git-native, versionable AI memory encoding style, conviction, metrics; replaces brittle role prompts with deep persona descriptions[^19]
- **Product Overview:** n8n prototype; tools: compile, extract, diff, tx, commit; MCP server; Open WebUI; GitHub Actions[^20]
- **Capabilities:** Compile (replay to Turtle), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only), story generation[^21]
- **Roadmap:** Move to TriG/named graphs, SHACL validation, evolved individuation pipeline, file ingestion, marketplace, cost pass-through billing[^22]
- **Integration Points:** GitHub (OAuth, webhooks, Actions), Open Router (via Helicone), Outseta (OIDC, billing), MCP protocol[^23]
- **Case Studies (Planned):** Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (NPR → OpenAI)[^24]
- **Style Observations:** CamelCase "storyBASE", conversational fillers ("you know"), power verb "extend", first-person tone, jargon without definition, parallel construction ("extract … diff … tx")[^25]
- **Rubric Scores:** Register Fit 3.5/5, Phrasing 3.0/5, Cadence 3.0/5, Strategic Alignment 4.0/5, Accuracy 4.0/5[^26]
- **Metrics:** Avg sentence length 35.2, active voice 0.72, jargon density 0.18, type-token ratio 0.42[^27]

---

## Ontology Highlights

The storyBASE ontology extends SKOS with:
- **Narrative Architecture** – Six top concepts: Opportunity, Strategy, Product, Architecture, Organization, Proof, Templates, Calibration[^28]
- **Style Taxonomy** – Diction, Tone/Voice, Grammar, Cadence, Rhetorical Devices, Orthography, Citation Conventions, Metrics, Review[^29]
- **Conviction Levels** – Notion → Stake → Boulder → Foundation (ordered escalation path for claim settledness)[^30]
- **Rubric Dimensions** – Register Fit, Phrasing, Cadence, Strategic Alignment, Tailoring, Resonance, Flow, Novelty, Accuracy[^31]

---

[^1]: storyBASE Product Overview – `<http://storybase.synthetic-identity.co/product/overview-storybase>` describes initial n8n prototype, toolchain (compile, extract, diff, tx, commit), MCP server, Open WebUI, and GitHub Actions for story generation.

[^2]: Conj Talk 2025 Sample – `<urn:uuid:conj-talk-2025-extraction>` labeled "Immutable Selves"; recorded 2025-01-01, input length 3421; generated by transaction `<http://storybase.org/narrative#Tx_20251109T223928Z_conj2025>`.

[^3]: storyBASE Data Model Lifecycle – `<http://storybase.synthetic-identity.co/model/data-lifecycle-storybase>` defines append-only transaction log, immutable files, snapshot as replay of sorted transactions, provenance in TX step, future named graphs for add/remove.

[^4]: Conj Talk 2025 Proof – `<urn:uuid:proof-conj-2025-talk>` describes conference talk with threaded diagrams from model to implementation, optional short demo with canned fallback, targeting Clojure developers and functional programming practitioners.

[^5]: Style Metrics (storyBASE check-in) – `<http://storybase.synthetic-identity.co/metrics/style>` reports avg sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42; note: "Conversational transcript with high jargon and active voice."

[^6]: Story Prompt README – Front matter declares `id: README`, `title: "storyBASE repo README"`, `version: 0.1.0`, `description: "autogenerated readme tracking storyBASE as written"`, `destination: /`, `model: anthropic/claude-sonnet-4.5`.

[^7]: storyBASE Modules Capabilities – `<http://storybase.synthetic-identity.co/module/storybase-capabilities>` describes Compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs).

[^8]: Opportunity Identity Vulnerability – `<urn:uuid:opportunity-identity-vulnerability>` labeled "Identity Vulnerability Crisis"; description: "Centralized, mutable identity systems vulnerable to deepfakes, synthetic identities, and impersonation fraud"; market context: "Enterprise identity and authentication".

[^9]: Strategy Functional Immutable Identity – `<urn:uuid:strategy-functional-immutable-identity>` labeled "Functional Immutable Identity Architecture"; applies Clojure principles (immutability, explicit state, functional composition, data-first design, knowledge graphs); approach: models identity as append-only event logs, authentication as pure functions, delegation as auditable chains.

[^10]: Product Vouch.io – `<urn:uuid:product-vouch-io>` labeled "Vouch.io Identity Platform"; enterprise identity using immutable event logs and delegation chains; note: "Past work, speaker now strategic advisor". Product Sic – `<urn:uuid:product-sic>` labeled "Sic AI Memory Platform"; uses narrative-driven knowledge graphs for AI individuals with deterministic individuality and provenance; note: "Current work, speaker is founder".

[^11]: Proof Conj 2025 Talk – `<urn:uuid:proof-conj-2025-talk>` labeled "Conj 2025 Experience Report"; artifact: threaded diagrams from model to implementation, optional short demo with canned fallback; audience: Clojure developers and functional programming practitioners.

[^12]: Architecture Immutable Identity – `<urn:uuid:architecture-immutable-identity>` labeled "Immutable Identity System Patterns"; components: append-only event logs with verifiable receipts, authentication as pure function at the edge, delegation as signed append-only events, knowledge graphs for entity and role resolution; principles: immutability, functional composition, explicit state management, data-first design.

[^13]: Style Observations (Conj Talk) – Include: brand name styling Vouch.io (domain extension), technical terms (append-only event logs, authentication as pure functions, persistent logs and knowledge graphs), rhetorical structures (triadic enumeration, problem to solution bridge), technical reframings (identity as evolving log, trust as computable provenance), parallel construction in takeaways, personal identity lens (trans woman lived experience informs contextual/evolving identity framing).

[^14]: Rubric Assessments (Conj Talk) – Clarity 4.5/5 (clear problem, well-structured, actionable; minor density in technical sections), Technical Depth 4.8/5 (strong Clojure grounding, concrete patterns, dual case studies), Narrative Coherence 4.6/5 (coherent arc from deepfakes through immutability to talk structure; dual product lens adds depth), Audience Engagement 4.3/5 (actionable takeaways, optional demo, clear value; could strengthen emotional hook).

[^15]: Style Metrics (Conj Talk) – `<urn:uuid:style-metrics>` labeled "Style Metrics for Conj Talk 2025"; avg sentence length 22.4, technical density 0.68, active voice ratio 0.71; note: "Moderate sentence length, high technical density, strong active voice in takeaways".

[^16]: storyBASE Market Opportunity – `<http://storybase.synthetic-identity.co/opportunity/storybase-market>` labeled "storyBASE Market Opportunity"; description: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory"; market context: "AI prompt engineering and organizational memory".

[^17]: Timing Thesis – `<http://storybase.synthetic-identity.co/thesis/timing-storybase>` labeled "storyBASE Timing Thesis"; description: "Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management"; timestamp window: "2024-2026".

[^18]: Positioning Thesis – `<http://storybase.synthetic-identity.co/thesis/positioning-storybase>` labeled "storyBASE Positioning Thesis"; description: "Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth".

[^19]: Moat Leverage – `<http://storybase.synthetic-identity.co/leverage/moat-storybase>` labeled "storyBASE Moat Leverage"; description: "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions".

[^20]: storyBASE Product Overview – `<http://storybase.synthetic-identity.co/product/overview-storybase>` describes initial prototype in n8n; tools: compile, ontology, extract, diff, tx, commit; MCP server; open WebUI at as written.ai; GitHub Actions for story generation.

[^21]: storyBASE Modules Capabilities – `<http://storybase.synthetic-identity.co/module/storybase-capabilities>` describes compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs).

[^22]: Narrative-Driven Roadmap – `<http://storybase.synthetic-identity.co/roadmap/narrative-storybase>` labeled "storyBASE Narrative-Driven Roadmap"; description: "Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing".

[^23]: Integration Points – `<http://storybase.synthetic-identity.co/integration/points-storybase>` labeled "storyBASE Integration Points"; description: "GitHub (OAuth, webhooks, Actions); Open Router (API proxy via Helicone); Outseta (OIDC, billing); MCP protocol (tool exposure); future GitHub Apps with scoped credentials".

[^24]: Case Studies – `<http://storybase.synthetic-identity.co/case/studies-storybase>` labeled "storyBASE Case Studies"; description: "Planned demo: Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)".

[^25]: Style Observations (storyBASE) – Include: brand name stylization CamelCase "storyBASE" with internal capitalization; idiolect phrasing (conversational filler "you know"); verb choice (power verb "extend"); simile (implicit comparison: AI without context = generic output); tone direct personal (first-person "I", "So I don't know"); jargon policy (RDF, canonization, skolemization used without definition; assumes literate audience); sentence length variation (short, punchy breaks); parallelism ("extract … diff … tx"); rhetorical question (transitions to roadmap); caret bracket marker (citation marker present but unfilled).

[^26]: Rubric Assessments (storyBASE) – Register Fit 3.5/5 (conversational, informal; first-person; fillers; direct but not concise; fits spoken context), Phrasing 3.0/5 (domain verbs; some stock phrases; idiolect emerging), Cadence 3.0/5 (sentence length varies; some punchy breaks; rhythm uneven due to spoken delivery), Strategic Alignment 4.0/5 (clear positioning; mission and moat articulated; roadmap detailed; aligns with narrative anchor), Audience Tailoring 3.5/5 (assumes programming-literate audience; jargon without definition; some context-setting), Resonance 3.0/5 (light analogies; planned demos add resonance; could use more stories), Flow 3.0/5 (logical progression; some digressions; transitions implicit; spoken delivery affects coherence), Novelty 3.5/5 (brand stylization distinct; "individuation pipeline" novel; some generic constructions), Accuracy 4.0/5 (technical details specific—n8n, Apache Jena, Outseta, Helicone; named entities correct; citation marker present but unfilled).

[^27]: Style Metrics (storyBASE check-in) – `<http://storybase.synthetic-identity.co/metrics/style>` labeled "Style metrics"; description: "Average sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42"; note: "Conversational transcript with high jargon and active voice."

[^28]: Narrative Architecture Concept Scheme – `<NarrativeArchitecture>` titled "Narrative Architecture Operating System"; description: "A Narrative Architecture is the operating system for story-led strategy: it aligns market opportunity, strategy, product, and organization so the same narrative flows from positioning to roadmap to proof"; top concepts: Opportunity, Strategy, Product, Architecture, Organization, Proof, Templates, Calibration.

[^29]: Style Top Concept – `<#Style>` defined in ontology; prefLabel "Style"; definition: "A taxonomy of linguistic and presentation features: diction, tone/voice, grammar/syntax, cadence/rhythm, rhetorical devices, orthography/typography, citation conventions, register, POV, tense/aspect, inclusivity, localization, metrics, review, and reusable voice profiles."

[^30]: Conviction Top Concept – `<#Conviction>` defined in ontology; prefLabel "Conviction"; definition: "Degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost"; levels: Notion (suggestive/observational; open graph edges) → Stake (proposed; has supporting value and connected nodes; still moveable) → Boulder (settled/central; hard to move; requires multi-party consensus) → Foundation (underpinning across subgraphs; effectively permanent unless refuted by extraordinary proof).

[^31]: Style Rubric – `<#StyleRubric>` broader concept under StyleReview; prefLabel "Style Rubric (General Oratory)"; definition: "Evaluation criteria for speeches and narrative artifacts, abstracted for general use"; dimensions: Register Fit, Phrasing (Idiolect), Cadence, Strategic Alignment, Audience Tailoring, Resonance, Flow, Novelty, Accuracy.