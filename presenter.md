# SIC
# AI memory that tells your story, as written.
###### A presentation of storyBASE

storyBASE is a Git-native RDF knowledge graph that serves as the narrative source of truth for AI-driven content generation. This presentation walks through its architecture, capabilities, and vision.[^intro]

[^intro]: The storyBASE system is described across three major transactions: the narrative architecture extraction (Tx_20251110T184512Z_sample1), the product/strategy check-in (2025-01-29T000000Z_sic-storybase-checkin), and the Conj 2025 talk extraction (Tx_20251109T223928Z_conj2025). These transactions establish the foundational concepts, product capabilities, and strategic positioning.

---

###### The Problem
# AI without memory is generic

Current AI models produce generic output because they lack persistent, versionable context. Organizations need AI that remembers their worldview, style, and strategy—not just search results.[^opportunity]

[^opportunity]: The storyBASE Market Opportunity (http://storybase.synthetic-identity.co/opportunity/storybase-market) identifies that "high-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory." This addresses the gap in organizational AI memory systems.

---

## What is storyBASE?

---

## Git-native RDF knowledge graph
###### Your narrative source of truth

storyBASE is an append-only transaction log that compiles into a Turtle snapshot. It encodes narrative architecture—opportunity, strategy, product, proof, style, and conviction—so AI agents can generate content that's specific, controllable, and aligned with your worldview.[^what-is-it]

[^what-is-it]: Product Overview (http://storybase.synthetic-identity.co/product/what-is-storybase) defines storyBASE as "RDF narrative source of truth (storyBASE) that steers AI output, making it specific, controllable, aligned with organizational worldview." The system uses SPARQL transactions stored in `.storybase` directories, compiled hierarchically into Turtle snapshots.

---

### The Mission

	Extend software development rigor into strategy, content, and marketing. Provide versionable, collaborative, narrative-driven AI memory.[^mission]

[^mission]: Mission statement from http://storybase.synthetic-identity.co/mission/storybase. This positions storyBASE as bringing Git-like version control and collaboration patterns to organizational narrative and strategy work.

---

### How It Works

	1. **Extract** narrative from inputs (transcripts, docs, conversations)
	2. **Diff** proposed changes against current snapshot
	3. **Commit** transactions to append-only log
	4. **Compile** snapshot from sorted transaction history
	5. **Generate** stories using snapshot as context

The individuation pipeline transforms unstructured input into structured RDF, maintaining full provenance.[^capabilities]

[^capabilities]: Module Capabilities (http://storybase.synthetic-identity.co/module/storybase-capabilities) describes the core workflow: "Compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs)."

---

###### Architecture
### Immutable by design

---

### Append-Only Transaction Log

	Every change is a transaction. Transactions are immutable files. The snapshot is the replay of sorted transactions. Provenance is built in.[^data-model]

This mirrors the identity-as-append-only-log model: you are the integral of your history, not a mutable present state.[^immutable-identity]

[^data-model]: Data Model Lifecycle (http://storybase.synthetic-identity.co/model/data-lifecycle-storybase) specifies "Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove."

[^immutable-identity]: Theme from Sample_1 (http://example.org/narrative#Theme_ImmutableIdentity): "Human and system identity modeled as integral of snapshots over time, not mutable present state." This philosophical foundation connects personal identity (gender transition as state change) to system architecture (immutable event logs).

---

### System Topology

	**n8n agent** orchestrates tools
	**MCP server** exposes to frontends (Agent.ai, ChatGPT, Open WebUI)
	**Transactions** in `.storybase` directories
	**Hierarchical compile** from root to leaves
	**Docker Compose** on Digital Ocean[^topology]

[^topology]: System Topology (http://storybase.synthetic-identity.co/architecture/topology-storybase) describes the orchestration layer and integration points. The MCP (Model Context Protocol) server provides a standard interface for AI frontends to access storyBASE tools.

---

### Integration Points

	**GitHub**: OAuth, webhooks, Actions
	**Open Router**: API proxy via Helicone
	**Outseta**: OIDC, billing
	**MCP protocol**: tool exposure
	**Future**: GitHub Apps with scoped credentials[^integrations]

[^integrations]: Integration Points (http://storybase.synthetic-identity.co/integration/points-storybase) and Dependencies (http://storybase.synthetic-identity.co/dependency/storybase-integrations) detail the external systems. Helicone provides API monitoring; Open Router proxies model access; Outseta handles authentication and billing.

---

###### Narrative Architecture
### The operating system for story-led strategy

---

### Six Core Domains

	1. **Opportunity**: Market context, actors, timing
	2. **Strategy**: Positioning, moat, narrative anchor
	3. **Product**: Capabilities, flows, offerings
	4. **Architecture**: System design, explainers, docs
	5. **Organization**: Roles, processes, change management
	6. **Proof**: Case studies, outcomes, metrics[^narrative-arch]

Each domain is a SKOS concept scheme with narrower concepts, creating a navigable knowledge graph.[^ontology]

[^narrative-arch]: The Narrative Architecture ontology defines these six top concepts (http://example.org/narrative#Opportunity, #Strategy, #Product, #Architecture, #Organization, #Proof) as the foundational structure. This framework appears in the ontology provided in the SNAPSHOT.

[^ontology]: The ontology uses SKOS (Simple Knowledge Organization System) and XKOS (Extended SKOS) to create hierarchical concept schemes with broader/narrower relationships, sequential ordering (xkos:next/previous), and depth levels. This enables both human navigation and machine reasoning.

---

### Style as Structure

	**Diction**: Terminology control, naming conventions, verb choice
	**Tone**: Direct/personal, authoritative, active voice
	**Cadence**: Sentence length variation, rhythm, rule of three
	**Devices**: Simile, metaphor, analogy, rhetorical questions
	**Metrics**: Readability, active voice ratio, jargon density[^style]

Style is not decoration—it's encoded structure that makes brand voice measurable and reproducible.[^style-metrics]

[^style]: The Style top concept (http://example.org/narrative#Style) was added to the ontology to encode linguistic and presentation features. It includes facets for diction, tone, grammar, cadence, rhetorical devices, orthography, punctuation, citation conventions, and more.

[^style-metrics]: Style Metrics (http://example.org/narrative#StyleMetrics) include quantitative signals like readability scores, active voice ratio, jargon density, type-token ratio, average sentence length, and rhythm variance. These enable drift detection and governance.

---

### Conviction Levels

	**Notion**: Exploratory, open graph edges
	**Stake**: Proposed, has supporting value
	**Boulder**: Settled, hard to move
	**Foundation**: Underpinning, effectively permanent[^conviction]

Conviction governs decision cost and change management. Foundations require extraordinary proof to shift.[^conviction-def]

[^conviction]: The Conviction top concept (http://example.org/narrative#Conviction) encodes "degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost." The four levels use xkos:next/previous to encode escalation paths.

[^conviction-def]: Conviction levels are defined with increasing resistance to change: Notion (suggestive/observational), Stake (proposed with supporting value), Boulder (settled/central, requires multi-party consensus), Foundation (underpinning across subgraphs, effectively permanent unless refuted by extraordinary proof).

---

###### The Roadmap
### From prototype to platform

---

### Near-Term

	**Move to named graphs (TriG)** for add/remove operations
	**SHACL validation** for schema enforcement
	**Evolved individuation pipeline**: snapshot + message → transaction
	**File ingestion via GitHub**: auto-extract from commits
	**storyBASE marketplace**: shareable narrative modules[^roadmap]

[^roadmap]: Narrative-Driven Roadmap (http://storybase.synthetic-identity.co/roadmap/narrative-storybase) outlines the technical evolution: "Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing."

---

### Case Study: Crooked Media

	**Planned demo**: Podcast transcripts auto-ingested
	**Stories auto-update** on new episodes
	**Perspectival operations**: Start with NPR voice, evolve with OpenAI
	**Shareable narrative modules** for media organizations[^case-study]

This demonstrates storyBASE as infrastructure for narrative-driven content pipelines.[^process]

[^case-study]: Case Studies (http://storybase.synthetic-identity.co/case/studies-storybase) describes the planned Crooked Media demo: "Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)."

[^process]: Process (http://storybase.synthetic-identity.co/process/storybase) distinguishes "Interactive individuation (extract → diff → tx → review → commit) vs. automated ingestion (file upload → extraction → PR); story generation triggered by transaction or .story file changes."

---

###### Positioning
### Where we play, how we win

---

### Primary Actors

	Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes.[^actors]

These users already think in systems and version control. storyBASE extends that rigor to narrative and strategy.[^positioning]

[^actors]: Primary Actors (http://storybase.synthetic-identity.co/actor/primary-storybase) defines the target: "Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes."

[^positioning]: Positioning Thesis (http://storybase.synthetic-identity.co/thesis/positioning-storybase): "Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth."

---

### Moat & Leverage

	Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics. Replaces brittle role prompts with deep, operable persona descriptions.[^moat]

The moat is not the technology—it's the accumulated narrative graph that becomes more valuable with every transaction.[^leverage]

[^moat]: Moat Leverage (http://storybase.synthetic-identity.co/leverage/moat-storybase) describes the defensibility: "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions."

[^leverage]: The network effect comes from the narrative graph itself: as organizations encode more of their worldview, style, and strategy, the storyBASE becomes harder to replace. This mirrors data network effects in traditional platforms.

---

### Timing Thesis

	Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management.[^timing]

The window is 2024-2026. We're building now.[^timing-window]

[^timing]: Timing Thesis (http://storybase.synthetic-identity.co/thesis/timing-storybase) identifies the convergence: "Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management."

[^timing-window]: The timestamp window "2024-2026" (http://storybase.synthetic-identity.co/thesis/timing-storybase) reflects the current maturation of AI tooling and organizational readiness for structured AI memory systems.

---

###### Proof
### It works

---

### Rubric Assessments

	**Strategic Alignment**: 4.0/5 — Clear positioning, mission, moat
	**Technical Depth**: 4.8/5 — Grounded in Clojure principles, verifiable architecture
	**Narrative Coherence**: 4.6/5 — Coherent arc from problem to proof
	**Accuracy**: 4.0/5 — Technical details specific, named entities correct[^rubric]

These scores come from the Conj 2025 talk extraction, assessed against the Style Rubric.[^rubric-def]

[^rubric]: Rubric assessments from the Conj 2025 extraction (urn:uuid:rubric-clarity, urn:uuid:rubric-technical-depth, urn:uuid:rubric-narrative-coherence, urn:uuid:rubric-accuracy) provide quantitative validation of narrative quality across multiple dimensions.

[^rubric-def]: The Style Rubric (http://example.org/narrative#StyleRubric) defines evaluation criteria: Register Fit, Phrasing (Idiolect), Cadence, Strategic Alignment, Audience Tailoring, Resonance, Flow, Novelty, and Accuracy. Each dimension is scored 0-5.

---

### Style Metrics

	**Average sentence length**: 22.4 (Conj talk), 28.5 (Sample 1), 35.2 (Check-in)
	**Active voice ratio**: 0.71–0.75
	**Jargon density**: 0.12–0.18
	**Technical density**: 0.68 (Conj talk)[^metrics]

Metrics vary by artifact type (talk vs. transcript vs. check-in) but maintain brand consistency.[^metrics-note]

[^metrics]: Style Metrics from three samples: Conj Talk (urn:uuid:style-metrics), Sample 1 (http://example.org/narrative#Metrics_Sample1), and Check-in (http://storybase.synthetic-identity.co/metrics/style) show variation across contexts while maintaining recognizable patterns.

[^metrics-note]: The variation in metrics reflects appropriate register shifts: talks are punchier (shorter sentences, higher active voice), transcripts are more conversational (longer sentences, some filler), check-ins are technical (higher jargon density).

---

### Transactions as Provenance

	Every claim in this presentation traces back to a transaction:
	
	**Tx_20251110T184512Z_sample1**: Narrative architecture extraction
	**2025-01-29T000000Z_sic-storybase-checkin**: Product/strategy check-in
	**Tx_20251109T223928Z_conj2025**: Conj 2025 talk extraction[^transactions]

Provenance is not an afterthought—it's the foundation.[^prov]

[^transactions]: The three transactions (http://example.org/narrative#Tx_20251110T184512Z_sample1, http://storybase.synthetic-identity.co/transaction/2025-01-29T000000Z_sic-storybase-checkin, http://example.org/narrative#Tx_20251109T223928Z_conj2025) establish the current state of the storyBASE graph.

[^prov]: All transactions use PROV-O (http://www.w3.org/ns/prov#) for provenance: prov:wasGeneratedBy links entities to transactions, prov:wasAttributedTo links to users, prov:wasAssociatedWith links to agents (storyTWIN), and prov:generatedAtTime provides timestamps.

---

###### The Vision
### AI that tells your story, as written

---

### Tagline

	AI that tells you a story as written[^tagline]

"As written" carries double meaning: *i.e.* (that is to say) and *as you wrote it*. The brand is **as written.ai**.[^tagline-note]

[^tagline]: Tagline (http://storybase.synthetic-identity.co/tagline/storybase) with note: "User-facing brand as written.ai; Latin i.e. meaning." The tagline encodes both the product promise (AI that respects your narrative) and the brand identity.

[^tagline-note]: The Latin *i.e.* (id est, "that is") connects to the brand name "Sic" (Latin for "thus" or "as written"), creating a coherent linguistic identity around fidelity to source material.

---

### From Vouch.io to storyBASE

	**Vouch.io**: Enterprise identity platform using immutable event logs and delegation chains
	**Sic**: AI memory company using narrative-driven knowledge graphs for AI individuals[^products]

Both apply the same principle: identity as append-only log, not mutable state.[^identity-model]

[^products]: Two products from the Conj 2025 extraction (urn:uuid:product-vouch-io, urn:uuid:product-sic) show the evolution from human identity systems to AI identity systems, both grounded in immutable state.

[^identity-model]: The identity model from Sample_1 (http://example.org/narrative#Theme_TransitionAsStateChange) frames "Personal transition (gender, professional) as functional transformation from immutable past states." This lived experience informs the technical architecture.

---

### Immutable Selves

	You are not a mutable object. You are the integral of your history.
	
	Your identity is not a profile to be updated. It's a log of facts, a sequence of state transitions, a narrative that compounds.[^immutable-selves]

This is true for humans, organizations, and AI agents.[^strategy]

[^immutable-selves]: The Immutable Identity theme (http://example.org/narrative#Theme_ImmutableIdentity) and the Functional Immutable Identity Architecture strategy (urn:uuid:strategy-functional-immutable-identity) connect personal identity to system design: "Applies Clojure principles (immutability, explicit state, functional composition, data-first design, knowledge graphs) to create trustworthy identity systems."

[^strategy]: The Strategy from Conj 2025 (urn:uuid:strategy-functional-immutable-identity) describes the approach: "Models identity as append-only event logs, authentication as pure functions, delegation as auditable chains" with differentiators "Immutable facts at the edge, verifiable receipts, graph-based resolution."

---

### What's Next

	**Build the marketplace**: Shareable narrative modules
	**Prove the model**: Crooked Media demo, public case studies
	**Extend the ontology**: More domains, deeper conviction modeling
	**Scale the community**: Programming-literate strategists who see the pattern[^next]

We're building the infrastructure for narrative-driven AI. Join us.[^call-to-action]

[^next]: The roadmap (http://storybase.synthetic-identity.co/roadmap/narrative-storybase) and case studies (http://storybase.synthetic-identity.co/case/studies-storybase) outline the path from prototype to platform.

[^call-to-action]: The Primary Actors (http://storybase.synthetic-identity.co/actor/primary-storybase) are "Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes"—the community we're building for.

---

## Now go tell your story, as written.

**storyBASE**: Git-native RDF knowledge graph for narrative-driven AI memory.

**as written.ai**: AI that tells you a story as written.

**Sic**: Thus. As written. Immutable.

For more: [github.com/synthetic-identity-co/storybase](https://github.com/synthetic-identity-co/storybase)