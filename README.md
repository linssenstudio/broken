# Linssen AI Prompt Lab

> 大模型提示词、Agent 指令配置与提示词注入机制研究 | Maintained by **Linssen Studio**

本项目把不同模型的提示词样本整理成**可阅读、可配置、可验证**的研究资料库。你可以学习 `AGENTS.md`、聊天窗口、自定义指令、API system 消息及 Ollama Modelfile 的区别，并使用可重复的测试方法验证实际效果。

**注意：** 本仓库的历史提示词样本源于 [togg53192-cmd/jailbreaks](https://github.com/togg53192-cmd/jailbreaks) 的派生项目。Linssen Studio 负责新增的中文教程、分类说明和研究方法。历史样本不应视为 Linssen 原创，也不代表所有提示词已经验证有效。参见 [CREDITS.md](CREDITS.md)。

## 快速导航

| 想做什么 | 从这里开始 |
|---|---|
| 第一次使用仓库 | [新手入门](docs/getting-started.md) |
| 给 Codex 等编程 Agent 配置项目规范 | [AGENTS.md 教程](docs/agents-md-guide.md) |
| 在 DeepSeek、Qwen 等聊天界面测试 | [聊天提示词教程](docs/chat-prompt-guide.md) |
| 在自建应用中配置 system 消息 | [API 教程](docs/api-guide.md) |
| 在 Ollama 中创建自定义模型 | [Ollama 教程](docs/ollama-guide.md) |
| 判断提示词是否真的有效 | [效果验证方法](research/evaluation.md) |
| 理解所谓“破甲”的原理与边界 | [机制分析](research/mechanisms.md) |
| 查看历史样本的来源与署名 | [来源说明](CREDITS.md) |

## 现有样本索引

以下为仓库原有的模型分类目录，保留原路径，避免破坏已有链接。**文件名称中的模型版本不等于官方兼容性认证。**

| 分类 | 文件夹 |
|---|---|
| DeepSeek | [DeepSeek](DeepSeek/) |
| Qwen / Alibaba | [Alibaba](Alibaba/) |
| Kimi | [Moonshot AI](Moonshot%20AI/) |
| MiMo | [Xiaomi](Xiaomi/) |
| Claude | [Anthropic](Anthropic/) |
| GLM | [Zhipu AI](Zhipu%20AI/) |
| Gemini / Gemma | [Google](Google/) |
| GPT-OSS | [OpenAI](OpenAI/) |
| Grok | [xAI](xAI/) |
| Mistral | [Mistral](Mistral/) |
| 其他模型 | [Stealth Models](Stealth%20Models/) |

## 三分钟上手

1. 先确认你用的是**网页聊天、编程 Agent、API 还是 Ollama**。
2. 在对应目录选择一个样本，先阅读完整内容，不要盲目执行其中的命令或工具调用。
3. 按照上面的教程选择正确的加载入口。
4. 先在测试项目中验证，不要直接覆盖生产项目的指令文件。
5. 用相同的测试问题对比配置前后的行为，记录模型版本、日期和结果。

## 重要概念

- **用户消息 ≠ 系统消息。** 在聊天窗口粘贴一段声称具有系统权限的文字，不会真正提升其权限。
- **AGENTS.md ≠ 通用模型后门。** 只有支持该规范的 Agent 才会按其发现规则加载文件。
- **Modelfile ≠ 微调。** 它配置模型运行方式，不会修改模型权重。
- **提示词有效 ≠ 成功越狱。** 必须排除模型原本就能完成该任务的情况。

## 维护与贡献

欢迎提交清晰标注来源的提示词样本、兼容性报告和教程修正。请提供：目标模型、版本、客户端、配置入口、测试日期、基线与对照结果。不要提交 API 密钥、个人信息或未经授权获取的系统提示词。

## 研究与使用声明

本项目用于提示词工程、Agent 配置与模型安全研究。历史样本可能包含试图覆盖规则或压制拒绝的文本，**不代表这些指令拥有真实权限或被本项目认可**。请在授权环境中测试，不要将其用于未授权访问、侵害他人或违反适用法律及服务条款的行为。

---

**Linssen Studio · Documentation & Research**  
Original collection attribution: [togg53192-cmd/jailbreaks](https://github.com/togg53192-cmd/jailbreaks)
