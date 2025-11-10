# storyBASE
## AI memory that tells your story, as written.

A Git-native RDF knowledge graph for narrative-driven AI memory and organizational strategy.

---

## What is storyBASE?

storyBASE is an RDF narrative source of truth that steers AI output, making it specific, controllable, and aligned with organizational worldview[^what-is]. It extends software development rigor—versioning, branching, collaboration—into strategy, content, marketing, and organizational operations[^positioning].

[^what-is]: From Product Overview: "RDF narrative source of truth (storyBASE) that steers AI output, making it specific, controllable, aligned with organizational worldview." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

[^positioning]: From Positioning Thesis: "Extend software development rigor (versioning, branching, collaboration) into strategy, content, marketing, organizational operations via RDF narrative source of truth." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

---

## The Problem

High-quality AI output requires extensive context. Current models use search, but lack specific, controllable, versionable memory[^opportunity]. Organizations need AI that remembers their worldview, style, and strategic narrative—not generic responses.

[^opportunity]: From Market Opportunity: "High-quality AI output requires extensive context; current models use search, but RDF-based narrative source of truth enables specific, controllable, versionable AI memory." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

---

## The Solution

storyBASE replaces brittle role prompts with deep, operable persona descriptions encoded in RDF[^moat]. It provides:

- **Git-native versioning** for narrative evolution
- **Branchable perspectives** for multi-stakeholder alignment
- **Append-only transaction logs** for provenance
- **Style, conviction, and narrative metrics** for governance

[^moat]: From Moat Leverage: "Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics; replaces brittle role prompts with deep, operable persona descriptions." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

---

## How It Works

### 1. Extract
Convert input (transcripts, documents, conversations) into RDF triples using the storyBASE ontology[^modules].

### 2. Diff
Semantically compare proposed changes against the current snapshot to surface conflicts and novelty.

### 3. Commit
Append transactions to Git as immutable SPARQL files, maintaining full provenance[^data-model].

### 4. Compile
Replay sorted transactions into a Turtle snapshot—the canonical state of the narrative graph.

### 5. Generate
Use the snapshot as context for AI models to produce stories, presentations, and artifacts aligned with your narrative.

[^modules]: From Modules & Capabilities: "Compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs)." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

[^data-model]: From Data Model Lifecycle: "Append-only transaction log; immutable files; snapshot = replay of sorted transactions; provenance in TX step; future named graphs for add/remove." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

---

## Architecture

storyBASE runs on a **Docker Compose stack** with:

- **n8n** for agent orchestration
- **MCP server** exposing tools to frontends (Agent.ai, ChatGPT, Open WebUI)
- **GitHub** for version control and webhooks
- **Open Router** (via Helicone) for model access
- **Outseta** for auth and billing[^topology]

Transactions live in `.storybase` directories. The system compiles hierarchically, allowing nested contexts and scoped narratives.

[^topology]: From System Topology: "n8n agent orchestrates tools; MCP server exposes to frontends (Agent.ai, ChatGPT, Open WebUI); transactions in .storybase directories; hierarchical compile; Docker Compose on Digital Ocean." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

---

## Narrative Architecture Ontology

storyBASE is built on a **Narrative Architecture** ontology with six core domains[^ontology]:

1. **Opportunity** – Market context, actors, timing
2. **Strategy** – Positioning, moat, narrative anchor
3. **Product** – Capabilities, flows, solution archetypes
4. **Architecture** – System topology, data model, integrations
5. **Organization** – Roles, processes, change management
6. **Proof** – Case studies, outcomes, metrics

Plus two cross-cutting domains:

- **Style** – Voice, cadence, rhetorical devices, metrics
- **Conviction** – Degree of settledness (Notion → Stake → Boulder → Foundation)

[^ontology]: The Narrative Architecture ontology defines a SKOS concept scheme with top concepts for Opportunity, Strategy, Product, Architecture, Organization, Proof, Templates, Calibration, Style, and Conviction. See ontology.rdf in this repository.

---

## Current State

### Transactions
The storyBASE currently contains **4 transactions**:

1. **Scarlet Dame Sample** (2025-10-30) – ~500k character blog corpus with mission, vision, tagline, style observations, and rubric assessments[^scarlet].
2. **Narrative Architecture Sample** (2025-11-10) – Voice memo on identity-as-append-only-log, with themes, actors, and style metrics[^sample1].
3. **SIC/storyBASE Check-in** (2025-01-29) – Product overview, roadmap, and strategic positioning[^checkin].
4. **Conj Talk 2025** (2025-11-09) – Conference proposal on immutable identity systems[^conj].

[^scarlet]: Transaction: Tx_20251030T150539Z_scarletdame. Includes Mission ("To transform personal experience into art through daily creative practice"), Vision ("A world where artists own their platforms"), and Tagline ("Process as Product, Art as Artifact").

[^sample1]: Transaction: Tx_20251110T184512Z_sample1. Themes include "Immutable Identity as Append-Only Log" and "Transition as State Machine." Actors: Scarlet Dame (speaker), Luke Vanderhart.

