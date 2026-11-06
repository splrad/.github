# SPLRAD 组织公共配置

本仓库保存 [`splrad`](https://github.com/splrad) 组织公开仓库共用的拉取请求模板和仓库级说明。它不包含产品代码；公共模板递送与共享治理逻辑集中在 [`splrad/steward`](https://github.com/splrad/steward)。

## 提供的内容

```text
.
├── .github/
│   └── pull_request_template.md    组织默认拉取请求模板
├── AGENTS.md                       中央公共审查规则
├── CODE_OF_CONDUCT.md              组织公共行为准则
├── CONTRIBUTING.md                 本仓库的贡献说明
├── LICENSE                         Apache License 2.0
└── SECURITY.md                     组织默认安全报告方式
```

### 拉取请求模板

`.github/pull_request_template.md` 是创建 PR 页面使用的组织默认模板。同仓和 fork 贡献均由贡献者显式创建 PR，并直接维护正文；草稿准备好后使用原生 Ready 操作。

项目确有不同需求时，可以在项目仓库内提供自己的模板；否则应沿用这里的通用版本，避免重复维护。

### 社区文件和安全报告

`CODE_OF_CONDUCT.md` 和 `SECURITY.md` 是组织的默认社区文件。公开仓库没有同名项目文件时，GitHub 会使用本仓库的版本；`steward` 保留自己的安全报告说明，因为它的中央凭据和运行环境需要更严格的边界。

各项目的贡献流程并不相同，因此 `steward` 和 `LayerScape` 各自维护 `CONTRIBUTING.md`。本仓库的贡献说明只适用于组织公共配置。

### Copilot 代码审查说明

组织 Copilot 指令采用中央公共规则；本仓库的 `AGENTS.md` 采用同版本公共正文，仓库专属约定保留在 `CONTRIBUTING.md`。

需要调整通用规则时，应修改 `splrad/steward` 的 [公共模板](https://github.com/splrad/steward/tree/main/templates/repository)。受审模板版本通过 Copier 接入 PR 采用，保留真实 `.copier-answers.yml`；同名差异和人工内容沿原 PR 审查。

## 与 Steward 的分工

- 本仓库只保存组织公共文件，不保存 GitHub App 私钥、令牌或项目发布配置。
- Steward 负责受管文件递送和共享治理；本仓采用独立标题检查与标签入口。普通 PR 的创建、正文及议题关联由贡献者维护。
- 各产品仓库保留自己的代码、文档和确有必要的项目专用配置。

这种分工让公共模板保持简短，也避免把中央自动化复制到每个仓库。

## 修改前检查

1. 确认改动属于组织通用规则，不是某个产品的专用要求。
2. 如果文件由 Steward 生成，先修改 Steward 中的来源文件。
3. 检查模板中的受管注释标记是否完整，不要改名或删除。
4. 通过拉取请求提交，填写变更说明并查看实际验证结果。

## 许可证

本仓库使用 [Apache License 2.0](LICENSE)。
