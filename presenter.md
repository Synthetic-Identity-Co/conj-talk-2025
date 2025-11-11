---

# storyBASE[^intro^]
# AI memory that tells your story, as written.
###### A Git-native RDF knowledge graph for narrative-driven AI

[^intro^]: storyBASE is an RDF narrative source of truth that steers AI output, making it specific, controllable, and aligned with organizational worldview. From transaction `storyBASE Product Overview` (2025-01-29).

storyBASE extends software development rigor—versioning, branching, collaboration—into strategy, content, and marketing through a versionable, narrative-driven AI memory system.

---

# The Problem
## AI without memory is generic

Current AI models use search for context, but lack a persistent, versionable source of truth. High-quality output requires extensive context that's specific, controllable, and aligned with your worldview[^context^].

[^context^]: From `storyBASE Market Opportunity`: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory."

---

###### Why Now
## The Convergence

Prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory create a window for narrative-driven context management[^timing^].

[^timing^]: `storyBASE Timing Thesis` (2024-2026): "Convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management."

The window is 2024–2026. We're building in it.

---

## What is storyBASE?

	Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics—replacing brittle role prompts with deep, operable persona descriptions[^moat^].

[^moat^]: From `storyBASE Moat Leverage`: "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions."

An RDF knowledge graph that becomes your AI's single source of truth.

---

### The Architecture
	Append-only transaction log → immutable snapshot → SPARQL query → AI context

storyBASE uses an append-only transaction log where immutable files replay to create snapshots. Provenance lives in each transaction. Future: named graphs for add/remove operations[^lifecycle^].

[^lifecycle^]: `storyBASE Data Model Lifecycle`: "Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove."

---

### Core Capabilities

	1. **Compile**: Replay transactions to Turtle snapshot
	2. **Extract**: RDF from input
	3. **Diff**: Semantic comparison
	4. **Tx**: Propose transaction
	5. **Commit**: Append-only to Git
	6. **Story**: YAML front matter + prompt → model outputs[^capabilities^]

[^capabilities^]: From `storyBASE Modules Capabilities`: "Compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs)."

---

###### System Topology
### How It Works

n8n agent orchestrates tools. MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI). Transactions live in `.storybase` directories. Hierarchical compile. Docker Compose on Digital Ocean[^topology^].

[^topology^]: `storyBASE System Topology`: "n8n agent orchestrates tools; MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI); transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean."

---

### Two Workflows

	**Interactive Individuation**: extract → diff → tx → review → commit
	
	**Automated Ingestion**: file upload → extraction → PR
	
Story generation triggers on transaction or `.story` file changes[^process^].

[^process^]: `storyBASE Process`: "Interactive individuation (extract → diff → tx → review → commit) vs. automated ingestion (file upload → extraction → PR); story generation triggered by transaction or .story file changes."

---

## Who It's For

Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes[^actors^].

[^actors^]: `storyBASE Primary Actors`: "Programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes."

People who understand that narrative is infrastructure.

---

###### Integration Points
### The Stack

	- **GitHub**: OAuth, webhooks, Actions
	- **Open Router**: API proxy via Helicone
	- **Outseta**: OIDC, billing
	- **MCP protocol**: Tool exposure
	- **Future**: GitHub Apps with scoped credentials[^integrations^]

[^integrations^]: `storyBASE Integration Points`: "GitHub (OAuth, webhooks, Actions); Open Router (API proxy via Helicone); Outseta (OIDC, billing); MCP protocol (tool exposure); future GitHub Apps with scoped credentials."

---

### Dependencies

n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access)[^dependencies^].

[^dependencies^]: `storyBASE Dependencies Integrations`: "n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access)."

---

## Roadmap

	1. Move transactions from SPARQL to named graphs (TriG)
	2. Add SHACL validation
	3. Evolved individuation pipeline (snapshot + message → transaction)
	4. File ingestion via GitHub
	5. storyBASE marketplace
	6. Cost pass-through billing[^roadmap^]

[^roadmap^]: `storyBASE Narrative-Driven Roadmap`: "Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing."

