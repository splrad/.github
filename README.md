# SPLRAD 组织公共配置

本仓库保存 [`splrad`](https://github.com/splrad) 组织公开仓库共用的拉取请求模板和仓库级说明。它不包含产品代码，也不负责执行自动化；相关规则和运行逻辑集中在 [`splrad/steward`](https://github.com/splrad/steward)。

## 提供的内容

```text
.github/
├── copilot-instructions.md    Copilot 代码审查的中文输出与结论格式
└── pull_request_template.md   组织默认拉取请求模板
LICENSE                        Apache License 2.0
```

### 拉取请求模板

`.github/pull_request_template.md` 提供组织默认模板。模板为 Steward 生成的标题与正文预留了受管区域，同时保留“人工补充”位置，用来填写自动摘要没有覆盖但审查者必须知道的信息。

项目确有不同需求时，可以在项目仓库内提供自己的模板；否则应沿用这里的通用版本，避免重复维护。

### Copilot 代码审查说明

`.github/copilot-instructions.md` 规定审查主体使用简体中文，并统一阻断问题、建议问题和最终结论的格式。该文件由 Steward 的公共配置生成并同步，不是独立的规则源。

需要调整通用审查规则时，应修改 `splrad/steward` 中的 [`config/copilot/common.md`](https://github.com/splrad/steward/blob/main/config/copilot/common.md)，通过 Steward 校验后再同步到受管仓库。直接改动生成文件，后续同步时会被中央配置纠正。

## 与 Steward 的分工

- 本仓库只保存组织公共文件，不保存 GitHub App 私钥、令牌或项目发布配置。
- Steward 负责仓库接入、拉取请求处理、配置校验和 Copilot 说明同步。
- 各产品仓库保留自己的代码、文档和确有必要的项目专用配置。

这种分工让公共模板保持简短，也避免把中央自动化复制到每个仓库。

## 修改前检查

1. 确认改动属于组织通用规则，不是某个产品的专用要求。
2. 如果文件由 Steward 生成，先修改 Steward 中的来源文件。
3. 检查模板中的受管注释标记是否完整，不要改名或删除。
4. 通过拉取请求提交，以便查看 Steward 生成的摘要和验证结果。

## 许可证

本仓库使用 [Apache License 2.0](LICENSE)。
