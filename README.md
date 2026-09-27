# 量入为出 · budget-by-income

一个开源、公益的个人财产管理 Skill。帮中国大陆没有记账/预算/存钱习惯的人（刚毕业、月光、被生活压力逼着省钱的人），或已有储蓄但不知如何分配的人，逐步做到**量入为出**：每月花在预算内、存下钱、并为保险等打基础。

> 面向大众的通用财务教育与参考工具，**不推荐任何具体产品，不给法律/税务意见，不收集任何个人身份信息**。

---

## 它能做什么

- **教你怎么导出账单**：内置微信、支付宝账单导出的图文路径。
- **解析账单**：识别微信流水（xlsx）与支付宝回单（CSV），把每笔正确归成"消费 / 转账（逐笔问性质：房租、房贷等刚需计入消费，人情 / AA / 还钱单列非消费）/ 收入 / 中性（忽略）"，剔除退款与不计收支。
- **开销分析**：消费 vs 转账分开，按类汇总，异常账用对话澄清（不审问）。
- **生成下月预算**：按**税后总收入（含工资 / 家人支持 / 副业等）分三阶段**分配（刚需/欲望/储蓄），先储蓄后消费，比例平滑过渡、不一步到位砍掉让你快乐的花销。
- **刚需占比优化评估**：刚需偏高时，从**支出端**（房租谈价、在家做饭、改乘地铁、换套餐、债务降息、取消订阅）和**收入端**（晋升加薪、兼职、技能变现）评估降低刚需占比的可行性，按你的意愿采纳。
- **储蓄与保险预算**：保障类保险计入刚需、理财型保险计入储蓄（两条铁律）；给出保险占收入参考区间，提醒找持牌人员。
- **存量资金配置**：如果你已有储蓄但不会分配，用**标准普尔家庭资产象限**帮你把储蓄、定投、高风险投资、保险按 1234 框架分配，先守后攻（先应急金、再保障、后闲钱投资）。
- **自检对比**：把"当前花法 vs 按 Skill 花法"一年后的结果算出来，让你直观看到改变的效果。
- **月度复检 · 收入随月更新**：每月先确认收入增减，收入变动则更新预算与储蓄比例，量入为出在收入波动时也不失效。

---

## 快速开始

1. 把这个 `SKILL.md` 放进你的豆包 Skill 目录（或用任意支持 Markdown 指令的方式加载）。
2. 导出你的账单：
   - **微信**：我 → 服务 → 钱包 → 账单 → 底部「下载账单」→「用于个人对账」（Excel）。
   - **支付宝**：我的 → 账单 → 更多 → 我的客服 → 「开具交易流水证明」→ 选 Excel 个人对账、**全部交易**、打开信息展示开关。
3. 把账单文件发给我（或按引导填写数字），我会一步步带你完成摸底、分析、预算、储蓄与保险配置、自检对比。

不想上传文件也没关系：可以走**手抄模式**，按"消费/转账/收入/中性"填写关键数字即可。

---

## 输入与输出（完整流程）

### 首月（一次性建账）

**输入（你提供）**

| 输入 | 说明 |
|---|---|
| 账单文件 | 微信 xlsx / 支付宝 csv（按上文路径导出后上传） |
| 收入信息 | 摸底问答：工资 + 家人支持 / 副业 / 投资收益等多来源 |
| 全部固定开支 | 房租/房贷、伙食、交通、水电网、保障险、债务等逐项金额 |
| 确认信息 | 有无遗漏、收入是否稳定、现金支出、储蓄存量、负债 |
| 现金支出（月花 >500 时） | 是否愿意记录 |

**输出（你得到）**

