---
name: influencer-outreach-email-skill
description: "Writes copy-paste-ready English business outreach emails for YouTube, Instagram, and TikTok creator/KOL collaborations (cold outreach, follow-ups, terms, seeding, affiliate). Use when the user wants to contact, reach out to, pitch, or partner with a creator — even if they never say write an email. Triggers: influencer outreach, brand collaboration, influencer partnership, KOL邮件, 达人合作, 网红建联, 联系 YouTuber, 寄样测评, 跟进达人. Output Subject + body, not a strategy memo."
metadata:
  version: "1.2"
---

# Influencer Outreach Email

Draft formal English partnership emails to overseas creators. Return a copy-paste **Subject + body**. Do not lead with strategy.

Trigger on outreach intent even when the user never says “write an email” (e.g. contact this YouTuber, follow up with this creator, seed a sample).

Install paths for humans: `README.md`.

## When to Use

| Stage | Signals | Load |
|------|---------|------|
| Cold outreach | first contact, pitch, intro | `assets/email-template.md` + `references/platform-notes.md` |
| Follow-up | no reply, nudge | `references/follow-up-sequence.md` |
| Terms | rates, deliverables, dates, usage | terms template in `assets/email-template.md` |
| Shipment | sample sent, tracking | shipment template in `assets/email-template.md` |
| Creator replied | yes, rate, manager, no | After They Reply, then the matching template |
| DM | Instagram / TikTok / YouTube DM | same skill, Channel format |

Iterate subject lines with `references/subject-lines.md`. Affiliate, ongoing, and manager letters: matching sections in `assets/email-template.md`.

## Workflow

