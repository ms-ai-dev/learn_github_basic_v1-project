---
description: "Create a GitHub Personal Access Token scoped to repo only, store it safely in a password manager, and understand that it is a password for machines, why it is safer than your password, and how it can be revoked and recreated at any time."
---

# Create Your GitHub Personal Access Token: A Pass Machines Can Use

> Generate a credential built specifically for programs to use, and understand why it is far safer than simply handing over your password.

## 1. Overview

This is lesson 10 of the "Learn GitHub Basics" series. In the earlier lessons you acted as a single person, clicking your way through GitHub in the browser. This time we flip the perspective: when a program needs to operate GitHub on your behalf, how does it prove "I am acting for you"? The answer is the Personal Access Token.

Let's be clear about one thing up front: this is a general GitHub skill, and it has nothing to do with any specific project you might use it on. Whether you later push code from the command line, manage repositories with a third-party tool, or let an automation script do the work for you, the same thing is proving your identity behind the scenes. Once you learn it, you hold the key that takes GitHub from "clicking around a web page" to "programmatic automation."

One more heads-up: you will not actually need this right away. This lesson is more about planting a lasting concept in your mind. For now it is enough to know that a token exists. But do remember it, because it will come up in many places later, especially when you work with a private repo.

---

## 2. Learning Objectives

Let's start with a fact you may not have realized before: every button you can click on the GitHub website, a program can also do. You click Create repository to make a repo, and a single command can do the exact same thing; you click Import repository to bring in a project, and the GitHub backend uses the same interface to do it for you. Precisely because every GitHub feature exposes a matching programmatic interface, you are able to operate it with the command line, with tools, and with scripts.

So here is the question: on the website you log in with your password once, and the browser remembers you. But a program has no browser and no logged-in session of yours, so what does it use to prove its identity? The most intuitive idea is to give it your password to use, and that is exactly where the danger begins. This lesson gives that question a safe answer.

By the end of this Task, you will be able to:

1. Explain in your own words what a Personal Access Token is, and how it fundamentally differs from your password.
2. Independently generate a least-privilege (repo only) classic token.
3. Store it safely in a password manager, and know that it can be revoked and recreated at any time.
4. Recognize the various names for this thing (PAT, GitHub token, auth token) and know they all refer to the same object.

---

## 3. Prerequisites

