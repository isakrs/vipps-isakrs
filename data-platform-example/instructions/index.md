---
title: Data Platform House Instructions And Backlog
---

# Data Platform House Instructions And Backlog

<style>
  .data-platform-feedback {
    border: 1px solid #d0d7de;
    border-radius: 8px;
    padding: 16px;
    background: #fff7f2;
    margin: 16px 0 24px;
  }

  .data-platform-feedback a {
    font-weight: 700;
  }

  .data-platform-kanban {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
    margin: 16px 0 28px;
  }

  .data-platform-lane {
    border: 1px solid #d0d7de;
    border-radius: 8px;
    background: #f6f8fa;
    padding: 14px;
  }

  .data-platform-lane h3 {
    margin-top: 0;
  }

  .data-platform-card {
    border: 1px solid #d0d7de;
    border-left: 4px solid #ff5b24;
    border-radius: 8px;
    background: #ffffff;
    padding: 12px;
    margin: 10px 0;
  }

  .data-platform-card strong {
    display: block;
    margin-bottom: 4px;
  }

  .data-platform-card span {
    color: #57606a;
    display: block;
    font-size: 0.92em;
  }

  .data-platform-source-grid {
    display: grid;
    gap: 12px;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    margin: 16px 0 24px;
  }

  .data-platform-source {
    border: 1px solid #d0d7de;
    border-radius: 8px;
    background: #ffffff;
    padding: 12px;
  }

  .data-platform-source strong {
    display: block;
    margin-bottom: 4px;
  }

  .data-platform-source span {
    color: #57606a;
    display: block;
    font-size: 0.92em;
  }
</style>

## Routes

The main experience address stays:

https://vipps.isakrs.com/data-platform-example/

That route should open the Three.js world first.

The instructions, backlog, and concept brief live here:

https://vipps.isakrs.com/data-platform-example/instructions/

The experience should stay public by direct link, but not available through
Google or other search engines yet. Keep `noindex` metadata on the Three.js
world, the instructions page, and the character knowledge pages until Isak
explicitly decides the experience is polished and approved enough for search
indexing.

We also want some form of automation that helps the project improve over time.
Everything else is open again.

## Current State

The previous implementation has been deleted and replaced with a clearer split:

- `/data-platform-example/` is the entrance to the Three.js world.
- `/data-platform-example/instructions/` is the planning brief, development
  backlog, and instruction source.

This file should serve two purposes:

- A useful written explainer that helps people understand how data flows and how
  the platform process works.
- A planning brief and storyboard for the Three.js experience.

The first real deliverable should be the Three.js experience. The written page
should support it by making the story, flow, characters, and process clear
before the scene becomes too complex.

[Enter the Three.js world](/data-platform-example/)

## Feedback Loop

Most feedback should happen through agent conversations. Tell an agent what
confused you, what should become more playable, which character should know
something, or which part of the data flow deserves a better scene. The agent can
turn clear input into instruction changes, backlog changes, character knowledge,
or implementation work.

Use the GitHub feedback form when the input should be saved outside the
conversation, shared with others, or tracked by the workday automation. A person
can fill it in directly, and an agent can also use it as the durable public
record when a conversation produces useful public-safe feedback.

## Open Asset Strategy

The experience should reuse strong existing Three.js examples, open three-dimensional
assets, open object libraries, and proven animation patterns wherever that gets
the house closer to a polished game faster. Do not reinvent character animation,
keyframe animation, lighting, loaders, controls, materials, props, or staged
environment structure when a permissive example already shows the right shape.

Reuse must still be tidy:

- Keep the data platform story, rooms, pipes, and dialogue specific to this
  experience.
- The borrowed keyframes house is the data platform house, not a decoration.
  Pipes should visibly enter, cross, and leave that house through meaningful
  ports.
- Use assets only when their license is compatible with public sharing.
- Give visible credit when attribution is required or useful.
- Keep a procedural fallback for important external assets so the page does not
  break if a model cannot load.
- Prefer direct vanilla Three.js adaptation for this repository. React-oriented
  libraries can inspire object patterns and interaction design, but should not
  force a framework or bundler into this static page unless the project
  deliberately changes direction.

The first preferred sources are:

<div class="data-platform-source-grid" aria-label="Preferred open object sources">
  <article class="data-platform-source">
    <strong><a href="https://threejs.org/examples/">Three.js examples</a></strong>
    <span>Use for animation, loaders, postprocessing, camera behavior, interaction patterns, and credited sample models.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://github.com/pmndrs/three-stdlib">three-stdlib</a></strong>
    <span>Use for reusable Three.js helpers and examples that can fit a static vanilla page.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://github.com/pmndrs/drei">drei</a></strong>
    <span>Use as inspiration for mature scene components, controls, effects, and interaction patterns, then adapt carefully.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://kenney.nl/assets?category=3d">Kenney</a></strong>
    <span>Use for cohesive Creative Commons Zero game-ready props, interface assets, and environment kits.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://quaternius.com/">Quaternius</a></strong>
    <span>Use for Creative Commons Zero low-poly characters, buildings, furniture, pipes, dinosaurs, and animation-friendly game kits.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://polyhaven.com/">Poly Haven</a></strong>
    <span>Use for Creative Commons Zero physically based materials, high-dynamic-range lighting, and realistic model detail.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://ambientcg.com/">ambientCG</a></strong>
    <span>Use for Creative Commons Zero textures, materials, and surface realism.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://github.com/KhronosGroup/glTF-Sample-Assets">Khronos glTF Sample Assets</a></strong>
    <span>Use for glTF loading, validation, animation, material, and extension reference assets.</span>
  </article>
