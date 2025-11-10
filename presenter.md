# SIC
# AI memory that tells your story, as written.
###### A presentation of storyBASE
	This presentation introduces storyBASE: a Git-native RDF knowledge graph that gives AI deterministic memory and narrative-driven individuality.[#storybase-overview]
	[#storybase-overview]: storyBASE is described as an "RDF narrative source of truth that steers AI output, making it specific, controllable, aligned with organizational worldview" (Product Overview, transaction 2025-01-29).

---

# storyBASE
## AI memory that remembers how you write

---

###### The Problem
### AI without memory is generic

	High-quality AI output requires extensive context. Current models use search and retrieval, but lack a versionable, narrative-driven source of truth.[#market-opportunity]
	[#market-opportunity]: The storyBASE Market Opportunity identifies that "high-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory" (Opportunity, transaction 2025-01-29).

Without persistent memory, every AI interaction starts from zero. Prompts grow brittle. Style drifts. Facts contradict. Organizations lose their voice.

---

###### The Opportunity
### Narrative-driven context management

	The convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates a window for narrative-driven solutions.[#timing-thesis]
	[#timing-thesis]: The storyBASE Timing Thesis states "convergence of prompt engineering maturity, multi-agent workflows, and demand for organizational AI memory creates window for narrative-driven context management" with a timestamp window of "2024-2026" (Timing Thesis, transaction 2025-01-29).

Organizations need AI that sounds like them, remembers their decisions, and evolves with their strategy—not generic assistants that forget yesterday's conversation.

---

### What is storyBASE?

	A Git-native RDF knowledge graph that encodes your narrative, style, and conviction—giving AI deterministic memory and versionable individuality.[#what-is-it]
	[#what-is-it]: Product Overview defines storyBASE as "RDF narrative source of truth (storyBASE) that steers AI output, making it specific, controllable, aligned with organizational worldview" (transaction 2025-01-29).

storyBASE replaces brittle role prompts with deep, operable persona descriptions. It's version-controlled, branchable, and collaborative—extending software development rigor into strategy, content, and organizational operations.

---

## How It Works
	From transactions to stories

---

### Append-only transaction log

	Every change is an immutable transaction. The snapshot is a replay of sorted transactions—provenance built in.[#data-lifecycle]
	[#data-lifecycle]: The Data Model Lifecycle describes "append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove" (transaction 2025-01-29).

Like Git for narrative. Every edit, extraction, and assertion is recorded. You can branch, diff, and merge worldviews.

---

### Extract → Diff → TX → Commit

	Interactive individuation: extract RDF from input, compare to snapshot, propose transaction, review, commit.[#process]
	[#process]: The storyBASE Process describes "interactive individuation (extract → diff → tx → review → commit) vs. automated ingestion (file upload → extraction → PR); story generation triggered by transaction or .story file changes" (transaction 2025-01-29).

Automated ingestion for scale: upload files, extract facts, open pull request. Human-in-the-loop for precision. Both paths preserve provenance.

---

### Story generation

	YAML front matter + prompt → model outputs. Stories auto-update when transactions or .story files change.[#modules-capabilities]
	[#modules-capabilities]: Modules Capabilities include "story generation (YAML front matter + prompt to model outputs)" alongside compile, extract, diff, tx, and commit tools (transaction 2025-01-29).

Write a `.story` file. Define the model, destination, and prompt. GitHub Actions regenerate outputs when the storyBASE evolves. Your narrative stays fresh.

---

## The Stack
	n8n, MCP, Git, RDF

---

### System topology

	n8n agent orchestrates tools. MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI). Transactions in .storybase directories. Docker Compose on Digital Ocean.[#system-topology]
	[#system-topology]: System Topology describes "n8n agent orchestrates tools; MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI); transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean" (transaction 2025-01-29).

The architecture is modular: compile snapshots, extract RDF, diff semantics, propose transactions, commit to Git. Each tool is a composable primitive.

---

### Integrations

	GitHub (OAuth, webhooks, Actions). Open Router (API proxy via Helicone). Outseta (OIDC, billing). MCP protocol (tool exposure). Future: GitHub Apps with scoped credentials.[#integration-points]
	[#integration-points]: Integration Points list "GitHub (OAuth, webhooks, Actions); Open Router (API proxy via Helicone); Outseta (OIDC, billing); MCP protocol (tool exposure); future GitHub Apps with scoped credentials" (transaction 2025-01-29).

Open standards. Pluggable models. Cost pass-through billing. You own your data; we provide the rails.

---

## What Makes It Different
	Git-native, narrative-driven, versionable

---

### Moat: versionable AI memory

	Git-native, branchable AI memory encoding style, conviction, narrative metrics. Replaces brittle role prompts with deep, operable persona descriptions.[#moat-leverage]
	[#moat-leverage]: Moat Leverage describes "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions" (transaction 2025-01-29).

You can branch a worldview. Test a positioning shift. Merge learnings. Roll back mistakes. AI memory becomes as rigorous as code.

---

### Style as data

	Average sentence length, active voice ratio, jargon density, type-token ratio—all tracked. Style observations and rubric assessments in the graph.[#style-metrics]
	[#style-metrics]: Style Metrics record "average sentence length 35.2, active voice ratio 0.72, jargon density 0.18, type-token ratio 0.42" with a note "conversational transcript with high jargon and active voice" (transaction 2025-01-29).

storyBASE doesn't just remember facts—it remembers *how you say them*. Brand voice becomes measurable, testable, evolvable.

---

### Conviction levels

	Claims move from Notion → Stake → Boulder → Foundation. Conviction governs change cost and decision weight.[#conviction]
	[#conviction]: The Conviction ontology defines four levels: Notion (exploratory), Stake (proposed), Boulder (settled, hard to move), and Foundation (underpinning, effectively permanent) with sequential escalation paths encoded via xkos:next/previous.

Not all facts are equal. Some are exploratory; others are foundational. storyBASE tracks settledness so you know what's safe to change and what requires consensus.

---

## Roadmap
	Named graphs, SHACL, marketplace

---

### Near-term: TriG and validation

	Move transactions from SPARQL to named graphs (TriG). Add SHACL validation. Implement evolved individuation pipeline (snapshot + message → transaction).[#narrative-roadmap]
	[#narrative-roadmap]: Narrative-Driven Roadmap describes "move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing" (transaction 2025-01-29).

Named graphs let us track add/remove operations cleanly. SHACL ensures the graph stays well-formed. The individuation pipeline becomes a single, elegant flow.

---

### Medium-term: file ingestion and marketplace

	GitHub file ingestion via webhooks. storyBASE marketplace for shared ontologies and templates. Cost pass-through billing.[#narrative-roadmap]

Upload a podcast transcript. Extract facts. Open a PR. Approve. Your storyBASE grows. Share your ontology; adopt others'. Pay only for what you use.

---

## Case Study Preview
	Crooked Media demo

	Planned demo: Crooked Media podcast transcripts auto-ingested. Stories auto-update. Perspectival operations (e.g., start with NPR voice, evolve with OpenAI style).[#case-studies]
	[#case-studies]: Case Studies describe "planned demo: Crooked Media podcast transcripts auto-ingested; stories auto-update; perspectival operations (e.g., start with NPR, evolve with OpenAI)" (transaction 2025-01-29).

Imagine: every episode becomes a transaction. The storyBASE learns the hosts' cadence, their recurring themes, their evolving positions. Stories regenerate automatically. The archive becomes a living, queryable memory.

---

## Who It's For
	Programming-literate strategists

	Primary actors: programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes.[#primary-actors]
	[#primary-actors]: Primary Actors are described as "programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes" (transaction 2025-01-29).

If you think in systems, value provenance, and want AI that remembers your decisions—storyBASE is for you.

---

## Positioning
	Extend software rigor into strategy

	Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth.[#positioning-thesis]
	[#positioning-thesis]: Positioning Thesis states "extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth" (transaction 2025-01-29).

Code has Git. Strategy has storyBASE. Same discipline. Same collaboration model. Different domain.

---

## Mission
	Versionable, collaborative, narrative-driven AI memory

	Extend software development rigor into strategy, content, marketing; provide versionable, collaborative, narrative-driven AI memory.[#mission]
	[#mission]: Mission is "extend software development rigor into strategy, content, marketing; provide versionable, collaborative, narrative-driven AI memory" (transaction 2025-01-29).

We believe organizations deserve AI that remembers, evolves, and speaks with their voice—not generic assistants that forget.

---

## Tagline
# AI that tells you a story as written

	User-facing brand: as written.ai. Latin "i.e." meaning—"that is to say."[#tagline]
	[#tagline]: Tagline is "AI that tells you a story as written" with note "user-facing brand as written.ai; Latin i.e. meaning" (transaction 2025-01-29).

---

## Try It
	Open WebUI at as written.ai

	MCP server exposes tools to Agent.ai, ChatGPT, Open WebUI. GitHub Actions regenerate stories on commit.[#product-overview]
	[#product-overview]: Product Overview mentions "MCP server; open WebUI at as written.ai; GitHub Actions for story generation" (transaction 2025-01-29).

Visit as written.ai. Connect your GitHub. Start a storyBASE. Watch your narrative become queryable, versionable, alive.

---

## Questions?

	For more: check the repo, read the transactions, explore the ontology.

This presentation was generated from the storyBASE itself—proof that the system works.