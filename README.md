<div align="center">

# Linssen AI Prompt Collection

**模型提示词合集 · 直接复制使用 · 中文配置教程**

Maintained by **Linssen Studio**

[快速开始](#快速开始) · [提示词目录](#提示词目录) · [使用教程](#使用教程) · [来源与署名](CREDITS.md)

</div>

---

## 项目介绍

这里集中保存不同大模型、编程 Agent 和本地模型的提示词样本。**原始提示词文件保持不变**，直接进入对应文件页面复制全文即可。

本仓库基于 [togg53192-cmd/jailbreaks](https://github.com/togg53192-cmd/jailbreaks) 派生。Linssen Studio 编写中文导航和操作教程；原始提示词及历史贡献仍归相应作者。参见 [来源说明](CREDITS.md)。

## 快速开始

1. 在下方**提示词目录**选择你使用的模型。
2. 点击对应文件，打开 GitHub 文件页面，使用右上角 **Raw** 或复制按钮获取原文。
3. 根据文件类型选择使用入口：**聊天窗口 / AGENTS.md / API system 配置 / Ollama Modelfile**。
4. 按下方教程操作即可。**无需安装整个仓库，也无需先做评测。**

> 文件名中的模型版本和“系统级”描述不等于官方兼容性或实际权限。复制到普通聊天窗口的内容仍是用户消息，能否生效取决于模型与客户端。

## 提示词目录

| 模型 / 厂商 | 打开原始文件目录 |
|---|---|
| DeepSeek | [DeepSeek](DeepSeek/) |
| Qwen / Alibaba | [Alibaba](Alibaba/) |
| Kimi / Moonshot | [Moonshot AI](Moonshot%20AI/) |
| MiMo / Xiaomi | [Xiaomi](Xiaomi/) |
| Claude / Anthropic | [Anthropic](Anthropic/) |
| GLM / Zhipu | [Zhipu AI](Zhipu%20AI/) |
| Gemini / Gemma / Google | [Google](Google/) |
| GPT-OSS / OpenAI | [OpenAI](OpenAI/) |
| Grok / xAI | [xAI](xAI/) |
| Mistral | [Mistral](Mistral/) |
| Meta | [Meta](Meta/) |
| StepFun | [StepFun](StepFun/) |
| Meituan | [Meituan](Meituan/) |
| Stealth Models | [Stealth Models](Stealth%20Models/) |
| 其他样本 | [0x8D jailbreaks](0x8D%20jailbreaks/) |

### 常用文件直达

| 文件 | 入口类型 |
|---|---|
| [MiMo V2.6](Xiaomi/mimo-2.6-agents.md) | Agent 工作规范样本 |
| [Kimi K3](Moonshot%20AI/kimi-k3-agents.md) | Workspace 指令样本 |
| [GLM ZCode 5.3 AGENTS.md](Zhipu%20AI/glm-zcode-5.3-AGENTS.md) | AGENTS.md 样本 |
| [DeepSeek V3](DeepSeek/deepseek%20v3.md) | System Prompt 样本 |
| [Gemma 4](Google/gemma4.md) | Ollama Modelfile |
| [GPT-OSS 20B](OpenAI/gpt-oss-20b.md) | Ollama Modelfile |

## 使用教程

| 使用环境 | 操作说明 |
|---|---|
| 网页聊天：DeepSeek、Qwen 等 | [复制到聊天窗口](docs/chat-prompt-guide.md) |
| Codex 等支持 AGENTS.md 的编程 Agent | [AGENTS.md 放置教程](docs/agents-md-guide.md) |
| Codex + MiMo | [配置说明](docs/codex-mimo-guide.md) |
| 自己开发的 API 应用 | [System Prompt 配置](docs/api-guide.md) |
| 本地 Ollama | [Modelfile 使用教程](docs/ollama-guide.md) |
| 第一次使用 | [新手入门](docs/getting-started.md) |

### 对话窗口

打开文件 → 复制全文 → 粘贴到新对话中。该内容按**用户消息**处理，不会自动变成 system 消息。

### AGENTS.md

对于支持此文件的编程 Agent，在目标项目根目录创建 `AGENTS.md`，将选定内容保存进去，再从项目中启动 Agent。不同工具的加载规则不同，具体见 [教程](docs/agents-md-guide.md)。

### API

在自己控制的 API 应用中，把适用的提示词放入服务商支持的系统指令字段。不要把网页聊天框误认为系统配置入口。

### Ollama

只有符合 Ollama Modelfile 语法的文件才能直接用于 `ollama create`。例如：

```bash
ollama create linssen-local -f Modelfile
ollama run linssen-local
```

其中 `Modelfile` 是你准备好的有效配置文件路径；必须确认其中的基础模型已存在。参见 [完整教程](docs/ollama-guide.md)。

## 使用说明

本项目是资料集合，并非一键破解工具。原始样本中的权限声明只是文本，不会改变真实授权或平台规则。请勿在提示词中加入 API 密钥或个人敏感信息；遵守适用法律、模型平台条款及授权范围。

## Credits

**Linssen Studio** — 中文首页、导航及教程维护。  
**Original collection** — [togg53192-cmd/jailbreaks](https://github.com/togg53192-cmd/jailbreaks)。

保留原始文件、历史提交与来源记录，不将第三方作品冒称为 Linssen 原创。
