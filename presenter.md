# SIC
# AI memory that tells your story, as written.
###### storyBASE: Git-native RDF knowledge graphs for narrative-driven AI

storyBASE is an RDF narrative source of truth that steers AI output, making it specific, controllable, and aligned with organizational worldview[^product-overview]. This presentation introduces the system architecture, narrative framework, and proof of concept.

[^product-overview]: From storyBASE Product Overview: "RDF narrative source of truth (storyBASE) that steers AI output, making it specific, controllable, aligned with organizational worldview." The system extends software development rigor (versioning, branching, collaboration) into strategy, content, and marketing via append-only transaction logs compiled into Turtle snapshots.

---

# storyBASE
## AI memory that tells your story, as written.

---

###### The Problem
## AI without context is generic

High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory[^opportunity].

[^opportunity]: From storyBASE Market Opportunity: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory." Market context is AI prompt engineering and organizational memory, with timing thesis centered on 2024-2026 convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory.

---

### The Opportunity
	Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates a window for narrative-driven context management[^timing].

The market opportunity sits at the intersection of AI prompt engineering and organizational memory. Current approaches rely on brittle role prompts and search-based context retrieval. storyBASE replaces these with deep, operable persona descriptions encoded in versionable RDF graphs.

[^timing]: From storyBASE Timing Thesis: "Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management" with timestamp window 2024-2026.

---

###### The Solution
## Git-native, versionable, branchable AI memory

storyBASE encodes style, conviction, and narrative metrics in an append-only transaction log, replacing brittle role prompts with deep, operable persona descriptions[^moat].

[^moat]: From storyBASE Moat Leverage: "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions."

---

### What is storyBASE?

	An RDF knowledge graph that captures narrative architecture—opportunity, strategy, product, proof, architecture, organization—plus style observations, rubric assessments, and conviction levels.

storyBASE is both a data model and a workflow. It compiles append-only SPARQL transactions into Turtle snapshots, enabling version control, semantic diffing, and provenance tracking. Every claim, style observation, and strategic assertion is traceable to its source transaction[^data-model].

[^data-model]: From storyBASE Data Model Lifecycle: "Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove."

---

## 1. Narrative Architecture
	The operating system for story-led strategy

---

### Narrative Architecture
	Aligns market opportunity, strategy, product, and organization so the same narrative flows from positioning to roadmap to proof.

A Narrative Architecture has six core domains: Opportunity, Strategy, Product, Architecture, Organization, and Proof. Each domain contains structured concepts that ladder from high-level positioning to executable artifacts[^narrative-anchor].

[^narrative-anchor]: From Narrative Anchor concept: "Framework linking immutable state, functional UI, and AI-driven generation via RDF knowledge graphs." The architecture ensures that narrative claims are testable, versionable, and aligned across all organizational outputs.

---

### Opportunity
	Frames the external landscape so we pursue a real, timely, winnable problem.

Opportunity analysis includes market context (TAM/SAM/SOM, segmentation, competitive landscape), actor incentive analysis (primary actors, jobs-to-be-done, power/dependency mapping), and trend forecasting (signals, conflicts, deltas, inflection points)[^opportunity-domain].

[^opportunity-domain]: From Opportunity top concept: "A clear view of the market ensures the narrative starts from truth. This section identifies why now, who cares, and what forces shape adoption." The storyBASE currently captures opportunity for AI prompt engineering and organizational memory markets.

---

### Strategy
	Decides how we win and anchors the story that powers choices, focus, and sequencing.

Strategy includes positioning thesis, moat & leverage, focus & sequencing, and the narrative anchor (tagline, mission, vision, key phrases)[^strategy-overview]. The narrative anchor is the compact, repeatable story that makes the organization memorable and directs execution.

[^strategy-overview]: From Strategy Overview: "States where we play, how we win, and what we won't do." The storyBASE positioning thesis is to "extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth."

---

### Product
	Shows how the story becomes usable capability—modules, flows, and offerings.

Product converts narrative into experience through modules & capabilities, personas & JTBD, differentiators, dependencies & integrations, and packaging & entitlement[^product-overview-detail]. The Product Ladder maps primitives → interfaces → behaviors → flows → narratives → milestones → offerings.

[^product-overview-detail]: From Product Overview: "Initial prototype in n8n; tools include compile, ontology, extract, diff, tx, commit; MCP server; open WebUI at as written.ai; GitHub Actions for story generation." Current capabilities include compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), and story generation (YAML front matter + prompt to model outputs).

---

