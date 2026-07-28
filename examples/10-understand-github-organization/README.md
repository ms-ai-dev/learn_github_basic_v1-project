---
description: "See that every repo on GitHub sits under an owner, tell a personal account from an Organization, find the exact repository someone shared with you inside an organization, and understand that creating a repo is the same choice of owner."
---

# Who a Repo Belongs To: Personal Accounts and GitHub Organizations

> Work out who a repo actually belongs to, and why a repository someone shared with you never turns up in your own list no matter how long you scroll.

## 1. Overview

This is lesson ten of the "Learn GitHub Basics" series. Let's start with a scene almost everyone runs into once.

Someone tells you the repository has been shared with you, go take a look. You log in to GitHub, open your Repositories, scroll from top to bottom, and it is not there. You refresh, still nothing. You start wondering whether they got it wrong, or whether the permissions were never granted.

In all likelihood nothing went wrong. That repository does exist, and you do have access, it is just not under your name but under an organization's name. Of course you cannot find it: you are searching your own room for something kept in a cabinet at the office.

This lesson makes that clear once and for all. Every repo on GitHub belongs to exactly one owner, and that owner can be a person or an organization. Once you see this, you will stop spending time looking in the wrong place.

---

## 2. Learning Objectives

For the first nine lessons, everything you touched was a repo you created yourself, so it naturally sat under your own name and the question of ownership never came up. But the moment you start dealing with other people, whether you join a company, join a team, or get pulled into a project, most of the repositories you touch are no longer ones you built. From then on "who does this repository belong to" becomes a daily question.

What this lesson gives you is not an operation but an instinct: whenever you are handed a repository, look at its owner first. With that instinct, "I cannot find the repo" stops being a problem that holds you up.

After finishing this Task, you will be able to:

1. Explain that a repo's full coordinate is its owner plus its name, and read the owner straight off a URL.
2. Explain in your own words what an Organization is and how it relates to a personal account.
3. Know which organizations you belong to, and find a specific repository inside one of them.
4. Understand that when you create a repo yourself, you are making the same choice of owner.

---

## 3. Prerequisites

- Lessons 01 through 09 of this course finished, so you can create a repo and have used GitHub Desktop.
- A GitHub account you can log in to.
- GitHub Desktop installed and signed in (the last observation in this lesson uses it, but you can follow the reading without it).

---

## 4. What You Will Build or Learn

This lesson produces nothing new and asks you to build nothing. What you take away is a piece of judgment: when you see a repository, you know who it belongs to; when you cannot find one, you know where to look; and when you create one, you know whose name it will land under.

---

## 5. A Repo's Full Coordinate Is Owner Plus Name

Let's start with the most visible place: the address bar.

Every GitHub repository URL looks like this: `github.com/OWNER/REPO`. Take `github.com/john-doe/my-notes`, where `john-doe` is the owner and `my-notes` is the repository name.

Here is the key part: the repository name by itself is not unique. There may be thousands of repositories called `my-notes` across GitHub, all unrelated, each belonging to a different owner. What is actually unique is the pair of owner and name, which is to say the full URL.

So when someone tells you a repository name, the name alone is not enough. Either ask who the owner is, or just have them send you the full URL. That is the simplest approach and the one least likely to go wrong.

---

## 6. An Organization Is Really Just an Account

So what exactly is the owner in that URL? The answer is simpler than you might expect: it is an account.

Two kinds of accounts on GitHub can own repositories. One is a personal account, the kind you got when you registered, with a specific human being behind it. The other is called an Organization, and behind it is not a person but a company, a team, or an open source project. From GitHub's point of view, though, the two are the same kind of thing: both are accounts, both have a globally unique name, both can own repositories, and both can appear in that owner segment of a URL.

In other words, when you see `github.com/some-company/some-repo`, you cannot tell from the URL alone whether `some-company` is a person or an organization, because structurally they sit in exactly the same position. Click through and you will know.

Why does this second kind of account exist? Because plenty of things should not belong to any one individual. A company's projects sit under an organization, people come and go, and the repositories stay put; if they sat under one employee's personal account, that person leaving would be a real problem. Open source projects work the same way: under an organization's name, anyone can take over maintenance.

As for how an organization manages people internally and groups them, that is a separate set of machinery this lesson does not touch at all. For now, all you need is this: it is an account that can own repositories.

---

## 7. Repos You Created Are Only Under Your Own Name

Back to that confusion about not finding a repository, which we can now explain.

