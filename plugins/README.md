# plugins

DSH 插件源码，**每个插件一个目录**：`plugins/<插件名>/`。

## 一个插件目录长什么样

```text
plugins/<插件名>/
├── README.md        # 做什么、怎么装、有什么能力
├── package.json     # name 建议 dsh-<功能>
├── src/             # 源码
└── ...              # 该插件自带的资源
```

## 安装到本机 DSH

本机实际运行的 profile 是 `desktop`：

```powershell
dsh plugin --profile desktop add <npm 包名 或 本地路径>
```

装好后重启 DSH 生效；插件卡片里可单独开关。

## 注意

- 不提交 `node_modules/` 与构建产物。
- 需要密钥的插件，把 key 写进 README 说明，**不要**提交真实值。
