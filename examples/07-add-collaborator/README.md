---
description: "Invite a collaborator into your repo on your own, understand the difference between default read/write access and finer-grained permissions, learn to invite people (and get invited) using an exact GitHub username, and never forget that without an invite there is no collaboration."
---

# Inviting a Collaborator: Letting Others Into Your Repo

> Learn how to invite a classmate, teacher, or coworker into your repo so they can genuinely work on the project alongside you.

## 1. Overview

This is the seventh lesson in the "Learn GitHub Basics" series, and it picks up right where lesson 06 left off. In lesson 06 you learned about the Private Repository, a repo that only you can see. That is great, but it immediately raises a very practical question: if nobody but me can see it, what do I do when a classmate, a teacher, or a coworker needs access to the project?

The answer is the star of this lesson: the collaborator. You can invite specific people in one at a time so they can work in the repo alongside you, while to everyone else the repo stays invisible. In other words, a collaborator is how you draw a precise circle somewhere between "just me" and "the whole world."

---

## 2. Learning Goals

Picture a concrete scenario. You set your course project to private, nice and safe. Now it is time to turn in your assignment, and your teacher needs to open your project to grade it. Or you and a classmate are working on a group project and both need to edit the same files in the same repo. But when they open your repo URL, all they see is a 404 (remember the incognito-window experiment from lesson 06?). To anyone without access, your private repo simply does not exist.

The only way in is for you to actively invite them as a collaborator. Once you learn this, you have truly connected two things that look contradictory but must coexist: privacy and collaboration. This is something every real team does every single day.

By the end of this task, you will be able to:

1. Explain in your own words what a collaborator is and what permissions they get by default once added.
2. Independently complete the full process of inviting someone into your own repo.
3. Understand why the GitHub username matters: to invite someone you need their exact username, and to get invited you need to give others your exact username.
4. Firmly remember one bottom line: without an invite, no one else can collaborate.

---

## 3. Prerequisites

- You have completed lessons 01 through 06 of this course, especially 06, so you know how to create a Private Repository.
- You have a repo of your own on hand (private or public both work; we recommend practicing on the private repo you created in lesson 06).
- Optional: if you can, find a classmate or friend who is willing to help out (someone with their own GitHub account) so you can actually send a real invite and get a more authentic feel for it.

---

## 4. What You Will Build or Learn

After this lesson, you will have personally invited a real person into your repo, and you will know clearly what they can and cannot do once they are in. More importantly, you will build a basic mental model for collaboration: access is not open by default; you grant it deliberately, one person at a time.

---

## 5. What Is a Collaborator

A collaborator is a person you have authorized to access one specific repo.

Once you add someone as a collaborator to a personal repo, they get two things by default at the same time:

- Read permission: they can view everything in the repo, files, history, branches, all of it.
- Write permission: they can directly edit files, create branches, and make commits.

Pay special attention to that second point. A collaborator's default permission is not "view only," it is "edit too." That means once you add someone, they can essentially work in the project just like you do. That is not a bad thing, since collaboration inherently requires the other person to be able to make changes, but keep this clear in your mind: adding a collaborator is like handing over a key that can change your project. So only invite people you truly trust.

---

## 6. The Default Is Read/Write, and Enterprise Setups Have Finer-Grained Permissions

The "default read/write" described above is the most common case for a personal repo. But in more formal, larger-scale collaboration (for example, managing an entire team through a GitHub Organization), adding members actually comes with a whole set of finer-grained permission tiers, letting you control exactly how far each person can go. A couple of examples will give you the idea:

- Some tiers can view but not edit, which suits an outside reviewer or an intern who is just observing.
- Some tiers can edit code but cannot change the repo's settings, and this one is especially important. Think about it: if anyone could touch the settings, then one slip of the hand could flip your private repo to public (lesson 06 covered how that is irreversible), and that would be a disaster. Separating "change content" from "change settings" exists precisely to prevent this.

We will not go deep into these advanced configurations here; just know they exist. For the personal-project scenario in this course, one sentence is enough: the collaborator you add can, by default, both read and write.

---

## 7. First, Get One Thing Straight: What Is a GitHub Username

Before you start inviting people, there is one concept you must nail down, or you may well add the wrong person: the GitHub username.

Your username is the globally unique identifier you chose when you registered on GitHub, and it shows up right in your profile address, in the form github.com/your-username. No one else on all of GitHub has exactly the same username as you. Be careful to distinguish it clearly:

- A username is not your display name. The display name can be changed freely, can be duplicated, and can be in any language, but it cannot be used to invite you.
- A username is not your email either. The search box for inviting a collaborator recognizes usernames, not emails.

This cuts both ways, and you need to stay alert to both:

- When you want to invite someone: you must first get their exact username. Not a single character can be wrong; a typo will at best fail to find the person, and at worst add a stranger with a similar name into your private project.
- When you want to be invited (for example, a teacher or team lead wants to add you into their repo): you need to actively and clearly give them your own exact username. Do not just give a display name, and do not just give an email, give the exact string that comes after github.com/.

The safest approach: just send the other person your profile URL, that is, github.com/your-username. That way they can copy and paste it and will not add the wrong person because they misheard or mistyped something.

By the way, since your username is your unique identifier on GitHub, just pick something you like and that relates to your name early on, and once you settle on it, do not keep wanting to change it. GitHub does allow you to change it, but it really is not worth the hassle: a username is not that precious after all, it is not your brand, and the name you present to the world later can be something entirely different from this username. As for why we do not recommend changing it around, we will devote a whole lesson to that later; for now just remember the conclusion.