</div>

## Development Backlog

This board is the lightweight product tracker for the house. It should stay
small, visible, and opinionated: cards should move because they make the signal
journey clearer, the game more playable, the characters more useful, or the
event version more convincing.

<div class="data-platform-feedback">
  <strong>Give input:</strong>
  Tell an agent what you noticed. If the input should be saved outside the
  conversation, use
  <a href="https://github.com/isakrs/vipps-isakrs/issues/new?template=data-platform-house-feedback.yml">the Data Platform House feedback form</a>.
  The form keeps public-safe context available to agents and the workday
  automation.
</div>

<div class="data-platform-kanban" aria-label="Data Platform House development backlog">
  <section class="data-platform-lane" aria-labelledby="backlog-now">
    <h3 id="backlog-now">Now</h3>
    <article class="data-platform-card">
      <strong>Improve world interaction</strong>
      <span>Make walking, tapping people, and following pipes feel more like a small game on desktop and mobile.</span>
    </article>
    <article class="data-platform-card">
      <strong>Make rooms belong to the house</strong>
      <span>Turn labels and characters into readable areas of the keyframes house instead of floating rooms around it.</span>
    </article>
    <article class="data-platform-card">
      <strong>Replace procedural props with open kits</strong>
      <span>Turn hand-made machines, shelves, furniture, and pipe details into better sourced three-dimensional objects where licenses allow it.</span>
    </article>
    <article class="data-platform-card">
      <strong>Explain payment event journey</strong>
      <span>Make a tap or send payment event readable from source to data product.</span>
    </article>
  </section>

  <section class="data-platform-lane" aria-labelledby="backlog-next">
    <h3 id="backlog-next">Next</h3>
    <article class="data-platform-card">
      <strong>Broaden knowledge-backed dialogue</strong>
      <span>Let characters answer room-specific prompts, safe repository questions, and pipe-mode questions from their Markdown source files.</span>
    </article>
    <article class="data-platform-card">
      <strong>Deepen pipe language</strong>
      <span>Build on the visible legend, checkpoints, and quality gate with batch, backfill, and manual correction scenes.</span>
    </article>
    <article class="data-platform-card">
      <strong>Add first team characters</strong>
      <span>Ground Param, Kien, and Malo in safe real artifacts and useful rooms.</span>
    </article>
    <article class="data-platform-card">
      <strong>Animate storage to database</strong>
      <span>Show data leaving storage, being checked, and becoming queryable.</span>
    </article>
    <article class="data-platform-card">
      <strong>Add repository conversations</strong>
      <span>Let characters explain public GitHub repositories from Isak's account.</span>
    </article>
  </section>

  <section class="data-platform-lane" aria-labelledby="backlog-later">
    <h3 id="backlog-later">Later</h3>
    <article class="data-platform-card">
      <strong>Large language model conversations</strong>
      <span>Connect characters to their Markdown knowledge files for real-time questions.</span>
    </article>
    <article class="data-platform-card">
      <strong>Approved realistic avatars</strong>
      <span>Use recognizable likeness only where each person has explicitly approved it.</span>
    </article>
    <article class="data-platform-card">
      <strong>Consulting showcase mode</strong>
      <span>Make a customer-safe version that explains the same platform ideas.</span>
    </article>
  </section>

  <section class="data-platform-lane" aria-labelledby="backlog-input">
    <h3 id="backlog-input">Input Wanted</h3>
    <article class="data-platform-card">
      <strong>First journey</strong>
      <span>Button click, payment event, temperature reading, scheduled export, or storage movement?</span>
    </article>
    <article class="data-platform-card">
      <strong>Character approvals</strong>
      <span>Who has approved likeness, speech style, and behavior style?</span>
    </article>
    <article class="data-platform-card">
      <strong>Public versus internal answers</strong>
      <span>Which questions can characters answer publicly, and which need restricted mode?</span>
    </article>
    <article class="data-platform-card">
      <strong>Repository suggestions</strong>
      <span>Which public GitHub repositories should become rooms, workbenches, or dialogue topics?</span>
    </article>
  </section>

  <section class="data-platform-lane" aria-labelledby="backlog-done">
    <h3 id="backlog-done">Done</h3>
    <article class="data-platform-card">
      <strong>Direction reset</strong>
      <span>The old implementation was removed and this brief became the source of truth.</span>
    </article>
    <article class="data-platform-card">
      <strong>Twice-workday automation</strong>
      <span>Workday automations now improve, commit, and push useful changes twice per workday.</span>
    </article>
    <article class="data-platform-card">
      <strong>Link-only discoverability</strong>
      <span>The page is public by direct link, but should stay out of search engines until it is more polished.</span>
    </article>
    <article class="data-platform-card">
      <strong>Experience route split</strong>
      <span>The main route now opens the Three.js world and this subpage keeps the instructions.</span>
    </article>
    <article class="data-platform-card">
      <strong>First house shell</strong>
      <span>The first scene has rooms, animated data pipes, avatars, and repository blueprints.</span>
    </article>
    <article class="data-platform-card">
      <strong>Cinematic scene foundation</strong>
      <span>The world now uses postprocessing, stronger lighting, a glass-stage house shell, richer machines, and an animated Isak guide model with fallback.</span>
    </article>
    <article class="data-platform-card">
      <strong>Borrowed open animation assets</strong>
      <span>The world now uses the Three.js keyframes house asset and the morph/skinning guide asset as credited foundations instead of hand-rolling every visual.</span>
    </article>
    <article class="data-platform-card">
      <strong>Open object library shelf</strong>
      <span>The world now has an asset-library room that points future work toward Three.js examples, reusable helpers, and permissive object libraries.</span>
    </article>
    <article class="data-platform-card">
      <strong>House made central</strong>
      <span>The borrowed keyframes house now acts as the actual data platform house, with pipes routed into and out of house ports.</span>
    </article>
    <article class="data-platform-card">
      <strong>Orbit view controls</strong>
      <span>Visitors can now turn around the house by dragging the scene, using rotate buttons, or rotating from the keyboard.</span>
    </article>
    <article class="data-platform-card">
      <strong>Pipe modes made visible</strong>
      <span>The world now shows a public-safe flow legend, incremental checkpoints, a quality gate, and a serving flow.</span>
    </article>
    <article class="data-platform-card">
      <strong>First playable signal chosen</strong>
      <span>The first journey is a payment event, such as tapping or sending to a person.</span>
    </article>
    <article class="data-platform-card">
      <strong>First knowledge files</strong>
      <span>Isak, Param, Kien, and Malo now have public-safe Markdown source files.</span>
    </article>
    <article class="data-platform-card">
      <strong>First repository blueprints chosen</strong>
      <span>modern-data-platform-example and vipps-isakrs are the first public examples.</span>
    </article>
    <article class="data-platform-card">
      <strong>Character knowledge connected</strong>
      <span>The world now loads Markdown character files at runtime and uses them to enrich public-safe dialogue and repository links.</span>
    </article>
    <article class="data-platform-card">
      <strong>Agent-first feedback loop</strong>
      <span>Feedback normally starts in agent conversations and is saved in GitHub only when it needs a durable public record.</span>
    </article>
  </section>
