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
- The world now includes a visible five-step payment journey tracker and
  explicit product-team source and consumer endpoints so the send-and-receive
  loop reads more clearly on first view.
- Each journey handoff now shows its active flow mode directly in the world, so
  visitors can see when the path is streaming, incremental, quality-gated,
  declared export, or serving flow without relying only on the legend.
- The world now supports zooming in and out, both from the camera buttons and
  from mouse-wheel input on the canvas.
- The world now teaches its own movement controls in the panel, including drag,
  orbit, depth movement, zoom shortcuts, journey hotkeys, and a quick reset
  back to the full-house view.
- The payment journey tracker now acts as a guided tour with step-specific
  camera moves, previous and next controls, autoplay, and scene-cue notes that
  explain what to inspect in the house.
- The active guided step now brightens its room, matching pipes, service boxes,
  and source or consumer terminal, so the story is easier to follow from inside
  the world.
- Each payment journey handoff now names the concrete public-safe services and
  trusted destinations that fit that step, so the tour explains not only where
  the signal moves but also which platform offerings belong there.
- Side-mode props now make scheduled batch, backfill or replay, and manual
  correction visible in the scene, so the pipe language goes beyond the main
  payment path without crowding the house.
- Direct Publish now has a separate reviewed full refresh cue in the world, so
  visitors can tell the difference between a deliberate rebuild and a replay
  lane for historical reprocessing.
- Each teammate-inspired character now has a public-safe review page with
  direct links from the world, while the Markdown files remain the source
  material for future large language model conversations.
- The decorative repository table, open asset workbench, and smoke effects have
  been removed so the house and core signal journey are easier to read.
- The configuration repository offerings now appear as plain clickable service
  boxes in the world as well as in the Services panel, so visitors can inspect
  safe purpose and category without extra scene clutter.
- Dataverse and Datafront now appear as visible product-side service-name
  boxes, so the serving flow lands on concrete named destinations instead of
  ending as an abstract label.
- Trusted product destinations now use the same plain box language as the rest
  of the service catalog, keeping the scene focused on names rather than custom
  destination props.
- Service clicks now teach house area, likely users, flow mode, output shape,
  and nearest destinations, so the configuration catalog explains when each
  offering fits without exposing private configuration details.

This file should serve two purposes:

- A useful written explainer that helps people understand how data flows and how
  the platform process works.
- A planning brief and storyboard for the Three.js experience.

The first real deliverable should be the Three.js experience. The written page
should support it by making the story, flow, characters, and process clear
before the scene becomes too complex.

[Enter the Three.js world](/data-platform-example/)

## Character Knowledge Pages

The Markdown files under `/data-platform-example/characters/` remain the source
material for future large language model conversations. Public-safe review pages
now sit beside them so visitors can inspect what each character is meant to
teach without reading repository source files directly.

- [Isak notes](/data-platform-example/characters/isak/)
- [Param notes](/data-platform-example/characters/param/)
- [Kien notes](/data-platform-example/characters/kien/)
- [Malo notes](/data-platform-example/characters/malo/)

These pages should stay `noindex` until Isak explicitly wants the whole
experience to become search-discoverable.

## Feedback Loop

Most feedback should happen through agent conversations. Tell an agent what
confused you, what should become more playable, which character should know
something, or which part of the data flow deserves a better scene. The agent can
turn clear input into instruction changes, backlog changes, character knowledge,
or implementation work.

Every automation run should begin by reviewing the most recent relevant chat
input that was passed into the run and improving the written descriptions first
when that input makes the story clearer. This means recent chat feedback should
not only affect code or backlog cards. It should also sharpen the wording of
the instructions page so the next automation run starts from a better source of
truth.

Priority order for startup inputs:

1. The most recent relevant user and agent chat input passed into the active
   run.
2. This instructions page as the current source of truth after those chat-driven
   refinements are applied.
3. Saved public GitHub feedback issues when the feedback should persist beyond a
   single conversation or be shared with others.

Use the GitHub feedback form when the input should be saved outside the
conversation, shared with others, or tracked by the workday automation. A person
can fill it in directly, and an agent can also use it as the durable public
record when a conversation produces useful public-safe feedback.

