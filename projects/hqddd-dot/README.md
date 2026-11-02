# hqddd-dot's project and AI agent guide

This is the project workspace for @hqddd-dot. Follow this guide when building the project and preparing it for the team to review.

| Item | Location |
| --- | --- |
| Repository | [onbiggerthingsB/Hackathon](https://github.com/onbiggerthingsB/Hackathon) |
| Owner | @hqddd-dot |
| Working branch | `project/hqddd-dot` |
| Project folder | `projects/hqddd-dot/` |
| Team instructions | [Root README](../../README.md) |
| Canonical agent guide | [This guide on main](https://github.com/onbiggerthingsB/Hackathon/blob/main/projects/hqddd-dot/README.md) |
| Project pull requests | [Find this branch's PRs](https://github.com/onbiggerthingsB/Hackathon/pulls?q=is%3Apr%20head%3Aproject%2Fhqddd-dot) |

## Start here

1. Read the root README and the current version of this guide on `main`.
2. Check `git status` and preserve existing local work. Run `git fetch origin`.
3. Switch to `project/hqddd-dot` if it exists locally. On a fresh clone, use `git switch --track origin/project/hqddd-dot`.
4. Merge `origin/main` into your project branch before starting. Resolve changes in your folder and coordinate conflicts in shared files with the team.
5. Keep this project's source, dependency files, assets, and hardware code inside `projects/hqddd-dot/`. Preserve the other teammates' work.
6. Keep these agent instructions in the README and replace the project handoff placeholders below as the project develops.

## Build and verify

- Follow @hqddd-dot's project brief and the teacher's announced requirements.
- Use the project's chosen tools and document the exact installation and launch commands.
- Keep credentials in local environment files. Document required variable names in `.env.example`.
- Run the project's checks and exercise the main interaction through its normal interface.
- Record which hardware was actually tested, along with any simulation or keyboard fallback.
- Describe failures and remaining limitations accurately in the handoff below.

## Open or update the pull request

1. Update the project handoff below with enough information for a teammate to run and understand the project.
2. Review `git diff`, stage the intended files in `projects/hqddd-dot/`, commit, and push to `project/hqddd-dot`.
3. Check the project PR link above for an existing open PR. Update that PR when continuing the same project. Otherwise, open a PR from `project/hqddd-dot` into `main`.
4. Use the title `Add <project name> for hqddd-dot` and complete the repository's PR template.
5. Keep the PR as a draft while required implementation or verification is unfinished.

## After opening the pull request

1. Copy the PR's permanent URL into the project handoff below. Commit and push that README update to the same branch so it appears in the same PR.
2. Check the final PR diff and any GitHub checks that are configured. Fix failures caused by this project, rerun the affected checks, and push the fixes to the same PR.
3. When the project is ready, mark the PR ready for review and ask one of the other three teammates to review it.
4. Give @hqddd-dot a final handoff containing the PR URL, the project folder, exact run commands, verification results, hardware requirements, remaining issues, and the next action expected from the team.
5. Leave the PR open for team review. Address requested changes on the same branch and summarize each fix in the PR.
6. After the reviewed PR is merged, fetch and merge the latest `origin/main` before further work. Coordinate shared-launcher or cross-project changes through a separate integration PR.

Maintain project-specific details in this README. The root team table provides a stable link here so every member can find the latest handoff.

## Project handoff

| Field | Current value |
| --- | --- |
| Project name | Paint Mixer Challenge |
| Department and class | Art · Painting & Drawing (Color Theory); also fits Freshman Arts Immersion: Painting & Drawing |
| Main idea and goal | Paint drops fall into a bowl and, when they touch, merge and mix like real paint (blue + yellow = green). Students match target colors across 5 levels: secondary, tertiary, tints & shades, earth tones, and master mixes. Works as a class demo (the teacher projects it) or as homework (students open the link). |
| Pull request | Pending: added after the PR opens |
| Demo or screenshot | No hosted demo yet. Turning on GitHub Pages for `main` would give a public link. |
| App entry point | `projects/hqddd-dot/index.html` |
| Hardware requirements | None. Any modern browser with a mouse, trackpad, or touch screen. |
| Integration notes | One static HTML file with no build step. Matter.js 0.20.0 loads from cdnjs. A shared launcher can link straight to `projects/hqddd-dot/index.html`. |

### Setup and run

No install needed. From the repository root:

```sh
cd projects/hqddd-dot
python3 -m http.server 8000
```

Then open http://localhost:8000/. Opening `index.html` directly in a browser also works. Both need internet access to load Matter.js from cdnjs.

### Controls and hardware

- **Red / Yellow / Blue / White / Black** buttons select a paint and drop one drop into the bowl.
- **Click or tap above the bowl** to drop the selected paint at that spot.
- Paint can't be removed. A color passes at a **93% match** within the **drop limit** (the recipe's drops + 2).
- **Hint** shows the recipe but caps that color at 1★. **Empty bowl** restarts the current color. **Skip color** picks a new one. **Next color** appears after a match.
- Stars: ★★★ = exact number of drops, ★★ = a few extra drops, ★ = used the hint. Solve 3 colors to unlock the next level.
- Tested with a mouse in a desktop Chromium browser. No other hardware.

### Verification and remaining work

- Ran it in the Claude desktop app's built-in Chromium browser at about 1024×700. Dropping an exact recipe (Orange = 1 Red + 1 Yellow) merged into one blob, scored 100%, and earned ★★★. Too many drops shows "Out of drops." No console errors.
- Not yet tested: Safari, phones or tablets, and a classroom projector.
- Next action for the reviewer: open `index.html`, play through Level 1, and check that the header shows the department and class clearly.
