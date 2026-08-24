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
│   └── platform-notes.md
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

手動インストールでは、`SKILL.md`、`README.md`（ローカライズ版が必要なら `README.zh-CN.md` / `README.ja.md` も）、`references/`、`assets/` を、クライアントがスキャンする skills ディレクトリへコピーします。`SKILL.md` はスキルフォルダの直下に置いてください。インストール後は新しいエージェントセッションを開始します（Codex は再起動）。

以下の手動コマンドは本リポジトリのルートで実行します。Windows は PowerShell、macOS / Linux は bash です。

### パス

| クライアント | ユーザーレベル | プロジェクトレベル |
|--------------|----------------|--------------------|
| Codex | `~/.codex/skills/<name>/` および `~/.agents/skills/<name>/` | `.agents/skills/<name>/` |
| Claude Code | `~/.claude/skills/<name>/` | `.claude/skills/<name>/` |
| その他の Agent Skills クライアント | 各製品ドキュメントのユーザースキルフォルダ | 各製品ドキュメントのプロジェクトスキルフォルダ |

`<name>` = `influencer-outreach-email-skill`。

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

プロジェクト導入先: `.agents/skills/influencer-outreach-email-skill/`。

GitHub 上にあれば `$skill-installer` も利用できます。完了後は Codex を再起動してください。スキルが出ない場合は `~/.codex/config.toml` で skills が有効か確認します（一部バージョンは `[features] skills = true`）。

### Claude

**Claude Code** — `~/.claude/skills/influencer-outreach-email-skill/`（ユーザー）または `.claude/skills/influencer-outreach-email-skill/`（リポジトリ）へコピーします。

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

スラッシュコマンド: `/influencer-outreach-email-skill`。表示されない場合は `/reload-plugins` またはセッションの再起動。

**Claude.ai** — Pro / Max / Team / Enterprise で Skills が有効であること（製品設定による）。

1. このフォルダを zip にする。展開後に `SKILL.md` または `influencer-outreach-email-skill/SKILL.md` が見えること。
2. [claude.ai](https://claude.ai) → **Settings** → **Capabilities**（画面によっては **Features**）→ **Skills**。
3. zip をアップロード。カスタムスキルはアカウント単位で、Claude Code には同期されません。

### その他のエージェント

各製品ドキュメントの skills ディレクトリへこのフォルダをコピーするか、次を実行します（Agent Skills 仕様）:

```bash
npx skills add sendsoon/influencer-outreach-email-skill
```

ユーザーレベルは `-g`。`--agent` の値は `npx skills --help` で確認してください。

## 入力

- ブランド／製品と 1–2 文の価値提案
- クリエイター名、プラットフォーム、コンテンツの傾向（実際に見た作品があるとよい）
- フォロワー数または推定ティア（Nano / Micro / Mid / Macro）
- 協業形態: 有償 / シーディング / アフィリエイト / 継続
- 宛先が本人かマネージャー／MCN か
- 報酬レンジ（任意）
- CTA: 返信、通話、またはリンク

不足がある場合、エージェントは最大 1–3 問だけ確認し、`{{brand_name}}`、`{{creator_name}}`、`{{collab_type}}` などのプレースホルダで下書きします。

## 出力

```
Subject: ...

---

<メール本文>

---

Assumptions / placeholders:
- ...
```

DM の先頭行は `DM:` です。トーンは対等で専門的。フォーマリティはクリエイターのティアに合わせます。スパム表現（`FREE`、`$$$`、`ACT NOW`）は使いません。初回は 80–150 語、フォローアップはより短く。日韓・LATAM・SEA のクリエイターでは、ユーザーが言語を指定していなければ英語版と現地語版の両方を出します。

## フォローアップ間隔

| 通数 | 時期 | 形 |
|------|------|------|
| #1 | Day 0 | 全文 |
| #2 | 3–5 日後 | 短く、新しい情報を 1 点 |
| #3 | さらに 4–6 日後 | 3–6 文、圧力なし |
| #4 breakup | さらに 5–7 日後 | 締めのあと停止 |

同一スレッドは最大 4 通。詳細は `references/follow-up-sequence.md`。

## プロンプト例

- Help me partner with this YouTuber
- Draft a seeding email for this Instagram creator
- Follow up with last week’s KOL
- Confirm terms and send them over
- They replied with a rate — draft the response
- Make this an Instagram DM

## 対象外

- メール送信、スクレイピング、クリエイターメールの検証
- 同一文面の一斉送信（クリエイターごとに異なるフック）
- 見ていない動画、報酬、法務条項の捏造
- 18 歳未満の可能性があるクリエイターへの商用アプローチ（年齢／保護者を確認。有償案件は法務確認を促す）
