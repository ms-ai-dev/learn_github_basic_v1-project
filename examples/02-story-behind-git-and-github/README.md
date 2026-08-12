---
description: "By the end you can say what Git and GitHub each are, where each came from, how they relate, why GitHub can afford to let you use it for free, and why its work plus social design makes it a door-opener for your career and your portfolio even if you never write code."
---

# The Story Behind Git and GitHub: Two Origins, and a Stage That Is Not Just for Technical People

> This lesson has nothing to click. It covers the background: what Git and GitHub each are, where they came from, why GitHub gives you a place to keep your work for free, and why that place is not the exclusive property of programmers.

## 1. Overview

Every other lesson has you doing something: creating a repo, editing files, opening branches, inviting people, installing a desktop app. This one is different. It does not ask you to click a single button.

There are three reasons for that.

**First, you are about to use two things with confusingly similar names every single day: Git and GitHub.** Most people never sort out the difference, and still cannot explain it after years of use. That does not stop you from clicking buttons, but it does hurt your judgment: when something breaks you do not know what to blame, when you switch tools you do not know what you can take with you, and when the topic comes up you cannot follow the conversation.

**Second, GitHub is a company's product, yet it lets you store unlimited projects for free**, hosts your website for free, and lets you collaborate for free. That should strike you as slightly odd. Once you understand why it is so generous, you will know how far that generosity can be trusted and how far to lean on it.

**Third, and this is the one most people miss: you probably assume this is a place for programmers.** Open GitHub and it is code as far as the eye can see, so that impression is entirely natural. But it is the single biggest misconception this course wants to break. GitHub is built on work plus social, not code plus social, and a place that stores your work long-term and comes with a social layer attached works for anyone who wants to be seen for what they have done, whether or not they write code. That thread runs through this whole course, so let us establish it now.

So this lesson covers two origin stories, one balance sheet, and one position.

---

## 2. Learning Goals

Two awkward moments to start with.

The first: someone asks whether you know Git, and you say yes. They ask about GitHub, and you say yes again. Then they ask how the two relate, and you freeze. Or the reverse: someone tells you "we don't use GitHub here, we use GitLab," and your heart sinks because you assume you have to learn everything over again.

The second: you are not technical, someone suggests you "put your stuff on GitHub," and your first thought is "isn't that for programmers? would I even belong there?" So you keep your proposals in a local folder, your resume reaches its seventh revision still named resume-final-v3, and everything you have done over the years is visible to nobody but you.

Both kinds of hesitation come from the same gap: nobody told you what these two things are, or what this platform fundamentally is. Close that gap and every operation you learn afterwards lands on a clear map instead of being one more isolated button.

By the end of this Task, you will be able to:

1. Explain where Git came from and what problem it was built to solve.
2. Explain where GitHub came from and what it added on top of Git.
3. State the difference and the relationship in one sentence, and know what switching platforms would actually cost you.
4. Explain why GitHub can afford its free tier, and how to make good use of that generosity.
5. Explain why GitHub's work plus social design applies just as much to people who never write code, and why it works as a door-opener for your portfolio and your career.

---

## 3. Prerequisites

- A GitHub account you can log into (you can read this lesson without one, you just cannot do the exercises).
- A modern browser.
- No programming experience, and no prior knowledge of Git.

---

## 4. What You Will Build or Learn

This lesson produces no files. What you take away is context: where these two tools came from, what each one is responsible for, why it is worth keeping your long-term work on them, and why you have every right to stand on this stage. The concrete operations in later lessons become much easier to absorb once you have it.

---

## 5. The Story of Git: A Tool Forced Into Existence by a Falling Out

Before 2005, the Linux kernel was one of the largest open source projects in the world, with thousands of developers submitting changes. Managing that many people required a version control system, and the one they used was a commercial product called BitKeeper, whose vendor generously allowed the kernel community to use it for free.