</div>

The backlog stays local to this page for now. Agent conversations are the
primary input queue; saved GitHub feedback is the durable public record when
something should outlive the conversation. This board is the curated product
view.

## Confirmed Direction

Audience:

- External people who do not already know the Vipps MobilePay data platform.
- People inside Vipps MobilePay who need to understand how data flows and how
  the platform process works.
- A live company-event audience, for example North by North.
- A future consulting or portfolio audience where the experience can show both
  data platform thinking and interactive Three.js craft.

First deliverable:

- A polished Three.js experience, not just a written presentation.
- A small game where visitors can walk around, orbit the house, inspect rooms
  and pipes, and talk to people.
- Something that can also run in the background during an event while the team
  explains the data flow.
- Something that can later be used as a memorable selling point when explaining
  data platform work to new customers or collaborators.
- The written page remains useful as the explanatory backing and storyboard.

Show-and-tell flavor:

- The experience should support live role play.
- Dino and Wraptor can be explained with the team's dinosaur costumes.
- Smoke machines are part of the performance language. The Three.js version can
  also use virtual smoke when data moves, when a transformation happens, or when
  something exciting enters a new stage.
- Data moving from a storage account to a database should be visible in the
  three-dimensional scene, not only explained in text.

Character direction:

- Characters should resemble real teammates in look, speech, knowledge, and
  behavior when that is explicitly approved and safe to publish.
- Characters should be backed by Markdown knowledge files, so each person has a
  clear source of truth for what they know and explain.
- Characters should eventually be connected to large language models so visitors
  can ask real-time questions, not only choose from fixed dialogue.
- Characters can also talk about public GitHub repositories on Isak's account:
  what they are, why they exist, which data platform concept they demonstrate,
  and what a visitor should look at first.
- The first characters should be Isak, Param, Kien, and Malo.
- Isak is the most important first character and should be the main person to ask
  about the data platform.
- Malo should appear as an architect.
- The Three.js world should load the Markdown character knowledge files directly
  so dialogue stays reviewable, public-safe, and easy to improve without
  rewriting scene code.
- After the first set, the experience should grow toward the whole Data Insights
  team and then key collaborators around Vipps MobilePay.

First concepts to explain:

- Ingestion processes.
- Analytics projects.
- Data export.
- Data products.

First signal journey:

- A payment event, such as tapping to pay or sending money to a person.
- The public story should stay conceptual and must not expose real Vipps
  MobilePay payment data or real user data.
- The first path should show the event becoming a platform signal, landing in a
  storage account, moving through Databricks and Spark-style processing, being
  modeled with dbt-style transformations, and then becoming useful as a data
  product, analytics project, or declared data export.

Technologies that can be named:

- Databricks.
- dbt.
- GitHub Actions.
- Spark.
- Storage account, with Azure Storage Account or S3 as concrete examples.
- GitHub repositories as public, inspectable examples.

Large language model boundary:

- Characters can answer public-safe conceptual questions about data platform
  design, technologies, repositories, rooms, and the visible signal journey.
- Characters must not expose real Vipps MobilePay data, real Vipps MobilePay
  user data, secrets, private source images, or sensitive internal details.
- If internal and public modes are ever added, they should be separated clearly.
- Until that exists, default to public-safe explanations and metaphorical
  examples.

Architecture direction:

- The house should mirror the real Vipps MobilePay data platform to some extent,
  but it can stay metaphorical where that makes the story easier to understand
  or safer to share.
- It should also work as a reusable example for a customer-style setting, such
  as a Bama-like scenario, where the same platform ideas are explained without
  needing Vipps MobilePay-specific details.

Publishing direction:

- The page should stay public by direct link, but should not be available
  through Google or other search engines yet.
- It does not need to be promoted broadly yet. It is acceptable if someone finds
  the address through a direct link.
- The desired polish is fairly high before actively sharing it with others.

Automation direction:

- The automation should inspect Isak's personal repositories for inspiration and
  Git contributions.
- The automation may update the public page automatically.
- The automation must commit and push changes so every automatic change can be
  rolled back through Git history.

## Starting Vision

We want to explain a data platform through an explorable house metaphor, but the
main experience should be following a concrete data signal through the whole
system.

The visitor should be able to start with a signal as it emerges, such as:

- A button click in an application.
- A payment event.
- A temperature reading from a sensor.
- A file landing in storage.
- A row exported from an operational system.

Then they should follow that signal all the way through the platform until it is
used by people, models, dashboards, exports, alerts, or downstream systems.

The visitor should also be able to step into the process at each stage and
understand what is happening there.

Possible direction:

- The house represents the data platform.
- Pipes represent the signal moving in, through, and out of the platform.
- Rooms represent checkpoints in the signal journey.
- Characters inside rooms represent real people or real roles from the team and
  explain work they have actually done.
- The visitor can follow the signal from room to room or jump directly into a
  stage to understand that part of the flow.
- The interaction should feel like a small exploratory game: walk around, enter
  rooms, inspect machinery, follow pipes, and talk to humans.
- Dialogue can borrow the feeling of an old handheld role-playing game, but the
  characters should be smarter than fixed dialogue trees. Each character should
  have a Markdown knowledge file and eventually a large language model-backed
  conversation layer.
- The visual ambition could eventually be a polished Three.js scene with
  animated characters, camera movement, cutaway rooms, and richer materials.

None of this is locked in yet.

## First Playable Journey

The first playable journey is a payment event.

The visitor should be able to follow a payment-related signal, such as a tap or
send action, without seeing real payment data or real user data.

Suggested journey:

1. A person taps or sends a payment.
2. The application emits a conceptual payment event.
3. The event is captured by the ingestion process.
4. The event lands in a storage account, such as Azure Storage Account or S3.
5. Databricks and Spark-style processing validate and shape the data.
6. dbt-style models turn the signal into reusable analytical meaning.
7. An analytics project consumes the modeled data.
8. A declared data export sends an approved output to a destination.
9. A data product presents governed, useful data with ownership and support.

The experience should show both the happy path and the platform thinking around
it: ownership, contracts, quality gates, lineage, privacy, and safe use.

## Real Artifacts

"Real artifacts" means evidence that a character, room, or repository
conversation is grounded in something concrete instead of invented decoration.

Artifacts can include:

- Public GitHub repositories.
- Specific public files or examples.
- Local personal repository paths that are safe to summarize.
- Documentation pages.
- GitHub Actions workflows.
- Markdown knowledge files for characters.
- A dashboard, notebook, table, model, or job when it is safe and approved to
  mention.

For the first version, use public-safe artifacts:

- `https://github.com/isakrs/modern-data-platform-example` for the operating
  model, contracts, governance, analytics projects, data products, and declared
  exports.
- `https://github.com/isakrs/vipps-isakrs` for the live Three.js/static-site
  implementation, automation direction, backlog, and feedback loop.
- `https://github.com/isakrs/opcua-influxdb-grafana-dummy` or
  `https://github.com/isakrs/node-opcua-logger` later as older sensor-event
  examples if the house needs a non-payment contrast journey.

This means the first characters can explain real, public examples without
claiming ownership over sensitive internal systems.

## Character Knowledge Files

These files are the first public-safe source material for future character
conversations:

