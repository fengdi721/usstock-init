# 财经英语：衍生品英语与听力

> **一句话总结**：第 11–20 周跟着期权主线学“期权英语”和“券商界面英语”，第 21–26 周练听力，从带文字稿听财报电话会，到不看文字稿也能写出 3 条要点。

本篇对应第 11–26 周，每周仍然只用 1 小时。前 10 周的方法（Anki、精读流程、AI 拆长句）继续用，见 [学习方法与每周安排](01-method.md)。

## 和A股对比：为什么这一段英语更难

A股没有场内个股期权（只有少数 ETF 期权和股指期权），所以你脑子里没有现成的中文概念可以“对号入座”。很多词连中文翻译都不统一：*strike* 有人叫“行权价”，有人叫“执行价”；*premium* 有人叫“权利金”，有人叫“期权费”。

所以这一段的原则是：**直接记英文**。券商界面、帮助文档、美国论坛、视频都用英文，中文只是帮你理解的拐杖。你在 IBKR 下单时，屏幕上写的是 *STRIKE*，不是“行权价”。

| 时间 | 主题 | 每周 1 小时怎么分 |
|---|---|---|
| 第 11–15 周 | 期权核心词汇 + 读期权链 | Anki 35 分钟 + 读一篇券商/交易所教程 25 分钟 |
| 第 16–20 周 | 策略英语 + 券商界面和风险提示 | Anki 30 分钟 + 读 IBKR 帮助文档或下单界面 30 分钟 |
| 第 21–23 周 | 听力入门：带文字稿听 | Anki 20 分钟 + 听力 40 分钟 |
| 第 24–26 周 | 听力进阶：不看文字稿听 + 做笔记 | Anki 15 分钟 + 听力 45 分钟 |

---

## 一、期权核心词汇 60 个（第 11–15 周）

和 [核心词汇 200](02-core-vocabulary.md) 一样，每周背 12 个左右，放进同一个 Anki 卡组。

### 1. 合约基本要素

| # | English | 中文 | 例句 |
|---|---|---|---|
| 1 | option | 期权 | *An option gives you the right, not the obligation, to buy or sell.* |
| 2 | call (option) | 看涨期权 | *I bought a call on Apple.* |
| 3 | put (option) | 看跌期权 | *Puts protect you if the stock falls.* |
| 4 | underlying (asset) | 标的资产 | *The underlying is SPY.* |
| 5 | strike (price) | 行权价 | *The $200 strike is the most active today.* |
| 6 | expiration (date) / expiry | 到期日 | *These options expire on Friday.* |
| 7 | premium | 权利金；期权价格 | *I paid a premium of $3.50 per share.* |
| 8 | contract | 合约 | *One contract covers 100 shares.* |
| 9 | multiplier | 合约乘数 | *The multiplier is 100, so $3.50 costs $350.* |
| 10 | exercise | 行权 | *You can exercise the call to buy shares at the strike.* |
| 11 | assignment / assigned | 被指派（被行权） | *I was assigned on my short put.* |
| 12 | holder / writer | 买方 / 卖方（开仓卖出的人） | *The writer collects the premium.* |
| 13 | American-style / European-style | 美式 / 欧式 | *US stock options are American-style.* |
| 14 | open interest (OI) | 未平仓合约数 | *Open interest at the $150 strike is 40,000.* |
| 15 | weekly / monthly (options) | 周期权 / 月期权 | *Monthly options expire on the third Friday.* |

### 2. 价值与定价

