# Classroom readiness implementation plan

> **For agentic workers:** Use subagent-driven development for independent work, with a final integrated review. Preserve the existing project branch and teammates' files.

**Goal:** Make Coding Index deliverable, easier to evaluate, and useful for a student's complete resource-to-agent workflow.

**Architecture:** Keep the existing Next.js app and Matter.js world. Add optional reviewed resource metadata, a browser-local project tray, and a deterministic brief generator. Keep search and the large catalog on the server.

**Tech Stack:** Existing Next.js, React, Matter.js and TypeScript. Node built-in tests; no new packages.

**Spec:** The user-approved recommendations in the criteria audit at `../../../../../../../../research/coding-index-criteria-audit-2026-11-02/README.md` and `/Users/likerun/HACKATHON_REQUIREMENTS.md`.

## Global constraints

- Preserve the reference-inspired dark layout and falling icon interaction.
- Keep work on `project/onbiggerthingsB`; leave the pull request open for team review.
- Preserve other members' project files; do not invent their projects or contributions.
- No new dependencies, secrets, paid services or unrelated configuration changes.
- Distinguish checked guidance from unverified community imports.
- Retain keyboard and reduced-motion access to every essential action.
- Public deployment and draft PR are included in the user's accepted delivery sequence. Do not merge or submit the organizer's form.

## Review focus

- Corrupt or stale browser data must not crash the tray or copy operation.
- Duplicate additions must not multiply resources or overwhelm the brief.
- Drag release must not also open the resource, and must work after rerenders.
- Remote agents must receive public source URLs, not local-only origin assumptions.
- Identical GitHub favicons must be distinguishable with visible resource names.

## Task 1: Delivery path and team readiness

- [ ] Confirm live GitHub state, hosting account and existing project settings.
- [ ] Add a concise team delivery register with confirmed facts and explicit unknowns.
- [ ] Build and prepare the standalone app for an appropriate existing hosting account.
- [ ] Commit and push the project branch; open a draft PR and record its URL.
- [ ] Deploy the verified app and test public page, API and agent guide. Update handoff evidence.

## Task 2: Reviewed featured resources

Owner files: `lib/resources.ts`, `data/coding-resources.json`, `app/resources/[id]/page.tsx`, `tests/resource-guidance.test.*`.

Interface: export `ResourceGuidance` with `bestFor: string`, `frameworks: string[]`, `setup: "low" | "moderate" | "advanced"`, `caveat: string`, `checkedAt: string`, `sourceUrls: string[]`. Add optional `Resource.guidance`.

- [ ] Add a failing test for guidance presence, shape and unchanged catalog identity/count.
- [ ] Check official documentation for at least 12 useful featured resources; retain evidence URLs and date. Setup difficulty is editorial guidance, not a vendor claim.
- [ ] Parse optional guidance, expose it in API output, and render it on resource pages.
- [ ] Run focused tests and type checking.

## Task 3: Physics drop target and readable results

Owner files: `components/IconFloor.tsx`, `components/floor/*`, focused drag tests if a pure helper is introduced.

Interface: optional `getDropBounds(): {left:number;right:number;top:number;bottom:number}|null`, `onResourceDrop(src:string): void` props. Invoke only after an actual drag released inside the target. Preserve click-to-open elsewhere. Show visible concise names for raised results while retaining hover details.

- [ ] Establish drag/click acceptance checks before edits.
- [ ] Implement optional drop target and resource name captions without per-frame React state.
- [ ] Preserve pause/reduced-motion operation and clean lifecycle teardown.
- [ ] Type check; hand off browser checks to root.

## Task 4: Recognizable icons

Owner files: `app/api/resource-icon/[id]/route.ts`, optional pure helper and tests.

- [ ] Test that repository links do not all choose the host favicon.
- [ ] Return a deterministic resource-name monogram for GitHub repository resources; keep cached favicons for actual product sites.
- [ ] Preserve bounded cache, timeout and safe fallback behavior.

## Task 5: Project tray and student workflow

Owner files: `components/CodingIndex.tsx`, `components/ProjectTray.tsx`, `lib/project-brief.ts`, `app/globals.css`, `app/llms.txt/route.ts`, `tests/project-brief.test.*`.

- [ ] Write failing tests for unique resource selection, invalid storage, limits and a brief including goal, stack, sources, guidance and acceptance steps.
- [ ] Implement pure tray parsing and brief generation; store only validated data locally.
- [ ] Add an always reachable tray/drop target, goal/stack fields, add/remove buttons, copy and download.
- [ ] Connect Matter drop events; allow the same task with buttons and keyboard.
- [ ] Surface reviewed guidance in details and result rows, enlarge class label, add useful starting queries and the Tools category.
- [ ] Update the agent guide for project packs and public access.

## Task 6: Integrated validation and delivery

- [ ] Run meaningful Node tests, TypeScript and production build.
- [ ] Review React/Next changes with an independent reviewer and address findings.
- [ ] Browser-check desktop/narrow view, drag-to-tray, duplicates, keyboard, pause, persistence, copy/download and repeated search.
- [ ] Validate deployed site and API without login. Do not claim actual classmate testing or school-network testing without it.
- [ ] Update project README and team register with actual evidence and remaining human dependencies.

## Execution ledger

- 2026-11-02: Plan checked against the accepted audit. Tasks 2 and 5 share only the `guidance` interface; tasks 3 and 5 share only drop callbacks; task 4 consumes the existing catalog API. Ownership avoids concurrent file edits. Existing feature branch is retained to preserve the established team workflow. Higher-priority instructions authorize continuing without a second plan approval and parallelizing independent work.
- Tasks 2–5 implemented and locally verified. Fourteen resources have checked guidance; names and monograms distinguish results; the tray persists and exports a project brief. Independent review identified one storage hydration issue, fixed with two regression tests and re-reviewed as resolved.
- Ego Browser confirmed desktop and emulated-touch additions, no click-through dialog, persistence after reload, button-based addition, brief download, reduced motion and the mobile layout. Pure browser-protocol calls were needed because high-level automation changed tab visibility/viewport between input events. No production input workaround was added for the automation behavior.
- Final local tests/build, public deployment and GitHub handoffs remain in progress. Exact deadline, form URL, teammate entries and real peer testing remain unconfirmed.
