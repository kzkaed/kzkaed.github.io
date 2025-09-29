# Project Plan

Last updated: 2025-09-29 07:00 (local time)

## Objectives
- Maintain and evolve kzkaed.github.io as a lightweight, fast, and readable personal site.
- Capture decisions and rationale using ADRs in docs/adr.
- Publish incremental improvements with minimal process overhead.

## Scope (near-term)
- Content: Add initial posts/pages and a simple home layout.
- Infrastructure: Keep using GitHub Pages with minimal tooling.
- Process: Track high-level plan here and record important decisions as ADRs.

## Milestones
1. MVP site skeleton
   - Home page with brief intro
   - Plans page linked from nav
2. First content drop
   - 1–2 short posts or pages
3. Quality/pass polish
   - Basic styling pass
   - Check mobile readability
4. Sustainment
   - Set cadence for updates (see Next Steps)

## Timeline (lightweight)
- Week 1: Create/verify pages and links, publish MVP
- Week 2: Add first content; review typography and spacing
- Week 3+: Iterate monthly with small improvements

## Next Steps (1–2 weeks)
- Create a minimal home/index with links to Plans
- Write a short “Scutigera Post” post/page
- Review typography (font-size, line-height) for readability

## Risks & Mitigations
- Scope creep → Keep milestones small and ship weekly
- Broken links → Add a quick manual link check before publishing
- Inconsistent style → Establish a tiny style checklist in README

## Communication
- Changelog is implicit via git history

## References
- Todos:
  - Consider adding a linter or formatter for Markdown (e.g., markdownlint)
  - Explore Astro content collections for richer content management

## AI-Assist Plan
### Goals
- Speed up content drafting and reviews while keeping a human-in-the-loop.
- Preserve privacy; keep prompts and outputs lightweight and transparent.
- Avoid vendor lock-in; prefer simple, optional tooling.

### Near-term use cases
- Draft post outlines and headings for human refinement.
- Generate meta descriptions and alt text suggestions.
- Run quick readability and link-check prompts.

### Guardrails
- Never auto-publish AI output; human review required.
- No sensitive/PII in prompts or context.
- Verify facts and links; cite sources when appropriate.
- Document AI usage briefly in PR descriptions.
- Keep prompts/checklists in-repo under docs/ai.

### Milestones
1. Define guidelines and prompt snippets
   - docs/ai/README with usage and guardrails
   - docs/ai/prompts: post-outline.md, adr-helper.md
2. Trial on one post
   - Use AI to draft a "Hello" post
   - Edit and review thoroughly
   - Document process and lessons learned
3. Integrate a short "AI review" checklist in README

### Next steps (1–2 weeks)
- Add docs/ai/README and two prompt snippets.
- Draft one AI-assisted "Hello" post and edit manually.
-

### Metrics (lightweight)
- Time saved per draft (self-estimate).
- Number of AI-assisted drafts merged.
- Review fixes needed due to AI errors.

### Risks & mitigations
- Hallucinations → strict human review, cite sources.
- Style drift → maintain style checklist; edit for voice.
- Tool dependency → keep tooling optional; store prompts locally.

---
Changelog
- 2025-09-29: Added AI-Assist plan
- 2025-09-29: Initial plan created