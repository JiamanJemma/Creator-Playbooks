<div align="center">
  <h1>🤖 Creator Playbooks</h1>
  <p><b>不写一行代码，用纯 Markdown 规则将你的 AI 私人助理改造成「全自动自媒体分发引擎」。</b></p>
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-purple.svg)](https://opensource.org/licenses/MIT)
  [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
</div>

---

## 💡 这是什么？

这是一个基于 **"Prompt as Code（提示词即代码）"** 理念构建的开源知识库。
很多创作者在多平台分发时，面临排版错乱、复制粘贴麻烦、标签格式不同、发布时间踩雷等问题。本项目提供了一整套经过**真实流量数据验证**的 Markdown 格式约束文件。

只要把这些 `.md` 文件喂给你的 Cursor、Gemini 等系统，你的 AI 就会像拥有肌肉记忆一样，每次完美吐出**严丝合缝对齐各大平台网页表单**的无脑复制版文案。

## 🎯 核心黑科技

- **[防御性分发映射]**：强制 AI 摒弃废话标题（如 `**标题**`），直接将抖音/TikTok/视频号等“单框平台”连成完美长段落，小红书则自动限制 20 字符。
- **[算法防内卷机制]**：自动配置 48 小时冷却池时间表。比如 TikTok 自动错开国内抖音时间，定锚次日早晨北美晚高峰出海。
- **[UI 防呆克隆]**：B站输出区块严格按照 `【标题】➡️【标签】➡️【视频简介】➡️【发布时间】➡️【动态】` 的顺序，完美映射网页版的填写下拉框，从上到下无脑 CV（复制粘贴）。

## 🚀 目录结构

```text
📦 creator-playbooks
 ┣ 📂 playbooks
 ┃ ┣ 📜 publish.md         # 全局发布总控台（指令底层）
 ┃ ┣ 📜 video.md           # 视频后期管线（剪辑/字幕）
 ┃ ┗ 📜 aigc.md            # AIGC 视觉资产（封面/配图生成）
 ┣ 📂 config
 ┃ ┗ 📜 platform-rules.md  # 👑 核心：各平台流量峰值与排版映射表
 ┗ 📜 README.md
```

## 🛠 如何使用 (How to Use)

1. **Fork 本仓库**：克隆或下载到你的本地电脑。
2. **脱敏与替换变量**：
   - 全局搜索 `<YOUR_IP_NAME>`（例如：佳蔓Jemma），替换成你的超级个体品牌名。
   - 打开 `config/platform-rules.md`，根据你的后台粉丝活跃数据，微调各个平台的黄金发布时间（详见文档注释）。
3. **注入灵魂**：将整个文件夹作为你的 AI IDE（如 Cursor）的 Workspace 引入，或在配置 Rules 时关联这些文件。
4. **一键开工**：对 AI 说：“我已经剪好了视频，给我一套全平台文案。” 然后你就看着它开始表演吧。

## 🤝 贡献指南 (Contributing)

发现某个平台的表单结构又改版了？欢迎提交 Pull Request 更新排版映射规则！
无论是 YouTube 的算法变化，还是小红书的 字符限制升级，我们共同维护这份**“抗击平台熵增”**的武器库。

## 📜 许可证 (License)

本项目采用 [MIT License](LICENSE) 开源。分享本身，就是在构建我们的护城河。

---
> *"一秒钟就能复刻的时代，真正的护城河不在代码里，在你占据的用户心智里。" —— 5% 的行动者*
