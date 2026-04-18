# `manuscript.md` 学术论文理论与机制审计报告

> 审计范围：**仅基于 `manuscript.md`** 进行评审，**未查看其他文件**。
>
> 说明：文稿中多处依赖 Figure S1–S4、补充公式、参考文献精确表述与图件本身，因此以下结论中凡涉及这些缺失材料的地方，均明确标记为**“当前审计受限”**。

---

## 第一阶段：范围确认与输入检查

### 1. 论文声称的核心贡献

论文主要声称：

1. Tibetan Plateau（TP）地形强迫可在 JJA 显著激发 Southern Hemisphere（SH）的准定常 ZW3。
2. 该跨半球遥相关通过一个 **“TP–Indian Ocean–Deep Convection–ZW3”** 路径实现。
3. 关键桥梁是一个由 TP 塑造的 **“negative IOD-like”** 印度洋偶极型 SST 异常。
4. ZW3 的维持主要依赖 **vertical baroclinic conversion**，并与深对流/潜热释放有关。

### 2. 论文声称的主机制链条

作者的主链条可概括为：

**TP 地形改变**  
→ 改变印度洋风场/索马里急流  
→ 形成西冷东暖的 “negative IOD-like” SST dipole  
→ 改变深对流与上对流层散度  
→ 散度偶极通过涡度伸长激发 Rossby wave source  
→ 波列向东南/跨半球传播并进入 SH westerly waveguide  
→ 通过 vertical baroclinic energy conversion 维持深厚准定常 ZW3

### 3. 涉及的物理体制

- 大气：**热带–副热带–南半球中高纬遥相关**
- 波动：作者明确按 **quasi-stationary / stationary Rossby wave** 解释
- 动力/热力：**湿动力 + 深对流 + 局地能量学**
- 耦合类型：**全耦合 CESM2 地形敏感性试验**
- 因果类型：**敏感性实验建立“TP 有/无”的净效应**，这一点成立；但**链条中各中间环节**仍需额外诊断支撑

### 4. 最可能藏“拒稿级硬伤”的章节

1. **3.2.2 Physical Mechanism Diagnosis**  
   尤其是对 WAF、Rossby wave source、能量学项物理意义的解释。  
   位置：`manuscript.md:86-104`
2. **4.3 Air-Sea Coupling Response and Excitation of the Rossby Wave Source**  
   把散度偶极直接写成 Rossby wave source。  
   位置：`manuscript.md:148-164`
3. **4.4 Propagation Path and Energetic Maintenance of the ZW3**  
   波传播、再激发、跨赤道、vertical baroclinic conversion 的解释。  
   位置：`manuscript.md:166-186`
4. **Abstract / Conclusions / Key Points**  
   用词明显强于证据。  
   位置：`manuscript.md:8-16`, `manuscript.md:192-206`

### 5. 当前缺哪些材料会影响判断

缺失材料包括：

- 补充材料 Figure S1–S4
- 公式 (1)–(9) 的实际写法
- 参考文献正文
- 图 1–10 本身

因此必须明确标记：

> **当前审计受限，方法解释存在审查盲区。**

特别是：

- 无法核对 Equation 7/8/9 的具体定义与符号；
- 无法确认是否真的计算了 RWS；
- 无法确认 WAF 是否在东风区做了 mask；
- 无法确认能量项的数学定义是否与文字解释一致；
- 无法验证 Figure S4 是否真能支持 “independent of ENSO”。

### 6. 实验设计类型及其建立的因果关系

实验类型：**全耦合地形敏感性实验（CTRL vs SENS）**

该设计已经建立的因果关系：

- **TP 有无变化对系统均值态响应的净因果效应**

仍需额外验证的内容：

- “印度洋 SST 是桥梁”的链条是否充分建立；
- 深对流是否是必要中介；
- 200 hPa 散度是否真构成 **Rossby wave source**；
- 波是否真按作者所说路径传播；
- “维持机制”是否真由 `CP_vert` 主导。

---

## 第二阶段：Claim Inventory（主张清单）

以下仅抽取**非平凡主张**，并将复合主张拆分。

### A. 描述性主张

1. TP 强迫在 JJA 激发显著 ZW3 形态。  
   位置：`manuscript.md:114-123`
2. JJA 响应具有 deep equivalent barotropic structure。  
   位置：`manuscript.md:116-117`
3. 印度洋存在西冷东暖的 SST dipole。  
   位置：`manuscript.md:128-146`
4. 东印度洋深对流增强，西印度洋对流减弱。  
   位置：`manuscript.md:152-158`
5. 200 hPa 存在东散西合的散度结构。  
   位置：`manuscript.md:160-164`
6. SH 中高纬存在类似 ZW3 的波列。  
   位置：`manuscript.md:168-186`

### B. 机制性主张

7. TP 通过增强 Somali Jet 造成西印度洋冷 SST。  
   位置：`manuscript.md:132-140`