- [Isak](/data-platform-example/characters/isak.html)
- [Param](/data-platform-example/characters/param.html)
- [Kien](/data-platform-example/characters/kien.html)
- [Malo](/data-platform-example/characters/malo.html)

They should stay reviewable, concise, and safe for the public version.

## GitHub Repository Conversations

Characters should also be able to talk about public GitHub repositories on
Isak's account.

The goal is not to make visitors read source code in the scene. The goal is to
turn repositories into explainable artifacts:

- A repository can become a blueprint on a wall, a workbench in a room, a book in
  a library, a control panel, or a portal into a deeper explanation.
- A character can explain what the repository demonstrates and why it matters.
- A character can point to the files, examples, or ideas a visitor should inspect
  first.
- A repository can show how the same data platform concept appears in code,
  documentation, automation, or a demo.
- A repository can help connect the consulting showcase version with practical
  proof that Isak can build the thing being explained.

Repository conversations should answer:

- What is this repository for?
- Which data platform concept does it demonstrate?
- What should a new visitor look at first?
- What room, pipe, character, or signal journey should it influence?
- Is it safe for the public version, or should it stay internal-only?
- What could be improved next?

Possible first treatment:

1. Add a GitHub library or blueprint table inside the house.
2. Let Isak explain a selected repository in plain language.
3. Connect that repository to one platform concept, such as ingestion, analytics
   projects, data export, or data products.
4. Add a link out to the repository for visitors who want to go deeper.
5. Let the automation notice new public repository work and suggest better
   repository dialogue when it clarifies the experience.

First repositories to represent:

- `modern-data-platform-example`: the main blueprint for producer-owned
  contracts, platform validation, governed access, analytics projects, declared
  exports, and data products.
- `vipps-isakrs`: the repository that contains this public experience, the
  instructions, the backlog, the feedback form, and the automation direction.
- `opcua-influxdb-grafana-dummy` or `node-opcua-logger`: optional later
  historical examples for sensor-style event ingestion and observability.

## Written Explainer Direction

The written page should still be useful, even though the first real deliverable
is the Three.js experience.

The page should help someone understand:

- Where data starts.
- How it enters the platform.
- What process and ownership expectations exist around it.
- How different flow modes work.

Current visible flow modes in the world:

- Streaming: the payment signal arrives live from the conceptual tap or send.
- Incremental processing: checkpoint rings show that some movement happens in
  controlled chunks rather than as one full refresh.
- Quality gate: a distinct gate marks the point where validation and trust
  checks must pass before modeled outputs continue.
- Declared export: a dedicated branch shows governed outbound delivery rather
  than raw copying.
- Serving flow: a separate path shows trusted outputs heading toward a data
  product, dashboard, or downstream use.
- Repository reference: the GitHub Actions path acts as an implementation
  blueprint rather than production data movement.
- How the data becomes trustworthy enough to use.
- Where it is used at the end.
- Who to ask when they are confused or something breaks.

The page should read like an approachable walkthrough and storyboard, not like
raw platform documentation. It can use the house metaphor, but the reader should
come away with a real understanding of the data flow and process.

Possible page structure:

1. Start with one concrete signal.
2. Show the whole journey in a simple flow overview.
3. Walk stage by stage through the process.
4. Use small sidebars for characters and real team work.
5. Use pipe labels to show whether each flow is scheduled, streaming,
   incremental, a backfill, or an export.
6. End with how the signal is used and who owns keeping it healthy.
7. Keep open questions and next-version ideas at the bottom.

This written page should be valuable even before the Three.js version is fully
polished. The interactive house can be built by turning each section into a
room, pipe, character, or dialogue moment.

## Interactive House Deliverable

The house is the target experience.

The written explainer is the foundation, not the final destination. The Three.js
house should grow from the signal journey, pipe semantics, real people, and real
work examples.

The house should:

- Let visitors follow one signal through the building.
- Let visitors enter rooms to understand a stage in the process.
- Let visitors move around like a small game rather than only clicking through a
  fixed slide deck.
- Show different pipe types through shape, rhythm, labels, and machinery.
- Include characters grounded in real people and real work.
- Let characters explain their room, the technology around them, the pipelines
  they own or have worked on, and how to build a great data platform.
- Let characters explain relevant public GitHub repositories from Isak's
  account when those repositories demonstrate the room, pipe, or platform idea
  they are talking about.
- Support real-time questions through a large language model layer, with one
  Markdown knowledge file per character.
- Show concrete movement between platform components, such as data moving from
  a storage account to a database.
- Support event-mode presentation, where it can run in the background while the
  team explains the flow live.
- Include playful effects such as virtual smoke, dinosaur-costume-inspired
  characters for Dino and Wraptor, and visible machinery around pipes.
- Keep the written explainer available, so the interactive version does not
  become the only way to understand the process.

The house should still be built in small steps. The best path is:

1. Make the written explainer and storyboard useful.
2. Choose the first signal journey.
3. Identify the first real people, artifacts, and flow modes.
4. Build the first interactive house prototype.
5. Add event-mode visuals and role-play hooks.
6. Let automation help refine the explainer, storyboard, and house.

