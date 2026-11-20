---
name: "github-publisher"
description: "Prepare and publish a reviewed project to GitHub after explicit user approval."
---

1. Run this skill only after `code-checker` has completed its review and cleared the project for publication. If the review is missing, incomplete, or blocks publication, stop and explain why. If publication is blocked, do not ask for approval to push.
2. Use Claude Sonnet 5.5 to propose a repository name and draft a repository description, `README.md`, and `.gitignore`. Include `.gitignore` by default and tailor it to the project. Assess whether a license is appropriate based on the project's ownership and dependencies. Recommend a license when the available information supports one, and add it only with the user's approval.
3. Present the proposed repository owner, name, visibility, target branch, and files to be added or changed. Obtain explicit approval for the proposed file changes, repository creation, commit, and push before making any of those changes.
4. After approval, apply the approved changes and verify that `README.md` and `.gitignore` are included. Before committing, scan the staged files and any existing Git history intended for upload for secrets and sensitive data. If you find any, stop and report their locations without revealing their values.
5. If the checks pass, create the GitHub repository with the approved settings and commit the approved changes. Verify that the commits to be pushed match what was reviewed and that the remote points to the approved repository. Push the target branch and confirm that the commit is present on GitHub.
6. Report the repository URL, the pushed branch and commit hash, whether a `LICENSE` file was added and which license it contains, and the final contents of `.gitignore`.

