---
description: "By the end you can use a Pull Request to merge the v2 work from the dev-1 branch back into main, and understand the concepts of Merge, PR, and Conflict."
---

# Pull Request: Merging Branch Work Back Into the Main Line

> This lesson teaches you how to use a Pull Request to officially merge the work you finished on the dev-1 branch in the previous lesson back into the main branch.

## 1. Overview

In the previous lesson (03 Working with Git Branch), you added v1 to main in your own repo, then created the dev-1 branch and changed its content to v2. The work on dev-1 is now done and it turned out well, so it is time to merge it back into main. Parallel universes cannot stay parallel forever. Work produced on a branch has to be integrated into the main line before it counts as an official part of the project. This lesson walks you through that whole process, using a Pull Request on GitHub to merge dev-1 back into main.

---

## 2. Learning Objectives

In the previous lesson you learned to create a Branch and work comfortably on an isolated line without touching main. But the value of a branch is not in staying isolated forever. It is in eventually folding the work back into the main line. If finished work stays on a branch indefinitely, it never becomes an official part of the project and nobody else can use it. Merge is the action that solves this: it applies the verified changes from a branch back to the main branch. On GitHub, we start and complete this merge through a Pull Request (PR for short). A Pull Request literally means "a request to pull", and you can think of it as one sentence: I finished some work, please merge the result into the main branch.

By the end of this Task, you will be able to:

1. Explain in your own words what Merge and Pull Request each are, and how they relate.
2. Read the merge direction of a PR: tell the source (compare) from the target (base), and confirm at a glance which way the changes flow.
3. Create a Pull Request for the dev-1 branch in your own repo, with a good title and description.
4. Complete the merge, fold the v2 changes from dev-1 into main, and verify the result.
5. Understand what a Conflict is, and why you will not run into one in this lesson's exercise.

---

## 3. Prerequisites

- You have completed the previous lesson (03 Working with Git Branch): you added v1 to main in your own repo, created the dev-1 branch, and changed its content to v2.
- You can sign in to your GitHub account in a browser and switch branches inside a repo.

---

## 4. What You Will Build or Learn

You will merge the changes on the dev-1 branch back into main through a Pull Request, in your own repo. When you are done, the README on the main branch will go from v1 to v2, and the two parallel branches become one. You will also end up with a complete merge record: a PR with a title and description, one Merge, and the updated content on main. This is your first branch merge completed on GitHub.

---

## 5. What Is Merge

Let's continue with the blog example. You tried a new writing style on a branch called try-new-style, spent several days on it, and it turned out great. Now you want to apply this new-style version to main. That process of "applying" is Merge.

Technically, Merge does three things:

1. Find the differences: compare the two Branches and see what is different between them.
2. Package the changes: bundle together all the changes you made on one Branch.
3. Apply the changes: apply that bundle of changes onto the target Branch.

Put simply, Merge is moving the work from one branch over to another.

---

## 6. What Is a Pull Request

A Pull Request is how you start a Merge on GitHub. A standard PR flow looks like this:

1. You finish your work on your own branch.
2. You create a PR that explains what you did and requests to merge the result into the main branch.
3. On a team, other people review your code and offer feedback.
4. Once everything looks good, you click the Merge button to officially complete the merge.

In this lesson's exercise, because it is your own repository, you do both the review and the merge yourself. But the flow itself is the same as team collaboration. Understand the flow now, and it will feel familiar when you join a team later.

Here is one concept to burn into your memory: a merge always has a direction. Every Pull Request involves two branches, one is the source (where the changes come from, which GitHub calls compare in a PR) and one is the target (where the changes get merged into, which GitHub calls base). The top of the PR page spells out which way the merge goes, in a form like "base: <target> merged from compare: <source>". With any PR, the first thing you should fix your eyes on is this direction, to confirm it is not reversed. The most common pattern is this: a branch with a specific name (like dev-1, alice-login, feature-search) merges into a branch with a standard name (usually just main). In other words, changes always flow from a specific feature branch toward the standard main line. Once the direction is reversed, you would be merging main's content into the feature branch, which is usually not what you want. The merge you are doing in this lesson goes from dev-1 (source) to main (target).