| # | English | 中文 | 例句 |
|---|---|---|---|
| 16 | in the money (ITM) | 实值 | *A $90 call is in the money when the stock is $100.* |
| 17 | at the money (ATM) | 平值 | *ATM options have the most time value.* |
| 18 | out of the money (OTM) | 虚值 | *OTM options expire worthless most of the time.* |
| 19 | intrinsic value | 内在价值 | *The call has $10 of intrinsic value.* |
| 20 | extrinsic value / time value | 时间价值 | *Time value decays as expiration approaches.* |
| 21 | expire worthless | 到期作废（价值归零） | *My puts expired worthless.* |
| 22 | breakeven | 盈亏平衡点 | *Breakeven is the strike plus the premium.* |
| 23 | implied volatility (IV) | 隐含波动率 | *IV jumps before earnings.* |
| 24 | historical / realized volatility | 历史 / 已实现波动率 | *IV is higher than realized volatility.* |
| 25 | IV rank / IV percentile | IV 排名 / 百分位 | *IV rank is 80, so options are expensive.* |
| 26 | IV crush | 波动率暴跌（财报后） | *Even though the stock rose, IV crush killed my call.* |
| 27 | Greeks | 希腊字母 | *Check the Greeks before you trade.* |
| 28 | delta | Delta（价格敏感度） | *A 0.30 delta call moves $0.30 per $1 move.* |
| 29 | gamma | Gamma（Delta 的变化速度） | *Gamma is highest near expiration.* |
| 30 | theta / time decay | Theta / 时间损耗 | *Theta is −0.05, so I lose $5 a day per contract.* |
| 31 | vega | Vega（对波动率的敏感度） | *Long options have positive vega.* |
| 32 | mark / mid (price) | 标记价 / 中间价 | *Place your limit at the mid.* |

### 3. 交易动作与策略

| # | English | 中文 | 例句 |
|---|---|---|---|
| 33 | buy to open (BTO) | 买入开仓 | *Buy to open 1 AAPL call.* |
| 34 | sell to open (STO) | 卖出开仓 | *Sell to open 1 put to collect premium.* |
| 35 | buy to close (BTC) | 买入平仓 | *Buy to close the call before earnings.* |
| 36 | sell to close (STC) | 卖出平仓 | *Sell to close at a 50% profit.* |
| 37 | long call / long put | 买入看涨 / 买入看跌 | *A long put is a bearish bet with limited risk.* |
| 38 | short call / short put | 卖出看涨 / 卖出看跌 | *A naked short call has unlimited risk.* |
| 39 | covered call | 备兑看涨 | *Selling a covered call caps your upside.* |
| 40 | cash-secured put (CSP) | 现金担保看跌 | *A cash-secured put is like a limit order that pays you.* |
| 41 | the wheel | 轮动策略 | *The wheel combines CSPs and covered calls.* |
| 42 | protective put | 保护性看跌 | *A protective put works like insurance.* |
| 43 | spread | 价差（组合） | *A spread limits both risk and reward.* |
| 44 | vertical spread | 垂直价差 | *A vertical spread uses two strikes, same expiry.* |
| 45 | bull call spread / debit spread | 牛市看涨价差 / 借方价差 | *I paid a $1.20 debit for the spread.* |
| 46 | bear put spread | 熊市看跌价差 | *A bear put spread profits if the stock drops.* |
| 47 | credit spread | 贷方价差（收钱开仓） | *I collected a $0.80 credit.* |
| 48 | leg | （组合中的）腿 | *The order has two legs.* |
| 49 | roll (out / up / down) | 移仓（展期 / 上移 / 下移） | *I rolled the call out to next month for a credit.* |
| 50 | debit / credit | 付出 / 收入（权利金） | *The roll was done for a net credit of $0.40.* |

### 4. 风险与账户

| # | English | 中文 | 例句 |
|---|---|---|---|
| 51 | naked / uncovered | 裸卖（无对冲） | *Naked calls require the highest approval level.* |
| 52 | early assignment | 提前被指派 | *Early assignment often happens before ex-dividend dates.* |
| 53 | pin risk | 到期价贴近行权价的风险 | *Close positions near the strike to avoid pin risk.* |
| 54 | max loss / max profit | 最大亏损 / 最大盈利 | *Max loss is the debit paid.* |
| 55 | margin requirement | 保证金要求 | *The margin requirement for this spread is $500.* |
| 56 | buying power | 购买力 | *Selling the put reduced my buying power by $9,500.* |
| 57 | trading permissions / options level | 交易权限 / 期权等级 | *Apply for options trading permissions in Settings.* |
| 58 | liquidity / wide market | 流动性 / 价差过大 | *Avoid options with a wide market.* |
| 59 | auto-exercise | 自动行权 | *Options $0.01 ITM are auto-exercised at expiration.* |
| 60 | Characteristics and Risks of Standardized Options | 《标准化期权的特征与风险》 | *Your broker must give you the ODD before you trade options.* |

