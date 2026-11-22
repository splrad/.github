# SPLRAD 组织公共配置

本仓库保存 [`splrad`](https://github.com/splrad) 组织公开仓库共用的拉取请求模板和仓库级说明。它不包含产品代码，也不负责执行自动化；相关规则和运行逻辑集中在 [`splrad/steward`](https://github.com/splrad/steward)。

## 提供的内容

```text
.
├── .github/
│   └── pull_request_template.md    组织默认拉取请求模板
├── AGENTS.md                       通过 Copier 采用的公共代码审查规则
├── CODE_OF_CONDUCT.md              组织公共行为准则
├── CONTRIBUTING.md                 本仓库的贡献说明
├── LICENSE                         Apache License 2.0
└── SECURITY.md                     组织默认安全报告方式
```

### 拉取请求模板

`.github/pull_request_template.md` 是创建 PR 页面使用的组织默认模板。普通 PR 由作者填写和维护标题、正文及补充说明，准备好后使用 GitHub 原生 **Ready for review** 操作提交审查；更新正文时应保留有效的人工补充内容。

项目确有不同需求时，可以在项目仓库内提供自己的模板；否则应沿用这里的通用版本，避免重复维护。

### 社区文件和安全报告

`CODE_OF_CONDUCT.md` 和 `SECURITY.md` 是组织的默认社区文件。公开仓库没有同名项目文件时，GitHub 会使用本仓库的版本；`steward` 保留自己的安全报告说明，因为它的中央凭据和运行环境需要更严格的边界。

各项目的贡献流程并不相同，因此 `steward` 和 `LayerScape` 各自维护 `CONTRIBUTING.md`。本仓库的贡献说明只适用于组织公共配置。

### Copilot 代码审查说明

各仓的 `AGENTS.md` 通过 Copier 采用已审的公共模板版本。调整公共代码审查规则时，请修改 Steward 的 [AGENTS.md 模板](https://github.com/splrad/steward/blob/main/templates/repository/AGENTS.md)。仓库专有的贡献约定见本仓 [CONTRIBUTING.md](CONTRIBUTING.md)。

组织 Copilot 指令和 Codex 的审查语言设置采用[中央组织稿](https://github.com/splrad/steward/blob/main/config/review/copilot-organization.md)。入口设置及模板采用步骤见[维护说明](https://github.com/splrad/steward/blob/main/config/review/README.md)。

## 修改前检查

1. 确认改动属于组织通用规则，不是某个产品的专用要求。
2. 如果文件由 Steward 生成，先修改 Steward 中的来源文件。
3. 检查模板中的填写说明、链接和原生 Ready 操作是否准确。
4. 通过拉取请求提交，说明改动及验证结果，并等待审查和适用的自动检查。

## 许可证

本仓库使用 [Apache License 2.0](LICENSE)。
