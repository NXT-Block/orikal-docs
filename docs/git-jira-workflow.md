# 🔁 Git & Jira Workflow Guide – Orikal

This document outlines the standardized workflow for working with Jira tickets and Git branches across all Orikal repositories. It ensures automated linking between commits, pull requests, and Jira issues — enabling smooth progress tracking and efficient collaboration.

---

## 🧭 Branching Strategy

Each repository in the Orikal ecosystem follows this structure:

- `main` → Production-ready code
- `dev` → Integration branch for all active work (except documentation)
- `work-dev` → Integration branch for documentation (`orikal-docs` repository only)
- `feature/NXTB-XX-description` → Short-lived branches per Jira ticket

### ✅ Example for Code Repositories

For Jira ticket `NXTB-15: [FRONT] Bootstrap Next.js app`:

```bash
git checkout dev
git pull origin dev
git checkout -b NXTB-15-front-bootstrap-next-js-app
```

### ✅ Example for Documentation Repository (`orikal-docs`)

For Jira ticket `NXTB-102: [DOC] Add Git & Jira workflow guide`:

```bash
git checkout work-dev
git pull origin work-dev
git checkout -b doc/NXTB-102-git-jira-workflow
```

> ℹ️ To ensure that the branch is correctly linked to the Jira issue and displayed under **Development**, it is recommended to **create the branch directly from the Jira interface**. This guarantees that the branch naming is recognized by Jira and avoids inconsistencies.

---

## 🔗 Linking Git to Jira

To automatically link commits and PRs to Jira issues, include the ticket key (`NXTB-XX`) in:

- Branch names
- Commit messages
- Pull request titles or descriptions

Jira will then display all related activity (branch, commits, PRs) inside the issue view under **Development**.

---

## ✅ Automatic Jira Transition on PR Merge

When a pull request is merged, Jira can automatically update the issue status.

Currently, the ticket is automatically moved from **"In Progress"** to **"To Be Reviewed"** when a PR is opened.

To ensure this works:

- Include the ticket key in your PR title or description (e.g. `Fixes NXTB-15`)
- Use one of the supported transition keywords if Jira automation is configured:

```md
Fixes NXTB-15
Closes NXTB-15
Resolves NXTB-15
```

✅ Supported keywords: `Fixes`, `Closes`, `Resolves`  
✅ Use them in the PR **title or description**

> 🔁 The ticket will be moved to "To Be Reviewed" on PR open, and potentially to "Done" if a rule is set upon merge.

---

## ✍️ Commit Message Format

To help Jira identify and link your work correctly, follow this simple format when writing your commit messages:

### ✅ Commit Example:
```bash
git commit -m "NXTB-55: Add section on branch naming from Jira"
```

### Format:
```
NXTB-XX: Short but descriptive message
```

- Always begin with the **Jira ticket key** (e.g. `NXTB-55`)
- Follow it with a colon `:` and a **clear summary** of the commit

> ℹ️ While this does not trigger transitions, it ensures your commits are properly linked in the Jira issue view.

---

## 🌟 Closing Multiple Tickets in One PR

You can reference and transition multiple Jira issues in a single PR:

```md
Fixes NXTB-12  
Closes NXTB-15  
Resolves NXTB-18
```

All referenced tickets will be updated according to the configured Jira automation rules.

---

## 📝 Pull Request Example

A good PR description should clearly state the ticket it addresses and give context for reviewers:

```md
### 🎟️ Jira Ticket
Fixes NXTB-42

### 🧾 Description
Implements the wallet connection UI and sets up basic layout routing.

### ✅ Checklist
- [x] Code compiles and passes tests
- [x] Linked to a Jira ticket
- [x] Targets the appropriate integration branch (`dev` or `work-dev`)
- [x] PR ready for review/merge
```

> 💡 While a `.github/pull_request_template.md` can be used in each repo, this format is only a recommendation.

---

## 📂 Cleaning Up

Once a feature branch has been merged:

- Delete it locally:
```bash
git branch -d NXTB-15-front-bootstrap-next-js-app
```

- Delete it remotely:
```bash
git push origin --delete NXTB-15-front-bootstrap-next-js-app
```

---

## ✅ Summary

| Step | Action |
|------|--------|
| 1 | Create branch from `dev` or `work-dev` with ticket ID *(preferably from Jira)* |
| 2 | Commit and push with ticket reference (include `NXTB-XX` in messages) |
| 3 | Create a PR targeting `dev` or `work-dev` |
| 4 | Add ticket key in PR title or description (e.g. `Fixes NXTB-XX`) |
| 5 | PR opens → Jira ticket moves to "To Be Reviewed" automatically |
| 6 | Merge PR → Further transition to "Done" if automation is configured or commit includes `#done` |

--- 

