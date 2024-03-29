**Technical Memo 3#**

------

Theme: DSC

Update time: 2021/02/26

------

DSC基本原理与经典应用

在程序温度（升／降／恒温及其组合）过程中，测量样品与参考物之间的热流差，以表征所有与热效应有关的物理变化和化学变化。

### **典型应用**

| 玻璃化转变   | 相容性        |
| ------- | ---------- |
| 熔融、结晶   | 热稳定性、氧化稳定性 |
| 熔融热、结晶热 | 反应动力学      |
| 共熔温度、纯度 | 热力学函数      |
| 物质鉴别    | 液相、固相比例    |
| 多晶型     | 比热         |

### DSC与DTA是什么关系？

DSC的前身是差热分析DTA，我简单介绍下工作原理的区别

DTA呢，只能测试△T信号，无法建立△H与△T之间的联系

而DSC测试△T信号，并建立△H与△T之间的联系

### DSC测试需要注意哪些条件？

**主要有如下几点：**升温速率、样品用量、制样方式、实验气氛、坩埚的选取、样品温度控制（STC）、DSC基线。

### 升温速率有哪些影响？

| **快速升温**        | **慢速升温**         |
| --------------- | ---------------- |
| 使DSC峰形变大        | 有利于相邻峰或相邻失重平台的分离 |
| 特征温度向高温漂移       | DSC/DTA峰形较小      |
| 相邻峰或失重台阶的分离能力下降 | ——————————       |

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/4Coxww3Vbq5IYhObXNxQuiaHWnCDCzqBYm92ep0VEKuBGrS5v4VRUP4B7icHoOPpIJrcEEPNX0OGqANtR8lPQjlg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

热分析领域常用而标准的升温速率是10K/min

利用多个不同升温速率下得到的一系列测试结果，可进行动力学分析

在存在竞争反应路径的情况下，不同的升温速率得到的终产物组成可能不同

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/Cu5qQlKZvqAKvvibqLx9b6141Gqx6BZAHyFMEXMj0WdjEZWpHNFqsnJcxskNkjbInxSQYgrtkiaM5c7tQ7ugwpKQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 样品量对DSC测试有哪些影响？

| **样品量小**       | **样品量大**            |
| -------------- | ------------------- |
| 所测特征温度较低，更“真实” | 峰值温度向高温漂移           |
| 有利于气体产物扩散      | 样品内温度梯度较大，气体产物扩散亦稍差 |
| 相邻峰（平台）分离能力增强  | 峰分离能力下降             |
| DSC 峰形也较小      | 峰形加宽                |
| ————————————   | 能增大 DSC 检测信号        |

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/4Coxww3Vbq5IYhObXNxQuiaHWnCDCzqBY7xorXey390l1Go3iaQkria5g8k8icHYzNicuszw6lyVV3U2gcF7uicaRreA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

一般情况下，以较小的样品量为宜。热分析常用的样品量为5～15mg。

在样品存在不均匀性的情况下，可能需要使用较大的样品量才具有代表性。

### 测试过程中，如何选择升温速率和样品量？

（1）提高对微弱的热效应的检测灵敏度：提高升温速率，加大样品量；

（2）提高微量成份的热失重检测灵敏度：加大样品量；

（3）提高相邻峰（失重平台）的分离度：慢速升温速率，小的样品量。

### 如何选择合适的**DSC样品**制样方式？

（1）块状样品：建议切成薄片或碎粒；

（2）粉末样品：使其在坩埚底部铺平成一薄层；

（3）堆积方式：一般建议堆积紧密，有利于样品内部的热传导；对于有大量气体产物生成的反应，可适当疏松堆积。

### DSC测试气氛分哪些类，有何区别？

气氛主要是动态气氛、静态气氛和真空3类，可以从以下三点来分别

（1）从保护天平室与传感器、防止分解物污染的角度，一般推荐使用动态吹扫气氛；

（2）对于高分子TG测试，在某些场合使用真空气氛，能够降低小分子添加剂的沸点，达到分离失重台阶的目的；

