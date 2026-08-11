---
title: Data Platform House Restart Brief
---

<meta name="robots" content="noindex, nofollow, noarchive, noimageindex">

# Data Platform House Restart Brief

## What We Are Keeping

The public address should stay:

https://vipps.isakrs.com/data-platform-example/

We also want some form of automation that helps the project improve over time.
Everything else is open again.

## Current State

The previous implementation has been deleted.

This file is now the only source artifact for the page. It should serve two
purposes:

- A useful blog-like explainer that helps people understand how data flows and
  how the platform process works.
- A planning brief and storyboard for a future interactive version.

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
- The interaction could feel like an old handheld role-playing game: walk up to
  a person, press a button, and get a short dialogue box.
- The visual ambition could eventually be a polished Three.js scene with
  animated characters, camera movement, cutaway rooms, and richer materials.

None of this is locked in yet.

## Blog-Like Explainer Direction

The first useful version can be a readable page rather than a full interactive
scene.

The page should help someone understand:

- Where data starts.
- How it enters the platform.
- What process and ownership expectations exist around it.
- How different flow modes work.
- How the data becomes trustworthy enough to use.
- Where it is used at the end.
- Who to ask when they are confused or something breaks.

The page should read like an approachable walkthrough, not like raw platform
documentation. It can use the house metaphor, but the reader should come away
with a real understanding of the data flow and process.

Possible page structure:

1. Start with one concrete signal.
2. Show the whole journey in a simple flow overview.
3. Walk stage by stage through the process.
4. Use small sidebars for characters and real team work.
5. Use pipe labels to show whether each flow is scheduled, streaming,
   incremental, a backfill, or an export.
6. End with how the signal is used and who owns keeping it healthy.
7. Keep open questions and next-version ideas at the bottom.

This blog-like page should be valuable even before the Three.js version exists.
The future interactive house can be built by turning each section into a room,
pipe, character, or dialogue moment.

## Eventual Interactive House

The house should come eventually.

The blog-like explainer is the foundation, not the final destination. Once the
signal journey, pipe semantics, real people, and real work examples are clear,
the page can grow into an interactive house experience.

The eventual house should:

- Let visitors follow one signal through the building.
- Let visitors enter rooms to understand a stage in the process.
- Show different pipe types through shape, rhythm, labels, and machinery.
- Include characters grounded in real people and real work.
- Let characters explain their part of the platform in short dialogue.
- Keep the written explainer available, so the interactive version does not
  become the only way to understand the process.

The house should not be rushed before the story is clear. The best path is:

1. Make the written explainer useful.
2. Choose the first signal journey.
3. Identify the first real people, artifacts, and flow modes.
4. Turn the explainer into a storyboard.
5. Build the first interactive house prototype.
6. Let automation help refine the explainer, storyboard, and eventually the
   house.

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

Characters should feel connected to real people, not generic mascots.

Possible character design principles:

- Each character has a name, room, responsibility, and short dialogue.
- Each character is connected to one or more real artifacts, such as Git
  commits, pull requests, documentation, dashboards, data products, jobs,
  configuration files, or notebooks.
- Character dialogue should explain real work in plain language.
- The visitor should be able to ask a character what they are doing, what they
  built, what they own, and who to talk to next.
- Characters can guide visitors across rooms when a signal moves from one
  ownership area to another.
- The scene should make collaboration visible. For example, two people working
  together on data models should appear together in the modeling room, connected
  to the relevant model flow.

Possible ways to ground characters in reality:

- Use Git history to identify who has contributed most to a component.
- Use documentation ownership and code ownership to connect people to rooms.
- Use recent commits to surface what people have actually worked on lately.
- Use manually approved notes from the team to avoid guessing.
- Use explicitly approved reference images if recognizable likenesses are wanted.

Privacy and consent boundaries:

- Do not store, publish, or commit Slack profile photos or private source images
  unless they have been explicitly approved for this page.
- If approved images are not available, use stylized avatars with coarse,
  respectful cues rather than recognizable likenesses.
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

### Temperature Reading

A sensor emits a temperature reading. The reading flows through capture,
storage, validation, enrichment, quality checks, and serving. It may become an
alert, dashboard, model input, or operational decision.

