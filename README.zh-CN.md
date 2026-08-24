# influencer-outreach-email-skill

[English](README.md) | **简体中文** | [日本語](README.ja.md)

为品牌起草可直接复制粘贴的 **Subject + 正文**，用于联系海外创作者（YouTube、Instagram、TikTok 等）谈商务合作。

**主要功能**

- 冷启动建联：付费合作、寄样测评、联盟返佣、长期合作的第一步，或写给经理 / MCN
- 未回复时：第二封跟进、最后一封收尾（同一线索最多三封）
- 条款确认：交付物、档期、酬劳、使用权
- 样品已寄出 / 物流跟踪通知
- 对方已回复后的妥善回信：先致谢、一次只问一件事；要 media kit / 报价卡再谈 brief；有授权预算才确认条款；不擅自还价；明确拒绝则礼貌结束、不再跟进

每封针对一位创作者单独写。信息不全时最多追问 1–3 个问题，其余用占位符出稿。

## 安装

```bash
npx skills add sendsoon/influencer-outreach-email-skill
npx skills update influencer-outreach-email-skill
```

## 示例

**输入**

```
品牌：SendSoon — 比 SendGrid / Klaviyo 更便宜的海外 EDM
达人：Arun Maini，YouTube「Mrwhosetheboss」（@Mrwhosetheboss），约 2280 万粉，科技评测
看过：Google Pixel 11 Hands on — The Phone Crisis Begins；指出 11 Pro 无线充电「快 29%」只适用于较小的 Pro，XL 小字是 17%
合作：付费植入一条 + 联盟返佣
收件人：Arun 本人
酬劳：USD 100–500
佣金：10%，有效期 30 天
CTA：短回复即可
品牌链接：https://sendsoonai.com/
发件人：Charles Zhou，Partnerships，SendSoon，charles@mail.sendsoonai.com
```

**输出**

```
Subject: Arun — Pixel 11 small print + SendSoon

---

Hi Arun,

I watched your Pixel 11 hands-on — catching that the “29% faster wireless charging” only applies to the smaller Pro, while the XL is 17% in the small print, is exactly the kind of test we’d want to keep.

SendSoon is an overseas EDM platform — email infrastructure for campaigns and transactional mail, typically around 60% of comparable SendGrid cost and about 80% of comparable Klaviyo (https://sendsoonai.com/). I'm reaching out about a paid + affiliate collaboration with Mrwhosetheboss: one dedicated integration. You'd keep your usual review format; we'd provide talking points and a unique link, not a script. We had USD 100–500 plus 10% commission on referred sales (30-day cookie) in mind.

If this is relevant, a short reply is enough. I can send a one-page brief with talking points (not a rigid script).

Best,
Charles Zhou
Partnerships, SendSoon
charles@mail.sendsoonai.com
```

