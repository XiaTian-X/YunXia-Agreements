<p align="center">
  <img src="https://raw.githubusercontent.com/XiaTian-X/xia-logo/main/yunxia/latest/yunxia-primary-latest.svg" alt="允夏 Yǔn Xià" width="360">
</p>

<h1 align="center">允夏系列协议</h1>

<p align="center">维护协议的形成、审阅、固定版本、发布和后续修订。</p>

本仓库集中维护允夏系列协议的正文和维护事实。协议管理工具与项目采用 Skill 由独立的 [YunXia](https://github.com/XiaTian-X/YunXia) 仓库开发，两仓分别提交和推送。

## 当前协议

| 协议 | 工作正文 | 固定历史 | 正式发布 |
| --- | --- | --- | --- |
| [允夏许可证](agreements/yunxia-license/README.md) | [0.9.3 审阅草案](agreements/yunxia-license/text.txt) | 三份 imported-draft | 暂无 |

协议的显示名称与稳定 ID 分开。每个协议独立审阅、编号、推荐和发布，标签使用 `<协议ID>/v<版本>`。协议收录及技术检查不会自动形成任何项目的许可采用。

## 开始维护

从 [AGENTS.md](AGENTS.md) 和 [任务导航](docs/README.md) 进入，阅读 [系列原则](docs/principles.md) 以及协议专属设计、审阅和采用指南。工具版本由 `toolchain.lock.json` 固定；按其中完整提交读取工具维护指南并执行命令。

Agent 可以从初步目标参与立项、起草、修改、实质审阅和已授权发布。确认过的事实和授权直接复用，缺失事实集中补问；检查通过不自动构成批准或发布决定。

## 目录与历史

```text
.
├── AGENTS.md
├── repository.json             # 仓库身份与历史基线入口
├── toolchain.lock.json          # 固定维护工具提交
├── agreements/<协议ID>/        # 当前正文和相关材料
├── registry/<协议ID>/          # 固定版本与发布事实
├── provenance/                 # 拆仓来源及原始摘要
└── docs/                       # 系列原则、任务导航与来源说明
```

正文历史从 registry 固定的 Git 提交和路径读取，工作树不重复保存历版正文。`main` 从协议维护的独立起点开始；固定的 `history/pre-split` 保留拆分前真实 Git 对象，不合并进 main。完整克隆需要取得这条历史来源，浅克隆或缺对象时检查明确失败，不用当前正文代替。

[迁移清单](provenance/repository-migration.json) 记录原仓截止提交、registry 原始摘要及载荷取材。迁移保留协议正文原字节、三字段采用引用、原 Git 提交和历史草案身份，没有创建正式发布。必要历史对象是引用依赖，不额外生成备份。

本仓库可以放在工具仓库的 `repositories/YunXia-Agreements/`，由父仓整体忽略。这里有独立 `.git` 和远端，不是 submodule，也不是可清理的缓存。

## 来源与范围

本仓库自身的正式采用及完整权属仍待确认，详见 [来源与范围](docs/project-rights.md)。协议的发行、工具安装和技术检查不替代具体项目的真实采用确认。
