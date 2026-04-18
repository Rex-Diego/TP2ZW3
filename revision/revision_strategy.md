# TP-ZW3 论文修改策略



## 第一部分：最高优先级修改（P0）——不改就发不了

这些是三位审稿人都关注的核心问题，必须首先解决。

---

### P0-1. 重写能量转换分析框架（对应 R2-III, R3-Comment 1/2/3）

**问题出在哪？**

文中把"斜压能量转换 CP"分成了水平项 CP_hor 和垂直项 CP_vert，然后求和。审稿人指出这在物理上有根本性的概念混淆。

用一个比喻来解释：把大气中的能量想象成"钱"。

- **背景场**就像一个"银行"，存着巨量资金
- **涡动（波）** 就像一个"个人账户"，有两种存款方式：**位能存款**（APE）和**动能存款**（KE）
- **CP_hor**（水平斜压转换）= 从银行取钱存到个人的"位能账户"（背景APE → 涡动APE）
- **CP_vert**（垂直项 ω'T'）= 个人把"位能账户"的钱转到自己的"动能账户"（涡动APE → 涡动KE）
- **CK**（正压转换）= 从银行取钱存到个人的"动能账户"（背景KE → 涡动KE）

文中的错误相当于：把"从银行取了多少钱"（CP_hor）和"自己内部转账了多少"（CP_vert）加在一起，说这就是"从银行总共获取的能量"——但内部转账不是从银行拿的钱啊！

更严重的是，文中还说CP_vert（即ω'T'）是"非绝热加热的代理变量"。但实际上：
- 非绝热加热（潜热释放）对涡动位能的贡献应该用 **Q'T'** 来衡量（Q是加热率，T'是温度扰动）
- ω'T' 在干绝热过程中也可以存在（只要有暖空气上升就行），所以不能等同于非绝热加热

**具体怎么改：**

**(a) 修改 Eq.9 及其物理解释（Section 3.2.2）**

- 不再把 CP_hor 和 CP_vert 求和成一个 CP
- 分别讨论三个独立的能量转换路径：
  1. **CK**：背景动能 → 涡动动能（正压过程）
  2. **CP_hor**：背景有效位能 → 涡动有效位能（斜压过程，这才是真正从"背景场"获取能量）
  3. **CP_vert**（ω'T'）：涡动有效位能 → 涡动动能（涡动内部的能量形式转换）
- 把 CP_vert 的讨论重新定位：它说明的是"涡动内部位能向动能的高效转换"，体现了深对流环境下垂直运动对波列动能的补充，而**不是**从背景场获取能量

**(b) 补充计算非绝热加热项 CQ（新增诊断量）**

- 如果要论证"湿过程/潜热释放对ZW3维持很重要"，需要计算真正的非绝热加热能量生成率：
  - **CQ ∝ Q'T'**（Q是非绝热加热率，T'是温度扰动）
  - CESM2 可以输出非绝热加热率（包括潜热加热 DTCOND 等变量）
- 用 CQ 来替代之前"ω'T' 是非绝热加热proxy"的论证
- 参考文献：Kosaka and Nakamura (2006) 中对 CQ 的定义

**(c) 修正 Chang et al. (2002) 的引用**

- 删除"ω'T' serves as a key proxy variable for kinetic energy generation driven by diabatic heating"这句
- Chang et al. (2002) 实际讨论的是：潜热释放增强了瞬变涡旋的斜压能量转换效率，并放大了上层波振幅。可以在讨论CQ的地方引用，但要准确描述其结论
- 补充引用：Kosaka and Nakamura (2006) 对CQ的定义和诊断方法

**(d) 删除"mechanical energy"表述（Section 3.2.2，L.299-300）**

- 把"latent heat release is often directly converted into mechanical energy via vertical motion"改为更准确的表述
- 例如："latent heat release first generates eddy available potential energy (via diabatic heating), which is then efficiently converted to eddy kinetic energy through vigorous vertical motion in deep convective regions"

**(e) 重做 Fig.9 及 Section 4.4 的能量分析**

- Fig.9 保留 CK、CP_hor、CP_vert 三个面板，但修改讨论语言
- 新增 CQ 的空间分布图（可以作为新的一个panel或supplementary figure）
- 新增：对整个南半球对流层进行空间积分（R2-III-B的建议），给出一个积分后的能量收支表或柱状图，定量说明各项的相对重要性
- 关键结论修改方向：从"CP_vert主导能量获取"改为"涡动主要通过CP_hor从背景场获取有效位能，而在深对流区域，非绝热加热（CQ）额外注入有效位能，随后通过高效的垂直转换（CP_vert）转化为动能，共同维持ZW3的深厚正压结构"

