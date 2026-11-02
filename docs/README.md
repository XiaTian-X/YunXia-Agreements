# 协议维护导航

本仓库只维护协议资料和真实维护记录。先读 [AGENTS.md](../AGENTS.md)、[系列原则](principles.md) 及目标协议的设计和审阅材料。

通用维护流程只在工具仓库保存。读取 `toolchain.lock.json` 的 `repository` 和 `commit`，从该确切提交读取 `docs/maintenance.md`；使用同一工具版本执行检查和维护，不复制另一份命令手册。工具仓库的 [项目入口](https://github.com/XiaTian-X/YunXia) 仅用于导航，不替代锁定提交。

| 任务 | 固定工具指南章节 | 本仓库中的结果 |
| --- | --- | --- |
| 从想法立项和起草 | `#create` | 协议定位、草案、设计取舍及待核项 |
| 修改正文、说明或名称 | `#edit` | 当前材料及变更影响，固定历史保持不变 |
| 实质审阅或冻结候选 | `#review` | 审阅分析、实际决定、候选登记及标签 |
| 发布到本地目录 | `#local-publication` | 核验后的本地交付回执 |
| 发布到 GitHub | `#github-publication` | 实际公开附件、回执及同步核验 |
| 修订下一版 | `#revision` | 明确基线、新目标版本及后续审阅 |
| 推荐、暂停、停止维护或撤回 | `#maintenance-state` | 实际决定和维护状态 |
| 提交和推送 | `#git` | 按阶段提交的本仓库事实 |
| 继续其他会话的任务 | `#resume` | 核对当前状态并确定下一步 |
| 处理锁或发布中断 | `#recovery` | 保留现场，核验并恢复未完成操作 |

当前协议：[允夏许可证](../agreements/yunxia-license/README.md)。工作元数据和 registry 是不同层次，工作阶段不能替代固定版本或发布结果。三份历史草案仍为 imported-draft，迁移没有补造审阅或正式发布。

[迁移清单](../provenance/repository-migration.json) 固定拆分来源和历史取材，[来源说明](provenance.json) 保留原始证据定位，[本仓库范围](project-rights.md) 说明材料与权属未知项。
