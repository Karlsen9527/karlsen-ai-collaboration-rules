# 发布约定

## core 5.0.1 发布约定

本节仅适用于 5.0.1；以下 5.0.0 及更早契约完整保留，其中“本次”“当前”和基线只指各历史发布。本次仅在总纲首段澄清通用规范与项目规范的适用和修改授权边界，既有合规流程不增加义务，归 PATCH；不叠加旧版文件全摘要预批准或标签要求。

用户批准精确版本 5.0.1、core 原始字节 SHA-256 10c579082b84d2eac94b00e9c5106cfcb861da395f192b842292bd0053e93bbf（8232 bytes），及必要发布记录、清单和入口更新。正文不得改变，变化须重算并补批；配套摘要用于发布完整性，不声称用户逐字审核全部配套。

基线 B=d8515369a88d294d4fe9734615ca0baf2b8f9a9b。仅更新 core/PROTOCOL.md、releases/manifest.json、AGENTS.md、CLAUDE.md、README.md、CHANGELOG.md、ACCEPTANCE.md、releases/README.md、projects/rules-repository/PROJECT_SPEC.md、adapters/README.md、adapters/codex/README.md、adapters/dsh/README.md 共 12 路径；独立标准及清单、模板、模型配置和业务项目不变，不新增自动化。

沿用 5.0.0 的 C/P/R 顺序：C 包含固定材料及候选清单，version=5.0.1、status=initial-review、effective=false、approved_release=null、target_tag=null；files 按路径升序机器记录 11 个非清单材料的原始字节 SHA-256 和大小，related_standards 原样保留。核验真实 C 后，P 只转换 /status 为 approved、/effective 为 true、/approved_release 为恰含 version、protocol_sha256、approval_reference、candidate_commit、approved_on 的对象；版本和摘要复制固定值，引用及 UTC 日期来自真实批准，candidate_commit 填已核验的真实 C，其他字段与材料字节不变。JSON 两空格缩进、UTF-8/LF、末尾换行。

核对 private、main=B 和分支状态后，在获准分支创建草稿 PR、转 ready 并按 merge 合并；合并前核验 head=P 及完整范围，用 expected_head_sha=P 操作。读取真实 R，核验 R 与 P 树一致及同提交正文、清单和可信批准；不创建标签或 GitHub Release。实质基线、范围、字节或权限变化先停止受影响写入并查明。回执保留真实 C/P/R、PR、摘要、批准引用和未验证项，不保存私人审批原文；发布不等于业务迁移、客户端同步或运行能力部署。

## core 5.0.0 发布约定

本节仅适用于 5.0.0；以下 4.0.0 及更早契约完整保留，其中“本次”“当前”和基线只指各历史发布。此次增加总纲及任务回复必遵要求，归 MAJOR；不叠加旧版文件全摘要预批准或标签要求。

用户批准精确版本 5.0.0、core 原始字节 SHA-256 35346cdbd928263f51c73bfaf8d7140d02dccfcce224cc33026609a5be34a7c6（8029 bytes），及必要发布记录、清单和入口更新。正文不得改变，变化须重算并补批；配套摘要用于发布完整性，不声称用户逐字审核全部配套。

基线 B=5c4ccab4936eee5ea85414c91e98b604ceddb6c4。仅更新 core/PROTOCOL.md、releases/manifest.json、AGENTS.md、CLAUDE.md、README.md、CHANGELOG.md、ACCEPTANCE.md、releases/README.md、projects/rules-repository/PROJECT_SPEC.md、adapters/README.md、adapters/codex/README.md、adapters/dsh/README.md 共 12 路径；独立标准及清单、模板、模型配置和业务项目不变，不新增自动化。

沿用 4.0.0 的 C/P/R 顺序：C 包含固定材料及候选清单，version=5.0.0、status=initial-review、effective=false、approved_release=null、target_tag=null；files 按路径升序机器记录 11 个非清单材料的原始字节 SHA-256 和大小，related_standards 原样保留。核验真实 C 后，P 只转换 /status 为 approved、/effective 为 true、/approved_release 为恰含 version、protocol_sha256、approval_reference、candidate_commit、approved_on 的对象；版本和摘要复制固定值，引用及 UTC 日期来自真实批准，candidate_commit 填已核验的真实 C，其他字段与材料字节不变。JSON 两空格缩进、UTF-8/LF、末尾换行。