---

## 7. A Complete Workflow

Putting Commit, Branch, and Merge together, a typical feature-development flow looks like this:

- Starting point: main has only Commit 1, whose content is "initial project files".
- Branch off: from Commit 1, split off a feature-search branch to develop the search feature.
- Commit repeatedly on the branch: on feature-search, do Commit 2 "add search box", Commit 3 "implement search logic", Commit 4 "polish search feature" in order. During this time, main stays at Commit 1 and does not move.
- Merge back to the main line: once the feature is done, merge feature-search back into main. This produces a Merge commit that contains all the changes from Commits 2, 3, and 4. Now main has the complete search feature too.
- Wrap up: feature-search has served its purpose and can be deleted.

What you are doing in this lesson is exactly the "merge back to the main line" step of this flow: merging dev-1 back into main.

---

## 8. Hands-On Step 1: Create the Pull Request

First make sure you are currently on the dev-1 branch. If you are not sure, confirm it with the branch switcher on the page.

Open the repo page. If you just made changes on dev-1, a yellow banner appears near the top of the page with text like "dev-1 had recent pushes X seconds ago", next to a green "Compare & pull request" button. Click it to go straight to the page for creating a PR.

![Yellow banner and the Compare and pull request button](img/04-merge-branch-1.jpeg)

If you do not see this yellow banner, no problem. You can click the "Pull requests" tab at the top of the repository, then click the green "New pull request" button and manually choose the branches to merge.

---

## 9. Hands-On Step 2: Fill In the PR Information

Once you reach the creation page, the page title is "Open a pull request". There are a few things to look at closely here.

**Comparison info**: near the top, the page shows the merge direction, in a form like base: main merged from compare: dev-1. Matching this against the direction concept from the previous section, here the target is main and the source is dev-1, so the direction is correct: you are merging dev-1's changes into main. If there is a green check and the words "Able to merge" next to it, that means this merge can complete automatically with no conflicts.

**Title (Add a title)**: GitHub defaults to using the message of your last Commit as the title, for example "Update README.md". You can keep the default or change it to something more descriptive.

**Description (Add a description)**: here you can explain what this PR actually does. For a simple exercise you can leave it blank, or write a line, for example "Update the version from v1 to v2".

**Change preview**: the bottom of the page shows all the changes this PR includes. You will see `- v1` on a red background meaning a deletion, and `+ v2` on a green background meaning an addition. This lets you clearly see what will happen after the merge, before you merge.

![Open a pull request page, showing the comparison info and the change preview](img/04-merge-branch-2.jpeg)

Once everything looks right, click the green "Create pull request" button.

---

## 10. Hands-On Step 3: Merge the PR

After it is created successfully, the page jumps to the detail page for this PR. The title looks like "Update README.md #1", where #1 means this is the first PR in your repository.

You will see a green "Open" label, meaning the PR is waiting to be handled. Below it are "No conflicts with base branch" and "Merging can be performed automatically", indicating it is safe to merge automatically. Further down is a big green "Merge pull request" button, and beneath the button is an "Add a comment" area where you can leave a comment; this step is optional.

![The Merge pull request button on the PR detail page](img/04-merge-branch-3.jpeg)

Do the merge: click the green "Merge pull request", the button changes to "Confirm merge", and click it once more to confirm.

Merge complete! You will see a purple "Merged" label, and the page shows how many commits this merge brought into main. A "Delete branch" button also appears. You can click it to delete the now-merged dev-1 branch and keep the repository tidy. Deleting the branch will not lose any data, because the changes are already in main.

---

## 11. Hands-On Step 4: Verify the Merge Result

The merge is done, and the final step is to confirm the work really made it into main.

