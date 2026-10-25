# LinkedIn 官方 API 自动发布 — 授权指引 + 帖子文案

## 一、你需要完成的一次性授权（约 20 分钟，需登录你的 LinkedIn 账号）

> 我无法替你完成这一步，因为 LinkedIn 要求开发者应用绑定你的真实账号并需人工审核。完成后把凭据给我，后续 4 篇我可以自动发。

### 第 1 步：创建开发者应用
1. 打开 https://www.linkedin.com/developers/apps → **Create app**
2. 填写：App name（如 `Wirsh Content Publisher`）、LinkedIn Page（选你的公司主页，没有可先选个人）、App logo
3. 创建后进入 App 的 **Products** 页，申请 **Share on LinkedIn**（个人发帖权限 `w_member_social`）——可能需要 LinkedIn 审核，通常几分钟到几天

### 第 2 步：配置 OAuth
1. App 的 **Auth** 页记下 **Client ID** 和 **Client Secret**（Secret 只显示一次，立即保存）
2. 在 **OAuth 2.0 settings** 里把 Redirect URL 先填 `https://www.linkedin.com/developers/tools/oauth`（或你自己的回调地址）

### 第 3 步：获取授权 Token（一次性，我用它发帖）
1. 访问授权链接（把 `{CLIENT_ID}` 换成你的）：
```
https://www.linkedin.com/oauth/v2/authorization?response_type=code&client_id={CLIENT_ID}&redirect_uri=https%3A%2F%2Fwww.linkedin.com%2Fdevelopers%2Ftools%2Foauth&scope=w_member_social%20openid%20profile%20email
```
2. 登录并同意授权后，浏览器地址栏会带 `?code=XXXX`
3. 把这个 `code` 和 Client ID/Secret 一起给我（或按第 4 步自己换 token）

### 第 4 步（可选）自己换 Token
```bash
curl -X POST https://www.linkedin.com/oauth/v2/accessToken \
  -F grant_type=authorization_code \
  -F code={STEP3_CODE} \
  -F redirect_uri=https://www.linkedin.com/developers/tools/oauth \
  -F client_id={CLIENT_ID} \
  -F client_secret={CLIENT_SECRET}
```
返回 `{"access_token": "..."}`。把 access_token 给我即可，或存到服务器环境变量 `LINKEDIN_ACCESS_TOKEN`。

> ⚠️ Token 有时效（默认约 60 天可刷新）。长期自动发需要 refresh_token；先按一次性授权跑通，后续要长期自动化再配刷新。

---

## 二、4 篇帖子文案（LinkedIn 风格，可直接发布）

### 帖子 1（对应 blog1 选购指南）
> **标题**：Which Geimori grinder should you buy? We asked 635 verified customers.
>
> Espresso-only on a budget? GU38. Espresso + filter with room to grow? GU63. No outlet nearby? T38. Flat-burr clarity without the pro price? GU64.
>
> The honest answer is always the same: there's no best grinder, only the best grinder for your workflow. Full breakdown with verified ratings 👇
>
> #coffee #espresso #grinder #homebarista #specialtycoffee
> (附仓库链接 https://github.com/sunnysunsunsunny2023-dotcom/geimori-blogs)

### 帖子 2（对应 blog2 单剂量研磨）
> **标题**：Single-dose grinding: the 3-second tip that changes your morning cup
>
> Weigh → grind → pump the bellows 3-4 times. That's the routine our most satisfied customers swear by.
>
> Single-dose means what you grind is what you brew — fresher coffee, no stale hopper mix, and the freedom to switch beans anytime. Dialing in a new bag? Change one variable at a time; in 2-3 tries you'll hit the sweet spot.
>
> #coffee #singledose #espresso #grinding #coffeelovers

### 帖子 3（对应 blog3 客户反馈）
> **标题**：What 635 verified reviews taught us about our coffee gear
>
> Across 635 verified reviews we hold 4.2/5 — but the average hides the useful part. Customers repeat two phrases more than any others: "easy to use" and "works well."
>
> We also listen to the low-star feedback: clearer multi-language manuals, stricter packaging checks, proactive shipping updates, and QC reviews of affected batches. That's how you turn complaints into better products.
>
> #customerreviews #coffee #smallbusiness #qualityfirst #ecommerce

### 帖子 4（对应 blog4 家用意式 troubleshooting）
> **标题**：Fix the 5 most common home espresso problems (no technician needed)
>
> 1. Dial drifting? Recalibrate the zero point, brush the collar.
> 2. Retention? Pump the bellows 3-4 times after grinding.
> 3. Sour or bitter? Change one variable at a time — grind finer or coarser.
> 4. Weak steam? It's milk residue, not a broken machine — purge and descale.
> 5. Lingering flavors? 3-5g purge dose of the new beans.
>
> Most espresso problems have simple fixes. Save this for the next morning shot.
>
> #espresso #coffee #homebarista #troubleshooting #barista

---

## 三、拿到 Token 后我会做什么
1. 写一个小脚本（或直接 curl）调用 LinkedIn **Posts API**（新版，POST https://api.linkedin.com/rest/posts）
2. 逐篇发 4 条帖子（`author=urn:li:person:{你的ID}`，`visibility=PUBLIC`）
3. 验证每条发布成功并回传帖子链接
4. 视你意愿挂到 Calendar/CodeAct 做定期发布

> 发布是公开对外操作，每次执行前我都会先跟你确认内容与时间，不会静默代发。
