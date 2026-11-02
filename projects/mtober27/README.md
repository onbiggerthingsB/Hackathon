# mtober27's project and AI agent guide

This is the project workspace for @mtober27. Follow this guide when building the project and preparing it for the team to review.

| Item | Location |
| --- | --- |
| Repository | [onbiggerthingsB/Hackathon](https://github.com/onbiggerthingsB/Hackathon) |
| Owner | @mtober27 |
| Working branch | `project/mtober27` |
| Project folder | `projects/mtober27/` |
| Team instructions | [Root README](../../README.md) |
| Canonical agent guide | [This guide on main](https://github.com/onbiggerthingsB/Hackathon/blob/main/projects/mtober27/README.md) |
| Project pull requests | [Find this branch's PRs](https://github.com/onbiggerthingsB/Hackathon/pulls?q=is%3Apr%20head%3Aproject%2Fmtober27) |

## Start here

1. Read the root README and the current version of this guide on `main`.
2. Check `git status` and preserve existing local work. Run `git fetch origin`.
3. Switch to `project/mtober27` if it exists locally. On a fresh clone, use `git switch --track origin/project/mtober27`.
4. Merge `origin/main` into your project branch before starting. Resolve changes in your folder and coordinate conflicts in shared files with the team.
5. Keep this project's source, dependency files, assets, and hardware code inside `projects/mtober27/`. Preserve the other teammates' work.
6. Keep these agent instructions in the README and replace the project handoff placeholders below as the project develops.

## Build and verify

- Follow @mtober27's project brief and the teacher's announced requirements.
- Use the project's chosen tools and document the exact installation and launch commands.
- Keep credentials in local environment files. Document required variable names in `.env.example`.
- Run the project's checks and exercise the main interaction through its normal interface.
- Record which hardware was actually tested, along with any simulation or keyboard fallback.
- Describe failures and remaining limitations accurately in the handoff below.

## Open or update the pull request

1. Update the project handoff below with enough information for a teammate to run and understand the project.
2. Review `git diff`, stage the intended files in `projects/mtober27/`, commit, and push to `project/mtober27`.
3. Check the project PR link above for an existing open PR. Update that PR when continuing the same project. Otherwise, open a PR from `project/mtober27` into `main`.
4. Use the title `Add <project name> for mtober27` and complete the repository's PR template.
5. Keep the PR as a draft while required implementation or verification is unfinished.

## After opening the pull request

1. Copy the PR's permanent URL into the project handoff below. Commit and push that README update to the same branch so it appears in the same PR.
2. Check the final PR diff and any GitHub checks that are configured. Fix failures caused by this project, rerun the affected checks, and push the fixes to the same PR.
3. When the project is ready, mark the PR ready for review and ask one of the other three teammates to review it.
4. Give @mtober27 a final handoff containing the PR URL, the project folder, exact run commands, verification results, hardware requirements, remaining issues, and the next action expected from the team.
5. Leave the PR open for team review. Address requested changes on the same branch and summarize each fix in the PR.
6. After the reviewed PR is merged, fetch and merge the latest `origin/main` before further work. Coordinate shared-launcher or cross-project changes through a separate integration PR.

Maintain project-specific details in this README. The root team table provides a stable link here so every member can find the latest handoff.

## Project handoff

| Field | Current value |
| --- | --- |
| Project name | Galton Board |
| Main idea and goal | Math Department, Statistics. Balls fall through pegs and pile into a bell curve. Students compare the piles with the binomial prediction. |
| Pull request | https://github.com/onbiggerthingsB/Hackathon/pull/1 |
| Demo or screenshot | Run locally from `projects/mtober27/index.html`. No hosted demo yet. |
| App entry point | `projects/mtober27/index.html` |
| Hardware requirements | None |
| Integration notes | Static page. No build step and no shared launcher yet. Serve this folder and link to `index.html`. |

### Setup and run

No install and no environment variables. From the repository root:

```sh
cd projects/mtober27
python3 -m http.server 8765
```

Open http://127.0.0.1:8765/

Matter.js 0.20.0 is already in `vendor/matter.min.js`.

### Controls and hardware

No hardware. Tested in desktop Chrome.

| Control | What it does |
| --- | --- |
| Drop 1, Drop 40, Drop 120 | Release that many balls. The board holds 140. |
| Click the board | Drop one ball. |
| Pause / Resume | Freeze or continue the physics. Space does this when focus is not in a control. |
| Reset | Clear the balls and return the wind to fair. R does this when focus is not in a control. |
| Peg rows | 6 to 12. Changing it clears the board. |
| Side wind | Push falling balls left or right. Reset before comparing that run with a fair one. |
| Show the fair prediction | Show or hide the red binomial marks. |

### Verification and remaining work

Checked on November 2, 2026 in headless Chrome.

- A fair 8-row run of 100 balls averaged bin 3.9. The fair value is 4.0. Every settled ball stayed inside its assigned bin.
- Earlier fair runs of 120 balls averaged 4.1 and 3.8. Side wind of 0.8 moved the average about one bin off center.
- The spread is wider than a perfect coin-flip model at 8 rows. The page says so.
- The page was also checked at a laptop size. Department, class, controls, piles, and the comparison chart are on the first screen.

Still open: a public class link, and a classmate trying the page without help. The next step is a teammate review of this pull request.