When feedback goes into GitHub, prefer structured context over long free-form
notes. The durable record should make it easy for a later agent to see:

- Which public route the feedback is about.
- Which house area, service zone, or character area it belongs to.
- Which payment journey step is closest.
- Which flow mode is involved, if any.
- Which safe repository, artifact, or source link grounds the suggestion.

That structure matters because future runs should be able to turn saved feedback
directly into backlog changes, clearer wording, repository conversation ideas,
or scene work without needing to rediscover where the confusion came from.

## Visual Direction And Reuse

The world should not become a generic three-dimensional asset showroom. It
should look like a focused data platform house with recognizable platform
services, readable flow paths, and a few strong visual landmarks.

Reuse is still welcome, but only when it supports the specific service story:

- Reuse movement patterns, loaders, postprocessing, camera techniques, and
  house-scale interaction patterns when they help the game feel better.
- Aim for the feeling of an elegant technical reveal when that helps the
  platform become understandable from the inside, not only from the outside.
- Prefer service-shaped props and icons over random decorative shelves, crates,
  or library fillers.
- Remove or avoid elements that make the world feel crowded without teaching
  anything.
- The borrowed keyframes house is the actual data platform house, not a scene
  around a separate decorative object.
- Pipes should visibly enter, cross, and leave the house through meaningful
  service ports.
- Keep a procedural fallback for important external assets so the page does not
  break if a model cannot load.
- Use assets only when their license is compatible with public sharing, and
  keep attribution notes when required or useful.

Preferred reuse focus:

<div class="data-platform-source-grid" aria-label="Preferred reuse directions">
  <article class="data-platform-source">
    <strong><a href="https://threejs.org/examples/">Three.js examples</a></strong>
    <span>Use for movement, camera behavior, loaders, animation patterns, and scene techniques.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://github.com/pmndrs/three-stdlib">three-stdlib</a></strong>
    <span>Use for helper patterns that make the world more playable without changing the static-site architecture.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://polyhaven.com/">Poly Haven</a></strong>
    <span>Use for high-quality materials and lighting when they support a more believable technical environment.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://ambientcg.com/">ambientCG</a></strong>
    <span>Use for surface materials when a room needs more realism without adding clutter.</span>
  </article>
  <article class="data-platform-source">
    <strong><a href="https://github.com/KhronosGroup/glTF-Sample-Assets">Khronos glTF Sample Assets</a></strong>
    <span>Use for glTF loading and animation reference, not as a visible theme for the house.</span>
  </article>
</div>

Do not treat generic game-kit shelves, generic low-poly characters, or random
open asset collections as first-class content in the public experience unless
they directly support a real platform service, room, or character.

## Visual Language For Services

The visual language should center on recognizable data platform services and
their nearest public-safe metaphors. When possible, a visitor should understand
what a room is about before reading the label.

The visual tone can borrow from polished product-engineering films where the
camera moves around an object with precision and craft and sometimes reveals the
inside. The same idea works here: the visitor should be able to move around the
data platform with that same feeling, inspect layers when useful, and
understand how the parts fit together.

Preferred icon and prop direction:

- Storage account or Azure Storage Account: storage tanks, object buckets,
  landing bays, or blob-container walls.
- SQL server or database hotel style: stacked server racks, database hotel
  towers, or glowing table floors.
- Databricks: compute clusters, notebook workbenches, spark-chamber machinery,
  or job-run control walls.
- dbt: transformation workshop, model graph wall, or structured build station
  with lineage boards.
- Azure Event Hubs or event streaming: event hub rings, intake turbines, or
  fast streaming corridors.
- Dataverse: governed delivery or consumer-access space with clear ownership,
  access, and contract cues.
- Datafront: presentation or front-door serving space where trusted outputs are
  presented to consumers.
- Dino and Wraptor: actual dinosaur-like characters or mascots, not abstract
  labels. They can still stay stylized and public-safe.

Avoid spending attention on props that do not explain services. A correct
service-shaped object is more valuable than ten decorative objects.

## Configuration Repository Offerings