- A GitHub account you can log into normally.
- Ideally, a password manager on hand (1Password, Bitwarden, or even your browser's built-in one) to store the token safely.
- This entire lesson is done in the browser. No command line is needed, and there is no difference between Mac and Windows; the steps are identical.

---

## 4. What You Will Build or Learn

After finishing this lesson, you will have generated a real, working GitHub token with your own hands, stored it safely in a password manager, and clearly understood what it is, how to keep it safe, and how to stop the bleeding with one click if something goes wrong. This is the starting point for all your future automation.

---

## 5. The Core Analogy: A Token Is a Password for Machines

To understand a token, remember one sentence: a password is for you, a living person, while a token is for machines.

When you operate GitHub in the browser yourself, you type your password once to log in, and that proves "I am me." But when a program (command-line Git, a development tool, an automation script) needs to operate GitHub on your behalf, there is no browser in front of it and no logged-in session of yours. It still needs something to prove "I am acting for so-and-so, please let me through." That credential, issued specifically for programs, is the Personal Access Token.

So you can think of a token as a "password for machines": it works much like a password, proving identity and getting GitHub to let you through, but it is issued to a program, not to a person. And precisely because the user is a program rather than a person, it is designed to be more flexible, and far safer, than a password. Let's look at what makes it good.

---

## 6. Why Not Just Use Your Password, and What Makes a Token Better

The most intuitive idea is: why not just give my GitHub password to the program? This is extremely dangerous, and the reason fits in one sentence: a password holds too much power, and when something goes wrong there is no way to contain the damage.

Your GitHub password can do almost anything: delete repos, change your email, close your account, and operate every organization you have joined. Handing it to a tool is like giving someone the master key to your home, with every door wide open to it. Worse, if some tool leaks your password, your only remedy is to change it; but the moment you do, every other tool legitimately using that password stops working too, and you have to reconfigure them one by one.

Tokens exist to solve exactly this, and they have three advantages a password cannot offer:

- Permissions can be narrowed. When you generate one, you can grant only "read and write repositories," not delete repos, not manage organizations, not change your account. Even if it leaks, whoever holds it cannot do much. It is just a "key card that opens one specific room," not a master key.
- It can be revoked individually at any time, with no side effects. You can issue several tokens for different programs at once, and if one causes trouble you delete just that one; the rest of your tokens and your password are completely unharmed.
- It can be set to expire. Have it automatically stop working after 30 or 90 days, so even if you forget to revoke it manually, it turns into a useless string on its own once it expires.

Here lies a token's most important value: isolation. Compare two kinds of "loss." If your password is lost, someone may even take over your account itself, and you lose that account entirely; but if a token is lost, your account is still yours, and at most someone can access the small slice of data within its granted scope until you revoke it, and the moment you revoke it, the bleeding stops. A token separates "ownership of the account" from "access to the data," and that is the fundamental reason it is far safer than a password.

One more fact: precisely because a password is too powerful, GitHub has, since August 2021, completely banned using your login password for command-line Git operations and API calls. Programmatic operations can only use a token. In other words, this is not optional; it is a step you will have to take sooner or later.

---

## 7. A Token Does One More Thing: It Proves You Are You

So far we have described the token as a "password for machines," governing "what you can do," that is, permissions. But a token quietly does one more thing: it proves "you are you," that is, identity. These two things sound like the same thing, but they are actually different, and it is worth calling out separately.

Here is a college example that makes it click. At the start of the term, a teacher needs to grant you access to some material, so first they have to know who you are, and you tell them your GitHub username. But a username is semi-public: you told the teacher, but classmates might see it too, or it could end up on some roster. So the problem arises: since others also know your username, can't someone impersonate you and tell the teacher "I am this username"?

A username alone really cannot prevent impersonation, because it is just a "name" that anyone can claim. But there is one thing no one can impersonate: the token. Only the real you holds that string of characters that belongs to you alone; whoever can produce that token can be verified as "genuinely this person." Anyone can shout a name, but only you have that secret credential.

So remember this distinction: "you are you" (identity) and "you have permission" (authorization) are two different things. You might genuinely be you but lack permission on a certain repo; you might have permission but must first prove you are you. The clever thing about a token is that it packs both of these into a single string, proving who you are while also defining what you can do.

For now it is enough to know this layer exists; you do not need to dig deeper. We use the small college example only to give you an intuition for "a single credential representing both identity and permission." When you later run into a situation that requires "proving you are you," you will naturally connect the dots.

---

## 8. Let's Line Up the Names: It Has Several

In different places you will see this thing called by several names. Don't let it confuse you; they all refer to the same object:

- Personal Access Token, PAT for short, is its formal full name.
- GitHub token, or just token, is the most casual name.
- auth token (authentication token) emphasizes that it is used to "authenticate identity."

From now on, whether in this course or in other tutorials, whenever these words pop up, the thing in your mind should be the string we generate in this lesson.

By the way, GitHub tokens actually come in two kinds. One is the newer fine-grained token, which can control permissions precisely down to a single repository, but has many setup steps and a more complex concept; the other is the classic Tokens (classic), whose permissions are coarser but which is simple and direct. In this lesson we use classic, because it is easier to get started with and friendlier to beginners.

---

## 9. Hands-On: Generate a classic Token

The whole process is done in the browser, identical on Mac and Windows, with no command line to touch.

**Step one, go to Settings.** Click your avatar in the top-right corner, and in the dropdown menu click Settings.

**Step two, find Developer settings.** Scroll the left sidebar all the way down to the very bottom and click Developer settings. It is tucked away because a token counts as a developer tool, but don't be scared off by the name; you don't have to be a developer to use it. If digging through the layers is a hassle, type github.com/settings/tokens straight into the address bar to jump there in one step.

**Step three, choose the type.** Under Personal access tokens, choose Tokens (classic).

**Step four, start generating.** In the top-right corner click Generate new token, then choose Generate new token (classic). At this point GitHub may ask you to enter your login password again to confirm you are the account owner; this is a normal security measure, since you are creating a pass.

**Step five, fill in the details.** This screen has three key fields:

- Note: give the token a name you will recognize by its purpose, such as my-learning-token. It is just a label for yourself and does not affect functionality.
- Expiration: set a validity period. 90 days is a good fit for learning. The list also has No expiration, which you could pick to save trouble, but I would not recommend making a habit of it; setting an expiration on a credential is a good habit in itself.
- Select scopes: this is the most important step. Just check the single repo item. Once you check it, a string of sub-permissions underneath will be checked automatically, and that is normal. Leave all other permissions untouched.

**Step six, generate.** Scroll to the bottom of the page and click the green Generate token.

---

## 10. Shown Only Once: Save It in Your Password Manager Immediately

After generation, a string starting with ghp_ appears on the page. That is your token.

The most critical point: this string is shown only this once. The moment you refresh or leave this page, you will never see it again. GitHub does not store the plaintext, so you cannot "recover" it; you can only generate a new one. So right now, do two things immediately:

1. Click the copy icon next to the token to copy it.
2. Open your password manager (1Password, Bitwarden, or your browser's built-in one), and create a new entry: name it GitHub Personal Access Token, paste this token into the password field, and note its permission (repo) and creation date in the notes.

Never paste it into a chat log, a notes app, or a txt file on your desktop. A token is as sensitive as a password, and anyone who can see those places can use it to access your repositories. A password manager stores it encrypted and requires a master password to view, which is a much higher level of security.

---

## 11. Revocable Any Time: Feel How Disposable a Token Is

Finally, let's have you experience firsthand the one way a token differs most from a password: a token can be thrown away on a whim.

You can return to github.com/settings/tokens at any time, find any token in the list, and click Delete to void it. Once voided, any program using this token immediately loses access, but your account, password, repositories, and login session are all completely unharmed. When you need one again, just generate a new one; make as many as you want, delete whichever you want.

Compare this with "changing your password" and it clicks: changing your password is a big deal that affects everything, and one change forces you to reconfigure everywhere else; whereas voiding a token merely closes one specific door, casually, with no psychological burden. This "disposability" is exactly the point of a token's existence.

---

## 12. Exercises

### Exercise 1: Generate and Safely Store a Token

**Goal:** Independently generate a classic token with repo permission only, and store it safely.

**What to do:**

1. Type github.com/settings/tokens straight into the address bar to reach the Tokens (classic) page.
2. Click Generate new token, choose Generate new token (classic), and enter your password to confirm your identity when prompted.
3. Fill Note with a name you will recognize by its purpose (such as my-learning-token); set Expiration to 90 days.
4. Under Select scopes, check only the repo item and nothing else.
5. Scroll to the bottom and click Generate token, then immediately copy the string starting with ghp_.
6. Store it in your password manager, noting the permission (repo) and the date.

**What you will observe:**

The token starting with ghp_ appears only this once and is gone once you refresh the page. Once stored in your password manager, you have a safe, ready-to-use credential.

> **Key insight:** Grant just enough permission and no more; every extra box you check adds a little more risk. Checking only repo keeps the blast radius as small as possible if it ever leaks.

### Exercise 2 (Optional, Highly Recommended): Revoke It and Feel the Difference From a Password

**Goal:** Void a token with your own hands, and let your body remember how fundamentally it differs from a password.

**What to do:**

1. Return to github.com/settings/tokens.
2. If you would feel bad deleting the one from Exercise 1, generate another one just for practice deletion first.
3. Select a token in the list, click Delete, and confirm when prompted.
4. After deleting, deliberately check: has anything changed for your account, your repositories, or your login session?

**What you will observe:**

The token disappears from the list, but your account is business as usual, and you are not even logged out. If a program was using that token, that program stops working, and that is all; swap in a new token and it recovers.

> **Key insight:** Revoking a token carries no psychological burden, because it only touches "data access," never "account ownership." You would never dare void a password so casually. This is the value of isolation, and you just verified it with your own hands.

---

## 13. Recap: What We Learned

- A password is for you, a living person; a token is for machines. They work similarly but serve different users.
- Handing your password directly to a program is dangerous: a password holds too much power, and a leak leaves no way to contain the damage.
- A token's three advantages: permissions can be narrowed, it can be revoked individually, and it can be set to expire.
- A token's most important value is isolation: it separates "account ownership" from "data access," so losing a token does not mean losing your account.
- A token not only defines "what you can do" (permission) but also proves "you are you" (identity); anyone can claim a name, but only you have that credential.
- PAT, GitHub token, and auth token all refer to the same thing; this course uses the simple Tokens (classic).
- When generating, check only repo, following the principle of least privilege; a token is shown only once, so you must copy it immediately and save it in a password manager.
- A token can be revoked and recreated with one click at any time, and this is exactly what sets it apart from a password and makes it safer.

---

## 14. A Word From Your Mentor

**Why this matters:**

You might feel that today you just "generated a token," an operation that took under five minutes. But behind it lies a way of thinking that is extremely important in information security and will serve you for a lifetime: the Principle of Least Privilege. We could have checked all the permissions and been done with it, so why check only repo? Because every additional permission adds a little more risk. Grant just enough permission and not a bit more, and the blast radius when something goes wrong stays as small as possible.

**Key insights:**

- This principle is everywhere in the working world: a database account gets only the few tables the application needs, a cloud service key is authorized for only specific services, a new employee gets only the permissions required to do the job. It is not that you are not trusted; it is that the smaller the permission, the smaller the cost when something goes wrong.
- Good security habits are not about "fixing things after they break" but about "keeping risk contained from the start." A token's revocability, expiration, and scope narrowing bake exactly this mindset into the tool.
- Where you store a credential matters as much as how much permission you grant: always use a password manager, and never leave it lying around in plaintext.

**Next step:**

From now on, whenever you create a token, an API key, or any kind of credential, first ask yourself two questions: exactly which permissions does this operation need (check only the necessary ones), and where should this credential be stored (always use a password manager). Security incidents often happen not because hackers are too clever, but because someone granted far more permission than needed, or stuck a credential somewhere it should never have been. People who build these two habits get trusted on any team.

---

## 15. Quick Reference

**What it is:** A "password" for machines, used for authentication scenarios beyond browser login (command-line Git, API, various development tools).

**Several names:** Personal Access Token (PAT), GitHub token, auth token; they all refer to the same thing.

**Where to generate:** Type github.com/settings/tokens straight into the address bar, choose Tokens (classic), then Generate new token (classic).

**Key settings:** Give Note a name you will recognize by its purpose; set Expiration to 90 days; under Select scopes, check only repo.

**Saving:** The token starts with ghp_ and is shown only once; copy it immediately and store it in a password manager, never in plaintext.

**Stopping the bleeding:** Return to github.com/settings/tokens and Delete it with one click to revoke it, with your account itself completely unharmed.
