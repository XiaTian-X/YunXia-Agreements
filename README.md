<p align="center">
  <img src="https://raw.githubusercontent.com/XiaTian-X/xia-logo/main/yunxia/latest/yunxia-primary-latest.svg" alt="允夏 Yǔn Xià" width="360">
</p>

<h1 align="center">允夏系列协议 YǔnXià Agreements</h1>

<p align="center">维护协议的形成、审阅、固定版本、发布和后续修订。</p>

<p align="center">
  <a href="#当前协议">当前协议</a> ·
  <a href="#固定历史草案">固定历史草案</a> ·
  <a href="#开始维护">开始维护</a> ·
  <a href="#目录与历史">目录与历史</a>
</p>

本仓库集中维护允夏系列协议的正文和维护事实。协议管理工具与项目采用 Skill 由独立的 [YunXia](https://github.com/XiaTian-X/YunXia) 仓库开发，两仓分别提交和推送。

## 当前协议

| 协议 | 工作正文 | 固定历史 | 正式发布 |
| --- | --- | --- | --- |
| [允夏许可证](agreements/yunxia-license/README.md) | [0.9.3 审阅草案](agreements/yunxia-license/text.txt) | [三份 imported-draft](#固定历史草案) | 暂无 |

协议的显示名称与稳定 ID 分开。每个协议独立审阅、编号、推荐和发布，标签使用 `<协议ID>/v<版本>`。协议收录及技术检查不会自动形成任何项目的许可采用。

当前工作稿的定位、目标版本、基线和审阅状态见 [协议元数据](agreements/yunxia-license/agreement.json)。设计理由见 [设计说明](agreements/yunxia-license/design.md)，未决事项见 [审阅分析](agreements/yunxia-license/review.md)，人工采用路径见 [采用指南](agreements/yunxia-license/adoption.md)。工作正文可以继续修改，不能仅凭工作版本名称把它当作固定版本引用。

## 固定历史草案

以下版本均保留 `imported-draft` 身份，未记录正式发布。正文链接指向 registry 已绑定的完整 Git 提交；原始名称、字节和摘要保持不变。

| 固定版本 | 历史名称 | 原始正文 | 版本登记 |
| --- | --- | --- | --- |
| `0.9.2-draft.1` | 中文智能体宽松许可证 | [查看正文](https://github.com/XiaTian-X/YunXia-Agreements/blob/cc76cb61f05c48f51e22f67af3660b261d213e32/releases/yunxia-license/0.9.2-draft.1/text.txt) | [registry](registry/yunxia-license/0.9.2-draft.1.json) |
| `0.9.3-draft.1` | 中文智能体宽松许可证 | [查看正文](https://github.com/XiaTian-X/YunXia-Agreements/blob/cc76cb61f05c48f51e22f67af3660b261d213e32/releases/yunxia-license/0.9.3-draft.1/text.txt) | [registry](registry/yunxia-license/0.9.3-draft.1.json) |
| `0.9.3-draft.2` | 允夏许可证 / YunXia License | [查看正文](https://github.com/XiaTian-X/YunXia-Agreements/blob/cc76cb61f05c48f51e22f67af3660b261d213e32/releases/yunxia-license/0.9.3-draft.2/text.txt) | [registry](registry/yunxia-license/0.9.3-draft.2.json) |

在完整克隆中，可直接比较同一固定提交中的两份历史正文。例如：

```bash
git diff \
  cc76cb61f05c48f51e22f67af3660b261d213e32:releases/yunxia-license/0.9.3-draft.1/text.txt \
  cc76cb61f05c48f51e22f67af3660b261d213e32:releases/yunxia-license/0.9.3-draft.2/text.txt
```

拆仓后的日常变化可在本仓库的 [提交记录](https://github.com/XiaTian-X/YunXia-Agreements/commits/main/) 查看，固定候选或正式版本则按各自协议标签比较。当前未创建这类发布标签，不用迁移分支代替协议版本。

## 开始维护

从 [AGENTS.md](AGENTS.md) 和 [任务导航](docs/README.md) 进入，阅读 [系列原则](docs/principles.md) 以及协议专属设计、审阅和采用指南。工具版本由 [toolchain.lock.json](toolchain.lock.json) 固定；按其中完整提交读取工具的 `AGENTS.md` 和 `docs/maintenance.md`，并使用同一版本执行命令。

首次准备工具可从 [工具仓库的获取说明](https://github.com/XiaTian-X/YunXia/blob/main/docs/development.md#toolchain) 进入，实际执行版本仍以本仓库锁文件为准。固定工具可以放在本仓库忽略的 `.yunxia-tool/`；若已有工具目录，先核对 Git 根、远端、完整提交和未提交改动，不自动切换或重置父工具仓库。

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

工具仓库的 `sources.lock.json` 选择用于构建 Skill 的协议目录快照；它不等于本仓库 main 的实时状态。协议维护、Skill 适配和具体项目采用分别进行，发布或更新协议不会自动改变已经采用它的项目。

## 来源与范围

本仓库自身的正式采用及完整权属仍待确认，详见 [来源与范围](docs/project-rights.md)。协议的发行、工具安装和技术检查不替代具体项目的真实采用确认。
