# influencer-outreach-email-skill

[English](README.md) | **简体中文** | [日本語](README.ja.md)

为海外创作者（YouTube、Instagram、TikTok 等）起草商务合作邮件。语言跟随达人市场——英语、对方语言、或双语——不再默认只出英文。

Agent 应在出现合作意向时触发——influencer outreach、brand collaboration、「联系这个 YouTuber」——并返回可直接复制的 **Subject + 正文**，而不是策略备忘。

仓库根目录**就是**该 Skill。文件夹名须保持 `influencer-outreach-email-skill`，以便与 `SKILL.md` 中的 `name` 一致。

## 覆盖范围

| 阶段 | 内容 |
|------|------|
| 冷启动 | 付费、寄样、联盟、长期合作的第一步、经理/机构 |
| 跟进 | 未回复时的 #2 / #3 / breakup |
| 条款 | 交付物、档期、费用、使用权 |
| 寄送 | 样品物流跟踪 |
| 对方已回复 | 先要 media kit、再谈 brief / 报价、转经理、拒绝 |
| 私信 | 应用内短文案；Nano / Micro 且无邮箱时优先 |

## 目录

```
influencer-outreach-email-skill/
├── SKILL.md                      # Agent 指令
├── README.md                     # 安装与用法（英文）
├── README.zh-CN.md               # 中文
├── README.ja.md                  # 日文
├── references/
│   ├── subject-lines.md
│   ├── follow-up-sequence.md
│   └── platform-notes.md
└── assets/
    └── email-template.md         # 占位符与完整示例
```

## 安装

推荐（克隆本仓库并安装 Skill）：

```bash
npx skills add sendsoon/influencer-outreach-email-skill
```

用户级安装到 Claude Code 与 Codex（Windows 若 symlink 失败请加 `--copy`）：

```bash
npx skills add sendsoon/influencer-outreach-email-skill -g -a claude-code -a codex -y
```

手动安装时，将 `SKILL.md`、`README.md`（需要本地化文档时一并复制 `README.zh-CN.md` / `README.ja.md`）、`references/`、`assets/` 拷入客户端会扫描的 skills 目录。`SKILL.md` 必须位于 Skill 文件夹根目录。安装后请新开 Agent 会话（Codex 需重启）。

以下手动命令在本仓库根目录执行。Windows 用 PowerShell，macOS / Linux 用 bash。

### 路径

| 客户端 | 用户级 | 项目级 |
|--------|--------|--------|
| Codex | `~/.codex/skills/<name>/` 与 `~/.agents/skills/<name>/` | `.agents/skills/<name>/` |
| Claude Code | `~/.claude/skills/<name>/` | `.claude/skills/<name>/` |
| 其他 Agent Skills 客户端 | 该产品文档中的用户级 skills 目录 | 该产品文档中的项目级 skills 目录 |

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

项目级安装路径：`.agents/skills/influencer-outreach-email-skill/`。

若仓库已在 GitHub，也可用 `$skill-installer`；完成后重启 Codex。Skill 未出现时，检查 `~/.codex/config.toml` 是否启用 skills（部分版本需 `[features] skills = true`）。

### Claude

**Claude Code** — 复制到 `~/.claude/skills/influencer-outreach-email-skill/`（用户级）或 `.claude/skills/influencer-outreach-email-skill/`（仓库级）。

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

斜杠命令：`/influencer-outreach-email-skill`。若未出现，执行 `/reload-plugins` 或重开会话。

**Claude.ai** — 需 Pro / Max / Team / Enterprise，并已开启 Skills（以产品设置为准）。

1. 将本文件夹打成 zip，解压后应看到 `SKILL.md` 或 `influencer-outreach-email-skill/SKILL.md`。
2. [claude.ai](https://claude.ai) → **Settings** → **Capabilities**（有的界面为 **Features**）→ **Skills**。
3. 上传 zip。自定义 Skill 仅对当前账号生效，不会同步到 Claude Code。

### 其他 Agent

按该产品文档中的 skills 目录拷贝本文件夹（遵循 Agent Skills 规范），或：

```bash
npx skills add sendsoon/influencer-outreach-email-skill
```

用户级安装加 `-g`。`--agent` 取值以 `npx skills --help` 为准。

## 输入

- 品牌 / 产品及 1–2 句卖点
- 创作者姓名、平台、内容风格（最好有一条实际看过的内容）
- 粉丝量或预估层级（Nano / Micro / Mid / Macro）
- 合作形式：付费 / 寄样 / 联盟 / 长期
- 写给创作者本人还是经理 / MCN
- 费用区间（如有）
- CTA：回复、通话或链接

信息不全时，Agent 最多追问 1–3 个问题，并用 `{{brand_name}}`、`{{creator_name}}`、`{{collab_type}}` 等占位符出稿。

## 输出

```
Subject: ...

---

<邮件正文>

---

Assumptions / placeholders:
- ...
```

私信第一行为 `DM:`。语气：对等、专业；正式程度跟随达人量级。避免垃圾邮件用语（`FREE`、`$$$`、`ACT NOW`）。冷启动 80–150 词；跟进更短。日韩 / 拉美 / 东南亚达人：用户未指定语言时同时出英语版 + 目标语言版。

## 跟进节奏

| 触达 | 时间 | 写法 |
|------|------|------|
| #1 | Day 0 | 完整邮件 |
| #2 | 3–5 天 | 更短，补一条新信息 |
| #3 | 再过 4–6 天 | 3–6 句，不施压 |
| #4 breakup | 再过 5–7 天 | 收尾后停止 |

同一线索最多四封。细则见 `references/follow-up-sequence.md`。

## 示例请求

- Help me partner with this YouTuber
- Draft a seeding email for this Instagram creator
- Follow up with last week’s KOL
- Confirm terms and send them over
- They replied with a rate — draft the response
- Make this an Instagram DM

## 不在范围内

- 代发邮件、爬取或验证创作者邮箱
- 群发同一正文（每位创作者须有独立钩子）
- 编造视频、费用或法律条款
- 对可能未满 18 岁的创作者做商务建联（先确认年龄/监护；付费合作应咨询法务）
