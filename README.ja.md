# influencer-outreach-email-skill

[English](README.md) | [简体中文](README.zh-CN.md) | **日本語**

海外クリエイター（YouTube、Instagram、TikTok など）とのブランド協業向けに、コピー可能な **Subject + 本文** を作成します。

**主な機能**

- 初回アプローチ：有償協業、シーディング、アフィリエイト、継続案件の第一歩、マネージャー／MCN 宛
- 未返信時：2 通目のフォロー、最後の締め（同一スレッドは最大 3 通）
- 条件確認：成果物、公開時期、報酬、利用権
- サンプル発送・追跡番号の通知
- 返信後の適切な返答：先に礼を述べ、1 通につき依頼は 1 つ。まだ見積もりがなく予算未承認ならメディアキット／レートカードを依頼。見積もり済みなら保留または条件確定。勝手に値下げしない。明確な辞退には短い礼で止め、再追わない

1 通につき 1 人のクリエイター。製品または協業の説明があれば下書きする。追加情報があれば本文を厚くし、なければ「the creator / クリエイター」などの代称を使う。先に質問しない。

## インストール

```bash
npx skills add sendsoon/influencer-outreach-email-skill
npx skills update influencer-outreach-email-skill
```

## 例

**入力**

```
ブランド：SendSoon — SendGrid / Klaviyo より安い海外 EDM
クリエイター：Arun Maini、YouTube「Mrwhosetheboss」（@Mrwhosetheboss）、約 2,280 万、テックレビュー
視聴：Google Pixel 11 Hands on — The Phone Crisis Begins。「無線充電 29% 高速」は小さい Pro のみ、XL は注記で 17%
協業：有償インテグレーション 1 本 + アフィリエイト
宛先：Arun 本人
報酬：USD 100–500
コミッション：10%、Cookie 30 日
CTA：短い返信で十分
ブランド URL：https://sendsoonai.com/
差出人：Charles Zhou, Partnerships, SendSoon, charles@mail.sendsoonai.com
```

**出力**

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

---

Assumptions / stand-ins:
- None
```