### Operational Export

A source system exports rows on a schedule. The platform receives the files,
checks contracts, publishes tables, grants access, and serves the data to
analytics projects or downstream systems.

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

We may want to draw inspiration from existing local repositories, especially
ones that already explain a data platform or data platform operating model.

Candidate source:

- `/Users/isakrathestoere/Code/isakrs/modern-data-platform-example`

Possible ideas from that repository to consider:

- Producer-owned data contracts.
- Platform validation and governance.
- Purpose-based access for analytics projects.
- Declared exports for downstream systems.
- Configuration as the interface between product teams, platform teams, and
  analytics teams.

These should be treated as inspiration, not automatic requirements.

## Automation Idea

We want an automation that runs on workdays around noon.

Possible responsibilities:

- Look at new Git contributions in selected local repositories.
- Notice changes that reveal platform concepts, ownership, services, or new
  data flows.
- Improve the blog-like explainer when it can make the flow or process easier
  to understand.
- Preserve the eventual interactive house direction while keeping the written
  explainer useful on its own.
- Notice concrete signal journeys that could become example flows.
- Notice whether flows are scheduled, continuous, incremental, full refreshes,
  backfills, manual corrections, or exports.
- Notice real team contributions that could become character dialogue or room
  ownership notes.
- Propose updates to this brief, a storyboard, or the eventual interactive page.
- Eventually extend the house with new rooms, pipes, characters, or dialogue.

Open question: should the automation directly change the public page, or should
it create draft suggestions for review first?

## Clarifying Questions

1. Who is the main audience for this experience: the Data Insights team, new
   data platform users, leadership, external visitors, or someone else?

2. Should the first real deliverable be this blog-like explainer page, a
   storyboard, a static presentation, or a small interactive Three.js prototype?

3. Should the experience be more like a guided presentation, a small game where
   you move around, or a hybrid where buttons move the camera between rooms?

4. Which repositories should the automation inspect for inspiration and Git
   contributions?

5. Should the automation update the public page automatically, or should it
   only update this brief and ask for approval before changing the experience?

6. How close should characters look to real team members? Should they be
   stylized team-inspired avatars, recognizable likenesses based only on
   explicitly approved images, or something in between?

7. Which people or roles must exist in the first version, if any?

8. Which real work should the first characters be attached to?

9. What sources are acceptable for connecting people to work: Git history,
   code ownership, documentation ownership, dashboards, team notes, or manual
   approval only?

10. Should character dialogue mention real names and concrete artifacts, or
    should it use real inspiration but keep the wording role-based?

11. Which platform concepts are mandatory to explain first?

12. What should the first blog-like explainer page teach in one sitting?

13. Which signal should be the first complete journey: application click,
   payment event, temperature reading, scheduled export, or something else?

14. Which flow modes must be visible in the first version: scheduled batch,
    continuous streaming, incremental processing, full refresh, backfill, manual
    correction, data quality gate, export, or something else?

15. How should the visitor learn the difference between flow modes: pipe shape,
    animation rhythm, labels, character dialogue, room machinery, or a legend?

16. Should the first journey use real Vipps MobilePay terminology and systems,
    or should it stay fictional and safe?

17. What should count as "used" at the end of the journey: dashboard, data
    product, machine learning model, operational export, alert, decision, or
    application feature?

18. How much technical depth should each step reveal before it becomes too much
    for the intended audience?

19. Should the house mirror the real Vipps MobilePay data platform architecture,
   or should it stay metaphorical and easier to understand?

20. What should a character explain when you talk to them: their current work,
    the room they are in, the pipe they own, or how to get help?

21. Should the visual style aim for realistic materials, playful low-poly
    characters, pixel-game dialogue over a modern three-dimensional scene, or
    something else?

22. Should the page remain unlisted and blocked from search indexing?

23. What is the desired level of polish before sharing it with others?

24. Should the automation commit and push changes, create draft pull requests,
    or only leave local notes?

25. How should we decide that the automation made the house better instead of
    just adding more things?

## Suggested Next Step

Answer the questions that matter most right now, especially audience, first
blog-like explainer topic, first signal journey, which real people and real work
to include, automation behavior, source repositories, and privacy boundaries for
characters.
