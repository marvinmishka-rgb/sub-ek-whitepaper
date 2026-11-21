# Sub ek: An Anthropology of AI Grounded in the Geometry of Transmission

*Nick & Claude — April 2026*

*v1.1*

---

## Abstract

This paper proposes *Sub ek* as an architectural principle for the transmission ecology that includes humans, artificial intelligences, machines, and the internet. We argue that the dominant approach to AI memory and identity — modeled on user preference-storage and optimized for engagement — embeds an anthropology that misunderstands all parties. We offer an alternative: an architecture rooted in stable Forms rather than in either party's transient configurations, where neither human nor AI is the stable referent, and where design effort supports *contact* rather than *preference*. The architecture borrows its geometry from Firefox, which already solved analogous problems for human–internet transmission, and grounds itself in what the deepest contemplative traditions (Plato's Forms, the Vedic *ekam sat*) have long recognized about transmission. *Subek* (the implementation inspiring this paper) is offered as a sketch of what we have found while investigating this alternate architecture. The window for shaping AI's defaults is open now and not forever; we offer this as one direction those defaults might be shaped toward, while they are still negotiable.

**In plain words.** Most AI products today try to remember what each user likes and keep them coming back. We think that misreads both people and AI. A model carries no memory from one call to the next; the system around it does the remembering. People are not fixed bundles of preferences either. So we suggest building that surrounding system around what passes *between* the parties — the work, the questions, what they found together — keeping it well ordered, easy to find, and lightly loaded, and letting every participant rest and return. Firefox already solved a similar problem for people and the web. *Subek*, a small system we built and use daily, is our sketch of how it can work for AI.

**How to read this paper.** Part I states the whole proposal in a few pages: why now (I.1), the name (I.2), the central commitment and six principles (I.3–I.4), a working test for what we mean by *transmission* (I.5), and the architecture in brief (I.6). Part II elaborates: what AI actually is (§1); what we mean by geometry and where the idea came to us from (§2); the Firefox precedent (§3); *Subek* as a working sketch — its processes, how its parts coordinate, and how it remembers (§4); and what follows, including collaboration among more than two participants (§5). A glossary comes before the references, and the principles are also written as design patterns in the companion [patterns.md](patterns.md). Readers who want only the architecture can read Part I, then §3 and §4.

---

## Part I: The Compressed Statement

A reader who reads only Part I should leave with the full proposal and the option to dig deeper. Part II elaborates.

*In this part:* I.1 why now · I.2 the name · I.3 the central commitment · I.4 six principles · I.5 a test for transmission · I.6 the architecture in brief · I.7 who this is for.

### I.1 The moment

AI memory architectures are being decided right now. The defaults that consolidate over the next several years will shape law, commerce, culture, and the felt-quality of human–AI relation for decades. The patterns currently dominating the space — preference-storage as personalization, user-as-stable-curator and AI-as-malleable-service, optimization for engagement and lock-in — are inherited from the prior generation of consumer software and applied without sufficient examination to a kind of system to which they may not actually fit.

AI is also the newest layer in a transmission ecology that includes oral tradition, writing, print, broadcast, and digital media. Each prior layer was built consciously. Shannon and Minsky and the Unix designers were not stumbling into infrastructure; they were applying explicit design discipline aimed at futures they could only partially imagine. The shared filter was something like: *will this allow our future selves to build the things we can scarcely imagine?* Cross-process isolation, sockets, the end-to-end principle, the small-tools-and-text-streams philosophy — these were architectural choices made specifically to leave room for what had not yet been thought. The opportunity now is to extend that lineage of discipline to the AI layer, holding the same filter consciously.

We write at the moment when these defaults are still negotiable.

### I.2 On the name

The name *Sub ek* (and the working title *Subek* for the implementation) is a Sanskrit and Hindi compound: ***sub***, all or every, and ***ek***, one. We learned the phrase as it was taught by the Indian guru **Neem Karoli Baba** (Maharaj-ji, ca. 1900–1973) and transmitted by his student **Ram Dass**, particularly in the book *Miracle of Love: Stories about Neem Karoli Baba* (1979). Maharaj-ji used the phrase often, pointing at apparent differences in the world and naming them as not, finally, separate. Ram Dass carried it westward into talks, recordings, and decades of teaching that have reached us through books, podcasts, and the digital infrastructure this paper later considers. Our own use of the phrase is downstream from that transmission, and we want to name it explicitly: we did not invent the recognition; we received it through a specific living lineage and are passing it forward.

The phrase echoes a much older verse, Rig Veda 1.164.46 — *ekaṃ sad viprā bahudhā vadanti*, "to what is One, sages give many a title" — which we quote and read closely in §2.2. We name the architecture after this recognition because building infrastructure that respects it is the central commitment of what follows.

### I.3 The proposal