First prototype scope:

1. A playable Three.js house shell with a few connected rooms.
2. One clear signal journey through ingestion, analytics project work, data
   export, and data product use.
3. Isak as the main data platform guide.
4. Param, Kien, and Malo as the next visible characters.
5. At least one visible storage-account-to-database pipe.
6. At least three pipe modes with distinct motion, shape, or machinery:
   scheduled batch, incremental processing, and export.
7. Markdown knowledge files for the first characters, even before the live large
   language model integration is built.
8. At least one public GitHub repository from Isak's account represented as a
   blueprint, library item, or workbench artifact.

## Core Experience Goal

The experience should answer this question:

> What happens to a signal after it is created, and how does it become useful?

The experience should make the invisible journey visible:

1. A signal emerges in a source system.
2. The signal is captured or exported.
3. The producer describes what the signal means.
4. The platform validates, lands, and processes it.
5. The signal becomes part of governed platform data.
6. Transformations, models, or enrichment make it more useful.
7. Access rules decide who can use it and why.
8. The signal becomes an insight, dashboard, data product, export, alert, or
   downstream feature.
9. Ownership, monitoring, lineage, and support paths explain who keeps it
   trustworthy.

Each stage should let the visitor pause and ask:

- What is happening here?
- Who owns this step?
- What artifact proves this step exists?
- What can go wrong?
- Who should I ask for help?
- What does the signal look like before and after this step?

## Pipe Semantics And Flow Modes

Not all pipes should look or behave the same.

The visual language should make it clear how data moves. A visitor should be
able to tell whether a pipe represents a scheduled job, a continuous stream, an
incremental load, a backfill, a manual correction, or a downstream export.

Possible pipe types:

- Continuous streaming pipe: steady motion, small frequent packets, no visible
  gaps, used when signals arrive as they happen.
- Incremental processing pipe: packets move in ordered chunks, with visible
  watermarks or checkpoints showing what has already been processed.
- Scheduled batch pipe: data moves in larger bursts, with a clock, calendar,
  or pulse that makes the schedule visible.
- Full refresh pipe: a larger wave replaces or rebuilds the previous state.
- Backfill or replay pipe: a repair crew sends historical packets through a
  marked maintenance route.
- Manual correction pipe: slower, guarded, clearly marked as human-reviewed.
- Data quality gate: a valve, filter, or inspection station where bad packets
  can be stopped, flagged, or routed for follow-up.
- Serving or export pipe: a pipe leaving the house with an explicit destination
  and ownership marker.

Each pipe should answer:

- What starts this flow?
- Does it run continuously, incrementally, or on a schedule?
- How fresh is the data expected to be?
- What tells us that the flow is healthy?
- What happens when it fails?
- Who owns the flow and who uses the output?

The same signal journey may pass through several pipe types. For example, an
application click may start as a continuous event stream, become an incremental
modeled table, and later feed a scheduled dashboard or export.

## Characters And Real Team Work

The characters should be a major part of the experience.

The goal is that a visitor can meet people in the house and understand both:

- Who on the team has worked on this part of the platform.
- What real platform work, data flow, model, dashboard, export, automation,
  infrastructure, or support responsibility that person can explain.

Characters should feel connected to real people, not generic mascots. The
ambition is that they resemble teammates in look, speech, knowledge, and
behavior, while staying respectful and approved for the way the page may be
shared.

Possible character design principles:

- Each character has a name, room, responsibility, Markdown knowledge file, and
  dialogue style.
- Each character is connected to one or more real artifacts, such as Git
  commits, pull requests, documentation, dashboards, data products, jobs,
  configuration files, or notebooks.
- Character dialogue should explain real work in plain language.
- The visitor should be able to ask a character what they are doing, what they
  built, what they own, and who to talk to next.
- Character answers should be genuinely educational: the person should explain
  the room they are in, the technology and pipelines around them, how the flow
  works, and how someone can build or use the platform well.
- Character answers can include public GitHub repository context when it helps:
  what the repository demonstrates, what to inspect first, and how it connects
  to the current room or pipe.
- Characters can guide visitors across rooms when a signal moves from one
  ownership area to another.
- The scene should make collaboration visible. For example, two people working
  together on data models should appear together in the modeling room, connected
  to the relevant model flow.

First characters:

- Isak: main data platform guide and the primary person visitors should ask
  about data platform questions.
- Malo: architect character, helping explain platform shape, operating model,
  and design tradeoffs.
- Param: early team character, to be grounded in real artifacts before the
  exact room and dialogue are finalized.
- Kien: early team character, to be grounded in real artifacts before the exact
  room and dialogue are finalized.

Later character expansion:

- Add the rest of Data Insights.
- Add key collaborators around Vipps MobilePay where they have worked with Data
  Insights or the data platform.
- Prefer adding people when there is a real artifact, process, or platform
  responsibility they can explain.

Possible ways to ground characters in reality:

- Use Git history to identify who has contributed most to a component.
- Use documentation ownership and code ownership to connect people to rooms.
- Use recent commits to surface what people have actually worked on lately.
- Use public repositories on Isak's GitHub account to ground explanations in
  concrete examples and demos.
- Use manually approved notes from the team to avoid guessing.
- Use explicitly approved reference images if recognizable likenesses are wanted.
- Use one Markdown knowledge file per character so the dialogue has a
  reviewable source of truth.

Privacy and consent boundaries:

- Do not store, publish, or commit Slack profile photos or private source images
  unless they have been explicitly approved for this page.
- Do not publish recognizable likenesses, speech imitation, or behavior
  imitation for a teammate without that person's approval.
- If approved images and approval for likeness are not available, use stylized
  avatars with coarse, respectful cues rather than recognizable likenesses.
- Character dialogue should not expose private context, sensitive internal
  details, or unsupported claims about what someone owns.
- If the page becomes shareable beyond the immediate team, every real-person
  character should have a clear approval path.

## Example Signal Journeys

These are candidate journeys. We should choose one first instead of trying to
explain everything at once.

### Application Button Click

A person taps a button in an application. The click becomes an event. The event
is captured, landed, validated, modeled, and eventually used to understand
behavior, product quality, or business impact.

### Payment Event

A person taps to pay or sends money to another person. The application emits a
conceptual payment event. The platform captures the event, lands it in a storage
account, processes it with Databricks and Spark-style jobs, models it with
dbt-style transformations, and serves safe, governed outputs through analytics
projects, declared data exports, or data products.

This journey must never show real payment data or real user data.

### Temperature Reading

A sensor emits a temperature reading. The reading flows through capture,
storage, validation, enrichment, quality checks, and serving. It may become an
alert, dashboard, model input, or operational decision.

### Operational Export

A source system exports rows on a schedule. The platform receives the files,
checks contracts, publishes tables, grants access, and serves the data to
analytics projects or downstream systems.

### Storage Account To Database

Data lands in a storage account. The platform picks it up, validates the shape,
applies the right processing pattern, and writes it into a database or table
where it can be queried, modeled, exported, or used by another system.

## Stepping Into The Process

The house should support two modes:

- Follow mode: the visitor watches one signal move through the whole flow.
- Step-in mode: the visitor enters a room, talks to the people there, and learns
  that stage in more detail.

Potential rooms:

- Source room: where the signal emerges.
- Capture room: where the signal becomes data the platform can receive.
- Contract room: where meaning, ownership, freshness, and sensitivity are
  described.
- Landing room: where raw data arrives.
- Validation room: where format, schema, and quality expectations are checked.
- Processing room: where the signal is transformed or enriched.
- Governance room: where access, lineage, ownership, and retention are visible.
- Modeling room: where data becomes reusable models or data products.
- Serving room: where dashboards, exports, alerts, or downstream systems use the
  result.
- Support room: where users learn who to ask when something is unclear or broken.

## Possible Source Inspiration

The automation should prefer Isak's personal repositories for inspiration and
Git contribution signals. It should avoid treating internal production
repositories as source material unless they are explicitly added later.

Starting source candidates:

- `https://github.com/isakrs`
- `/Users/isakrathestoere/Code/isakrs/modern-data-platform-example`
- `/Users/isakrathestoere/Code/vipps-isakrs`
- `/Users/isakrathestoere/Code/isakrs-personal`

Possible ideas from that repository to consider:

- Producer-owned data contracts.
- Platform validation and governance.
- Purpose-based access for analytics projects.
- Declared exports for downstream systems.
- Configuration as the interface between product teams, platform teams, and
  analytics teams.

These should be treated as inspiration, not automatic requirements.

Repository source rules:

- Prefer public repositories from Isak's GitHub account for external-facing
  dialogue.
- Local personal repository checkouts can be used for richer context, but do not
  publish private or sensitive details discovered locally.
- When a repository becomes part of a character conversation, explain the idea it
  demonstrates instead of dumping raw commit history.
- Link to public repositories when that helps visitors continue learning outside
  the house.

## Consulting And Showcase Value

The experience should eventually work in three situations:

1. A North by North-style company event where the team can role play the data
   flow live while the Three.js house runs in the background.
2. A self-guided internal or external explanation where someone can explore the
   house and understand the core concepts without a presenter.
3. A future consulting or portfolio setting where the experience shows platform
   thinking, storytelling, technical depth, and interactive craft.

For a consulting-style version, the exact company details can become fictional
or customer-specific while the core pattern remains the same: signals enter the
platform, become trustworthy, become useful, and are owned by real people and
processes.

## Automation Idea

We want an automation that runs on workdays around noon and improves this work
without waiting for manual approval every time.

Responsibilities:

- Look at new Git contributions in Isak's personal repositories.
- Look at public GitHub repositories on Isak's account when they can become
  useful character dialogue, room artifacts, or consulting showcase examples.
- Notice changes that reveal platform concepts, ownership, services, or new
  data flows.
- Improve the written explainer when it can make the flow or process easier
  to understand.
