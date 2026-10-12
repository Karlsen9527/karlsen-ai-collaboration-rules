# 协作规范入口

先按 [AGENTS.md](AGENTS.md) 判断适用范围。当前 [core/PROTOCOL.md](core/PROTOCOL.md) 6.0.0 只用于用户与谢多多的沟通和任务组织；Claude 等任务执行者默认不加载、维护 core，不承担聊天菜单，按完整任务路线、项目明确约束及环境安全权限规则执行。不要另建 Claude 专用规范。

若任务明确采用独立工程标准，按其固定快照及原依赖核验，不以当前 core 替换历史依赖。实际客户端发现入口、旧绑定解除或同步须依 [adapters/README.md](adapters/README.md) 单独验证，不能因文件已发布就宣称接入完成。Codex 偏好模板不适用于 Claude，也不改变任何权限。
