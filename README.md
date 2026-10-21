# Password Policy Generator — Policy Documents & Compliance Checker for Teams

Design a password policy the way modern guidance actually recommends and get **two deliverables instantly**: a clean, readable **policy document** you can hand to a team, and a machine-readable **JSON export** — plus a **compliance checker** that tests passwords against your rules locally. Built-in defaults follow **NIST SP 800-63B**: length first, no forced rotation, breached-password screening, MFA on top.

**Live Demo:** https://anaskhan0009.github.io/password-policy-generator/

## Features

- **Local account system** — sign up / log in on this device (passwords stored only as salted SHA-256 hashes, never plain text), continue as guest, per-account data separation, account deletion, and Export / Import of your records as JSON
- **Full record manager (CRUD)** — create, view, edit and delete your own saved records; the core tool works fully without an account, signing in unlocks saving for saved policies, so a team can keep its baseline, variants and revisions
- **Policy designer** — minimum length, character classes, rotation/max-age, history, lockout threshold, passphrase support, denylist screening and MFA requirements
- **Readable policy document** generated from your settings, covering storage requirements (Argon2id/bcrypt) for the systems side too
- **JSON export** of the same settings for documentation or tooling
- **Compliance checker** — pass/fail per rule with leetspeak-aware common-password detection, 100% local

## How to Use

1. Set the rules in the designer — start from the NIST-friendly defaults if unsure.
2. Generate the document, then copy it or download the JSON version.
3. Test a few sample passwords in the compliance checker to see how the policy behaves.
4. Save the policy to your records below with a name and notes.

## Why Most Password Policies Fail

“8 characters, one symbol, change every 90 days” produces `Summer2025!` — predictable patterns that cracking rigs try first. Length is what actually multiplies guessing work, forced rotation pushes people into predictable sequences, and the single most damaging habit is reuse across sites. This generator defaults to the evidence-based alternative and explains the reasoning inside the document it writes.

## Ethical Use

This is a **defensive, educational tool** — it only ever helps you understand and improve your own security and privacy. Nothing here can be used to attack, track or deceive anyone else.

## Tech

Single self-contained `index.html` — HTML, CSS, vanilla JavaScript, WebCrypto (salted SHA-256 password hashing), localStorage persistence. No servers, no tracking, no external requests.

---

Built by **Dinal Studios** — free cyber security tools and web apps.
GitHub: https://github.com/anaskhan0009
