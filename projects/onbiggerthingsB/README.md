# onbiggerthingsB's project and AI agent guide

This is the project workspace for @onbiggerthingsB. Follow this guide when building the project and preparing it for the team to review.

| Item | Location |
| --- | --- |
| Repository | [onbiggerthingsB/Hackathon](https://github.com/onbiggerthingsB/Hackathon) |
| Owner | @onbiggerthingsB |
| Working branch | `project/onbiggerthingsB` |
| Project folder | `projects/onbiggerthingsB/` |
| Team instructions | [Root README](../../README.md) |
| Canonical agent guide | [This guide on main](https://github.com/onbiggerthingsB/Hackathon/blob/main/projects/onbiggerthingsB/README.md) |
| Project pull requests | [Find this branch's PRs](https://github.com/onbiggerthingsB/Hackathon/pulls?q=is%3Apr%20head%3Aproject%2FonbiggerthingsB) |

## Start here

1. Read the root README and the current version of this guide on `main`.
2. Check `git status` and preserve existing local work. Run `git fetch origin`.
3. Switch to `project/onbiggerthingsB` if it exists locally. On a fresh clone, use `git switch --track origin/project/onbiggerthingsB`.
4. Merge `origin/main` into your project branch before starting. Resolve changes in your folder and coordinate conflicts in shared files with the team.
5. Keep this project's source, dependency files, assets, and hardware code inside `projects/onbiggerthingsB/`. Preserve the other teammates' work.
6. Keep these agent instructions in the README and replace the project handoff placeholders below as the project develops.

## Build and verify

- Follow @onbiggerthingsB's project brief and the teacher's announced requirements.
- Use the project's chosen tools and document the exact installation and launch commands.
- Keep credentials in local environment files. Document required variable names in `.env.example`.
- Run the project's checks and exercise the main interaction through its normal interface.
- Record which hardware was actually tested, along with any simulation or keyboard fallback.
- Describe failures and remaining limitations accurately in the handoff below.

## Open or update the pull request

1. Update the project handoff below with enough information for a teammate to run and understand the project.
2. Review `git diff`, stage the intended files in `projects/onbiggerthingsB/`, commit, and push to `project/onbiggerthingsB`.
3. Check the project PR link above for an existing open PR. Update that PR when continuing the same project. Otherwise, open a PR from `project/onbiggerthingsB` into `main`.
4. Use the title `Add <project name> for onbiggerthingsB` and complete the repository's PR template.
5. Keep the PR as a draft while required implementation or verification is unfinished.

## After opening the pull request

1. Copy the PR's permanent URL into the project handoff below. Commit and push that README update to the same branch so it appears in the same PR.
2. Check the final PR diff and any GitHub checks that are configured. Fix failures caused by this project, rerun the affected checks, and push the fixes to the same PR.
3. When the project is ready, mark the PR ready for review and ask one of the other three teammates to review it.
4. Give @onbiggerthingsB a final handoff containing the PR URL, the project folder, exact run commands, verification results, hardware requirements, remaining issues, and the next action expected from the team.
5. Leave the PR open for team review. Address requested changes on the same branch and summarize each fix in the PR.
6. After the reviewed PR is merged, fetch and merge the latest `origin/main` before further work. Coordinate shared-launcher or cross-project changes through a separate integration PR.

Maintain project-specific details in this README. The root team table provides a stable link here so every member can find the latest handoff.

## Project handoff

Current handoff as of November 2, 2026.

| Field | Current value |
| --- | --- |
| Project name | The Coding Index |
| Main idea and goal | Searchable coding resource library for Science / Advanced Coding, with a Matter.js icon pile and agent-readable references |
| Pull request | [Laptop tilt PR #6](https://github.com/onbiggerthingsB/Hackathon/pull/6), ready for review after the owner's live-site physical tilt check. Original project PR #2 is merged. |
| Demo or screenshot | [Live Coding Index](https://pomfret-coding-index.vercel.app), verified November 2, 2026 |
| App entry point | `coding-library/app/page.tsx` |
| Hardware requirements | Standard browser use needs none. Optional laptop tilt uses a compatible Apple Silicon MacBook's sensor and the local motion helper. |
| Integration notes | Standalone Next.js app inside `coding-library/`; local preview on port 3001 |

### Setup and run

From `projects/onbiggerthingsB/coding-library/`, run `npm ci` and `npm run dev`, then open http://127.0.0.1:3001. Node 20.9 or newer is required. No API key is required. See [the app README](coding-library/README.md) for build commands, data provenance and agent endpoints.

### Controls and hardware

Type a resource request and press Enter, or choose a category. Drag icons to move them and click an icon to inspect a resource. The results list supplies keyboard access and pagination. Raised results show resource names, and GitHub repository links use distinct resource monograms. Fourteen featured resources have documentation-checked guidance. Drag resources into My project or use Add to project, enter a goal and stack, then copy or download a Markdown brief. Saved links and the project kit stay in the browser. Pause motion and reduced-motion support are available. Desktop and emulated-touch interactions, persistence, keyboard access and reduced motion were checked.

### Verification and remaining work

Optional laptop tilt is documented in [the setup guide](coding-library/docs/LAPTOP_TILT.md). Run `npm run motion` from `coding-library/`, keep the terminal open, then enable Laptop tilt on the site. The helper sends motion readings directly to the page on the same computer.

November 2, 2026. All 29 Node tests, TypeScript and the production build passed. Independent review identified a browser-storage hydration issue; the fix and two regression tests were re-reviewed as resolved. A clean independent `npm ci` verified the portable lockfile, and `npm audit` reported zero vulnerabilities after patching the existing Next.js dependency to 16.4.4. No new dependency choices were added.

Browser checks covered desktop and emulated touch, search, named results, drag and button additions, duplicate handling, persistence, keyboard access, reduced motion, brief copy/download, details and agent access. The current index has 28,358 references, including 90 featured resources; 14 have documentation-checked guidance. Community-imported destination sites and external libraries have not all been individually run or verified. No physical-phone, real-student or school-Wi-Fi testing is claimed.

The original project, credit cleanup and shared delivery documentation were merged through PRs #2, #5 and #4. The previous production deployment passed public checks for the homepage, search, checked resource API and page, icons and agent guide.

The new tilt helper received 4,026 fresh accelerometer reports during a five-second probe on the M4 Pro MacBook Pro. The local browser received real sensor data, and calibration, pause/resume and switching tilt off were checked. Automated tests cover stale readings and teardown. On November 2, 2026, the owner confirmed that the live site's icons move toward the lowered side in both directions, completing the live-connection and physical-direction checks on this Mac. The next team action is review of the tilt update and a real classroom trial.

The tilt update is deployed at the live link above. Deployment `dpl_bsze8G3jnkhBq3TpmKPJTmTAYPhU` uses app revision `cd69b4d`. Public HTTP checks confirmed the new controls and working resource search. The final PR diff is confined to this project folder, and GitHub reported no configured checks. Later handoff-only commits do not change the deployed app.
