#### sic[theme][#theme-citation]
# 
## Immutable Selves
### A Functional Approach to Digital Identity
# 
#### Scarlet Dame
###### Founder, Sic | Former Chief Strategist, Vouch.io
	[#theme-citation]: Custom theme for Sic. The talk draws from narr:Tagline_1 "Immutable Selves: A Functional Approach to Digital Identity" and narr:Actor_ScarletDame, who exemplifies the append-only log model through personal identity history (Dylan Butman → Scarlet Spectacular → Scarlet Dame).

---
# Identity is mutable state
## And we're treating it like Backbone.js

The core analogy from narr:ComparativeAnalysis_1: today's identity systems query and mutate state like Backbone.js queried and mutated the DOM. We need the Om/React paradigm shift—identity as pure function of immutable history.[^backbone]

[^backbone]: narr:StyleObs_5 and narr:ComparativeAnalysis_1. Backbone.js (2012) represents the mutable-DOM era; Om (2013) introduced functional rendering from single source of truth. The speaker's 13-year Clojure career (narr:CaseContext_1) spans this evolution.

---
###### Personal context
# I am the append-only log

My identity history—Dylan → Scarlet Spectacular → Scarlet Dame—is immutable. Each name is a snapshot. The truth doesn't change; the rendering does.[^identity-history]

[^identity-history]: narr:Actor_ScarletDame and narr:Theme_TransitionAsStateChange. The speaker's transition exemplifies identity as "integral of snapshots over time, not mutable present state" (narr:Theme_ImmutableIdentity).

---
### From 2012 to today
# We learned this lesson in UI

In 2012: query the DOM, mutate the picture.  
In 2013: Om showed us state machines and pure functions.  
In 2025: we still treat identity like Backbone.[^ui-evolution]

[^ui-evolution]: narr:StyleObs_3 (anaphora: "You saw… Then you queried… Then you mutated") and narr:CaseContext_1. The speaker's career arc mirrors the paradigm shift from mutable to functional UI.

---
###### The problem
# 
### Passwords, keys, profiles—
# all mutable, siloed, vulnerable

No single source of truth. No provenance. No equality. Just mutation and hope.[^problem]

[^problem]: narr:ProblemContext_1 (berecognized.id) and narr:ProblemContext_2 (aswritten.ai). Fragmented, mutable identity state creates vulnerability; AI models as "black boxes" with no version control for persona.

---
## The Functional Identity Thesis

---
### What if identity was
# compiled from an append-only log?

Not a profile you edit. A history you render.[^thesis]

[^thesis]: narr:Mission_1 and narr:Primitive_1. The mission: "Move identity from mutable documents and profiles to compiled surfaces rendered from append-only logs and single sources of truth."

---
###### Three primitives
# 
### 1. Append-only transaction log
### 2. Single source of truth (SSoT)
### 3. Pure function renderer

These compose into everything else.[^primitives]

[^primitives]: narr:Primitive_1, narr:Primitive_2, narr:Primitive_3. The Product Ladder (narr:ProductLadder) shows how primitives → behaviors → flows → narratives.

---
### The flow
# SSoT → query → render → interact → event → transact → append → recompile

Identity as continuous compilation.[^flow]

[^flow]: narr:Flow_1. End-to-end loop from narr:ProductLadder. Each interaction produces transactions, not mutations (narr:Behavior_1).

---
## What You Get For Free

---
# Equality

Two identities are equal if their logs hash the same. Provenance is innate.[^equality]

[^equality]: narr:LeverageProfile_1: "Immutability enables equality, provenance, versioning, branching, generative testing, decentralization, and infinite read scale—for free."

---
# Provenance

Every assertion traces back to a transaction. You know who said what, when.[^provenance]

[^provenance]: narr:OutcomesProof_1: "Proof of provenance and authority innate; hash of last tx + SSoT state enables 'be recognized' property."

---
# Versioning & Branching

Git for identity. Fork, merge, rewind. Test alternate futures.[^versioning]

[^versioning]: narr:LeverageProfile_1 and narr:RequiredCapabilities_2 (RDF + git versioning). The storyBASE product itself demonstrates this (narr:Module/storybase-capabilities: "Git version control").

---
# Infinite Read Scale

Snapshots are cacheable, replayable, distributable. Reads are free.[^scale]

[^scale]: narr:LeverageProfile_1. Append-only architecture decouples reads from writes; snapshots can be served from CDN or local cache.

---
## The Trade-off

---
###### What we gave up
# Distributed writes

All transactions go through a single transactor. That's the bottleneck.[^tradeoff]

[^tradeoff]: narr:DesignTradeoff_1: "Bottleneck at single transactor; all logic in event clients; transact is just adding triples." Why worth it: consistency, provenance, auditability.

---
### But
# Logic lives in event clients
## Transact is just adding triples

The transactor is simple. The intelligence is at the edge.[^edge]

[^edge]: narr:DesignTradeoff_1 and urn:uuid:strategy-functional-immutable-identity ("Immutable facts at the edge, verifiable receipts"). Clients validate and construct transactions; the transactor appends.

---
## Two Systems, Same Pattern

---
### berecognized.id
# Immutable Identification

SSoT (Datomic) → datalog query → render to identification/privileges → event → transact → append → recompile.[^berecognized]

[^berecognized]: narr:Archetype_1, narr:ArchetypeTitle_1, narr:ApproachPattern_1. Proof-of-provenance identity system; canonical flow applied to access control.

---
### aswritten.ai
# Immutable AI Identity

SSoT (RDF + git) → SPARQL query → render to AI memory/identity → event → transact → append → recompile.[^aswritten]

[^aswritten]: narr:Archetype_2, narr:ArchetypeTitle_2, narr:ApproachPattern_2. Digital twin as compiled model; same pattern, different stack (RDF instead of Datomic).

---
###### The stakes
# 
### Without provenance
# AI identity is narrative manipulation

Persona prompts mutate rendered state. No version control. No audit trail. Embedded propaganda, deepfakes, synthetic fraud.[^ai-stakes]

[^ai-stakes]: narr:ProblemContext_2 and urn:uuid:opportunity-identity-vulnerability ("Centralized, mutable identity systems vulnerable to deepfakes, synthetic identities, and impersonation fraud").

---
## Proof: 13 Years in Production

---
### From Backbone to Om to Datomic
# The same principles apply

UI, identity, AI—immutability is the unlock.[^proof]

[^proof]: narr:CaseStudy_1, narr:CaseContext_1, narr:CaseIntervention_1. Speaker's career: Backbone.js (2012) → Om (2013) → production systems at scale. Applied Clojure principles (immutability, pure functions, SSoT) across domains.

---
### Results
# Provenance ✓  
# Equality ✓  
# Versioning ✓  
# Decentralization ✓  
# Infinite read scale ✓

Systems in production. Architectural guarantees delivered.[^results]

[^results]: narr:CaseResults_1. Quantified impact from narr:CaseStudy_1: all promised properties achieved in production systems (berecognized.id, aswritten.ai).

---
### Lesson
# Single transactor is an acceptable bottleneck

When provenance, auditability, and equality matter more than write throughput.[^lesson]

[^lesson]: narr:CaseLessons_1 and narr:ComparativeAnalyses_1. Insights from 13 years: "Same principles apply across UI, identity, and AI; immutability is the unlock; single transactor is acceptable bottleneck."

---
## Takeaways

---
### 1. Model identity as an evolving log
# not a static profile

Render from history. Don't mutate state.[^takeaway-1]

[^takeaway-1]: narr:Mission_1 and urn:uuid:style-obs-8 ("Technical reframing: identity as an evolving log of facts rather than a static profile").

---
### 2. Trust is provenance you can compute
# not credentials you hope are valid

Hash the log. Verify the chain.[^takeaway-2]

[^takeaway-2]: urn:uuid:style-obs-9 ("Trust as provenance that you can compute") and narr:OutcomesProof_1 (cryptographic proof of identity state).

---
### 3. The pattern generalizes
# UI → Identity → AI

Append-only + SSoT + pure render = deterministic, auditable, decentralized systems.[^takeaway-3]

[^takeaway-3]: narr:CaseLessons_1 and narr:Narrative_1 ("From mutable documents to compiled selves"). The Product Ladder (narr:ProductLadder) shows how primitives compose across domains.

---
## Questions?

Scarlet Dame  
scarlet@sic.ai  
github.com/pleasetrythisathome

The talk draws from the "Immutable Selves" sample (narr:Sample_1), extracted via narr:Tx_20251111T214920Z_immutable_selves. All claims are grounded in the storyBASE snapshot compiled from append-only transactions—practicing what we preach.[^meta]

[^meta]: This presentation is itself a proof: generated from narr:Sample_1 (5,847 characters, "Immutable Selves talk") via the storyBASE system described in the talk. The snapshot (compiled 2025-11-12T18:03:44.132Z) is the SSoT; this rendering is the pure function output.