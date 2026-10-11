# 洗稿 · note-rewrite

保留文章核心表达和关键锚点，重新组织标题、正文、例子、图内文案和视觉形式。支持纯文字改写与同主题多篇图文制作。

例如原文的核心是“搭子根据天气教你穿搭”，新稿可以更换衣物组合、重写建议、修改排版配色，核心仍是“搭子根据天气教你穿搭”。人物、地点和作息不要求每篇重设。

## 在 Codex 中安装

可以直接告诉 Codex：

> 安装这个 skill：https://github.com/chasssswen/note-rewrite/tree/main/skills/note-rewrite

或使用本机已安装的 skill-installer：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo chasssswen/note-rewrite --path skills/note-rewrite --method git
```

私有仓库需要使用有访问权限的 GitHub 账号和已有 Git 凭据。安装目标已有同名 skill 时，安装器会停止，先处理旧目录。安装后在下一轮对话调用 `$note-rewrite`，例如：

> 用洗稿 skill，参考这篇笔记做两个新版本，保留核心表达和关键锚点，重写文案与图文呈现形式。

## 工作流程

1. 读完整原文及全部配图，提炼核心表达和关键锚点。
2. 列清保留内容、替换内容和用户指定不动的部分。
3. 为每篇设计新的表达方案，不强制换主题或场景。
4. 同步重写文案、指令和对应成果。
5. 图文任务用 AI 改造视觉，保证品牌、文字和数据准确。
6. 检查核心完整、替换范围、前后一致性及篇间差异。
7. 按范围交付文字或图片、文案、预览和 ZIP。

完整规则见 [SKILL.md](skills/note-rewrite/SKILL.md)。

## 依赖与交付

纯文字改写没有额外脚本依赖。图文制作需要所在环境提供图像生成/编辑能力；精确贴图和排字遵循当前工具规则及有效授权。

本 skill 可独立运行。百度搭子内容可结合当前环境已安装的 `$dazi-note-studio` 和现有品牌/UI 素材，也可使用用户提供的准确资料；仓库不包含私有素材库，不依赖仓库外的相对链接。

不固定文章字数、图片页数或人物场景；用户具体要求优先。真实数据和实测结果保持准确，改写后仍需保留原文关键功能、条件和结论。

仓库包含 `skills/note-rewrite/SKILL.md` 和界面元数据 `agents/openai.yaml`，不包含参考原稿、生成图片或客户素材。
