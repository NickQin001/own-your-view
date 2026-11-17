# v0.1.5 发布与安装包说明

版本：0.1.5，早期试用版。[GitHub 版本与下载](https://github.com/NickQin001/own-your-view/releases/tag/v0.1.5)。

## 两种安装包

- `own-your-view-v0.1.5.zip`：完整公共源码，包含 Skill、说明、许可、模板和测试材料。
- `own-your-view-skillhub-0.1.5.zip`：SkillHub 专用上传包，根目录仅 `SKILL.md`、`LICENSE`、`README.md`。
- `SHA256SUMS.txt`：两个包的 SHA256，随 Release 提供。源码不包含构建 ZIP 自身。

平台包在核心 YAML 中增加 slug、version、displayName、summary、license、homepage；Skill 正文与仓库核心相同。平台元信息不复制进核心文件。

## SkillHub 填写信息

| 项目 | 值 |
|---|---|
| slug | own-your-view |
| version | 0.1.5 |
| displayName | Own Your View · 想清楚，再相信 |
| summary | 通过逐步提问、反例和关键事实查证检验观点，确认后可保存可复查的现行判断。 |
| license | MIT |
| homepage | https://github.com/NickQin001/own-your-view |

变更说明：

> 默认改为个人共享观点库：首次调用把实际绝对路径保存到用户主目录的 .own-your-view/config.json，后续工作区复用。沿用明确约定或当前工作区的旧库，不自动搬迁、扫描或合并。配置初始化不等于观点入库；观点仍须明确确认并读回核验。保留结构化推敲、适用边界及异常处理；不承诺跨设备同步或跨模型一致性。

## 提交与状态核验

优先更新已有 `own-your-view` 条目，核对归属和版本，避免重复创建。使用平台当前支持的网页上传或已登录 CLI；不在聊天、仓库或包内提供凭证。发布前使用本机 CLI 帮助核对参数并进行本地 dry-run。

GitHub 发布、SkillHub 提交、审核通过与公开可见是不同状态。此文提供包和填写信息，不充当 SkillHub 提交回执；以平台返回和公开版本内容为准。GitHub 发布也不会自动更新他人的安装副本。

历史包保留在各版本 Release，不覆盖旧附件。真实观点库、全局个人规则、备份和本地验证依赖不属于发布内容。

验证范围见[本轮摘要](tests/20261117_个人共享库验收.md)，历史变化见[发行说明](RELEASE_NOTES.md)。
