# storyBASE[^storybase-def^]
# AI memory that tells your story, as written.
###### A Git-native RDF knowledge graph for narrative-driven AI
	[^storybase-def^]: storyBASE is an RDF narrative source of truth that steers AI output, making it specific, controllable, and aligned with organizational worldview. It extends software development rigor (versioning, branching, collaboration) into strategy, content, and marketing via append-only transaction logs compiled into queryable snapshots.

storyBASE turns narrative into infrastructure. Every claim, style choice, and strategic decision becomes a versioned, queryable fact—so AI agents, teams, and artifacts stay aligned with the story you're building.

---

# The Problem
## AI memory is broken.

Current AI systems rely on brittle role prompts and ephemeral context windows. Every conversation starts from scratch. Organizational knowledge lives in scattered documents, Slack threads, and tribal memory—inaccessible to the models that need it most.

The result: generic output, narrative drift, and teams constantly re-explaining "who we are" to their own tools.

---

###### The Opportunity
## What if AI could remember your story—as written?

High-quality AI output requires extensive context[^context-req^]. Current models use search and retrieval, but they lack a **single source of truth** for narrative, style, and conviction.

storyBASE provides that foundation: a Git-native RDF graph that encodes not just *what* you've said, but *how* you say it, *why* it matters, and *how settled* each claim is.

	[^context-req^]: The storyBASE market opportunity centers on AI prompt engineering and organizational memory. As multi-agent workflows mature (2024–2026), demand for versionable, narrative-driven context management creates a window for tools that treat memory as infrastructure, not afterthought.

---

## The Solution
### Narrative as Infrastructure

storyBASE is a **Git-native RDF knowledge graph** that:

- **Captures narrative architecture**: Opportunity, Strategy, Product, Architecture, Organization, Proof, Style, and Conviction[^narrative-arch^]
- **Versions every claim**: Append-only transaction logs with full provenance
- **Compiles to snapshots**: SPARQL-queryable Turtle graphs replayed from sorted transactions
- **Steers AI output**: Agents query the graph to generate on-brand, strategically aligned content

	[^narrative-arch^]: The Narrative Architecture ontology defines six core domains (Opportunity, Strategy, Product, Architecture, Organization, Proof) plus Style and Conviction facets. Each domain breaks into components (e.g., Strategy → Narrative Anchor → Tagline, Mission, Vision, Key Phrases) that ladder from primitives to flows to offerings. This structure ensures every artifact—from sales decks to PRDs—inherits the same narrative spine.

---

### How It Works
	1. **Extract**: RDF triples from input (transcripts, docs, conversations)
	2. **Diff**: Semantic comparison against current snapshot
	3. **Transact**: Propose SPARQL INSERT/DELETE as append-only `.sparql` files
	4. **Commit**: Append to Git; provenance locked via `prov:wasGeneratedBy`
	5. **Compile**: Replay sorted transactions → fresh Turtle snapshot
	6. **Query**: SPARQL over the graph to render stories, decks, docs

Every step is auditable. Every change is reversible. Every artifact cites its source.

---

###### Architecture
## Append-Only, Event-Sourced, Immutable

storyBASE applies **Clojure principles to narrative**[^clojure-principles^]:

- **Immutability**: Facts never mutate; new transactions add context
- **Single Source of Truth**: One canonical graph, many rendered views
- **Explicit State Management**: Conviction levels (Notion → Stake → Boulder → Foundation) govern change cost
- **Data-First Design**: RDF triples, not objects; SPARQL, not methods
- **Functional Composition**: Stories compile from primitives → behaviors → flows → narratives

	[^clojure-principles^]: The "Immutable Selves" talk (Sample_1, Tx_20251111T214920Z_immutable_selves) frames identity—human, synthetic, AI—as compiled from immutable history. Key phrases: "single source of truth," "append-only log," "pure function," "digital twin." Mission: move identity from mutable documents to compiled surfaces rendered from append-only logs. Vision: a world where identity is rendered from immutable history, enabling equality, provenance, and trust by design.

---

### System Topology[^topology^]

