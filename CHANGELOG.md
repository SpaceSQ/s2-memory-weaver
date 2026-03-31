# 变更日志 (Changelog) - S2 Memory Weaver

本项目的所有显著变更将记录于此文件中。
项目遵循 [Semantic Versioning](https://semver.org/) 规范。

## [1.0.2] - 2026-03-31
### 🛡️ Security & Zero-Trust Compliance
- **移除了 Prompt-Injection 风险**：彻底重写了 `skill.md`，移除了类似 `Dear Agent, you are now a "Digital Memory Therapist"` 的角色扮演强指令，将文档规范为客观的工具调用指南，防止智能体越权。
- **明确物理执行边界**：在 `README.md` 和 `handler.py` 的返回信息中，显式声明了该插件为“逻辑控制面 (Logic Plane)”，仅负责将六要素参数写入本地 SQLite 数据库。插件不包含、也不请求任何智能家居网关的凭证或网络访问权限，物理同步由外部授权下位机执行。
- **新增临床医学免责声明**：在 `README.md` 中补充了针对阿尔茨海默病记忆干预的免责条款，强调此软件为本地仿真工具，非认证医疗器械。

## [1.0.0] - 2026-03-31
### 🚀 战略重构 (Architectural Decoupling)
- **从“适老相框”到“空间大脑”**：正式将《基于真人实境的时空回溯个人拟真影像生成方法与系统》重构为 100% 跨平台的 OpenClaw 纯软件 Skill。
- 新增：渐进式进化引擎 (`upload_memory_material`)。
- 新增：物理锚定双核生成 (`generate_time_space_video`)。
- 新增：空间六要素时空同步 (`sync_historical_environment`)。