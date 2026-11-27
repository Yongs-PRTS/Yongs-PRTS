<div align="center">

# Hi, I'm Yongs-PRTS 👋

**AI Coding 工作流实战 · 独立开发降本折腾 · 开源效率脚本与排错笔记**

[![Offline 2FA & Guides](https://img.shields.io/badge/Free_Tools-Offline_2FA_%26_15_Docs-0969DA?style=flat-square&logo=gitbook&logoColor=white)](https://young777.duckdns.org/?tab=help)
[![Self-Service Portal](https://img.shields.io/badge/StarWay-Self--Service_Portal-10B981?style=flat-square&logo=lightning&logoColor=white)](https://young777.duckdns.org/)
[![WeChat](https://img.shields.io/badge/WeChat-YyFBI007-07C160?style=flat-square&logo=wechat&logoColor=white)](#contact)
[![QQ](https://img.shields.io/badge/QQ-2748178842-12B7F5?style=flat-square&logo=tencentqq&logoColor=white)](#contact)
[![Telegram](https://img.shields.io/badge/Telegram-@younage-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/younage)
[![X](https://img.shields.io/badge/X-@PPrisses69263-111111?style=flat-square&logo=x&logoColor=white)](https://x.com/PPrisses69263)

</div>

---

### 🧭 我在折腾什么

平时主要深耕 **AI Coding 终端与 IDE 工作流**（`Codex CLI` / `Claude Code` / `Antigravity` / `Gemini` / `Cursor`），以及 Node.js / Python 零依赖工程效率脚本。

这个主页用来沉淀我在稀土掘金持续更新的**一手实测文章、开箱即用脚本与配置模板、免费离线工具与防封排错文档**，帮你少踩环境配置、网络风控与订阅账单的坑。

---

### 🔥 精选实战笔记（稀土掘金持续更新）

| 方向 | 文章标题 | 核心看点 |
| :--- | :--- | :--- |
| **工程源码** | [Codex CLI + Node.js 实战：写一个 80 行自动 Code Review 与单测补全脚本（附完整源码）](https://juejin.cn/post/7712354269614342159) | 零依赖跨平台脚本、`--sandbox read-only` 防误改、`pre-commit` `[P0]` 阻断、`--test` 补单测 |
| **选型降本** | [每月花 150 还是 1500？2026 程序员最省钱的 AI 编程全家桶组合实测](https://juejin.cn/post/7712353300062027802) | 三档月预算实测对比、主副模型高低配分流策略、月省 80% 账单 |
| **防封排错** | [别再裸登把号搞封了！Antigravity Tools 无密导入、Mac 损坏修复与 403/0 额度排错实录](https://juejin.cn/post/7711952106991386633) | `1//` RT 免密导入、`xattr` 损坏修复、OAuth 回调与 403/0 额度自救 |
| **热点实测** | [这波 Google 真的太大方了！Antigravity Pro 直接放开 Carbon，用完内置浏览器我彻底真香](https://juejin.cn/post/7711322267037122587) | Pro 解锁 Carbon 模型 + 内置浏览器真实开发体感实测 |
| **账单复盘** | [从 Cursor 切到 Codex / Claude Code 两周：真实开销、额度坑与省 80% 账单的配置实录](https://juejin.cn/post/7711322267036499995) | Cursor 切终端 Agent 两周真实开销、额度计算避坑实录 |
| **首页推荐** | [Codex CLI 上手避坑实录：Windows/Mac 配置、`config.toml` 模板与 6 个高频报错排查](https://juejin.cn/post/7711199035106213938) | 终端代理脚本、安全沙箱模板、6 大高频报错一键对照 |

---

### 🧰 免费工具 & 开箱即用配置模板

* 🔐 **[在线离线 2FA / TOTP 验证码生成器（免登录 · 纯前端本地计算）](https://young777.duckdns.org/?tab=help)**
  输入 2FA 密钥即可实时生成 6 位动态验证码，全部 SHA-1 / HMAC-SHA1 计算均在浏览器本地完成，密钥绝不上传服务器。
* 📖 **[AI 编程与海外账号排错指南（15 篇图文实测教程）](https://young777.duckdns.org/?tab=help)**
  覆盖 **Google 登录二维码/人机验证与报错全表**、**Antigravity Tools `1//` RT 无密导入与 Mac 损坏修复**、ChatGPT 付款未获批准 / 降智三步自查、Codex 额度重置与无痛切号、Google 家庭组地区不一致修复等高频问题。

<details>
<summary><b>⚡ 点此展开：Codex CLI 常用 <code>~/.codex/config.toml</code> 与终端代理速查模板</b></summary>

#### 1. 官方订阅安全起手模板 (`~/.codex/config.toml`)
```toml
# 修改文件或执行命令前先确认，防止误改生产代码
approval_policy = "on-request"

# 沙箱限制在当前工作目录内读写
sandbox_mode = "workspace-write"
```

#### 2. 轻量任务切换国产兼容模型（节省高阶额度）
```toml
model = "deepseek-chat"
model_provider = "deepseek"

[model_providers.deepseek]
name = "DeepSeek"
base_url = "https://api.deepseek.com/v1"
env_key = "DEEPSEEK_API_KEY"
```

#### 3. 终端临时代理脚本（把 `7897` 换成你自己的本地端口）
```powershell
# Windows PowerShell
$env:HTTP_PROXY="http://127.0.0.1:7897"
$env:HTTPS_PROXY="http://127.0.0.1:7897"
```
```bash
# macOS / Linux (zsh / bash)
export http_proxy="http://127.0.0.1:7897"
export https_proxy="http://127.0.0.1:7897"
```

</details>

<details>
<summary><b>🛡️ 点此展开：<code>AGENTS.md</code> 自动 Code Review 基准红线 + <code>package.json</code> 快捷命令</b></summary>

#### `AGENTS.md`（放到仓库根目录，Codex CLI 自动加载）
```markdown
# Code Review 团队基准规范

## 必须标为 [P0] 阻断的红线
1. SQL 拼接未参数化、文件路径拼接未做目录穿越校验（path.resolve 前缀检查）。
2. 涉及订单状态流转、库存扣减或回调接口缺少原子条件更新 / 幂等校验。
3. 敏感凭证（Token、密钥、用户隐私字段）被打印到日志或泄露到前台响应体。

## 明确忽略的噪音项（禁止刷屏）
- 单双引号、分号、尾随逗号等纯代码风格问题（交由 Prettier / ESLint 处理）。
- 不影响正确性的主观命名偏好。
```

#### `package.json` 快捷命令（配合掘金 80 行源码 `scripts/codex-review.mjs`）
```json
{
  "scripts": {
    "review": "node scripts/codex-review.mjs",
    "review:test": "node scripts/codex-review.mjs --test",
    "review:dry": "node scripts/codex-review.mjs --dry-run"
  }
}
```

</details>

---

### 🚀 自建自助站与技术协助（星途数字商店）

如果你折腾环境、海外卡风控、接码验证实在耗时间，也可以直接用我自建的自助工具与服务站（**现货支持自助下单，热门缺货款现已开放「可预订排单」，补货按单优先发出**）：

👉 **直达入口：[星途数字商店（young777.duckdns.org）](https://young777.duckdns.org/)** ｜ **[免费帮助中心 & 2FA 工具](https://young777.duckdns.org/?tab=help)**

| 分类 | 包含内容 | 特点说明 |
| :--- | :--- | :--- |
| **🎓 新手避坑与远程协助（¥9.9 起）** | Codex 远程代安装 / 海外账号协助接码 / 接入国产大模型省钱教程 / AI 编程工具包 | 适合新手快速跑通环境，少折腾一整晚 |
| **⚡ 主流 AI 订阅与独立成品号** | ChatGPT Plus & Pro（Session 免密代充 / 成品号）、Claude Pro、Antigravity Pro / Gemini Pro & Ultra、Cursor / Grok 等 | 无需提供账号密码，一单一核，支持热门缺货预订排单，配套 15 篇防封防降智教程与人工售后兜底 |

---

<a id="contact"></a>
### 💬 技术交流与联系方式

遇到配置报错、额度排查、账号风控或需要远程协助，欢迎直接联系（备注 **GitHub / 掘金** 通过更快）：

| 渠道 | 账号 / 链接 | 说明 |
| :--- | :--- | :--- |
| **微信（主力）** | `YyFBI007` | 回复最快，售后与技术交流首选 |
| **QQ** | `2748178842` | 远程协助 / 传文件方便 |
| **Telegram** | [@younage](https://t.me/younage) | 国际直连 |
| **X (Twitter)** | [@PPrisses69263](https://x.com/PPrisses69263) | AI 工具动态同步 |

---

<div align="center">
<sub>🛠️ 下面是我平时维护的一些开源小项目，觉得有帮助欢迎点个 ⭐ Star！</sub>
</div>