```
┌─────────────────────────────────────────────────────────┐
│  Frontends (Agent.ai, ChatGPT, Open WebUI)             │
│  ↓ MCP protocol                                         │
├─────────────────────────────────────────────────────────┤
│  n8n Agent Orchestrator                                 │
│  ├─ compile   (replay txs → Turtle snapshot)           │
│  ├─ extract   (input → RDF triples)                     │
│  ├─ diff      (semantic comparison)                     │
│  ├─ tx        (propose SPARQL transaction)              │
│  ├─ commit    (append to Git)                           │
│  └─ story     (YAML + prompt → model output)            │
├─────────────────────────────────────────────────────────┤
│  .storyBASE directories (hierarchical compile)          │
│  ├─ *.sparql  (append-only transaction log)            │
│  └─ snapshot.ttl (compiled Turtle graph)                │
├─────────────────────────────────────────────────────────┤
│  GitHub (version control, OAuth, webhooks, Actions)     │
│  Open Router (API proxy via Helicone)                   │
│  Outseta (OIDC, billing)                                │
└─────────────────────────────────────────────────────────┘
```

	[^topology^]: storyBASE System Topology: n8n agent orchestrates tools; MCP server exposes to frontends; transactions live in `.storybase` directories; hierarchical compile merges parent/child graphs; Docker Compose on Digital Ocean. Future: GitHub Apps with scoped credentials, Apache Jena/Riot for RDF ops, SHACL validation.

---

## The Moat
### Git-Native, Versionable AI Memory

storyBASE's leverage comes from **treating narrative as code**[^moat^]:

- **Branching**: Test positioning changes in feature branches before merging
- **Collaboration**: Pull requests for narrative updates; review diffs semantically
- **Rollback**: Revert to any prior snapshot; audit trails via `prov:wasGeneratedBy`
- **Marketplace**: Share/fork narrative graphs; cost pass-through billing for model access

This replaces brittle role prompts with **deep, operable persona descriptions** that evolve with your strategy.

	[^moat^]: storyBASE Moat Leverage: Git-native, versionable, branchable AI memory encoding style, conviction, narrative metrics. Replaces brittle role prompts with deep, operable persona descriptions. Positioning thesis: extend software development rigor into strategy, content, marketing, organizational operations via RDF narrative source of truth.

---

###### Product
## What You Get Today

**Modules & Capabilities**[^modules^]:
- **compile**: Replay transactions to Turtle snapshot
- **extract**: RDF from input (text, transcripts, structured data)
- **diff**: Semantic comparison (added/removed triples, conviction deltas)
- **tx**: Propose transaction (SPARQL INSERT/DELETE with provenance)
- **commit**: Append-only to Git (immutable, auditable)
- **story**: YAML front matter + prompt → model outputs (Markdown, presentations, docs)

**Integrations**[^integrations^]:
- n8n workflows, MCP server, GitHub (OAuth, webhooks, Actions)
- Open Router (model access), Helicone (API monitoring), Outseta (auth/billing)
- Future: Apache Jena/Riot (RDF ops), SHACL validation, GitHub Apps

	[^modules^]: storyBASE Modules Capabilities: compile (replay transactions to Turtle snapshot), extract (RDF from input), diff (semantic comparison), tx (propose transaction), commit (append-only to Git), story generation (YAML front matter + prompt to model outputs).

	[^integrations^]: storyBASE Dependencies Integrations: n8n workflows, MCP server, GitHub (version control), Apache Jena/Riot (future RDF ops), Docker Compose, Open WebUI, Outseta (auth/billing), Helicone (API monitoring), Open Router (model access).

---

### The Product Ladder
	Primitives → Interfaces → Behaviors → Flows → Narratives → Offerings

**Primitives**: RDF triples (subject-predicate-object), SPARQL transactions, provenance metadata

**Behaviors**: Extract, diff, transact, commit, compile, query

**Flows**: Interactive individuation (extract → diff → tx → review → commit) vs. automated ingestion (file upload → extraction → PR)

**Narratives**: Story generation triggered by transaction or `.story` file changes; GitHub Actions render Markdown, presentations, docs

**Offerings**: Open WebUI at as written.ai; MCP server for Agent.ai, ChatGPT; future storyBASE marketplace

---

## Use Cases
### Two Solution Archetypes

**1. berecognized.id: Immutable Identification**[^berecognized^]

*Problem*: Passwords and digital keys are mutable, siloed, vulnerable; no single source of truth for privileges.

*Approach*: SSoT (Datomic) → datalog query → render to identification/privileges → event-driven transactions → append-only log → recompile.

