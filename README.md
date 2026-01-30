# GitHub Best Practices (Team Standard)

> This document defines how our team should use GitHub to keep code clean,
> reduce conflicts, and collaborate smoothly.

These practices are based on GitHub’s official recommendations and real-world
team experience.

---

## 1. Never Commit Directly to `main`

  **Rule**
  - `main` branch must always be stable and deployable.
  - No one pushes code directly to `main`.
  
  **Why**
  - Prevents broken code in production
  - Ensures review before merge
  - Keeps history clean
  
  **Correct flow**
  main → feature branch → Pull Request → main

## 2. Use Meaningful Branch Names

  **Branch naming format**
  feature/login-api
  fix/null-pointer-in-invoice
  
  
  **Why**
  - Easy to understand purpose
  - Helps reviewers and future developers

---

## 3. Keep Commits Small and Focused

  **Good commit**
  - Solves one problem
  - Easy to review
  - Easy to revert
  
  **Bad commit**
  - Contains multiple features
  - Mixes formatting + logic + refactor
  
  **Rule**
  > If a commit message needs “and”, split it.

## 4. Always Create a Pull Request (PR)

  **What is a PR?**
  A request to merge your branch into `main`.
  
  **PR must include**
  - What changed
  - Why it changed
  - How to test it
  
  **Why PRs are important**
  - Code review catches bugs early
  - Knowledge sharing
  - Maintains code quality


## 5. Pull Latest Code Before You Start Work

  **Before creating a new branch**
  git checkout main
  git pull origin main


## 6. Do Not Commit Sensitive Files

  Never commit
    .env
    API keys
    passwords
    private certificates

  Use
    .gitignore
    environment variables

  Why
    Security risk
    Can leak credentials publicly


## 7. Delete Branch After Merge
  After PR is merged:
    Delete the feature branch
  
  Why
    Keeps repository clean
    Avoids confusion
