# GitHub Best Practices (Team Standard)

> This document defines how our team should use GitHub to keep code clean,
> reduce conflicts, and collaborate smoothly.

These practices are based on GitHub’s official recommendations and real-world
team experience.

---

## 1. Never Commit Directly to `main`

### Rule
- `main` branch must always be stable and deployable.
- No one pushes code directly to `main`.

### Why
- Prevents broken code in production
- Ensures review before merge
- Keeps history clean

### Correct Flow
```
main → feature branch → Pull Request → main
```

---

## 2. Use Meaningful Branch Names

### Branch Naming Format
```
feature/login-api
fix/null-pointer-in-invoice
```

### Why
- Easy to understand purpose
- Helps reviewers and future developers

---

## 3. Keep Commits Small and Focused

### Good Commit
- Solves one problem
- Easy to review
- Easy to revert

### Bad Commit
- Contains multiple features
- Mixes formatting, logic, and refactor

### Rule
> If a commit message needs **“and”**, split it.

---

## 4. Always Create a Pull Request (PR)

### What is a PR?
A request to merge your branch into `main`.

### PR Must Include
- What changed
- Why it changed
- How to test it

### Why PRs Are Important
- Code review catches bugs early
- Knowledge sharing
- Maintains code quality

---

## 5. Pull Latest Code Before You Start Work

### Before Creating a New Branch
```bash
git checkout main
git pull origin main
```

---

## 6. One Feature = One Pull Request

### Do
- One task per PR

### Don’t
- Mix multiple features or fixes in one PR

### Why
- Easier review
- Easier rollback
- Faster approvals

---

## 7. Do Not Commit Sensitive Files

### Never Commit
- `.env`
- API keys
- passwords
- private certificates

### Use
- `.gitignore`
- environment variables

### Why
- Security risk
- Can leak credentials publicly

---

## 8. Delete Branch After Merge

### After PR Is Merged
- Delete the feature branch

### Why
- Keeps repository clean
- Avoids confusion