（3）若需使用真空或静态气氛，须保证反应过程中的释出气体无危害性。

在不同的气氛条件下，结果有时候也是不同的，我们举个“NR/SBR 橡胶中增塑剂的分解”的例子：

将 NR/SBR 共混橡胶材料，在 N2 气氛下按照标准的 TG 方法进行分析，增塑剂的失重量为 9.87%。（增塑剂失重与橡胶分解台阶有较大重叠）

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/Cu5qQlKZvqAKvvibqLx9b6141Gqx6BZAH9CEx7LNDIc1gwTOmXoOIYsYMBka5PuBFZ9icV8HLEqEzYTiaqIfGch2g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

将该样品在真空下进行测试，由于增塑剂沸点的降低，挥发温度与橡胶分解温度拉开距离，得到了更准确的增塑剂质量百分比：13.10%。

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/Cu5qQlKZvqAKvvibqLx9b6141Gqx6BZAHY0X5QzZicc1e92XnsK8lbCPouAV0hIvpg5PPZM2FMowyRbYqRbF1dhg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### DSC测试常用气氛和特殊气氛有哪些？

常用气氛：

N2: 常用惰性气氛

Ar: 惰性气氛，多用于金属材料的高温测试。

He: 惰性气氛，因其导热性好，有时用于低温下的测试

Air: 氧化性气氛，可作反应气氛

O2: 强氧化性气氛，一般用作反应气氛

特殊气氛（如H2、CO、HCl 等）：

考虑气氛在测试所达到的最高温度下是否会与热电偶、坩埚等发生反应，注意防止爆炸和中毒。

通过改变测试气氛（如真空-氮气-空气），有助于深入剖析材料成分。

### DSC都有哪些坩埚，他们有什么区别？

为了适应千变万化的各种样品，避免样品与坩埚材料之间的不相兼容，设备供应商配备了多种不同材质不同特点的坩埚，其中几种坩埚图示如下：

