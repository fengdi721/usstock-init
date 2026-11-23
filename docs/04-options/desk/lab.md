# 估值实验与独立交接

用 Python 3 标准库即可重跑本页。先把下面的代码复制到本地 Python 环境运行，然后把结果同课程底稿核对。函数专用于欧式、零利率、无股息的教学 Call，余日采用 ACT/365。IV 输入 0.24 表示 24%。

```python
from math import erf, exp, log, pi, sqrt

def normal_cdf(x):
    return (1 + erf(x / sqrt(2))) / 2

def call(spot, strike, days, vol):
    if spot <= 0 or strike <= 0 or days < 0 or vol < 0:
        raise ValueError("检查现货、行权价、余日和波动率")
    width = vol * sqrt(days / 365)
    if width == 0:
        return max(spot - strike, 0)
    d1 = log(spot / strike) / width + width / 2
    return spot * normal_cdf(d1) - strike * normal_cdf(d1 - width)

def implied(price, spot, strike, days):
    if days <= 0 or not max(spot - strike, 0) < price < spot:
        raise ValueError("本实验只反解严格位于无套利区间内的未到期价格")
    lo, hi = 0.0, 1.0
    while call(spot, strike, days, hi) < price:
        hi *= 2
    for _ in range(70):
        mid = (lo + hi) / 2
        if call(spot, strike, days, mid) < price:
            lo = mid
        else:
            hi = mid
    return (lo + hi) / 2

def greeks(spot, strike, days, vol):
    # 正余期、正波动率。Theta 按日，Vega 按 1 个百分点。
    t = days / 365
    width = vol * sqrt(t)
    d1 = log(spot / strike) / width + width / 2
    density = exp(-d1*d1 / 2) / sqrt(2*pi)
    return (normal_cdf(d1), density / (spot * width),
            -spot * density * vol / (2 * sqrt(t) * 365),
            spot * density * sqrt(t) / 100)

opening = call(100, 100, 30, 0.24)
print("D0 price / Delta Gamma Theta Vega", opening, greeks(100, 100, 30, 0.24))
print("Bid/Ask IV", [implied(p, 100, 100, 30) for p in (2.68, 2.80)])
for spot, vol in [(102, .27), (92, .36), (108, .18), (100, .16), (98, .26)]:
    mark = call(spot, 100, 29, vol)
    stock_pnl = -514 * (spot - 100)
    mark_change = (mark - opening) * 1000 + stock_pnl
    net_since_fill = (mark - 2.80) * 1000 + stock_pnl - 7
    print(spot, vol, *(round(x, 2) for x in (mark, mark_change, net_since_fill)))

assert abs(implied(opening, 100, 100, 30) - .24) < 1e-8
h = .01
fd_delta = (call(100+h, 100, 30, .24) - call(100-h, 100, 30, .24)) / (2*h)
assert abs(fd_delta - greeks(100, 100, 30, .24)[0]) < 1e-5
assert call(102, 100, 0, .27) == 2
```

**基准结果。** D0 价格 2.744415，Delta 0.513722，Gamma 0.057947，Theta −0.045722，Vega 0.114306。输出表后三列依次是新估值、相对 D0 模型市值的组合变化、从成交起算的累计净额。D1 的 102 / 27% 一行应分别约为 4.17、396.53、333.94 美元；第一列估值的单位是美元/股，后两列为全账美元。若所有损益都小了 100 倍，回查乘数；若 Vega 整整大了 100 倍，检查 1.00 和 1 个百分点的换算。

## 闭卷任务

同事留下同一张 D0 成交单。你接班时的新快照为 S=98，IV=26%，剩余 29 天。席位要求期末净 Delta 在 ±50 股，模型市值与可平仓估计分列。双边为 1.95 / 2.06，Bid 有 10 张，模拟可按 98 平股票。日末尚未新增成交。先独立填完交接单，再运行代码并打开参考答案。

| 提交项 | 需给出的证据 | 分值 |
|---|---|---:|
| 报价与模型 | 输入单位、合约条款、理论价、买卖盘深度、反解检查 | 20 |
| 持仓与执行 | 各腿股数、方向和现金，重算新对冲数量 | 20 |
| 损益 | 期权、股票、费用、净额，独立核对可退出价值 | 25 |
| 风险 | 写出限额偏离，给出盘中、隔夜两种处理及其代价 | 20 |
| 研究 | 指出模拟成交与真实执行的差异，设计一个可证伪的样本外实验 | 15 |

??? success "会议前的参考交接单"
    D1 Call 模型价 2.003046，落在模拟双边内。新 Delta 为 0.405544，期权合计 +405.54 股，已有对冲 −514 股，净额 **−108.46 股**。若按整数股恢复接近中性，买回 108 股，余 −406 股，净 Delta 约 −0.46 股。调整前已超过 ±50 股限额，交接单先写当前状态，再写拟调整数量。

    相对成交，期权腿 (2.003046−2.80)×1,000=−796.95，股票腿 +1,028，费用 −7，累计 **+224.05 美元**。以可成交 Bid 1.95 计，立即双腿平仓约 **+171 美元**，未扣新增平仓费。差额 53.05 来自产生估值的价格口径。独立核对用现金 48,593 加期权市值 2,003.05 减空股市值 50,372。

    若盘中能成交，买回 108 股后记录实际价格、手续费与剩余 Gamma。若临时停牌导致无法再平衡，记录超限时刻、向风险负责人报告，给出继续下跌及突然反弹的重新估值；恢复后按最新 Delta 决定数量。隔夜波动、借券和资金条件仍要写入报告。

    研究作业可选“提高对冲频率能否提高扣费后收益”。锁定一条对冲频率规则，以同一批时间序列同时计算两本自融资账；测试前固定费用、点差、流动性筛选和事件窗口，对比残余方向风险、尾部亏损及净收益。

**重做条件。** 写反对冲方向、重复扣除滑点或把卖空现金当利润，需修正账本并重跑。完成初次交接后，请另一人只改一个输入（如乘数、股息假设或报价时间）。能从报表定位变化，并说明哪一部分需要换模型，是本项目的最终验收。
