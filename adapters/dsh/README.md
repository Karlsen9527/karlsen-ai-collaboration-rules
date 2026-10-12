# DSH 有限批次适配

## 当前作用域

core 6.0.0 只用于用户与谢多多，DSH 默认不加载、维护 core，不承担聊天菜单；按完整任务路线、项目明确约束及环境安全权限规则执行。以下为明确选用工程 1.1.0 有限批次模式时才适用的历史技术说明；工程正文、独立清单及其 core 2.0.0 依赖仍按原固定快照核验，不能用当前配套说明替代原材料摘要。本次发布不启动 goal，不同步业务项目，也不承诺自动在线或回传通道已接通。

本文件是工程 1.1.0 的附属材料，无独立规范版本；仅在项目明确选用工程正文第十二、十三节时使用。共用短口令、授权、唯一领用、Q0 与证据规则全部引用中央正文，不在项目或本适配维护另一份。文档不安装插件、不启用调度器，也不证明本机加载通过。

## 固定源码依据与本机预检

参考 deepseek-ai/deepseek-harness 0.2.0-rc.2，固定提交 639ed015397290b3745d163aafe02ffee4aa3f84。实际安装版本、命令、工具、权限与公开原生状态须独立核对，差异先停止受影响步骤。用户在启动前完成项目、角色、授权及旧 goal 处理；[原生命令](https://github.com/deepseek-ai/deepseek-harness/blob/639ed015397290b3745d163aafe02ffee4aa3f84/packages/goal/command-goal/README.md) 的 `/goal <objective>` 直接创建并激活，不等待模型先做预检。若误启动，立即冻结任务写入并请求原生停止，不能谎称已暂停。

[工具契约](https://github.com/deepseek-ai/deepseek-harness/blob/639ed015397290b3745d163aafe02ffee4aa3f84/packages/goal/tool-goal/README.md) 要求 update_goal 使用 prior get_goal 返回的精确 goal_id/revision 和 action。create/edit/pause/resume 要求直接人类消息及顶层运行权限；自动 goal 回合可真实 complete/blocked。blocked 默认至少三轮，且须满足同一障碍持续存在的语义，不能空转凑次数。暂停后的恢复依用户原生控制，不得凭状态 armed/disarmed 重放许可。

## 终态前完成全部交付

自动 goal 回合成功 complete 或 blocked 后，[wrapup 源码](https://github.com/deepseek-ai/deepseek-harness/blob/639ed015397290b3745d163aafe02ffee4aa3f84/packages/goal/tool-goal/src/wrapup.ts) 要求只作最终回复，不再调用工具。因此所有获准报告、提交、推送、PR 绑定、远端核验及末次 get_goal 都在终态调用前完成。报告写 terminal_status=pending；不能预填 complete，也不能计划终态之后补报告、取时间或再 get_goal。

终态调用返回后，最终回复直接呈现该真实回执及已有交付链接；未由工具提供的时间不补造。用户随后将最终回复和可公开状态带回协调者，由获准有界收证分别判断交付、审阅和终态。用户转交不等于独立读取原生状态。终态调用失败或结果不明时按中央停手契约处理，不自动重试或另建目标。

[driver 说明](https://github.com/deepseek-ai/deepseek-harness/blob/639ed015397290b3745d163aafe02ffee4aa3f84/packages/goal/goal-round-driver/README.md) 描述同会话续行；恢复/分叉不保证重新激活，异常无自动重试保证。没有自主暂停、无人工介入或全天在线保证。两项报告、roundsStarted 与自填回合编号不能单独证明自动跨回合。