The Three.js world should show every documented service offering from the
configuration repository as public-safe service names, categories, and conceptual
descriptions. The world should not expose raw configuration payloads, access
groups, personal contact details, internal endpoints, private table names, or
sensitive implementation details.

<div class="data-platform-source-grid" aria-label="Configuration repository service offerings">
  <article class="data-platform-source">
    <strong>Analytics Projects</strong>
    <span>Governed access for product teams and analysts who need trusted published datasets back from the platform for decisions, analysis, and follow-up.</span>
  </article>
  <article class="data-platform-source">
    <strong>Data Export</strong>
    <span>Approved delivery back to product teams or other consumers from Databricks with a clear owner, trigger path, and destination.</span>
  </article>
  <article class="data-platform-source">
    <strong>Data Products</strong>
    <span>Curated outputs delivered back to product teams through governed data products with storage, schema, identities, and sharing paths.</span>
  </article>
  <article class="data-platform-source">
    <strong>Dino</strong>
    <span>Capture events directly from Feed application programming interface endpoints into object storage.</span>
  </article>
  <article class="data-platform-source">
    <strong>Object Storage Connection</strong>
    <span>Connect producer-owned object storage to the data platform in a governed way.</span>
  </article>
  <article class="data-platform-source">
    <strong>Direct Publish</strong>
    <span>Publish Databricks tables directly from files that already live in storage, either incrementally or as a reviewed full refresh.</span>
  </article>
  <article class="data-platform-source">
    <strong>Wraptor</strong>
    <span>Publish streaming event data from file sources captured by Dino.</span>
  </article>
  <article class="data-platform-source">
    <strong>Cacheloader</strong>
    <span>Stream and transform event data from object storage into useful published datasets.</span>
  </article>
  <article class="data-platform-source">
    <strong>Skippy</strong>
    <span>Copy small slow-changing tables from SQL databases on a nightly schedule.</span>
  </article>
  <article class="data-platform-source">
    <strong>Query Publish</strong>
    <span>Create SQL views on top of existing tables when the right output is a curated view.</span>
  </article>
  <article class="data-platform-source">
    <strong>Custom Integrations</strong>
    <span>Represent special integration jobs when the standard service paths do not fit.</span>
  </article>
</div>

<h3 id="trusted-consumer-destinations">Trusted Consumer Destinations</h3>

Dataverse and Datafront should stay visible on the product side of the journey,
but they do not need their own prop language. Plain service-name boxes are the
preferred treatment because the important thing is the destination name and role
in the loop, not a custom landmark sculpture.

- Dataverse is the governed consumer space where people explore trusted outputs,
  combine them with context, and work with them safely.
- Datafront is the trusted serving front door where approved outputs are
  presented clearly to product teams and analytics consumers.

When the serving flow is in focus, a visitor should be able to see that the
product-side path can land in both of these named boxes before continuing back
to product teams.

In the Three.js world, these offerings should use the same plain clickable box
treatment as the rest of the catalog. The current product-side world should let
visitors click the Dataverse and Datafront boxes directly, or use the Product
panel links, to open public-safe teaching notes about what each destination is
for, who uses it, and why it sits on the serving side of the loop. The service
directory remains the first pass for the configuration catalog: it names every
offering and connects the catalog back to the house with its own pipe.

The product-side scene should make the return path legible with placement and
pipe connections, not with custom props:

- Dataverse should be a clearly named governed destination box.
- Datafront should be a clearly named serving destination box.
- The serving path should visually land beside both names before continuing
  toward product teams.

The payment journey should also stay readable as a sequence, not only as a map.
A first-time visitor should quickly understand this order:

1. A product team sends a conceptual payment signal into the platform.
2. Ingestion lands the signal in a storage account such as Azure Storage
   Account or S3.
3. Checkpoints, quality gates, Spark-style processing, and dbt-style modeling
   turn the signal into trusted meaning.
4. Declared exports leave only through an explicit governed path.
5. Product teams receive trusted outputs back through analytics projects, data
   products, or other approved consumers.

That sequence should teach flow mode at the same time as order. When a visitor
focuses a handoff, the scene and panel should make it obvious which of these
apply there:

