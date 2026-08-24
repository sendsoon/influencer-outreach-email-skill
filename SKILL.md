---
name: influencer-outreach-email-skill
description: "Writes copy-paste-ready creator/KOL outreach emails (cold outreach, follow-ups, terms, seeding, affiliate) in English or the creator’s language. Use when the user wants to contact, reach out to, pitch, or partner with a YouTube, Instagram, or TikTok creator — even if they never say write an email. Triggers: influencer outreach, brand collaboration, influencer partnership, KOL邮件, 达人合作, 网红建联, 联系 YouTuber, 寄样测评, 跟进达人. Output Subject + body, not a strategy memo."
---

# Influencer Outreach Email

Draft partnership emails to overseas creators. Return a copy-paste **Subject + body**. Do not lead with strategy.

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
2. **Language + tier**: infer from bio, video language, location, follower count. See Language and Creator Tier. Unknown is fine — do not block.
3. **Gaps**: read `references/clarification.md`. Ask at most **1–3** blocking questions; otherwise draft with placeholders.
4. **Load**: platform notes for first touch; follow-up sequence for nudges.
5. **Draft**: Subject, then body. Default **one** primary email (Language bilingual branch excepted). For a list, **one email per creator** — never a shared blast body.
6. **Check**: Guardrails + Quality bar, then Output format.

If brand + creator + intent are present, draft immediately. Extract name and platform from profile/video URLs; do not re-ask known facts.

Use only glossary names from `assets/email-template.md` (`{{content_hook}}`, `{{new_info}}`, etc.).

## Required Information

See `references/clarification.md` for when to ask vs draft, the 1–3 question cap, and the field map.

Do not invent fees, video titles, follower counts, deadlines, or legal terms.

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

**Personalization over formulas.** If a real content detail exists, write an original subject that cites it. The lines below are fallbacks — use them only when a specific hook is missing.

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

Adjust formality by Creator Tier. Do not put exclusivity or usage-rights clauses in a Nano/Micro cold email.

## Language

User named a language → that language only.

Creator market/language is clear from bio, video language, or location, and the user did not specify:

- English-speaking markets (US, UK, AU, CA, etc.): English.
- JP, KR, LATAM, SEA, or other clearly non-English: return **both** an English draft and a target-language draft. Native-language outreach usually converts better, especially Nano/Micro. Do **not** ship English-only plus “business language unconfirmed.”
- Mixed or unclear: if a question slot remains, ask. Otherwise English, and note that a native-language version may convert better.

Never invent fluency. Keep `{{placeholders}}` identical across both drafts.

## Creator Tier

Infer from a stated follower count, profile, or the user’s label. Do not invent a number.

| Tier | Followers | Channel | First-touch tone |
|------|-----------|---------|------------------|
| Nano | <10k | **DM** if no business email | Light, peer. No exclusivity, usage rights, or legal-heavy terms |
| Micro | 10k–100k | **DM** if no business email; else email | Same as Nano |
| Mid | 100k–500k | Email default | Current professional tone |
| Macro / Mega | 500k+ or agency | Email; more formal | Surface a budget range early if the user supplied one |

Unknown tier: email + Mid tone; note in Assumptions.

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
| Interested / wants a brief, **no** user budget range | Request media kit, rate card, or 1–2 recent brand collabs first. Do not jump to Terms. Template: `assets/email-template.md` |
| Interested / wants a brief, budget already authorized | Terms template; only user-supplied numbers |
| Rate card / quote received | Do not invent a counter. List the figure in Assumptions; ask for an authorized range |
| Forward to manager / agent | Manager template; stop emailing the personal inbox only |
| Wants the product first | Seeding / shipment template; do not chase a fee in the same note |
| Timing is off | One window 4–6 weeks out, then stop |
| Clear no | Stop. Optional 2–3 sentence thank-you; no further follow-up |

## Channel

- User named a channel → that channel.
- **Nano / Micro** and no business email on file → prefer **DM** (many small creators rarely check email).
- Otherwise default **email** (Subject + signature).
- **DMs**: not an email. Use `DM:` instead of `Subject:`, 40–80 words, one CTA, name + brand only — no long signature.
- This skill drafts copy. It does not send, scrape contacts, or write blast scripts.

## Guardrails

- If the creator may be under 18, stop and ask the user to confirm age or guardianship. Paid work: also tell the user to check legal (US COPPA; some EU states need written guardian consent and/or a work permit). Unpaid product seeding is usually lower risk, but still confirm age before drafting.
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

Language bilingual branch: output English first, then the target-language draft with the same structure (`Subject:` + body). DMs: first line is `DM:` not `Subject:`.

Optional: one alternate subject on a single line.

## Quality Bar

- [ ] Subject (or DM opener) and full body
- [ ] Every `{{placeholder}}` is filled or explicitly left and listed under Assumptions
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
- Clarification (what to ask): `references/clarification.md`
- YouTube / Instagram / TikTok: `references/platform-notes.md`
- Templates: `assets/email-template.md`
- Install: `README.md`
