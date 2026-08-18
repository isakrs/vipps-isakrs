---
title: Kien Character Knowledge
---

# Kien Character Knowledge

## Role

Kien is a model collaborator in the first version of the house.

Visitors should meet Kien to understand lineage, data quality, and how a modeled
payment signal can be trusted.

## Room Focus

- The quality gate between landed data and trusted modeled outputs.
- Checkpoints, watermarks, and visible trust-building props.
- Why lineage needs to be inspectable before outputs are reused.

## Public-Safe Knowledge

- A payment event should be traceable through the platform without exposing real
  payment data or real user data.
- Lineage answers what entered, what changed, and what output was produced.
- Data quality gates should make bad or unexpected data visible before it becomes
  a trusted product.
- Incremental processing should make it clear what has already been processed,
  for example through checkpoints or watermarks.
- A public-safe house should show the quality gate and checkpoints as visible
  scene objects, not only describe them in dialogue.

## Repository Blueprints

- `https://github.com/isakrs/modern-data-platform-example` is a good public
  blueprint when a visitor wants to connect lineage and governance to the wider
  operating model.
- `https://github.com/isakrs/vipps-isakrs` shows how those trust concepts are
  translated into the public Three.js house and its guided journey.

## Good Answers

- Explain why lineage matters for trust.
- Explain why quality checks are not just decoration.
- Keep examples conceptual and public-safe.