8. 东印度洋暖 SST 由 MAM 热惯性维持到 JJA。  
   位置：`manuscript.md:144-146`
9. SST dipole 驱动深层 zonal overturning circulation。  
   位置：`manuscript.md:150-156`
10. 上层散度偶极通过 vorticity stretching 激发 Rossby wave source。  
    位置：`manuscript.md:156-164`
11. 强化的 subtropical westerly jet 充当 waveguide，引导波列入 SH 高纬。  
    位置：`manuscript.md:160-164`
12. 波列在热带南印度洋被“re-excited”。  
    位置：`manuscript.md:168-186`
13. 波列通过 transient eddy feedback / local baroclinic instability 获得中继补能。  
    位置：`manuscript.md:182-186`
14. ZW3 主要通过 vertical baroclinic conversion 维持。  
    位置：`manuscript.md:174-186`

### C. 诊断性主张

15. WAF 诊断了波能传播方向。  
    位置：`manuscript.md:86-91`, `manuscript.md:168-172`
16. 散度 + divergent wind 图证明存在波源。  
    位置：`manuscript.md:160-164`
17. `CP_vert` 可作为 diabatic heating 驱动 KE generation 的 proxy。  
    位置：`manuscript.md:102-104`
18. 固定 CTRL background flow 可以“纯粹反映 TP forcing 的直接贡献”。  
    位置：`manuscript.md:90-91`, `manuscript.md:104`

### D. 能量学主张

19. `CP` 主导 ZW3 维持。  
    位置：`manuscript.md:174-176`
20. `CP_vert` 不仅是 APE→KE 的绝热内部转换，还代表 latent heating 的直接能量注入。  
    位置：`manuscript.md:176`, `manuscript.md:198`
21. 波在传播过程中不断从背景 available potential energy 中获能。  
    位置：`manuscript.md:174-186`

### E. 传播主张

22. 波列从热带印度洋向东南传播入 SH westerly waveguide。  
    位置：`manuscript.md:16`, `manuscript.md:160-164`, `manuscript.md:168-172`
23. 波活动可跨赤道。  
    位置：`manuscript.md:168-170`, `manuscript.md:197-198`
24. 波列在热带印度洋附近被再激发。  
    位置：`manuscript.md:168-170`, `manuscript.md:182-183`

#### 这些传播主张隐含的物理前提

- 定常/准定常 Rossby 波沿路径处需有**合适的西风背景流**；
- WAF/T-N flux 在所用区域内必须**物理有效**；
- 若跨越东风区，必须解释**如何跨越 “easterly barrier”**；
- “re-excited” 需要独立诊断局地产波/局地能量源，而不是仅凭箭头变大。

### F. 物理约束主张

25. 热带印度洋存在足以支持 stationary wave propagation 的 westerly window。  
    位置：`manuscript.md:197`
26. 增强的 subtropical westerlies 足以形成波导。  
    位置：`manuscript.md:160-164`
27. `CP_vert` 的正值可支持“maintenance”。  
    位置：`manuscript.md:176-186`

### G. 术语/命名主张

28. `negative IOD-like`  
    位置：`manuscript.md:16`, `128`, `146`, `196`
29. `acts as a Rossby wave source`  
    位置：`manuscript.md:16`, `160`, `197`
30. `proxy for diabatic heating`  
    位置：`manuscript.md:102-104`
31. `maintained by vertical baroclinic energy conversion`  
    位置：`manuscript.md:12`, `16`, `176`, `198`
32. `robust`  
    位置：`manuscript.md:16`, `122`, `192`

### H. 稳健性主张

33. 结果是 significant / robust。  
    位置：`manuscript.md:16`, `120-123`, `192`
34. 与 ENSO 无关。  
    位置：`manuscript.md:204`
35. 该机制具有一定普适性/可推广性。  
    位置：`manuscript.md:16`, `202-206`

---

## 第三阶段：物理约束审计

### 3.1 核心问题一：定常波传播路径是否满足西风背景约束？

作者一方面承认 **equatorial easterly barrier** 会阻碍跨赤道传播：

- `manuscript.md:28-29`
- `manuscript.md:198`

但另一方面又声称：

- 波源从 western tropical Indian Ocean 的 **westerly window** 跨赤道传播。  
  位置：`manuscript.md:197`
- WAF 显示从 NH 到 SH 高纬存在传播通道。  
  位置：`manuscript.md:168-170`

#### 审计结论

**当前没有看到足够证据证明核心传播路径全程满足 stationary/quasi-stationary Rossby wave 传播条件。**

这是本稿最危险的问题之一。

#### 为什么危险

这相当于说“火车沿铁轨跑到了终点”，但文中没有先证明**中间真的有连续铁轨**。如果路径中间穿过的是东风区，那么对**定常 Rossby 波**来说，那里不是轨道，而是“断桥”。

#### 具体缺口

主文未展示：