In 2005 that goodwill ended. The vendor and the community fell out, and the free license was withdrawn. Overnight, the most important open source project in the world had no tool to manage its code.

The reaction of Linux's creator, Linus Torvalds, is telling: rather than shop for a replacement, he wrote one. Only a handful of days passed between starting and having the new tool manage its own source code. That tool was Git.

Three hard requirements shaped Git into what it is today:

- **It had to be fast.** The kernel codebase is enormous. If a single operation took half a minute, thousands of developers would be collectively wasting their lives every day.
- **It had to be distributed.** No single central server could be the authority. Every person's machine had to carry the complete history.
- **It had to resist tampering.** Anyone can submit to an open source project, so every change needed to be verifiable as untouched.

A note on the name. Linus has a self-deprecating streak; he says he names his projects after himself, and in British English "git" means an unpleasant person. A tool that reshaped an entire industry is named after its author insulting himself. A few months in he handed maintenance to Junio Hamano, who has maintained it ever since.

One detail in this story is worth holding onto: **Git only ever cared about text, and it has no idea whether what it manages is code.** All it sees is lines, and who changed which line when. That fact matters later.

---

## 6. What Git Actually Solved: Everyone Holds a Complete History

The mainstream tools before Git were centralized: a project's history lived on one central server, and your machine only held the current version of the files. Viewing history meant asking the server, creating a branch meant creating it on the server, and when the server went down everyone stopped working.

Git flipped that completely. When you clone a project, what you get is not the latest set of files but **the project's complete history since day one**. As a result:

- You can work offline. Committing, reading history, switching branches all happen locally, and you sync whenever you reconnect.
- Branches become extremely cheap. Creating one bothers no server and copies no code, so you can create them freely and throw them away just as freely.
- Backups happen for free. Every clone is a complete copy, so the more people involved, the harder the project is to erase.

You will feel all three later: the branch lesson has you open a branch to experiment, and the desktop lesson makes the line between "local" and "remote" concrete. Both trace back to this.

---

## 7. The Story of GitHub: Building a Public Square Around a Command Line Tool

Git is powerful, but it had a very practical problem: it is a command line tool, and it only manages the history on your own machine. Two people who want to work together have to get the repository onto a machine both can reach and configure the permissions themselves. In 2008, that was enough to put off almost everyone.

In 2008, a few developers (Tom Preston-Werner, Chris Wanstrath, PJ Hyett, and Scott Chacon) built a website called GitHub. What it did sounds unremarkable: it hosted your Git repositories online. But they did one more thing that genuinely changed the landscape: **they added a social layer**.

On GitHub a repository is not just a pile of files. It has a home page, a README as its front door, stars that signal other people's approval, forks that let others take a copy, issues for discussion, and people watching it. You get a profile page of your own too, showing everything you have made plus a full year of contribution history. You can follow someone, and someone can follow you.

Notice what that list actually consists of: a home page, a front door, approval, attention, discussion, a timeline. **None of it has anything to do with code; it is a design for showing work and being social**, and it just happened to serve people who wrote code first. That is what section 10 unpacks, so hold the thought.

The most important invention among these is the Pull Request. Note that a PR is not a Git feature; it is a product concept GitHub created. It took "I made some changes, would you take a look and merge them?", something that used to be handled through back and forth email, and turned it into a button anyone can use, with a discussion thread and a diff attached. Team collaboration worldwide now runs on that flow, and you will learn it in a later lesson.

That turned Git from a tool into a public square. Projects that used to be scattered across countless websites converged on one place where you could find a project, look at the work, and propose a change without leaving. In 2018 Microsoft bought GitHub for 7.5 billion dollars, and what that price bought was not the code but the fact that everyone was here.

---

## 8. Git Is Not GitHub, and That Is the Distinction Worth Keeping

Now the two can be placed side by side:

