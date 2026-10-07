# 发布约定

## 发布单元与状态权威

本仓库没有代表所有标准的总版本。core 的标识与版本唯一来源是 [core/PROTOCOL.md](../core/PROTOCOL.md)；工程标准的标识与版本唯一来源是[工程正文](../standards/AGENT_COLLABORATION.md)；目录标准保留其自身版本来源。清单与导航展示值必须与正文核验一致。

根 [manifest.json](manifest.json) 始终表示其所在固定快照的当前 core，不改成版本数组，也不设第二份“当前 core 清单”。工程 1.0.0 使用 [独立清单](../standards/releases/agent-collaboration/1.0.0/manifest.json)，目录 1.0.0 使用[原独立清单](../standards/releases/project-structure/1.0.0/manifest.json)。Codex 和任务模板按文件哈希定位，不另立版本或清单。

发布、生效和批准状态由对应清单及可信批准共同确定，正文不持有随批准翻转的 status。规范生效不证明客户端自动加载、配置安装、同步、产品部署或全天运行。清单、标签、Git author、PR 作者、机器人评论和同账号事件都不能自行证明批准身份或权限。

## 兼容契约与历史范围

core 2.0.0 正文中明确的兼容契约是本版随精确材料申请批准的契约，不追认为 core 1.0.0 曾承诺。旧合规做法因必遵义务变化而必须调整时按 MAJOR；完全可选且不使旧做法失效的能力才是 MINOR，仅修辞澄清为 PATCH。保持 R001–R021 原文不等于义务完全兼容。工程标准首次 1.0.0、目录标准保持 1.0.0，各自独立生命周期。

源仓库的发布任务须在获准外置任务记录中固定原适用治理基线。正在申请批准的正文、此发布约定以及目标标签名均不自行授予发布权限。用户批准本次精确材料与动作后，才可在相应范围采用本约定办理本次发布。

## 原始字节 冻结与后生事实

先形成最终版本文字、稳定适用说明、内容和引用，再计算原始 UTF-8/LF 字节摘要并申请精确批准。批准后不再改非清单文件的任何字节，不把 v0.2 候选摘要用于已改变的正式材料。每个文件分别记录算法、expected、computed、字节数和来源，禁止先规范化换行或重新序列化源 JSON 再冒充原字节哈希。

本批 core 2.0.0 与工程 1.0.0 的 17 路径分为 15 个冻结文件和 2 个后生事实清单。根 files 精确登记 15 个冻结文件；两份清单不列自身或对方的最终哈希。批准范围必须包含候选清单完整结构、静态值和下文唯一允许转换的字段。其余既有三文件及历史对象保持原字节。回执可以另算最终清单哈希，但不把该值回填清单。

## 根清单字段契约

- protocol_id、version：只表示 core；与 core 正文一致。
- status、effective：候选 initial-review / false；有可核对真实批准时才转换 approved / true。
- protocol_path、protocol_sha256、hash_algorithm、hash_scope：定位 core，正文原始字节哈希，算法 sha256；protocol_sha256 必须等于 files 中 core 项。
- summary：本版内容的稳定摘要，不含“本版已批准”或实际批准时间，候选与批准阶段不变。
- approved_release：候选为 null；转换后恰含 version、protocol_sha256、approval_reference、candidate_commit、approved_on。版本、哈希为已冻结值，真实批准引用及 UTC 日期来自可信批准；candidate_commit 必须是已经产生且核验的 C。
- target_tag：core-v2.0.0，名称不证明已经创建。
- files：15 项，按 path 升序排列，每项仅 path、sha256、size_bytes；路径唯一。不是 ZIP 摘要，也不包含两份清单。
- related_standards：工程条目含 standard_id、version、manifest_path、target_tag；目录条目含 standard_id、version、commit、path、sha256、target_tag。目录来源固定 7208，不把当前 main 当成旧来源。

## 工程清单字段契约