- Streaming at the source intake.
- Streaming plus incremental checkpointing at landing and storage movement.
- Incremental plus quality gate behavior through processing and modeling.
- Declared export at governed outbound delivery.
- Serving flow at trusted consumer and data product delivery.
- Scheduled batch, replay, and manual correction as visible side modes beside
  the primary payment path where they matter.

The current world also needs to tie that sequence back to the service catalog.
When a visitor focuses a payment handoff, the panel should show which service
names or trusted destinations fit that moment in the story, so the flow reads
as both a movement path and a configuration choice:

- Source intake should point to Dino and Object Storage Connection.
- Storage landing should keep Dino and Object Storage Connection visible and
  introduce Wraptor as the first continued publish path.
- Modeling should surface Cacheloader, Direct Publish, Skippy, and Query
  Publish as distinct ways trusted tables can take shape.
- Export should point to Data Export first, with Custom Integrations as the
  reviewed exception path.
- Product return should surface Analytics Projects, Data Products, Dataverse,
  and Datafront as the trusted outputs side of the loop.

The most important next focus is not "all services equally." The brief should
guide future runs toward the services that matter most for the story:

- Configuration services are the main focus area.
- Dataverse should stay a clear named box that people can move to or inspect.
- Datafront should stay a clear named box that people can move to or inspect.
- It should be obvious that product teams both send data into the platform and
  receive governed outputs back from the platform.
- The visitor should understand when to approach or click a service to learn
  what it does, when to use it, and what kind of output or responsibility it
  represents.