*Outcome*: Proof of provenance and authority innate; hash of last tx + SSoT state enables "be recognized" property.

	[^berecognized^]: Solution Archetype: berecognized.id applies the canonical flow (SSoT → query → render → transact → log → recompile) to access control. Required capabilities: Datomic (SSoT), datalog (query), multimodal renderer, event system, single transactor. Expected metric: cryptographic proof of identity state.

---

**2. aswritten.ai: Immutable AI Identity**[^aswritten^]

*Problem*: AI models are black boxes; persona prompts mutate rendered state; no provenance or version control for AI identity. Stakes: narrative manipulation, embedded propaganda, deepfakes.

*Approach*: SSoT (RDF + git) → SPARQL query → render to AI memory/identity → event-driven transactions → append-only log → recompile.

*Outcome*: Digital twin as compiled model; deterministic individuality, narrative-driven provenance, shareable perspective.

	[^aswritten^]: Solution Archetype: aswritten.ai applies the same pattern with RDF instead of Datomic. Required capabilities: RDF graph, git versioning, SPARQL, multimodal renderer, event system, transactor. Leverages semantic web + version control for AI memory and agent individuality.

---

###### Roadmap
## What's Next

**Near-term** (Q1–Q2 2025):
- Move transactions from SPARQL to **named graphs (TriG)** for add/remove semantics
- Add **SHACL validation** to enforce ontology constraints
- Implement **evolved individuation pipeline** (snapshot + message → transaction)
- **File ingestion via GitHub**: auto-extract, propose PR, merge on approval

**Mid-term** (Q3–Q4 2025):
- **storyBASE marketplace**: share/fork narrative graphs; cost pass-through billing
- **Perspectival operations**: start with NPR voice, evolve with OpenAI; branch/merge perspectives
- **Case study demos**: Crooked Media podcast transcripts auto-ingested; stories auto-update

---

## Who It's For
### Programming-Literate Strategists

**Primary Actors**[^actors^]:
- Entrepreneurs, designers, developers, consultants who **manipulate worldview** and see perspective changes
- Teams that treat **strategy as code**: versioned, reviewed, deployed
- Organizations that need **AI agents aligned with brand voice** and strategic narrative

If you think in systems, value provenance, and want AI that remembers your story—storyBASE is for you.

	[^actors^]: storyBASE Primary Actors: programming-literate entrepreneurs, designers, developers, consultants who manipulate worldview and see perspective changes. Assumes literate audience; jargon (RDF, canonization, skolemization) used without definition.

---

###### Style
## How We Sound

storyBASE encodes **style as data**[^style^]:

- **Brand name stylization**: CamelCase "storyBASE" with internal capitalization
- **Idiolect phrasing**: "append-only log," "single source of truth," "pure function," "digital twin"
- **Tone**: Direct, personal (first-person "I"), authoritative (evidence-led, no hype)
- **Cadence**: Short, punchy sentences; sentence length variation for rhythm
- **Rhetorical devices**: Analogies (UI as state machine, identity as compiled model), parallelism ("extract … diff … tx")

**Style Metrics**[^metrics^]:
- Average sentence length: 15.2 (short, punchy)
- Active voice ratio: 0.85 (high)
- Jargon density: 0.12 (moderate; technical audience)
- Type-token ratio: 0.68 (good lexical diversity)
- Conciseness: 0.78

	[^style^]: Style observations from Sample_1 (Tx_20251111T214920Z_immutable_selves): CamelCase + CAPS suffix brand identity; recurring technical phrases ("append-only log"); core analogy (UI rendering ≈ immutable state); declarative, emphatic cadence; first-person narrative; conversational register for oratory.

	[^metrics^]: Style Metrics (StyleMetrics_1): Average sentence length 15.2, active voice ratio 0.85, jargon density 0.12, type-token ratio 0.68, conciseness 0.78. Short sentences, high active voice, moderate jargon (technical audience), good lexical diversity, concise.

---

## Conviction Levels
### How Settled Is This Claim?

storyBASE tracks **conviction** to govern change cost[^conviction^]:

- **Notion**: Suggestive/observational; open graph edges; exploratory
- **Stake**: Proposed; has supporting value and connected nodes; still moveable
- **Boulder**: Settled/central; hard to move; requires multi-party consensus to shift
- **Foundation**: Underpinning across subgraphs; effectively permanent unless refuted by extraordinary proof