- standard_id、version、status、effective：工程标识与正文版本，候选 initial-review / false。
- document：path、sha256、size_bytes、encoding=UTF-8、line_endings=LF。
- supporting_files：仅 templates/task-context.md、templates/MINIMAL_EXAMPLES.md，按路径排序，每项 path、sha256、size_bytes；与根 files 同源并交叉核验。
- target_repository、target_tag、manifest_path：目标 Karlsen9527/karlsen-ai-collaboration-rules、agent-collaboration-v1.0.0 及独立清单路径；不证明实际发布。
- referenced_general_rules_version、referenced_general_rules：core 2.0.0，以及同一固定快照的 core path、sha256、manifest_path；不预填本清单所在未来 commit。
- referenced_project_structure：目录 standard_id、version、commit、path、sha256、target_tag、manifest_path，固定旧版。
- approval：候选 null；正式对象恰含 reference、approved_at、candidate_commit、standard_id、version、document_path、document_sha256、material_files。material_files 逐项复制根 files 的冻结值并校验相等，不另造独立材料集合。

## 候选到批准唯一允许字段转换

以下是必须由最终批准覆盖的转换契约，本段本身不是批准：

| 文件 | 允许 JSON 路径 | 从候选到正式 |
| --- | --- | --- |
| releases/manifest.json | /status | initial-review → approved |
| releases/manifest.json | /effective | false → true |
| releases/manifest.json | /approved_release | null → 上述五字段真实批准对象 |
| standards/releases/agent-collaboration/1.0.0/manifest.json | /status | initial-review → approved |
| standards/releases/agent-collaboration/1.0.0/manifest.json | /effective | false → true |
| standards/releases/agent-collaboration/1.0.0/manifest.json | /approval | null → 上述八字段真实批准对象 |

两对象内的 reference/approval_reference、approved_at/approved_on 取自同一次真实批准；candidate_commit 取真实 C。工程批准对象中的标识、版本、正文路径及哈希、material_files 和 core 批准对象中的版本及正文哈希必须原样复制已冻结静态值。不得新增其他字段或借转换改 summary、版本、路径、哈希、材料数量、依赖、目标仓库或标签。

两清单保持两空格 JSON 缩进、UTF-8、LF 和末尾换行；C→P 的结构差异仅限表中六个路径。15 冻结文件原始字节完全相同。不预填 release_commit、自身 commit、自身 sha256 或未经发生的 published_at。不存在为了回填 R 而产生第三个内容提交的要求。

## C P R 的有界发布顺序

B 是最后核实的 main 基线；本批基线为 7208cef99ea7783a5b574b5f6829889795e1c03e。C 是包含 15 冻结文件和 2 候选清单的提交。P 基于 C，仅转换两清单的批准后生字段。R 是 PR 合并后 main 上的真实发布提交。字母只是符号，不当作真实 SHA。

1. 取得精确本地快照、15 文件摘要、完整候选清单及允许转换规则的可信批准，明确私有目标、临时分支、C/P、PR、merge 方式、两枚标签、回执及恢复边界。C 尚未存在时批准绑定可取回材料，外置记录 candidate_commit 保持 null，生成 C 后另行登记。
2. 发布前落实标签创建路线；重新读取 private、main=B、分支与标签实际状态。临时分支为 release/core-2.0.0-agent-collaboration-1.0.0；同名既有对象先核验，不覆盖未知内容。main 漂移时暂停受影响动作，不能擅自吸收差异。
3. 从 B 创建临时分支并形成 C。推荐说明：Prepare core 2.0.0 and agent collaboration 1.0.0 release candidate。远端重读 C，15 冻结文件与批准字节一致，2 清单仍 initial-review/false 且批准对象 null。
4. 在获准外置记录登记真实 C，按唯一允许转换生成 P。推荐说明：Record approved core 2.0.0 and agent collaboration 1.0.0 release。核验 C..P 仅 2 清单六个路径，所有冻结字节一致，真实批准可核对。
5. 创建面向 main 的审阅 PR，默认草稿，不启用 auto-merge；若最终动作批准覆盖，将其转为 ready。说明版本矩阵、17 路径、摘要和未实测边界。合并前重新核验 main=B、PR head=P、完整树和必要检查。
6. 仅在批准涵盖合并时，使用 expected_head_sha=P 和 merge 方式合并，读取真实 R。核验 R 树与 P 一致；若合并结果包含未批准差异，停止标签并报告。
7. 通过已落实且已批准路线创建 core-v2.0.0 和 agent-collaboration-v1.0.0，两者均指向 R。不得重写同名冲突标签、目录旧标签或补造 core 1.0.0 标签。不通过创建 GitHub Release 代建标签。
8. 重读 R、两枚标签、15 冻结文件和最终清单；校验 B..R 17 路径、旧历史仍可读，按 [ACCEPTANCE.md](../ACCEPTANCE.md) 交付真实发布回执。C 定位批准内容，R 定位最终发布；不把二者互换。