- **Git is a version control tool** that lives on your own machine. It is free, open source, and owned by no company. It records every change, manages branches, and merges content. It keeps working offline, and it would keep working even if every hosting site on earth shut down.
- **GitHub is a website that hosts Git repositories**, and it belongs to a company. It puts your repository online, gives it an address, controls who can read and write it, and adds PRs, issues, profile pages, stars, and contribution graphs, none of which Git itself has.

In one sentence: **Git manages the history; GitHub manages where that history lives, who gets to work around it, and how other people see it.**

GitHub is not the only site of its kind. GitLab, Bitbucket, and Codeberg are common alternatives, and the same Git runs underneath all of them. That leads to a reassuring conclusion: the project history you build up on GitHub is portable. As long as you have cloned it locally, you hold the complete history, and pushing it to another platform is all it takes. Nobody can lock you in.

So "we use GitLab instead of GitHub" implies far less relearning than it sounds. The mental model you build in this course, commit, branch, merge, and PR, holds on any of them. Only the position and color of the buttons change.

---

## 9. How GitHub Can Afford to Be This Generous

Now for that slightly odd balance sheet. Roughly speaking, a free account gets you:

- As many repositories as you want, public and private, with no cap.
- Collaborators on private repositories too, so you never have to make something public just to save money.
- A free automation allowance, so GitHub can run things for you after each push.
- Free static website hosting, so a repository can become a page anyone can visit.
- A full set of education benefits for students and teachers, plus extra consideration for open source maintainers.

The exact allowances change from year to year, so do not memorize them; check the official pricing page when you need to. The question worth thinking through is a different one: why would a company do this?

The answer is not charity. It is a carefully calculated bet:

- **People are the entry point.** If it works well for you personally, then once you join a company you are likely to recommend that the company buy the enterprise plan. The paying customer is the company, not you.
- **The crowd itself is the moat.** The world's projects are here, which is why you have to be here; and your being here makes it even harder for the next person to be anywhere else. A free tier is the cheapest way to keep that loop spinning.
- **Public content has value to the platform.** The public work you publish makes the square livelier and becomes material for other people to search and learn from. You are not just taking; you are contributing too.
- **There is a cloud business behind it.** Microsoft bought GitHub for the path that runs from making something to shipping it, and the end of that path is selling cloud services.

So the generosity is sustainable and you can rely on it. But precisely because it is a business rather than a promise, two boundaries are worth remembering: first, **do not treat GitHub as your only copy**, since a local clone or a mirror on another platform costs you almost nothing; second, **the rules of a free tier do change**, so lean on it with your eyes open.

---

## 10. This Stage Is Not Just for Technical People

Now back to the thread planted in section 1, which is what this lesson really wants you to leave with.

**First, let us admit where the impression comes from.** You open GitHub, the front page pushes open source projects, you click in and the screen is full of code, and the discussions are full of jargon. Concluding "this is a place for programmers" is completely reasonable. Plenty of non-technical people turn around right at that step.

**But take the platform apart and it gives you two things.**

One is **a place for your work to live**: a repo is the home of one piece of work, the README is its front door, and every revision leaves a timestamp and a note, so who changed what and when is perfectly clear. As section 5 said, Git only sees text and has no idea whether it is managing code. And the output of most professions, stripped to its core, is text: copy and campaign plans, research reports, lesson plans and slides, scripts and manuscripts, the conclusions of an analysis, product requirements, even a resume you keep revising.

The other is **a social layer that comes with the place**: your profile is your front door, stars are other people's approval, follows are ongoing attention, issues are public discussion, and the contribution graph is a timeline nobody can fake. Not one of those is exclusive to code.

**Put the two together and you get a door-opener.** When you want someone to believe you can do the work, what you lack is never adjectives, it is evidence. "Strong at event planning" on a resume is a claim you made about yourself; a public repo is something they can click into: which events you ran, how each version of the plan changed, what your retrospective said, and over what span of time. The first is a statement, the second is evidence. In an era where anyone can have AI generate polished phrasing, something a person can click into and inspect only grows in weight.

