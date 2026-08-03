# vipps.isakrs.com

Static GitHub Pages site for Vipps presentations, demos, and social pages.

## Main Sections

- `/presentations/` collects screen-friendly presentation viewers as cards.
- `/millionaire/` collects Vipps Millionaire games and rendered source decks.
- `/ai-day-11-06-2026/` is the AI Day page.

Most work material is intentionally unlisted. The site uses `noindex` metadata
and `robots.txt`, but anyone with the exact link can still open public pages.

## Meeting To Presentation Workflow

After a meeting, an agent can turn the recording or transcript into a published
presentation page:

1. Record the meeting and save the transcript, recording, chat export, notes, or
   agenda somewhere local or connected.
2. Open this repository in Codex or another agent-aware coding tool.
3. Ask the agent to create a presentation from the meeting conclusions and place
   it under `/presentations/<name-or-date>/`.

Example prompt:

```text
Use the meeting transcript at <path-or-link> to make a concise presentation
about the conclusions. Put it under /presentations/<date-or-topic>/, update the
presentations gallery card, commit, push, and verify the public page address.
```

The agent should extract decisions, rationale, open questions, action items,
owners, deadlines, risks, and follow-up needs. It should keep slides visual and
short, avoid inventing unsupported conclusions, and avoid committing raw meeting
recordings or transcripts.

## PowerPoint Media

Rendered PowerPoint slides are still images. When a deck contains embedded
video, extract the referenced files from `ppt/media/`, convert them to
browser-friendly MP4 when needed, place them in the page's `media/` folder, and
wire the viewer to show them on the matching slides. GitHub Pages can serve
static MP4 files; a backend is only needed for private access, streaming,
transcoding, or files that are too large for GitHub.

## Publishing

There is no build step. Add or update static files, then commit and push to
`main`. GitHub Pages deploys automatically.