!!! tip "缩写也要做卡片"
    美国论坛和视频里大量使用缩写：*BTO / STC / CSP / CC / IV / OI / DTE*（days to expiration，距到期天数）。正面放缩写，背面放全称 + 中文，记缩写比记全称更有用。

### 练习：读一句话说出意思

??? question "1. *I sold a 30-delta put, 45 DTE, for $2.10.*"
    我卖出了一张 Delta 约 0.30、离到期还有 45 天的看跌期权，收到权利金每股 2.10 美元（一张合约 210 美元）。

??? question "2. *The call expired worthless, so I kept the full premium.*"
    这张看涨期权到期作废了，所以我（卖方）保留了全部权利金。

??? question "3. *Rolled my covered call up and out for a small credit.*"
    把备兑看涨期权移到更高的行权价、更远的到期日，并且净收到一点权利金。

??? question "4. *IV crush after earnings wiped out my gains even though I was right on direction.*"
    财报后隐含波动率暴跌，抵消了我的盈利，尽管我方向判断对了。

??? question "5. *Got assigned early on my short call right before the ex-dividend date.*"
    在除息日前，我卖出的看涨期权被提前指派了（对方行权，为了拿股息）。

---

## 二、读懂期权链（第 12–13 周）

期权链（option chain）是你最常看的英文界面。左边是 Calls，右边是 Puts，中间是 Strike。

```
            CALLS                         |        |                 PUTS
 Bid    Ask    Last   Vol    OI    Delta  | STRIKE | Bid    Ask    Last   Vol    OI    Delta
 7.10   7.25   7.15   1,203  8,450 0.72   |  195   | 1.85   1.92   1.88   2,310  9,120 -0.28
 4.30   4.40   4.35   5,870 15,300 0.55   |  200   | 3.95   4.05   4.00   4,050 12,880 -0.45
 2.35   2.42   2.40   3,920 11,050 0.38   |  205   | 7.00   7.20   7.05     980  6,300 -0.62

 Expiration: Dec 19 '26 (43 DTE)   Underlying: 201.20   IV: 28.4%
```

| 列 | 意思 | 怎么用 |
|---|---|---|
| *Bid / Ask* | 买价 / 卖价 | 下限价单时一般挂在中间价附近（比如 200 Call 挂 4.35） |
| *Last* | 最新成交价 | 不活跃的期权 *Last* 可能是几小时前的，别信 |
| *Vol* | 今天成交量 | 越大越好成交 |
| *OI* | 未平仓合约数 | 低于几百的不要碰，流动性差 |
| *Delta* | Delta | 也可以粗略看成“到期时变成实值的概率” |
| *DTE* | 距到期天数 | 43 天 |

**算一个例子**：买 1 张 200 Call，按 4.35 成交。

- 花费：4.35 × 100 = **435 美元**（再加手续费）
- 盈亏平衡点（*breakeven*）：200 + 4.35 = **204.35**
- 最大亏损（*max loss*）：435 美元，股价到期时低于 200 就全亏
- Delta 0.55：股价涨 1 美元，这张期权大约涨 0.55 × 100 = 55 美元

---

## 三、券商界面英语（第 16–18 周）

这一节对照 IBKR（盈透）的界面。不同券商措辞略有差异，但核心词都一样。

### 1. 下单窗口（Order Ticket）

| 字段 | 意思 | 常见选项 |
|---|---|---|
| *Action* | 方向 | *BUY / SELL* |
| *Quantity* | 数量 | 股票按股，期权按张（1 张 = 100 股） |
| *Order Type* | 订单类型 | *LMT*（限价）、*MKT*（市价）、*STP*（止损）、*STP LMT*（止损限价）、*TRAIL*（追踪止损） |
| *Limit Price* | 限价 | — |
| *Aux. Price / Stop Price* | 触发价 | 止损单的触发价 |
| *Time in Force (TIF)* | 有效期 | *DAY*（当日有效）、*GTC*（撤单前有效）、*IOC*（立即成交否则取消）、*OPG*（开盘集合竞价） |
| *Outside RTH* | 允许在常规交易时间外成交 | RTH = Regular Trading Hours，勾上才能盘前盘后成交 |
| *Destination / Routing* | 路由 | 一般选 *SMART*（智能路由） |
| *Transmit / Submit* | 发送订单 | — |
| *Preview / What-If* | 预览 | 下单前看手续费和保证金影响，**每次都点** |