---

###### Demo
### Planned Case Study

Crooked Media podcast transcripts auto-ingested. Stories auto-update. Perspectival operations: start with NPR voice, evolve with OpenAI perspective[^case^].

[^case^]: `storyBASE Case Studies`: "Planned demo: Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)."

Narrative as a living, queryable, versionable asset.

---

### Role Topology

Programming-literate users. Admin vs. read-write vs. read-only modes. GitHub role-based access. Future: scoped permissions via GitHub Apps[^roles^].

[^roles^]: `storyBASE Role Topology`: "Programming-literate users; admin vs. read-write vs. read-only modes; GitHub role-based access; future scoped permissions via GitHub Apps."

---

## The Mission

Extend software development rigor into strategy, content, marketing. Provide versionable, collaborative, narrative-driven AI memory[^mission^].

[^mission^]: `storyBASE Mission`: "Extend software development rigor into strategy, content, marketing; provide versionable, collaborative, narrative-driven AI memory."

---

###### Brand
### as written.ai

	"AI that tells you a story as written"

User-facing brand: **as written.ai**. Latin *i.e.* meaning—exactly as stated, with provenance[^tagline^].

[^tagline^]: `storyBASE Tagline`: "AI that tells you a story as written" with note "User-facing brand as written.ai; Latin i.e. meaning."

---

## Current State

Initial prototype in n8n. Tools: compile, ontology, extract, diff, tx, commit. MCP server live. Open WebUI at as written.ai. GitHub Actions for story generation[^overview^].

[^overview^]: `storyBASE Product Overview`: "Initial prototype in n8n; tools include compile, ontology, extract, diff, tx, commit; MCP server; open WebUI at as written.ai; GitHub Actions for story generation."

This presentation was generated from the storyBASE.

---

### Style Observations

	1. CamelCase 'storyBASE' with internal capitalization
	2. Conversational filler 'you know' signals informal register
	3. Power verb 'extend' frames value proposition
	4. Technical jargon (RDF, canonization, skolemization) assumes literate audience[^style^]

[^style^]: From `Style Observations` 1, 2, 3, 6 in transaction 2025-01-29.

---

###### Metrics
### Style Profile

	- Average sentence length: 35.2
	- Active voice ratio: 0.72
	- Jargon density: 0.18
	- Type-token ratio: 0.42

Conversational transcript with high jargon and active voice[^metrics^].

[^metrics^]: `Style metrics`: "Average sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42" with note "Conversational transcript with high jargon and active voice."

---

## Rubric Scores

	- **Strategic Alignment**: 4.0/5 — Clear positioning, mission, moat, roadmap
	- **Register Fit**: 3.5/5 — Conversational, informal, direct
	- **Accuracy**: 4.0/5 — Technical details specific; citation markers present[^rubric^]

[^rubric^]: From `Rubric assessments` (Strategic Alignment, Register Fit, Accuracy) in transaction 2025-01-29.

---

### What Makes It Different

Git-native. Versionable. Branchable. Narrative-first. Replaces brittle role prompts with deep persona descriptions that encode style, conviction, and metrics.

It's not a vector database. It's a knowledge graph with provenance.

---

## The Opportunity

AI prompt engineering and organizational memory converge. RDF-based narrative source of truth enables specific, controllable, versionable AI memory where current models use search[^opportunity^].

[^opportunity^]: `storyBASE Market Opportunity`: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory" in market context "AI prompt engineering and organizational memory."

---

###### Positioning
### The Thesis

Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth[^positioning^].

[^positioning^]: `storyBASE Positioning Thesis`: "Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth."

---

## Try It

	- **Open WebUI**: as written.ai
	- **GitHub**: github.com/synthetic-identity-co/storyBASE
	- **MCP Server**: Connect via Agent.ai or ChatGPT

All transactions are append-only. All snapshots are reproducible. All stories cite their sources.

---

# AI memory that tells your story, as written.

	storyBASE: Git-native RDF knowledge graph for narrative-driven AI

**as written.ai**