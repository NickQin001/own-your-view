# Own Your View

Examine an idea that resonates with you before you adopt it or act on it.

[中文说明](README.zh-CN.md) · Created by [NickQin001](https://github.com/NickQin001) · [MIT](LICENSE)

Early feedback version **v0.1.5** · 2026-11-17 · [Release and downloads](https://github.com/NickQin001/own-your-view/releases/tag/v0.1.5)

## What changed

- Reflection uses **Current understanding → Key check → One question**, showing a section only when it adds substantive content. In Chinese, the labels are **本轮理解 / 关键检验 / 一个问题**.
- Direct answers, summaries, library listings and save confirmations follow the request instead of repeating a review template. Explicit format requests are respected.
- A personal library is shared across workspaces through a persistent absolute-path configuration. Existing libraries are retained without automatic migration or merging.
- Create the library or write judgments only after explicit confirmation, then read back to verify the result and retained entries.

Evidence checks, counterexamples, alternative explanations and uncertainty remain essential. Agreement with the AI is not proof; the assistant does not decide for you.

## Try it

For a compatible skill host, follow its installation process using [skills/own-your-view](https://github.com/NickQin001/own-your-view/tree/v0.1.5/skills/own-your-view). The release page has a full repository ZIP and a separate SkillHub upload ZIP.

For a file-reading assistant, extract the repository and ask it to read `skills/own-your-view/SKILL.md`, then provide your idea. You can also supply the complete file in a chat. File reading is not proof of native skill registration; a text-only chat may not have persistent file access.

> Please use own-your-view to examine “More tools always make work more efficient.” My reason is that each tool saves a little effort. Focus on the most important issue first.

If your host supports the skill selector, invoke `$own-your-view`. Installed copies do not automatically follow repository updates.

## Conversation and storage

The assistant responds to new information, checks the key issue, and asks one useful question when needed. It can withdraw an invalid counterexample, preserve disagreement or close a round without forcing a conclusion. If you ask it to stop, it stops.

After a normal close, you may explicitly confirm saving a current judgment. On first use, the assistant records an absolute library path in `.own-your-view/config.json` under the actual user home. All workspaces using that home read this file. An explicitly configured library or the current workspace's existing legacy library is reused; otherwise the default is `.own-your-view/consensus.json` under the user home. Initial setup creates only the path configuration. The library is created only after explicit save confirmation.

This is a file convention defined by the skill, not a native host memory feature. It requires access to the same home and library; it does not synchronize devices or scan and merge other workspaces. Invalid or inaccessible configuration is reported rather than falling back to an empty workspace library. See [configuration and templates](templates/README.md).

Entries preserve the claim, scope, key counterexample and response, conditions for reconsideration, date and `updated_at`. They are revisable judgments, not established truths. Only empty and fictional examples are included in [templates](templates/README.md).

A personal host rule requiring six-part reports needs a user-authorized exception to use this presentation. The skill does not override host instructions, modify native global settings or synchronize private libraries on its own. Its path configuration is a separate local file.

## Validation and limits

For v0.1.5, one reviewer thread exercised three isolated profiles and four library-listing requests: first-use configuration, shared reads from another workspace and its subdirectory, and corrupt configuration. The main process separately inspected configuration, missing fallback files and original file hashes. See the [v0.1.5 validation record](tests/20261117_个人共享库验收.md). Given test home directories do not establish automatic host discovery; this was not a cross-model test.

One new reviewer thread produced nine fictional dialogue responses and eight isolated file-operation examples for v0.1.4. Stored responses and file results were reviewed, including missing/corrupt files, no write before confirmation, append with old-entry preservation and first-write readback.

These were batch scenarios with all inputs visible. File actions were orchestrated by case ID. This supports the observed outputs and artifacts, not general intent recognition, automatic skill selection, independent per-case conversations, cross-model equivalence or long-term learning outcomes. See the [validation summary](tests/20261116_呈现与观点库验收.md) and [release notes](RELEASE_NOTES.md).

This is a reflection aid for everyday ideas, not professional advice. Tools and chat retention depend on the host. The skill adds no telemetry or automatic feedback submission; private judgments are not uploaded to this repository.

Specific, de-identified feedback is welcome through [Issues](https://github.com/NickQin001/own-your-view/issues). See [feedback guidance](FEEDBACK.en.md), [sources](SOURCES.md) and [MIT license](LICENSE). Preserve the license and attribution when reusing the work.
