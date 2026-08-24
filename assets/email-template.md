# Email Templates

Replace `{{placeholders}}`; leave them in place when unknown. Do not invent facts. Language follows `SKILL.md` (English, target language, or both).

Always include a `Subject:` line. Format: `SKILL.md` → Output Format.

## Variable Glossary

| Placeholder | Meaning |
|-------------|---------|
| `{{brand_name}}` | Brand |
| `{{product_name}}` | Product (may match the brand) |
| `{{value_prop}}` | One-sentence value, not a feature list |
| `{{creator_name}}` | Greeting name (not `@handle` as Dear) |
| `{{handle}}` | Channel name or @handle |
| `{{platform}}` | YouTube / Instagram / TikTok |
| `{{content_hook}}` | A real piece of content plus a concrete detail |
| `{{content_theme}}` | Usual topics, e.g. tech reviews |
| `{{new_info}}` | Follow-up increment (sample, window, brief, unique link) |
| `{{collab_type}}` | paid collaboration / product seeding / affiliate / paid + affiliate / ongoing partnership |
| `{{proposal}}` | One-line deliverable, e.g. one dedicated integration |
| `{{creator_value}}` | Fee, product, creative control, audience fit |
| `{{fee_range}}` | Only if the user supplied it; otherwise delete the sentence |
| `{{cta}}` | Single action; default: reply to this email |
| `{{timeline}}` | Target window |
| `{{deliverables}}` | Terms: count and specs |
| `{{publish_window}}` | Terms: go-live window |
| `{{usage_rights}}` | Terms: organic / paid / etc. |
| `{{tracking_number}}` | Shipment |
| `{{sender_name}}` | Sign-off name |
| `{{sender_title}}` | e.g. Partnerships |
| `{{sender_company}}` | Brand or agency |
| `{{sender_email}}` | Reply-to |
| `{{calendar_link}}` | Only when the CTA is a call |
| `{{manager_name}}` | Agent / MCN greeting |
| `{{affiliate_terms}}` | Affiliate: commission and cookie window (user-supplied) |

Paid, affiliate, follow-up, and terms filled examples use SendSoon × Mrwhosetheboss. Copy tone, not fees or dates, onto a different brand. Seeding filled examples are a physical product only — never mix them into a SaaS pitch.

---

## 1. First Outreach — Paid Collaboration

```
Subject: {{creator_name}} — idea for a {{brand_name}} collab

---

Hi {{creator_name}},

{{content_hook}}.

{{brand_name}} makes {{product_name}} — {{value_prop}}. I'm reaching out about a {{collab_type}} with {{handle}}: {{proposal}}. {{creator_value}}{{fee_range}}

If this is relevant, {{cta}}.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

Fee line (only if a budget exists), appended after value: ` We had {{fee_range}} in mind, and I'm open to a number that fits your rate card.`

Default CTA: `a short reply is enough`. Do not add a second CTA (brief, call, or link) unless that is the only CTA the user asked for. Call CTA only if requested: `a 15-minute call works — here's my calendar: {{calendar_link}}`.

### Filled example

```
Subject: Arun — Pixel 11 small print + SendSoon

---

Hi Arun,

I watched your Pixel 11 hands-on — catching that the “29% faster wireless charging” only applies to the smaller Pro, while the XL is 17% in the small print, is exactly the kind of test we’d want to keep.

SendSoon is an overseas EDM platform — email infrastructure for campaigns and transactional mail, typically around 60% of comparable SendGrid cost and about 80% of comparable Klaviyo (https://sendsoonai.com/). I'm reaching out about a paid + affiliate collaboration with Mrwhosetheboss: one dedicated integration. You'd keep your usual review format; we'd provide talking points and a unique link, not a script. We had USD 100–500 plus 10% commission on referred sales (30-day cookie) in mind.

If this is relevant, a short reply is enough.

Best,
Charles Zhou
Partnerships, SendSoon
charles@mail.sendsoonai.com
```

---

## 2. First Outreach — Product Seeding

Seeding is try-and-see, not a paid ad. No posting requirement. **Physical product only** — do not reuse this example on SendSoon or any SaaS brand.

```
Subject: {{brand_name}} × {{creator_name}}: product seeding

---

Hi {{creator_name}},

{{content_hook}}.

I'd like to send you {{product_name}} from {{brand_name}} to try. {{value_prop}}. This is {{collab_type}} — no posting requirement. If you do share something, please keep it in your own voice.

If you're open to receiving a sample, {{cta}} with a shipping address or a form link. No ID or payment details needed at this stage.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

### Filled example

```
Subject: Northstar × Maya: product seeding