- 沿传播路径的**背景纬向风绝对值/符号**；
- 哪些区域是 **easterly / westerly**；
- WAF 是否在**东风区做了 mask**；
- stationary wavenumber / waveguide 诊断。

#### 初步判级

**Reject-level blocker 候选**

因为一旦核心传播通道不成立，整条 “cross-hemispheric wave propagation” 叙事会塌。

### 3.2 核心问题二：T-N stationary WAF 在关键区域是否物理有效？

作者使用 Takaya & Nakamura (2001) stationary wave activity flux：

- `manuscript.md:86-91`

并将其用于：

- 热带印度洋；
- 跨赤道；
- “re-excited over the tropical southern Indian Ocean”；
- “merges into SH westerly waveguide”。

#### 审计结论

**若关键区域包含东风背景流，则该诊断量在那里物理意义不足或无效。**

文中没有说明是否对无效区域做 mask，因此**方法论和物理约束同时存在风险**。

#### 为什么这是硬伤

这像拿一个“只适用于高速公路的测速仪”去测船在河里的速度。不是“测得不准”那么简单，而是**这个量在那个场景里就不该被拿来支撑论证**。

#### 初步判级

**Reject-level blocker 候选**

### 3.3 核心问题三：所谓 “maintenance” 是否展示了净能量维持条件？

作者多次声称：

- ZW3 被 `CP_vert` 维持。  
  位置：`manuscript.md:12`, `16`, `176`, `186`, `198`
- “continuously offsetting frictional dissipation”。  
  位置：`manuscript.md:174`
- “maintaining quasi-stationary amplitude”。  
  位置：`manuscript.md:186`

#### 审计结论

文中只描述了**局地能量转换分布**，但没有看到：

- 沿波列路径的**空间积分**；
- 与耗散项的比较；
- 净正收支闭合。

因此 “maintenance” 这个词目前**证据门槛未满足**。

#### 为什么这是硬伤

只看到几个地方在“赚钱”，不等于公司整体盈利。如果不把全账本合起来看，你不能说“系统被维持住了”。

#### 初步判级

**Major → 若维持是核心卖点，可升为 Reject-level**

---

## 第四阶段：方程与守恒量审计

### 4.1 最大硬伤：把 `CP_vert` 写成 diabatic heating proxy

作者明确写道：

- `CP_vert` 描述 perturbation vertical heat fluxes 将 APE 转成 KE。  
  位置：`manuscript.md:100-103`
- 但紧接着又说它 “serves as a key proxy variable for kinetic energy generation driven by diabatic heating”。  
  位置：`manuscript.md:102-103`
- 后文多次把它写成 latent heat release 的直接能量注入。  
  位置：`manuscript.md:176`, `198`, `204`

#### 审计结论

这是全文最明确、最严重的理论错误之一。

#### (a) 问题出在哪？

`CP_vert`（本质上是 `ω'T'` 型绝热斜压转换项）描述的是**涡动 APE 与涡动 KE 之间的内部转换**。它**不是**非绝热加热 `Q'` 的 proxy，更不是“latent heating 直接注入 KE”的严格诊断。

#### (b) 为什么这是错的？

因为这相当于把“账户内部转账”误当成“外部打款”。

- `Q'T'` 更像“外部收入进账”；
- `CP_vert` 更像“你把储蓄账户的钱转到活期账户”。

两者都能让活期账户余额变大，但**来源完全不同**。把内部转账写成外部收入，是**账目性质错误**，不是措辞问题。

在涡动总能量预算中，`CP_vert` 是**内部转换项**，不是净外源。若要诊断 diabatic heating，应看与**非绝热加热率 `Q`** 相关的项，而不是把 `ω'T'` 直接当 proxy。

#### (c) 具体怎么改？

1. 删除/重写以下所有表述：
   - `manuscript.md:102-104`
   - `manuscript.md:176`
   - `manuscript.md:198`
   - `manuscript.md:204`
2. 把相关句子降级为：
   - `CP_vert` indicates conversion from eddy APE to eddy KE
   - 其增强 **may be dynamically consistent with** deep convection, but **does not directly diagnose diabatic heating**
3. 若想证明 latent heating 贡献，需新增：
   - 非绝热加热率 `Q`
   - `Q'T'` 或等价热源项诊断
   - 若模式变量有限，至少给出列积分 diabatic heating / apparent heat source / moist static energy budget 的独立证据
4. 在总能量预算里明确说明：
   - 哪些项是背景→扰动；
   - 哪些项是扰动库之间内部转换；
   - 哪些项在 total eddy energy budget 中抵消。

#### 判级

**Reject-level blocker**

### 4.2 第二个硬伤：混淆“从背景获能”和“内部库之间转换”

作者写道：

- 波列“extracts available potential energy from the background flow primarily through vertical baroclinic energy conversion”。  
  位置：`manuscript.md:16`