- Preserve the eventual interactive house direction while keeping the written
  explainer useful on its own.
- Notice concrete signal journeys that could become example flows.
- Notice whether flows are scheduled, continuous, incremental, full refreshes,
  backfills, manual corrections, or exports.
- Notice real team contributions that could become character dialogue or room
  ownership notes.
- Notice personal GitHub repositories that could help characters explain data
  platform ideas with practical examples.
- Update this brief, a storyboard, or the eventual interactive page directly
  when there is a useful improvement.
- Eventually extend the Three.js house with new rooms, pipes, characters,
  effects, or dialogue.
- Commit and push every automatic change so the project can be rolled back
  through Git history.
- Avoid publishing private details, private images, or unsupported real-person
  claims.

The automation should not only add more material. It should make the experience
better in at least one visible way.

Examples of "better":

- A visitor can follow the signal journey more clearly than before.
- A pipe type becomes easier to distinguish from other pipe types.
- A character gains a better grounded explanation with a reviewable artifact.
- A room explains one mandatory concept more clearly.
- The experience moves closer to being playable, visually polished, or useful
  during a live event.
- The page becomes easier to understand without exposing sensitive details.

Examples of "only more":

- Adding another room that does not clarify the journey.
- Adding another character without a real reason for that character to exist.
- Adding decorative objects that do not support the data flow story.
- Copying raw contribution history without turning it into useful explanation.

## Answered So Far

1. Main audience:
   external people and people inside Vipps MobilePay. A concrete target use case
   is showing it at a company event such as North by North. A later consulting
   or portfolio audience is also valuable.

2. First real deliverable:
   a polished, playful Three.js experience that people can explore by
   themselves and that can also run in the background while the team explains
   the data flow live.

3. Performance style:
   the experience should support role play, Dino and Wraptor dinosaur costumes,
   smoke-machine energy, and a playful live explanation style.

4. Concrete movement to show:
   when data moves from a storage account to a database, that movement should be
   visible in the three-dimensional scene.

5. Interaction model:
   a small game where people move around, inspect things, enter rooms, and talk
   to humans.

6. Character conversations:
   characters should have Markdown knowledge files and eventually be backed by
   large language models so visitors can ask real-time questions.

7. Automation source material:
   the automation should use Isak's personal repositories for inspiration and
   Git contribution signals.

8. Automation behavior:
   the automation should update automatically, commit, and push so every change
   can be rolled back.

9. Character resemblance:
   characters should resemble real teammates in look, speech, knowledge, and
   behavior, subject to explicit approval and privacy boundaries.

10. First characters:
    Isak, Param, Kien, and Malo, with Isak as the most important character and
    Malo as an architect.

11. First platform concepts:
    ingestion processes, analytics projects, data export, and data products.

12. Architecture style:
    partly real Vipps MobilePay platform, partly metaphorical, and reusable for
    customer-style examples when useful.

13. Character teaching scope:
    characters should explain the room, the technology, the pipelines they own
    or have worked on, and how to build a great data platform.

14. Visual style:
    realistic house, realistic materials, realistic team-inspired characters
    where approved, visible pipes, virtual smoke, and event-ready polish.

15. Search indexing:
    the page should stay public by direct link, but should not be available
    through Google or other search engines yet.

16. Sharing polish:
    fairly high polish before actively sharing, while still being acceptable if
    someone finds the address by digging.

17. GitHub repository conversations:
    characters can also talk about public GitHub repositories on Isak's account,
    especially when a repository demonstrates a data platform concept, a room,
    a pipe, or a consulting showcase idea.

18. First playable journey:
    a payment event, such as tapping to pay or sending money to a person.

19. First public repositories:
    `modern-data-platform-example` and `vipps-isakrs` should be represented
    first. Older sensor-event repositories can be used later as contrast
    examples.

20. Real artifacts:
    "real artifacts" means concrete sources such as public repositories,
    documentation, workflows, files, dashboards, models, notebooks, jobs, or
    Markdown knowledge files. Use public-safe artifacts first.

21. Character approval assumption:
    proceed as if the first teammate-inspired characters are approved for now,
    with the understanding that they can be removed, anonymized, or changed if
    someone does not approve after seeing it.

22. Large language model safety:
    use judgement, keep answers public-safe by default, and do not expose real
    Vipps MobilePay data, real user data, secrets, or sensitive internal
    details.

23. Named technologies:
    Databricks, dbt, GitHub Actions, Spark, storage account, Azure Storage
    Account, and S3 can be named when useful.

24. Minimum playable scope:
    the work can move into Three.js when one concept is explained or when the
    contours of the page show that it is moving in the right direction.

## Remaining Clarifying Questions

1. Should the first repository links open in the same tab or as an explicit
   "learn more" action from the GitHub room?

2. Which character should explain dbt modeling first: Param, Kien, or both
   together?

## Suggested Next Step

Make the Three.js scene explain the payment event journey more clearly by
connecting visible pipe motion, room labels, and character dialogue to the same
tap-or-send story.