---

Hi Maya,

Your pour-over Reel last Tuesday — the overhead grind shot and the quiet caption — is close to how we show the kettle.

I'd like to send you the Northstar gooseneck kettle to try. It holds brew temperature steady enough for repeatable recipes at home. This is product seeding — no posting requirement. If you do share something, please keep it in your own voice.

If you're open to receiving a sample, a short reply with a shipping address or a form link is enough. No ID or payment details needed at this stage.

Best,
Jordan Hale
Partnerships, Northstar
jordan@northstar.example
```

---

## 3. Follow-up

Full cadence (second follow-up, then closing): `references/follow-up-sequence.md`. Cap: three emails including the first. This section is touch #2.

```
Subject: Following up: {{brand_name}} × {{creator_name}}

---

Hi {{creator_name}},

I know inbox volume is high, so I wanted to send a shorter note.

We're still interested in a {{collab_type}} around {{content_theme}}. One update: {{new_info}}.

If the timing is off, no need to reply. If useful, a short reply is enough.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
```

### Filled example (#2)

```
Subject: Following up: SendSoon × Arun

---

Hi Arun,

I know inbox volume is high, so I wanted to send a shorter note.

We're still interested in a paid + affiliate integration around your tech reviews. One update: we can share a unique link and a one-page talking-points list as soon as you want them.

If the timing is off, no need to reply. If useful, a short reply is enough.

Best,
Charles Zhou
Partnerships, SendSoon
```

### Touch #3 (closing)

Copy: `references/follow-up-sequence.md`. Do not send a “checking in” email between #2 and #3.

```
Subject: Closing the loop — {{brand_name}}

---

Hi {{creator_name}},

I'll close the loop on the {{brand_name}} idea so I don't add noise.

If a {{collab_type}} becomes useful later, I'm easy to reach at {{sender_email}}. Wishing you good filming weeks ahead.

Best,
{{sender_name}}
```

---

## 4. Collaboration Terms Confirmation

Record only what both sides agreed or the user supplied. Unset items stay as placeholders and are listed in Assumptions.

```
Subject: Confirming deliverables and timeline — {{brand_name}}

---

Hi {{creator_name}},

Thank you for being open to a {{collab_type}} with {{brand_name}}. I'm writing to confirm the details so we're aligned before anything goes live.

• Deliverables: {{deliverables}}
• Target publish window: {{publish_window}}
• Compensation: {{fee_range}}
• Usage: {{usage_rights}}
• Disclosure: paid partnership disclosure per {{platform}} rules

Please reply to confirm or mark anything that should change. Once this is locked, I'll send the sample / brief / contract next (whichever applies).

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

### Filled example

```
Subject: Confirming deliverables and timeline — SendSoon

---

Hi Arun,

Thank you for being open to a paid + affiliate collaboration with SendSoon. I'm writing to confirm the details so we're aligned before anything goes live.

• Deliverables: 1 dedicated YouTube integration; unique affiliate link
• Target publish window: to confirm after you reply
• Compensation: USD 100–500 plus 10% commission on referred sales (30-day cookie)
• Usage: organic posting on your channel only; no paid amplification or whitelisting
• Disclosure: paid partnership disclosure per YouTube rules

Please reply to confirm or mark anything that should change. Once this is locked, I'll send the talking points and affiliate link next.

Best,
Charles Zhou
Partnerships, SendSoon
charles@mail.sendsoonai.com
```

---

## 5. Product Shipped (optional)

```
Subject: {{brand_name}} sample shipped — tracking inside

---

Hi {{creator_name}},

The {{product_name}} has shipped. Tracking: {{tracking_number}}.

No posting timeline on our side. When it arrives, a quick confirmation is helpful so I know it didn't get stuck in customs. If anything is missing or damaged, reply with a photo and I'll resend.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
```

---

## 6. First Outreach — Affiliate

Use only user-supplied commission figures. Do not invent cookie windows or “top creator earnings.”

```
Subject: Affiliate idea for {{handle}} + {{brand_name}}

---

Hi {{creator_name}},

{{content_hook}}.

{{brand_name}} makes {{product_name}} — {{value_prop}}. I'm reaching out about an affiliate partnership: {{affiliate_terms}}. You'd keep your usual format; we'd provide a unique link or code and talking points, not a script.

If a revenue-share collab is relevant, {{cta}}.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

---

## 7. First Outreach — Manager / Agency

```
Subject: {{brand_name}} × {{creator_name}}: {{collab_type}}