In many non-technical fields this is close to an unfair advantage: someone else hands over a PDF attachment, and you hand over a link containing both the work and the entire process that produced it. That is not you being better than them; it is you using a tool that is better at leaving evidence.

A few concrete shapes, to make it real:

- A marketer keeps one directory per campaign, with the plan, the asset list, the performance data, and the retrospective, and after a year that is a portfolio someone can page through.
- A teacher version-controls slides and lesson plans, sees exactly what changed each term, and takes the whole set along when changing schools.
- A writer keeps every draft, so when an editor asks where that one line from the previous version went, it takes seconds to find.
- A career changer keeps study notes and exercises in a public repository, so at an interview there is no need to argue about how hard they worked; the other person can just look at a year of records.

**Two honest caveats.** GitHub is best at text and how it evolves, not at large files. Video, high-resolution design files, and piles of raw assets can be uploaded, but it manages them poorly; those belong elsewhere, with a link and a note in the repo. And public has boundaries: an employer's internal material, client privacy, or a draft you are not ready to show should be private, and a later lesson covers that line in detail.

So the position of this lesson is clear: **you have every right to stand on this stage without becoming a programmer first.** As for actually moving your daily work here and turning it into a habit, lesson 07 walks you through it step by step.

---

## 11. How to Use This Free Stage

Bringing that balance sheet and that position down to your own situation, three things are worth deciding now.

**First, treat it as your default workspace, not the place you turn in assignments.** Since storage costs nothing, your notes, homework, proposals, resume drafts, and reading summaries can all live here. What matters is not which field you work in, but whether you need a record.

**Second, make public whatever can be public.** Public repositories consume none of your allowance and turn into a portfolio anyone can see. A stranger who wants to understand you can open your profile and see what you work on and for how long. That is the most valuable part of the free tier, and where the door-opener from the previous section actually takes effect.

**Third, be clear about what must never be public.** The flip side of generosity is that public content spreads fast and cannot be recalled. Passwords, keys, client material, and internal company documents belong in a private repository. The private repo lesson covers that line in depth.

---

## 12. Exercises

This lesson asks you to create and change nothing. All three exercises are about looking at something once and building a feel for it.

### Exercise 1: Retell the Origin of Git in One Sentence

**Goal:** Put the story into your own words instead of letting it slide past you.

**How to do it:**

1. Close this page.
2. In one sentence, tell yourself (or anyone nearby) who wrote Git, why, and what makes it distinctive.
3. Reopen this page, compare against sections 5 and 6, and see what you left out.

**What you will observe:**

Most people leave out "distributed" on the first try and only remember "Linus wrote it." Yet distribution is exactly what determines how the tool feels to use later.

> **Key insight:** You only know something once you can say it in your own words; the parts you cannot retell are the parts you did not really understand.

### Exercise 2: Go Look at What the Free Tier Actually Includes

**Goal:** Replace a vague sense of GitHub's generosity with a concrete one.

**How to do it:**

1. Open the Pricing page on github.com.
2. Read only the Free column, item by item.
3. Pick one thing you did not know you could use for free and write it down.

**What you will observe:**

The free tier includes far more than most people assume. Plenty of people have used GitHub for years and only ever used the "store my code" part.

> **Key insight:** Something free that you never learned about might as well not exist.

### Exercise 3: Find a Repository With Not a Single Line of Code

**Goal:** See for yourself that the people standing in this square are not only programmers.

**How to do it:**

1. Use the search box at the top of GitHub with a non-code keyword such as `awesome`, `handbook`, `notes`, `book`, or `curriculum`, then sort the results by stars.
2. Pick one, click in, and look at its README, its file list, its star count, and how many people have contributed.
3. Click the Pull requests tab, open one, and see how a single change gets discussed and merged.
4. Then open the profile of one of its contributors and take a look at their contribution graph.

**What you will observe:**

There are plenty of high-star repositories with no code in them at all: lists, handbooks, notes, tutorials, even whole books. And they use exactly the same presentation and collaboration flow as the code projects do.