### 2. 账户页面（Account）

| 英文 | 中文 | 说明 |
|---|---|---|
| *Net Liquidation Value (NLV)* | 账户净清算价值 | 现在全部平仓能拿到多少钱，最重要的数字 |
| *Cash Balance / Settled Cash* | 现金 / 已结算现金 | 美股 T+1 结算 |
| *Buying Power* | 购买力 | 保证金账户里会大于现金，**不代表你应该用满** |
| *Excess Liquidity* | 剩余流动性 | 降到 0 会被强制平仓 |
| *Initial Margin / Maintenance Margin* | 初始保证金 / 维持保证金 | — |
| *Unrealized P&L / Realized P&L* | 浮动盈亏 / 已实现盈亏 | — |
| *Daily P&L* | 当日盈亏 | — |
| *Market Value* | 市值 | — |
| *Avg Price / Cost Basis* | 平均成本 | 报税时要用 |
| *Dividends / Withholding Tax* | 股息 / 预扣税 | 签了 W-8BEN 后美股股息预扣 15% |

### 3. 你一定会看到的提示和警告

这些提示出现时，**先读懂再点确认**。

| 原文 | 意思 | 该怎么办 |
|---|---|---|
| *This order may result in an immediate margin deficiency.* | 这笔订单会立刻导致保证金不足 | 不要下，减少数量 |
| *Your order is outside the price cap / exceeds the percentage constraint.* | 你的价格离市价太远 | 检查是否输错价格 |
| *The order will be held until the market opens.* | 订单会在开盘时才提交 | 正常，盘后下单会这样 |
| *You are about to sell short.* | 你将要卖空 | 如果你本意是卖掉持仓，说明数量输多了 |
| *Insufficient trading permissions.* | 交易权限不足 | 去 *Settings → Trading Permissions* 申请 |
| *Margin Call / Liquidation warning* | 追加保证金 / 强制平仓警告 | 立刻减仓或入金 |
| *Exercise / Lapse notice* | 行权 / 放弃行权通知 | 到期前处理 |
| *Corporate action: reverse split / spin-off* | 公司行动：合股 / 分拆 | 期权合约可能被调整，查 *adjusted options* |

### 4. 读帮助文档

IBKR 的帮助文档（*IBKR Knowledge Base*、*IBKR Campus*）免费、详细，是很好的阅读材料。读法和第 5–10 周的精读流程一样。

**例句拆解**：

> *If an option is in the money by $0.01 or more at expiration, it will be automatically exercised unless the account holder submits contrary instructions.*

- **主干**：it will be automatically exercised（会被自动行权）
- **If ... in the money by $0.01 or more at expiration**：如果到期时实值 0.01 美元或以上
- **unless ... submits contrary instructions**：除非账户持有人提交相反的指令
- **对你的意义**：你买的期权到期时哪怕只有一点点实值，也会被自动行权，变成 100 股股票，可能需要一大笔钱。**所以要在到期前平仓。**

!!! warning "保证金和风险条款不要靠翻译插件"
    涉及钱的条款（保证金、强平、行权），翻译插件经常翻错。比如 *close out* 是“平仓”，不是“关闭”；*liquidate* 是“强制平仓”，不是“清算公司”。遇到这类句子，用 [学习方法](01-method.md) 里的 AI 拆解提示词，并要求它“解释对我的资金有什么影响”。

---

## 四、策略英语：读美国论坛和教程（第 19–20 周）

美国散户讨论期权最集中的地方是 Reddit（r/options、r/thetagang）。帖子短、口语多、缩写多，非常适合练习。

| 口语 / 俚语 | 意思 |
|---|---|
| *theta gang* | 卖期权收时间价值的一派 |
| *tendies* | 赚的钱（戏称） |
| *bag holder* | 被套牢的人 |
| *YOLO* | 全仓押注 |
| *lotto ticket* | 很便宜的虚值期权，像买彩票 |
| *0DTE* | 当天到期的期权 |
| *diamond hands / paper hands* | 死拿不卖 / 一跌就卖 |
| *got burned* | 亏了一笔 |
| *let it ride* | 不平仓，继续持有 |