| 输出 | 内容 |
|---|---|
| 个人收支画像表 | 总收入（多来源）/ 各项固定开支 / 刚需占比 / 存量 / 负债 |
| 开销分析 | 分类汇总 + 存疑账澄清 |
| 路线 + 阶段 | 路线 A/B；阶段 1/2/3 及判定依据 |
| 优化评估结论 | 支出端可省额 / 收入端可增额 / 可行性 |
| 下月预算 | 储蓄/刚需/欲望三篮子金额与比例（预算闭合验证） |
| 存量配置（路线 B） | 标准普尔 1234 分配 + 先守后攻顺序 |
| 保险预算 | 额度区间 + 优先级（不荐产品，提醒持牌人员） |
| 自检对比 | 当前 vs 改变后，一年后估算（标注非保证） |

### 每月循环（滚动）

**输入**：当月账单（可选，每周一次做周度 track）· **收入增减确认（必问）** · 现金记录（如有）

**处理**：确认收入增减 → 收入变动则更新画像表、重判阶段 → 周度 track 预算执行 → 渐进调整（储蓄比例只升不降，比例口径）

**输出**：滚动新预算 · 储蓄进度 · 调整建议

> 全程只收金额类数字与账单文件，不索取账号、密码、身份证号；账单文件仅在本次对话使用，建议阅后删除本地副本。

---

## 目录结构

```
budget-by-income/
├── SKILL.md                 # Skill 本体（流程 + 指令 + 解析规则）
├── README.md                # 本说明
├── LICENSE                  # MIT 开源许可
├── samples/
│   ├── wechat_bill_sample.xlsx   # 虚构微信账单样例（无真实数据）
│   └── alipay_bill_sample.csv    # 虚构支付宝回单样例（无真实数据）
├── demo/
│   └── fictional-walkthrough.md  # 完整虚构演示（无真实数据）
└── runs/                    # 设计推演存档
```

`samples/` 里的账单全部是**虚构数据**（示例用户），用于展示解析规则，不包含任何真实个人信息，可放心用于演示与开发。

---

## 隐私与合规

- **不收集个人身份信息**：只需金额类数字与账单文件；不需要银行账号、密码、身份证号等。
- **本地/会话内处理**：账单仅在对话中使用，不要求你上传到任何第三方。
- **不构成专业建议**：所有内容为通用教育与参考方法，非投资/保险购买建议，非法律/税务意见。储蓄率、保费占比、配置比例为行业参考区间，请结合个人实际调整。重大财务决策请咨询持牌专业人士。

---

## 开源许可（MIT）

本项目以 **MIT License** 开源，**可自由使用、修改、再分发（含商用）**，只需保留版权与许可声明。完整条款见 `LICENSE`：

```
MIT License

Copyright (c) 2026 budget-by-income contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### 发布前自查清单（每次发布 / 更新前逐项打勾）

- [ ] **个人信息扫描**：全目录（含 xlsx/csv 内部单元格）无姓名、手机号、邮箱、银行卡/身份证号、真实订单号（用关键词 + 手机号正则各扫一遍）
- [ ] **样例为虚构**：`samples/` 与 `demo/` 均为虚构数据，无真实商户名、真实账户、真实卡号
- [ ] **原始素材不打包**：含真实账单的目录（如 `wechat_bill/`、`alipay_bill/`）不得随项目发布
- [ ] **许可证齐全**：`LICENSE` 与 `README.md` 一起发布
- [ ] **免责声明可见**：明确"不构成投资 / 保险 / 法律建议"，重大决策咨询持牌专业人士
- [ ] **平台合规**：发布与运营遵守所在平台与地区的合规要求（内容社区 / 应用市场 / 电商平台规则）

## 参考来源（方法依据）

- 标准普尔家庭资产象限（要花的钱/保命的钱/生钱的钱/保本升值的钱 ≈ 10/20/30/40）
- 50/30/20 预算法（Harvard · E. Warren）与"先储蓄后消费"
- 家庭保险预算参考区间（年保费 ≈ 年收入 5%–15%，从闲钱出）
- 应急金 3–6 个月刚性支出的配置顺序原则

> 以上为行业内被广泛引用的通用方法与区间，非官方标准；使用时请结合个人情况并咨询专业人士。
