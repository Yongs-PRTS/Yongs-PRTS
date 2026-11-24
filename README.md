<div align="center">

# Hi, I'm Yongs-PRTS 👋

**AI Coding 工作流实战 · 独立开发降本折腾 · 开源效率工具与排错笔记**

[![Offline 2FA & Guides](https://img.shields.io/badge/Free_Tools-Offline_2FA_%26_Docs-0969DA?style=flat-square&logo=gitbook&logoColor=white)](https://young777.duckdns.org/?tab=help)
[![Self-Service Portal](https://img.shields.io/badge/StarWay-Self--Service_Portal-10B981?style=flat-square&logo=lightning&logoColor=white)](https://young777.duckdns.org/)
[![WeChat](https://img.shields.io/badge/WeChat-YyFBI007-07C160?style=flat-square&logo=wechat&logoColor=white)](#contact)
[![QQ](https://img.shields.io/badge/QQ-2748178842-12B7F5?style=flat-square&logo=tencentqq&logoColor=white)](#contact)
[![Telegram](https://img.shields.io/badge/Telegram-@younage-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/younage)
[![X](https://img.shields.io/badge/X-@PPrisses69263-111111?style=flat-square&logo=x&logoColor=white)](https://x.com/PPrisses69263)

</div>

---

### 🧭 我在折腾什么

平时主要深耕 **AI Coding 终端与 IDE 工作流**（`Codex CLI` / `Claude Code` / `Antigravity` / `Gemini` / `Cursor`），以及 Python / JavaScript 效率脚本开发。

这个主页用来沉淀我在稀土掘金持续更新的**一手实测文章、开箱即用配置模板、免费排错工具**，帮你少踩环境配置、网络风控与订阅账单的坑。

---

### 🔥 精选实战笔记（掘金持续更新）

| 方向 | 文章标题 | 核心看点 |
| :--- | :--- | :--- |
| **热点实测** | [这波 Google 真的太大方了！Antigravity Pro 直接放开 Carbon，用完内置浏览器我彻底真香](https://juejin.cn/post/7711322267037122587) | 额度重置 + Pro 解锁 Carbon + 内置浏览器实测体感 |
| **降本方案** | [从 Cursor 切到 Codex / Claude Code 两周：真实开销、额度坑与省 80% 账单的配置实录](https://juejin.cn/post/7711322267036499995) | 高低配模型分流策略、额度计算避坑、月省 80% 实录 |
| **排错手册** | [Codex CLI 上手避坑实录：Windows/Mac 配置、`config.toml` 模板与 6 个高频报错排查](https://juejin.cn/post/7711199035106213938) | 终端代理脚本、安全沙箱模板、6 大报错一键对照 |

---

### 🧰 免费工具 & 开箱即用配置模板

* 🔐 **[在线离线 2FA / TOTP 验证码生成器（免登录 · 纯前端本地计算）](https://young777.duckdns.org/?tab=help)**
  输入 2FA 密钥即可实时生成 6 位动态验证码，全部 SHA-1 / HMAC-SHA1 计算均在浏览器本地完成，密钥绝不上传服务器。
* 📖 **[AI 编程与海外账号排错指南（13 篇实测教程）](https://young777.duckdns.org/?tab=help)**
  涵盖 ChatGPT 付款未获批准 / 降智三步自查、Codex 额度重置与无痛切号、Google 家庭组地区不一致修复、Antigravity 登录排查等高频问题。

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

---

### 🚀 自建自助站与技术协助（星途数字商店）

如果你折腾环境、接码验证、海外卡风控实在耗时间，也可以直接用我自建的自助工具与服务站：

👉 **直达入口：[星途数字商店（young777.duckdns.org）](https://young777.duckdns.org/)** ｜ **[免费帮助中心 & 2FA 工具](https://young777.duckdns.org/?tab=help)**

| 分类 | 包含内容 | 特点说明 |
| :--- | :--- | :--- |
| **🎓 实用工具与教学（¥9.9 起）** | Codex 远程代安装 / 海外账号协助接码 / 接入国产大模型教程 / AI 编程工具包 | 适合新手快速跑通环境，少折腾一整晚 |
| **⚡ 主流 AI 订阅与独立账号** | ChatGPT Plus & Pro（Session 免密代充 / 成品号）、Claude Pro、Gemini Pro / Antigravity 等 | 无需提供账号密码，一单一核，配套完整防降智与 2FA 教程 |

---

<a id="contact"></a>
### 💬 技术交流与联系方式

遇到配置报错、额度排查或需要协助，欢迎直接联系（备注 **GitHub / 掘金** 通过更快）：

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
