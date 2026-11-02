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

Replace these placeholders as work progresses.

| Field | Current value |
| --- | --- |
| Project name | Awaiting the owner's choice |
| Main idea and goal | Awaiting the project brief |
| Pull request | Add the permanent PR URL after opening it |
| Demo or screenshot | Add a link when available |
| App entry point | Add the relative path |
| Hardware requirements | List the exact devices or write `None` |
| Integration notes | Describe how the team can launch or combine this project |

### Setup and run

Add exact commands, their working directory, dependencies, environment variable names, and the local URL or other entry point.

### Controls and hardware

Describe the controls, hardware connection steps, and any fallback mode. State which devices you actually tested.

### Verification and remaining work

List the checks and manual interactions you ran, their results, remaining issues, and the next action for the reviewer.