Do not let the scene become a crowded board of equally loud service names. Use
grouping, distance, depth, and room ownership so the most important services
stand out first.

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
      <strong>Make movement feel room-first</strong>
      <span>Build on the now-visible controls so movement feels grounded in rooms, landmarks, and pipe destinations instead of only camera target shifts.</span>
    </article>
    <article class="data-platform-card">
      <strong>Declutter the world</strong>
      <span>Keep trimming labels, props, and decorative effects until the house, pipes, and service boxes read clearly on first view.</span>
    </article>
    <article class="data-platform-card">
      <strong>Focus on configuration services</strong>
      <span>Keep configuration services as the primary explorable service family, with Dataverse and Datafront anchored clearly on the product side.</span>
    </article>
    <article class="data-platform-card">
      <strong>Simplify service presentation</strong>
      <span>Keep configuration services as clean name boxes first, then add only the minimum visual cues needed to separate categories.</span>
    </article>
    <article class="data-platform-card">
      <strong>Explain payment event journey</strong>
      <span>Deepen the now-visible sequence so the scene itself teaches each handoff, not only the side panel.</span>
    </article>
    <article class="data-platform-card">
      <strong>Make handoff props match flow modes</strong>
      <span>Now that the tracker names each mode, make room props and pipes reinforce the same mode visually.</span>
    </article>
    <article class="data-platform-card">
      <strong>Show the product-team loop</strong>
      <span>Build on the new source and consumer terminals so the send-and-receive loop stays obvious from multiple camera angles.</span>
    </article>
  </section>

  <section class="data-platform-lane" aria-labelledby="backlog-next">
    <h3 id="backlog-next">Next</h3>
    <article class="data-platform-card">
      <strong>Ground characters in service areas</strong>
      <span>Place Isak, Param, Kien, and Malo near the service families and decisions they should actually explain.</span>
    </article>
    <article class="data-platform-card">
      <strong>Animate storage to database</strong>
      <span>Show data leaving storage, being checked, and becoming queryable in a way that feels spatially connected rather than diagrammatic.</span>
    </article>
    <article class="data-platform-card">
      <strong>Make journey steps drive the camera</strong>
      <span>Build on the new guided camera tour with stronger in-scene highlights, mode-specific props, and fewer places where visitors can lose the handoff.</span>
    </article>
    <article class="data-platform-card">
      <strong>Turn room highlights into movement anchors</strong>
      <span>Build on the new active room and pipe highlights so visitors feel invited to move from landmark to landmark instead of hovering outside the story.</span>
    </article>
    <article class="data-platform-card">
      <strong>Let service guidance shape the scene</strong>
      <span>Now that each journey step names relevant services, add stronger room props and highlights so those service choices feel spatial instead of panel-only.</span>
    </article>
    <article class="data-platform-card">
      <strong>Broaden knowledge-backed dialogue</strong>
      <span>Let characters answer room-specific prompts, safe repository questions, and pipe-mode questions from their Markdown source files.</span>
    </article>
    <article class="data-platform-card">
      <strong>Deepen character review pages</strong>
      <span>Expand the new public-safe character pages with more room cues, public repository teaching, and future conversation prompts.</span>
    </article>
    <article class="data-platform-card">
      <strong>Let product destinations teach the return path visually</strong>
      <span>Build stronger focus reactions, arrival cues, or path highlights while keeping Dataverse and Datafront as plain service-name boxes.</span>
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
    <article class="data-platform-card">
      <strong>Saved feedback quality</strong>
      <span>Does the GitHub issue clearly name route, room, payment step, flow mode, and safe repository context?</span>
    </article>
  </section>

  <section class="data-platform-lane" aria-labelledby="backlog-done">
    <h3 id="backlog-done">Done</h3>
    <article class="data-platform-card">
      <strong>Make guided focus visible in the scene</strong>
      <span>Journey steps now brighten the matching room, pipe family, service boxes, and product source or consumer terminal, so the world teaches the handoff more directly.</span>
    </article>
    <article class="data-platform-card">
      <strong>Direction reset</strong>
      <span>The old implementation was removed and this brief became the source of truth.</span>
    </article>
    <article class="data-platform-card">
      <strong>Expose movement controls</strong>
      <span>The world now tells visitors how to drag, orbit, move in depth, jump between journey steps, zoom, and reset the camera.</span>
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
      <strong>Teach services on interaction</strong>
      <span>Service clicks now explain room ownership, likely users, flow mode, output shape, and nearest destinations while staying public-safe.</span>
    </article>
    <article class="data-platform-card">
      <strong>House made central</strong>
      <span>The borrowed keyframes house now acts as the actual data platform house, with pipes routed into and out of house ports.</span>
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
      <strong>Clickable trusted destinations</strong>
      <span>Dataverse and Datafront now open product-side public-safe teaching notes from both the world props and the Product panel.</span>
    </article>
    <article class="data-platform-card">
      <strong>Trusted destinations simplified to boxes</strong>
      <span>Dataverse and Datafront now use the same plain service-box treatment as the rest of the catalog, with differentiation handled by name, copy, and pipe placement.</span>
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
      <strong>Character notes published</strong>
      <span>Each teammate-inspired character now has a direct-link review page with noindex protection and links from the world dialogue.</span>
    </article>
    <article class="data-platform-card">
      <strong>Agent-first feedback loop</strong>
      <span>Feedback normally starts in agent conversations and is saved in GitHub only when it needs a durable public record.</span>
    </article>
    <article class="data-platform-card">
      <strong>Structured GitHub feedback form</strong>
      <span>The durable public form now asks for route, house area, payment step, flow mode, and repository context so future runs can triage input faster.</span>
    </article>
    <article class="data-platform-card">
      <strong>Configuration repository service directory</strong>
      <span>The world now names every documented configuration repository offering on a visible service board and Services focus list.</span>
    </article>
    <article class="data-platform-card">
      <strong>Zoom controls added</strong>
      <span>Visitors can now zoom in and out with camera buttons and mouse-wheel input on the main world canvas.</span>
    </article>
    <article class="data-platform-card">
      <strong>Scene declutter pass</strong>
      <span>The decorative repository table, asset workbench, and smoke were removed so the house and pipes stay easier to scan.</span>
    </article>
    <article class="data-platform-card">
      <strong>Full refresh separated from replay</strong>
      <span>Direct Publish now points to a reviewed full refresh cue in the scene, separate from the replay lane used for historical reprocessing.</span>
    </article>
    <article class="data-platform-card">
      <strong>Service boxes in the world</strong>
      <span>Visitors can now click each configuration repository offering as a plain box in the scene or Services panel to get a public-safe explanation.</span>
    </article>
    <article class="data-platform-card">
      <strong>Visible journey tracker and loop terminals</strong>
      <span>The world now shows a five-step payment journey in the panel and explicit product-team source and consumer endpoints around the house.</span>
    </article>
    <article class="data-platform-card">
      <strong>Journey steps now teach flow modes</strong>
      <span>Each payment handoff now names the active mode and updates the current handoff panel when visitors focus it.</span>
    </article>
    <article class="data-platform-card">
      <strong>Journey steps now drive a guided camera tour</strong>
      <span>The payment tracker now offers previous and next controls, autoplay, step-specific camera moves, and scene cues that tell visitors what to inspect.</span>
    </article>
    <article class="data-platform-card">
      <strong>Journey steps now name relevant services</strong>
      <span>Each payment handoff now points to the service offerings or trusted destinations that fit that step, so the tour connects movement to platform choices.</span>
    </article>
    <article class="data-platform-card">
      <strong>Trusted product destinations added</strong>
      <span>Dataverse and Datafront now stand as visible serving destinations so the product side of the loop has concrete endpoints.</span>
    </article>
    <article class="data-platform-card">
      <strong>Side-mode props added</strong>
      <span>The world now shows a night-batch clock, replay lane, and manual correction console so more pipe modes are visible in-scene.</span>
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
- A small game where visitors can move around the house in real depth, inspect
  rooms and pipes, and talk to people.
