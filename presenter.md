# storyBASE^[#storybase-product]^
# AI memory that tells your story, as written.
###### A Git-native RDF knowledge graph for narrative-driven AI
	[#storybase-product]: storyBASE is an "RDF narrative source of truth that steers AI output, making it specific, controllable, aligned with organizational worldview" (Product Overview, transaction 2025-01-29).

storyBASE extends software development rigor—versioning, branching, collaboration—into strategy, content, and organizational memory^[#positioning]^. It replaces brittle role prompts with deep, operable persona descriptions encoded as versionable knowledge graphs.

	[#positioning]: "Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth" (Positioning Thesis, transaction 2025-01-29).

---

# What is storyBASE?

---

###### The Problem
# AI without memory is generic

High-quality AI output requires extensive context^[#market-context]^. Current models use search, but search is brittle—no version control, no provenance, no narrative coherence.

	[#market-context]: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory" (Market Opportunity, transaction 2025-01-29).

---

## The Solution
###### Git-native RDF knowledge graphs

storyBASE is an append-only transaction log that compiles into a semantic snapshot^[#data-lifecycle]^. Every fact has provenance. Every change is auditable. Every story is reproducible.

	[#data-lifecycle]: "Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove" (Data Model Lifecycle, transaction 2025-01-29).

---

### How It Works

---

###### Narrative Architecture
### Six domains, one story

storyBASE organizes knowledge into **Opportunity, Strategy, Product, Architecture, Organization, and Proof**^[#narrative-arch]^—the operating system for story-led strategy.

	[#narrative-arch]: The Narrative Architecture ontology defines six top-level domains that "align market opportunity, strategy, product, and organization so the same narrative flows from positioning to roadmap to proof" (Ontology, NarrativeArchitecture ConceptScheme).

Each domain contains structured concepts: from Market Context and Timing Thesis in Opportunity, to Solution Archetypes and Product Ladder in Product, to Case Studies and Metrics in Proof.

---

###### Transactions
### Immutable, append-only facts

Every change is a **transaction**^[#transactions]^: a SPARQL INSERT or TriG named graph, timestamped and attributed. Transactions never mutate—only add or retract.

	[#transactions]: Transactions are stored as immutable files in `.storybase` directories; the snapshot is "replay of sorted transactions" with "provenance in TX step" (Data Model Lifecycle, transaction 2025-01-29). Current prototype uses SPARQL; roadmap includes "move transactions from SPARQL to named graphs (TriG)" (Narrative-Driven Roadmap, transaction 2025-01-29).

The storyBASE currently contains **4 transactions**^[#tx-count]^, including extractions from voice memos, product check-ins, and conference talk proposals.

	[#tx-count]: Snapshot compiled from 4 transaction files: `1762897917add_style_metrics.sparql`, `1762897917add_solution_archetypes.sparql`, `1762800383add_sample1_narrative_architecture.sparql`, `1762731465sic-storybase-checkin.sparql`, `1762728019add_conj_talk_2025_extraction.sparql` (TRANSACTIONS input).

---

###### Compile
### Snapshot = f(transactions)

Run **compile** to replay all transactions in order^[#compile]^. The result: a Turtle snapshot—your single source of truth, ready to query with SPARQL.

	[#compile]: "Compile (replay transactions to Turtle snapshot)" is one of the core storyBASE capabilities (Modules Capabilities, transaction 2025-01-29). The system topology describes "hierarchical compile" across `.storybase` directories (System Topology, transaction 2025-01-29).

The current snapshot contains **673 triples**^[#snapshot-stats]^ across Narrative Architecture, Style, Conviction, and sample extractions.

	[#snapshot-stats]: Snapshot stats report "inserted: 584, deleted: 0, skippedDuplicates: 89" (SNAPSHOT.stats).

---

### The Tools

---

###### Extract
### RDF from input

**Extract** takes unstructured input—transcripts, memos, documents—and generates RDF triples^[#extract]^. It identifies themes, actors, style observations, and rubric assessments.

	[#extract]: "Extract (RDF from input)" is a core capability (Modules Capabilities, transaction 2025-01-29). The process is "interactive individuation (extract → diff → tx → review → commit)" (Process, transaction 2025-01-29).

Example: a voice memo becomes `Sample_1` with linked `Theme_ImmutableIdentity`, `Actor_ScarletDame`, and `StyleObs_AppendOnlyLog`^[#sample1]^.

	[#sample1]: Transaction `Tx_20251110T184512Z_sample1` extracted from an 11,800-character voice memo, creating themes (Immutable Identity, Transition as State Machine), actors (Scarlet Dame, Luke Vanderhart), style observations (brand stylization, idiolect phrasing, metaphor), and rubric assessments (Sample_1, transaction 2025-11-10).

---

###### Diff
### Semantic comparison

**Diff** compares proposed triples against the current snapshot^[#diff]^. It surfaces conflicts, duplicates, and novel claims—so you review *meaning*, not syntax.

	[#diff]: "Diff (semantic comparison)" is a core capability (Modules Capabilities, transaction 2025-01-29). The individuation pipeline includes "snapshot + message to transaction" with diff as a review step (Narrative-Driven Roadmap, transaction 2025-01-29).

---

###### Tx
### Propose a transaction

**Tx** generates a candidate transaction file^[#tx-tool]^. It's a pull request for your knowledge graph—review, refine, then commit.

	[#tx-tool]: "Tx (propose transaction)" is a core capability (Modules Capabilities, transaction 2025-01-29). The process is "extract → diff → tx → review → commit" (Process, transaction 2025-01-29).

---

###### Commit
### Append to Git

**Commit** appends the transaction to the log and pushes to Git^[#commit]^. Immutable. Auditable. Versionable.

	[#commit]: "Commit (append-only to Git)" is a core capability (Modules Capabilities, transaction 2025-01-29). GitHub integration includes "OAuth, webhooks, Actions" with "future GitHub Apps with scoped credentials" (Integration Points, transaction 2025-01-29).

---

###### Story
### Generate from snapshot

**Story** takes a `.story` file—YAML front matter + prompt—and generates output^[#story]^. The snapshot is the context; the prompt is the lens.

	[#story]: "Story generation (YAML front matter + prompt to model outputs)" is a core capability (Modules Capabilities, transaction 2025-01-29). GitHub Actions trigger story generation on "transaction or .story file changes" (Process, transaction 2025-01-29).

This presentation is a `.story` file^[#presenter-story]^. The prompt: "draft a presentation of the storyBASE using the provided format."

	[#presenter-story]: `/presenter.story` defines id, title, model (`anthropic/claude-sonnet-4.5`), and prompt referencing the iA Presenter format (STORIES input).

---

### The Architecture

---

###### System Topology
### n8n + MCP + Git

**n8n** orchestrates tools. **MCP server** exposes them to frontends (Agent.ai, ChatGPT, Open WebUI). **Git** is the database^[#topology]^.

	[#topology]: "n8n agent orchestrates tools; MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI); transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean" (System Topology, transaction 2025-01-29).

---

###### Dependencies
### Open-source semantic web stack

- **Apache Jena/Riot** (future RDF ops)^[#deps]^
- **GitHub** (version control, webhooks, Actions)
- **Open Router** (model access via Helicone)
- **Outseta** (auth/billing)
- **Open WebUI** (chat interface at aswritten.ai)

	[#deps]: "n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access)" (Dependencies Integrations, transaction 2025-01-29).

---

###### Data Model
### Immutable, provenance-first

Every triple links to a **transaction** via `prov:wasGeneratedBy`^[#prov]^. Every transaction links to an **agent** and **user**. The graph *is* the audit log.

	[#prov]: Transactions use PROV-O: `prov:wasAssociatedWith`, `prov:wasAttributedTo`, `prov:generatedAtTime` (e.g., `Tx_20251110T184512Z_sample1` attributed to `pleasetrythisathome`, associated with `storyTWIN`, generated `2025-11-10T18:45:12.711Z`; SNAPSHOT).

---

### The Roadmap

---

###### Near-term
### TriG, SHACL, ingestion

- **Named graphs** (TriG) for add/remove semantics^[#roadmap-trig]^
- **SHACL validation** for schema enforcement
- **File ingestion** via GitHub (auto-extract, auto-PR)
- **Evolved individuation pipeline** (snapshot + message → transaction)

	[#roadmap-trig]: "Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub" (Narrative-Driven Roadmap, transaction 2025-01-29).

---

###### Mid-term
### Marketplace, billing, demos

- **storyBASE marketplace** (share/fork knowledge graphs)^[#roadmap-market]^
- **Cost pass-through billing** (Outseta + Helicone)
- **Case study demos** (e.g., Crooked Media podcast auto-ingestion)

	[#roadmap-market]: Roadmap includes "storyBASE marketplace; cost pass-through billing" (Narrative-Driven Roadmap, transaction 2025-01-29). Planned demo: "Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)" (Case Studies, transaction 2025-01-29).

---

### The Style System

---

###### Style as Data
### Encode voice, measure drift

storyBASE includes a **Style** ontology^[#style-ontology]^: diction, tone, cadence, rhetorical devices, orthography, citation conventions, metrics, and review.

	[#style-ontology]: The Style top concept includes facets for "Diction & Word Choice, Tone & Voice, Grammar & Syntax, Cadence & Rhythm, Rhetorical Devices, Orthography & Spelling, Punctuation & Typography, Citation Conventions, Register & Formality, POV, Tense & Aspect, Inclusive Language, Localization, Style Metrics, Style Review" (Ontology, #Style).

---

###### Style Observations
### Annotated with Web Annotation

Style observations use **oa:Annotation** to link text spans to style concepts^[#style-obs]^. Example: `StyleObs_storyBASE` marks "storyBASE" as `BrandNameStylization` with note "CamelCase + CAPS suffix."

	[#style-obs]: `StyleObs_storyBASE` is an `oa:Annotation` with `oa:hasBody` → `BrandNameStylization`, `oa:hasTarget` → text position selector (start 1523, end 1532, exact "storyBASE"), note "CamelCase + CAPS suffix; brand identity marker" (Sample_1, transaction 2025-11-10).

---

###### Style Metrics
### Quantify voice

- **Average Sentence Length**: 15.2 (Sample_1)^[#metrics-sample1]^
- **Active Voice Ratio**: 0.85
- **Jargon Density**: 0.12
- **Type-Token Ratio**: 0.68
- **Conciseness**: 0.78

	[#metrics-sample1]: `StyleMetrics_1` for Sample_1: "Short sentences, high active voice, moderate jargon (technical audience), good lexical diversity, concise" (transaction 2025-11-11).

---

###### Rubric Assessments
### 9-dimension evaluation

Every sample is scored on **Register Fit, Phrasing, Cadence, Strategic Alignment, Audience Tailoring, Resonance, Flow, Novelty, Accuracy**^[#rubric]^.

	[#rubric]: The Style Rubric defines 9 dimensions linked to style facets: Register Fit (→ RegisterFormality, ToneVoice), Phrasing (→ IdiolectPhrasing, StockPhrases), Cadence (→ CadenceRhythm, ShortPunchyCadence), Strategic Alignment (→ StrategyOverview, NarrativeAnchor), Audience Tailoring (→ TailoringAudienceFit, AudienceFrames), Resonance (→ ResonanceUse, RhetoricalDevices), Flow (→ FlowCoherence, TransitionsNatural), Novelty (→ NoveltyOriginality, ClicheDensity), Accuracy (→ FactualAccuracy, CitationPresence) (Ontology, #StyleRubric).

Sample_1 scores: Register 4.0, Phrasing 3.5, Cadence 3.0, Strategy 4.5, Tailoring 4.0, Resonance 4.5, Flow 3.0, Novelty 4.0, Accuracy 4.0^[#rubric-sample1]^.

	[#rubric-sample1]: Rubric assessments for Sample_1 (voice memo, 11,800 chars): "Conversational, personal; active voice; fits talk/oratory context" (Register), "Idiolect present ('append-only log', 'functional transformation')" (Phrasing), "Variable; punchy clauses mixed with run-ons" (Cadence), "Directly advances narrative architecture thesis" (Strategy), "Audience = Clojure/tech community" (Tailoring), "Personal transition story as analogy for immutable state" (Resonance), "Coherent arc; some tangents" (Flow), "Fresh framing (identity as append-only log)" (Novelty), "Technical claims sound; no inline citations (acceptable for voice memo)" (Accuracy) (transaction 2025-11-10).

---

### The Conviction System

---

###### Conviction Levels
### From notion to foundation

Claims escalate through four levels^[#conviction-levels]^:

1. **Notion**: exploratory, open edges
2. **Stake**: proposed, connected, moveable
3. **Boulder**: settled, central, consensus-required
4. **Foundation**: underpinning, permanent unless refuted

	[#conviction-levels]: Conviction is "degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost" with ordered levels Notion → Stake → Boulder → Foundation (Ontology, #Conviction).

---

###### Conviction Aggregates
### Rolling metrics

Each claim tracks^[#conviction-agg]^:
- **Conviction score** (0–1)
- **Weight** (for thresholding)
- **Distance to narrative** (graph path length)
- **Individuation count** (unique, similar observations)
- **Rolling mean** (if numeric)
- **Computed at** (timestamp)

	[#conviction-agg]: `ConvictionAggregate` class maintains "rolling metrics for a claim: score, weight, distances, individuation counts, and last update time" with properties `convictionScore`, `convictionWeight`, `distanceToNarrative`, `individuationCount`, `rollingMean`, `rollingN`, `computedAt` (Ontology, #ConvictionAggregate).

---

### The Use Cases

---

###### Solution Archetypes
### Repeatable patterns

storyBASE encodes **Solution Archetypes**^[#archetypes]^: reusable end-to-end patterns with title, problem context, approach, capabilities, implementation path, outcomes, time-to-value, risks, metrics, and storyboard.

	[#archetypes]: "A Solution Archetype is a reusable end-to-end pattern that solves a class of problems with known steps, risks, and payoffs—accelerating sales and delivery" (Ontology, #SolutionArchetypes). Components include ArchetypeTitle, ProblemContext, ApproachPattern, RequiredCapabilities, ImplementationPath, OutcomesProof, TimeToValue, RisksMitigations, ArchetypeMetrics, ExampleStoryboard.

---

###### Archetype 1
### berecognized.id: Immutable Identification

**Problem**: Passwords and digital keys are mutable, siloed, vulnerable; no single source of truth for privileges^[#arch1-problem]^.

**Approach**: SSoT (Datomic) → datalog query → render to identification/privileges → event-driven transactions → append-only log → recompile^[#arch1-approach]^.

**Capabilities**: Datomic (SSoT), datalog (query), multimodal renderer, event system, single transactor^[#arch1-caps]^.

**Outcome**: Proof of provenance and authority innate; hash of last tx + SSoT state enables 'be recognized' property^[#arch1-outcome]^.

	[#arch1-problem]: ProblemContext_1: "Passwords and digital keys are mutable, siloed, and vulnerable; no single source of truth for privileges" with note "Triggering condition: fragmented, mutable identity state" (transaction 2025-11-11).
	[#arch1-approach]: ApproachPattern_1: "SSoT (Datomic) → datalog query → render to identification/privileges → event-driven transactions → append-only log → recompile" with note "Canonical flow applied to access control" (transaction 2025-11-11).
	[#arch1-caps]: RequiredCapabilities_1: "Datomic (SSoT), datalog (query), multimodal renderer, event system, single transactor" with note "Specific modules from Clojure ecosystem" (transaction 2025-11-11).
	[#arch1-outcome]: OutcomesProof_1: "Proof of provenance and authority innate; hash of last tx + SSoT state enables 'be recognized' property" with note "Expected metric: cryptographic proof of identity state" (transaction 2025-11-11).

---

###### Archetype 2
### aswritten.ai: Immutable AI Identity

**Problem**: AI models are black boxes; persona prompts mutate rendered state; no provenance or version control for AI identity^[#arch2-problem]^.

**Approach**: SSoT (RDF + git) → SPARQL query → render to AI memory/identity → event-driven transactions → append-only log → recompile^[#arch2-approach]^.

**Capabilities**: RDF graph, git versioning, SPARQL, multimodal renderer, event system, transactor^[#arch2-caps]^.

	[#arch2-problem]: ProblemContext_2: "AI models are black boxes; persona prompts mutate rendered state; no provenance or version control for AI identity" with note "Stakes: narrative manipulation, embedded propaganda, deepfakes" (transaction 2025-11-11).
	[#arch2-approach]: ApproachPattern_2: "SSoT (RDF + git) → SPARQL query → render to AI memory/identity → event-driven transactions → append-only log → recompile" with note "Same pattern, different stack: RDF instead of Datomic" (transaction 2025-11-11).
	[#arch2-caps]: RequiredCapabilities_2: "RDF graph, git versioning, SPARQL, multimodal renderer, event system, transactor" with note "Leverages semantic web + version control" (transaction 2025-11-11).

---

### The Samples

---

###### Sample 1
### Voice memo: Punch talk conceptual framing

**Source**: Voice memo, 11,800 characters, 2025-01-15^[#sample1-meta]^  
**Speaker**: Scarlet Dame  
**Theme**: Immutable Identity as Append-Only Log; Transition as State Machine  
**Actors**: Scarlet Dame, Luke Vanderhart  
**Anchor**: Narrative Architecture for Identity Systems  

	[#sample1-meta]: Sample_1: "Transcribed voice memo outlining narrative architecture for identity-as-append-only-log talk; speaker: Scarlet Dame" (transaction 2025-11-10).

---

###### Sample 2
### SIC / storyBASE / as written.ai Product & Strategy Check-in

**Source**: Spoken transcript, 18,437 characters, 2025-01-29^[#sample2-meta]^  
**Speaker**: Scarlet Dame  
**Topics**: Market opportunity, timing thesis, positioning, moat, mission, product overview, modules, roadmap, system topology, data lifecycle, integration points, process, case studies  

	[#sample2-meta]: Sample "SIC / storyBASE / as written.ai Product & Strategy Check-in": "Spoken transcript with conversational register and technical depth on storyBASE product evolution" (transaction 2025-01-29).

---

###### Sample 3
### Conj Talk 2025: Immutable Selves

**Source**: Conference talk proposal, 3,421 characters, 2025-01-01^[#sample3-meta]^  
**Opportunity**: Identity Vulnerability Crisis (deepfakes, synthetic identities, impersonation fraud)  
**Strategy**: Functional Immutable Identity Architecture (Clojure principles applied to identity)  
**Products**: Vouch.io (enterprise identity), Sic (AI memory)  
**Proof**: Conj 2025 Experience Report (threaded diagrams, optional demo)  

	[#sample3-meta]: Sample "Conj Talk 2025: Immutable Selves" (transaction 2025-11-09). Opportunity: "Centralized, mutable identity systems vulnerable to deepfakes, synthetic identities, and impersonation fraud" (Identity Vulnerability Crisis). Strategy: "Applies Clojure principles (immutability, explicit state, functional composition, data-first design, knowledge graphs) to create trustworthy identity systems" (Functional Immutable Identity Architecture). Products: Vouch.io ("Enterprise identity platform using immutable event logs and delegation chains"), Sic ("AI memory company using narrative-driven knowledge graphs to create AI individuals with deterministic individuality and provenance"). Proof: "Conference talk and experience report" with "Threaded diagrams from model to implementation, optional short demo with canned fallback" for "Clojure developers and functional programming practitioners" (Conj 2025 Experience Report).

---

### The Stories

---

###### README.story
### Autogenerated repo README

**Prompt**: "Summarize the current state of the storyBASE. Create a section for each story. Summarize the intent of the story, its relationship to the whole, and a brief summary of how it will be approached from the current storyBASE state. Briefly summarize the repository structure and a description of each asset. Briefly summarize each transaction and its significance to the storyBASE graph, stories, and assets. Include mermaid charts where helpful."^[#readme-story]^

	[#readme-story]: `/README.story` defines id `README`, title "storyBASE repo README", model `anthropic/claude-sonnet-4.5`, destination `/` (STORIES input).

---

###### presenter.story
### This presentation

**Prompt**: "Use the storyBASE to draft a presentation of the storyBASE using the provided format. Focus on presenting clear narrative statements in the slide copy and provide a brief talk track for each slide. Cite important claims with footnotes to the storyBASE and explain context in the footnote."^[#presenter-story-prompt]^

	[#presenter-story-prompt]: `/presenter.story` prompt (STORIES input).

---

###### conj-talk-2025.story
### Immutable Selves Talk

**Prompt**: "Use the storyBASE to draft the clojure conj talk using the provided format. Focus on presenting clear narrative statements in the slide copy and provide a brief talk track for each slide. The goal of the talk is to lay out: My personal history and professional journey from developer to organizational strategist implementing clojure principles across digital identity systems. A working model for what identity is in physical, digital, and AI space. The failure of centralized, mutable, and object oriented human and AI identity paradigms. Clojure principles from code to structure. Identity as transactions. Vouch.io + As Written case studies. Cite important claims with footnotes to the storyBASE and explain context in the footnote."^[#conj-story-prompt]^

	[#conj-story-prompt]: `/conj-talk-2025.story` prompt (STORIES input).

---

### The Transactions

---

###### Transaction 1
### add_style_metrics.sparql

**Date**: 2025-11-11  
**Content**: Adds `StyleMetrics_1` for Sample_1 with average sentence length 15.2, active voice ratio 0.85, jargon density 0.12, type-token ratio 0.68, conciseness 0.78^[#tx1]^.

	[#tx1]: Transaction `1762897917add_style_metrics.sparql` inserts `StyleMetrics_1` with note "Short sentences, high active voice, moderate jargon (technical audience), good lexical diversity, concise" (TRANSACTIONS).

---

###### Transaction 2
### add_solution_archetypes.sparql

**Date**: 2025-11-11  
**Content**: Adds two solution archetypes: berecognized.id (Datomic-based immutable identification) and aswritten.ai (RDF-based immutable AI identity)^[#tx2]^.

	[#tx2]: Transaction `1762897917add_solution_archetypes.sparql` inserts `Archetype_1` (berecognized.id) and `Archetype_2` (aswritten.ai) with problem contexts, approach patterns, required capabilities, and outcomes (TRANSACTIONS).

---

###### Transaction 3
### add_sample1_narrative_architecture.sparql

**Date**: 2025-11-10  
**Content**: Extracts Sample_1 (voice memo), themes (Immutable Identity, Transition as State Machine), actors (Scarlet Dame, Luke Vanderhart), anchor (Narrative Architecture for Identity Systems), 6 style observations, 9 rubric assessments, and style metrics^[#tx3]^.

	[#tx3]: Transaction `1762800383add_sample1_narrative_architecture.sparql` (Tx_20251110T184512Z_sample1) inserts Sample_1, themes, actors, anchor, style observations (storyBASE brand stylization, append-only log idiolect, UI state machine metaphor, transition analogy, short clause cadence, first-person POV), rubric assessments (Register 4.0, Phrasing 3.5, Cadence 3.0, Strategy 4.5, Tailoring 4.0, Resonance 4.5, Flow 3.0, Novelty 4.0, Accuracy 4.0), and metrics (avg sentence length 28.5, active voice 0.75, jargon 0.12) (TRANSACTIONS).

---

###### Transaction 4
### sic-storybase-checkin.sparql

**Date**: 2025-11-09  
**Content**: Extracts Sample (SIC check-in), opportunity (storyBASE market), timing thesis, primary actors, positioning thesis, moat leverage, tagline, mission, product overview, modules, dependencies, roadmap, system topology, data lifecycle, integration points, role topology, process, case studies, 10 style observations, 9 rubric assessments, and style metrics^[#tx4]^.

	[#tx4]: Transaction `1762731465sic-storybase-checkin.sparql` (transaction 2025-01-29) inserts sample (18,437 chars), opportunity ("High-quality AI output requires extensive context"), timing thesis ("Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management"), primary actors ("Programming-literate entrepreneurs, designers, developers, consultants"), positioning thesis ("Extend software development rigor"), moat leverage ("Git-native, versionable, branchable AI memory"), tagline ("AI that tells you a story as written"), mission ("Extend software development rigor into strategy, content, marketing"), product overview ("Initial prototype in n8n; tools include compile, ontology, extract, diff, tx, commit; MCP server; open WebUI at as written.ai; GitHub Actions for story generation"), modules ("Compile, extract, diff, tx, commit, story generation"), dependencies ("n8n, MCP, GitHub, Apache Jena/Riot, Docker Compose, Open WebUI, Outseta, Helicone, Open Router"), roadmap ("TriG, SHACL, individuation pipeline, file ingestion, marketplace, billing"), system topology ("n8n agent orchestrates tools; MCP server exposes to frontends; transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean"), data lifecycle ("Append-only transaction log; immutable files; snapshot = replay of sorted transactions"), integration points ("GitHub, Open Router, Outseta, MCP, future GitHub Apps"), role topology ("Programming-literate users; admin vs. read-write vs. read-only modes; GitHub role-based access"), process ("Interactive individuation vs. automated ingestion; story generation triggered by transaction or .story file changes"), case studies ("Planned demo: Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations"), 10 style observations (brand stylization, idiolect phrasing, verb choice, simile, tone, jargon policy, sentence length variation, parallelism, rhetorical question, caret bracket marker), 9 rubric assessments (Register 3.5, Phrasing 3.0, Cadence 3.0, Strategic Alignment 4.0, Audience Tailoring 3.5, Resonance 3.0, Flow 3.0, Novelty 3.5, Accuracy 4.0), and style metrics (avg sentence length 35.2, active voice 0.72, jargon 0.18, type-token 0.42) (TRANSACTIONS).

---

###### Transaction 5
### add_conj_talk_2025_extraction.sparql

**Date**: 2025-11-09  
**Content**: Extracts Sample (Conj Talk 2025), opportunity (Identity Vulnerability Crisis), strategy (Functional Immutable Identity Architecture), products (Vouch.io, Sic), proof (Conj 2025 Experience Report), architecture (Immutable Identity System Patterns), organizations (Sic, Vouch.io), 11 style observations, 4 rubric assessments, and style metrics^[#tx5]^.

	[#tx5]: Transaction `1762728019add_conj_talk_2025_extraction.sparql` (Tx_20251109T223928Z_conj2025) inserts sample (3,421 chars), opportunity ("Centralized, mutable identity systems vulnerable to deepfakes, synthetic identities, and impersonation fraud"), strategy ("Applies Clojure principles (immutability, explicit state, functional composition, data-first design, knowledge graphs) to create trustworthy identity systems"), products (Vouch.io: "Enterprise identity platform using immutable event logs and delegation chains"; Sic: "AI memory company using narrative-driven knowledge graphs to create AI individuals with deterministic individuality and provenance"), proof ("Conference talk and experience report" with "Threaded diagrams from model to implementation, optional short demo with canned fallback" for "Clojure developers and functional programming practitioners"), architecture ("Append-only event logs with verifiable receipts, authentication as pure function at the edge, delegation as signed append-only events, knowledge graphs for entity and role resolution" with principles "Immutability, functional composition, explicit state management, data-first design"), organizations (Sic: "Founder" with "Narrative-driven knowledge graphs for AI individuals"; Vouch.io: "Former Chief Strategist, current strategic advisor" with "Enterprise identity and delegation"), 11 style observations (brand name styling Vouch.io, technical terms append-only event logs, authentication as pure functions, persistent logs and knowledge graphs, brand name Sic, rhetorical structure triadic enumeration, problem to solution bridge, technical reframing identity, technical reframing trust, list structure parallel construction, personal identity lens), 4 rubric assessments (Clarity 4.5, Technical Depth 4.8, Narrative Coherence 4.6, Audience Engagement 4.3), and style metrics (avg sentence length 22.4, technical density 0.68, active voice 0.71) (TRANSACTIONS).

---

### Why Now?

---

###### Timing Thesis
### 2024–2026 window

Convergence of **prompt engineering maturity**, **multi-agent workflows**, and **demand for organizational AI memory** creates a window for narrative-driven context management^[#timing]^.

	[#timing]: "Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management" with timestamp window "2024-2026" (Timing Thesis, transaction 2025-01-29).

---

### Who Is It For?

---

###### Primary Actors
### Programming-literate worldview manipulators

**Entrepreneurs, designers, developers, consultants** who manipulate worldview and see perspective changes^[#actors]^.

	[#actors]: "Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes" (Primary Actors, transaction 2025-01-29).

---

### What's Next?

---

###### Roadmap Highlights
### TriG, SHACL, marketplace

1. **Named graphs** (TriG) for add/remove semantics
2. **SHACL validation** for schema enforcement
3. **Evolved individuation pipeline** (snapshot + message → transaction)
4. **File ingestion** via GitHub (auto-extract, auto-PR)
5. **storyBASE marketplace** (share/fork knowledge graphs)
6. **Cost pass-through billing** (Outseta + Helicone)

All driven by the narrative: what makes the story more true, more usable, more shareable^[#roadmap-narrative]^.

	[#roadmap-narrative]: Roadmap is "narrative-driven" and "related to core narrative expansion" (Narrative-Driven Roadmap, transaction 2025-01-29).

---

## Try It

Open WebUI at **aswritten.ai**^[#webui]^  
MCP server for Agent.ai, ChatGPT, Claude Desktop  
GitHub repo (coming soon)

	[#webui]: "Open WebUI at as written.ai" (Product Overview, transaction 2025-01-29).

---

## Questions?

**Scarlet Dame**  
Founder, Synthetic Identity Co.  
Former Chief Strategist, Vouch.io^[#scarlet]^

	[#scarlet]: Scarlet Dame is "Founder" of Sic and "Former Chief Strategist, current strategic advisor" at Vouch.io (Organizations, transaction 2025-11-09).

---

# AI memory that tells your story, as written.