核对 private、main=B 和分支状态后，在获准分支创建草稿 PR、转 ready 并按 merge 合并；合并前核验 head=P 及完整范围，用 expected_head_sha=P 操作。读取真实 R，核验 R 与 P 树一致及同提交正文、清单和可信批准；不创建标签或 GitHub Release。实质基线、范围、字节或权限变化先停止受影响写入并查明。回执保留真实 C/P/R、PR、摘要、批准引用和未验证项，不保存私人审批原文；发布不等于业务迁移、客户端同步或运行能力部署。

## core 4.0.0 轻量发布约定

本节只适用于 4.0.0；以下 3.0.0 及更早段落按原文保留，只约束各自历史发布，不把八文件全摘要预批准、标签或其他旧规模套用于本次。4.0.0 的适用对象和旧合规流程改变，归 MAJOR。

用户批准精确版本 4.0.0、core 原始字节 SHA-256 069df8edfc37fefe08439b40e71bcb9250b3e775df6d477728d1e374281cfbe0（7058 bytes），及规范仓库必要清单、变更记录和入口说明的有界更新。正文不得改变；正文变化须重算并补批。根清单 files 记录配套的发布完整性，不声称用户逐字审核了每个配套文件。

基线 B=6cffa0b3b45aa870316a34dedfab4e656b604b3b。本次最多修改 core/PROTOCOL.md、releases/manifest.json、AGENTS.md、CLAUDE.md、README.md、CHANGELOG.md、ACCEPTANCE.md、releases/README.md、projects/rules-repository/PROJECT_SPEC.md、adapters/README.md、adapters/codex/README.md、adapters/dsh/README.md。不得改独立标准正文或清单、模板、模型配置和业务仓库；不新增自动化。

在获准短期分支形成候选提交 C：version=4.0.0、status=initial-review、effective=false、approved_release=null、target_tag=null；files 按路径升序记录本次所有非清单改动文件的原始字节 SHA-256 和大小，不含清单自身。related_standards 保留既有固定引用，不重新批准或升级工程 1.1.0 的 core 2.0.0 依赖。

读回 C 核验后，P 仅把根清单 /status 转为 approved、/effective 转为 true、/approved_release 转为恰含 version、protocol_sha256、approval_reference、candidate_commit、approved_on 的对象。前两项复制固定版本与正文摘要；批准引用与 UTC 日期取自真实批准，candidate_commit 只填已产生并核验的真实 C。其他字段及材料字节不变；JSON 两空格缩进、UTF-8/LF、末尾换行。仓库不保存私人批准原文。

发布前核对 private、main=B 及分支状态。按已批准范围创建 PR、审阅并合并；合并前核验 main=B、head=P、白名单差异和字节，以 expected_head_sha=P 按 merge 合并，读取真实 R 并核验 R 与 P 树一致。本次以固定 R、同提交正文与根清单、正文哈希和可信批准定位，不创建标签或 GitHub Release。基线、字节、权限或范围实质变化时先停止受影响写入并查明；不强推或重写历史。

回执记录真实 C/P/R、PR、摘要、批准引用和未验证项；核验后才报告发布完成。发布仅更新规范仓库，不证明业务项目迁移、客户端旧绑定解除或同步、goal 和自动在线能力已部署；这些实施须另有授权与实际证据。

## 历史范围说明

以下各版本原发布记录完整保留。段落中的“本次”“当前”和候选回退均只指该历史发布。

## core 3.0.0 独立发布契约

本节仅适用于本次 R014 主动进度说明的 core 3.0.0 发布；下文历史契约完整保留，不将其文件数量、标签或动作套用于本次。此次八路径范围不成为未来修订的固定要求。新义务要求有后续工作的答复主动交代预计时间和汇报节点、在明显延期时更新，旧合规做法需调整，按已批准的 core 2.0.0 兼容契约归 MAJOR。

### 范围、候选与冻结

基线 B=bfc785b7c45a11cc39cf0a6374349ca5a92ffe01。只修改 core/PROTOCOL.md、releases/manifest.json、releases/README.md、AGENTS.md、README.md、CHANGELOG.md、projects/rules-repository/PROJECT_SPEC.md、ACCEPTANCE.md。除 core 版本和 R014 补充外，不改其他通用条文；其余改动仅为本次发布的清单、导航、历史定位及验收说明。

根清单仍是所选固定快照的唯一 core 清单。候选 version=3.0.0、status=initial-review、effective=false、approved_release=null、target_tag=null。files 按路径升序记录本次七个非清单文件的 path/sha256/size_bytes；不含清单自身，不预填包含自身的未来提交或发布时点。related_standards 只定位既有工程 1.1.0 和目录 1.0.0 的固定版本，不重新批准它们，也不改变其 core 依赖。