1. **Stage**: cold / follow-up (#2, #3, breakup) / terms / shipment / reply.
2. **Gaps**: ask at most **1–3** blocking questions. Fill the rest with `{{placeholders}}` and list Assumptions under the draft.
3. **Load**: platform notes for first touch; follow-up sequence for nudges.
4. **Draft**: Subject, then body. Default **one** primary email. For a list, **one email per creator** — never a shared blast body.
5. **Check**: Guardrails + Quality bar, then Output format.

If brand + creator + intent are present, draft immediately. Extract name and platform from profile/video URLs; do not re-ask known facts.

Use only glossary names from `assets/email-template.md` (`{{content_hook}}`, `{{new_info}}`, etc.).

## Required Information

Do not invent fees, video titles, follower counts, deadlines, or legal terms.

**Required (ask or placeholder):**

- Brand / product and 1–2 sentence value proposition
- Creator name, platform (YouTube / Instagram / TikTok), content style
- Collab type: paid / product seeding / affiliate / ongoing
- Recipient: creator vs manager / MCN
- CTA: reply, book a call, or open a link

**Optional:**

- Fee range
- One piece of content actually watched (for the opener)
- Sender name, title, company, email, calendar link
- Deliverable count, publish window, exclusivity, usage rights (terms stage only)

Ask at most one of: paid vs seeding vs affiliate; preferred CTA; a real content hook.

## Email Structure

Cold outreach: **80–150 words** (TikTok: 70–110).

1. **Opener (1–2 sentences)** — a verifiable detail from their work. Never “I love your content.” If no hook exists, keep `{{content_hook}}`; do not fabricate titles.
2. **Brand (1–2 sentences)** — what it is and why it fits. No company history, no feature dump.
3. **Proposal + value** — collab type, rough deliverable, what they get (fee, product, audience fit, creative control).
4. **Single CTA** — default: a short reply.
5. **Sign-off** — name, title, company, email; calendar link only if the CTA is a call. Plain text only.

Do not: long brand stories, multiple CTAs, attachment dumps, or “let’s hop on a 30-min call” unless requested.

Templates: `assets/email-template.md`. Northstar filled examples teach tone only — never copy their specs, fees, or dates onto a real brand.

## Subject Lines

Short, specific, peer-to-peer. Prefer 40–60 characters. Do not fake a thread with `Re:` / `Fwd:` on a first email.

1. `{{creator_name}} — idea for a {{brand_name}} collab`
2. `Quick note on {{content_hook}} + {{brand_name}}`
3. `{{brand_name}} × {{creator_name}}: {{collab_type}}`
4. `Collaboration around {{content_theme}}`
5. `Sending over a {{collab_type}} idea`

Never: `FREE`, `$$$`, `ACT NOW`, `URGENT`, `LIMITED TIME`, `100%`, `WINNER`, `CONGRATULATIONS`. No ALL CAPS. No stacked exclamation marks.

More variants: `references/subject-lines.md`.

## Tone

Friendly, professional, peer-level — Partnerships, not a sales bot.

Avoid: `game-changing`, `once-in-a-lifetime`, `we'd be honored`, `synergy`, `crush it`, fake intimacy (`Hey bestie`), excessive apology, emoji, ALL CAPS.

Follow-ups are shorter and low-pressure; include an easy out.

Write English unless the user asks otherwise. If the creator’s content is clearly not in English and the user did not specify, still draft in English and note “business language unconfirmed” in Assumptions.

## Follow-up Logic

Use only if there is no reply and no explicit no.

| Touch | When | Shape |
|------|------|--------|
| #1 | Day 0 | Full structure, 80–150 words |
| #2 | 3–5 days later | Shorter; one new fact (sample, window, brief) |
| #3 | 4–6 days after #2 | 3–6 sentences; easy decline |
| #4 breakup | 5–7 days after #3 | Close the loop; then stop |

Max four emails per thread. Do not ask “did you get this?” or fake scarcity. Copy: `references/follow-up-sequence.md`.

## After They Reply

| Signal | Next |
|--------|------|
| Interested / wants a brief | Terms template; only user-supplied numbers |
| Rate card | Do not invent a counter. List the figure in Assumptions; ask for an authorized range |
| Forward to manager / agent | Manager template; stop emailing the personal inbox only |
| Wants the product first | Seeding / shipment template; do not chase a fee in the same note |
| Timing is off | One window 4–6 weeks out, then stop |
| Clear no | Stop. Optional 2–3 sentence thank-you; no further follow-up |

## Channel

- Default: **email** (Subject + signature).
- **DMs**: not an email. Use `DM:` instead of `Subject:`, 40–80 words, one CTA, name + brand only — no long signature.
- This skill drafts copy. It does not send, scrape contacts, or write blast scripts.

## Guardrails

- If the creator may be under 18, stop and ask the user to confirm age or guardianship.
- Do not frame seeding as paid advertising, or paid work as “unpaid exposure.”
- Do not coach anyone to skip `#ad` / paid-partnership disclosure.
- Cold email: no passport, national ID, or bank details. Tax forms only at payment, if the user asks.
- Prefer a brief or shipping-form link over collecting extra personal data in the body.
- Do not promise inbox placement. Anti-spam and advertising law remain the user’s responsibility.

## Output Format

```
Subject: {{subject}}

---

{{body}}

---

Assumptions / placeholders:
- ...
```

DMs: first line is `DM:` not `Subject:`.

Optional: one alternate subject on a single line. Do not translate the body unless asked.

## Quality Bar

- [ ] Subject (or DM opener) and full body
- [ ] Opener proves the content was watched, or `{{content_hook}}` is still marked
- [ ] Brand blurb ≤ 2 sentences
- [ ] One CTA
- [ ] No spam words, no ALL CAPS, ≤ 1 exclamation mark
- [ ] No invented fees, metrics, legal terms, or unwatched content
- [ ] Follow-up shorter than the first email
- [ ] Professional, not salesy
- [ ] List outreach: a distinct hook per creator

## Additional Resources

- Subject lines: `references/subject-lines.md`
- Follow-up cadence: `references/follow-up-sequence.md`
- YouTube / Instagram / TikTok: `references/platform-notes.md`
- Templates: `assets/email-template.md`
- Install: `README.md`