**需要从模式输出的变量：**
- 如果已保存：DTCOND（对流加热率）、QRL（长波辐射加热）、QRS（短波辐射加热）等
- 如果没有保存，需要回去检查模式输出文件里有没有这些变量，或者用温度倾向方程反推

---

### P0-2. 计算并展示 Rossby Wave Source（对应 R2-I, R2-II）

**问题出在哪？**

文中说"上层散度风和涡度产生了Rossby波源"，但没有真正算出波源在哪里、有多强。审稿人说：光给我看散度和涡度各自的分布图还不够，我需要看到它们具体在哪里、以什么方式产生了波源。

**什么是 Rossby Wave Source (RWS)？**

Sardeshmukh and Hoskins (1988) 定义：

```
S = -∇ · (vχ · ζa)
```

其中 vχ 是散度风（辐散风），ζa 是绝对涡度。展开后：

```
S = -ζa · D - vχ · ∇ζa
```

第一项：涡度的辐散效应（涡度拉伸项）——散度D作用于绝对涡度
第二项：散度风对涡度的平流——辐散风把涡度从一个地方搬到另一个地方

**具体怎么改：**

**(a) 计算 RWS**

- 需要的变量：200 hPa 的水平风场（u, v）
- 用 Helmholtz 分解把总风场分成旋转风和散度风
- 计算绝对涡度 ζa = ζ + f
- 按上面公式计算 S
- 分别对 CTRL 和 SENS 计算，然后取差值
- 工具：NCL 有现成的函数（`uv2dv_cfd` + `dv2uvf` 可以做 Helmholtz 分解），Python 中 `windspharm` 包也可以

**(b) 修改 Fig.7**

- 在 Fig.7 中新增一个 panel 展示 RWS 的空间分布
- 或者替换掉当前的某个不太必要的 panel
- 关键是要清楚展示：波源最强的区域在哪里（预期在热带印度洋上空），以及它与散度风和涡度的关系

**(c) 在南半球也寻找波源**

- R2 特别指出：既然定常Rossby波不能跨赤道，那SH的波列一定是由SH本地的波源激发的
- 所以需要展示RWS在南半球是否也有显著信号
- 如果有——说明不是NH的波直接传过来的，而是热带过程在SH也产生了波源，这其实更支持"印度洋SST → 热带对流 → SH波源"的机制

**(d) 补充引用 Sardeshmukh and Hoskins (1988)**

- R2 已经指出参考文献缺了这篇，需要在正文和参考文献列表中补充

---

### P0-3. 重构跨赤道传播的叙述（对应 R2-II）

**问题出在哪？**

文中 Section 4.4（L.669-676）描述了一个从北半球到南半球的"Rossby波传播通道"。R2 指出一个基本的大气动力学事实：

**定常Rossby波无法穿越东风区。**

解释一下：Rossby波的相速度天然是向西的。要让Rossby波变成"定常"（静止不动），需要一个向东的背景风来"拖住"它。在赤道附近的南半球一侧，JJA是东风（西向），所以定常Rossby波根本不可能在那里传播。

这意味着文中Fig.8暗示的"波从NH连续传播穿过赤道到达SH"在物理上是不可能的。

**具体怎么改：**

**(a) 修改 Fig.8**

- 在赤道附近气候态纬向风为东风（西向）的区域，将波活动通量矢量 mask 掉（设为空白）
- 因为在东风区里，T-N波活动通量的定义本身就不适用（它基于定常波假设）
- 可以叠加一条等值线，标出气候态200hPa纬向风为零的线（即"临界纬度"），让读者清楚看到波导的边界
- R2 还建议 Fig.8b-c 也用位势高度Z（像Fig.8a一样），而不是经向风v，以便直接对比

**(b) 重写 L.669-676 的叙述**

- 不能再说"波从NH传播到SH"
- 正确的叙述应该是一个**两段式过程**：
  1. TP强迫在NH激发Rossby波（通过正压/斜压过程），但这些波无法穿越赤道东风屏障
  2. TP通过调制印度洋SST和热带对流（air-sea coupling），在热带地区产生了一个独立的Rossby波源（对应P0-2中计算的RWS）
  3. 这个位于热带/SH的波源重新激发了向SH传播的Rossby波列