!!! info "读论坛是为了学英语，不是学策略"
    论坛里很多帖子是在炫耀高风险交易。你读它是为了熟悉说法，策略本身以本站阶段三的内容为准。

**推荐阅读材料（免费）**

| 材料 | 链接 | 用法 |
|---|---|---|
| OCC《标准化期权的特征与风险》 | <https://www.theocc.com/company-information/documents-and-archives/options-disclosure-document> | 开期权权限前必须确认读过，挑第 1–2 章精读 |
| Options Industry Council (OIC) 教程 | <https://www.optionseducation.org> | 有分级课程和视频，语速慢，带字幕 |
| Cboe Options Institute | <https://www.cboe.com/optionsinstitute/> | 交易所官方教程 |
| IBKR Campus（Traders' Academy） | <https://www.interactivebrokers.com/campus/> | 和你要用的平台完全一致 |
| Investopedia 期权词条 | <https://www.investopedia.com/options-basics-tutorial-4583012> | 遇到不懂的词就查 |
| Reddit r/options 的 FAQ | <https://www.reddit.com/r/options/wiki/faq/> | 先读 FAQ，再读帖子 |

---

## 五、听力：财报电话会（第 21–26 周）

### 为什么从财报电话会开始练听力

1. **结构固定**：每场都是“开场声明 → CEO 讲话 → CFO 讲数字 → 分析师问答”，听几场就熟了。
2. **有文字稿**：可以先看后听，再不看听。
3. **和投资直接相关**：练听力的同时你在研究一家公司。
4. **管理层发言是念稿子**：语速稳定，发音清楚，比新闻和访谈好懂得多。问答环节才是真正的挑战。

### 一场电话会的结构

| 环节 | 时长 | 谁说话 | 关键句式 | 难度 |
|---|---|---|---|---|
| 1. Operator 开场 | 1 分钟 | 会议主持 | *Good afternoon and welcome to ... All lines are in listen-only mode.* | ★☆☆ |
| 2. Safe harbor（法律声明） | 1 分钟 | IR 负责人 | *Today's discussion contains forward-looking statements...* | ★☆☆ 可跳过 |
| 3. Prepared remarks（CEO） | 5–15 分钟 | CEO | 战略、亮点、产品 | ★★☆ |
| 4. Prepared remarks（CFO） | 5–10 分钟 | CFO | 数字、利润率、指引 | ★★☆ 数字多 |
| 5. Q&A（问答） | 20–40 分钟 | 分析师 + 管理层 | *Thanks for taking my question...* | ★★★ |

### 电话会高频句式

**主持人和开场**

| 句子 | 意思 |
|---|---|
| *Please stand by, your conference will begin shortly.* | 请稍候，会议即将开始 |
| *I would now like to turn the call over to ...* | 现在把会议交给…… |
| *Our first question comes from ... with Morgan Stanley.* | 第一个问题来自摩根士丹利的…… |
| *Your line is open.* | 你可以提问了 |

**CEO / CFO 常用表达**

| 句子 | 意思 | 信号 |
|---|---|---|
| *We delivered a strong quarter.* | 我们交出了一个强劲的季度 | 正面（套话，要看数字） |
| *We're seeing strong momentum / tailwinds in ...* | 我们在……看到强劲势头 / 顺风 | 正面 |
| *We're seeing some softness in ...* | ……有些疲软 | **负面**，委婉说法 |
| *The macro environment remains challenging.* | 宏观环境仍然有挑战 | 负面，常为下调指引铺垫 |
| *We remain cautiously optimistic.* | 我们保持谨慎乐观 | 中性偏谨慎 |
| *Let me walk you through the numbers.* | 我来带大家过一下数字 | CFO 开始讲数字 |
| *On a constant-currency basis, ...* | 按固定汇率计算 | 剔除汇率影响 |
| *Sequentially, ...* | 环比 | — |
| *We're reiterating our full-year guidance.* | 我们重申全年指引 | 维持不变 |
| *We're taking a more prudent approach to our outlook.* | 我们对展望采取更审慎的态度 | **负面**，通常意味着下调 |
| *We're not going to provide guidance on that.* | 这方面我们不提供指引 | 回避 |
| *It's still early days.* | 还处在早期 | 回避具体数字 |

**分析师提问**