![图片](https://mmbiz.qpic.cn/mmbiz_png/Cu5qQlKZvqAKvvibqLx9b6141Gqx6BZAH7KW0aTIo7I8smn4eqWGKVhxw9mlAqtqzarS4ic6FJvTcAsticbhrtkLQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**常用坩埚：**Al, Al2O3, PtRh

**其它坩埚：**PtRh+Al2O3,  Steel, Cu, Graphite, ZrO2, Ag, Au, Quartz 等

**压力坩埚：**中压坩埚，高压坩埚

| Al坩埚     | 传热性好，灵敏度、峰分离能力、基线性能等均佳温度范围较窄（< 600℃）用于中低温型DSC测试可用于比热测试                                                |
| -------- | ----------------------------------------------------------------------------------------------------- |
| PtRh 坩埚  | 传热性好，灵敏度高、峰分离能力、基线性能佳温度范围宽广适于精确测量比热易与熔化的金属样品形成合金清洗与回收：可使用氢氟酸浸泡清洗                                      |
| Al2O3 坩埚 | 样品适应面广，其灵敏度、峰分离能力、基线漂移等较PtRh差温度范围宽广（可用于高温1650℃ ）不适于测定比热易与部分无机熔融样品（如硅酸盐、氧化铁等）反应或扩散渗透清洗与回收：可使用王水与氨水浸泡清洗 |
| Cu坩埚     | 对塑料的氧化有催化作用，有时用于氧化诱导期（O.I.T.）测试                                                                       |
| 中压与高压坩埚  | 适用：挥发性液体样品，液相反应，需要维持气体分压的封闭体系反应中压坩埚最高使用压力20bar高压坩埚为100bar温度较低、挥发物压力不太大时，可用密闭压制的Al坩埚代替                 |

### DSC测试中坩埚加盖与否如何选择？

首先要知道坩埚加盖的优缺点以及坩埚盖扎孔的目的

| 优点                      | 缺点            | 扎孔的目的         |
| ----------------------- | ------------- | ------------- |
| 有利于体系内部温度均匀             | 减少了反应气氛与样品的接触 | 保证样品与气氛一定接触   |
| 减少辐射效应与样品颜色的影响          | 产物气体不易带走      | 允许一定程度的气固反应   |
| 防止微细样品粉末飞扬，或在抽取真空过程中被带走 | 导致反应体系压力较高    | 允许气体产物随动态气氛带走 |
| 有效防止传感器受到污染             |               | 保持坩埚内外压力平衡    |

（1）物理效应测试（熔融、结晶、相变等DSC测试），通常选择加盖坩埚；

（2）未知样品，出于安全性考虑，通常选择加盖坩埚；

（3）气固反应（如氧化诱导期测试或吸附反应），使用不加盖敞口坩埚；

（4）液相反应，易挥发样品，使用加盖压制Al 坩埚、中压或高压坩埚；

（5）有气体生成的反应（包括多数分解反应 ）或偏重于 TG 的测试，在不污染损害样品支架的前提下，根据实验需要，进行加盖与否的选择。

### 如何测试较微弱的、不易测出的玻璃化转变？

按照一般的热分析规律，可考虑加大样品量与使用较快一些的升温速率。

对于半结晶性的高分子材料，咱们三步走：

（1）先升过熔点使样品充分熔融；

（2）随后淬冷至玻璃化温度以下；

（3） 再次升温时玻璃化转变较为明显.

### 使用液氮进行冷却的降温测试，如何使温度曲线尽快达到线性？

在降温段之前设置一个恒温段（一般5～10min左右），将LN打开，初始流量不需很大，让仪器在降温之前先适应一下LN。然后降温段设置的流量根据情况酌情加大一些，但无需开到最大，仪器会自动根据冷却需要调节液氮流量。这样就能使冷却温度线较快的达到线性。

### 铝坩埚的加盖与压制有哪些实验技巧？

（1）坩埚盖子扎孔密闭：这是常规的坩埚使用方法，它适用于固体测试，样品可以粉末，颗粒，片状，块状等等。

（2）坩埚盖子扎孔，不密闭：这种方法是一种比较经济的方法，对于节省坩埚损耗很有帮助。有些样品做完试验后可以取出来且不污染坩埚，我们可以采取这种方法，不用压机将坩埚盖子和平盘压死，这样坩埚就可以重复使用了。

（3）敞口坩埚：即不加坩埚盖子，它适用于需要与吹扫气氛充分接触的实验（如氧化诱导期测试），但由于样品表面与流动气体接触会带走一定的热量，量热精度会稍低一些。

（4）坩埚密闭：坩埚盖子不扎孔，用压机将坩埚牢牢密封住，它适用于常规的液体测试。对于一些需要完全密闭，能承受更高压力的测试，耐驰还提供专门的中压、高压坩埚。

### DSC操作过程中有哪些要特别注意的？

（1）仪器可一直处于开机状态，尽量避免频繁开机关机

（2）仪器应至少提前1小时开机

（3）尽量避免在仪器极限温度附近进行恒温操作

（4）试验完成后，必须等炉温降到200°C以下后才能打开炉体

（5）测试样品及其分解物不能对传感器、热电偶造成污染

**具体措施：**实验前应对样品的组成有大致了解，如有危害性气体产生，实验要加大吹扫气的用量

（6）测试样品及其分解物绝对不能与测量坩锅发生反应，具体为：

铝坩锅测试，测试终止温度不能超过600°C；

绝对避免使用铂坩锅进行测试金属样品；

金属样品的测试需查蒸气压～温度表格。

### 炉体如果已发生污染，该如何处理？

（1）使用棉花棒蘸上酒精轻轻擦洗；

（2）使用大流量惰性吹扫气氛空烧至600℃；

（3）在日常使用温度范围内进行基线的验证测试，若基线正常无峰，传感器一般仍可继续使用；

（4）使用标样In与Zn进行温度与灵敏度的验证测试，若温度与热焓较理论值发生了较大偏差，需要重新进行校正。

> https://mp.weixin.qq.co2m/s/H8a6Twpt5CpO5ZaZ0GvdiA
