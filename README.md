# Own Your View

Examine an idea that resonates with you before you adopt it or act on it.

[中文说明](README.zh-CN.md) · Created by [NickQin001](https://github.com/NickQin001) · [MIT](LICENSE)

Early feedback version **v0.1.1** · 2026-10-14.

## Why try it?

A quote, book, or interview can feel convincing before its assumptions are clear. Own Your View helps you inspect your reasons, consider counterexamples, and decide what to keep, change, or leave open.

The AI can give a counterexample right away. It usually waits for your response before suggesting a rewritten view. You can challenge its reasoning, ask for a direct answer, keep your original view, or stop.

This project is looking for people with the same use case and for suggestions grounded in actual experience.

## Try it

The single runtime entry is [skills/own-your-view/SKILL.md](skills/own-your-view/SKILL.md). In an AI environment that can read local files, use:

```text
Read and use skills/own-your-view/SKILL.md.

I read that having more productivity tools always makes you more efficient.
This resonates with me because tools reduce repetitive work.
Help me examine this idea before suggesting a rewritten view.
```

Paths are relative to this repository folder. If your AI cannot read local files, provide the skill's contents together with your request. Native skill installation depends on your tool; an installation command and cross-platform compatibility have not been validated for this release.

Instructions are maintained in Chinese in one core file. A model that can understand them should follow the language of your request, or another language you explicitly choose. Four language scenarios have been simulated; this is not a guarantee for every language or model.

You can start with your own paraphrase. A relevant source passage is only needed when the interpretation or a key fact depends on it.

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

Eight initial model-simulation cases and four later language cases have been reviewed. They came from one reviewing thread in batches, not from independent human participants. Structural and local-file checks passed.

Real-user outcomes, full regression coverage, third-party skill comparisons, and cross-model/install compatibility are still untested. Satisfaction or agreement with AI does not establish improved reasoning.

[Validation record](tests/检查记录.md) · [Test plan](tests/测试方案.md) · [Source acknowledgements](SOURCES.md)

## Authorship and license

Created by NickQin001 with AI assistance in drafting and review. Inspired by mechanisms in existing Socratic-dialogue and argument-review skills, acknowledged in SOURCES.md; this project does not claim those general ideas as its invention.

MIT permits use, modification, redistribution, and commercial use, with the copyright and license notices retained in copies or substantial portions. It does not require prominent advertising of the original author or that all changes be contributed back.

[Release notes](RELEASE_NOTES.md) · [中文发布与隐私说明](PUBLISHING.zh-CN.md)
