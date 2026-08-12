---
description: "Create a dev-1 branch on your own repo so the README shows v1 on main and v2 on dev-1, and demonstrate that the two do not affect each other by switching branches."
---

# Managing Your Parallel Universes with Branches

## 1. Goal

Understand what a Branch is and when to use one, then walk all the way through the branch flow on your own repo: commit v1 on main, create a new dev-1 branch, commit v2 on dev-1, and finally switch back and forth to see branch isolation with your own eyes. Once you finish this section, you will have the most essential branch operations in the GitHub web UI down.

---

## 2. What to Do

1. Read this section's README and understand what a Branch is and when you should use one.
2. On the main branch of your own repo, edit the README, add a v1 line, then Commit.
3. Create a new branch, dev-1, from main.
4. Switch to the dev-1 branch, change v1 to v2 in the README, then Commit.
5. Switch back to main and confirm the README still shows v1.
6. Switch to dev-1 again and confirm the README shows v2, experiencing the branch switch.

**Estimated time:** About 15 minutes

---

## 3. Checklist

- [ ] **Understand the Branch concept**: after reading the README, you can explain what a Branch is and its typical use cases.
- [ ] **Commit v1 on main**: the README on the main branch has a v1 line and has been Committed.
- [ ] **Created the dev-1 branch**: you can see and switch to dev-1 in the branch switcher.
- [ ] **Recognize the current branch**: at any moment you can tell which branch you are on from the branch switcher in the top left, along with how many branches the repo has in total.
- [ ] **Commit v2 on dev-1**: the README on the dev-1 branch shows v2 and has been Committed.
- [ ] **Verify branch isolation**: the README is still v1 when you switch back to main and v2 when you switch to dev-1, and you have experienced firsthand that the two branches do not affect each other.
