# skills

DSH 技能，**每个技能一个目录**：`skills/<技能名>/SKILL.md`。

## 一个技能目录长什么样

```text
skills/<技能名>/
├── SKILL.md         # 必须：frontmatter（name、description）+ 正文
└── references/      # 可选：脚本、模板、参考资料
```

`SKILL.md` 的最小格式：

```md
---
name: 技能名（kebab-case）
description: 一句话说明「什么时候用这个技能」
---

# 技能名

## 步骤
## 命令 / 模板
## 坑与验证
```

## 注意

- 目录名、`name`、索引表里的名字三者保持一致。
- 技能要能被「按描述猜用途」，description 写清触发场景。