### Architecture
	Explains the technical system that makes the narrative credible, scalable, and defensible.

Architecture underwrites the narrative with system topology, data model & lifecycle, integration points, security & privacy model, scalability & performance, reliability & resilience, observability, and compliance posture[^architecture-overview].

[^architecture-overview]: From Architecture Overview: "Plain-language explanation of choices, tradeoffs, and value." The storyBASE system topology uses n8n agent orchestration, MCP server exposure to frontends (Agent.ai, ChatGPT, Open WebUI), transactions in .storybase directories, hierarchical compile, and Docker Compose on Digital Ocean.

---

### Organization
	Maps roles and processes that consistently deliver the narrative promise.

Organization defines role topology (org by domain, RACI & decision rights, skill matrices, hiring plan, operating cadence) and process (core workflows, intake & prioritization, change management, quality & review gates, incident response, feedback loops)[^organization].

[^organization]: From Organization top concept: "Narratives are delivered by people and process. This section ensures the org design supports building, selling, and supporting the promised experience." Current role topology includes programming-literate users with admin vs. read-write vs. read-only modes, GitHub role-based access, and future scoped permissions via GitHub Apps.

---

### Proof
	Demonstrates outcomes that validate the story with evidence customers trust.

Proof includes case studies (context, intervention, results, artifacts, lessons), outcomes (quotes, talks, customer artifacts), and metrics & monitoring (north-star metrics, leading indicators, operational dashboards, instrumentation plan, review rituals)[^proof].

[^proof]: From Proof top concept: "Evidence converts belief into commitment. This section curates the artifacts and results that validate claims with real-world outcomes." Planned demo includes Crooked Media podcast transcripts auto-ingested, stories auto-update, and perspectival operations (e.g., start with NPR, evolve with OpenAI).

---

## 2. Style & Conviction
	Encoding voice and settledness

---

### Style
	Encodes how the narrative sounds and reads—choices of words, structure, rhythm, devices, and conventions—so brand voice is consistent and measurable.

Style taxonomy includes diction & word choice, tone & voice, register & formality, POV (person), tense & aspect, grammar & syntax, cadence & rhythm, rhetorical devices, orthography & spelling, punctuation & typography, citation conventions, inclusive language & accessibility, localization & internationalization, style metrics, and style review[^style].

[^style]: From Style top concept: "A taxonomy of linguistic and presentation features: diction, tone/voice, grammar/syntax, cadence/rhythm, rhetorical devices, orthography/typography, citation conventions, register, POV, tense/aspect, inclusivity, localization, metrics, review, and reusable voice profiles." The storyBASE captures style observations including brand name stylization (CamelCase 'storyBASE'), idiolect phrasing (conversational filler 'you know'), verb choice (power verb 'extend'), and jargon policy (technical jargon used without definition, assumes literate audience).

---

### Style Observations
	Captured from samples to build voice profiles

The storyBASE contains 10 style observations from the SIC/storyBASE check-in sample, including brand name stylization, idiolect phrasing, verb choice, simile, tone direct personal, jargon policy, sentence length variation, parallelism, rhetorical question, and caret bracket marker[^style-obs].

[^style-obs]: From Style Observations in SIC check-in sample: Examples include "CamelCase 'storyBASE' with internal capitalization," "Conversational filler 'you know' signals informal register," "Power verb 'extend' frames value proposition," "Technical jargon (RDF, canonization, skolemization) used without definition; assumes literate audience," and "Citation marker present but unfilled; signals placeholder."

---

### Style Metrics
	Quantitative signals for governance and drift detection

Style metrics include readability scores, active-voice ratio, jargon density, type-token ratio, average sentence length, and rhythm variance. The SIC check-in sample shows average sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42[^style-metrics].

[^style-metrics]: From Style Metrics for SIC check-in: "Average sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42" with note "Conversational transcript with high jargon and active voice."

---

### Conviction
	Degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost.

Conviction has four ordered levels: Notion (suggestive/observational; open graph edges; exploratory), Stake (proposed; has supporting value and connected nodes; still moveable), Boulder (settled/central; hard to move; requires multi-party consensus to shift), Foundation (underpinning across subgraphs; effectively permanent unless refuted by extraordinary proof)[^conviction].

[^conviction]: From Conviction top concept and ordered levels. Conviction is used to govern decisions and change cost, with escalation path from Notion → Stake → Boulder → Foundation. The system maintains rolling metrics for claims: score, weight, distances, individuation counts, and last update time.

---

## 3. System Architecture
	How storyBASE works

---

