Basic of EIS

------

> *DOC INFO*: 电化学阻抗谱 (basic of EIS)		*2021/03/10*	*Last update: 2023/02/02*	*Zhong F.    U.Tokyo*	*601330948@qq.com*
>
> **Thank you, Matt Lacey, yyds!*

------

[TOC]

### 原理

由Ohm定律有：

$E=IR$

对于阻抗 Z 而言，可以简单地理解成替换了Ohm定律中的 R，则有：

$E=I\displaystyle \pmb{Z}$

于是，输入一个振动（oscillating）的电压，测量振动的响应电流。

输入电压：$E(t) = \left|E\right|\sin(\omega t)$

其中$\omega=2\pi f$【注1：关于为什么使用角频率（文尾）】

得到的响应电流为：$I(t) = \left|I\right|\sin(\omega t + \theta)$

相位有变化是因为存在感抗 （reactance, e.g., a capacitance or inductance）

故有

$\displaystyle \pmb{Z} = \frac{E(t)}{I(t)} = \frac{|E| \sin(\omega t)}{|I| \sin(\omega t + \theta)} = |Z| \frac{\sin(\omega t)}{\sin(\omega t + \theta)}$

图示如下：

![img](http://lacey.se/img/eis/lissajous.gif)

<img src="https://www.gamry.com/assets/Uploads/origin-lissajous-figure.jpg" alt="origin lissajous figure" style="zoom:50%;" />

这样会得到电流与电压的关系，即Lissajous curve。最早期的阻抗谱就是通过观察这些Lissajous curve所得到的。



由Eular公式：

$$
e^{jx} = \cos(x) + j \sin(x)
$$
可以将阻抗Z写为
$$
\displaystyle \pmb{Z} = \left|Z\right| e^{j\theta} = \frac{\left|E\right|e^{j \omega t}}{\left|I\right|e^{j \omega t + \theta}}
$$
或者更简单的写为
$$
\displaystyle \pmb{E} = I \pmb{Z} = I\left|Z\right|e^{j \theta}
$$
通过oscillating voltage对 oscillating current所得出的**Z**有一个模|Z|和一个相位角 $\theta$ ，可以用极坐标表示，但更一般的是用笛卡复平面（Cartesian complex plane）表示。将**Z**的实部与虚部拆开，有：
$$
 \displaystyle \pmb{Z} = Z' + j Z''
$$
Z'和Z''分别是电阻与电感部分（Z' and Z'' are resistive and reactive parts of the impedance respectively.）

可以将阻抗画在相位矢量图（Argand diagram，如下）上，其是Nyquist图的基础。

<img src="http://lacey.se/img/eis/argand.png" alt="img" style="zoom:50%;" />

### Nyquist图

1. 阻抗总是在最高频率出最低；
2. Z''是负值；按照惯例，capacitance is a negative reactance, 所以阻抗谱在大多数情况下，只有正的Z′值，负的Z″值；
3. Nyquist图的形状特征对应电路的一定特征。
4. 正方形！

### Randles电路

![The Randles circuit](http://lacey.se/img/eis/ec-randles.png)

> A simple model for an electrode immersed in an electrolyte is simply the series combination of the **ionic resistance**, **R~i~**, with the **double layer capacitance**, **C~dl~**. 
>
> If a faradaic reaction is taking place, of the sort:
> $$
> \displaystyle \text{O} + \text{e}^- \rightleftharpoons \text{R}
> $$
> then that reaction is occurring in parallel with the charging of the double layer – so the **charge transfer resistance**, **R~ct~**, associated with the faradaic reaction is in parallel with C~dl~.
>
> **The key assumption is that the rate of the faradaic reaction is controlled by diffusion of the reactants to the electrode surface.** The **diffusional resistance element (the Warburg impedance, W**), is therefore **in series** with R~ct~.
>
> Ranldes电路的核心假设是法拉第反应速率受反应物的扩散到电极表面的速度控制，即界面过程的速控步为扩散，故需要在R~ct~串一个扩散阻抗即Warburg阻抗。

t



### Laplace impedance measurement

可以通过Laplace impedance测出传统AC (alternative current) impedance区分不出来的desolvation和solvation阻抗。这是因为AC impedance测出的阻抗是通过充放电取平均所得到的。下图即为Laplace impedance测出来的充放电过程中的阻抗区别。

<img src="https://pubs.acs.org/na101/home/literatum/publisher/achs/journals/content/ancham/2020/ancham.2020.92.issue-5/acs.analchem.9b05321/20200225/images/large/ac9b05321_0002.jpeg" alt="img" style="zoom:25%;" />



对半圆的特征频率进一步分析可以使用distribution of relaxation times (DRT) analysis。该方法的本质就是对EIS谱进行去卷积（deconvolution）。



### 界面阻抗——模拟与测量

Michael Hess做了一个还行的工作^[6]^，主要是关于SEI的阻抗的模拟，以及其在不同温度下的表现，具有很大的参考意义。还有相关过电势。他指出界面的过电势并不是随着界面电阻的增大而线性变化的（恒流充放时）。

界面过电势分为三个部分：

1. B-V部分。对应电荷转移过程；——B-V方程
2. 离子在电解液中的传导；——Ohm定律
3. 离子在SEI中的传导。——Hess自己的半经验方程^[7]^。



### 关于活化能

Activation energy was calculated by follow equation:

$$\frac{T}{R_{ct}}=A\cdot exp(\frac{-E_a}{RT})$$

so, $$ln \frac{T}{A \cdot R_{ct}}=\frac{-E_a}{RT}$$; 所以一般作图：$$ln \frac{T}{R_{ct}}$$(y axis)与$$\frac{1000}{T}$$(x axis)，斜率为E~a~



### Reference

> [1] http://lacey.se/science/eis/eis-principles/
>
> [2] http://lacey.se/science/eis/simulation-randles-circuit/
>
> [3] Matt Lacey写了线上EIS**演示**web app：http://lacey.se/apps/eis/simulate-eis/，使用说明：http://lacey.se/science/eis/equivalent-circuit-simulation/。
>
> [4] Tanibata, N.; Morimoto, R.; Nishikawa, K.; Takeda, H.; Nakayama, M. Asymmetry in the Solvation–Desolvation Resistance for Li Metal Batteries. *Anal. Chem.* **2020**, *92* (5), 3499–3502. https://doi.org/10.1021/acs.analchem.9b05321.
>
> [5] Schichlein, H.; Müller, A. C.; Voigts, M.; Krügel, A.; Ivers-Tiffée, E. Deconvolution of Electrochemical Impedance Spectra for the Identification of Electrode Reaction Mechanisms in Solid Oxide Fuel Cells. *Journal of Applied Electrochemistry* **2002**, *32* (8), 875–882. https://doi.org/10.1023/A:1020599525160.
>
> [6] Hess, M. Temperature-Dependence of the Solid-Electrolyte Interphase Overpotential: Part I. Two Parallel Mechanisms, One Phase Transition. *J. Electrochem. Soc.* **165**, A323 (2018).
>
> [7] M. Hess, “Non-linearity of the solid-electrolyte-interphase overpotential,” Electrochim Acta, 244, 69 (2017).



注释

> 【注1】
>
> 关于为什么用角频率：角频率是单位时间内的角位移，或正弦波相移变化率（单位时间内相位变化量）。假设正弦信号周期为T，则在T时间内，相位变化了2*pi，则单位时间内相位变化为2*pi / T，也就是角频率公式。
>
> 模拟频率的单位：f 赫兹	Ω 弧度每秒=2pif 
>
> 数字频率w=TΩ,T是对某个具体模拟信号的等间隔采样的时间间隔[采样频率=fs=1/T,根据采样定理,该模拟信号的最高频率=0.5fs,实际需要超过的部分,例如语音信号最高3400HZ,取4000,故采样频率=8000Hz；采样之前还要对模拟信号滤波,滤除高于0.5fs的无用分量],故单位=弧度；w=0\~2pi对应模拟频率的f=0\~f s
> 对于离散信号的连续频谱,在w=0\~2pi上等间隔采样N个点[便于利用计算机处理],k=0\~N-1虽然没有单位,实际与w有对应关系的,即k=0~N-1对应的w频率=0,[2pi/N],...,[2pi/N]k,...,自然也跟模拟信号的频率有对应关系了.
>
> https://www.zhihu.com/question/29863278
>
> https://www.zybang.com/question/84e570112b090ae5b63992d324ed87e4.html