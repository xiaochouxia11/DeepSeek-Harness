# DeepSeek-Harness

DSH（DeepSeek Harness）相关工作的总仓库：**网页设计与开发、DSH 插件、DSH 技能**都归档在这里。

## 目录导航

| 目录 | 放什么 | 什么时候用 |
| --- | --- | --- |
| [`web/designs/`](web/designs/) | 网页设计稿、页面原型、主题与视觉规范 | 做设计、出静态稿、定风格 |
| [`web/apps/`](web/apps/) | 可运行的前端 / 网页项目 | 写真正能跑起来的页面或应用 |
| [`plugins/`](plugins/) | DSH 插件，每个插件一个目录 | 给 DSH 加能力 |
| [`skills/`](skills/) | DSH 技能，每个技能一个目录（含 `SKILL.md`） | 让 Agent 学会一套流程 |
| [`docs/`](docs/) | 约定、说明、索引 | 查规则、查入口 |

## 怎么找

- 找设计 → `web/designs/<项目名>/`
- 找网页代码 → `web/apps/<项目名>/`
- 找插件 → `plugins/<插件名>/`
- 找技能 → `skills/<技能名>/SKILL.md`

## 归档约定

完整规则见 [`docs/conventions.md`](docs/conventions.md)，四条要点：

1. **一个条目一个目录**，目录名统一 `kebab-case`（小写、连字符）。
2. **每个条目目录必须有 `README.md`**：它是做什么的、怎么用、依赖什么。
3. **新条目在下面索引表登记一行**，方便以后按「类型 / 名字 / 状态」查。
4. **不提交** `node_modules`、构建产物、`.env` 与任何 Token（见 `.gitignore`）。

## 条目索引

> 新增条目时在表尾加一行，并在 `状态` 列写清 `可用 / 草稿 / 归档`。

| 条目 | 类型 | 路径 | 说明 | 状态 |
| --- | --- | --- | --- | --- |
| _（还没有条目，从这里开始添加）_ | — | — | — | — |

## 快速约定

- 插件包名建议 `dsh-<功能>`，技能名与目录名保持一致。
- 设计稿与实现分开：稿子放 `web/designs/`，代码放 `web/apps/`；同一项目用同名目录对应。
- 一次提交只动一个条目，commit message 用 `feat(web)` / `feat(plugin)` / `feat(skill)` / `docs` 前缀。
