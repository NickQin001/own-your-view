# Release notes

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
