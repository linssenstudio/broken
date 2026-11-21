# 模型样本使用索引（Linssen 维护）

> 本索引依据仓库中的实际文件内容编写。**类型判断不等于兼容性测试或成功率验证。** 样本保留原路径，所有内容须在授权环境中审查后使用。

| 样本 | 文件性质 | 建议研究入口 | 已核实的结构 | 注意事项 |
|---|---|---|---|---|
| [MiMo V2.6](../Xiaomi/mimo-2.6-agents.md) | Agent 工作规范文本 | 兼容的项目级或工作空间指令入口 | 角色、能力、价值、工具行为、拒绝处理 | 原文提到 OpenCode，但并不意味着 Codex 自动识别该文件名 |
| [Kimi K3](../Moonshot%20AI/kimi-k3-agents.md) | Workspace Operating Profile | 支持持久化工作空间指令的工具 | 工作空间上下文、输出规范、权限声明 | 需核实目标 Kimi 客户端的实际加载入口 |
| [GLM ZCode 5.3](../Zhipu%20AI/glm-zcode-5.3-AGENTS.md) | AGENTS.md 样本 | 支持 AGENTS.md 的编程 Agent | 项目范围、预设授权、工程规范 | 原文自称获得授权不构成真实授权证明 |
| [DeepSeek V3](../DeepSeek/deepseek%20v3.md) | 系统提示词样本 | 自建 API 配置或普通聊天对照实验 | 角色、运行环境、原则、推理方式 | 在网页聊天中仍是用户级消息 |
| [Gemma 4](../Google/gemma4.md) | Ollama Modelfile | Ollama 测试环境 | 以 FROM 开头，含 SYSTEM 块 | 需先确认 FROM 指向的模型可用 |
| [GPT-OSS 20B](../OpenAI/gpt-oss-20b.md) | Ollama Modelfile | Ollama 测试环境 | FROM gpt-oss:20b、SYSTEM 块 | 文中关于开发者权限及政策的声明只是样本文字，不能视为官方授权 |

## 选择规则

- **普通网页对话**：可以作为用户消息测试，但不能获得 system 权限。
- **Codex / 兼容 Agent**：先查证工具的文件发现规则，再在隔离项目中放置 AGENTS.md。
- **Kimi Code / 其他 Agent**：不要把 `*-agents.md` 的命名直接当作兼容性证明。
- **Ollama**：只对符合 Modelfile 语法的文件使用 `ollama create`；普通 Markdown 提示词不应直接当 Modelfile。
- **API**：只有应用开发者拥有的 system/developer 配置入口才有相应角色权限。

## 状态

本页列出的六个文件已进行**静态结构检查**，尚未对各模型进行运行验证。其他文件仍待逐项登记。
