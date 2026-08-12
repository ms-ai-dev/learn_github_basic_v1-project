---
description: "Create and merge a Pull Request for dev-1 in your own repo, so the README on main goes from v1 to v2."
---

# Use a Pull Request to Merge Your Branch Back Into main

## 1. Goal

In the previous lesson, you changed the README to v2 on the dev-1 branch. In this lesson you will officially merge that work back into main. You will first understand the concepts of Merge and Pull Request, then create a PR for dev-1, complete the merge, and finally switch back to main to confirm the change took effect. When you are done, the two parallel branches become one and the README on main shows v2.

---

## 2. What to Do

1. Read this lesson's README to understand what Merge and Pull Request are, and the complete flow of a PR from creation to merge.
2. Confirm you completed the previous lesson: the README content on the dev-1 branch is v2.
3. On the dev-1 branch page, click "Compare & pull request" in the yellow banner at the top (if you do not see it, create one manually with "New pull request" under the "Pull requests" tab).
4. Fill in the PR's title and description, confirm the comparison direction is merging from dev-1 to main and shows "Able to merge", then click "Create pull request".
5. On the PR detail page, click "Merge pull request", then click "Confirm merge" to complete the merge.
6. Switch back to the main branch and confirm the README now shows v2.
7. (Optional) Click "Delete branch" to delete the now-merged dev-1 and keep the repository tidy.

**Estimated time:** About 15 minutes

---

## 3. Checklist

- [ ] **Understand Merge and PR**: you can explain in your own words what Merge is, what a Pull Request is, and roughly what a Conflict is about.
- [ ] **Read the merge direction**: on the PR page you can recognize that the base (target) is main and the compare (source) is dev-1, and confirm the change direction is from dev-1 to main.
- [ ] **Create the PR successfully**: you created a Pull Request for dev-1, with a clear title and description.
- [ ] **Merge successfully**: you completed the merge and the page shows a purple "Merged" label.
- [ ] **Verify the result on main**: after switching back to the main branch, the README now shows v2.
- [ ] **Understand the Conflict concept**: you understand that a conflict is caused by different edits to the same spot, needs a human to resolve, and will not happen when you work alone.