标签若需用户在已有环境完成，必须在最终批准前说明分工和等待点；交付真实 R 后由用户执行已批准标签动作，再只读核验。未核验两标签前，只能报告 main 合并完成、标签待完成，不能称规范发布完成。此分工不授权助手使用用户电脑或凭据。

## 读取与历史定位

1. 从可信渠道或已有已批准 pin 取得目标固定提交，不仅信任 main、同账号文字或标签名。
2. 同一提交读取目标正文与清单，核验标识、版本、路径、原始字节、状态和可信批准。根清单只代表那个快照的 core。
3. 工程采用者另核验独立清单、正文、配套文件和依赖；仅支持旧 core 字段的接入器不能冒称整包支持。
4. 新版本查询与采用分开；保持权限、撤销和缓存检查。离线旧字节一致不证明当前权限或未撤销。
5. core 1.0.0 历史组合为 [7115 正文](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/7115cc9e8c262f6d07c7f89558c1f477593bf8e5/core/PROTOCOL.md)及[7115 根清单](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/7115cc9e8c262f6d07c7f89558c1f477593bf8e5/releases/manifest.json)，正文 SHA-256 284cae9edb5f41ef88d26dc7ce19e4cf8ab167468e3de0adf04d53879209d8c0。无旧标签，不补造。
6. 目录 1.0.0 为 [7208 正文](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/7208cef99ea7783a5b574b5f6829889795e1c03e/standards/PROJECT_STRUCTURE.md)及[原清单](https://github.com/Karlsen9527/karlsen-ai-collaboration-rules/blob/7208cef99ea7783a5b574b5f6829889795e1c03e/standards/releases/project-structure/1.0.0/manifest.json)，正文 SHA-256 01ec4306eb4b37468ad63e518a9c9a129ade863acfe4fc7538c51c7bd2961177，原标签 project-structure-v1.0.0 指向 7208cef99ea7783a5b574b5f6829889795e1c03e。原清单引用 core 1.0.0 是历史事实，保持不变。

旧版不因新版本存在而自动 revoked 或 effective=false；撤销、停用或回退需真实决定。新发布只让 main 出现新版，不改写旧组合。目录标准旧文中的本次不改旧 core，限定其当时独立发布；本次另行申请 core 新版，不能借新正文改写历史。

## 批准证据与失败恢复

真实批准必须关联经过认证的用户渠道、精确材料、逐文件哈希、有界动作与批准时间。仓库只写适合共享的引用与必要事实，不复制私聊、批准原文、私人日志或身份秘密。批准引用不可核对则保持未核实并暂停依赖步骤，清单本身不是信任根。

工具返回不确定时先读回实际分支、提交、PR、标签，确认未发生才作相同范围重试，不重做已完成动作。字节不符、main/head 漂移、权限或目标变化、同名标签冲突时停止受影响写入并说明。用户停止时核实已完成外部状态，不自行回滚或删除标签。发布后缺陷通过另行批准的新版本修复或 revert，禁止强推改历史。

本约定不创建 GitHub 保护规则、签名服务、自动发布、CI、轮询器或加载服务；这些能力未有实际证据时保持未验证。
