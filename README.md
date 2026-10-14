# AI 协作规范仓库

本仓库维护用户与主助手的唯一协作正文、独立工程标准与目录标准。发布和生效状态以同一固定快照的对应清单及可核对的可信批准为准；本文的版本导航不构成批准，也不证明部署。

## 发布单元与版本来源

| 单元 | 标识 | 本快照正文版本 | 版本唯一来源 | 状态与材料清单 |
| --- | --- | --- | --- | --- |
| 用户与主助手协作 | general-collaboration-protocol | 9.0.0 | [core 正文](core/PROTOCOL.md) | [根清单](releases/manifest.json) |
| 工程协作 | agent-engineering-collaboration | 1.1.0 | [工程正文](standards/AGENT_COLLABORATION.md) | [独立清单](standards/releases/agent-collaboration/1.1.0/manifest.json) |
| 目录与版本管理 | project-structure-and-versioning | 1.0.0 | [目录正文](standards/PROJECT_STRUCTURE.md) | [原独立清单](standards/releases/project-structure/1.0.0/manifest.json) |

没有单一“仓库总版本”。两行 Codex 偏好与模板是逐文件固定的附属材料，不另设版本权威。core 2.0.0 的兼容契约随其精确材料批准，不追认 core 1.0.0 已承诺该契约。旧合规流程可能需调整原始字节核验、并发与历史证据处理；仅保留旧条文不证明完全兼容。工程标准采用仍由各项目决定。

本快照 core 9.0.0 为待审候选：新需求持续收集，用户明确补充完毕后汇总、补齐关键缺口，以双选菜单确认需求；确认仅进入方案设计。原三选菜单限于方案执行决策，明确小改不能绕过需求收集。旧合规流程需调整，归 MAJOR。唯一规则正文仍为 core；候选不构成生效，旧批准不自动撤销。

历史 core 2.0.0 及其根清单固定从 [原发布 07fffb46](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/tree/07fffb46a1946392d63614dd82e698cef8f0cec0) 读取。工程 1.1.0 仍按 [原发布 bfc785b7](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/tree/bfc785b7c45a11cc39cf0a6374349ca5a92ffe01) 及其独立清单核验，固定 core 2.0.0 依赖不变。旧根清单摘要只核验旧发布材料，不校验当前导航文件；新版 core 根清单也不替代工程 1.1.0 的独立批准。有限批次仅对显式选用者适用，不改变旧 1.0.0 工作流。

## 结构

- [AGENTS.md](AGENTS.md) 与 [CLAUDE.md](CLAUDE.md)：薄加载入口
- [adapters/README.md](adapters/README.md)：接入与缓存契约、运行验证边界
- [DSH 接入说明](adapters/dsh/README.md)：有限批次原生权限及终态交付顺序
- [Codex 接入说明](adapters/codex/README.md)及[两行配置示例](adapters/codex/config.toml.example)：不自动安装
- [通用模板导航](templates/README.md)与[新需求开场口令](templates/new-requirement-opener.md)：先单独发送口令，确认完整读完规范后再另发需求；后续按 core 第5节持续收集，结束补充后确认需求；加载唯一 core 正文，不复制第二套规则
- [项目模板](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/07fffb46a1946392d63614dd82e698cef8f0cec0/templates/project-spec.md)、[工程任务模板](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/07fffb46a1946392d63614dd82e698cef8f0cec0/templates/task-context.md)、[最小示例与唯一 A01–A16 场景](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/07fffb46a1946392d63614dd82e698cef8f0cec0/templates/MINIMAL_EXAMPLES.md)
- [本仓库实施说明](projects/rules-repository/PROJECT_SPEC.md)：稳定维护职责与流程
- [发布约定](releases/README.md)、[内容变更记录](CHANGELOG.md)、[验收要求](ACCEPTANCE.md)
- [.gitignore](.gitignore)：降低误纳入风险，不是访问控制

## 使用与信任

主干按 projects/<project-id>/ 组织项目，不用长期项目分支隔离上下文；短期变更分支用于审查，业务代码保留在业务仓库。执行者只按完整任务路线读取当前项目明确约束及自己的任务上下文，不默认加载 core；工程标准只对明确采用的任务适用，其已固定的历史依赖继续保留。

本仓库为公开仓库，固定提交正文可匿名读取，无需登录 GitHub；目录不是权限隔离，任何读者都可能看到仓库内全部项目规范。不提交个人对话、实际审批原文、身份秘密、凭据、私人日志、上传原图或同事私人数据。SHA-256 证明内容一致，不证明身份、授权或运行通过。

启动项目、批准变更和发布前固定可信来源及适用 pin；核验正式发布或执行依赖原批准的动作时，同提交核验适用正文、清单和批准引用，普通读取与自身会话采用按下述能力及信任边界处理；可复用仍有效的已核验缓存，不要求日常每句沟通重复核验。新版本只触发影响评估，不自动更新旧项目 pin、用户模型配置或任务 revision；源仓库发布、项目采纳与客户端部署分别批准、分别验收。读取入口不保证客户端会发现或执行它。

公开可读和内容哈希不证明批准。外部使用者可在自身会话明确采用固定内容，但不可把无法核对的私人批准引用称为已核验；仅暂停依赖该批准的动作，读取、讨论与准备材料可继续。不得公开私人批准原文，细则见 [接入说明](adapters/README.md)。

## 历史固定入口

- [core 1.0.0 正文](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/7115cc9e8c262f6d07c7f89558c1f477593bf8e5/core/PROTOCOL.md)与[当时根清单](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/7115cc9e8c262f6d07c7f89558c1f477593bf8e5/releases/manifest.json)，固定提交 7115cc9e8c262f6d07c7f89558c1f477593bf8e5。原正文 SHA-256：284cae9edb5f41ef88d26dc7ce19e4cf8ab167468e3de0adf04d53879209d8c0。该版没有历史标签，不补造。
- [目录标准 1.0.0 快照](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/tree/7208cef99ea7783a5b574b5f6829889795e1c03e)，原标签 project-structure-v1.0.0 指向 7208cef99ea7783a5b574b5f6829889795e1c03e；历史清单引用 core 1.0.0 保持原样。
- 历史版本不因出现新版本而自动 revoked 或 effective=false。撤销需真实决定；当前 main 同名文件不能代替旧版字节。

## 维护方式

维护者按对应版本契约固定正文、版本和机器摘要，取得精确正文及有界发布范围批准。配套更新须限于批准的必要范围；根清单材料摘要证明发布完整性，不代表用户逐字审阅所有配套。正文冻结后不回填批准状态或日期，真实审批只进入获准清单字段；实际远端结果放发布回执。具体见发布约定。不自动创建工作流、签名服务、同步器或 GitHub Release。

参考资料：[Claude 的 AGENTS.md 说明](https://code.claude.com/docs/en/memory#agents-md)、[Anthropic Constitution](https://www.anthropic.com/constitution)、[Agent Skills 规范](https://agentskills.io/specification)。资料仅解释各自机制，不构成本仓库自动执行保证。
