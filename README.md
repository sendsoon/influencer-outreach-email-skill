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
│   └── platform-notes.md
└── assets/
    └── email-template.md         # Placeholders + filled examples
```

## Install

Copy `SKILL.md`, `README.md` (plus `README.zh-CN.md` / `README.ja.md` if you want localized docs), `references/`, and `assets/` into a skills directory the client scans. `SKILL.md` must sit at the skill-folder root. Start a new agent session afterward (restart Codex).

Run the commands from this repo root. PowerShell on Windows; bash on macOS/Linux.

### Paths

| Client | User-level | Project-level |
|--------|------------|---------------|
| Codex | `~/.codex/skills/<name>/` and `~/.agents/skills/<name>/` | `.agents/skills/<name>/` |
| Claude Code | `~/.claude/skills/<name>/` | `.claude/skills/<name>/` |
| Other Agent Skills clients | Product-specific user skills folder | Product-specific project skills folder |

`<name>` = `influencer-outreach-email-skill`.

### Codex

```powershell
function Install-SkillTo($dest) {
  New-Item -ItemType Directory -Force $dest | Out-Null
  Copy-Item -Force SKILL.md, README.md, README.zh-CN.md, README.ja.md $dest
  Copy-Item -Recurse -Force references, assets $dest
}
Install-SkillTo "$env:USERPROFILE\.codex\skills\influencer-outreach-email-skill"
Install-SkillTo "$env:USERPROFILE\.agents\skills\influencer-outreach-email-skill"
```

```bash
install_skill() { mkdir -p "$1"; cp SKILL.md README.md README.zh-CN.md README.ja.md "$1/"; cp -R references assets "$1/"; }
install_skill ~/.codex/skills/influencer-outreach-email-skill
install_skill ~/.agents/skills/influencer-outreach-email-skill
```

Project install: `.agents/skills/influencer-outreach-email-skill/`.

From a GitHub URL, `$skill-installer` also works; restart Codex. If the skill does not appear, confirm skills are enabled in `~/.codex/config.toml` (`[features] skills = true` on some versions).

### Claude

**Claude Code** — copy to `~/.claude/skills/influencer-outreach-email-skill/` (user) or `.claude/skills/influencer-outreach-email-skill/` (repo).

```powershell
$dest = "$env:USERPROFILE\.claude\skills\influencer-outreach-email-skill"
New-Item -ItemType Directory -Force $dest | Out-Null
Copy-Item -Force SKILL.md, README.md, README.zh-CN.md, README.ja.md $dest
Copy-Item -Recurse -Force references, assets $dest
```

```bash
mkdir -p ~/.claude/skills/influencer-outreach-email-skill
cp SKILL.md README.md README.zh-CN.md README.ja.md ~/.claude/skills/influencer-outreach-email-skill/
cp -R references assets ~/.claude/skills/influencer-outreach-email-skill/
```

Slash command: `/influencer-outreach-email-skill`. If it is missing, `/reload-plugins` or restart the session.

**Claude.ai** — Pro / Max / Team / Enterprise, with Skills enabled (product settings vary).

1. Zip this folder so the archive contains `SKILL.md` or `influencer-outreach-email-skill/SKILL.md`.
2. [claude.ai](https://claude.ai) → **Settings** → **Capabilities** (sometimes **Features**) → **Skills**.
3. Upload the zip. Custom skills are per account and do not sync to Claude Code.

### Other agents

Copy the folder into that product’s documented skills directory (Agent Skills spec). If this repo is on GitHub:

```bash
npx skills add <owner/repo> --agent claude
npx skills add <owner/repo>
```

Use `-g` for user-level install. Confirm `--agent` values with `npx skills --help`.

### Local development (one checkout, several clients)

```powershell
$src = (Resolve-Path .).Path
$dests = @(
  "$env:USERPROFILE\.codex\skills\influencer-outreach-email-skill",
  "$env:USERPROFILE\.agents\skills\influencer-outreach-email-skill",
  "$env:USERPROFILE\.claude\skills\influencer-outreach-email-skill"
)
foreach ($d in $dests) {
  New-Item -ItemType Directory -Force (Split-Path $d) | Out-Null
  if (Test-Path $d) { Remove-Item -Recurse -Force $d }
  cmd /c mklink /J "$d" "$src"
}
```

macOS / Linux: `ln -s`.

### Team repos

| Audience | Path |
|----------|------|
| Codex | `.agents/skills/influencer-outreach-email-skill/` |
| Claude Code | `.claude/skills/influencer-outreach-email-skill/` |
| Codex + Claude Code | Both paths (copy or link) |

### Verify

- Folder name is `influencer-outreach-email-skill` and contains `SKILL.md`, `references/`, `assets/`.
- New chat: “Help me partner with this YouTuber” should return Subject + body (language follows the creator’s market).
- The name appears in Codex skills and the Claude Code `/` menu.

## Inputs

- Brand / product and 1–2 sentence value proposition
- Creator name, platform, content style (ideally one piece of content you watched)
- Follower count or estimated tier (Nano / Micro / Mid / Macro)
- Collab type: paid / seeding / affiliate / ongoing
- Creator vs manager / MCN
- Fee range, if any
- CTA: reply, call, or link

If details are missing, the agent asks 1–3 questions and drafts with `{{brand_name}}`, `{{creator_name}}`, `{{collab_type}}`, and similar placeholders.

## Output

```
Subject: ...

---

<email body>

---

Assumptions / placeholders:
- ...
```

DMs use `DM:` on the first line. Tone: professional, peer-level; formality follows creator tier. No spam phrasing (`FREE`, `$$$`, `ACT NOW`). Cold emails: 80–150 words; follow-ups shorter. JP / KR / LATAM / SEA creators: English + target-language drafts when the user did not specify a language.

## Follow-up cadence

| Touch | When | Shape |
|------|------|--------|
| #1 | Day 0 | Full email |
| #2 | 3–5 days | Shorter, one new fact |
| #3 | 4–6 days later | 3–6 sentences, no pressure |
| #4 breakup | 5–7 days later | Close; then stop |

Max four emails. Details: `references/follow-up-sequence.md`.

## Example prompts

- Help me partner with this YouTuber
- Draft a seeding email for this Instagram creator
- Follow up with last week’s KOL
- Confirm terms and send them over
- They replied with a rate — draft the response
- Make this an Instagram DM

## Out of scope

- Sending mail, scraping, or validating creator emails
- Identical blast copy (one distinct hook per creator)
- Invented videos, fees, or legal terms
- Commercial outreach to creators who may be under 18 (confirm age/guardianship first; paid work should go through legal)