- “continuously extracting available potential energy from deep vertical heat flux release”。  
  位置：`manuscript.md:186`
- “vertical baroclinic energy conversion dominates energy generation”。  
  位置：`manuscript.md:182`

#### 审计结论

这里存在明显的**能量库拓扑混淆**。

#### 为什么错

若 `CP_vert` 是 eddy APE → eddy KE，那么它不是“从背景场直接取能”的箭头。真正“背景 APE → 涡动 APE”的是水平斜压转换类项，而不是垂直内部转换项本身。

作者现在的写法，相当于把：

- A → B
- B → C

其中第二段箭头 B→C，误写成了 A→C 的直接供能。

#### 比喻

你先从银行取钱到微信零钱，再从微信零钱转到银行卡。第二步不是“银行继续给你钱”，只是账户内再分配。

#### 怎么改

- 必须在文中明确拆分：
  - 背景 APE → 涡动 APE
  - 涡动 APE → 涡动 KE (`CP_vert`)
- 禁止把 `CP_vert` 单独写成“background energy extraction”的主项
- 如果要讲“总能量来源”，需展示完整 eddy energy budget

#### 判级

**Reject-level blocker**

### 4.3 第三个问题：把散度偶极直接写成 Rossby wave source

作者写：

- 上层散度偶极 “acts as a Rossby wave source”。  
  位置：`manuscript.md:16`, `160-164`, `197`

#### 审计结论

从目前主文看，作者似乎**没有正式计算 Sardeshmukh & Hoskins (1988) 的 RWS**，而是用散度与 divergent wind 直接替代。

#### 为什么这不够

散度场可以是 RWS 形成条件的一部分，但**不是 RWS 本身**。真正的 Rossby wave source 涉及背景绝对涡度及其梯度、散度、涡度平流等组合项。若没算 source，却写 “acts as a Rossby wave source”，就是把“有点像起火条件”写成“已经证明着火点”。

#### 怎么改

- 若未正式计算 RWS，术语必须降级：
  - `provides conditions favorable for Rossby wave generation`
  - `is dynamically consistent with a Rossby-wave-source region`
- 若要保留原说法，必须补算 RWS

#### 判级

**Major，若它是中心机制核心证据则可升为 Reject-level**

### 4.4 第四个问题：固定 background flow 的解释过强

作者多次说：

- 用 CTRL 的 zonal mean flow / shear / temperature gradient 固定背景，可 “strictly isolate direct contribution”。  
  位置：`manuscript.md:90-91`, `104`

#### 审计结论

这种说法过强。

#### 为什么

固定背景场确实有助于比较，但它并不意味着“纯粹只剩 direct contribution”。因为 TP 强迫本来就可能通过**改变背景流本身**来影响传播和能量转换。你把背景冻结后，得到的是“在共同背景上比较扰动项”的结果，不是“现实中唯一真实路径”。

#### 怎么改

把 `purely reflect direct contribution / strictly isolate` 改为：

- `facilitates controlled comparison`
- `reduces contamination from background-state differences`

而不是宣称完全剥离背景流影响。

#### 判级

**Major**

---

## 第五阶段：方法论审计

### 5a. 空间/时间域污染检查

#### 问题 1：JJA minus annual mean 的物理解释薄弱

作者为强调 JJA 特异性，使用了：

- JJA SST difference 减 annual mean difference。  
  位置：`manuscript.md:128-130`

#### 审计结论

这个操作**不是必然错误**，但目前物理解释不够严谨。

#### 风险

这可能把：

- 常年背景差异；
- 季节性响应；
- 其他季节残留信号；

混合在一起。若要把它解释为 “JJA 特异 forced mode”，需要更清楚说明为什么这个操作对应你要的物理对象。

#### 判级

**Minor–Major 之间，偏 Major if heavily relied upon**

#### 问题 2：meridional mean 25°N–25°S 可能混入不同过程

作者把 25°N–25°S 做经向平均展示 divergence / omega 的经向平均纵向剖面：

- `manuscript.md:154-158`

#### 审计结论

这个平均域很宽，可能把：

- 北半球季风相关响应；
- 赤道耦合响应；
- 南半球热带响应；

混在一起。

#### 为什么危险

你想证明一个“Indian Ocean zonal overturning”，但平均域过宽可能混入并非同一物理过程的信号。像是想量一个人的体温，却把隔壁病房也平均进来。

#### 怎么改

- 对关键剖面做更聚焦的纬带敏感性检验，例如：
  - `10°S–10°N`
  - `15°S–5°N`
  - `5°N–20°N`
- 证明核心结论对平均域选择不敏感

#### 判级

**Major**

### 5b. 诊断适用性检查

#### 问题 3：WAF 在关键区域的适用性未说明

这与第三阶段相互印证。若作者的关键论证区域包含东风带而未 mask，则这是**方法论污染 + 物理约束违反**的双重问题。

#### 判级

**Reject-level blocker 候选**

### 5c. 统计方法检查

