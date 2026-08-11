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

This file is now the only source artifact for the page. It is a planning brief,
not the final experience.

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
- Characters inside rooms explain what they are doing when you talk to them.
- The visitor can follow the signal from room to room or jump directly into a
  stage to understand that part of the flow.
- The interaction could feel like an old handheld role-playing game: walk up to
  a person, press a button, and get a short dialogue box.
- The visual ambition could eventually be a polished Three.js scene with
  animated characters, camera movement, cutaway rooms, and richer materials.

None of this is locked in yet.

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
- Notice concrete signal journeys that could become example flows.
- Propose updates to this brief, a storyboard, or the eventual interactive page.
- Eventually extend the house with new rooms, pipes, characters, or dialogue.

Open question: should the automation directly change the public page, or should
it create draft suggestions for review first?

## Clarifying Questions

1. Who is the main audience for this experience: the Data Insights team, new
   data platform users, leadership, external visitors, or someone else?

2. What should the first real deliverable be: a written concept, a storyboard,
   a static presentation, or a small interactive Three.js prototype?

3. Should the experience be more like a guided presentation, a small game where
   you move around, or a hybrid where buttons move the camera between rooms?

4. Which repositories should the automation inspect for inspiration and Git
   contributions?

5. Should the automation update the public page automatically, or should it
   only update this brief and ask for approval before changing the experience?

6. How close should characters look to real team members? Should they be
   abstract role characters, stylized team-inspired avatars, or recognizable
   likenesses based only on explicitly approved images?

7. Which people or roles must exist in the first version, if any?

8. Which platform concepts are mandatory to explain first?

9. Which signal should be the first complete journey: application click,
   payment event, temperature reading, scheduled export, or something else?

10. Should the first journey use real Vipps MobilePay terminology and systems,
    or should it stay fictional and safe?

11. What should count as "used" at the end of the journey: dashboard, data
    product, machine learning model, operational export, alert, decision, or
    application feature?

12. How much technical depth should each step reveal before it becomes too much
    for the intended audience?

13. Should the house mirror the real Vipps MobilePay data platform architecture,
   or should it stay metaphorical and easier to understand?

14. What should a character explain when you talk to them: their current work,
    the room they are in, the pipe they own, or how to get help?

15. Should the visual style aim for realistic materials, playful low-poly
    characters, pixel-game dialogue over a modern three-dimensional scene, or
    something else?

16. Should the page remain unlisted and blocked from search indexing?

17. What is the desired level of polish before sharing it with others?

18. Should the automation commit and push changes, create draft pull requests,
    or only leave local notes?

19. How should we decide that the automation made the house better instead of
    just adding more things?

## Suggested Next Step

Answer the questions that matter most right now, especially audience, first
deliverable, first signal journey, automation behavior, source repositories, and
privacy boundaries for characters.
