# SCI Submission Agent

一个面向 Codex 的可复用 skill，把 SCI 投稿从选刊、投稿前准备、在线投稿、初审和同行评审，整理到编辑决定、返修和重投。它会生成计划、材料清单、Cover Letter、状态询问邮件和逐条审稿回复框架。

## 使用

把整个目录复制到 Codex 的技能目录：

```text
%CODEX_HOME%\skills\sci-submission-agent
```

然后在对话中调用：

```text
Use $sci-submission-agent to prepare a submission checklist for my manuscript.
```

也可以直接给出中文请求，例如：

```text
请用 $sci-submission-agent 根据这篇论文和目标期刊，生成投稿前清单和 Cover Letter 草稿。
```

先提供题目、摘要、文章类型、目标期刊、当前阶段和期刊来信。信息不完整时，agent 会列出待补充字段，不会替用户猜测研究结果、指标或声明。

## 内容结构

- `SKILL.md`：路由、工作边界和输出规则。
- `references/workflow.md`：从 Day 1 到返修的阶段流程、材料矩阵、状态说明和时间线使用方法。
- `references/templates.md`：信息采集表、期刊比较表、Cover Letter、状态询问、审稿回复和投稿前核对表。
- `agents/openai.yaml`：Codex UI 中显示的名称、描述和默认提示。

## 资料范围

流程根据用户提供的中文图片整理。图片中的 Day 数、审稿周期、接受率、指标和格式示例属于经验参考；期刊官网的最新 Guide for Authors、投稿系统和编辑部通知优先。仓库不包含原始图片，也不要求把个人稿件、作者联系方式或未公开数据上传到 GitHub。

## 边界

这个 agent 用于规划、核查和草拟文本。它不会编造数据、引用、伦理审批、审稿人联系方式或期刊指标，也不会在用户明确确认前代表用户提交稿件、发送外部邮件或接受收费/版权选项。

## 许可证

MIT，见 [LICENSE](LICENSE)。
