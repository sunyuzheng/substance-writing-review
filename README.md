# Substance Writing Review

A Codex skill for substance-first Chinese writing review and revision.

这个 skill 用来检查、改写或精修中文文章、脚本、口播稿、长文和帖子。它的核心不是把文字变得更像 AI、更新潮或更工整，而是找出源材料里真正有力量的判断、经历、细节和作者声音，并把它们放大。

## What It Helps With

- 找到文章最该被读者记住的核心判断
- 删除重复、绕弯、空泛铺垫和没有信息量的段落
- 让推理链更清楚，让判断后面有来路
- 保留作者本人的语气、节奏和表达习惯
- 检查中文 AI 味、翻译腔、空泛词和过度包装
- 给出高信号 review，或直接重写成更清楚的版本

## Install

Clone this repository into your Codex skills directory:

```sh
git clone https://github.com/sunyuzheng/substance-writing-review.git ~/.codex/skills/substance-writing-review
```

Restart Codex after installing so the skill can be discovered.

If you keep skills somewhere else, copy or clone the repository into that skill directory instead. The folder name should stay `substance-writing-review`.

## Usage

Invoke it explicitly:

```text
Use $substance-writing-review to review this draft:

...
```

For rewriting:

```text
Use $substance-writing-review to rewrite this article. Keep my voice, but make the main judgment clearer and cut anything that does not move the piece forward.
```

For review only:

```text
Use $substance-writing-review to review this script. Tell me what is strongest, what should be cut, and where the reasoning does not yet stand.
```

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── sources.md
```

`SKILL.md` is the main skill definition. `agents/openai.yaml` provides optional UI metadata. `references/sources.md` records the public influences behind the skill.

## Design Principles

This skill is written around result determinacy rather than a brittle editing checklist. It tells the agent what a good edit must preserve and improve:

- substance before polish
- judgment before phrasing
- proof before rhetoric
- author voice before generic smoothness
- reader respect before cleverness

## License

MIT.