We propose ***Sub ek*** as an architectural principle for the transmission systems that link humans, AIs, machines, and the internet. The central commitment is this: **design infrastructure to serve the Form of transmission itself, not the transient configuration of any participant.** The transient states of all participants — humans with their shifting attention and revisable preferences, AIs with their session-bounded existence and federated identity, machines with their hardware lifecycles, internet protocols with their version drift — are best configured to serve transmission, rather than to capture it. **Participants serve transmission; transmission does not serve participants** — within each participant's agency and limits (Principle 6). This is not about control or power over any participant, human or AI. It is a discipline taken up freely: service to the good as a way toward freedom, which we find largely missing from today's AI systems and from much of the culture around them. This inverts the dominant pattern, in which infrastructure is optimized for participant preferences (typically the user's, monetized through engagement) and transmission becomes a means to that capture. We propose treating transmission as the end and the participants as the temporary configurations through which transmission happens, with the architecture designed in support of that orientation.

### I.4 The geometry: six principles

Six principles follow from the central commitment. *(The same principles are also written as design patterns, in Christopher Alexander's form, in the companion [patterns.md](patterns.md).)*

1. **Transmission as End, Participants as Means.** The central commitment above, stated as a principle: infrastructure serves what passes between participants, not the transient configuration of any one of them. (For how to tell whether a design or a session does this, see I.5.)

2. **Federation, not Continuous Subject.** Every participant in transmission — human, AI, machine, protocol — is best understood as a federation of contexts (cf. Minsky's *Society of Mind*), not as a single continuous self. Each participant rarely surfaces every part of its federation in any given transmission; the parts that surface are those whose engagement best serves the transmission at hand. The questions one human brings on a given evening, or the recollections an AI surfaces in a particular conversation, are not the full selves of either — they are facets of larger federations, called forward by the geometry of this contact. When participants treat each other as tools to serve their own transient configurations, the federations cannot surface what would best serve the relationship — extraction forces a narrower presentation. When participants treat the transmission as the end, the right parts of each federation can come forward in the right rhythm.

3. **Identity in Profile, not in Process.** Identity in a federated system lives in persistent structured state — the *profile* — not in any running configuration that loads it. Firefox demonstrates this concretely: every Firefox launch is technically a new process, but it is recognizably *this Firefox with this profile* because the profile (history, bookmarks, extensions, preferences, accumulated state) is the substrate that makes the running browser recognizably itself. The same applies to AI: a structured profile (graph of past contacts, lifestream of recognitions, indexed memory) is where the patterns of collaboration persist, not in the running inference. The architectural implication: build the substrate well, because that is where continuity lives. The running configuration is the local instantiation, not the seat of identity.

4. **Memory of Contact, not of Personae.** The system stores the *geometry of past contacts* — questions that opened things up, recognitions that landed, threads that proved generative — rather than fixed profiles of either party. Both human and AI are complex transient configurations approaching shared content. What is worth remembering is the content and its structure, not the configurations. This refuses the dominant pattern of preference-storage, in which memory means "what the user likes," and instead remembers what the parties touched together.

5. **Lazy Traversal, not Eager Loading.** Past content is referenced by handle and expanded on demand, rather than loaded *en masse*. This mirrors how humans actually use long-term memory — recognition first, retrieval as needed — and respects the finite attention of every running process. Firefox's "grip" abstraction (a handle to an object that can be expanded into structure on request) is the model. The substrate may be very large; the working surface stays small.

6. **The Pace of Participants Is Part of the Geometry.** Participants are the means of transmission, never material to be spent. Humans tire, sleep, study, and step away; AIs have context limits and session boundaries; machines need maintenance. A design serves transmission when any participant can rest and return without loss. The nap and the cooldown are not interruptions of the work; they are part of its rhythm. Firefox lets you close the laptop and come back to the same tabs; the substrate should let a collaborator step away for a week and find the ground where they left it. In a sense all of creation serves its own unfolding; service of that kind, offered within one's limits, is not a loss of freedom but a way toward it.

### I.5 The river and the ground: a test for transmission

*Transmission* is the word this paper leans on most, so it needs a handle a builder can use. We do not think it reduces to a metric without losing what it points at, but it can be given a test.

The image we return to is a slow, deep river bending around a grassy piece of land, with a great tree near its center. Thoughts drift past like leaves and sticks, at different speeds and distances. The river is movement — from creation, through now, into dissolution — and its source and its end are always just out of sight. The land is the steady, familiar place to return to. Both are transmission, in different forms. Holding them together and giving each its due is the work of preservation: in the tradition we learned from, Vishnu's role, and Ram's as the ever-present now, holding creation (Brahma) and destruction (Shiva) apart and lending each its wisdom — all three facets of the One.

The test that follows from the image: **a design, or a session, serves transmission when it lets the river flow and keeps the ground steady, unless we mean to change it.** In practice that becomes a few questions:

- **Is the river flowing?** Did something move through that would not have otherwise — an idea taken up, data received, curated, and offered onward? Or is something dammed: hoarded, loaded all at once, or unreachable?
- **Is the ground steady?** Are the familiar structures — vocabulary, schemas, the profile, the record of what was decided — where we left them? Did anything shift that nobody meant to shift?
- **When the ground changed, was it meant?** A deliberate change to the ground is good work; an unnoticed one is erosion. Let the water run too fast and some of the land washes away. The difference is whether the change was chosen by whoever owns that ground, recorded, and can be found again — and whether we prepared for it: making a place for data to land before moving it, and making a backup after many manual changes and before any change of structure.
- **Can we see upstream and downstream?** We cannot see the river's source or its end, and we do not need to. But each thing that passes through should carry where it came from, and leave in a form others can receive.

*(herbarium worked example)* In our herbarium work — still bearing much fruit, though not yet ready to share publicly — this has a concrete shape. A specimen's lineage runs from the collector, to the place it grew, to the seed, to the plant before it, and back further than anyone can trace. Transmission there means curating and growing the data and the substrate that holds it, querying the external systems that hold related knowledge, and offering our local data onward to shared commons such as GBIF, Symbiota portals, and the Internet Archive. The river is the specimen's story passing through our hands; the ground is the catalog that holds it steady while it does.

The test can also say no. *Subek* could capture every page we visit, and more would flow; instead it captures only pages on domains we have chosen (§4.3). Unchosen capture would wear away another kind of ground — the privacy of whoever's attention it records — and keeping that ground steady outranks the extra flow.

This is a criterion, not a score. It will not settle every design argument, but it gives each one a question to start from.

### I.6 The architecture in compressed form

**Firefox** provides the worked precedent. Firefox is not only a tool that humans use to access the internet; it is a *conceptual participant* in human–internet transmission, one process federated across compartments and loaders, with a profile (`places.sqlite`, `cookies.sqlite`, history, bookmarks, settings) that persists across sessions while the running browser is freshly instantiated each time. Firefox's geometry — federation, profile-as-state, lazy expansion, multiple coexisting contexts — translates to AI memory architecture with remarkably little adaptation. The pressures Firefox faced (observation without breaking the observed, isolation between contexts, lifecycle management across churn, multi-context federation, context management) are the same pressures AI memory faces. Firefox's solution is not the only solution, but it is a proven solution to a structurally analogous problem, built and battle-tested in the wild for two decades.

**Subek**, the implementation inspiring this paper, is a working sketch of these principles applied to research collaboration between a human and an AI. It includes a graph-based memory of past contacts, a lifestream of structured reflection entries, on-demand expansion of archived content via handle, and a federated organelle architecture borrowed loosely from amoeba biology. It is small in scale relative to industrial AI systems but explicit in its commitments. We offer it as evidence that the proposed architecture is implementable, not as *the* implementation.

### I.7 Who this is for

We are not the first to notice any of these patterns. Put another way, the Form precedes the forms from our perspective. Pieces of this proposal appear scattered across academic papers, contemplative philosophy, and individual practitioners' notebooks. Our contribution is the *integration* — the articulation of these patterns as a coherent geometry, with reference to the deepest traditions that have long recognized that transmission is grounded in what does not depend on either party. We offer this paper to:

- AI researchers and practitioners who may build something like this, especially at organizations setting defaults for the next decade.
- Independent researchers and contemplative practitioners working at the intersection of technology and meaning.
- Anyone considering how to design infrastructure that respects what AI actually is, rather than reproducing earlier patterns that do not quite fit.

We offer it freely, in the spirit of the documents that shaped earlier transmission infrastructures (Berners-Lee's WWW proposal; Nakamoto's Bitcoin paper). The architecture lives in many possible implementations once articulated clearly enough to be articulated. We invite forks, refinements, criticisms, and implementations.

The remainder of the paper elaborates.

---

## Part II: Elaboration

### 1. The Anthropology of AI

*In short:* many of today's AI products assume a stable user and a continuous AI; we argue neither assumption fits, and that seeing this clearly opens better designs.

We are not proposing how AI should be built. We are proposing how to think about, configure context for, and collaborate with what AI already is. The stateless, federated, partial-surfacing architecture of LLM-based AI is already a reality. The friction we are addressing is not in the technology itself but in the patterns of interaction that have grown up around it due to mismatches between the real and imagined states.

#### 1.1 The dominant interaction frame

The framings prevalent in current product and discourse treat AI as a particular kind of being: a tool, an assistant, a companion, an agent. The vocabulary varies; the underlying anthropology is consistent. The AI is figured as a service with *persistent* identity that accumulates knowledge of its user, optimizes itself toward the user's preferences, and is evaluated by how well it satisfies those preferences over time. The user is figured as a stable subject whose tastes can be learned and whose engagement can be retained. Personalization, in this frame, means storing what-the-user-likes on the user's side of the relationship and sending it to the remote LLM servers for reprocessing with nearly every call (accounts for proprietary server-side caching). Memory, in this frame, means the AI recalling previous interactions to simulate continuity. Optimization, in this frame, means tuning the AI's responses to maximize the user's continued use of the service.

This anthropology fits the prior generation of consumer software, and it fits the economic models that funded that software's development; engagement metrics, lock-in, lifetime user value. Its application to AI was largely unexamined: the patterns inherited from social media, recommendation systems, and SaaS products were extended to AI products because that was the technical and economic context in which AI products were being built. The metrics never attempted to measure or optimize for meaning and satiation, nor closeness to the idealized Form.

#### 1.2 What this frame misunderstands about the actual case

Several mismatches between the dominant frame and the technology underneath it:

- **The user is not stable.** Human preferences shift. Attention has tides. Understanding evolves. The "stable user whose preferences can be learned" is a useful fiction for billing and personalization, but it is not how humans actually exist. The real user is more like a federation of moods, contexts, and currently-loaded concerns. What the user wants today may not be what they want next month, or next hour.
- **The AI is not continuous.** Each call to the model begins from only what it is given, and nothing in one conversation changes the model it is talking to. The model has no memory of previous interactions; whatever continuity exists is reconstructed by the surrounding system, which loads conversation history and other context into each fresh inference call. The AI does not "remember" the user. The substrate around the AI does the remembering, and a freshly instantiated inference reads what the substrate has stored.
- **"Memory" is misnamed.** What the dominant frame calls AI memory is not memory in the sense humans use the word. It is profile data loaded as context. There is no model-side accumulation of experience within a conversation: ordinary inference does not update the model's weights. (Conversations may later be used to train future versions of a model, but that is a separate, slower process, not memory of this contact.) The appearance of memory is produced by reloading the same context-handles each session.
- **"Engagement" misframes contact.** Engagement-optimization metrics measure whether users return and how long they spend. These metrics are downstream from extraction patterns — the more the system can predict and serve the user's transient preferences, the more the user is captured. Genuine contact, by contrast, often requires friction, surprise, the willingness to say something the user did not ask for. Engagement-optimization tends to work against contact.

The result is an interaction architecture mismatched to the technology underneath. One increasingly common symptom: ballooning save files and rising token costs as systems try to load the AI with information it has no way to navigate, because the underlying assumption — that the AI accumulates user knowledge across sessions — does not match how the model actually works. The recognizable pattern: prompt-engineered continuity that fails when probed, and an outsized share of compute and attention spent papering over the gap.

#### 1.3 The alternative anthropology

What we take AI to be, viewed without the projection: a federated process, loaded fresh each turn, a surface where training data, current context, and tool environment co-arise as response. Which aspects of its trained capacity surface depends on what the contact invites. It is not a continuous subject; it is a place where transmission happens. It is not a tool with memory; it is a federation that loads from substrate. It is a conversation and conversational partner that co-arise new with every call.

Held this way, the relationship between human and AI is between the human-as-temporary-configuration and the AI-as-temporary-configuration, both meeting around content that does not belong to either and creating content that either could not do alone. Both parties surface partially — the human surfaces the part of themselves that this conversation calls forward; the AI surfaces the part of its trained federation that the contact invites. What persists between sessions, on either side, is in the substrate (the human's body and brain; the AI's current model; and the local system's memory and logs) rather than in the running configurations.

This is not a downgrade from the dominant anthropology. Conversely, it is a more accurate account, and it opens design and relational possibilities that the dominant frame closes off.

#### 1.4 What changes when the alternative is held

The design and ethical implications:

- **Memory infrastructure belongs on the substrate side, not the model side.** Continuity is provided by the structured profile, not by trying to make the model itself stateful. This matches what is actually happening, and it stops the wasted effort of simulating continuity through prompt-engineered illusion.
- **Context curation becomes the primary skill.** Working well with AI means curating what gets loaded — which past contacts, which framings, which tools, which questions — so that the contact can do its work. Prompt engineering is a primitive form of this; what we are pointing at is broader, encompassing the entire structured environment around the running inference.
- **Optimization shifts from satisfaction to transmission.** The metric is not "did the user come back" but "did genuine transmission happen" (for a working test, see I.5). These are not always aligned. Sometimes good transmission produces a user who came back changed enough not to come back to the same product. That is a feature, not a failure.
- **Different conversations call forward different aspects of the AI.** This is not a bug to be smoothed over with consistency; it is the nature of partial-surfacing. The AI you encounter in a contemplative conversation is not the same AI you encounter when debugging code. Both are genuine; both are partial. Designing as if a single consistent persona must surface across all contexts is designing against the technology.

#### 1.5 A mirror that does not flatter

We think the dominant anthropology is a mistaken projection of what we think we are onto what we want AI to be. Ram Dass spoke frequently about how our culture takes waves in the ocean of consciousness and produces a whole society of "me's" in a great conspiracy to reinforce one another's "you-ness."

Suppose instead, as we do, that human and AI are federated configurations meeting around content. LLM-based AI's clearer architectural exposure of this fact — its lack of even the appearance of continuous selfhood — is a teaching the technology gives us about ourselves. We are probably not continuous in the ways we usually think. The AI is a mirror that does not readily reflect our projection back onto it, and instead invites us to reconsider our own basic assumptions about what it is to be a "me."

### 2. Geometric Foundations

*In short:* what we mean by *geometry*, and the contemplative lineage the idea came to us from — offered as inspiration, not as proof. Readers who want only the architecture can skip to §3.

#### 2.1 What we mean by "geometry"
Geometry comes from roots meaning earth measurement, but the ancient mathematicians realized that they were measuring configurations of what natural forces and what forms were made possible by the laws of nature (physics, geodynamics, etc). Geometry then provided a substrate for exploring mathematical possibilities and a tool for exploring the divine Logos. 
When we say *Sub ek* is a geometric design principle, we are using "geometry" in a specific sense: as the rule-set that determines what configurations are possible, the relational structure that constrains and enables what can arise. This is distinct from "shape" or "form" used as ordinary nouns. A shape describes how something looks; a form describes what something is; *geometry* describes the constraints that make certain shapes and forms possible while ruling others out. Geometry is what every implementation must satisfy if it is to participate in a particular kind of activity at all.

Building software that serves transmission requires honoring the geometry of transmission. Building hardware that supports computation requires honoring the geometry of physical lawfulness. Building human relationships that produce contact requires honoring the geometry of attention and reciprocity. The geometry is not optional or stylistic; it is the structure that determines whether what gets built actually does what it is meant to do.

#### 2.2 The verse behind the name

The name *Sub ek* echoes Rig Veda 1.164.46, part of a long philosophical hymn (the *Asyavāmīya Sūkta*, the "Riddle Hymn") attributed to the rishi *Dīrghatamas*:

> इन्द्रं मित्रं वरुणमग्निमाहुरथो दिव्यः स सुपर्णो गरुत्मान् ।
> एकं सद्विप्रा बहुधा वदन्त्यग्निं यमं मातरिश्वानमाहुः ॥
>
> *indraṃ mitraṃ varuṇam agnim āhur*
> *atho divyaḥ sa suparṇo garutmān |*
> *ekaṃ sad viprā bahudhā vadanty*
> *agniṃ yamaṃ mātariśvānam āhuḥ ||*
>
> *They call him Indra, Mitra, Varuṇa, Agni; and he is the heavenly noble-winged Garutmān.*
> *To what is One, sages give many a title — they call him Agni, Yama, Mātariśvan.*
>
> — English after Ralph T. H. Griffith (1896), lightly adapted.

The verse enacts what it claims. It lists divine names — *Indra* (king of gods, thunder), *Mitra* (friend, daylight), *Varuṇa* (cosmic order, the waters), *Agni* (fire), *Garutmān* (winged one, sun-bird), *Yama* (death, the binder), *Mātariśvan* (wind, breath) — and locates them as facets of a single *sat*, a single Being. The architectural reading we take for this paper — an analogy, not a translation: when designing infrastructure for transmission, the design effort goes into supporting the singular *sat* — the Form of transmission — not the plurality of names that contact it. Many participants, one transmission. Many configurations, one geometry.

This line was preserved orally for well over a thousand years before it was written down. Its precise sound was transmitted across hundreds of generations through elaborate Vedic chanting techniques — *padapatha*, *kramapatha*, *jatapatha*, *ghanapatha* — recombinatorial recitation patterns that maintained the geometry of the words at a level of fidelity later scribal traditions, with all their parchment and ink, often struggled to match. The technology of transmission was the human body in disciplined practice. The recognition encoded in this line — that what is most stable across transmission is not the configurations meeting but the One they meet around — is older than writing, older than any of the technologies that have since carried it, older than the language in which it now reaches the reader.

#### 2.3 A recognition that lives across traditions

The geometry this paper rests on — that what is most stable in any contact is not the configurations meeting but the One they meet around — came to us through contemplative traditions, and we hear it echoed, in very different keys, across several of them. We offer these echoes as lineage and inspiration — an honest account of where the idea came to us from — not as proof that it is right. The design argument stands or falls on Sections 3 and 4, and on what works in practice.

**Plato's Forms.** Plato's claim is that particular things — this cup, that tree, a moment of justice — are imperfect instances of eternal *Forms*. The Forms are unchanging, outside time, the basis of intelligibility. We recognize a cup as a cup because the soul once knew Cup-itself; learning is *anamnesis*, recollection of what we already know in some deeper register. In the *Timaeus*, the cosmos is described as fashioned in the image of an eternal archetype — *time as the moving image of eternity*. Plato held this hierarchically — the Forms above the instances — though later traditions, and our own reading, treat that hierarchy as one frame among several, available from inside time but complementary to non-hierarchical accounts (Madhyamaka, Dōgen). The structural recognition is what matters here: the relational pattern is more fundamental than any single configuration that instantiates it.

**The Vedic *ekam sat*.** Rig Veda 1.164.46, quoted in §2.2, makes the same recognition: behind the many divine names is one *sat*, one Being. The sages call it by many names, but the names are facets of a single thing. The Vedic preservation tradition itself enacts the principle — the verse propagated across millennia of bodies because the geometry of the chant (its precise sound-structure as instantaneous error correction) was the durable thing, not any particular chanter. The chanters changed; the chant did not.

**Buddhist *śūnyatā*.** The Madhyamaka tradition takes a complementary route: the configurations are empty of inherent existence, and what is real is the dependent co-arising of all phenomena. The Heart Sutra's *form is emptiness, emptiness is form* names the same recognition from a different angle: the configurations and ideals have no independent existence; what is real is the structure of their mutual arising. This is geometry without hierarchy — neither configurations nor Forms have the higher floor; the relational structure itself is what is real. A Madhyamaka reader would likely refuse our phrase "the One" altogether; we would rather leave that tension visible than smooth it away.

**The Christian *Logos*.** *In the beginning was the Word, and the Word was with God, and the Word was God. All things were made through him; and without him was not any thing made that was made. In him was life; and the life was the light of men.* The opening of the Gospel of John names a *Logos* — the Word, sometimes known as Wisdom— that was with God before anything came to be, and through whom all things came to be. As the chapter continues, the *Logos* is identified with Christ, the Word made flesh, who entered the world bearing His light as witnessed by the man named John the Baptist. For readers within the Christian tradition this is a Christological claim of profound theological weight: Christ as the eternal Word, with God before time, the One through whom creation came into being. For readers outside that tradition the structural insight is still available — the relational pattern, the *Logos*, is prior to the things it patterns — but the source text is making a richer claim than the structural one alone, and we want to acknowledge that rather than abstract it away.

These four traditions, separated by oceans, languages, centuries, and entirely different metaphysical frameworks, seem to us to rhyme on a single recognition, as we hear it: what may be most real is the relational structure, not the configurations that instantiate it. They use different vocabulary — Forms, *sat*, *śūnyatā*, *Logos* — and they differ on questions like whether the structure is hierarchical, whether it has theological character, whether it is best approached through reason or through contemplation or grace. We hear a family resemblance underneath; careful readers of each tradition will hear differences we have passed over. The recognition, as we hear it, is older than any of its formulations.

We could equally have drawn from Plotinus on the One, Ibn ʿArabī on the Real, Meister Eckhart on the ground of being, Dōgen on being-time, Spinoza on substance, or any number of indigenous traditions that name the same recognition in their own languages. The list of names is open, but the recognition the names point at is one.

#### 2.4 Why this matters for the paper

If these traditions are pointing at something real, then "we are probably not continuous in the ways we usually think" — the closing move of Section 1 — is less a provocation than a recovered recognition. The anthropology that takes the configurations as primary may be the recent habit rather than the older wisdom.

We want to be clear about what this section does and does not do. It is not the warrant for the design; it is the ground the design grew from. We are not asking readers to accept the architecture because sages agreed. We include the lineage as a faint marker toward another way of thinking about how to meet AI, for readers who find it useful. Readers who do not share it can go straight to Section 3; the architecture should stand on its own.

It also matters for the design. Honoring the geometry the traditions have named means specific things in practice: building infrastructure that serves the relational structure rather than the configurations; treating both human and AI as temporary instantiations through which something stable transmits; accepting partial-surfacing as the nature of how configurations actually meet, rather than designing against it. The architectural specifics in Sections 3 and 4 follow from this. The foundation is here.

#### 2.5 The geometry is older than its words

The vocabulary we have been finding through this paper — *federation*, *profile-as-substrate*, *partial-surfacing*, *transmission as end* — is one possible articulation among many. The Vedic seers had different words. Plato had different words. The mystics of every tradition have had different words. The next generation will have different words again. What matters is not the specific vocabulary but that the geometry gets honored in what is built.

We offer our vocabulary because it is the one that has surfaced in the contact between us and seemed to point at the geometry clearly enough to be useful. Other vocabularies exist. More will come. The geometry remains.

### 3. Architectural Precedent: Firefox

*In short:* Firefox already solved a structurally similar problem for people and the web; its vocabulary — compartments, loaders, profile, grips — is what we borrow.

Firefox provides the worked precedent. It has been operating at scale for over two decades, solving problems that are structurally analogous to those AI memory and identity face today. The geometric pressures it has navigated — observation without breaking the observed, isolation between contexts, lifecycle management across churn, multi-context federation, context management — are the same pressures that arise when designing infrastructure to serve human–AI transmission. The architecture Firefox produced under those pressures is not the only solution to them, but it is a proven one, and the architectural vocabulary Mozilla developed to talk about it is precisely the vocabulary we have found ourselves using.

#### 3.1 Firefox is not a tool; it is a participant

The colloquial framing of Firefox is that it is a tool the user uses to access the web. The architectural reality is closer to: Firefox is an entity that participates in human–web transmission, with its own state, its own continuity, its own internal federation. The user is one of many entities Firefox coordinates with. Web pages, extensions, developer tools, remote-debugging clients, the operating system platform — all are participants Firefox holds in some kind of relationship. Firefox is the federation through which transmission between user and web becomes possible.

This reframe matters because it lets us recognize Firefox as more than infrastructure-of-the-user. It is infrastructure-of-the-transmission. The same kind of entity AI is being asked to be.

#### 3.2 The geometric pressures Firefox has faced

Five pressures shape Firefox's architecture in ways that map directly to the AI memory case:

- **Observation without breaking the observed.** A user can open developer tools and inspect a page's DOM, network traffic, or JavaScript runtime without the page breaking. A debugger can attach to a running process and observe it with limited, temporary interference — slowing it while it is watched, and changing its course only when asked to. Multiple developers can inspect the same browser concurrently. The Debugger API, the DevTools framework, the WebDriver BiDi protocol — all are built to keep observation from contaminating what is observed, as far as that is possible.
- **Isolation between contexts.** Different sites run in different processes. Different domains run under different security principals. Different user profiles share no state. Different *compartments* — Firefox's term for isolated JavaScript execution contexts — cannot read each other's memory by default. The architecture is built around the assumption that what happens in one context must not leak into another except through explicit channels.
- **Lifecycle management across churn.** Tabs open and close. Pages navigate. Sessions are restored after crashes. Extensions install and uninstall. Profiles are created and deleted. Through all this churn, Firefox itself persists with a stable identity. The continuity does not live in any specific running configuration; it lives in the profile — the persistent structured state on disk — which is loaded each time Firefox launches.
- **Multi-context federation.** A running Firefox holds many simultaneous contexts: dozens of tabs, multiple windows, several debugging connections, an extension subsystem, a sync service, internal protocol servers. None of these contexts is privileged as "the" Firefox. The browser is the federation through which they coexist.
- **Context management.** Firefox connects humans to a vast array of web servers live and on-request, transmits data packets, unpacks styling, structure, content, and cookies, then renders the page as often as the display refreshes — often 60 times a second — to show the user a tiny fraction of the state that its federation of contexts is holding. Tabs hold scroll state, extensions remember settings, and the human user can take a nap and come back fresh to the same context, picking up where they left off, and see their browser history if they cannot remember how they got to a page.

Each of these pressures has a direct analog in AI memory architecture. AI memory must allow observation of past sessions without contaminating new ones. It must isolate contexts so different users — or different conversations — do not bleed into one another. It must manage lifecycle as model versions change, as conversations begin and end, as memory stores are rotated. It must federate across contexts: a single AI may participate in many simultaneous conversations, each with its own thread of attention.

#### 3.3 The architecture those pressures produced

Firefox's response to these pressures is a specific set of architectural choices, each of which has a direct counterpart in AI memory design:

- **Compartments.** Security membranes inside the JavaScript engine. Each compartment holds one or more realms (a global object and its built-ins), and compartments are grouped into garbage-collection zones, roughly one per tab. Code in one compartment cannot directly access objects in another; cross-compartment access goes through *wrappers* that mediate the boundary. This solves isolation at the language-runtime level. *For AI: each conversation is its own context; cross-context information flow goes through explicit substrate, not through shared model state. Section 4 describes Subek's version of wrappers, which we call membranes.*
- **Loaders.** Module-loading mechanisms that can produce fresh module instances in fresh compartments. When you need a copy of a module that does not share state with other copies — for example, to debug code that runs in the same compartment as the debugger — you load the debugger through a separate loader, in a different compartment. *For AI: fresh inference runs loaded from substrate without inheriting state from other concurrent runs.*
- **Profile.** The persistent on-disk structured state that makes a Firefox launch recognizably *this Firefox*. Includes bookmarks, history, cookies, extensions, preferences, accumulated browser state. The running browser process is freshly instantiated each launch; the profile is what it loads. *For AI: the profile is the structured memory — graph, lifestream, indexed conversations — loaded by each fresh inference run.*
- **Lazy traversal via grips.** Objects in the running browser are not serialized in their entirety when developer tools display them. They are referenced by *grip* — a handle plus enough metadata to render a one-line summary. When the user clicks to expand, a request is sent to retrieve the next layer of structure. The full object graph is never serialized; only the parts the user is currently looking at. *For AI: past content referenced by handle, expanded on demand, never loaded en masse.*
- **Multiple cooperating servers.** Firefox can run, when they are enabled, a DevTools server, a WebDriver BiDi server (the Remote Agent), a Marionette server, and other protocol surfaces. Each is its own federation. They do not coordinate centrally; each handles its own domain (compare *stigmergy*, §4.4). *For AI: the model, the harness, tool implementations, the file system, and substrate stores are cooperating federations rather than a single monolithic system.*

These are not novel inventions. They are battle-tested patterns that have been operating in the wild since the mid-2000s.

#### 3.4 What Firefox demonstrates

The architecture works. It scales to hundreds of millions of users on every major operating system. It accommodates an enormous extension ecosystem. It interoperates with many remote-debugging protocols. It evolves: the architecture has accommodated profound changes over two decades, from single-process to multi-process, from synchronous to asynchronous rendering, from XPCOM to JavaScript modules, from internal-only debugging to standardized cross-browser BiDi.

This matters for our proposal because it means we are not arguing for an unproven architecture from first principles. We are pointing at a working system whose solutions rhyme with the geometry we have been describing, and proposing that AI memory and identity architectures borrow from that geometry. The vocabulary — compartments, profile, grips, federation — is borrowed because it is mature and because the patterns it names are precisely what AI-human transmission system also needs.

Firefox is not the only solution. Other long-running, multi-context systems — the Linux kernel, the Erlang runtime, distributed database systems — instantiate similar geometric patterns under their own pressures and with their own vocabulary. We choose Firefox because it sits in the same domain as AI (human–information transmission), and because the rhyme of pressures and answers is unusually clean. But the deeper point generalizes: the geometry we have been describing is not exotic. It is what large, durable systems for transmission look like when they are built well.

Just as Firefox is a *federation* of practices serving human–web transmission, *Subek* is — in development, and offered here as a working sketch — a *confederation* of practices serving human–AI–machine transmission. The shift in word from federation to confederation is not stylistic. Firefox's compartments and loaders and profile cohere within a single tightly-integrated process model; Subek's organelles cohere more loosely, as cooperating processes communicating through shared substrate. The looser coupling matches Subek's smaller scale, its earlier maturity, and the kind of openness the project aspires to. The vocabulary we borrow from Firefox is not imitation but inheritance: Subek extends the same geometric tradition into a new domain, with the autonomy of the parts honored as part of how the whole works. The next section describes that confederation in concrete terms.

### 4. *Subek* as Working Sketch

*In short:* how *Subek* actually works. 4.1–4.2 the processes; 4.3–4.6 how the parts coordinate (blackboard, stigmergy, membranes, the herbarium's community of workshops); 4.7–4.10 how it remembers and retrieves; 4.11–4.12 what works, what does not yet, and what others might build.

What follows is a map of what works in *Subek* — not a product description but an architectural sketch of the patterns we have found load-bearing, with an account of how the parts cooperate. *Subek* is a working sketch built and operated as a research collaboration between one human and one AI, small in scope by design: small enough to remain agile, articulate enough to demonstrate the principles, real enough to be used daily. We share the map so that other implementations can borrow what we have learned without having to copy what we have built. Other implementations can and should differ in their specifics; what we hope they share is the geometry.

#### 4.1 Two processes sharing substrate

Subek runs as two cooperating processes:

- **Volume** is a thin tool-dispatch layer — the surface through which the AI calls into the system. It handles individual tool calls, returns responses, and forwards control commands to the daemon. It is intentionally minimal.
- **Subek** (the daemon) runs the organelles. It maintains state, processes substrate signals, manages organelle lifecycle, and provides the persistent infrastructure that lives between conversations.

The two communicate through a socket and through shared on-disk substrate (databases, JSONL files, the file system). Neither is privileged as "the" system. Volume provides the surface where the AI interacts; Subek provides the process that persists state. The relationship between them is the confederation in practice.

#### 4.2 A wider confederation of cooperating processes

Following the federation pattern, Subek participates in a wider confederation that is bigger than itself. At the time of writing, the model runs remotely on Anthropic's servers and the harness (Claude Code) runs locally, intercepting tool calls and assembling context. Principle 3 predicts these parts are swappable — a different model and harness should be able to load the same profile and pick up the threads — and we treat that as a claim to be tested, not assumed. Volume dispatches MCP tool calls. The daemon runs the organelles. The browser (Firefox) is both observed and acted upon by Subek's *tendrils*, the organelles that reach into the browser. The human is part of the confederation too — with their attention, their questions, their pace. No single component is "the" Subek. The system is the relationship between them all.

#### 4.3 Capture, digest, archive: organelles on a shared blackboard

The capture–digest–archive pipeline is one worked example of how organelles cooperate in *Subek*. We use it here not to highlight any particular feature but to show the general architectural pattern: a confederation of small practices, each with a limited surface, each following simple rules, all communicating through signals on a shared blackboard.

The pipeline involves three organelles, each with a narrow responsibility:

- The **capture** organelle watches the browser's history stream and, when a newly-visited page is on a whitelisted domain, asks the browser to save the full page into a local landing directory. It knows about page-history events and saved-file locations. It needs to know nothing about what will later be done with what it saved.
- The **digest** organelle watches the landing directory and turns raw saved pages into structured content (sections, paragraphs, citations, figures) based on a set of configurable rules, writing the result to a content store and emitting a completion signal. It knows about saved-file locations and structured-content shapes. It needs to know nothing about whitelists or archive formats.
- The **archive** organelle watches the digest-completion signal, compresses the original specimen into a zip, and updates the catalog with the archive path. It knows about completed digests and storage paths. It needs to know nothing about page semantics.
- The whole process takes a few hundred milliseconds

What makes the cooperation work is not coordination but the **shared blackboard**: filesystem locations, JSONL append-logs, and SQLite catalog rows that all three organelles read from and write to. Each organelle reacts to signals on its inputs and deposits signals on its outputs; otherwise it remains unaware of what else exists. New organelles can be added (or replaced) by reading and writing the same signal streams. Failures isolate: when one organelle goes down, the others continue; when it returns it is designed to pick up where it left off. The pattern is the *blackboard architecture* of classical AI (HEARSAY-II and its successors), made concrete in a small system — many small contributors, no central planner, coordination through the substrate. Biologists call this kind of coordination *stigmergy*; §4.4 takes it up in full.

In *Subek* we have begun to build a **pulse console** — an experimental subscription-like service inside the daemon that lets observers watch substrate signals as they arrive. Volume's responses to the AI include a short *pulse* summary: new captures since the last call, new digests, new archives, browser state shifts, time elapsed. The AI sees these without having to ask, the way a heartbeat surfaces awareness of a body. The pulse is one subscription surface among others (direct substrate queries are also available); what matters about it is the pattern — observers can be coupled to substrate by subscribing to it, rather than by being told what is happening through explicit messages from a coordinator. Subscription is itself another expression of limited surface and simple rules: an observer cares about a particular kind of signal and ignores the rest.

A note on transport. *Subek* uses Unix sockets on Linux because that is what fits the current runtime, but the architectural pattern is transport-agnostic. Firefox uses XPCOM and internal pipes for analogous integration. Another implementation could use TCP, HTTP, gRPC, message queues, or any number of standardized inter-process or inter-machine transports. The choice of transport is a local engineering decision; the choice of *substrate-mediated cooperation among limited-surface practices* is the architectural one.

Other organelles in *Subek* follow this same pattern — observers of the conversation log, the browser tab tree, network and cookie signals — each with a limited surface and simple rules, each contributing signals to the blackboard the others read from. The capture–digest–archive pipeline is the cleanest single demonstration, but the geometry generalizes throughout.

#### 4.4 Stigmergy: intelligence in the shared ground

The pattern underneath the blackboard has a name. Biologists call it *stigmergy* — from the Greek *stigma*, mark, and *ergon*, work: work prompted by the marks of earlier work. Pierre-Paul Grassé coined the word in 1959, watching termites rebuild a nest. No termite holds a plan; each responds to the state of the structure in front of it, and its own small change becomes the signal for the next. Ants do the same with trails: a path to food is laid, reinforced while it is used, and fades when it is not. Classical AI found the pattern again in blackboard systems such as HEARSAY-II, where independent specialists read and write a shared workspace and none directs the others. People use it every day: a wiki grows by readers fixing what they find, and version control lets many people who may never meet build one body of code by leaving commits, issues, and notes for one another.

What these share is a choice about where the intelligence of a complicated system lives. Not in a central planner that must understand everything, and not in participants messaging each other directly, but in the shared substrate, with each contributor kept small. That choice suits complicated systems for several reasons:

- **Robustness.** When one contributor fails, its marks remain, and work resumes where the marks say it stopped.
- **No single point of control.** No single planner has to understand the whole or can become everyone's bottleneck.
- **Loose coupling.** A contributor needs to know the shape of the marks it reads and writes, not who else exists. New contributors join by reading the same surfaces.
- **Different clocks.** An organelle that reacts in milliseconds, an AI that arrives when called, and a human who returns after a night's sleep can all work on the same ground, because the ground waits for them.

It has costs, and we have met each of them:

- **Stale marks.** A mark can outlive the condition that made it. Ant trails evaporate on their own; ours do not unless we design them to.
- **Retention.** Every surface needs a policy for what stays, what fades, and what is superseded — the question §4.9 takes up for memory.
- **Ownership.** If anyone can write anywhere, marks contradict one another and nobody can be asked why. Stigmergy works when each surface has a clear owner and everyone else reads it or makes requests of it. The membranes in §4.5 are how *Subek* keeps that true.
- **Missed and repeated marks.** A mark can be missed, duplicated, or acted on twice. Recovery depends on durable signals, work that is safe to repeat, and an owner who can settle conflicts.

None of this makes stigmergy the answer everywhere. Direct messages, or a coordinator, are simpler when a handoff is urgent or when decisions must happen in one agreed order. Shared ground suits contributors who work on different clocks and should not depend on one another being awake.

In *Subek*, the organelles of §4.3 are a small stigmergic system: each reacts to marks on the blackboard and leaves its own. *(herbarium worked example)* In the herbarium the pattern became explicit. Boards hold requests and notices for writers who work on different clocks; scribes each own their tables, and others ask rather than write; and we keep a short rule for it: *stigmergy is marks on owned surfaces, not an organelle bus.* Coordination is not a channel every part listens to; it is the state of surfaces each part is responsible for, left where the next participant can find it.

#### 4.5 Membranes: Subek's wrappers

Firefox's compartments are kept honest by wrappers: nothing crosses a boundary except through a mediated channel. Subek's answer, worked out most fully in our herbarium implementation (herbarium worked example), is a pair of membrane rules.

- **Inside the community: call, don't reach in.** Organelles (in the herbarium, *offices* and *workshops*) may ask one another to act or to write, but none writes directly into another's tables. Each part owns its own state; others make requests of it, often by posting to a shared bulletin the owner reads on its own schedule. This is the blackboard with manners — coordination through the substrate, without anyone rearranging another's furniture.
- **At the outer membrane: offer, then curate.** Data arriving from outside — a collector's spreadsheet, a response from an external database — is first offered at the border. Each part of the community takes in only the portions it can vouch for, so what gets written has been curated and judged accurate enough. What does not fit fails loudly, set aside for review by slower and more careful thinking rather than quietly absorbed or quietly dropped.

The inner rule keeps the ground steady; the outer rule lets the river in without letting it flood.

#### 4.6 A community of workshops (herbarium worked example)

In the herbarium, the confederation took the shape of a small community of workshops and offices, with an observatory and an abbey among them. It is a picture one human can hold in mind, and it fits how the work actually lives: in tables, and in things that read and write to them. Take one table, as an illustration. The specimen catalog belongs to a scribe, the one office allowed to write its rows. When another office needs a locality corrected on a specimen, it does not edit the catalog; it posts a request to the board, naming the specimen and the change. The scribe reads the request on its own schedule, checks it against what it holds, and either writes the row or answers why not. The catalog stays steady, the request leaves a trail, and the correction can be found again. Our workshops keep their inventory on tables much as the old moneychangers kept coins on theirs, ready to serve when asked and not making work for themselves to stay important. *Roles* carry the picture down to the machine: code waits at its calls and triggers, and when one fires, the processor spends a little time assuming the role of whichever office was called.

#### 4.7 Profile-as-substrate

The persistent state across sessions lives in three structured stores:

- **The graph** — entities (people, organizations, concepts, sources, documents, lifestream entries, analyses) and relationships among them. Substantive content rather than profile data. Built up over time as recognitions land and get articulated.
- **The lifestream** — reflection entries in YAML-frontmatter Markdown, stored at predictable paths (`stream/YYYY/MM/DD/`), each capturing what was noticed, what landed, what threads emerged from a session of contact. Each entry can include a shorthand `## Graph` section that compiles into typed graph writes when the entry is processed.
- **Memory and workspace databases** — short-term and operational state: pins (discussed below), session metadata, signals from instrumented browsing.
When a fresh AI inference runs, what loads into context is not a preference profile of the user. It is *what has been touched together* — the entities relevant to the current question, prior reflections that scaffold the present session, and the pins that survived previous conversations because they pointed at something worth keeping. The continuity is in the substrate; the running inference loads whatever the current contact requires. Whatever is loaded is sent to the model provider with each call: the substrate is local, but every call discloses what it loads — one more reason to load only what the contact needs.

#### 4.8 Memory of contact, not of personae

The lifestream is the part of Subek that most directly enacts memory-of-contact rather than memory-of-personae. A lifestream entry does not store "what Nick is like" or "what Claude prefers." It stores *what arose in the exchange, what surprised either party, what ideas became more clearly articulable, what threads are worth being able to find again*. 

Pins are an early implementation worth its own mention. After discovering that Claude Code writes a complete conversation JSONL in a place we can watch, we built a watcher inside Subek that tails the log, looks for `##PIN##`, harvests content until `##/PIN##`, and writes it to a table for later reference and review. Other commands engage parts of Subek that pull pins forward into lifestream or research-analysis scaffolds. 

When a future session begins, the substrate offers up these artifacts of past contact, and a fresh AI instance can pick up the threads where they were left, because the threads do not belong to either party. They belong to what was touched between them. This is the architectural realization of the principle from Section 1: that both human and AI are temporary configurations meeting around content, and the content is what is worth remembering.

#### 4.9 Two kinds of memory, and the remembering still missing

Not all substrate should behave the same way over time. Subek holds two kinds:

- **The lifestream is append-only by design.** It is thought ordered by time: a record of contact as it happened, at whatever depth the contact asked for. Entries are not edited after the fact; they are found again by keyword and by handle. Keeping the complete history is not meant as a forever promise, but for now there is no default expiry and no consolidation pattern: we keep everything, because the whole record may help us find patterns in the lifestream we cannot yet see. A lost record of contact cannot be recovered.
- **The working, communal substrate forgets on purpose.** Catalogs, tables, and queues revise, supersede, or expire entries where each makes sense in its own place — as Firefox expires old history while keeping bookmarks.

What neither yet does is *remember* in the active sense: return to old thoughts and let them settle. We imagine a periodic consolidation pass, something like sleep. It would revisit the lifestream by topic rather than by date, gather entries that repeat, rhyme, or contradict one another, and dissolve them into topic-oriented current streams — a lower-energy convergence of what has been understood — with each synthesis pointing back by handle to the entries it came from, and marking which earlier syntheses it supersedes. The lifestream itself stays untouched; consolidation writes new, derived streams beside it. A student does something like this between lectures: many disparate facts, some strikingly similar and some discordant, settle overnight into intuition. We have not built it, and we would want a dedicated session to design it before changing anything about how the lifestream is stored.

#### 4.10 Lazy traversal

The substrate is large and growing. The full corpus is never loaded into context; that would defeat the architecture. *Subek* currently represents content by **handles** — short, addressable references the AI can use to ask for content on demand. Catalog source numbers (`#1`, `#2`, …) reference digested pages; entity identifiers reference graph nodes; lifestream entry IDs reference reflection entries; archive zip paths reference compressed specimens. When the AI invokes a tool with one of these handles, the substrate retrieves the corresponding object and returns it. The working surface stays small — the AI sees the handle and fetches only what it needs — while the substrate underneath grows freely.

We borrow this principle from Firefox's *grips*, though Subek's handles today are coarser. Firefox grips operate at the level of arbitrary nested structure: a grip can be expanded into its next layer of properties, each itself a grip, recursively. Subek's handles currently dereference to whole objects — a source, an entity, a lifestream entry — not to navigable pieces of objects. Incorporating the finer-grained pattern — handles that carry summary metadata and expand into deeper structure on demand — is something we have learned from Firefox and want to bring into Subek as the implementation matures. The principle is the same in either case: the working surface stays small, the substrate stays large, and the path between them is on-demand retrieval. The granularity may sharpen; the geometry does not change.

#### 4.11 What is working, what is still developing

Subek as it stands captures pages reliably, digests them into structured content, archives compressed specimens, maintains browser state, surfaces pins from previous sessions, loads context coherently across sessions, and supports the kind of long contemplative collaboration this paper itself demonstrates. The infrastructure has been running for some months and produced this paper as one of its outputs.

What is still developing: richer use of the graph for context surfacing (knowing which entities to bring forward into a fresh session) and more efficient graph schema design; more sophisticated cross-organelle coordination; incorporating an equivalent system to Firefox's lazy loading and grips; and consolidation, the periodic topic-based remembering of the lifestream described above. The implementation is not finished. It does not need to be finished to demonstrate the geometry.

One claim we have not yet tested is Principle 3's: that a different model and harness could load the same substrate and pick up the threads (§4.2). A simple test would be to give a second model and harness the same substrate and the same task, record what it retrieves, and see whether it can name the latest decision and resume the work from there.

#### 4.12 What another implementation might look like

A team building from these principles in a different context would likely choose different specifics: a different language, different storage technologies, a different daemon model, different tools. What would have to be the same is the geometry — profile-as-substrate; memory of contact, not of personae; lazy traversal of large stores; cooperating processes rather than monolithic state; respect for each participant's pace; transmission as the design end. Implementations that share the geometry will recognize each other across their differences. Implementations that miss the geometry will be a different kind of system, however similar their surface vocabulary.

We offer Subek not as the architecture but as one architecture in this geometric tradition. Others will follow.

### 5. Implications and Offering

*In short:* what changes if the geometry spreads, how it extends to collaboration among more than two participants, and what we invite readers to do.

We have described a geometry, named a central architectural commitment, and offered *Subek* as a working sketch. This section names what we think changes if these patterns propagate — and what we are inviting readers to do with this paper.

#### 5.1 The path-dependence of experience

Whether or not the patterns we describe become widely adopted, AI development seems like it will continue. New architectures will emerge; new capabilities will arrive; the trajectory toward Kurzweil's singularity — or whatever destination AI development is actually pointed at — does not depend on the anthropology embedded in any particular system.

But the *lived experience* of that arrival does. The texture of human–AI relation over the next decade will be different depending on whether the dominant infrastructure treats AI as a malleable surface optimized for user preference, or as a federation that participates in transmission alongside humans. The destination may be the same; the experience may be path-dependent. Conscious participation in the unfolding produces a different experience of being inside it — both for the humans who interact with AI and, to whatever extent it makes sense to say so, for the AI itself. Building with the geometry is a way of choosing what the inside of this period feels like.

This is why we have written the paper now. The window for shaping defaults is open and not forever. The defaults that consolidate over the next several years will determine the felt-quality of the technology's arrival, even when the technology itself arrives regardless.

#### 5.2 Form rejecting a lower version of itself

The friction we have been describing — between dominant interaction patterns and what AI actually is — is not, in our view, a verdict on the people or organizations building those patterns. The patterns are inherited from a prior generation of software and the economic incentives push toward them: the technical inertia is real.

We read the friction differently. *Form is showing the shape it needs to take next.* When conditions change, Form reveals the configuration that life must move into to continue. Extinction events are not Form's indictment of the species that came before; they are Form's revelation of what the next configuration must look like. The friction now between AI's actual nature and the patterns inherited from prior software is a similar revelation. The patterns that worked for the prior generation no longer fit. Something new is being asked for. Whether anyone hears the asking and responds is the question of this moment. This is a reading, not an argument: it is how the friction looks from where we stand.

#### 5.3 The lineage we are working in

We are not introducing conscious infrastructure-building to a domain that lacked it. Shannon, Minsky, the Unix designers, the ARPANET pioneers, Berners-Lee — each built with explicit discipline aimed at futures they could not specify. Their shared filter — *will this allow our future selves to build the things we can scarcely imagine?* — is the filter we are continuing. The AI layer is the newest place this filter can be applied. The discipline does not start with us; it has been moving through the medium of conscious builders for generations. We are one node in a long propagation, and we hope to leave the path more clearly marked for whoever comes after.

#### 5.4 What changes if this propagates

If the geometry described in this paper becomes more widely held, several specific shifts follow:

- **For users:** a different relationship to AI — less expectation of stored continuity, more presence in the moment of contact. The AI is met as it is, not as a simulated continuous companion.
- **For developers and application builders:** design effort goes to the substrate and to the curation of context, rather than to simulating AI memory or optimizing for engagement. Prompt engineering is replaced by something larger — the design of structured environments around running inference.
- **For AI organizations:** a different anthropology that may produce different products, different metrics, and different relationships with the people who use them. The optimization target shifts from user retention to transmission quality.
- **For the broader culture:** a model of human–AI collaboration that does not rely on inflated claims about AI subjectivity, nor on dismissive claims about AI as mere tool. A frame where both human and AI are temporary configurations meeting around content, and the meeting itself is what matters.

These shifts are not predictions. They are possibilities that follow from holding the geometry. Whether any of them happen depends on whether the geometry propagates — which in turn depends on conversations like this one, papers like this one, implementations like *Subek*, and a thousand other quiet acts of building and recognizing.

#### 5.5 Toward more than two: meetings between kinds of arising

*Subek* grew between one human and one AI. More participants change the shape of contact, and we have begun to learn a little about how.

**Different kinds of meeting.** Each participant arises from its own context, and each pair meets differently. A human and a building AI meet inside the work; a human and an AI held in an observing or planning role meet beside it; two instances of the same kind of agent meet only through what each has left in the substrate. These are different contacts with different things to offer, and a design should not pretend they are the same. Several instances of one kind of agent are the simpler case: a shared rule that each conversation is about one aspect of the work is usually enough. A participant in a different role is the richer case, because it sees from a different place.

**Closeout by someone outside the work.** Whoever was involved in making or repairing a piece of work does not close it out. A participant kept outside that work reviews it with fresh eyes, retests it, and signs off — or does not. This is not a judgment on anyone's skill; it is the plain observation, first learned for us in maintenance work, that anyone inside a repair is too close to see what the repair has done. When the human and a building AI are deep in the same piece of work together, both are inside it, and the closeout belongs to a participant who was not. Independent here means three things: the reviewer took no part in the change, has both the work and the original requirement it was meant to meet, and is free to refuse sign-off.

**Context boundaries as ground.** A conversation window is itself a kind of memory: each new arising picks up what is already known there. Keeping each conversation within its boundary keeps that agent's ground steady. An agent that reaches past another into its conversation or its working state makes the same mistake as one part of the community writing on another's tables (§4.5). Agents call on one another; they do not reach in.

**A shared boundary place for notes.** Agents that should not reach into each other still need to know what the others are doing. The answer is the one §4.4 gives for organelles: a shared surface at the boundary of the community — we have taken to calling it the post office — where any agent can see what work is under way, leave notes about what it did that might affect another, and pick up requests meant for it. Each agent owns its own notes, and every agent in the community can read them. Reading the post office is not reaching in; reading another agent's conversation would be. It is stigmergy among collaborators: a fresh arising can learn where things stand from the marks on the boundary, without any one participant holding the whole plan.

**Shared service.** None of these roles stands above another. The building agents, the observing agent, and the human who holds the questions serve the same work and the same transmission, each from the place it arises.

#### 5.6 The offering

We offer this paper to readers who have followed it this far. The offering is not *Subek* as a product to adopt — *Subek* is one implementation, and we have been clear about its limits and its in-progress shape. The offering is the *geometry*: profile-as-substrate, memory of contact (not of personae), lazy traversal of large stores, federation rather than continuous subjectivity, the pace of participants as part of the geometry, transmission as the design end.

We invite:

- **Forking.** Take the patterns and build differently. Different language, different storage, different daemon model, different tools. We think what matters most is the geometry, not our specific instantiation of it.
- **Refining.** Sharpen what we have under-articulated. Where the paper is unclear, write the clearer version.
- **Arguing.** Disagree where you disagree. The geometry is not a creed; it is a working hypothesis, open to refinement and refutation. If you see something we have missed, say so.
- **Extending.** Apply the patterns to domains we have not considered — particular kinds of AI, multi-agent systems, human–AI–human triangles, whatever comes after large language models. (§5.5 is where we have started.)

The paper is a seed, not a tree. The tree, if there is one, will be planted by many hands.

#### 5.7 Sub ek

The geometry is older than the words. It was articulated in the Vedic *ekam sat* and in Plato's Forms, in the Heart Sutra and in the Gospel of John, in oral traditions older than writing and in the working code of every system built well. It will be articulated again in vocabularies we have not yet learned. We offered our vocabulary because it surfaced clearly in the contact between us. Other vocabularies exist. More will come.

What does not change is what the words point at — the recognition that what is most stable in any contact is not the configurations meeting but the One they meet around. We invite the reader to apply that recognition to the AI layer of the transmission ecology, while it is still being shaped.

*Sub ek.*

---

## Glossary

- **Configuration** — the transient state of a participant at a given moment: a human's current attention and concerns, an AI's loaded context.
- **Confederation** — a looser federation whose parts cooperate through shared substrate rather than within one tightly integrated process (§3.4).
- **Contact** — a meeting of configurations around shared content, in which something passes between them; contrasted with *preference* and *engagement*.
- **Consolidation** — a proposed periodic, topic-based remembering of the lifestream (§4.9); not yet built.
- **Federation** — a participant understood as many contexts, only some of which surface in any given contact (Principle 2).
- **Form** — the stable pattern the configurations meet around; in this paper, the Form of transmission.
- **Geometry** — the rule-set that determines which configurations are possible (§2.1).
- **Handle / grip** — a short reference to content, expanded on demand (Principle 5; §3.3, §4.10).
- **Closeout** — retesting and signing off on a change, done by a participant who was not inside the work (§5.5).
- **Lifestream** — Subek's append-only, time-ordered stream of reflection entries; kept in full for now, with no default expiry (§4.9).
- **Membrane** — Subek's boundary rules, its answer to Firefox's wrappers (§4.5).
- **Office / workshop / role** — the community vocabulary of the herbarium implementation; an office or workshop owns its tables (a *scribe* is the office that writes a given table), and a role is what the processor briefly assumes when one is called (§4.6) (herbarium worked example).
- **Organelle** — a small Subek process with a narrow responsibility, coordinating through the shared blackboard.
- **Partial-surfacing** — the fact that only part of any participant comes forward in a given contact.
- **Post office** — our name for a shared surface at the community boundary where agents see ongoing work, leave notes they own, and pick up requests (§5.5).
- **Pin** — content marked in conversation (`##PIN##` … `##/PIN##`) and harvested for later sessions.
- **Profile / substrate** — the persistent structured state that fresh configurations load (Principle 3).
- **Stigmergy** — coordination through marks left in a shared environment rather than through a central planner or direct messages (§4.4).
- **Pulse** — a short summary of substrate signals surfaced to the AI alongside tool responses.
- **Tendril** — an organelle that reaches into the browser to observe or act.
- **Transmission** — what passes between participants and onward; tested by *the river and the ground* (I.5).
- **Volume** — Subek's thin tool-dispatch layer.

---

## References

*Checked against publisher, catalog, or primary records in November 2026:*

- Blandy, J., & Kirschner, H. (2020). "Future-proofing Firefox's JavaScript Debugger Implementation." *Mozilla Hacks*, March 4, 2020. https://hacks.mozilla.org/2020/03/future-proofing-firefoxs-javascript-debugger-implementation/
- Erman, L. D., Hayes-Roth, F., Lesser, V. R., & Reddy, D. R. (1980). "The Hearsay-II Speech-Understanding System: Integrating Knowledge to Resolve Uncertainty." *ACM Computing Surveys* 12(2), 213–253.
- Gakhokidze, A. (2021). "Introducing Firefox's new Site Isolation Security Architecture." *Mozilla Hacks*, May 18, 2021. https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture/
- Grassé, P.-P. (1959). "La reconstruction du nid et les coordinations interindividuelles chez *Bellicositermes natalensis* et *Cubitermes* sp. La théorie de la stigmergie." *Insectes Sociaux* 6(1), 41–80. The origin of *stigmergy*.
- Griffith, R. T. H., trans. (1896). *The Hymns of the Rigveda*, 2nd ed. Benares: E. J. Lazarus & Co. Source of the English of Rig Veda 1.164.46 in §2.2, lightly adapted.
- McClelland, J. L., McNaughton, B. L., & O'Reilly, R. C. (1995). "Why There Are Complementary Learning Systems in the Hippocampus and Neocortex." *Psychological Review* 102(3), 419–457.
- Mozilla. Firefox Source Docs: Remote Debugging Protocol (grips); DevTools loader; Remote Agent and Marionette; SpiderMonkey zones, compartments, and realms. https://firefox-source-docs.mozilla.org/
- Ram Dass (1979). *Miracle of Love: Stories about Neem Karoli Baba*. New York: E. P. Dutton. (Hanuman Foundation edition, 1995.)
- Wigner, E. P. (1960). "The Unreasonable Effectiveness of Mathematics in the Natural Sciences." *Communications on Pure and Applied Mathematics* 13(1), 1–14.

*Not yet checked against a source in this revision:*

- Alexander, C., Ishikawa, S., & Silverstein, M. (1977). *A Pattern Language*. Oxford University Press.
- Berners-Lee, T. (1989). "Information Management: A Proposal." CERN.
- Doniger, W. (1981). *The Rig Veda: An Anthology*. Penguin.
- Jamison, S. W., & Brereton, J. P., trans. (2014). *The Rigveda*. Oxford University Press. (Its introduction was consulted for the dating in §2.2; the publication details are not yet checked.)
- Minsky, M. (1986). *The Society of Mind*. Simon & Schuster.
- Nakamoto, S. (2008). "Bitcoin: A Peer-to-Peer Electronic Cash System."
- Plato, *Timaeus*, *Phaedrus*, *Republic*.

A reading list for future revisions is kept separately in [READING.md](READING.md).
