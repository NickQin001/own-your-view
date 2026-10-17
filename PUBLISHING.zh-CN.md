# 首次发布与寻找试用者

2026-10-17 版本说明：本包对应 v0.1.2 早期试用版，[GitHub 版本页](https://github.com/NickQin001/own-your-view/releases/tag/v0.1.2)提供源码与下载。旧 v0.1.1 标签和下载包保留，不包含本次核心修订。验证范围及未覆盖项见 [检查账本](tests/检查记录.md)。GitHub 发布不等于 SkillHub 已更新，也不会自动升级个人安装副本。

SkillHub 下列 2026-10-16 段落是 v0.1.1 准备记录，不要用旧 ZIP 提交新版。若从 GitHub 导入，请选本仓库的 `skills/own-your-view`，核对版本填写为 `0.1.2` 且内容含本次三项改良；平台是否重新抓取源码需在提交页核实。本项目未收到平台提交或审核回执，不声称已更新 SkillHub。不要重复创建同名条目，先在自己的已有条目中检查更新入口。

更新日期：2026-10-14。公开名称：Own Your View · 想清楚，再相信；项目地址：[NickQin001/own-your-view](https://github.com/NickQin001/own-your-view)。公开仓库已上传并核验 14 个文件，默认分支 main，MIT 许可证已被 GitHub 识别，Issues 已启用。本文介绍后续发布维护与反馈渠道；具体文件和发行状态以远程页面为准。

## SkillHub 发布准备（2026-10-16）

状态：上传包与填写文案已准备，尚未提交、未通过平台审核，也没有 SkillHub 上架链接。GitHub 仍是源码与反馈入口。

官方[使用指南](https://skillhub.cn/tutorials)说明：一次性发布少量 Skill 可用网页；发布需要手机号登录和实名认证，人脸核身需本人完成。Windows CLI 路线需 WSL，本次准备网页上传。官网的[Agent 发布规范](https://skillhub.cn/ai/release.md)列出必填元信息 slug、version、displayName；已在专用包中补齐，原始核心文件保持不变。

### 上传文件与填写内容

本地“当前版本”文件夹中的 `own-your-view-skillhub-0.1.1.zip` 是此次专用上传包，ZIP 根目录只有 SKILL.md、LICENSE、README.md。不要上传整个本地项目或带 .git 的文件夹。此 ZIP 被既有 .gitignore 排除，不随 GitHub 源码提交；它与 GitHub 的旧发行 ZIP 是不同产物。

填写文案如下；分类是否可选以实际表单为准：

| 内容 | 准备值 |
| --- | --- |
| 显示名称 | Own Your View · 想清楚，再相信 |
| Slug | own-your-view（可用性仍需提交页确认） |
| 版本 | 0.1.1 |
| 简介 | 通过逐步提问、反例和关键事实查证，帮助你检验产生共鸣的观点，形成自己的判断。 |
| 作者署名 | NickQin001 |
| 许可证 | MIT |
| 项目主页 / 源码 | https://github.com/NickQin001/own-your-view |
| 建议分类 | 教育学习；若表单无该选项，按实际选项选择最接近的类别 |
| 版本说明 | 首次在 SkillHub 发布。基于核心版本 0.1.1，补充平台发布元信息，核心交互规则保持一致。 |

详细介绍可复制：

> 读到或听到一个让你产生共鸣的观点后，先检查它的依据、反例和适用边界，再决定保留、修改或暂不确定。Own Your View 每次聚焦一个关键问题，AI 可以直接举反例，通常等你回应后再提供可审阅的改写。你可以反驳 AI、保留原观点或随时停止。适用于日常观点、阅读和访谈感悟；默认跟随提问语言。项目按 MIT 开源，欢迎通过 GitHub Issues 提供具体、脱敏的试用反馈。目前处于早期试用阶段，不承诺观点绝对正确或学习效果。

### 需要本人完成的环节

1. 打开[个人发布页](https://skillhub.cn/dashboard/publish)，登录后按官网要求完成实名认证。实名资料只在官网提交，不发送到聊天。官方[服务协议](https://privacy.qq.com/document/preview/5bd4610b10f043d98df5dd69233cc3b3)与[隐私协议](https://privacy.qq.com/document/preview/af7cf7a60e444f93a3fbff81c929cca8)需本人查看；本次抓取协议正文超时，未完成条款核对。
2. 上传上述 ZIP，核对自动识别的名称、版本、简介和文件列表。如 Slug 冲突，先确认现有条目归属，不覆盖其他条目；确认自己的平台账号后再决定替代 Slug。
3. 提交后记录平台实际返回的状态。提交成功或 pending_review 仅代表进入审核；详情页公开可访问且内容正确后，才记录为已上架。

平台官方仓库提到 GitHub 导入，但尚未通过已登录表单验证子目录导入及授权范围。本次优先准备 ZIP 上传；不需要为一次网页发布创建 API 密钥。以后若改用 CLI，先核验官方客户端、认证保存方式及权限，不把密钥贴入聊天或文档。

### 已完成核验与缺口

- ZIP 三个文件均已解压读取核对，正文与当前核心逐字一致，仅增加 SkillHub 元信息；保留 MIT 署名和来源。
- 原始核心通过 skill-creator 结构校验。平台包另做 YAML 字段、版本、Slug 和正文一致性核验；没有安装 SkillHub CLI，未运行其 dry-run，不能声称通过平台校验。
- 官方公开搜索中未看到与 own-your-view 完全匹配的结果；模糊搜索不能证明 Slug 未被占用。
- ZIP SHA256：`B788F70030FDE578DF20C7786CF4DFEC85D1E38B958B09655241510DE769FBE4`。平台 SKILL.md SHA256：`A56B9A4DAC113A2B26D6CC80F7E0DD45A72FFD8D4A7C0157C9EE7CA82BB3CED1`。

## 先把署名与隐私分开

许可证使用 `Copyright (c) 2026 NickQin001`，项目介绍链接到公开 GitHub 主页；不写真实姓名、个人邮箱或工作单位。这样可以保留来源，但不保证用户名不会被熟人或其他账号关联到现实身份。

2026-10-14 的公开接口检查显示：姓名、邮箱、公司、位置、网站、简介和社交账号字段为空。没有审计现有仓库的全部内容、历史提交或头像，不能据此判断整个账户完全匿名。没有读取账户的私有设置。

在 GitHub 点击右上角头像 → Settings：

1. 在 Public profile 检查公开名称、头像和其他资料。可以用公开笔名，避免写入不希望公开的身份信息。
2. 在 Emails 启用 **Keep my email addresses private**。如页面提供 **Block command line pushes that expose my email**，也启用它。
3. 如果以后通过本地 Git 提交，使用该页面显示的 GitHub `noreply` 地址，并只为本仓库配置提交作者。改变配置不会清除历史提交已经记录的旧信息。

用户名和公开显示名称是不同的字段。若想改用户名，Settings → Account → Change username；先阅读 GitHub 对旧链接等影响的提示，再决定。当前无需为了发布而强制改名。

参考：[提交邮箱设置](https://docs.github.com/en/account-and-profile/how-tos/email-preferences/setting-your-commit-email-address)、[修改用户名](https://docs.github.com/en/account-and-profile/how-tos/account-management/changing-your-username)。

## 邮箱隐藏仍然可以收到反馈

邮箱隐私控制公开提交中是否展示个人邮箱，通知设置控制 GitHub 是否把仓库动态发到你的邮箱。这是两个独立用途。保留已验证的账号邮箱并启用邮箱隐私，不会因此关闭 Issues 或 Pull Request 的通知。

发布后到本仓库的 Watch → Custom 选择 Issues；再打开 [通知设置](https://github.com/settings/notifications)，为 Watching / Participating 选择 Email。使用者提交的意见可以保留在 Issues 中，GitHub 将按订阅和通知设置发送邮件；不需要把个人邮箱写进 README。

如果以后希望接受私下意见，可以另设项目联系邮箱。公开地址也可能收到垃圾邮件或钓鱼内容，无法预先判断比例；当前建议先用 Issues。参考：[GitHub 通知说明](https://docs.github.com/en/subscriptions-and-notifications/get-started/configuring-notifications)。

## 发布入口与安全优先

这里的 GitHub 插件是支持该能力的 ChatGPT / Codex 界面中的连接，和 VS Code 扩展市场不是同一个入口。截图中的 Copilot、主题、Pull Requests 等扩展也不是这次网页发布的必要条件；不需要为了发布本项目安装它们。

[OpenAI 插件说明](https://learn.chatgpt.com/docs/plugins)与[更新日志](https://learn.chatgpt.com/docs/changelog)对 IDE 支持的描述存在冲突；不能仅凭其中一页断言本机可用性。本机扩展后台能执行插件安装命令，但独立终端会话启动先出现缺完整包提示，使用报错建议参数后又出现工作区路由超时。用户最终通过官网完成连接，本会话已实际读取 GitHub 账号及已有仓库元数据。无需继续处理终端启动问题才能推进发布。

本次使用从官方发行附件下载、经官方 SHA256 校验的 GitHub CLI 2.102.0 便携版，不修改系统 PATH。用户在本机完成独立授权后，主流程确认登录账号及系统凭证库存储，创建了本项目公开仓库。账号连接成功不代表全部仓库都已授权，也不等于完整 OAuth 审计；没有修改账号隐私设置或其他仓库。

## 路线一：通过已连接的 GitHub 发布入口

本会话已完成 GitHub 连接，可以继续核对目标账户、仓库和待上传文件。新仓库需要通过官网或另行授权的官方 GitHub CLI 创建，不能假设插件拥有缺失的接口；创建后再使用可用写入能力上传。不要向聊天提供密码、验证码或访问令牌。

官方 GitHub CLI 支持 [创建仓库](https://cli.github.com/manual/gh_repo_create)，但其[网页登录](https://cli.github.com/manual/gh_auth_login)是另一项账号授权，不能假设与插件连接共享。默认授权可能包含 `repo`、`read:org`、`gist`，范围不限于本公开项目；如果用户不接受新增权限，改为在官网手动创建空仓库，再由插件处理上传。登录默认尝试系统凭证存储，失败时可能回退到明文文件；不要启用 `--insecure-storage`，也不要将凭证文件纳入项目包。

准备公开的内容就是本文件所在的整个项目包，包括隐藏的 `.github` 文件夹。上层的 archive、LATEST、私人交接和其他项目均不在上传范围内。

`.gitignore` 仅控制 Git 提交，不替代网页上传前的文件列表核对。

## 路线二：直接在网页发布（2026-10-14 首次发布历史步骤）

适合暂不使用连接入口的情况，不需要先学 Git 命令。

1. 登录 NickQin001 账户，打开 GitHub 的 [New repository](https://github.com/new) 页面。
2. Owner 选 NickQin001，Repository name 填 `own-your-view`；若提示已占用，先确认是否自己已有该仓库，不覆盖旧内容。
3. Description 可直接复制：

   `A lightweight AI skill for examining everyday ideas before adopting or acting on them. Feedback welcome.`

4. 选择 Public。当前文件已含 README 和 MIT LICENSE，不必再让 GitHub生成另一个版本，创建仓库。
5. 进入上传文件页面。仓库有文件时可用 **Add file → Upload files**；空仓库首页也提供上传已有文件的入口。将本文件夹里的文件及子文件夹上传，保持目录结构，检查根目录直接包含 README.md、LICENSE 和 skills 文件夹。
6. `.github` 是隐藏目录，文件管理器可能需要开启隐藏项目才能看到。若网页没有上传成功，可用 **Add file → Create new file** 输入 `.github/ISSUE_TEMPLATE/feedback.md`，粘贴本地同名文件内容。该文件应位于默认分支，模板才会出现在新建 Issue 页面。
7. 提交说明可填 `Publish Own Your View v0.1.1 early feedback version`，提交后检查英文首页、中文链接、核心文件及 LICENSE 是否都能打开。
8. 确认仓库启用了 Issues，查看反馈模板是否出现。需要发布版本时进入 Releases，创建 `v0.1.1`，使用 RELEASE_NOTES.md 的内容，并标为早期试用 / pre-release。

参考：[创建仓库](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)、[上传文件](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)、[Issue 模板](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates)、[发布版本](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)。界面和账户权限可能有差异，以实际页面为准。

## 让别人更容易发现和试用

发布只是有了一个可访问的地址，不保证有人发现。先完成下面这些具体动作，再根据反馈决定是否继续扩大分享。

- 仓库 About 添加相关 Topics，例如 `agent-skills`、`critical-thinking`、`socratic-method`、`learning`、`ai`。这些是可选主题，不宣称已获得任何目录收录。
- 在自己的 GitHub 主页置顶这个仓库。
- 在自己已经参与、允许项目分享的 AI 或阅读讨论社区发一则简短邀请，附一个自拟使用案例和项目链接；先看社区规则。
- 请少量愿意试用的人带着真实观点使用，收集具体哪里有帮助、哪里太费力；不要只以星标数或好评判断效果。
- 回应反馈时说明哪些建议采纳、为什么，以及对应修改。不为一次反馈叠加大量永久约束。

Topics 的作用见 [GitHub 官方说明](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)。对外发帖和私信由用户决定，本材料不会自动发送。

## 可直接使用的分享文案

中文：

> 我做了一个叫 Own Your View（想清楚，再相信）的小 Skill：读到或听到一个很有共鸣的观点后，让 AI 帮我检查依据和反例，再决定哪些部分值得保留。AI 可以直接举反例，但通常等我回应后再建议改写。我把它按 MIT 开源，希望找到有类似需求的人。欢迎试用后告诉我哪里有帮助、哪里问得太多，或者哪里判断错了。项目地址可以从我的 GitHub 主页 NickQin001 进入。

English:

> I made Own Your View, a small AI skill for examining ideas that resonate with us before we adopt or act on them. It can offer counterexamples immediately, but usually waits for our own response before suggesting a rewritten view. I'm sharing it under MIT to find people with a similar use case and learn from concrete feedback. If you try it, I'd love to hear where it helped, made thinking harder, or got something wrong. You can find it through my GitHub profile, NickQin001.

实际发布前不要把“已开源”文案当作已经发生的事实发出；发布后把最后一句替换为核验过的仓库链接。文案没有测试效果或用户数量的承诺。
