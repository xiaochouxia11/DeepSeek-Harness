# 归档与命名约定

## 1. 目录结构

```text
DeepSeek-Harness/
├── README.md            # 总索引：这里放什么、怎么找
├── docs/                # 约定与说明
├── web/
│   ├── designs/         # 网页设计稿、原型、主题、视觉规范
│   └── apps/            # 可运行的网页 / 前端应用
├── plugins/             # DSH 插件，每个插件一个目录
└── skills/              # DSH 技能，每个技能一个目录
```

新增内容时先判断属于哪一类，再放进对应目录；**不要**在根目录堆散文件。

## 2. 命名规则

| 对象 | 规则 | 示例 |
| --- | --- | --- |
| 目录 / 文件 | 小写 kebab-case | `image-relay`、`sync-openai-repos` |
| 插件包名 | `dsh-<功能>` | `dsh-image-relay` |
| 技能 | 目录名与 `SKILL.md` 的 `name` 一致 | `skills/dsh-badge/SKILL.md` |
| 设计稿版本 | `v1`、`v2`，或日期 `2026-11-08` | `web/designs/login-page/v2/` |
| 网页应用 | 与设计稿同名，放在 `apps/` | `web/apps/login-page/` |

## 3. 每个条目必须有 README

模板：

```md
# 名称

一句话说明。

## 用途
## 入口 / 结构
## 使用方式
## 依赖与限制
## 备注（可选：截图、链接、变更记录）
```

## 4. 索引表

根 `README.md` 的「条目索引」表是唯一的总入口，新增条目时同步加一行：

```md
| 名称 | 类型 | 路径 | 说明 | 状态 |
```

类型取 `网页设计` / `网页应用` / `插件` / `技能` / `文档`；状态取 `可用` / `草稿` / `归档`。

## 5. 提交规范

- 一次提交只动一个条目；跨条目改动拆开。
- commit message 前缀：`feat(web)`、`feat(plugin)`、`feat(skill)`、`docs`、`chore`。
- 分支：小改动直接 `main`；大改动用 `feat/<条目名>` 分支 + PR。

## 6. 绝对不提交

- `node_modules/`、`.pnpm-store/`、构建产物（`dist/`、`build/`、`.next/`、`out/`）
- `.env`、密钥、Token、证书
- 系统/编辑器垃圾（`.DS_Store`、`Thumbs.db`、`.idea/`）

需要放配置模板时用 `*.env.example`，值留空。
