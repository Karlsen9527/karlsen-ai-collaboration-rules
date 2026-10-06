# AI 协作规范仓库

中文名称：《通用对话协作规范》  
稳定标识：general-collaboration-protocol  
版本：1.0.0；发布状态：approved（已批准生效）。

发布状态以同一提交的发布清单及可信批准证据为准。规范批准生效与工具自动加载是不同事项；自动加载尚未启用。

这是 GitHub 私有仓库 karlsen-ai-collaboration-rules 的首个正式规范版本。当前正文来自用户明确批准的固定候选，版本、正文 SHA-256、候选提交与批准引用见[发布清单](releases/manifest.json)及[发布记录](releases/README.md)。创建或推送仓库的许可不等于规则全文批准；仓库记录本身不替代可信批准证据。

## 结构

- [core/PROTOCOL.md](core/PROTOCOL.md)：唯一通用正文，使用稳定规则编号
- [releases/manifest.json](releases/manifest.json)：版本、状态、摘要、正文 SHA-256
- [AGENTS.md](AGENTS.md) 与 [CLAUDE.md](CLAUDE.md)：薄加载入口，不复制正文
- [adapters/README.md](adapters/README.md)：模型/工具接入契约及未实现边界
- [templates/project-spec.md](templates/project-spec.md)：项目规范模板
- [templates/task-context.md](templates/task-context.md)：任务上下文空模板，实例存于任务私有空间
- [projects/rules-repository/PROJECT_SPEC.md](projects/rules-repository/PROJECT_SPEC.md)：本仓库实施规范
- [releases/README.md](releases/README.md)：草稿转正式的发布约定
- [CHANGELOG.md](CHANGELOG.md)：内容变更记录
- [ACCEPTANCE.md](ACCEPTANCE.md)：验收与接入测试清单
- [.gitignore](.gitignore)：降低意外纳入私有文件的风险

## 使用与信任

主干按 projects/<project-id>/ 组织项目，不用长期项目分支分隔上下文；短期变更分支可用于审查。业务代码保留在各自业务仓库。

任务只读取通用正文、明确当前项目及自己的上下文。共享仓库只包含可共享规范；目录不是权限隔离。获得仓库权限的成员可看到仓库内所有项目规范，不得将个人对话、任务审批、凭据、内部工作笔记、上传原图或同事私人数据提交进来。

正式接入须先建立可信发布源，再核验同一提交的正文与清单。SHA-256 用于内容一致性校验，不证明批准者身份或授权。加载入口不会自行同步，也不保证任意客户端会发现或执行它。参见[接入约定](adapters/README.md)。

## 维护方式

维护者提出变更，用户批准确切正文后才能发布 approved 版本。首次批准流程见[发布约定](releases/README.md)。后续新增模型复用同一正文，仅增加必要入口；不得复制分叉通用规则。

相关官方资料：[Claude 的 AGENTS.md 说明](https://code.claude.com/docs/en/memory#agents-md)、[Anthropic Constitution](https://www.anthropic.com/constitution)、[Agent Skills 规范](https://agentskills.io/specification)。这些资料仅帮助理解各自机制，不构成本仓库规则或自动执行保证。