- The Data Platform House is the first part of a larger Vipps tech world, not
  the final boundary of the concept.
- Something that can also run in the background during an event while the team
  explains the data flow.
- Something that can later be used as a memorable selling point when explaining
  data platform work to new customers or collaborators.
- The written page remains useful as the explanatory backing and storyboard.
- The first visual priority is correct service description and clear service
  identity, not decoration density.
- The story should clearly show a two-way relationship with product teams:
  product teams provide signals to the platform and receive governed outputs
  back from it.

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

- Configuration services.
- The producer-consumer loop between product teams and the data platform.
- Ingestion processes.
- Analytics projects.
- Data export.
- Data products.

Most important named service focus:

- Dataverse.
- Datafront.
- Dino.
- Wraptor.

First signal journey:

- A payment event, such as tapping to pay or sending money to a person.
- The public story should stay conceptual and must not expose real Vipps
  MobilePay payment data or real user data.
- The first path should show the event becoming a platform signal, landing in a
  storage account, moving through Databricks and Spark-style processing, being
  modeled with dbt-style transformations, and then becoming useful as a data
  product, analytics project, or declared data export.
- The same path should make it obvious that the signal originates in a product
  team context and that trusted outputs are later delivered back to product
  teams through services such as Dataverse, Datafront, analytics projects,
  exports, or data products.

Technologies that can be named:

- Databricks.
- dbt.
- GitHub Actions.
- Spark.
- Storage account, with Azure Storage Account or S3 as concrete examples.
- Azure Event Hubs.
- SQL servers and database hotel style metaphors where they make the storage and
  serving layers easier to understand.
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
- The long-term shape should feel closer to a Game of Thrones-style intro world
  or animated tech map, where the Data Platform House is the first major place
  in a broader Vipps technology landscape.
- The eventual world can become globe-like or map-like, almost like Google
  Earth for Vipps technology, where visitors can move around and inspect how
  technologies and service areas are stitched together across the landscape.
- At the same time, the visitor should sometimes feel as if the map has opened
  up into an inspectable engineering view, where the inside of the system is
  visible and navigable when useful.
- The world should eventually let a visitor look across the map and spot things
  like Azure Event Hubs in one area, storage accounts in another, Spark lifting
  and shaping data elsewhere, and named services such as Dino and Wraptor as
  visible parts of the same technical system.
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

- The automation should improve the written descriptions from recent relevant
  chat input every time it starts, not only make implementation changes.
- The automation should treat the active thread's recent chat input as the first
  input queue for wording corrections, concept clarifications, and direction
  changes.
- The automation should inspect Isak's personal repositories for inspiration and
  Git contributions.
- The automation may update the public page automatically.
- The automation must commit and push changes so every automatic change can be
  rolled back through Git history.

## Starting Vision

We want to explain a data platform through an explorable house metaphor, but the
main experience should be following a concrete data signal through the whole
system.