---

## 8. Hands-On: Adding a Person as a Collaborator

The whole process takes under two minutes. Let's use the example of inviting a classmate named John.

**Step one, go to the repo's Settings.** Open the home page of the repo you want to add a collaborator to. At the far right of that row of tabs at the top (Code, Issues, Pull requests, and so on) is Settings, with a gear icon. Click into it.

**Step two, find Collaborators.** Once you are in Settings, look at the left sidebar. Under the Access category there is an item called Collaborators (in a personal repo). Click it. If this is your first time on this page, GitHub may ask you to re-enter your password to confirm your identity, which is a normal security measure.

**Step three, add the collaborator.** On the right side of the page there is a green Add people button. Click it, and a search box pops up. Enter the other person's exact GitHub username here (remember what section 7 said, it is the username, not the email). GitHub will list matching users; once you confirm the avatar and name match the person you are looking for, select them, then click Add [username] to this repository.

**Step four, that's it, the invite has gone out.** You will see the person in the Collaborators list with the status Pending invite.

---

## 9. After the Invite Goes Out: It Only Counts Once They Accept

Here is a detail many people overlook: clicking Add does not mean the other person is instantly in.

After you add them, the person receives an invitation email and can also see the invite in their GitHub notifications. They must click accept themselves before they officially become a collaborator on the repo. Until they accept, the status you see on the Collaborators page stays as Pending invite.

So the full chain is: you send the invite, the other person receives it, the other person accepts, and only then is collaboration truly established. If you have invited someone and they say they still cannot see your repo, nine times out of ten that invite is still sitting unclicked in their inbox.

---

## 10. A String to Keep Taut: No Invite, No Collaboration

Connect lessons 06 and 07 and there is a bottom line worth carving into your memory: for a private repo, without your invite, others simply cannot get in and cannot collaborate.

This is not a restriction, it is exactly a protection. The default state of private is "just me," and no one in the world can slip in on their own around that; the only way in is the invite you send by hand. So every time you want to bring someone in, you have to actively think of this step: I need to go into Settings and add them as a collaborator, otherwise they cannot even find the door.

Put another way, this also means the initiative for security is entirely in your hands. Who gets in, who does not, and when to remove someone, is all yours to decide alone.

You may not need this string yet, but sooner or later you will. Maybe someday your advisor helps revise your thesis and needs to get into your repo to make edits directly; maybe a student you mentor, or a classmate, wants to build something together with you. At that moment when collaboration is genuinely needed, this thought should flash through your mind immediately: can the other person get in? Have I added them as a collaborator? If not, they are still outside the door, and you need to go into Settings and invite them in first. Building this reflex up front actually matters more than pulling someone in to rehearse right now, which is why we do not specifically arrange a hands-on exercise for this lesson: understand the process for adding a collaborator above, keep it in mind, and when the day you really need it comes, you will use it naturally.

---

## 11. Recap: What We Learned

- A collaborator is a person you invite into a specific repo; it lets even a private repo support collaboration.
- In a personal repo, a collaborator has both Read and Write permissions by default, meaning they can both view and edit.
- Larger-scale collaboration (like an Organization) has finer-grained permission tiers, such as read-only, or edit-code-but-not-settings, which this course does not cover in depth.
- Invites recognize the exact GitHub username, not a display name and not an email; to get invited, clearly give the other person your username or profile URL.
- Add path: repo, Settings, Collaborators under Access on the left, Add people.
- An invite takes effect only when the other person accepts; before they accept it stays Pending invite.
- Bottom line: for a private repo, without an invite, others cannot access it and cannot collaborate.

---

## 12. A Word From Your Mentor

**Why this matters:**

Adding a collaborator is a simple operation, but behind it hides an important workplace lesson: the foundation of collaboration is trust, and trust is expressed through permissions. When you add someone as a collaborator, you are essentially saying, I trust you, I am willing to let you into my project space, and even to change my things. That is why I keep stressing that you should only invite people you truly trust, and keep stressing that you should use the exact username so you do not hand the key to the wrong person.

**Key insights:**

- Permission management is a study in proportion. Give too little and others cannot participate effectively; give too much and you invite unnecessary risk. A collaborator's read/write permission is a simple, sufficient starting point for most learning and small-team scenarios.
- Access is closed by default, and that is a good thing. It means the initiative for security is always in your hands; if you do not open the door yourself, no one can get in.
- The username is your precise coordinate in the world of collaboration. It is fine if you cannot remember someone's display name, but you must give the other person a username or profile link they cannot mistake.

**Next step:**

Bring this habit into your real collaboration. The next time you work on a project with someone, the first thing to do is think it through clearly: who needs to get in, do I have their exact username, and have I added them. As you take part in larger projects, you will run into finer-grained collaboration mechanisms like Organizations, Teams, and Branch Protection, but today you have already mastered the most fundamental first step, inviting the right people into your project.

---

## 13. Quick Reference

**What a collaborator is:** a person you invite into a specific repo; in a personal repo they have Read plus Write by default, meaning they can both view and edit.

**Add path:** repo, Settings, Collaborators under Access on the left, the green Add people button.

**It recognizes the username:** enter the other person's exact GitHub username in the search box, not a display name and not an email. The safest option is to have the person send you their profile link, github.com/USERNAME.

**It needs the other person to accept:** after you add them, they receive an invitation email; before they accept, the status is Pending invite, and it only takes effect once they accept.

**Bottom line:** for a private repo, without your invite, others cannot access it and cannot collaborate.
