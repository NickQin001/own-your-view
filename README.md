# Own Your View

Examine an idea that resonates with you before you adopt it or act on it.

[中文说明](README.zh-CN.md) · Created by [NickQin001](https://github.com/NickQin001) · [MIT](LICENSE)

Repository: [https://github.com/NickQin001/own-your-view](https://github.com/NickQin001/own-your-view)

Early feedback version **v0.1.2** · 2026-10-17 · [Release and download](https://github.com/NickQin001/own-your-view/releases/tag/v0.1.2).

### What changes in v0.1.2?

Counterexamples must preserve the conditions and goal you actually stated. Failing to carry out your method is an execution warning, not automatically evidence against it. If an objection misses your claim, the AI should withdraw it without declaring your whole claim proven.

For real-world effects, relevant verifiable evidence takes priority; a hypothetical example is labelled and cannot establish how often something happens. With disagreement, specific objections and revised claims receive fresh consideration. Repeated denial alone does not make a supported correction false, and the conversation may end without agreement.

## Why try it?

A quote, book, or interview can feel convincing before its assumptions are clear. Own Your View helps you inspect your reasons, consider counterexamples, and decide what to keep, change, or leave open.

The AI can give a counterexample right away. It usually waits for your response before suggesting a rewritten view. You can challenge its reasoning, ask for a direct answer, keep your original view, or stop.

This project is looking for people with the same use case and for suggestions grounded in actual experience.

## Quick start

### Codex: install once, then invoke by name

First review the [v0.1.2 core instructions](https://github.com/NickQin001/own-your-view/blob/v0.1.2/skills/own-your-view/SKILL.md). In your own Codex chat, paste:

```text
$skill-installer

Install the skill I have selected:
Repository: https://github.com/NickQin001/own-your-view
Skill directory: skills/own-your-view
Revision: v0.1.2

Install only this skill in my personal Codex skills location.
If an installation with the same name already exists, inspect it first;
do not overwrite it without my approval.
Do not modify other skills, global instructions, or unrelated settings.
After installation, verify that its name is own-your-view and explain how to invoke it.
```

This is a prompt for Codex, not a shell command. You initiate installation on your own device and approve any permissions requested by your environment; sharing this link does not install anything automatically. If `$skill-installer` is unavailable, use the no-install option below.

After installation, use the skill on your next turn:

```text
$own-your-view

I read that having more productivity tools always makes you more efficient.
This resonates with me because tools reduce repetitive work.
Help me examine this idea before suggesting a rewritten view.
```

In Codex, type `$` and select `own-your-view`, or look for it in `/skills`. If it does not appear, restart Codex and check again. See [OpenAI's skills documentation](https://learn.chatgpt.com/docs/build-skills) for installation and invocation behavior. Installation and discovery were checked in one Windows Codex setup; compatibility with other environments and automatic selection behavior are not certified.

### Other AI chats: try it without installing

Download and extract `own-your-view-v0.1.2.zip` from the [v0.1.2 release](https://github.com/NickQin001/own-your-view/releases/tag/v0.1.2). The full prompt is [skills/own-your-view/SKILL.md](skills/own-your-view/SKILL.md); README files explain usage, not the runtime rules. Upload that file to a chat that can read text files, or paste its complete contents, then send:

```text
Read the complete SKILL.md I provided and follow its instructions.
If you cannot access the full file, say so before proceeding.

My idea: Having more productivity tools always makes you more efficient.
Why it resonates with me: Tools reduce repetitive work.
What I want to examine: When does this claim fail?

Start with one important question or counterexample.
Do not suggest a rewritten view yet.
```

Replace the idea, reason, and question with your own. This supplies conversation instructions; it does not install a native skill or make `$own-your-view` available in an ordinary chat. In an environment that can read local files, you can instead ask it to read `skills/own-your-view/SKILL.md`, relative to the extracted repository folder.

Instructions are maintained in Chinese in one core file. A model that can understand them should follow the language of your request, or another language you explicitly choose. English installation and usage examples do not imply a separate English rule set. Chinese-only source instructions can be harder for English-only readers to audit; the English summary here is not a full translation. A translated explanation can help you inspect them, but should not silently replace the core. Correct reply language alone does not establish correct reasoning, cultural fit, or equivalent behavior across models. See the [validation record](tests/检查记录.md) for tested behavior and limitations.

You can start with your own paraphrase. A relevant source passage is only needed when the interpretation or a key fact depends on it. Share only the skill file and this repository link with a friend, not your private conversation history.

### Updating an installed copy

The installation prompt pins the runtime to `v0.1.2`. An installed copy does not update when GitHub or local source changes. If you already installed v0.1.1, explicitly ask your installer to update only `own-your-view` to v0.1.2 after reviewing the changes; back up and preserve local edits before approving replacement. The v0.1.1 tag and ZIP remain available as the original snapshot.

## What a conversation can look like

A hypothetical counterexample from a model simulation:

> You add a second task manager, then spend more time copying updates between the two than you save through its automation.

The next question invites your judgment:

> How does that example affect your view—which part would you keep, revise, or remain unsure about?

That challenges “always” while preserving the possible value of reducing repetitive work. The full simulated inputs and outputs are available in [the validation records](tests/模拟记录.md).

## What to expect

- Usually one focused question at a time, with relevant counterexamples and space for your own judgment.
- Key facts checked when the host provides browsing and permission; unknowns stay explicit.
- Suggested rewrites normally offered after you respond, or earlier when you explicitly request one.
- A provisional conclusion that may retain uncertainty and disagreement.
- Where appropriate, one optional, low-cost way to test the idea further. Simple explanation or formatting requests do not receive extra homework.

The skill is intended for everyday ideas and reading reflections. It is not a professional decision tool. The host determines available tools and how chat data is stored; the skill itself adds no telemetry, automatic feedback submission, or personal profile.

## Help improve it

[Feedback prompts in English](FEEDBACK.en.md) · [中文反馈](FEEDBACK.md)

Share feedback through [Issues](https://github.com/NickQin001/own-your-view/issues) using [the bilingual template](.github/ISSUE_TEMPLATE/feedback.md). Suggestions from people who have not tried it are welcome when labelled as such. Pull requests with a small, explained change are also welcome.

We want to know where it helped, made thinking harder, gave an irrelevant objection, rewrote your view too early, or failed to stop. A short anonymized excerpt or a made-up example is enough.

## Current evidence

Historical v0.1.1 checks reviewed eight initial model-simulation cases and four later language cases. For v0.1.2, twelve scripted Chinese/English conversations produced 36 responses in one reviewing thread. This was not isolated, turn-by-turn testing: later inputs were visible. Review found residual targeting issues; a final instruction was tightened but not independently rerun. Real-source retrieval, human outcomes and cross-model equivalence remain untested. See the [inputs](tests/20261017_多轮测试输入.md), [raw responses](tests/20261017_多轮模拟记录.md) and [validation record](tests/检查记录.md). This remains an early feedback release, not a fully validated reasoning tool.

One Windows Codex installation was checked: installation completed, the core file matched v0.1.1, structural validation passed, and the skill appeared in the session's available-skills metadata. The visible IDE picker and automatic selection behavior were not independently tested.

Real-user outcomes, full regression coverage, third-party skill comparisons, and cross-model/cross-platform compatibility are still untested. Satisfaction or agreement with AI does not establish improved reasoning.

[Validation record](tests/检查记录.md) · [Test plan](tests/测试方案.md) · [Source acknowledgements](SOURCES.md)

## Authorship and license

Created by NickQin001 with AI assistance in drafting and review. Inspired by mechanisms in existing Socratic-dialogue and argument-review skills, acknowledged in SOURCES.md; this project does not claim those general ideas as its invention.

MIT permits use, modification, redistribution, and commercial use, with the copyright and license notices retained in copies or substantial portions. It does not require prominent advertising of the original author or that all changes be contributed back.

[Release notes](RELEASE_NOTES.md) · [中文发布与隐私说明](PUBLISHING.zh-CN.md)