| 句子 | 意思 |
|---|---|
| *Thanks for taking my question(s).* | 谢谢回答我的问题（几乎每个人都这样开头） |
| *Congrats on the quarter.* | 恭喜这个季度的业绩 |
| *I wanted to ask about ...* / *Can you double-click on ...* | 我想问…… / 能不能再深入讲讲……（*double-click* 是硅谷口语） |
| *How should we think about ... going forward?* | 未来我们应该怎么看待……？ |
| *Any color on ...?* | 能不能多说点……的细节？（*color* = 细节、背景） |
| *If I could squeeze in a follow-up, ...* | 如果能再追问一个…… |

!!! tip "听力的诀窍：抓关键词，不抓每个词"
    你不需要听懂每个字。CFO 讲话时，盯住三类词就能抓住 80%：**数字**（*two point four billion*、*up eighteen percent*）、**方向词**（*increase / decline / flat / accelerate / decelerate*）、**指引词**（*raise / reiterate / lower / outlook*）。

### 听数字：最需要专门练的部分

英文大数字按“三位一组”读，中文按“四位一组”，这是中国人听数字最容易乱的地方。

| 数字 | 英文读法 | 中文 |
|---|---|---|
| 2,410,000,000 | *two point four one billion* / *two billion four hundred ten million* | 24.1 亿 |
| 610,000,000 | *six hundred ten million* | 6.1 亿 |
| 14,200,000,000 | *fourteen point two billion* | 142 亿 |
| 1.12 | *a dollar twelve* / *one dollar and twelve cents* | 1.12 美元 |
| 0.48 | *forty-eight cents* | 0.48 美元 |
| 46.2% | *forty-six point two percent* | 46.2% |
| 210 bps | *two hundred ten basis points* / *two-ten bips* | 2.1 个百分点 |
| Q3 FY26 | *third quarter of fiscal twenty-six* | 2026 财年第三季度 |
| $2.50–2.52B | *two fifty to two fifty-two billion* / *between two point five and two point five two billion* | 25.0–25.2 亿 |

**换算口诀**：

- 1 million = 100 万；10 million = 1,000 万；100 million = 1 亿
- 1 billion = 10 亿；10 billion = 100 亿；100 billion = 1,000 亿
- 1 trillion = 1 万亿

把 billion 前面的数字 × 10 就是“亿”：*4.2 billion* = 42 亿。

**练习方法**：每天花 3 分钟，打开任意一个英文数字朗读网站或让 AI 随机生成 10 个财务数字的英文读法，你听写下来再对答案。

### 三步听力法

每场电话会按这三步走，一场分两周完成。

**第一步：先读（10 分钟）**
找到文字稿（*transcript*），只读 CEO 和 CFO 的发言（prepared remarks），用 Anki 记下生词。

**第二步：带文字稿听（20 分钟）**
边听边看文字稿，用 0.75 倍速开始，跟不上就暂停。目标是“耳朵认识这些词的发音”。

**第三步：不看文字稿听（15–20 分钟）**
关掉文字稿，用 1.0 倍速听同一段，听完用中文写 3 条要点，然后打开文字稿核对。

### 去哪找录音和文字稿（免费）

| 来源 | 链接 | 说明 |
|---|---|---|
| 公司 IR 网站 | 搜索“公司名 + investor relations” | 录音（*webcast replay*）一般保留 3–12 个月，部分公司附文字稿 |
| YouTube | 搜索“公司名 + earnings call Q3 2026” | 很多有自动字幕，可以调速 |
| Motley Fool 文字稿 | <https://www.fool.com/earnings-call-transcripts/> | 免费文字稿 |
| Seeking Alpha | <https://seekingalpha.com> | 文字稿免费额度有限 |
| Yahoo Finance | 个股页面 → *Earnings* | 有时附录音链接 |

### 第 21–26 周逐周安排