### System Topology
	n8n agent orchestrates tools; MCP server exposes to frontends; transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean[^topology].

The system uses n8n workflows for agent orchestration, MCP server for tool exposure to Agent.ai, ChatGPT, and Open WebUI, GitHub for version control, Apache Jena/Riot for future RDF ops, Docker Compose for deployment, Open WebUI for interface, Outseta for auth/billing, Helicone for API monitoring, and Open Router for model access[^integrations].

[^topology]: From storyBASE System Topology.

[^integrations]: From storyBASE Dependencies Integrations: "n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access)."

---

### Data Model & Lifecycle
	Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove.

Transactions are SPARQL INSERT DATA statements stored in .storybase directories. Each transaction includes provenance (prov:wasAssociatedWith, prov:wasAttributedTo, prov:generatedAtTime, sb:originPath, sb:originRef, storytwin:model). The compile step replays sorted transactions to produce a Turtle snapshot[^data-lifecycle].

[^data-lifecycle]: From storyBASE Data Model Lifecycle. Current implementation uses SPARQL files; roadmap includes move to named graphs (TriG) and SHACL validation.

---

### Integration Points
	GitHub (OAuth, webhooks, Actions); Open Router (API proxy via Helicone); Outseta (OIDC, billing); MCP protocol (tool exposure); future GitHub Apps with scoped credentials[^integration-points].

The system integrates with GitHub for version control and automation, Open Router for model access with Helicone monitoring, Outseta for authentication and billing, and MCP protocol for tool exposure to AI frontends. Future plans include GitHub Apps with scoped credentials for finer-grained access control[^integration-points].

[^integration-points]: From storyBASE Integration Points.

---

### Process
	Interactive individuation (extract → diff → tx → review → commit) vs. automated ingestion (file upload → extraction → PR); story generation triggered by transaction or .story file changes[^process].

The interactive individuation pipeline allows users to extract RDF from input, diff against current snapshot, propose transactions, review changes, and commit to Git. Automated ingestion supports file upload, extraction, and pull request creation. Story generation is triggered by transaction commits or .story file changes via GitHub Actions[^process].

[^process]: From storyBASE Process.

---

## 4. Current State
	Three transactions, three stories, working prototype

---

### Transactions
	1. Sample 1: Narrative architecture extraction (voice memo, Scarlet Dame)
	2. SIC/storyBASE check-in: Product & strategy (spoken transcript)
	3. Conj Talk 2025: Immutable Selves (conference proposal)

The storyBASE contains three transactions totaling 517 inserted triples. Transaction 1 extracts narrative architecture from a voice memo outlining identity-as-append-only-log talk. Transaction 2 captures product and strategy from a spoken check-in. Transaction 3 extracts the Conj 2025 talk proposal on immutable identity systems[^transactions].

[^transactions]: From TRANSACTIONS in snapshot. Transaction 1 (Tx_20251110T184512Z_sample1) generated 2025-11-10T18:45:12.711Z by storyTWIN using anthropic/claude-sonnet-4.5. Transaction 2 (2025-01-29T000000Z_sic-storybase-checkin) generated 2025-11-09T23:37:05.079Z by n8n.storyTWIN/MCP. Transaction 3 (Tx_20251109T223928Z_conj2025) generated 2025-11-09T22:39:28.133Z by n8n.storyTWIN/MCP using anthropic/claude-sonnet-4.5.

---

### Stories
	1. README.story: Autogenerated repo README tracking storyBASE state
	2. presenter.story: IA presenter template for talk presentation
	3. conj-talk-2025.story: Immutable Selves talk for Clojure Conj

Stories are YAML front matter + prompt templates that generate outputs from the storyBASE snapshot. The README story summarizes current state, stories, assets, and transactions. The presenter story drafts presentations using IA Presenter format. The conj-talk story generates the Immutable Selves talk with personal history, identity model, failure of mutable paradigms, Clojure principles, and Vouch.io + As Written case studies[^stories].

[^stories]: From STORIES in snapshot. Each story has id, title, version, description, destination, and model fields. Stories are triggered by GitHub Actions on transaction or .story file changes.

---

### Rubric Assessments
	Nine dimensions scored 0-5 for narrative quality

The storyBASE includes rubric assessments for samples across nine dimensions: Register Fit, Phrasing (Idiolect), Cadence, Strategic Alignment, Audience Tailoring, Resonance, Flow, Novelty, and Accuracy. Sample 1 scores range from 3.0 (Cadence, Flow) to 4.5 (Strategic Alignment, Resonance). SIC check-in scores range from 3.0 (Phrasing, Cadence, Flow, Resonance, Novelty) to 4.0 (Strategic Alignment, Accuracy)[^rubric].