- 这其实更好地支持了"TP-Indian Ocean-Deep Convection-ZW3"通道的核心叙事——印度洋和热带对流是关键的"中继站"，不是简单的波传播

**(c) "westerly window"的证据（L.821）**

- R2 追问"热带西印度洋的westerly window在哪里？"
- 需要检查CTRL气候态200hPa纬向风场，看热带印度洋上空是否确实存在西风区域
- 如果存在：在Fig.8中用等值线标出
- 如果不存在：删除"westerly window"的说法，改用更准确的表述

---

## 第二部分：高优先级修改（P1）——直接影响论证质量

---

### P1-1. 放弃"negative IOD-like"命名（对应 R2-5, R3-Comment 5）

**怎么改：**

- 全文搜索替换所有"negative IOD-like"、"IOD-like"的表述
- 改用中性术语，例如：
  - "zonal SST dipole"（纬向SST偶极子）
  - "dipolar SST anomaly pattern"（偶极型SST异常模态）
  - "west-cold, east-warm SST pattern"（西冷东暖SST模态）
- 在首次出现时可以补充一句："This pattern bears some resemblance to the negative phase of the IOD but differs in its spatial extent and center locations (see Saji et al., 1999 for the canonical IOD definition)"
- 这样既承认了与IOD的相似性，又明确区分了两者

---

### P1-2. 修正背景场定义的描述（对应 R3-Comment 4）

**怎么改：**

- L.313-314 原文说"背景流切变和温度梯度都固定为CTRL的气候态"
- 需要明确区分两个不同的"背景场"：
  - 波活动通量（WAF, Eq.7）：背景场 = CTRL的**纬向平均**流（这是T-N通量的标准定义）
  - 能量转换（Eq.8-9）：背景场 = CTRL的**纬向平均**流（如果确实是这样用的）
- 在方法部分（Section 3.2.2）明确写出每个诊断量使用的背景场定义
- 如果WAF和能量转换使用的背景场不同，需要说明理由

---

### P1-3. 缩小 Fig.6c 的经向平均范围（对应 R3-Comment 8）

**为什么重要：**

Fig.6c 目前对25°N-25°S做平均。但10°N-25°N是TP直接影响的区域——那里的散度异常可能直接来自TP的机械/热力强迫，而不是IOD型SST异常驱动的。把这些信号混在一起，就无法证明"SST偶极子 → 对流 → 上层散度"这条因果链。

**怎么改：**

- 重做Fig.6c，将平均范围缩小到 **10°S-10°N**
- 如果信号仍然显著——好消息，因果论证更干净了
- 如果信号变弱——需要诚实讨论，可能加一个panel对比两个范围的结果
- 同样的逻辑也适用于 Fig.6f（垂直速度的经向平均），建议一并缩小范围
- 可以把25°N-25°S的原图作为补充材料保留

---

### P1-4. 解释去除年均值操作的物理合理性（对应 R3-Comment 6）

**怎么改：**

- 在描述Fig.3c时，补充1-2句解释为什么去除年均值：
  - "The annual-mean SST difference (CTRL-SENS) represents the year-round, seasonally-invariant component of the TP's thermal impact on the Indian Ocean. By subtracting this background, Figure 3c isolates the component that is unique to the JJA season, i.e., the seasonal enhancement of the dipolar pattern driven by the concurrent monsoon circulation."
- 或者更简单的策略：如果Fig.3a已经足够说明JJA的SST偶极子特征，可以把Fig.3c移到补充材料，降低其在论证链中的权重

---

### P1-5. 补充东印度洋MAM暖异常的成因（对应 R3-Comment 7, R2-5-ocean memory）

**怎么改：**

- 在Section 4.2讨论"ocean memory"时，补充1-2句解释MAM暖异常的物理成因
- 可能的机制：在MAM期间，TP热力强迫尚未完全激活季风环流，因此印度洋表面风场响应较弱，但TP对大气环流的调制可能已通过减弱表面风速等方式产生了SST增暖
- 引用 Zhao et al. (2021) 关于"季风爆发前后TP对印度洋响应截然相反"的结论
- R1-5 也建议引用 Xie et al. (2009) 中关于印度洋热惯性时间尺度（1-3个月）的数据