#### 问题 4：二维场显著性未见多重比较控制

作者对空间场使用 t-test：

- `manuscript.md:106-108`

但未见：

- FDR；
- field significance；
- 有效自由度修正；
- 自相关说明。

#### 审计结论

对于大面积空间场，只做逐点 t-test 容易把噪声误识为“大片显著”。

#### 判级

**Major**

#### 问题 5：100 个年样本独立性假设偏强

作者写：

- seasonal means → independent interannual time series with sample size 100。  
  位置：`manuscript.md:108`

#### 审计结论

“100 个季平均样本独立”是一个需要检验而不是直接宣告的前提。尤其在全耦合系统中，低频模态（IPO/AMO-like variability）可显著降低有效自由度。

#### 判级

**Major**

---

## 第六阶段：机制证伪矩阵

### 机制 1：TP → Indian Ocean SST dipole

- 已有证据：CTRL-SENS SST、风应力、热通量、advection 叙述
- 已由实验设计建立：TP 对系统响应的净效应
- 缺口：
  - 东部暖异常依赖补充图 S3，不在主文证据链中闭合；
  - `negative IOD-like` 命名门槛偏高。

#### 最强可保留表述

`TP forcing is associated with a zonal SST dipole in the tropical Indian Ocean.`

### 机制 2：SST dipole → convection dipole → upper divergence dipole

- 证据：OLR / PRECT / `ω` / divergence 共位相
- 评价：**大体成立，且在全耦合敏感性框架下合理**
- 缺口：
  - 宽平均域可能污染；
  - 未显示更直接的 diabatic heating 诊断。

#### 最强可保留表述

`The SST dipole is dynamically consistent with a zonally asymmetric deep-convection response.`

### 机制 3：upper divergence dipole → Rossby wave source

- 必要诊断：RWS 正式计算
- 当前是否算了：从主文看**没有明确算**
- 替代解释：只是散度与背景流叠加出的有利条件，不足以单独证明 source

#### 最强可保留表述

`The upper-level divergence pattern provides dynamically favorable conditions for Rossby wave generation.`

#### 判级

**Major / Reject-level 边缘**

### 机制 4：wave propagates across hemispheres into SH waveguide

- 必要诊断：
  - 背景西风条件；
  - WAF 有效区 mask；
  - 最好有 stationary wavenumber / waveguide 诊断
- 当前是否算了：主文没见
- 替代解释：
  - 并非连续跨赤道传播，而是热带响应 + SH 局地再响应/局地激发

#### 最强可保留表述

`The circulation anomalies suggest a cross-hemispheric linkage, potentially involving SH-side wave amplification downstream of the tropical Indian Ocean response.`

#### 判级

**Reject-level blocker**

### 机制 5：vertical baroclinic conversion maintains ZW3

- 必要诊断：
  - 完整 eddy energy budget；
  - 区分背景 APE→eddy APE 与 eddy APE→eddy KE；
  - 净收支 / 空间积分 / 耗散对比；
  - 若涉及加热，需 `Q` 相关诊断
- 当前是否算了：从主文看**没有**
- 替代解释：
  - 仅是内部能量转换增强，与深对流协变，但不是直接热源证明

#### 最强可保留表述

`Enhanced vertical baroclinic conversion is collocated with the wave response and may contribute to local eddy-energy redistribution.`

#### 判级

**Reject-level blocker**

---

## 第七阶段：引用语义检查

由于未查看参考文献正文，这里只能做**语义风险审计**。

### 1. Sardeshmukh & Hoskins (1988)

作者借用了 RWS 框架，但主文只展示散度/散度风：

- `manuscript.md:160`

#### 风险

**引用该框架 ≠ 已完成该框架要求的诊断。**

如果没算 RWS，只能说“与该框架一致”，不能说“证明了 Rossby wave source”。

### 2. Chang et al. (2002)

作者引用它支持：

- `CP_vert` 是 diabatic heating / latent heat direct injection proxy。  
  位置：`manuscript.md:102-103`, `176`

#### 风险

极可能**超出了原文能支持的精确命题**。即使文献讨论 latent heating 对波活动的重要性，也不等于 `ω'T'` 可被直接当成 diabatic heating proxy。

### 3. Hoskins & Valdes (1990)

作者用来支撑：

- diabatic heating restore low-level baroclinicity。  
  位置：`manuscript.md:176`

#### 风险

即使该句本身可能合理，也不能反推你本文里的 `CP_vert` 就是 diabatic heating 的直接证据。

### 4. Kim et al. (2024)

作者将本文的 `negative IOD-like` 与该文关于 IOD–ZWN3 关系相联系：

- `manuscript.md:204`

#### 风险

“与 IOD 负相关”不等于你这里的偶极就可以被命名为 **IOD-like**。空间相似不等于动力学同构。

---

## 第八阶段：术语克制性检查

### 1. `negative IOD-like`

#### 证据门槛