[^checkin]: Transaction: 2025-01-29T000000Z_sic-storybase-checkin. Defines storyBASE mission, moat, timing thesis, and product capabilities.

[^conj]: Transaction: Tx_20251109T223928Z_conj2025. Opportunity: "Identity Vulnerability Crisis." Strategy: "Functional Immutable Identity Architecture." Products: Vouch.io, Sic.

### Stories
Three `.story` files define generation targets:

- **README.story** – Auto-generated repository overview
- **presenter.story** – iA Presenter slide deck for storyBASE
- **conj-talk-2025.story** – Clojure Conj talk on immutable identity

---

## Roadmap

### Near-term
- Move from SPARQL to **TriG** (named graphs for add/remove)[^roadmap]
- Add **SHACL validation** for transaction integrity
- Implement **evolved individuation pipeline** (snapshot + message → transaction)
- **File ingestion via GitHub** (upload → extraction → PR)

### Medium-term
- **storyBASE marketplace** for shared ontologies and templates
- **Cost pass-through billing** for model usage
- **GitHub Apps** with scoped credentials for fine-grained access

[^roadmap]: From Narrative-Driven Roadmap: "Move transactions from SPARQL to named graphs (TriG); add SHACL validation; implement evolved individuation pipeline (snapshot + message to transaction); file ingestion via GitHub; storyBASE marketplace; cost pass-through billing." Transaction: 2025-01-29T000000Z_sic-storybase-checkin.

---

## Use Cases

### 1. Organizational Memory
Capture strategy, style, and conviction in a versionable graph. Branch for scenarios, merge when aligned.

### 2. AI Persona Engineering
Replace "you are a helpful assistant" with a rich RDF profile encoding voice, values, and narrative anchors.

### 3. Content Generation
Generate presentations, READMEs, case studies, and social posts that stay on-narrative.

### 4. Strategic Alignment
Ensure every artifact—from PRDs to sales decks—flows from the same source of truth.

---

## Getting Started

### Prerequisites
- Docker & Docker Compose
- GitHub account
- Open Router API key (optional, for model access)

### Installation
```bash
git clone https://github.com/your-org/storybase.git
cd storybase
docker-compose up -d
```

### First Transaction
```bash
# Extract RDF from a sample input
curl -X POST http://localhost:5678/extract \
  -H "Content-Type: application/json" \
  -d '{"input": "Your narrative text here"}'

# Review the diff
curl http://localhost:5678/diff

# Commit the transaction
curl -X POST http://localhost:5678/commit
```

### Generate a Story
Create a `.story` file in the repo root:

```yaml
---
id: my-first-story
title: "My First Story"
model: anthropic/claude-sonnet-4.5
---

Summarize the current state of the storyBASE.
```

Trigger generation via GitHub Actions or the MCP server.

---

## Repository Structure

```
.
├── .storyBASE/               # Transaction log (SPARQL files)
├── ontology.rdf              # Narrative Architecture ontology
├── README.story              # This file's generation prompt
├── presenter.story           # Slide deck generation prompt
├── conj-talk-2025.story      # Conference talk generation prompt
├── docker-compose.yml        # Service definitions
└── n8n/                      # Workflow definitions
```

---

## Style & Voice

storyBASE encodes **style as data**. The ontology includes:

- **Diction** – Terminology control, naming conventions, verb choice
- **Tone & Voice** – Direct/personal, authoritative, active/passive
- **Cadence** – Sentence length variation, rule of three
- **Rhetorical Devices** – Simile, metaphor, analogy, anaphora
- **Metrics** – Readability, active-voice ratio, jargon density

Rubric assessments (0–5 scale) track:
- Register fit
- Phrasing (idiolect)
- Cadence
- Strategic alignment
- Audience tailoring
- Resonance
- Flow
- Novelty
- Accuracy

---

## Conviction Levels

Claims in the storyBASE carry **conviction** to govern change cost:

1. **Notion** – Exploratory, open edges
2. **Stake** – Proposed, moveable
3. **Boulder** – Settled, requires consensus to shift
4. **Foundation** – Underpinning, effectively permanent

This prevents narrative drift while allowing evolution.

---

## Contributing

storyBASE is **open for collaboration**. To contribute:

1. Fork the repository
2. Create a branch for your narrative changes
3. Add transactions via the `extract` → `diff` → `commit` flow
4. Submit a pull request with a clear description

All contributions must include provenance (transaction metadata) and align with the Narrative Architecture ontology.

---

## License

MIT License. See `LICENSE` file for details.

---

## Contact

- **Website**: [as-written.ai](https://as-written.ai)
- **GitHub**: [github.com/your-org/storybase](https://github.com/your-org/storybase)
- **Email**: hello@synthetic-identity.co

---

## Acknowledgments

Built with:
- **Apache Jena** for RDF processing
- **n8n** for workflow automation
- **MCP** for tool exposure
- **Open Router** for model access
- **iA Presenter** for slide generation

Inspired by:
- Clojure's immutable data structures
- Datomic's append-only architecture
- SKOS for knowledge organization
- PROV-O for provenance

---

*This README was generated from `README.story` using the storyBASE snapshot compiled on 2025-11-10T19:25:42.924Z.*