1. Click the repository name to go back to the repo home page.
2. Confirm you are on the main branch (the branch switcher shows main).
3. Look at the content of the README.

The README should now show v2. That means the changes from dev-1 have been successfully merged into main, and the two parallel universes have become one.

---

## 12. About Conflict

What happens at merge time if two people change the same line of the same file? That produces a Conflict.

**When it happens**: for example, in branch-A you change a line to "Hello World", and your teammate changes the same line to "Hi World" in branch-B. Both of you want to merge into main, and Git gets stuck, because it does not know which version to use. GitHub then flags a conflict and cannot merge automatically.

**How to resolve it**: GitHub pops up a text editing box and lets you decide manually which version to keep, or keep both, or write an entirely new version. Conflict resolution has many details, which we will not go into here. For now you only need to remember three things:

- Conflicts are normal; they are not errors.
- When Git cannot decide automatically, it asks a human to decide.
- In most cases, if people change different files or different lines, there will be no conflict.

In this lesson's exercise, you are the only one working, so you will not run into a conflict.

---

## 13. Recap: What We Learned

- Merge applies the changes from one branch to another, doing three things: find the differences, package the changes, apply the changes.
- A merge has a direction: from source (compare) to target (base), which the top of the PR spells out; the common pattern is a specific feature branch merging into the standard main.
- A Pull Request is how you start a merge on GitHub, and the flow is create, review, Merge, delete branch.
- You did the hands-on part: created a PR for dev-1, filled in a title and description, merged, and verified that the README on main became v2.
- You understand that a Conflict is caused by different edits to the same spot, needs a human to decide, and will not happen when you work alone.

---

## 14. A Note From Your Mentor

**Why this exercise matters:**

At this point, you have mastered Git's complete core workflow: Commit, Branch, Merge. These three actions are the skeleton of Git, and almost all collaboration is built on top of them. Picture a team of 10, where each person works on their own branch, submits it for review through a PR when done, others read it and offer suggestions, and after it passes it gets merged into main. It is exactly this flow that keeps complex collaboration orderly.

**Key insights:**

- A Pull Request is not just a technical operation. It is the vehicle for code review (teammates can leave comments in the PR to point out problems), a window for knowledge sharing (you learn a lot by reviewing other people's PRs), and a gate for quality assurance (many teams require a PR to be reviewed before it can be merged). So learning to write a clear PR, with a good title, a clear description, and a reasonable change scope, is an important professional skill.
- Merge often, stay in sync. Do not let a branch live on its own for too long, or its difference from main keeps growing and you end up with a pile of conflicts at merge time. A better practice is to frequently sync main's updates into your working branch, and merge back into main every time you finish a small piece. Small, quick steps are far more efficient than saving up for one big push.

**Next step:**

On real projects, build the habit of submitting your work through a PR, even if you are the only one. Every PR is a clear record of a stretch of work, and your future self will thank the present you for writing careful descriptions.

---

## 15. Quick Reference

**The full flow to create and merge a PR:** confirm you are on the dev-1 branch, click "Compare & pull request" in the yellow banner, fill in a title and description then click "Create pull request", on the detail page click "Merge pull request" then "Confirm merge", and finally switch back to main to confirm the README became v2.

**Key concepts:**

- Merge: merging branches, applying the changes from one branch to another.
- Merge direction: from source (compare) to target (base), confirmed by the base-from-compare line at the top of the PR; usually a feature branch to main.
- Pull Request: a request to merge, started and completed on GitHub.
- Conflict: different edits to the same spot, which a human must resolve by deciding which to keep.

**Key files:**

- `README.md`: the target file merged in this lesson; after the merge it shows v2 on main.

---

## 16. Reference Implementation

There is no code to run in this lesson. The reference result is simply this: your repo has a merged PR (with a purple Merged label), the README on the main branch shows v2, and all the changes from dev-1 have made it into main.
