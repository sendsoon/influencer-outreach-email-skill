# influencer-outreach-email-skill

[English](README.md) | [简体中文](README.zh-CN.md) | **日本語**

海外クリエイター（YouTube、Instagram、TikTok など）向けのパートナーシップメールを作成します。言語はクリエイターの市場に合わせます（英語、現地語、または両方）。英語専用ではありません。

エージェントは協業の意図（influencer outreach、brand collaboration、「この YouTuber に連絡して」）で起動し、戦略メモではなくコピー可能な **Subject + 本文** を返します。

リポジトリ直下**が**スキル本体です。フォルダ名は `influencer-outreach-email-skill` のままにし、`SKILL.md` の `name` と一致させてください。

## 対象範囲

| 段階 | 内容 |
|------|------|
| 初回アプローチ | 有償、シーディング、アフィリエイト、継続案件の第一歩、マネージャー／事務所 |
| フォローアップ | 未返信時の #2 / #3 / breakup |
| 条件確認 | 成果物、公開時期、報酬、利用権 |
| 発送 | サンプルの追跡番号 |
| 返信後 | メディアキット依頼、ブリーフ、レート、マネージャー転送、辞退 |
| DM | アプリ内の短い文面。Nano / Micro でメール不明なら優先 |

## 構成

```
influencer-outreach-email-skill/
├── SKILL.md                      # エージェント向け手順
├── README.md                     # インストールと使い方（英語）
├── README.zh-CN.md               # 中国語
├── README.ja.md                  # 日本語
├── references/
│   ├── subject-lines.md
│   ├── follow-up-sequence.md
│   ├── platform-notes.md
│   └── clarification.md          # 情報が足りないときの確認
└── assets/
    └── email-template.md         # プレースホルダと完成例
```

## インストール

推奨（このリポジトリを取得してスキルをインストール）:

```bash
npx skills add sendsoon/influencer-outreach-email-skill
```

Claude Code と Codex 向けのユーザーレベル（Windows で symlink が失敗する場合は `--copy` を追加）:

```bash
npx skills add sendsoon/influencer-outreach-email-skill -g -a claude-code -a codex -y
```

GitHub 上の最新版へ更新:

```bash
npx skills update influencer-outreach-email-skill
```

ユーザーレベル:

```bash
npx skills update influencer-outreach-email-skill -g -y
```

## 例

**入力**

```
Brand: Northstar — gooseneck kettle that holds brew temperature within 1°C
Creator: Maya Chen, YouTube “Weekend Brews”, ~85k, brew-gear reviews
Watched: water-temperature comparison, 92°C vs 96°C side-by-side
Collab: paid dedicated integration
Recipient: Maya
Fee: USD 3,500–4,500
CTA: short reply
```

**出力**

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
