# 阶段四：期权专项训练营（第 21–32 周）

!!! abstract "阶段目标"
    从“能解释 Call / Put”进阶到“能根据方向、幅度、期限和波动率选择有限风险策略，独立下组合单、管理仓位并复盘”。熟练不等于记住所有策略，而是面对一个观点时，能说明为什么做、最多亏多少、什么情况下退出，以及为什么不交易。

本阶段承接[阶段三的期权基础](../03-derivatives/02-options-basics.md)。所有报价案例若未特别注明，都是**教学模拟报价**，不是实时行情或投资建议；每张美股标准期权按 100 股计算，佣金、税和汇率影响另算。

## 一、详细执行计划

| 周 | 主题 | 核心产出 | 过关标准 |
|---|---|---|---|
| 21 | [基础实验室](01-foundation-lab.md) | 合约卡、到期损益表、到期前情景表 | 10 分钟内读懂一条期权链并算出最大盈亏 |
| 22 | [从观点到策略](02-strategy-selection.md) | 四维观点卡、策略决策树 | 不看策略名字也能从暴露反推结构 |
| 23 | [波动率策略](03-volatility-structures.md) | 跨式、宽跨式、蝶式、铁鹰对比 | 能区分“押方向”和“押实际波动超过隐含波动” |
| 24 | [时间结构](04-time-structures.md) | 日历、对角、穷人备兑看涨案例 | 能说明期限结构、短腿指派和 Vega 风险 |
| 25 | [合成头寸与等价关系](05-synthetics.md) | Put-Call Parity 检查表 | 能识别 covered call 与 short put 的相似风险 |
| 26 | [开仓、调仓与退出](06-position-management.md) | 开仓单、退出树、滚动记录 | 每次调整都能与“直接平仓”比较，而非机械滚动 |
| 27 | [事件、行权与到期周](07-events-expiration.md) | 财报、除息、到期周 SOP | 到期前不留下自己解释不了的交割风险 |
| 28 | [组合 Greeks 与仓位](08-portfolio-risk.md) | 组合风险表、压力测试 | 能把每张合约换算成账户层面的美元风险 |
| 29 | [策略案例册](09-casebook.md) | 6 个完整案例，含失败剧本 | 能在看答案前写出选择、拒绝和退出理由 |
| 30 | [个人策略手册](10-playbook.md) | 允许清单、禁做清单、模板 | 形成可执行、可审计的个人规则 |
| 31 | 模拟盘盲测 | 3 个未知情景，先计划后下单 | 无裸卖；实际成交偏差和风险均有记录 |
| 32 | [毕业考核](11-graduation.md) | 笔试、情景题、20 笔样本复盘 | 达到准入阈值后，才考虑最小规模实盘 |

建议每周 6 小时：2 小时读教程，1 小时手算，2 小时模拟盘，1 小时复盘。若某周未过关，重复训练，不按日历强行升级。

## 二、内容范围

本阶段会熟练使用的**有限风险**策略：

- Long Call / Long Put、Protective Put、Collar；
- Covered Call、Cash-Secured Put、Wheel（仅在真愿意持股时）；
- Bull Call、Bear Put、Bull Put、Bear Call 四类垂直价差；
- Long Straddle / Strangle、Long Butterfly、Iron Condor；
- Calendar、Diagonal、Poor Man's Covered Call；
- 合成股票与 Put-Call Parity（用于理解和检查，不鼓励加杠杆）。

只学习风险、不纳入新手实盘清单：裸卖 Call/Put、裸跨式/宽跨式、Ratio Spread、0DTE 高频交易、复杂未定义风险组合。

## 三、四道升级门

1. **知识门**：最大盈利、最大亏损、盈亏平衡点和 Greeks 符号全部算对。
2. **执行门**：组合单一次提交；会用限价单；知道如何整体平仓；不 leg in。
3. **风控门**：最坏情景不超过预设风险预算；事件和到期处理写在开仓前。
4. **行为门**：至少 20 笔模拟交易，按规则执行率 ≥ 90%，没有为了“回本”扩大风险。

通过前三道门，只代表可以继续模拟。四道门全部通过，也不代表必须实盘。

## 四、贯穿全阶段的统一案例

为方便横向比较，前八章统一使用虚构标的 **ABC**：现价 `$100`，无即将除息，期权流动性良好。30 天平值 IV 为 30%。具体期权权利金是教学模拟值，每章会注明 DTE、行权价和净借记/贷记。

统一风险预算示例：账户净值 `$20,000`，单笔**计划最大亏损**不超过 `$200`（1%）。这意味着：

- 可以考虑最大亏损 `$180` 的借方价差；
- 不能因为券商只占用 `$150` 保证金，就接受最大亏损 `$350` 的结构；
- 一张 `$95` 现金担保 Put 需要预留 `$9,500`，它不是“小仓位收租”。

## 五、官方参考资料

- [OCC：标准化期权特征与风险披露文件](https://www.theocc.com/company-information/documents-and-archives/options-disclosure-document)
- [SEC Investor.gov：期权入门与风险](https://www.investor.gov/introduction-investing/general-resources/news-alerts/alerts-bulletins-63)
- [Options Industry Council：策略库](https://www.optionseducation.org/strategies/all-strategies-en)
- [Cboe：期权策略基准指数](https://www.cboe.com/us/index_income/help/)

!!! danger "先读风险披露"
    期权买方可能损失全部权利金；某些卖方头寸可能损失超过最初收到的权利金，裸卖 Call 的潜在亏损没有上限。券商批准权限不等于策略适合你。
