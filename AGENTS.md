# 协作规范加载入口

本入口不复制通用规则。先检查同一提交的 releases/manifest.json，再读取 core/PROTOCOL.md 并核验正文哈希、版本和状态；可信批准来源须按 releases/README.md 验证。

当前 initial-review 草稿尚未生效，不得因读到本入口而宣称已批准。按明确的任务范围加载当前项目 PROJECT_SPEC，不主动遍历其他 projects 目录。个人 TASK_CONTEXT 留在任务自己的授权空间。

接入能力和缓存边界见 adapters/README.md。任何入口都不扩大上位权限或用户授权。
