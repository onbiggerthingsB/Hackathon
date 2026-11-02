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

Replace these placeholders as work progresses.

| Field | Current value |
| --- | --- |
| Project name | The Coding Index |
| Main idea and goal | Searchable coding resource library for Science / Advanced Coding, with a Matter.js icon pile and agent-readable references |
| Pull request | Add the permanent PR URL after opening it |
| Demo or screenshot | Add a link when available |
| App entry point | `coding-library/app/page.tsx` |
| Hardware requirements | None |
| Integration notes | Standalone Next.js app inside `coding-library/`; local preview on port 3001 |

### Setup and run

From `projects/onbiggerthingsB/coding-library/`, run `npm ci` and `npm run dev`, then open http://127.0.0.1:3001. Node 20.9 or newer is required. No API key is required. See [the app README](coding-library/README.md) for build commands, data provenance and agent endpoints.

### Controls and hardware

Type a resource request and press Enter, or choose a category. Drag icons to move them and click an icon to inspect a resource. The results list supplies keyboard access and pagination. Saved links stay in the browser. Pause motion and reduced-motion support are available. Desktop browser and narrow-screen emulation were tested.

### Verification and remaining work

November 2, 2026. TypeScript and production build passed. Browser checks covered search, icon selection, saved resources, details and agent access. The current merged index has 28,358 references, including 90 featured resources. Community-imported destination sites have not all been individually checked. Public deployment and the project pull request remain pending.