所有七个非清单文件先冻结原始 UTF-8/LF 字节，再机器计算摘要。最终批准须覆盖完整八文件候选、这些摘要、下面唯一后生转换及有界动作。讨论方向或准备候选的许可不能代替精确材料批准。真实审批原文留在可信授权渠道，仓库仅保存适合共享的引用。

### C / P / R 与有界发布

C 为短期分支 release/core-3.0.0-proactive-updates 中的真实候选提交；P 基于 C 仅转换根清单的批准字段；R 为获准 PR 合并后 main 的真实提交。尚未产生的提交只在外置记录记 null，不填入冻结正文。最终确认可一次覆盖：指定私有仓库、短期分支、C/P、草稿 PR、转 ready、merge 合并及有界只读回执，无需重复批准未变化的同范围微步骤。

本次只用不可变发布提交 R、同提交根清单、正文原始字节哈希及可信批准回执定位，不新增标签，不创建 GitHub Release；target_tag=null 明确表示没有目标标签，不是假定标签存在。此前发布契约的标签要求继续适用于其各自历史版本，不套用于本次。这个发布方式差异须包含在最终批准中。发布前核对仓库 private、main=B、短期分支无冲突；未获得完整最终批准前，候选保留本地，main 与旧批准组合不变。

形成 C 后远端重读八文件，核验七文件原始字节与冻结材料一致且根清单仍为候选。P 的 JSON 结构差异只允许 /status 从 initial-review 变 approved、/effective 从 false 变 true、/approved_release 从 null 变为恰含 version、protocol_sha256、approval_reference、candidate_commit、approved_on 的对象。版本与正文摘要复制冻结值；批准引用及 UTC 日期取自本次真实批准；candidate_commit 必须为已产生并核验的 C。其余字段和七个材料文件字节不变。JSON 两空格缩进、UTF-8/LF、末尾换行；最终清单摘要仅记外置回执。

创建到 main 的草稿 PR；仅在批准涵盖时转 ready。合并前重核 main=B、head=P、八路径差异、原始字节及适用检查；用 expected_head_sha=P 按 merge 方式合并，读取真实 R 并核验 R 与 P 树一致。不新增或移动标签；正式发布完成以 R、同提交正文与清单、真实批准及全部本次验收核验为准。

最终回执记录真实 C/P/R、PR、原始字节摘要、批准引用、检查结果与未验证边界。若基线漂移、字节不符、权限变化、未知分支冲突或结果不确定，先只读核实并停止受影响写入，不强推、不擅自回滚、不重复已完成动作。实质范围变化补充批准；同范围恢复复用有效批准。

### 保留历史与采用边界

core 2.0.0 的正文、根清单及发布材料仍固定从 07fffb46a1946392d63614dd82e698cef8f0cec0 读取，原 core-v2.0.0 标签不动。工程 1.1.0 仍固定从 bfc785b7c45a11cc39cf0a6374349ca5a92ffe01 读取，其正文、独立清单及固定 core 2.0.0 依赖不变；目录 1.0.0 仍从 7208cef99ea7783a5b574b5f6829889795e1c03e 读取。旧 core 1.0.0 和旧工程发布记录均保留。

候选 pending 时不替代已批准 core 2.0.0；新版本发布也不自动撤销旧批准、迁移业务项目 pin、改客户端配置或启用后台监控。采用新版需要核验其真实发布快照、清单和可信批准，并按项目或会话的有效授权处理；工程依赖不因当前 core 更新而静默升级。本次仅发布文档，不证明自动通知、等待或其他运行能力已实现。

## 工程 1.1.0 独立发布契约

本节只适用于工程 1.1.0；后文 core 2.0.0 + 工程 1.0.0 的原发布流程作为历史契约完整保留，不能套用为本次动作范围。批准来自可信用户渠道，本文件和清单不自授权。

### 组件与原字节

本次只新增工程 1.1.0，不重新发布 core 或目录。core 2.0.0 正文、根清单及其中完整材料集合固定从 07fffb46a1946392d63614dd82e698cef8f0cec0 核验；目录 1.0.0 固定从 7208cef99ea7783a5b574b5f6829889795e1c03e 核验。core/PROTOCOL.md、standards/PROJECT_STRUCTURE.md、releases/manifest.json、旧工程 1.0.0 manifest、旧目录 manifest 在新快照保持原字节，旧标签不移动。新 main 同名导航和工程文件不是旧根清单材料，不声称可用旧 files 摘要核验新文件。

