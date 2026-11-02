# Hackathon 2026

Our shared workspace for the Matter.js hackathon. Each teammate develops a project in their own folder and contributes it through a pull request into `main`.

## Team workspaces

| Teammate | Project and agent guide | Project branch |
| --- | --- | --- |
| @onbiggerthingsB | [Open guide](projects/onbiggerthingsB/README.md) | `project/onbiggerthingsB` |
| @mtober27 | [Open guide](projects/mtober27/README.md) | `project/mtober27` |
| @rfelsberg29-rgb | [Open guide](projects/rfelsberg29-rgb/README.md) | `project/rfelsberg29-rgb` |
| @hqddd-dot | [Open guide](projects/hqddd-dot/README.md) | `project/hqddd-dot` |

Each folder can contain its own app, dependencies, assets, and setup instructions. The starting branches are already available on GitHub.

Each member's guide contains their working instructions, a link to their project PRs, and a project handoff with run commands, hardware requirements, and verification results. Add the permanent PR URL to that handoff after opening the PR.

## Contribute your project

1. Accept the GitHub repository invitation.
2. Clone the group repository.

   ```sh
   git clone https://github.com/onbiggerthingsB/Hackathon.git
   cd Hackathon
   ```

3. Replace `YOUR_USERNAME` with your username from the table and check out your branch.

   ```sh
   git fetch origin
   git switch --track origin/project/YOUR_USERNAME
   ```

4. Add your project inside `projects/YOUR_USERNAME/`. Keep its dependency files and assets in that folder. When bringing in an existing project, copy its source files into this folder and leave its separate `.git` directory behind.
5. Keep your README's agent instructions and update its project handoff with the idea, exact setup and run commands, controls, hardware requirements, and current limitations.
6. Run your project locally and verify its main interaction.
7. Commit and push your work.

   ```sh
   git add projects/YOUR_USERNAME
   git commit -m "Add my hackathon project"
   git push -u origin HEAD
   ```

8. Open or update your project pull request on GitHub with `main` as the base and your project branch as the compare branch. Use a draft PR while building. Follow the steps after opening a PR in your member guide.
9. Add the PR URL to your project handoff, check the final diff and configured checks, then request a teammate's review when the project is ready.
10. The team merges after reviewing the project and its run instructions.

When teammates' changes have been merged, bring them into your branch with `git fetch origin` followed by `git merge origin/main`.

## Working with an AI coding agent

Give your agent the repository and your username, then use this prompt with `YOUR_USERNAME` replaced.

> Work on branch `project/YOUR_USERNAME` in the shared Hackathon repository. Your project belongs in `projects/YOUR_USERNAME/`. Read the root README and the member guide in your project folder, including its steps after opening a pull request. Preserve the other teammates' work and coordinate edits to shared files. Implement my project, verify its main interaction, and maintain the project handoff in the member README. Open or update the project PR into `main`, record its URL in the README, check the final diff and configured checks, and hand me the PR link and exact run instructions. Leave the PR open for team review.

Commit source files, dependency manifests, lockfiles, and required assets. Keep credentials in local environment files and document required variable names in `.env.example`.

## Combine the projects

Use a separate integration branch and pull request for a shared launcher, shared hardware input, or features used by several projects. Agree on shared interfaces as a team before moving code between project folders.

The final challenge requires four public, web-accessible Matter.js simulations covering four different academic departments. Each simulation must name its department and specific class prominently and serve a real educational purpose. An entry can earn up to 4 points, for a team maximum of 16.

Track department choices, owners, public links, pull requests, contribution evidence, reviewers, and remaining delivery checks in the [team delivery register](TEAM_DELIVERY.md). The register separates official requirements from our suggested readiness checks; unknown choices and unverified links stay marked pending.
