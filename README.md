# Qiaomu Highlight to Social Content

把 Qiaomu Clipper 中真实发生的 YouTube 高亮与批注，继续变成字幕金句图和有故事背景的社交平台文案。

## 为什么做这个 Skill

[Qiaomu Clipper](https://github.com/joeseesun/qiaomu-clipper) 已经打通了非常关键的前半程：

`YouTube 字幕阅读 → 翻译 → 高亮/批注 → 保存到 Obsidian`

这个 Skill 在此基础上补齐内容生产的后半程：

`读取高亮 → 推荐候选句 → 用户确认 → 回到原视频取帧 → 制作字幕图 → 核实人物故事 → 生成小红书/微博等文案`

核心原则是：**不让 Agent 脱离你的真实阅读行为，重新猜哪句话最重要。**

## 适合怎样使用

你可以对 Codex 或兼容 Skill 的 Agent 说：

- “把这个视频里我高亮的内容整理出来。”
- “就用这几句话制作字幕图。”
- “把刚才批注的内容做成一篇小红书。”

Skill 会区分作者原文、翻译、用户高亮、用户批注与 AI 提炼，并在制图前等待你确认选句。

## 安装

将仓库中的 `SKILL.md` 和 `agents/` 放入你的 Skill 目录，例如：

```text
~/.codex/skills/qiaomu-highlight-to-social-content/
```

重新启动或刷新 Agent 后即可被自动发现。

## 推荐搭配

- [Qiaomu Clipper](https://github.com/joeseesun/qiaomu-clipper)：负责 YouTube 字幕阅读、高亮、批注与 Obsidian 保存。
- 一个能够按时间点提取真实视频帧并绘制字幕的 Skill；本项目最初配合 `native-subtitle-quote-image` 使用。

## 致谢与关系说明

本项目的工作流基于向阳乔木开源的 Qiaomu Clipper 所提供的阅读、高亮、批注与 Obsidian 沉淀能力继续扩展。

本仓库是独立的上层 Agent Skill，不是 Qiaomu Clipper 的官方组件，也没有修改或重新分发 Qiaomu Clipper 的源码。感谢向阳乔木把关键的阅读入口开源出来。

## 隐私与版权

- 默认只读取用户明确指定的 Obsidian Vault 和相关笔记。
- 不保存或输出浏览器凭据、Cookies 和私人目录结构。
- 只有用户有权处理来源视频时才进行下载、取帧和再创作。
- 默认只生成本地素材，不自动发布到任何平台。

## License

MIT