---

Hi {{manager_name}},

I'm reaching out about a possible {{collab_type}} between {{brand_name}} and {{creator_name}} ({{handle}}). {{content_hook}} — that audience fit is why we're writing you rather than sending a generic blast.

{{brand_name}} makes {{product_name}} — {{value_prop}}. Proposal: {{proposal}}. {{creator_value}}{{fee_range}}

If you represent this creator for brand deals, {{cta}}.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

---

## 8. First Outreach — Ongoing Partnership (first step only)

Cold email: first project only. No 12-month exclusivity or auto-renewal.

```
Subject: {{brand_name}} × {{creator_name}}: first integration, then option to continue

---

Hi {{creator_name}},

{{content_hook}}.

{{brand_name}} makes {{product_name}} — {{value_prop}}. I'd like to start with {{proposal}} and, if it feels right on both sides, leave the door open for more. No exclusivity requested at this stage. {{creator_value}}{{fee_range}}

If a first project is relevant, {{cta}}.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

---

## 9. Request Media Kit / Recent Work (before terms)

Use when they are interested, they have **not** sent a rate, and the user has not authorized a budget range. Do not send Terms in the same note. If they already quoted, use §11 instead.

```
Subject: {{brand_name}} — media kit / recent collabs?

---

Hi {{creator_name}},

Glad this might be a fit. Before we lock deliverables, could you share a media kit, rate card, or two recent brand collabs I can learn from? That helps me come back with a brief that matches how you actually work.

No need to send a full SOW yet — a short reply with those materials is enough.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

---

## 10. Confirm Brief (talking points, not a contract)

Use when they asked for a brief **and** the user has authorized a budget, or this is seeding (no fee). For a paid collab with no authorized budget, use §9, not this template. Do not invent fees, exclusivity, or dates.

```
Subject: Brief for {{handle}} — {{brand_name}}

---

Hi {{creator_name}},

Thanks for being open to this. Here's a one-page direction — talking points, not a script. Keep your usual format.

• Deliverable: {{proposal}}
• Window: {{timeline}}
• Talking points: {{content_theme}} + {{value_prop}}
• Creative: you lead the story; we'll flag any must-say / must-not-say claims

Does this direction work? Happy to adjust before we lock dates.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

Fee line (only if a budget exists): append ` Compensation would be {{fee_range}} unless your rate card suggests a better fit.`

---

## 11. Acknowledge a Rate (hold for budget)

Use when they quoted a number and the user has **not** authorized a matching budget. Do not invent a counter-offer.

```
Subject: Thanks — reviewing your rate

---

Hi {{creator_name}},

Thank you for sharing your rate. I've noted it and will check with the team so I can come back with a clear next step.

I'll follow up as soon as I have an answer.

Best,
{{sender_name}}
{{sender_title}}, {{sender_company}}
{{sender_email}}
```

Put their quoted figure under Assumptions. If the user’s budget already covers the rate, skip this template and use Terms instead.

---

## 12. Thank-you After a Decline

Use after a clear no. Then stop — do not send remaining cadence emails.

```
Subject: Thanks — {{brand_name}}

---

Hi {{creator_name}},

Thanks for the note — completely understood. Wishing you good filming weeks ahead.

Best,
{{sender_name}}
```

Do not add “I’ll check back next quarter” unless the user asked.

---

## Assembly Notes

- Empty `{{fee_range}}`: delete the sentence, or use `Happy to work from your rate card.` Seeding: omit money entirely.
- Affiliate: only numbers inside `{{affiliate_terms}}`. If none, write `happy to share the current affiliate terms` and flag the missing rate in Assumptions.
- Ongoing deals: section 8. No exclusivity, MFN, or auto-renewal in a cold email.
- Greeting: `Hi Arun,` when you have a name; infer from the handle if needed; otherwise `Hi there,` — never `Dear Influencer`. Managers: `Hi {{manager_name}},` — do not address them as the creator.
- One CTA per email. After they reply: thank first. Media kit = §9 (no quote yet); brief = §10; rate hold = §11 (they already quoted); decline = §12. Never invent a counter-offer.
- If the user has a brief or shipping-form URL, point the CTA there. Do not request passport, national ID, or bank details in the body.
- Scan the draft for leftover `{{placeholders}}`. Fill what you know; list anything still wrapped in `{{ }}` under Assumptions. Never send a body that still says `{{creator_name}}` as if it were the greeting.
