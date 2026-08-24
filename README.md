# influencer-outreach-email-skill

**English** | [简体中文](README.zh-CN.md) | [日本語](README.ja.md)

Drafts partnership emails to overseas creators (YouTube, Instagram, TikTok, and similar). Language follows the creator’s market — English, their language, or both — not English-only by default.

The agent should fire on collaboration intent — influencer outreach, brand collaboration, “contact this YouTuber” — and return a copy-paste **Subject + body**, not a strategy memo.

The repo root **is** the skill. Keep the folder name `influencer-outreach-email-skill` so it matches `name` in `SKILL.md`.

## Scope

| Stage | What it covers |
|------|----------------|
| Cold outreach | Paid, seeding, affiliate, first step of an ongoing deal, manager/agency |
| Follow-up | #2 / #3 / breakup when there is no reply |
| Terms | Deliverables, window, fee, usage |
| Shipment | Sample tracking |
| Reply handling | Media kit request, brief, rate, manager handoff, decline |
| DM | Short in-app copy; preferred for Nano/Micro when no email is on file |

## Layout

```
influencer-outreach-email-skill/
├── SKILL.md                      # Agent instructions
├── README.md                     # Install and usage (English)
├── README.zh-CN.md               # Chinese
├── README.ja.md                  # Japanese
├── references/
│   ├── subject-lines.md
│   ├── follow-up-sequence.md
│   ├── platform-notes.md
│   └── clarification.md          # What to ask when facts are missing
└── assets/
    └── email-template.md         # Placeholders + filled examples
```

## Install

Recommended (clones this repo and installs the skill):

```bash
npx skills add sendsoon/influencer-outreach-email-skill
```

User-level for Claude Code and Codex (Windows: add `--copy` if symlinks fail):

```bash
npx skills add sendsoon/influencer-outreach-email-skill -g -a claude-code -a codex -y
```

Update to the latest from GitHub:

```bash
npx skills update influencer-outreach-email-skill
```

User-level:

```bash
npx skills update influencer-outreach-email-skill -g -y
```

## Example

**Input**

```
Brand: Northstar — gooseneck kettle that holds brew temperature within 1°C
Creator: Maya Chen, YouTube “Weekend Brews”, ~85k, brew-gear reviews
Watched: water-temperature comparison, 92°C vs 96°C side-by-side
Collab: paid dedicated integration
Recipient: Maya
Fee: USD 3,500–4,500
CTA: short reply
```

**Output**

```
Subject: Maya — idea for a Northstar collab

---

Hi Maya,

I watched your water-temperature comparison — the 92°C vs 96°C side-by-side is exactly the kind of test we built the Northstar kettle around.

Northstar makes a temperature-stable gooseneck kettle — it holds within 1°C so brew recipes are repeatable at home. I'm reaching out about a paid collaboration with Weekend Brews: one dedicated integration in a brew-gear video. You'd keep your usual test format; we'd provide talking points, not a script. We had USD 3,500–4,500 in mind, and I'm open to a number that fits your rate card.

If this is relevant, a short reply is enough. I can send a one-page brief with talking points (not a rigid script).

Best,
Jordan Hale
Partnerships, Northstar
jordan@northstar.example

---

Assumptions / placeholders:
- None
```
