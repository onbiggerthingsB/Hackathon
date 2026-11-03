# rfelsberg29-rgb's project and AI agent guide

This is the project workspace for @rfelsberg29-rgb. Follow this guide when building the project and preparing it for the team to review.

| Item | Location |
| --- | --- |
| Repository | [onbiggerthingsB/Hackathon](https://github.com/onbiggerthingsB/Hackathon) |
| Owner | @rfelsberg29-rgb |
| Working branch | `project/rfelsberg29-rgb` |
| Project folder | `projects/rfelsberg29-rgb/` |
| Team instructions | [Root README](../../README.md) |
| Canonical agent guide | [This guide on main](https://github.com/onbiggerthingsB/Hackathon/blob/main/projects/rfelsberg29-rgb/README.md) |
| Project pull requests | [Find this branch's PRs](https://github.com/onbiggerthingsB/Hackathon/pulls?q=is%3Apr%20head%3Aproject%2Frfelsberg29-rgb) |

## Start here

1. Read the root README and the current version of this guide on `main`.
2. Check `git status` and preserve existing local work. Run `git fetch origin`.
3. Switch to `project/rfelsberg29-rgb` if it exists locally. On a fresh clone, use `git switch --track origin/project/rfelsberg29-rgb`.
4. Merge `origin/main` into your project branch before starting. Resolve changes in your folder and coordinate conflicts in shared files with the team.
5. Keep this project's source, dependency files, assets, and hardware code inside `projects/rfelsberg29-rgb/`. Preserve the other teammates' work.
6. Keep these agent instructions in the README and replace the project handoff placeholders below as the project develops.

## Build and verify

- Follow @rfelsberg29-rgb's project brief and the teacher's announced requirements.
- Use the project's chosen tools and document the exact installation and launch commands.
- Keep credentials in local environment files. Document required variable names in `.env.example`.
- Run the project's checks and exercise the main interaction through its normal interface.
- Record which hardware was actually tested, along with any simulation or keyboard fallback.
- Describe failures and remaining limitations accurately in the handoff below.

## Open or update the pull request

1. Update the project handoff below with enough information for a teammate to run and understand the project.
2. Review `git diff`, stage the intended files in `projects/rfelsberg29-rgb/`, commit, and push to `project/rfelsberg29-rgb`.
3. Check the project PR link above for an existing open PR. Update that PR when continuing the same project. Otherwise, open a PR from `project/rfelsberg29-rgb` into `main`.
4. Use the title `Add <project name> for rfelsberg29-rgb` and complete the repository's PR template.
5. Keep the PR as a draft while required implementation or verification is unfinished.

## After opening the pull request

1. Copy the PR's permanent URL into the project handoff below. Commit and push that README update to the same branch so it appears in the same PR.
2. Check the final PR diff and any GitHub checks that are configured. Fix failures caused by this project, rerun the affected checks, and push the fixes to the same PR.
3. When the project is ready, mark the PR ready for review and ask one of the other three teammates to review it.
4. Give @rfelsberg29-rgb a final handoff containing the PR URL, the project folder, exact run commands, verification results, hardware requirements, remaining issues, and the next action expected from the team.
5. Leave the PR open for team review. Address requested changes on the same branch and summarize each fix in the PR.
6. After the reviewed PR is merged, fetch and merge the latest `origin/main` before further work. Coordinate shared-launcher or cross-project changes through a separate integration PR.

Maintain project-specific details in this README. The root team table provides a stable link here so every member can find the latest handoff.

## Project handoff

Imported on November 3, 2026 from Ryan's [class-repository PR #1](https://github.com/Pomfret-Coders/fallhackathon2026/pull/1), source commit [`ed48b37`](https://github.com/rfelsberg29-rgb/fallhackathon2026/commit/ed48b37ef290375ad0c8fcc2bdede5043d61ee0d). The original four files from `teams/torque/` are preserved unchanged in `history-trebuchet/`, including Ryan's project README. This team import does not change or merge the class-repository PR.

| Field | Current value |
| --- | --- |
| Project name | World History · The trebuchet (Team Torque) |
| Main idea and goal | A Matter.js counterweight trebuchet illustration for History / World History. Compare the release speed and range of light and heavy counterweights against a wall 110 m away. |
| Pull request | Add the permanent PR URL after opening it |
| Demo or screenshot | [Ryan's existing public demo](https://rfelsberg29-rgb.github.io/rfrepo26/history-trebuchet/) |
| App entry point | [history-trebuchet/index.html](history-trebuchet/index.html) |
| Hardware requirements | None. Standard browser with mouse, touch or keyboard controls. |
| Integration notes | Standalone HTML/CSS/JavaScript. Matter.js 0.20.0 loads from cdnjs; an internet connection is required for that dependency. No API key, package installation or build step is needed. |

### Setup and run

From the repository root:

```sh
cd projects/rfelsberg29-rgb/history-trebuchet
python3 -m http.server 3012 --bind 127.0.0.1
```

Open http://127.0.0.1:3012/. Stop the server with Control-C. Any static file server can serve this folder. The public demo remains hosted in Ryan's personal repository; importing these files does not publish a second website.

### Controls and hardware

Choose a counterweight from 1× through 5× and click **Fire**. The readouts show range, release speed and wall distance; the shot log retains the latest six outcomes. Use **Reset** before another shot at the same weight. Changing the weight while idle also rebuilds the scene. **Pause/Resume** controls the simulation. Space fires and R resets when the weight slider is not focused.

No external hardware or sensor connection is used. Browser interaction was tested on this computer; physical mobile-device testing was not performed.

### Verification and remaining work

Verification on November 3, 2026:

- The imported HTML, JavaScript, stylesheet and project README are byte-for-byte identical to the pinned source commit.
- `node --check history-trebuchet/sim.js` and `git diff --check` passed.
- Browser checks verified loading the Matter.js canvas, changing the weight, firing, resetting, pause/resume and the shot log. The 1× shot traveled 72.1 m at a displayed release speed of 36.0 m/s; 5× traveled 179.2 m at 78.8 m/s. These are observations from this run, not calibrated real-world measurements.
- The desktop layout and an emulated 390-pixel phone layout were inspected. The next reviewer should also try the demo on a physical phone and the school network.

The simulation is a qualitative teaching illustration: the arm motion is scripted and Matter.js simulates the released stone. Range recording can stop when a stone hits, leaves the visible field or reaches the time limit. After a completed shot, the original Fire control appears enabled but requires Reset or a weight change before it can launch again. This import preserves those source behaviors rather than changing Ryan's model. The team should review this PR before merging it into `main`.