| 周 | 材料 | 任务 | 完成标准 |
|---|---|---|---|
| 21 | 苹果最近一季电话会，只听 CEO 部分 | 三步听力法第一、二步 | 能跟着文字稿听完 |
| 22 | 同一场，CFO 部分 | 完整三步；数字听写 | 听写出 5 个关键数字 |
| 23 | 你持有或关注的一家公司，CEO + CFO | 完整三步 | 不看稿写出 3 条要点 |
| 24 | 同一家公司，Q&A 前 3 个问题 | 先读稿后听 | 能说出每个分析师问了什么 |
| 25 | 一场新的电话会（最好是本周刚发生的） | **直接不看稿听** prepared remarks 前 10 分钟 | 写出 3 条要点，再对照新闻报道检查 |
| 26 | 美联储主席新闻发布会前 10 分钟（*FOMC press conference*，YouTube 有） | 不看稿听 | 说出他对通胀和利率的态度：偏鹰（*hawkish*）还是偏鸽（*dovish*） |

第 26 周的检验标准（见 [财经英语首页](index.md)）：**听完一场财报电话会的前 10 分钟，能写出 3 条要点。** 做到了，你就已经超过了大多数只看中文二手信息的投资者。

### 听力材料拓展（26 周以后）

| 材料 | 难度 | 链接 | 说明 |
|---|---|---|---|
| CNBC Television YouTube 频道 | ★★☆ | <https://www.youtube.com/@CNBCtelevision> | 短视频，带字幕 |
| Bloomberg Podcasts / Odd Lots | ★★★ | <https://www.bloomberg.com/podcasts> | 深度对话，语速快 |
| NPR Planet Money | ★★☆ | <https://www.npr.org/podcasts/510289/planet-money> | 讲经济故事，发音标准，有文字稿 |
| WSJ Your Money Briefing | ★★☆ | <https://www.wsj.com/podcasts> | 10 分钟一集 |
| Fed 主席新闻发布会 | ★★☆ | <https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm> | 每次 FOMC 会后都有，带文字稿 |

---

## 常见坑

- **把 *exercise* 和 *assignment* 搞混**。买方 *exercise*（行权），卖方被 *assigned*（被指派）。你卖了期权，你是被动的那一方。
- **以为 *premium* 是“溢价”**。期权语境里 *premium* 就是期权价格，和“溢价”无关。
- **看 *Last* 下单**。不活跃期权的 *Last* 可能是很久以前的价格，要看 *Bid / Ask*。
- **忽略界面上的黄色警告**。很多新手的亏损来自一个没读懂就点了确认的弹窗。
- **听力只听不写**。不写要点就不知道自己到底听懂没有。每次听完都要写。
- **一开始就听 Q&A**。分析师口音各异、说话快、问题绕，先从念稿的 prepared remarks 开始。
- **一直开字幕**。字幕会让你“用眼睛听”。第 25 周起必须先关字幕听一遍。

## 本周练习

**第 11–15 周（期权词汇）**

- [ ] 把本篇第一节的 60 个词分 5 周导入 Anki
- [ ] 每周在 OIC 网站（optionseducation.org）读一篇入门文章，用精读流程处理
- [ ] 第 13 周：截一张真实期权链，逐列写出中文意思，并算一张合约的盈亏平衡点

**第 16–20 周（券商界面和文档）**

- [ ] 在 IBKR 模拟盘（Paper Trading）里打开下单窗口，把每个字段的意思写在笔记里
- [ ] 读 IBKR Knowledge Base 里关于“期权到期与自动行权”的文章，用 AI 拆解长句
- [ ] 读 OCC《标准化期权的特征与风险》第 1 章
- [ ] 第 20 周：在 r/options 读 5 个帖子，把看不懂的缩写和俚语做成卡片

**第 21–26 周（听力）**

- [ ] 按上面的逐周安排完成 6 次听力练习
- [ ] 每次听完写 3 条中文要点，存到 [交易日志](../journal/index.md) 的周复盘里
- [ ] 每天 3 分钟数字听写

## 中英术语

| English | 中文 |
|---|---|
| option chain | 期权链 |
| DTE (days to expiration) | 距到期天数 |
| order ticket | 下单窗口 |
| time in force (TIF) | 订单有效期 |
| regular trading hours (RTH) | 常规交易时间 |
| net liquidation value | 净清算价值 |
| paper trading | 模拟交易 |
| options disclosure document (ODD) | 期权风险披露文件 |
| prepared remarks | 管理层事先准备的发言 |
| Q&A session | 问答环节 |
| webcast replay | 网络直播回放 |
| hawkish / dovish | 鹰派 / 鸽派 |
| constant currency | 固定汇率 |