新工程唯一清单为 standards/releases/agent-collaboration/1.1.0/manifest.json；standard_id/version 与正文一致，候选 status=initial-review、effective=false、approval=null。document 记录工程正文原始字节；material_files 按路径升序记录本批九个非清单改动文件，每项仅 path/sha256/size_bytes。reused_supporting_files 定位未修改模板与最小示例的固定 source_commit/path/sha256/size_bytes；这些旧附属材料仅复用未变化的基础结构，相对链接按其 source_commit 解析，新模式新增字段与义务以 1.1.0 第十二、十三节为准。旧 TASK_CONTEXT 的 1.0.0 标记只说明其原始来源；新任务必须显式绑定实际采用的 1.1.0，不继承旧版本标记作为新任务适用规范。Codex 两行配置示例也只复用固定原字节，不部署。core 与目录依赖分别登记固定 commit、正文与清单路径和正文 SHA-256，不假设同一发布提交。清单不列自身或其他新清单最终哈希，不预填自身未来提交。

### C / D / R 与唯一后生转换

B=07fffb46a1946392d63614dd82e698cef8f0cec0。C 是获准远端分支中包含九个冻结文件与完整候选清单的真实提交。D 是基于 C 仅登记真实批准后生字段的提交。R 是该 PR 合并后 main 上的真实发布提交。这里 D 表示批准登记提交，不是业务任务派发提交。C/D/R 尚未产生时只记录 null，不编造 SHA。

最终批准应一次覆盖精确原字节、候选清单、下述转换、指定私有仓库/分支、草稿 PR、转 ready、merge 合并、一枚标签及有界只读回执。生成 C 后，外置交付记录绑定真实 C；D 的 JSON 结构差异只允许：

- /status：initial-review → approved。
- /effective：false → true。
- /approval：null → 对象，恰含 reference、approved_at、candidate_commit、standard_id、version、document_path、document_sha256、material_files。

reference 与 approved_at 必须来自本次真实可信批准；approved_at 为真实 UTC 时点，candidate_commit 为已产生并远端复核的 C。其余五项分别从已冻结静态标识、版本、正文路径、正文摘要与 material_files 原样复制。不得转换其他字段。JSON 为两空格缩进、UTF-8/LF、末尾换行。C→D 九个材料文件字节不变；旧清单亦不变。最终清单摘要只写外置回执，不回填自身。

### 有界发布与失败处理

发布前核对目标仓库仍 private、main=B、指定短期分支与 agent-collaboration-v1.1.0 标签无冲突，并落实获准标签创建路线。分支建议 release/agent-collaboration-1.1.0-finite-batch。只创建本节十路径的 C，读回核验；只转换上述一个清单形成 D，再核验 C..D。默认草稿 PR 到 main，批准覆盖时转 ready；合并前核对 main=B、head=D、完整文件差异和适用检查，用 expected_head_sha=D 以 merge 方式合并。读取真实 R，并验证 R 与 D 树一致。

唯一新标签 agent-collaboration-v1.1.0 必须指向核验的 R；不创建 GitHub Release，不移动旧标签，不重写冲突标签。若助手没有受支持的标签写入路线，须在最终批准前明确由用户在其已授权环境完成该一步；助手只读复核。不以 Release 代建标签，不因标签受阻擅自扩展电脑或凭据权限。标签未核验前只报告合并完成、正式发布待标签，禁止项目采用。

最终核验私有范围、B..R 十路径、九材料原始字节、最终清单、可信批准、一枚标签、五个保留文件及旧历史；只读回执登记实际 C/D/R 和最终清单摘要。任何基线漂移、字节不符、目标/权限变化、未知既有分支/标签或不确定结果，先只读查明并停止受影响写入，不强推、不自动回滚、不重复已完成动作。实质范围变化重新取得批准；确定仍属已批准范围的恢复不重复要求同一批准。

项目采用是独立内容范围，可在一次明确批准中与发布一起覆盖，但只有真实 R、正式清单、批准及标签全部核验后才能填入采用模板。采用的工程 pin 为 R；core/目录 pin 不变。批准须覆盖精确模板与仅限真实后生值的替换规则。模板未填真实值时不可提交，更不能当作有效采用。不得随采用开启 GOAL、新任务、测试或原生运行。

## 历史契约：core 2.0.0 与工程 1.0.0

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
