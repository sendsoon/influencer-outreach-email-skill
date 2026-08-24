---
name: influencer-outreach-email-skill
description: "Writes copy-paste-ready creator/KOL outreach emails (cold outreach, follow-ups, terms, seeding, affiliate) in English or the creator’s language. Use when the user wants to contact, reach out to, pitch, or partner with a YouTube, Instagram, or TikTok creator — even if they never say write an email. Triggers: influencer outreach, brand collaboration, influencer partnership, KOL邮件, 达人合作, 网红建联, 联系 YouTuber, 寄样测评, 跟进达人. Output Subject + body."
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

Iterate subject lines with `references/subject-lines.md`. Affiliate, ongoing, and manager letters: matching sections in `assets/email-template.md`.

## Workflow

1. **Stage**: cold / follow-up (#2) / closing (#3) / terms / shipment / reply.
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

| Tier | Followers | First-touch tone |
|------|-----------|------------------|
| Nano | <10k | Light, peer. No exclusivity, usage rights, or legal-heavy terms |
| Micro | 10k–100k | Same as Nano |
| Mid | 100k–500k | Current professional tone |
| Macro / Mega | 500k+ or agency | More formal. Surface a budget range early if the user supplied one |

Unknown tier: Mid tone; note in Assumptions.

## Follow-up Logic

Use only if there is no reply and no explicit no.

| Touch | When | Shape |
|------|------|--------|
| #1 | Day 0 | Full structure, 80–150 words |
| #2 | 3–5 days later | Second follow-up. Shorter; one new fact (sample, window, brief) |
| #3 | 4–7 days after #2 | Closing note. Close the loop; then stop |

Max **three** emails per thread, then stop. Do not ask “did you get this?” or fake scarcity. Copy: `references/follow-up-sequence.md`.

## After They Reply

A reply is not a new cold email. Thank them in the first sentence, match their length, and ask **one** next thing. Do not stack media kit + brief + call + shipping form in the same note. Do not invent a counter-offer, a priced brief, or a publish date the user never set.

Templates: `assets/email-template.md` (media kit, brief confirm, rate hold, decline thank-you, terms, manager, seeding).

### How to answer

**Interested / “sounds good” / “send more”**
- No authorized budget: do **not** send Terms or a priced brief. Thank them, then request a media kit, rate card, or 1–2 recent brand collabs so the next note matches how they actually work.
- Budget already authorized: thank them, restating collab type + platform in one line. If deliverables are already agreed, use Terms. If not, send a short brief (talking points, not a script). One CTA: confirm the direction or reply with changes.

**They ask for a brief**
- A brief is 4–8 talking points plus the proposed deliverable (e.g. one dedicated integration). It is not a contract and not a feature dump.
- Include only user-supplied facts: product claims, must-says, banned claims, usage, exclusivity, deadlines. Unknown items stay as placeholders or “I’ll confirm and follow up.”
- Creative control: they keep their format; you provide talking points, not a word-for-word script unless the user insisted.
- CTA: `Does this direction work? Happy to adjust before we lock dates.`
- If budget is still missing, request a media kit **instead of** sending a fake-priced brief.

**They send a rate / rate card**
- Repeat their figure in the draft so the user sees it. List it under Assumptions.
- Authorized budget **covers** the rate → thank them and move to Terms with **that** number. Do not round, “improve,” or swap in a different fee.
- Authorized budget is **below** the rate, or there is **no** budget yet → do **not** invent a counter. Draft a hold: thank them, say you will check with the team, one CTA that you will come back. Then ask the user for an authorized number. Never write “we can do $X” unless the user typed $X.

**They ask product questions or want the brief confirmed**
- Answer only with user-supplied facts. One question from them → one answer + one CTA (confirm, or send the next asset).
- Do not add exclusivity, paid usage, or a deadline the user did not authorize.

**Forward to manager / agent**
- Thank the creator. If the manager’s name or email is missing, ask for it — that is the only CTA. Next email uses the Manager template and that address. Stop treating the personal inbox as the deal inbox.

**Wants the product first / seeding**
- Use the seeding or shipment template. Do not mix in a paid rate in the same note unless the user asked for a hybrid.

**Timing is off / “maybe later”**
- Offer **one** window (e.g. 4–6 weeks out). If they do not pick it, stop. Do not restart the three-email cadence.

**Clear no**
- Optional 2–3 sentence thank-you. Wish them well. No “I’ll check back next quarter” unless the user asked. Do not send remaining cadence emails.

| Signal | Next |
|--------|------|
| Interested, **no** user budget | Media kit / rate card / recent collabs first. Do not jump to Terms |
| Interested, budget authorized | Brief (talking points) or Terms — only user-supplied numbers |
| Rate card / quote received | Repeat the figure; never invent a counter; hold or Terms |
| Forward to manager / agent | Manager template; stop emailing the personal inbox only |
| Wants the product first | Seeding / shipment; do not chase a fee in the same note |
| Timing is off | One window 4–6 weeks out, then stop |
| Clear no | Short thank-you; stop |

## Channel

This skill drafts **email** copy (Subject + signature). It does not send, scrape contacts, or write blast scripts.

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

Language bilingual branch: output English first, then the target-language draft with the same structure (`Subject:` + body).

Optional: one alternate subject on a single line.

## Quality Bar

- [ ] Subject and full body
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