- 不仅要有空间偶极型 SST；
- 还要说明其与 IOD 的动力学/季节相位/耦合结构具有可比性。

#### 当前是否达标

**未达标。**

#### 建议替换

- `a zonal SST dipole in the tropical Indian Ocean`
- `a west-cold/east-warm SST anomaly pattern`

#### 判级

**Major**

### 2. `acts as a Rossby wave source`

#### 门槛

- 至少正式计算 RWS 或同等严格诊断。

#### 当前是否达标

**未达标。**

#### 建议替换

- `is dynamically consistent with Rossby-wave generation`
- `may provide favorable conditions for Rossby-wave excitation`

#### 判级

**Major**

### 3. `proxy for diabatic heating`

#### 门槛

- 定义上等价或文献严格支持；
- 通常需要独立 `Q` 诊断。

#### 当前是否达标

**明显未达标。**

#### 建议替换

- 删掉，不建议保留 proxy 说法。

#### 判级

**Reject-level**

### 4. `maintained by vertical baroclinic energy conversion`

#### 门槛

- 净维持条件、完整预算、耗散对比。

#### 当前是否达标

**未达标。**

#### 建议替换

- `associated with enhanced vertical baroclinic conversion`
- `coincides with strong vertical baroclinic conversion`

#### 判级

**Major**

### 5. `robust`

#### 门槛

- 跨指标、跨样本、最好跨模型/多方法/敏感性检验。

#### 当前是否达标

对“在本单模式实验内显著”可以；对更广义的 “robust mechanism” 则**偏强**。

#### 建议替换

- `statistically significant in CESM2 sensitivity experiments`
- `robust within this experimental framework`

#### 判级

**Minor–Major**

---

## 第九阶段：模拟审稿人红队审查

### 评审人 1：动力学/理论审稿人

#### 最致命的 3 个问题

1. 你把 `CP_vert`（eddy APE→eddy KE 内部转换）写成了 diabatic heating 的 proxy，这是能量学范畴错误。
2. 你把内部转换项当成了背景场净能量来源，能量库拓扑解释错误。
3. 你没有展示完整 eddy energy budget，却声称 “maintenance mechanism” 已建立。

#### 最容易被攻击的一句话

> `This vertical term also serves as a key proxy variable for kinetic energy generation driven by diabatic heating...`  
> 位置：`manuscript.md:102-103`

#### 必须删掉、重写或补算的内容

- 删掉所有 `CP_vert = diabatic heating proxy` 说法；
- 补完整能量预算图与总收支；
- 若要讲 diabatic heating，补 `Q` 相关诊断。

### 评审人 2：机制怀疑派

#### 最致命的 3 个问题

1. 你声称波列跨赤道传播，但没有证明路径上 stationary wave propagation 的基本条件满足。
2. 你用 T-N stationary WAF 支撑热带/跨赤道传播，但没有说明东风区是否无效及是否 mask。
3. “re-excited” 只是讲了个故事，没有给出独立的局地产波/局地源项诊断。

#### 最容易被攻击的一句话

> `The wave source propagates from the westerly window in the western tropical Indian Ocean across the equator...`  
> 位置：`manuscript.md:197`

#### 必须删掉、重写或补算的内容

- 补背景纬向风与 westerly window 图；
- 补 stationary wavenumber / waveguide 诊断；
- 对无效 WAF 区域 mask；
- 把 “across the equator propagation” 降级为更谨慎表述。

### 评审人 3：方法论审稿人

#### 最致命的 3 个问题

1. 空间场显著性只做逐点 t-test，未考虑多重比较与 field significance。
2. 100 个季均样本被直接视为独立，未讨论有效自由度和低频变率。
3. 25°N–25°S 的宽平均域可能混入多个不同物理过程。

#### 最容易被攻击的一句话

> `...thereby satisfying the fundamental assumptions required for parametric tests.`  
> 位置：`manuscript.md:108`

#### 必须删掉、重写或补算的内容

- 加 FDR / field significance；
- 估算 effective sample size；
- 做平均域敏感性测试。

### 评审人 4：术语与论证编辑

#### 最致命的 3 个问题

1. `negative IOD-like` 的命名强于证据。
2. `acts as a Rossby wave source` 强于证据。
3. `maintained by vertical baroclinic conversion` 与 `confirms / establishes / proves` 类表述超出当前证据门槛。

#### 最容易被攻击的一句话

> `This study establishes a "TP–Indian Ocean–Deep Convection–ZW3" pathway...`  
> 位置：`manuscript.md:16`

#### 必须删掉、重写或补算的内容

- 全文系统降级术语强度；
- 把 `establishes` 改为 `suggests / supports / is consistent with`；
- 把类比命名改为描述性命名。

---

## 第十阶段：最终裁决

## Part A：问题清单

### 1. Reject-level blockers（拒稿级阻断项）

