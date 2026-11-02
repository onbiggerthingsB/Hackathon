# Hackathon 2026

Our shared workspace for the Matter.js hackathon. Each teammate develops a project in their own folder and contributes it through a pull request into `main`.

## Team workspaces

| Teammate | Project folder | Project branch |
| --- | --- | --- |
| @onbiggerthingsB | `projects/onbiggerthingsB/` | `project/onbiggerthingsB` |
| @mtober27 | `projects/mtober27/` | `project/mtober27` |
| @rfelsberg29-rgb | `projects/rfelsberg29-rgb/` | `project/rfelsberg29-rgb` |
| @hqddd-dot | `projects/hqddd-dot/` | `project/hqddd-dot` |

Each folder can contain its own app, dependencies, assets, and setup instructions. The starting branches are already available on GitHub.

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
5. Update your project's README with its idea, exact setup and run commands, controls, hardware requirements, and current limitations.
6. Run your project locally and verify its main interaction.
7. Commit and push your work.

   ```sh
   git add projects/YOUR_USERNAME
   git commit -m "Add my hackathon project"
   git push -u origin HEAD
   ```

8. Open a pull request on GitHub with `main` as the base and your project branch as the compare branch. Use a draft PR while building, then mark it ready and request a teammate's review when the project runs.
9. Merge after the team has reviewed the project and its run instructions.

When teammates' changes have been merged, bring them into your branch with `git fetch origin` followed by `git merge origin/main`.

## Working with an AI coding agent

Give your agent the repository and your username, then use this prompt with `YOUR_USERNAME` replaced.

> Work on branch `project/YOUR_USERNAME` in the shared Hackathon repository. Your project belongs in `projects/YOUR_USERNAME/`. Read the root README first. Preserve the other teammates' work and coordinate edits to shared files. Keep this project's dependencies and assets in its own folder. Implement my project, verify its main interaction, document the exact setup and run commands plus any required hardware, then open a pull request into `main` explaining the changes and verification.

Commit source files, dependency manifests, lockfiles, and required assets. Keep credentials in local environment files and document required variable names in `.env.example`.

## Combine the projects

Use a separate integration branch and pull request for a shared launcher, shared hardware input, or features used by several projects. Agree on shared interfaces as a team before moving code between project folders.

The final hackathon brief will determine how we combine the projects. Record agreed requirements here once they are announced.
