# 学习路线总计划

> 版本 v1，2026-11-06 确认。文档名可以直接点击跳转。

总时长约 6 个月（26 周），每周 6 小时。其中每周固定 1 小时给财经英语，其余 5 小时给当周主线内容。

---

## 先说一个关键事实：PEA 不能买美股

PEA（Plan d'Épargne en Actions）是法国的税收优惠账户，**只能持有欧盟/欧洲经济区公司的股票和符合条件的基金**。苹果、英伟达这类美国个股不能放进 PEA，美股期权更不行。

但 PEA 里可以买“跟踪美国指数的合成 ETF”，比如跟踪标普500或纳斯达克100、但符合 PEA 资格的 ETF（例如 Amundi、BNP Paribas Easy 等发行的 PEA 版本）。持有满 5 年后，PEA 收益只交社会税（2026 年起为 18.6%），不交所得税，非常适合长期持有。

所以合理的账户结构是两个账户配合：

| 账户 | 用途 | 举例 |
|---|---|---|
| **PEA**（已有） | 长期核心仓位：PEA 资格的美股指数 ETF | 每月定投标普500 PEA ETF |
| **CTO**（普通证券账户，需新开） | 美国个股、美股 ETF、期权 | Interactive Brokers（盈透），或 Fortuneo 自己的 CTO |

> 想交易美股期权，基本绕不开盈透（IBKR）这类券商。Fortuneo CTO 能买美股，但期权支持有限。这一点会在阶段一详细比较。

**资金分配示例**（仅为思路，不是建议）：
- 约 12,000 欧元：PEA，指数 ETF，长期不动
- 约 6,000 欧元：CTO，美国个股和美股 ETF
- 约 2,000 欧元：期权学习资金，阶段三之后才动用

---

## 阶段一：美股基础 + 法国账户与税务（第 1–4 周）

目标：搞清楚美股和A股的区别，选好券商，把账户开起来。

| 周 | 内容 | 产出文档 |
|---|---|---|
| 1 | 美股 vs A股：交易时间（巴黎时间 15:30–22:00）、T+0、无涨跌停、盘前盘后、最小交易单位1股、碎股 | [01-us-vs-a-share.md](01-foundations/01-us-vs-a-share.md) |
| 2 | 美股市场全景：NYSE/纳斯达克、三大指数、11个行业板块（GICS）、市值分类 | [02-market-overview.md](01-foundations/02-market-overview.md) |
| 3 | 法国居民的账户体系：PEA vs CTO vs 保险账户，券商对比（IBKR / Fortuneo / Trade Republic 等），开户流程 | [03-accounts-france.md](01-foundations/03-accounts-france.md) |
| 4 | 税务：W-8BEN 与 15% 股息预扣税、法国 PFU 统一税（2026 年起 31.4%）、3916 表格申报海外账户、2074 表格申报资本利得，每项都配计算例子 | [04-tax-france.md](01-foundations/04-tax-france.md) |

**阶段检查点**：CTO 账户开通，W-8BEN 签好，能用自己的话讲清楚 PEA 和 CTO 分别放什么。

## 阶段二：券商平台操作 + 读取市场信息（第 5–10 周）

目标：熟练使用券商平台下单，能独立读懂一家公司的财报和每天的市场新闻。

| 周 | 内容 | 产出文档 |
|---|---|---|
| 5 | 券商平台上手：界面、行情、自选股、模拟盘（IBKR Paper Trading） | [01-broker-walkthrough.md](02-platform/01-broker-walkthrough.md) |
| 6 | 订单类型：市价、限价、止损、止损限价、追踪止损、GTC/DAY，每种都配下单场景 | [02-order-types.md](02-platform/02-order-types.md) |
| 7 | 换汇与成本：EUR/USD 换汇、手续费、汇率风险 | [03-fx-and-costs.md](02-platform/03-fx-and-costs.md) |
| 8 | 读财报：10-K、10-Q、财报电话会，用一家真实公司做完整拆解 | [04-reading-filings.md](02-platform/04-reading-filings.md) |
| 9 | 基本面入门：营收、利润率、自由现金流、PE/PS/EV-EBITDA 估值 | [05-fundamentals.md](02-platform/05-fundamentals.md) |
| 10 | 信息源与每日例行：财经日历、新闻网站、SEC EDGAR、筛选器；K线和技术分析入门（只学最实用的几个） | [06-information-sources.md](02-platform/06-information-sources.md) |