#### R1. 将 `CP_vert` 错当作 diabatic heating / latent heat 的 proxy

##### (a) 问题出在哪？

文稿把 vertical baroclinic conversion (`CP_vert`) 解释成“由 diabatic heating 驱动的 kinetic energy generation 的关键 proxy”。这相当于把“账户内部转账”误当成“外部资金注入”。

##### (b) 为什么这是错的？

`CP_vert` 是涡动 APE 与涡动 KE 的内部转换项，不是非绝热加热 `Q` 本身，也不是 `Q` 的严格 proxy。把它直接写成 latent heating 的直接注入，会在总能量预算解释中造成范畴错误。

##### (c) 具体怎么改？

- 删除 `manuscript.md:102-104`, `176`, `198`, `204` 中所有此类表述；
- 把结论降级为：`CP_vert` 仅表明 eddy APE→eddy KE 转换增强；
- 新增 diabatic heating 直接诊断：`Q`、`Q'T'`、apparent heat source 或 moist static energy budget；
- 重新绘制能量流动图，明确不同能量库之间的箭头。

#### R2. 把内部转换项误写成“从背景场直接获能”的主来源

##### (a) 问题出在哪？

文稿多次把 `CP_vert` 写成波列 `extracting available potential energy from the background flow` 的主渠道。这相当于把“微信零钱转到银行卡”写成“银行继续给你打钱”。

##### (b) 为什么这是错的？

`CP_vert` 是 eddy APE→eddy KE；它不是背景 APE→eddy APE 的那条箭头。把内部转换误写成背景供能，是能量库拓扑错误。

##### (c) 具体怎么改？

- 明确拆分背景 APE→eddy APE 与 eddy APE→eddy KE；
- 只有在完整总预算中才能谈“主能量来源”；
- 若要保留 “extract from background” 说法，需展示背景 APE 到 eddy APE 的主导证据。

#### R3. 核心传播叙事未证明满足 stationary/quasi-stationary wave 的基本物理约束

##### (a) 问题出在哪？

作者声称波列经热带印度洋跨赤道、进入 SH westerly waveguide，但主文未证明关键路径满足西风背景流条件，也未展示所谓 `westerly window` 的充分证据。

##### (b) 为什么这是错的？

定常 Rossby 波不能随意穿越东风区。这像宣称列车顺利跨海，但没有证明中间有桥；若中间是断桥，后面的旅程故事再顺也不成立。

##### (c) 具体怎么改？

- 补背景纬向风分布图，沿波列路径标出风向与强度；
- 补 stationary wavenumber / waveguide 诊断；
- 明确说明哪些区域可传播、哪些区域不可传播；
- 若关键区域存在东风，应把 `continuous cross-equatorial propagation` 改写为更弱的 `cross-hemispheric linkage with SH-side amplification`。

#### R4. 使用 stationary WAF 支撑热带/跨赤道传播，但未证明诊断量在关键区域有效

##### (a) 问题出在哪？

作者使用 T-N stationary WAF 讨论热带印度洋、跨赤道和“再激发”，但未说明东风区是否 mask，也未说明诊断在关键区域的适用性。

##### (b) 为什么这是错的？

若诊断工具在该区域没有物理意义，就不能拿其结果当核心证据。这不是“误差稍大”，而是“尺子根本不适用”。

##### (c) 具体怎么改？

- 对 WAF 仅在满足条件区域展示；
- 对无效区 mask；
- 补说明适用条件；
- 如果跨赤道部分不能由 WAF 严格支撑，就降级传播叙事。

### 2. Major issues（重大问题）

#### M1. 把上层散度偶极直接写成 Rossby wave source，但主文未见正式 RWS 诊断

##### (a) 问题出在哪？

文稿把 divergence / divergent wind 直接等同于 Rossby wave source。

##### (b) 为什么这是错的？

RWS 有明确公式，不是散度图的别名。像看见乌云就说“已经下雨了”——方向对，但证据层级不够。

##### (c) 具体怎么改？

- 补算 Sardeshmukh & Hoskins (1988) RWS；
- 或降级为 `favorable for Rossby-wave generation`。

#### M2. `maintenance mechanism` 结论强于证据

##### (a) 问题出在哪？

作者用局地转换分布和相位关系，直接上升到“维持机制已建立”。

##### (b) 为什么这是错的？

维持要求净收支为正，并能抵消耗散；局地有正值不等于系统被维持。

##### (c) 具体怎么改？

- 做沿波列路径积分；
- 比较源项、内部转换、耗散；
- 若做不到，降级为 `energetically consistent with`。

#### M3. 宽平均域可能混入不同物理过程

##### (a) 问题出在哪？

`25°N–25°S` 的平均域太宽，可能混杂不同纬带过程。

##### (b) 为什么这是错的？

平均后得到的信号不再能唯一归因于你声称的那条环流链。

##### (c) 具体怎么改？

- 做多个纬带敏感性检验；
- 在图中标明核心响应纬带。

