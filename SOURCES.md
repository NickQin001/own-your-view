# 借鉴记录与复用边界

记录日期：2026-10-13。核心指令为围绕本项目已确认需求独立组织的中文文本；本包不附带第三方源码、原始对话、书籍或视频全文。

## 已参考的机制

| 来源 | 参考点 | 本项目的取舍 |
| --- | --- | --- |
| [liulifeng8918/socratic-dialogue-skill](https://github.com/liulifeng8918/socratic-dialogue-skill)，[核心指令](https://raw.githubusercontent.com/liulifeng8918/socratic-dialogue-skill/main/skills/socratic-dialogue/SKILL.md) | 围绕用户原话，轻量提问，允许直接回答与退出 | 反例可直接给；观点改写按用户回应情况延后，明确请求时例外 |
| [tronghieu/agent-skills 的 critical-thinking](https://github.com/tronghieu/agent-skills/tree/main/skills/critical-thinking)，[核心指令](https://raw.githubusercontent.com/tronghieu/agent-skills/main/skills/critical-thinking/SKILL.md) | 用户先表达判断，再对照审查；质疑锚定具体论证 | 不用与 AI 一致作为准确度；不自动保存个人推理档案；不采用完整审计分类体系 |

本地 grilling 工作方式也启发了逐项讨论，但本 Skill 不依赖它运行，不沿用每次提问必须给推荐答案的安排。

以上两份远程核心指令在记录日重新读取。链接指向可变的 main 分支，未固定 commit SHA，页面缓存与上游更新可能影响内容；不能据此重建精确版本对照实验。实际运行对照前需固定版本、模型、工具条件和输入。

## 本项目单独明确的重点

主动思考优先；区分反例与推荐改写；查证关键前提；允许分歧和阶段性收尾；保留可选验证行动；自愿换情境检验。这里记录的是具体设计选择，不主张这些理念由本项目首创。

## 尚未做的事

- 没有运行上述第三方 Skill，也没有证明本项目优于它们。
- 没有整体移植、逐段翻译或捆绑第三方实现；不假借其作者背书。
- 本项目已按用户选择采用 [MIT 许可证](LICENSE)，版权署名为公开 GitHub 用户名 NickQin001。本记录不是许可证，也不替代实际发布状态的核验。
- 后续若直接复制或改编第三方文本，先核验所用版本的许可、保留要求及适用范围，并添加必要声明；本项目的 MIT 授权不能代替第三方要求。
