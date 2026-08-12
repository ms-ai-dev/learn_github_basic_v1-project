---
description: "Successfully generate a classic Personal Access Token scoped to repo only and store it in a password manager, be able to explain the difference between a token and a password, and know that it can be revoked with one click at any time."
---

# Generate and Safely Store a GitHub Personal Access Token

## 1. Goal

Generate, with your own hands, a GitHub Personal Access Token built specifically for programs, and store it safely in a password manager. Through this task, you should truly understand the difference between a token and a password, learn to follow the principle of least privilege by granting only the necessary permissions, and know that a token can be revoked and recreated at any time.

---

## 2. What to Do

1. Read this lesson's README and understand why a token is a "password for machines," and what makes it safer than using your password directly.
2. Go to github.com/settings/tokens in the address bar and choose Tokens (classic).
3. Click Generate new token (classic) and enter your password to confirm your identity when prompted.
4. Fill in Note (a name you will recognize by its purpose), set Expiration to 90 days, and under Select scopes check only the repo item.
5. Once generated, immediately copy the token starting with ghp_, and store it in a password manager (1Password, Bitwarden, etc.), noting the permission and the date.
6. (Optional) Return to the token list, revoke a token, and observe that your account and repositories are completely unharmed, experiencing its disposability firsthand.

**Estimated time:** About 15 minutes

---

## 3. Checklist

- [ ] **Understand the token**: Can explain that a token is a password for machines, and how it differs from your own login password.
- [ ] **Reach the correct page**: Reached github.com/settings/tokens and chose Tokens (classic) rather than fine-grained.
- [ ] **Least privilege**: Checked only the repo permission and did not check any others.
- [ ] **Successfully generated**: Successfully generated the token and copied the string starting with ghp_.
- [ ] **Stored safely**: Stored the token in a password manager, and did not leave it in plaintext in a chat log, notes app, or desktop file.
- [ ] **Understand shown-only-once**: Understand that the token is shown only once, cannot be recovered after a refresh, and can only be regenerated.
- [ ] **Understand revocability**: Can explain that a token can be revoked with one click at any time, and that revoking it does not affect the account itself, which is exactly what makes it safer than a password.
- [ ] **Understand identity vs. permission**: Know that a token both proves "you are you" (identity) and defines "what you can do" (permission), and that these are two different things.