Repositories you created have you as the owner, so they all sit under your personal account, in the place lesson 01 showed you in "Finding Your Repo Again": click your avatar in the top right and choose Repositories, or go straight to `github.com/USERNAME?tab=repositories`.

That list is nice and clean, but it comes with a boundary that is easy to miss: **it only shows repositories under your own name**. Anything shared with you, anything under an organization, none of it is here.

So when you cannot find a repository in this list, your first thought should not be "they never gave me access" but "maybe it was never under my name to begin with." Nine times out of ten it is the latter.

---

## 8. Finding Out Which Organizations You Are In

Since a repository may sit under an organization, the next question is: which organizations do I actually belong to?

Click your avatar in the top right and you will find an Organizations item in the menu. Click it and you get a list of every organization you have joined.

![The Organizations entry in the avatar menu, and the page listing every organization you have joined](img/10-understand-github-organization-01.png)

This list is worth a dedicated look right after you start a new job or join a new team. It effectively tells you where else you can go looking, beyond your own patch.

If the list is empty, you currently belong to no organization, which is perfectly normal. Accounts still in the learning stage almost always look like that.

---

## 9. Finding That Repository Inside an Organization

Once you know which organization you are in, there is a path to the repository: click into that organization, then click the Repositories tab at the top.

![An organization's Repositories page, with a search box at the top and filters on the left for Public, Private, and more](img/10-understand-github-organization-02.png)

Look at the number in this screenshot: this organization has 140 repositories. Several hundred is common at a real company, and scrolling will not get you there, so always use the search box on that page. The column on the left also lets you narrow things down to just the public ones, just the private ones, or just the ones you have contributed to, which helps a lot.

While you are at it, note the address of this page: `github.com/orgs/ORG_NAME/repositories`. If you know the organization's name, you can type the address directly.

---

## 10. Being Able to Open a Repo Does Not Mean You Joined the Organization

There is a detail here that causes real confusion when it goes unexplained.

"Having access to one repository" and "having joined an organization" are two different things. Someone can add you as a collaborator on a single repository (exactly what lesson 07 covered) without pulling you into the organization at all. That produces a situation that looks contradictory: you can open that repository's URL and read its contents, yet you cannot find that organization in your Organizations list, let alone browse its repository list. You really are not inside it. You were simply handed the key to one door.

In that case the full URL is your only reliable way in. Which brings us back to what section 5 said: have people send you the full URL, not just a repository name. That one habit saves a great deal of back and forth.

---

## 11. The Other Direction: You Choose an Owner Too

Everything so far has been about finding other people's repositories. Now flip it around: when you create a repository, you are making the same choice, you just never noticed.

The creation page in lesson 01 had an Owner dropdown, and back then your account probably had only one option, so you clicked past it. Once you join an organization, that dropdown gains a few more options, and you have to think about whose name this repository should land under.

In GitHub Desktop the whole thing is split into two steps, which actually makes it clearer. First, choose New Repository from the File menu.

![GitHub Desktop's File menu, with New Repository as the first item](img/10-understand-github-organization-03.png)

Second, in the dialog that opens, fill in a name, pick a local path, optionally check README and choose a Git Ignore and a License, then click Create Repository.

![The Create a New Repository dialog: fill in Name, pick a Local Path, check the option to initialize with a README, then click Create Repository](img/10-understand-github-organization-04.png)

Notice that up to this point the repository lives entirely on your own machine and there is nothing on GitHub at all. This is exactly the local and remote boundary lesson 09 described.

The third step is the important one. Click Publish repository at the top, and in the window that opens, alongside the name and "Keep this code private," there is an Organization dropdown.

![The Publish Repository window: besides Name and Keep this code private, there is an Organization dropdown, defaulting to None, which when expanded lists every organization you belong to](img/10-understand-github-organization-05.png)

That dropdown defaults to None, meaning publish under your own name. Expand it and every organization you belong to is listed. Whichever you pick becomes this repository's owner, and that segment of the URL is settled along with it.

Here is a small trick for thinking about it: treat your personal account as a special organization that happens to have exactly one member and cannot take on any more. Seen that way, choosing None and choosing an organization are the same act, picking a home for this repository.

Make that choice before you publish, because it decides who owns the repository from then on, who can see it, and where other people have to go to find it.

---

## 12. Exercises

This lesson does not need you to create or change anything. All three exercises are just opening something and taking a look, which is enough to build the instinct.

### Exercise 1: Read a Repository's Owner

**Goal:** Build the habit of looking at the owner.

**What to do:**

1. Open any repo of your own, look at the address bar, and say out loud who that segment after `github.com/` is.
2. Open any well known open source project you can think of, and read its owner segment the same way.
3. Click that owner's name to visit their page, and see whether it is a person or an organization.

**What you will observe:**

A personal account's page has an avatar and a contribution graph; an organization's page has tabs like Repositories, People, and Teams. Structurally the owner sits in exactly the same position, but one click tells you which kind it is.

> **Key insight:** Repository names are not unique, but owner plus name is. Remembering the address beats remembering the name.

### Exercise 2: See Which Organizations You Are In

**Goal:** Know where else you can go looking, beyond your own name.

**What to do:**

1. Click your avatar in the top right, choose Organizations, and see what is in the list.
2. If there is anything, click into one, then click the Repositories tab at the top and try searching for a keyword.
3. If the list is empty, keep this page in mind and come straight back to it when you join a company or a team.

**What you will observe:**

An organization's repository list and your own are two completely separate lists. That also explains exactly why scrolling your own list never turns up something someone shared with you.

> **Key insight:** When you cannot find a repository, first ask whether you are looking in the wrong place.

### Exercise 3: Take a Look at the Organization Dropdown When Publishing

**Goal:** See with your own eyes what "choosing an owner" looks like.

**What to do:**

1. Open GitHub Desktop, choose New Repository from the File menu, give it any name (say `my-example-repo`), pick a local path, and click Create Repository.
2. Click Publish repository at the top.
3. In the window that opens, expand the Organization dropdown and look at the options.
4. Close the window when you are done. There is no need to actually publish, and you can delete that local folder whenever you like.

**What you will observe:**

The dropdown defaults to None (publish under your own name), with every organization you belong to listed below it. If you belong to none, None is the only entry, which is also normal and means every repository you create right now lands under your own name.

> **Key insight:** Every repository has an owner from the moment it is born. That is not optional; sometimes you just have no alternative to choose from.

---

## 13. Recap: What We Learned

- A repo's full coordinate is owner plus name, the URL `github.com/OWNER/REPO`. The name by itself is not unique.
- The owner is an account. A personal account has a person behind it and an Organization has a company or team behind it, but both can own repositories and both sit in the same place in a URL.
- The list of repositories under your own name only shows your own. Anything shared with you will not appear there, which is the most common reason a repository seems missing.
- To see which organizations you are in, use Organizations in the avatar menu; to find a repository inside one, open the organization's Repositories tab and use the search box.
- Being able to open a repository does not mean you joined that organization, since you may only be a collaborator on that one repo. In that case the full URL is your only reliable way in.
- When you create a repo you are choosing an owner too. In the browser it is the Owner dropdown; in GitHub Desktop it is the Organization dropdown when you publish.

---

## 14. A Word from Your Mentor

**Why this matters:**

This lesson taught you no new operations, but it clears up a snag that happens all the time in real work. Someone without the concept of an owner in their head keeps hitting the same frustration: you said you gave it to me, so why can I not find it? Once the instinct is there, that same situation takes you ten seconds. Ask for the full URL, or search inside the organization, done.

**Key insights:**

- There are no free-floating repositories on GitHub; every one of them hangs off some account. Think owner first, repository second, and you will not get lost.
- The difference between a personal account and an organization comes down to belonging. What belongs to a person goes with that person, and what belongs to an organization stays with the organization. That is exactly why company projects are never built under an employee's personal account.
- When passing along repository information, a full URL always beats a repository name. It is a tiny habit that saves a lot of communication overhead.

**Next step:**

From today on, glance at the owner in the address bar every time you are handed a repository. When you join a new team, the first thing to do is check Organizations to see which ones you were added to, then skim their repository lists. Those two moves take under two minutes and give you a clear picture of what you can reach.

---

## 15. Quick Reference

**A repository's full coordinate:** `github.com/OWNER/REPO`. The owner may be a personal account or an organization.

**Finding your own repositories:** Repositories in the avatar menu, or `github.com/USERNAME?tab=repositories`. Only shows what is under your own name.

**Seeing which organizations you are in:** Organizations in the avatar menu.

**Finding repositories in an organization:** `github.com/orgs/ORG_NAME/repositories`, using the search box on the page rather than scrolling.

**Choosing an owner when creating:** In the browser it is the Owner dropdown on the creation page; in GitHub Desktop it is the Organization dropdown in the Publish repository window, where None means under your own name.

**One line to remember:** If you cannot find a repository, check the owner. If it is not under your name, go look inside the organization.