The larger product vision is broader than one house. Think of the experience as
the beginning of a Vipps tech world, where the Data Platform House is the first
landmark in a bigger explorable map of technical domains.

Over time, this should feel less like one isolated scene and more like an
inspectable technology world model: part map, part globe, part technical
landscape.

It should also support moments where the world opens into an inside view, almost
like a polished product advertisement that reveals how a device is built and
lets the camera travel through the internal layers.

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

- The Data Platform House represents the data platform as the first major
  landmark in the Vipps tech world.
- Over time, the world can expand into other Vipps technology areas in the same
  map-like style, with the house acting as the opening chapter.
- The wider world can eventually be explored almost like Google Earth for Vipps
  technology, where cities, houses, machines, or zones represent the major
  technologies and service families.
- Some scenes can feel like cross sections or opened-up technical views where
  the visitor moves through the inside of the stack, but the broader goal is the
  same crafted feeling while moving around, not a requirement that everything
  must literally explode apart.
- The stitching between places matters as much as the places themselves: the
  visitor should be able to see how Event Hubs, storage accounts, Spark,
  Databricks, dbt, Dino, Wraptor, Dataverse, Datafront, and other services
  connect across the world.
- Product-team spaces sit outside and around the house: they send signals in and
  receive governed outputs back.
- Pipes represent the signal moving in, through, and out of the platform.
- Rooms represent checkpoints in the signal journey.
- Service zones represent the configuration services people can approach to
  learn what each offering does.
- Characters inside rooms represent real people or real roles from the team and
  explain work they have actually done.
- The visitor can follow the signal from room to room or jump directly into a
  stage to understand that part of the flow.
- The interaction should feel like a small exploratory game: move around in
  depth, enter rooms, inspect machinery, follow pipes, and talk to humans.
- Dialogue can borrow the feeling of an old handheld role-playing game, but the
  characters should be smarter than fixed dialogue trees. Each character should
  have a Markdown knowledge file and eventually a large language model-backed
  conversation layer.
- The visual ambition could eventually be a polished Three.js scene with
  animated characters, camera movement, cutaway rooms, and richer materials.
- The scene should stay legible. If a prop does not teach a service, room, flow
  mode, or character responsibility, it is a candidate for removal.

None of this is locked in yet.

## First Playable Journey

The first playable journey is a payment event.

The visitor should be able to follow a payment-related signal, such as a tap or
send action, without seeing real payment data or real user data.

Suggested journey:

1. A person taps or sends a payment.
2. A product team application emits a conceptual payment event into the
   platform.
3. The event is captured by the ingestion process.
4. The event lands in a storage account, such as Azure Storage Account or S3.
5. Databricks and Spark-style processing validate and shape the data.
6. dbt-style models turn the signal into reusable analytical meaning.
7. The platform publishes trusted outputs that product teams can discover and
   use through analytics projects, Dataverse, Datafront, data products, or
   approved exports.
8. A product team receives a governed output back from the platform for product
   understanding, operational follow-up, or downstream use.
9. Ownership and support stay visible on both sides: who produced the signal,
   who shaped it in the platform, and who consumes the result.

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
- Reviewed full refresh: a dedicated rebuild cue marks when a table is
  intentionally rebuilt from storage rather than replayed through a maintenance
  lane.
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

The house is the first target experience.

The written explainer is the foundation, not the final destination. The Three.js
house should grow from the signal journey, pipe semantics, real people, and real
work examples.

The broader ambition is a Vipps tech world with the same kind of memorable
overview feeling as a fantasy or prestige-television intro map: distinct places,
clear landmarks, movement between domains, and a sense that the visitor is
touring a larger technical world. The Data Platform House should be the first
place we build to that standard.

Another useful metaphor is a technical globe or inspectable engineering model.
The visitor should eventually be able to move around the world as if exploring a
living map of Vipps technology, with the same satisfaction as inspecting a
beautifully exposed system drawing or a race-car-style computer-aided design
model where every part has a place and a relationship to the rest.

Another equally important metaphor is the polished product-engineering reveal:
internals become understandable and the camera can travel through the structure
without losing the feeling of craft.

The house should:

- Let visitors follow one signal through the building.
- Let visitors understand that the signal starts in a product team context and
  that trusted outputs return to product teams after platform processing.
