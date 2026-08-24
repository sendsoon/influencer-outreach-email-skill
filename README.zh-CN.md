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
│   ├── platform-notes.md
│   └── clarification.md          # 信息不全时如何追问
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

更新到 GitHub 上的最新版本：

```bash
npx skills update influencer-outreach-email-skill
```

用户级：

```bash
npx skills update influencer-outreach-email-skill -g -y
```

## 示例

**输入**

```
品牌：Northstar — 恒温手冲壶，冲煮温度可稳定在 ±1°C
达人：Maya Chen，YouTube「Weekend Brews」，约 8.5 万粉，咖啡器具评测
看过：水温对比视频，92°C vs 96°C 并排测试
合作：付费植入一条
收件人：Maya 本人
酬劳：USD 3,500–4,500
CTA：短回复即可
```

**输出**

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
