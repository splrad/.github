# 为 SPLRAD 组织公共配置做贡献

此仓库只存放组织级公共文件，例如默认 Pull Request 模板、组织主页和 Copilot 审查说明。产品代码、发布逻辑和仓库自动化不在这里维护。

提交改动前，先确认它确实适用于多个 SPLRAD 公开仓库。某个产品独有的规则、构建命令或用户文档，应放在对应产品仓库。

`.github/copilot-instructions.md` 由 Steward 生成和同步。需要修改其中的通用审查规则时，请先修改 [`splrad/steward`](https://github.com/splrad/steward) 中的来源配置，不要直接改生成文件。`.github/pull_request_template.md` 中的受管注释也必须保留。

提交前请检查：

- Markdown 链接、文件路径和面向贡献者的说明仍然准确；
- 改动没有包含令牌、私有路径、客户信息或本机配置；
- `git diff --check` 没有报告空白错误；
- Pull Request 说明了改动为何应成为组织默认配置。

组织成员和外部贡献者都应通过 Pull Request 提交改动。提交后请等待维护者审查和适用的自动检查，不要直接修改 `main`。
