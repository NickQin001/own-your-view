# Release notes

## v0.1.3 — Consensus views MVP (2026-11-06)

Optional, document-first consensus library. Counterexample, fact-checking, and disagreement rules from v0.1.2 are unchanged. No new runtime dependency, telemetry, or automatic outbound action. An installed v0.1.2 copy does not upgrade by itself; review the skill and create your own `views/consensus.json` before using the library.

### Added

- **Opt-in write.** After a normal close, the skill asks whether to save this round’s current judgment. “Write it,” “确认入库,” or an equivalent yes is enough. No card or form is required. Nothing is written without that confirmation. If you end the conversation, exit rules still stop immediately; the skill does not keep asking in order to save an entry.
- **Two logical roles.** A write role and a decision-review role. By default the current assistant does both. An optional mapping of who does which is visible, opt-in, and explained. The public skill uses those generic role names only.
- **Entry fields.** Claim, scope, key counterexample and response, overturn conditions, and date, plus `updated_at` (ISO 8601, refreshed on append and revision). Optional: source, status, and a stable id. The wording is “共识观点 / 现行判断,” not a settled truth.
- **When to read.** Only when the topic is related. If relevance is unclear, one short question. A prior consensus is advice for you to review, not a decision made for you. If the situation hits an overturn condition, that is stated explicitly.
- **Storage.** The default public shape is one JSON array at `views/consensus.json`, relative to the workspace root, containing only entries you confirmed. The directory and file are created only when you confirm a write. You may optionally point projects at one shared absolute path. This repository ships only [templates/views/consensus.empty.json](templates/views/consensus.empty.json) and a fictional [templates/views/consensus.example.json](templates/views/consensus.example.json). See [templates/README.md](templates/README.md).
- **Optional hub and mirror.** Some environments may treat a shared hub file as the source of truth and keep an optional local mirror for reading. After a successful hub write, the mirror may be overwritten from the hub. If they disagree, the hub wins. The public skill does not hard-code a personal drive path or one product’s absolute path; those paths come from your own mapping.

### Adjusted relative to v0.1.2

- “收尾与行动” adds the save question and lines it up with the exit rule.
- “保持轻量与可退出” still refuses an automatic profile or automatic saving of private chat. A confirmed consensus document is the only new opt-in place to keep a record.
- The frontmatter `description` mentions optional save and topic-related review so the skill can be found. The main examination path is unchanged.

### Corrected from an earlier one-file-per-entry draft

- The default is not one Markdown file per entry, and not an optional index of those files.
- It is one JSON array. Revisions are compared with each entry’s `updated_at`, not with file creation time.
- Across machines, the optional pattern is hub as source of truth plus a local mirror, configured outside the public skill text.

### Not in this version

- No new “sage” bot, and no skill index whose library has nowhere to be stored.
- No feedback-mailbox automation, mail-notification bot, SkillHub admin flow, or extra platform republish.
- No real user consensus in the public tree, and no personal absolute paths or specific assistant product names in the public skill.

### Validation

No new scripted simulation was run for this change. Useful checks after landing: confirm / refuse / exit-interrupts-save, topic-related reads that label overturn conditions, JSON field completeness, an override path, and (only if that mode is on) hub-then-mirror overwrite.

中文：在反例与事实规则不变的前提下，增加「确认后写入单一 JSON 共识库，并在主题相关的计划或决策中供复查」的可选能力。每条含 `updated_at`。公开仓库只放 `templates/views/` 的空模板与虚构示例。枢纽与本机镜像用通用措辞，路径由你的映射提供，不写个人盘符或具体助手产品名。未确认不写入；你明确结束对话时，不为入库打断退出。已安装的 v0.1.2 不会自动升级。本版落地前未跑新一轮模拟回归。

## v0.1.2 — Early feedback release (2026-10-17)

- Preserve the user's conditions and evaluation goal when testing counterexamples; distinguish execution warnings from objections to the stated method.
- Withdraw inapplicable objections without treating the original claim as proven.
- Prioritize relevant, verifiable evidence for real-world effects; label hypotheticals and retain evidence gaps.
- Examine specific objections and revised claims, but do not concede supported facts merely to end disagreement. Stop without requiring agreement.
- Keep one Chinese runtime core with language-following behavior. Add paired Chinese/English multi-turn simulation inputs and record the actual execution limits in [the review ledger](tests/检查记录.md).

No new runtime dependencies, telemetry, authority to act externally, or automatic updates. Existing v0.1.1 downloads and installations are unchanged.

Validation limits: twelve scripted Chinese/English conversations (36 responses) were generated in one reviewing thread with later inputs visible. Review found residual targeting issues; the final clause about not inventing the user's reasons or success criteria was statically checked but not independently rerun. Real-source retrieval, human outcomes and cross-model equivalence remain untested. This release invites feedback; it is not a claim of complete validation.

中文：本版改良反例适用性、真实证据边界和持续分歧处理。最后一处定向修订尚未独立重测，真实检索与真人效果未验证。旧版保持可下载，已安装的副本不会自动升级。

## v0.1.1 — Early feedback release

Own Your View helps people examine everyday ideas that resonate with them before adopting or acting on them.

It offers relevant counterexamples, checks key facts when tools allow, and usually waits for the user's own response before proposing a rewritten view. Users can disagree, ask for a direct answer, or stop. Replies follow the user's language unless another language is requested.

This release includes one core skill, English/Chinese project introductions, an MIT license, a feedback template, source acknowledgements, and validation records. Eight initial model-simulation cases and four later language cases have been reviewed; these are not real-user learning outcomes or cross-model certification.

We are looking for people with a similar use case and for concrete suggestions. Please report where it helped, made thinking harder, offered an irrelevant objection, or rewrote your view too soon. A minimal anonymized excerpt is enough.

Created by NickQin001 with AI assistance. See [LICENSE](LICENSE), [English feedback](FEEDBACK.en.md), and [中文反馈](FEEDBACK.md).

The project was called Second Look during local preparation. Before its first public release, its display name and runtime identifier were changed to Own Your View / `own-your-view`; the conversational rules were not changed.

## 中文说明

这是用于收集反馈的早期试用版。欢迎分享具体问题，也欢迎指出这套方法什么时候不适用。尚无真人效果或长期认知提升数据，不要求用户认同 AI 才算成功。