> **Key insight:** This square rewards "you made something and left a record of it," not "what you made was code."

---

## 13. Recap: What We Learned

- Git was born in 2005, written by Linus Torvalds after the Linux kernel community lost the tool it depended on, with speed, distribution, and verifiability as its goals.
- Git's defining trait is that it is distributed: every clone carries the complete history, so you can work offline, branches are cheap, and backups happen naturally. And it only ever sees text, never caring whether that text is code.
- GitHub launched in 2008. It put Git repositories online and added profiles, stars, forks, issues, and contribution graphs, and the Pull Request is its invention rather than a Git feature.
- Git is the tool, free and open and owned by nobody; GitHub is a website hosting what the tool produces, owned by a company. GitLab, Bitbucket, and Codeberg are alternatives, and switching costs little relearning.
- GitHub's free tier is a calculated business decision: individuals are the entry point, companies pay, and the crowd itself is the moat.
- GitHub is built on work plus social, not code plus social. Your work gets a home, and that home comes with approval, attention, and a timeline nobody can fake, which is why it is a door-opener for people who never write code.
- Three ways to use it well: make it your default workspace, make public what can be public, but keep sensitive content private and never treat it as your only copy.

---

## 14. A Word From Your Mentor

**Why this lesson is worth reading:**

Everything after this is hands-on, and hands-on knowledge is the easiest to pick up and the easiest to forget. Two other things stay with you for years. One is judgment: knowing what is foundational and what is one company's product, and what travels with you across platforms. The other is a sense of entitlement, in the good sense: knowing whether you belong on this stage at all.

I want to stress the second one. I have met far too many non-technical people who produce real, substantial work every day, yet keep themselves outside the door because of one thought, "GitHub is for programmers." Years of their work ends up scattered across local folders and email attachments, and when the moment comes to show something, there is nothing presentable to show. That is not a capability problem, it is an admission-ticket problem, and the ticket was free all along.

**Key insights:**

- Telling a "tool" from a "platform" is where technical judgment starts. Git is the tool, GitHub is the platform, and the same distinction holds in other fields.
- Free things are not without cost; the cost is simply paid by someone else. Once you know who pays, you know how long the free part can last.
- The best backup a project has is not one website's promise but the complete copies scattered across many people's machines. That was one of Git's original design goals.
- People believe you based on what you can hand them to inspect, not on how you describe yourself. Putting your work somewhere public, timestamped, and clickable is the cheapest form of proof there is.

**Next step:**

Carry these two stories and this position forward. In the next lesson you create your first repo, and by then you will know what you are actually doing: using a tool written in 2005 out of necessity to stake out a small piece of a square that was built in 2008, and that piece is meant to be seen.

---

## 15. Quick Reference

**Git:** A distributed version control tool written by Linus Torvalds in 2005. Free, open source, runs locally, manages change history, and only ever sees text.

**GitHub:** A Git repository hosting site launched in 2008, acquired by Microsoft in 2018 for 7.5 billion dollars. It manages where a repository lives, who can read and write it, and how other people see it.

**One-sentence distinction:** Git manages the history; GitHub manages where that history lives, who works on it with you, and how others see it.

**Pull Request:** A GitHub invention, not a Git feature. Covered in a later lesson.

**Alternative platforms:** GitLab, Bitbucket, Codeberg. The same Git underneath, so switching requires little relearning.

**Roughly what the free tier gives you:** Unlimited public and private repositories, collaborators on private repos, an automation allowance, static website hosting, and student and teacher benefits. The exact numbers change yearly; check the Pricing page when you need them.

**Why it is a door-opener:** A repo holds the work, the README is its front door, stars and follows are social proof, and the contribution graph is a timeline nobody can fake. None of that is field-specific, as long as your output can land as text.

**Two boundaries:** Never treat GitHub as your only copy (a local clone is a complete backup); keep sensitive content private, and put large files and raw assets elsewhere with a link.