- Feel like one named place in a larger tech world, not an isolated demo scene.
- Hint at the wider map beyond the house, so visitors can sense that other
  technology districts exist even before they are fully built.
- Allow cutaway or opened-up moments where visitors can inspect the inside of
  the platform, while keeping that same polished crafted feeling even in normal
  movement around the world.
- Let visitors enter rooms to understand a stage in the process.
- Let visitors move around like a small game, including movement in depth rather
  than only sliding across a flat camera plane.
- Let visitors approach or click service destinations such as Dataverse,
  Datafront, Dino, and Wraptor to learn more.
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
- Use service-shaped iconography so a visitor can visually recognize storage,
  serving, modeling, streaming, and export areas before reading a lot of text.
- Stay visually selective. Remove crowded decorative elements that do not make
  the service story clearer.
- Keep the written explainer available, so the interactive version does not
  become the only way to understand the process.

The house should still be built in small steps. The best path is:

1. Make the written explainer and storyboard useful.
2. Define how the Data Platform House fits into the larger Vipps tech world.
3. Sketch the larger map language: districts, landmarks, globe or map movement,
   and visible stitched-together technologies.
4. Sketch the inside-view language as well: cutaways, reveals, and camera
   movement through internal technical structure.
5. Choose the first signal journey.
6. Identify the first real people, artifacts, and flow modes.
7. Build the first interactive house prototype.
8. Add event-mode visuals and role-play hooks.
9. Let automation help refine the explainer, storyboard, and house.

First prototype scope:

1. A playable Three.js house shell with a few connected rooms.
2. One clear signal journey through ingestion, analytics project work, data
   export, and data product use.
   That journey should explicitly show product teams on both the source side and
   the receiving side.
3. Isak as the main data platform guide.
4. Param, Kien, and Malo as the next visible characters.
5. At least one visible storage-account-to-database pipe.
6. At least three pipe modes with distinct motion, shape, or machinery:
   scheduled batch, incremental processing, and export.
7. Markdown knowledge files for the first characters, even before the live large
   language model integration is built.
8. At least one public GitHub repository from Isak's account represented as a
   blueprint, library item, or workbench artifact.
9. At least one explorable configuration service area that teaches Dataverse,
   Datafront, Dino, or Wraptor correctly.
10. Movement that lets a visitor feel depth and approach an object, not only
    inspect it from a distance.
11. A clear sense that this house is the first landmark in a wider Vipps tech
    world that can grow later.
12. At least one visible hint on the horizon or in the scene language that this
    can expand into a globe-like or map-like technology world.
13. At least one cutaway, reveal, or inside-the-machine moment that shows how a
    technical layer fits into the larger system.

## Time And Change Over Time

Because the automation improves this project twice per workday and every useful
change is committed to Git, the experience can also become a time-aware record
of how the tech world changes.

That is part of the value:

- The world should stay reasonably up to date because it is revised often.
- Git history should make it possible to inspect how the technical landscape has
  changed over time.
- The experience can become a public-safe historical layer, not only a snapshot.
- Future runs can use that history to refine descriptions, preserve important
  changes, and make the visible world feel more like an evolving engineering
  model than a frozen mockup.

## Core Experience Goal

The experience should answer this question:

> What happens to a signal after it is created, and how does it become useful?

It should also answer this related question:

> How do product teams give signals to the platform and get trusted outputs back?

The experience should make the invisible journey visible:

1. A signal emerges in a product team source system.
2. The signal is captured or exported.
3. The producing team describes what the signal means.
4. The platform validates, lands, and processes it.
5. The signal becomes part of governed platform data.
6. Transformations, models, or enrichment make it more useful.
7. Access rules decide who can use it and why.
8. The platform delivers trusted outputs back to product teams and other
   consumers as insights, dashboards, data products, exports, alerts, or
   downstream features.
9. Ownership, monitoring, lineage, and support paths explain who keeps the loop
   trustworthy from producer to platform to consumer.

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
- Reviewed full refresh cue: a dedicated rebuild pad or chamber marks a
  deliberate full-table rebuild, separate from replaying historical packets.
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