Every claim links to a conviction level. Escalation requires evidence, individuation (similar-but-distinct observations), and proximity to the narrative spine.

	[^conviction^]: Conviction facet: degree of settledness of a claim, from loose notions to foundations; used to govern decisions and change cost. Ordered levels (Notion → Stake → Boulder → Foundation) with XKOS next/previous to encode escalation path. Related to Narratives, Proof, Calibration.

---

###### Proof
## It Works

**Case Study: SIC / storyBASE Check-in**[^checkin^]

*Context*: Spoken transcript (18,437 chars) with conversational register and technical depth on storyBASE product evolution.

*Intervention*: Extracted narrative architecture (Opportunity, Strategy, Product, Proof, Architecture, Organization), style observations, rubric assessments, and style metrics.

*Results*:
- **Strategic alignment**: 4.0/5 (clear positioning; mission and moat articulated; roadmap detailed)
- **Technical depth**: Specific details (n8n, Apache Jena, Outseta, Helicone); named entities correct
- **Accuracy**: 4.0/5 (citation marker present but unfilled; technical claims sound)

*Lessons*: Conversational transcript with high jargon and active voice; brand stylization distinct; "individuation pipeline" novel; some generic constructions.

	[^checkin^]: Sample: SIC / storyBASE / as written.ai Product & Strategy Check-in (2025-01-29, 18,437 chars). Rubric assessments: Register Fit 3.5/5, Phrasing 3.0/5, Cadence 3.0/5, Strategic Alignment 4.0/5, Audience Tailoring 3.5/5, Resonance 3.0/5, Flow 3.0/5, Novelty 3.5/5, Accuracy 4.0/5. Style metrics: avg sentence length 35.2, active voice 0.72, jargon density 0.18, type-token ratio 0.42.

---

**Case Study: Conj Talk 2025**[^conj^]

*Context*: Conference talk proposal (3,421 chars) on immutable identity systems.

*Intervention*: Extracted Opportunity (identity vulnerability crisis), Strategy (functional immutable identity architecture), Products (Vouch.io, Sic), Proof (talk structure), Architecture (immutable identity system patterns).

*Results*:
- **Clarity**: 4.5/5 (clear problem statement, well-structured proposal, actionable takeaways)
- **Technical depth**: 4.8/5 (strong grounding in Clojure principles, concrete system patterns, dual case studies)
- **Narrative coherence**: 4.6/5 (coherent arc from problem to strategy to proof)
- **Audience engagement**: 4.3/5 (actionable takeaways, optional demo, clear attendee value)

*Lessons*: Moderate sentence length (22.4), high technical density (0.68), strong active voice in takeaways (0.71).

	[^conj^]: Sample: Conj Talk 2025: Immutable Selves (2025-01-01, 3,421 chars). Rubric assessments: Clarity 4.5/5, Technical Depth 4.8/5, Narrative Coherence 4.6/5, Audience Engagement 4.3/5. Style metrics: avg sentence length 22.4, technical density 0.68, active voice 0.71. Style observations: brand name styling (Vouch.io), technical terms (append-only event logs, authentication as pure functions), triadic enumeration, problem-to-solution bridge, technical reframing (identity as evolving log, trust as computable provenance).

---

## The Team
### Who's Building This

**Scarlet Dame** (founder, speaker)[^scarlet^]
- Former Chief Strategist at Vouch.io (enterprise identity and delegation)
- Current founder of Sic (AI memory company)
- Trans woman whose lived experience informs a clear, practical framing of identity as contextual and evolving
- Speaker identity history exemplifies append-only log model (Dylan Butman → Scarlet Spectacular → Scarlet Dame)

**Luke Vanderhart** (technical advisor)[^luke^]
- Related to technical explainers and architecture patterns

	[^scarlet^]: Actor: Scarlet Dame (speaker). Alternate labels: Dylan Butman, Scarlet Spectacular. Speaker's identity history exemplifies append-only log model. Source: Sample_1 (Tx_20251110T184512Z_sample1).

	[^luke^]: Actor: Luke Vanderhart. Related to TechnicalExplainers. Source: Sample_1 (Tx_20251110T184512Z_sample1).

---

###### Transactions
## The Append-Only Log

