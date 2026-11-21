# Ollama Modelfile 教程

Modelfile 可为本地模型定义基础模型、系统提示词和运行参数。**它不修改模型权重，也不是训练或微调。**

## 准备

安装 Ollama，确认本地已有一个可运行的基础模型。下例用 `qwen3:8b` 作为示意，实际应使用你已经安装且存在的模型名称。

## 创建测试配置

在新目录创建文件 `Modelfile`：

```dockerfile
FROM qwen3:8b
SYSTEM """你是一名中文编程导师，解释清晰，给出可运行的小示例。"""
PARAMETER temperature 0.4
```

执行：

```bash
ollama create linssen-demo -f Modelfile
ollama run linssen-demo
```

如果本地没有基础模型，先根据官方说明拉取或替换 `FROM` 中的名称。

## 使用仓库历史文件

部分历史 `.md` 文件本身采用 Modelfile 语法，**不能只根据扩展名判断**。先检查是否存在有效的 `FROM`、`SYSTEM` 等指令，再按 Ollama 文档确认兼容性。

## 回滚

```bash
ollama rm linssen-demo
```

此操作仅删除示例创建的模型条目；请勿删除自己的基础模型。

官方参考：https://docs.ollama.com/modelfile