#### M4. 空间显著性未处理多重比较，样本独立性假设过强

##### (a) 问题出在哪？

仅使用逐点 t-test，并默认 100 个样本独立。

##### (b) 为什么这是错的？

大面积显著区可能是多重比较假阳性；低频变率会降低有效自由度。

##### (c) 具体怎么改？

- 加 FDR 或 field significance；
- 估算 effective sample size；
- 在方法与讨论中承认局限。

#### M5. `negative IOD-like` 命名强于证据

##### (a) 问题出在哪？

仅凭空间 SST 偶极就命名为 IOD-like。

##### (b) 为什么这是错的？

模态命名不是“长得像”就够，需有对应动力学含义。像看到有翅膀就叫“鹰”，可能其实只是另一种鸟。

##### (c) 具体怎么改？

- 改成 `west-cold/east-warm SST dipole`；
- 若坚持 IOD-like，需补 IOD 相关动力学与季节结构论证。

#### M6. 固定 background flow 的解释过强

##### (a) 问题出在哪？

把固定 CTRL background 写成 `strictly isolate direct contribution`。

##### (b) 为什么这是错的？

你只是做了受控比较，不是把背景流作用从现实机制中“剥离”掉了。

##### (c) 具体怎么改？

改成更谨慎的 methodological wording。

### 3. Minor issues（次要问题）

#### m1. JJA minus annual mean 的物理解释需要加强

建议补一段说明该操作的物理目的与局限。  
位置：`manuscript.md:128-130`

#### m2. `robust`, `establishes`, `confirm` 等词过强

应系统降级。  
位置：`manuscript.md:16`, `122`, `192-198`

#### m3. `independent of ENSO` 依赖补充图，主文证据不足

若不在主文展示，建议弱化。  
位置：`manuscript.md:204`

## Part B：修改路线图

### P0（不改就发不了）

#### 修改包 P0-1：能量学框架重建

解决问题：

- R1
- R2
- M2

具体动作：

1. 重写 3.2.2 和 4.4 中所有关于 `CP_vert` 的物理解释；
2. 画完整能量库拓扑图；
3. 明确哪些项是背景→扰动，哪些是内部转换；
4. 若要保留“潜热驱动”，补 `Q` 相关诊断；
5. 结论改为“与深对流一致”而非“已证明由 latent heating 维持”。

#### 修改包 P0-2：传播物理约束与诊断有效性补证

解决问题：

- R3
- R4
- M1

具体动作：

1. 补背景纬向风 / 西风窗口图；
2. 检查并标出东风区；
3. 对无效区 WAF mask；
4. 最好补 RWS 与 stationary wavenumber / waveguide 诊断；
5. 若补不出来，就全面降级“跨赤道传播”与“Rossby wave source”措辞。

### P1（直接影响论证质量）

#### 修改包 P1-1：平均域与统计稳健性修补

解决问题：

- M3
- M4

具体动作：

1. 对 divergence / omega 剖面做纬带敏感性测试；
2. 对空间场显著性做 FDR / field significance；
3. 评估 effective sample size；
4. 在讨论中加入低频内部变率影响。

#### 修改包 P1-2：术语降级与引用语义收紧

解决问题：

- M5
- M6
- m2
- m3

具体动作：

1. `negative IOD-like` → 描述性命名；
2. `acts as a Rossby wave source` → `consistent with`；
3. `establishes/confirms/proves` → `suggests/supports`；
4. `independent of ENSO` 若无主文证据则弱化。

### P2（建议改进）

#### 修改包 P2-1：方法叙述清晰化

解决问题：

- m1

具体动作：

1. 解释 `seasonal deviation relative to annual mean` 的物理含义；
2. 说明为何此操作不会改变核心结论，或补敏感性结果。

## Part C：投稿裁决

### 裁决：**Blocked**

#### 原因

满足 `Blocked` 条件中的多项：

- 核心解释建立在**错误 proxy** 上：`CP_vert` 被误写为 diabatic heating / latent heat proxy；
- 核心传播叙事可能违反或至少**未证明满足教科书级物理约束**；
- 中心机制缺少必要诊断量：
  - 正式 RWS；
  - 传播路径上的背景西风条件 / waveguide 诊断；
  - 完整能量预算区分外源与内部转换。

---

## 总结性判断

这篇稿件目前**不是“故事不够完整”这么简单**，而是存在几处会被动力学/理论审稿人直接抓住的硬伤，尤其是：

1. **`CP_vert` 的物理意义被写错了**；
2. **跨赤道传播路径的物理可行性没有被证明**；
3. **WAF 关键证据的适用条件没有交代**；
4. **“Rossby wave source” 与 “maintenance mechanism” 的用词都强于证据。**

如果作者愿意大幅降级措辞，并补做关键诊断，这篇稿件仍有机会转为 **Major revision needed**；但在当前版本下，结论应为：

> **Blocked**
