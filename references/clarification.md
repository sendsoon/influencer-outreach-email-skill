# Clarification

Only **product / collaboration context** is required from the user. Creator fields should come from a **list or table** whenever one exists — not from a questionnaire.

Never invent emails, names, fees, video titles, follower counts, deadlines, cookie windows, or legal terms. Missing fields after the list is read become **stand-ins** (代称). Never leave `{{placeholders}}` in the pasted body. List every stand-in under Assumptions.

## Required (from the user)

A short description of **what the product is**, **what the collaboration is**, or both.

If even that is missing, ask **one** question: what is the product or the collaboration?

If **both** the product/collab brief **and** a creator list are missing, ask both in **one** turn, then wait. Do not add a third question.

## Data sources (creator + contact fields)

Users typically keep a CSV, Excel, TXT, database table, or a shared sheet (e.g. Google Sheets / Drive). Treat that as the source of truth for names, emails, handles, platforms, and other columns.

### Where to look (in order)

1. Files or links the user attached, pasted, or named in this turn.
2. An obvious list already in the workspace (`.csv`, `.xlsx`, `.xls`, `.tsv`, `.txt`, SQL dump, or a table they pointed at).
3. A Google Sheets / Drive / shared-form URL they provided.

Do not scrape private drives or guess unpublished URLs. If a sheet URL is behind login, ask them to export CSV or paste the tab — do not bypass access.

If **no data source is in play**, ask **once**:

> Do you have a creator list to use (CSV, Excel, TXT, database table, or a Google Sheet / shared form)? If yes, drop the file or link here and I will pull the fields from it.

Then wait. Do not draft in the same turn as this question unless they already said they have no list. If they say no or skip: draft from the product/collab brief + stand-ins. Do **not** ask for individual fields (name, fee, video, sender) instead of a list.

### After they add a source

Read it and map columns (headers vary; match by meaning, case-insensitive):

| Need | Typical column names |
|------|----------------------|
| Creator name | name, creator, influencer, KOL, 达人, 姓名 |
| Handle | handle, channel, username, @, YouTube, Instagram, TikTok |
| Platform | platform, channel type, 平台 |
| Email | email, mail, 邮箱, business email |
| Followers / tier | followers, subs, 粉丝 |
| Manager | manager, agency, MCN, 经纪人 |
| Notes / hook | notes, content, video, 备注, 作品 |
| Language / region | language, country, market, 地区 |

One **row** = one creator = **one email**. Never a shared blast body.

Pull every mapped field into the draft. If the row includes an email, also list `To: {email}` under Assumptions (this skill still does not send). If a column is empty or absent **after** this pass: use stand-ins. **Do not ask again** for those gaps.

## Optional extras (chat, not the list)

Still enrich from the message when present (collab type, fee, sender, CTA, language). Do not quiz for them. After the list is read, leftover gaps → stand-ins only.

## Stand-ins (when a field is still missing)

Use the matching language of the draft. Do not mix `{{creator_name}}` into a finished email.

| Missing field | English | 简体中文 (other languages: the same kind of noun) |
|---------------|---------|---------------------------------------------------|
| Creator name | Greeting `Hi there,`; refer to **the creator** | 称呼 `您好，`；正文称 **创作者** |
| Handle / channel | **your channel** | **您的频道** |
| Platform | **your audience** | **您的观众** |
| Content hook | **your recent work** — no fake title | **您最近的内容** — 不编标题 |
| Collab type | **a collaboration** | **一次合作** |
| Proposal / deliverable | **a dedicated integration** only if that was implied; else **a collaboration** | **一次合作** |
| Product name (brand known) | the product, or the brand name | **该产品** / 品牌名 |
| Fee / commission / cookie | Omit the money sentence | 不写酬劳句 |
| Sender name | **Partnerships** | **合作负责人** |
| Sender title | omit | 省略 |
| Sender company | the brand name | 品牌名 |
| Sender email | omit the email line | 不写邮箱行 |
| Manager name | `Hi there,`; **the manager** | `您好，`；**经纪人** |
| Timeline / publish window | **a window that works for you** | **合适的档期** |
| Tracking number | omit or “the tracking number” | **物流单号** |
| Follow-up new fact | Skip the “One update:” sentence | 不写「有一条新进展」 |

Unknown collab type: “a collaboration” / 「一次合作」. Unknown creator: never `Dear Influencer`.

## When they add or update the list later

If the user uploads a new file, pastes more rows, or fills empty cells, **re-read the source**, replace matching stand-ins, and re-issue Subject + body for the affected creator(s). Do not stall while waiting for a perfect table.
