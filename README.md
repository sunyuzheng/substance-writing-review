# Substance Writing

A Codex skill for substance-first Chinese drafting, rewriting, and deep editing.

这个 skill 用来起草、重写或深度精修中文文章、脚本、口播稿、长文和帖子。它先判断当前稿件想成为什么，再选择与材料、读者和 surface 相称的组织方式，同时保留作者自己的声音。

## What It Helps With

- 找到当前稿件最值得保留的判断、张力、场景或声音
- 为论证、叙事、探索、参考或声音驱动的稿件选择合适的组织力量
- 删除重复、绕弯、空泛铺垫和没有信息量的段落
- 识别“罗列代替洞见”“免责声明稀释定义”“标题锋利但正文很水”等情境性失真
- 保留作者本人的语气、节奏和表达习惯
- 判断用户反馈是局部选择还是全稿模式，并把它用在正确范围

## Install

Clone this repository into your Codex skills directory:

```sh
git clone https://github.com/sunyuzheng/substance-writing-review.git ~/.codex/skills/substance-writing-review
```

Restart Codex after installing so the skill can be discovered.

If you keep skills somewhere else, copy or clone the repository into that skill directory instead. The folder name should stay `substance-writing-review`.

## Usage

It can be invoked automatically for matching tasks or explicitly:

```text
Use $substance-writing-review to review this draft:

...
```

For rewriting:

```text
Use $substance-writing-review to rewrite this article. Keep my voice, clarify the organizing logic appropriate to this piece, and explain any major cuts.
```

For a first draft:

```text
Use $substance-writing-review to draft this Chinese article. Decide what kind of piece the material wants to become, choose an appropriate organizing logic, and preserve my voice.
```

For review only:

```text
Use $substance-writing-review to review this script. Tell me what gives it force, where it loses that force, and which changes would help without flattening its voice.
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

This skill uses result determinacy at the level the current task allows. It gives the agent room to choose while preserving the purpose and conditions behind its guidance:

- context before template
- substance before ornamental polish
- source fidelity before fluent invention
- author voice before generic smoothness
- explained defaults before universal rules
- reader respect before cleverness

## License

MIT.