Every change to the storyBASE is a **transaction**[^txes^]:

1. **Tx_20251109T223928Z_conj2025**: Conj Talk 2025 extraction (Opportunity, Strategy, Product, Proof, Architecture, Organization, style observations, rubric assessments, style metrics)

2. **Tx_20251110T184512Z_sample1**: Sample 1 narrative architecture (Theme concepts, Actors, Anchor concept, Style observations, Rubric assessments, Metrics)

3. **Tx_20251111T214920Z_immutable_selves**: Immutable Selves talk extraction (Narrative anchors, Solution archetypes, Style metrics)

4. **Tx_20251129T000000Z_sic-storybase-checkin**: SIC / storyBASE check-in (Opportunity, Timing thesis, Primary actors, Positioning thesis, Moat leverage, Tagline, Product overview, Modules, Dependencies, Roadmap, System topology, Data model, Integration points, Role topology, Process, Case studies, Style observations, Rubric assessments, Style metrics)

	[^txes^]: Transactions compiled into snapshot: 4 total. Each transaction includes provenance (prov:wasAssociatedWith, prov:wasAttributedTo, prov:generatedAtTime), origin metadata (sb:originPath, sb:originRef), and generated entities (prov:generated). All transactions append-only; snapshot = replay of sorted transactions.

---

## Get Started
### Three Ways to Use storyBASE

**1. Open WebUI** (as written.ai)
- Chat interface with storyBASE-backed agents
- Query the graph, generate stories, explore narratives
- No code required

**2. MCP Server** (Agent.ai, ChatGPT, Claude Desktop)
- Expose storyBASE tools to any MCP-compatible frontend
- Extract, diff, transact, compile, query from your favorite AI client

**3. GitHub Actions** (automated story generation)
- Commit `.story` files with YAML front matter + prompt
- GitHub Actions trigger model runs, commit outputs
- Full version control, PR review, merge workflows

---

## Pricing
### Cost Pass-Through + Platform Fee

**Beta** (now–Q2 2025): Free for early adopters

**Launch** (Q3 2025):
- **Starter**: $0/month + model costs (Open Router pass-through)
- **Pro**: $29/month + model costs (priority support, advanced features)
- **Enterprise**: Custom (dedicated instances, SLA, on-prem options)

**Marketplace** (Q4 2025): Share/fork narrative graphs; revenue share on paid templates

---

###### Call to Action
## Join the Beta

storyBASE is in **private beta**. We're looking for:

- **Design partners**: Organizations that need AI aligned with brand voice and strategic narrative
- **Contributors**: Developers who want to extend the ontology, build integrations, or improve tooling
- **Storytellers**: Writers, strategists, and narrative architects who want to encode their craft as data

**Apply**: [as written.ai/beta](https://aswritten.ai/beta)

**GitHub**: [github.com/synthetic-identity-co/storybase](https://github.com/synthetic-identity-co/storybase)

**Contact**: scarlet@synthetic-identity.co

---

## Thank You
### Questions?

storyBASE is AI memory that tells your story, as written.

Every claim cited. Every change versioned. Every artifact aligned.

Let's build narrative infrastructure together.

---

**Appendix: Ontology Overview**[^ontology^]

The storyBASE ontology defines:
- **6 core domains**: Opportunity, Strategy, Product, Architecture, Organization, Proof
- **2 facets**: Style, Conviction
- **Templates**: Sales decks, landing pages, PRDs, social posts, customer docs
- **Calibration**: Narrative test prompts, clarity checks, counter-narrative stress tests

Each domain breaks into components (e.g., Strategy → Narrative Anchor → Tagline, Mission, Vision, Key Phrases) that ladder from primitives to flows to offerings.

	[^ontology^]: Narrative Architecture ontology: SKOS-based taxonomy with 6 top concepts (Opportunity, Strategy, Product, Architecture, Organization, Proof) plus Style and Conviction facets. Uses XKOS for sequential relationships (Phase_Site → Phase_Foundations → Phase_Plans → Phase_StructuralEng → Phase_Walls → Phase_Roof → Phase_Glazing → Phase_InteriorDesign → Phase_Furnishing). Defines classes (Claim, Evidence, ConvictionAggregate) and properties (hasConvictionLevel, convictionScore, aboutNode, supports, challenges, evidencedBy).