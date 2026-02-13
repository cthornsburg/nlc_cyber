# Student Submissions Guide (CTF Writeups + Lab Requests)

This guide walks you through submitting content to the NLC Cyber GitHub repository even if you’ve **never used Git/GitHub**.

## What you can submit

### CTF solutions / writeups (allowed)
- How you approached a challenge (your thought process)
- Steps that are **reproducible**
- Tools/commands used (sanitized)
- What you learned

**Do NOT include:**
- Flags, tokens, passwords, API keys
- Real client/school data
- Details that violate competition rules

### Lab requests (allowed)
- A request for a new lab topic
- A bug report / clarification request for an existing lab
- A dataset suggestion (must be legal to share)

---

## Two ways to submit (pick one)

### Option A (easiest): Submit using the GitHub website (no Git installs)
This is the recommended approach if you’re new.

### Option B (power user): Submit with Git from your computer
Use this once you’re comfortable. (Not required to contribute.)

---

## Before you start

1) Create a GitHub account:
- https://github.com/signup

2) Open the repo:
- https://github.com/cthornsburg/nlc_cyber

3) Read the rules:
- `CONTRIBUTING.md` (in the repo)

---

# Option A — Submitting via the GitHub website

## A1) For a LAB REQUEST (or bug/clarification)

**Use a GitHub Issue** (think of it like a ticket).

1) Open the repo:
   - https://github.com/cthornsburg/nlc_cyber
2) Click **Issues**
3) Click **New issue**
4) Pick the best template (if shown), for example:
   - “new-lab” (new lab request)
   - “fix-errata” (bug/clarification)
5) Fill it out.

**What to include in a lab request:**
- What skill/topic you want (example: “Windows event log triage”)
- Difficulty level (intro/intermediate/advanced)
- What you want to be able to do at the end
- Any references/links (optional)

## A2) For a CTF WRITEUP (recommended workflow)

### Step 1 — Fork the repository
A **fork** is your own copy of the repo on GitHub.

1) Go to: https://github.com/cthornsburg/nlc_cyber
2) Click **Fork** (top right)
3) Accept defaults and create the fork

### Step 2 — Add your writeup file in your fork

1) In your forked repo, navigate to the writeups folder (or create one):
   - `ctf/writeups/`
2) Click **Add file → Create new file**
3) Name your file like:
   - `ctf/writeups/YYYY-MM-DD_platform_challenge-name.md`
   - Example: `ctf/writeups/2026-02-13_picoCTF_web_sql-injection.md`
4) Paste your writeup content
5) Add a clear commit message, like:
   - “Add writeup: picoCTF SQL Injection (sanitized)”
6) Click **Commit new file**

### Step 3 — Open a Pull Request (PR)
A **Pull Request** is how you ask to merge your changes into the main repo.

1) In your fork, click **Pull requests**
2) Click **New pull request**
3) Confirm it’s:
   - **base repository:** `cthornsburg/nlc_cyber`
   - **base branch:** `master`
   - **compare:** your fork + branch
4) Click **Create pull request**
5) In the PR description, include:
   - Challenge name + platform
   - What category (web/forensics/rev/crypto/etc.)
   - Confirmation: “No flags/secrets included”

---

# Writeup template (copy/paste)

```markdown
# [Platform] — [Challenge Name]

## Summary
1–3 sentences: what the challenge was about.

## What I tried (and why)
- Step-by-step, with reasoning.

## Solution (sanitized)
- Commands, tools, key observations.
- No flags, no secrets.

## Lessons learned
- What you’d do faster next time.
- Common pitfalls.

## References
- Links to docs/posts you used.
```

---

# Option B — Submitting with Git (advanced, optional)

If you want to learn Git, the basic flow is:

1) Install Git (Mac usually has it):
```bash
git --version
```

2) Clone your fork:
```bash
git clone git@github.com:<your-username>/nlc_cyber.git
cd nlc_cyber
```

3) Create a branch:
```bash
git checkout -b add-writeup-<topic>
```

4) Add your file(s), commit, push:
```bash
git add ctf/writeups/your-file.md
git commit -m "Add writeup: ..."
git push -u origin add-writeup-<topic>
```

5) Open a Pull Request on GitHub.

---

## Safety reminders (please read)
- This repo is public.
- Don’t upload sensitive data.
- Don’t post flags/secrets.
- When in doubt, ask before submitting.