[^rubric]: From Rubric Assessments in snapshot. Sample 1 assessments include "Conversational, personal; active voice; fits talk/oratory context. Some filler (voice memo)" (Register 4.0), "Idiolect present ('append-only log', 'functional transformation'); some repetition/self-correction" (Phrasing 3.5), "Personal transition story as analogy for immutable state; emotionally grounded, memorable" (Resonance 4.5). SIC check-in assessments include "Conversational, informal; first-person 'I'; fillers; direct but not concise; fits spoken context" (Register 3.5), "Clear positioning; mission and moat articulated; roadmap detailed; aligns with narrative anchor" (Strategic Alignment 4.0).

---

## 5. Roadmap
	From prototype to platform

---

### Narrative-Driven Roadmap
	Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing[^roadmap].

The roadmap prioritizes technical evolution (TriG, SHACL), workflow improvements (evolved individuation, file ingestion), and platform features (marketplace, billing). Each milestone advances the core narrative: extending software development rigor into strategy, content, and marketing[^roadmap].

[^roadmap]: From storyBASE Narrative-Driven Roadmap. Related to core narrative expansion.

---

### Case Studies (Planned)
	Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)[^case-studies].

The planned demo will show automated ingestion of podcast transcripts, automatic story updates on new transactions, and perspectival operations that allow the same narrative to be rendered from different viewpoints (e.g., NPR style vs. OpenAI style) by branching the storyBASE and applying different style profiles[^case-studies].

[^case-studies]: From storyBASE Case Studies.

---

## 6. Proof
	Working system, real outputs

---

### This Presentation
	Generated from storyBASE snapshot via presenter.story template

This presentation is itself proof: it was generated by the storyWRITER agent from the compiled storyBASE snapshot using the presenter.story template. Every claim is cited back to the RDF graph with provenance to source transactions[^meta-proof].

[^meta-proof]: From presenter.story: "Use the storyBASE to draft a presentation of the storyBASE using the provided format. Focus on presenting clear narrative statements in the slide copy and provide a brief talk track for each slide. Cite important claims with footnotes to the storyBASE and explain context in the footnote."

---

### Conj Talk 2025
	Immutable Selves: Identity as Append-Only Log

The Conj Talk 2025 proposal demonstrates storyBASE's ability to capture and generate technical narratives. The talk applies Clojure principles (immutability, explicit state, functional composition, data-first design, knowledge graphs) to create trustworthy identity systems, with case studies from Vouch.io (enterprise identity platform using immutable event logs and delegation chains) and Sic (AI memory company using narrative-driven knowledge graphs)[^conj-talk].

[^conj-talk]: From Conj Talk 2025 extraction (Tx_20251109T223928Z_conj2025). Strategy: "Applies Clojure principles (immutability, explicit state, functional composition, data-first design, knowledge graphs) to create trustworthy identity systems." Products: Vouch.io (past work, speaker now strategic advisor) and Sic (current work, speaker is founder). Rubric scores: Clarity 4.5, Technical Depth 4.8, Narrative Coherence 4.6, Audience Engagement 4.3.

---

### Sample 1: Narrative Architecture
	Voice memo extraction with style observations and rubric scores

Sample 1 demonstrates extraction of narrative architecture from a voice memo. The system captured themes (Immutable Identity as Append-Only Log, Transition as State Machine), actors (Scarlet Dame, Luke Vanderhart), style observations (brand name stylization, idiolect phrasing, metaphor, analogy), and rubric assessments across nine dimensions[^sample1].

[^sample1]: From Sample 1 (narr:Sample_1): "Transcribed voice memo outlining narrative architecture for identity-as-append-only-log talk; speaker: Scarlet Dame." Input length 11,800 characters. Created 2025-01-15. Generated by Tx_20251110T184512Z_sample1. Themes include "Human and system identity modeled as integral of snapshots over time, not mutable present state" and "Personal transition (gender, professional) as functional transformation from immutable past states."

---

## Now Go and Build
###### storyBASE is open source and ready for your narrative

For more information, visit as written.ai or explore the storyBASE repository on GitHub.

The storyBASE mission is to extend software development rigor into strategy, content, and marketing; provide versionable, collaborative, narrative-driven AI memory. The positioning thesis is to extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth[^mission].

[^mission]: From storyBASE Mission and storyBASE Positioning Thesis. The tagline is "AI that tells you a story as written" with user-facing brand as written.ai (Latin i.e. meaning).