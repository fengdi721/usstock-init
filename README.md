# 美股ABC：从A股老手到美股专业投资者

一位法国居民的美股学习路线和笔记，从“美股小白”开始，目标是熟练使用券商平台、读懂市场信息、理解并交易美股衍生品（以期权为主，配合正股）。

在线阅读：<https://fengdi721.github.io/usstock-init/>

## 本地预览

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve          # 打开 http://127.0.0.1:8000
```

## 目录结构

```
usstock/
├── mkdocs.yml                 站点配置和导航
├── requirements.txt           构建依赖
├── .github/workflows/         推送后自动发布到 GitHub Pages
└── docs/
    ├── index.md               首页
    ├── roadmap.md             学习路线总计划
    ├── 00-english/            财经英语（贯穿全程）
    ├── 01-foundations/        阶段一：美股基础、法国账户与税务
    ├── 02-platform/           阶段二：券商平台、读取市场信息
    ├── 03-derivatives/        阶段三：ETF、期权及其他衍生品
    ├── 04-system/             阶段四：投资体系与风险管理
    ├── glossary/              中英术语表
    └── journal/               交易日志与每周复盘
```

## 发布到 GitHub Pages

1. 推送到 GitHub 的 `main` 分支。
2. 在仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
3. 之后每次推送都会自动构建并发布。

## 敏感信息检查

每次推送到 `main` 或提交 pull request 时，GitHub Actions 会先用 [gitleaks](https://github.com/gitleaks/gitleaks) 扫描**完整提交历史**。发现问题时构建和发布都会停止，网站不会更新。

扫描内容（规则在 [.gitleaks.toml](.gitleaks.toml)）：

- gitleaks 默认规则：API key、token、密码、私钥等 150 多种
- 自定义规则：IBAN 银行账号、IBKR 账号（`U` + 7–8 位数字）、法国税号（13 位）、个人邮箱、法国电话号码

文档里用作示例的 `U1234567` 已经加入白名单。如果误报了别的示例，在 `.gitleaks.toml` 对应规则的 `allowlist` 里加上即可。

本地提交前也可以先扫一遍（需要先 `brew install gitleaks`）：

```bash
gitleaks git . --config .gitleaks.toml --redact --verbose
```

**被拦下之后怎么办：**
只删掉文件里的敏感内容再提交是不够的，因为它还留在提交历史里。要用 `git filter-repo` 或 BFG 改写历史后强制推送；如果是密码或 token，**先去对应网站把它作废**。

## Git 提交约定

- `docs(阶段): 内容`，例如 `docs(foundations): add US vs A-share comparison`
- `plan: ...` 计划调整
- `journal: week N review` 每周复盘
- `chore: ...` 站点配置等杂项

## 免责声明

仅用于个人学习，不构成投资建议。税务和账户规则会变化，涉及具体金额和申报时请以官方信息或专业顾问为准。