**阶段检查点**：模拟盘完成 20 笔不同类型订单；独立写出一份公司分析笔记。

## 阶段三：衍生品（第 11–20 周）

目标：先看懂，再在小资金上实际交易“配合正股”的期权策略。

| 周 | 内容 | 产出文档 |
|---|---|---|
| 11 | ETF 深入：指数 ETF、行业 ETF、杠杆和反向 ETF 的损耗陷阱 | [01-etf.md](03-derivatives/01-etf.md) |
| 12–13 | 期权基础：Call/Put、行权价、到期日、内在价值与时间价值、读期权链 | [02-options-basics.md](03-derivatives/02-options-basics.md) |
| 14 | 希腊字母：Delta、Gamma、Theta、Vega，用具体数字演示 | [03-greeks.md](03-derivatives/03-greeks.md) |
| 15 | 隐含波动率、财报季的波动率变化 | [04-implied-volatility.md](03-derivatives/04-implied-volatility.md) |
| 16–17 | 配合正股的策略：备兑看涨（Covered Call）、现金担保看跌（Cash-Secured Put）、轮动策略（Wheel）、保护性看跌（Protective Put） | [05-stock-plus-options.md](03-derivatives/05-stock-plus-options.md) |
| 18 | 价差策略入门：牛市看涨价差、熊市看跌价差，风险有限的玩法 | [06-spreads.md](03-derivatives/06-spreads.md) |
| 19 | 期权风险：被行权、提前行权、流动性、保证金账户 | [07-options-risks.md](03-derivatives/07-options-risks.md) |
| 20 | 了解即可：期货、窝轮/牛熊证（欧洲 Turbo）、加密 ETF | [08-other-products.md](03-derivatives/08-other-products.md) |

**阶段检查点**：模拟盘完成每种策略至少一次完整周期，之后才用真实资金做第一笔备兑看涨或现金担保看跌。

## 阶段四：建立自己的投资体系（第 21–26 周，之后长期执行）

| 周 | 内容 | 产出文档 |
|---|---|---|
| 21 | 组合构建：核心+卫星、仓位上限、再平衡 | [01-portfolio.md](04-system/01-portfolio.md) |
| 22 | 风险管理：单笔亏损上限、止损规则、期权仓位规模 | [02-risk-management.md](04-system/02-risk-management.md) |
| 23 | 交易日志模板和复盘方法 | [03-journal-template.md](04-system/03-journal-template.md) |
| 24–26 | 实战：每周写市场解读，按日志执行和复盘 | [journal](journal/index.md) |

---

## 贯穿全程：财经英语（每周 1 小时）

| 时间 | 内容 |
|---|---|
| 第 1–4 周 | 核心词汇 200 个（中英对照 + 例句），建立 `glossary/` 术语表 |
| 第 5–10 周 | 读懂新闻标题和财报摘要的句式套路，每周精读一篇 |
| 第 11–20 周 | 期权和衍生品专有词汇，读券商帮助文档 |
| 第 21 周起 | 听财报电话会、看英文财经视频，配合字幕和笔记 |

文档：[财经英语](00-english/index.md)，包括学习方法、词汇表、精读练习和推荐资源。

---

## 每份文档的统一格式

每篇文档都包含：
1. **一句话总结**
2. **和A股对比**（用你熟悉的东西帮助理解）
3. **详细讲解**
4. **具体例子**（带数字的计算或真实操作场景）
5. **常见坑**
6. **本周练习**
7. **中英术语**

## Git 提交约定

- 每篇文档单独提交，提交信息格式：`docs(阶段): 内容`，例如 `docs(foundations): add US vs A-share comparison`
- 计划调整单独提交：`plan: ...`
- 日志：`journal: week N review`
