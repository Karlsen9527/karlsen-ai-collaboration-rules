# 协作规范加载入口

本入口不复制通用规则。从可信渠道或既有批准 pin 取得选定固定提交，先检查该提交的 [releases/manifest.json](releases/manifest.json)，再读取同一提交的 [core/PROTOCOL.md](core/PROTOCOL.md)，核验标识、版本、原始字节、状态与可信批准；具体读取及历史契约见 [releases/README.md](releases/README.md)。不以 main 的文字、标签名称或本入口自行证明批准。

按明确任务范围加载当前项目 PROJECT_SPEC，不主动遍历其他 projects 目录。任务上下文与真实审批留在任务自己的授权空间。仅在项目明确采用时加载 [工程协作标准](standards/AGENT_COLLABORATION.md)、对应独立清单及配套文件；普通对话不强制工程表单。目录标准单独固定版本，不因 core 更新自动迁移。

接入能力、缓存与权限边界见 [adapters/README.md](adapters/README.md)。任何入口都不扩大上位权限或用户授权，不代表自动加载已经部署。
