**Technical Memo 1#**

------

Theme: **离子迁移数**（Transport and transference in battery electrolytes）

Update time: 2021/01/22

------

**原理**

假设一完美的体系，电流流动初始取决于电池的电导与电压差

$I_0 = \frac{\sigma}{k} \Delta V$

其中k=l/S（长度/面积）

施加一个很小的电压时（<10mV），达到稳态时，溶液浓度梯度不随时间变化。阳离子的电迁移正好被扩散所平衡

<img src="http://lacey.se/img/science/transportnumber3.png" alt="Steady state current flow in a symmetrical cell" style="zoom:25%;" />

此时电流$I_{ss}$为：$I_{ss} = \frac{t_+ \sigma}{k} \Delta V$

易得：$t_+ = \frac{I_{ss}}{I_0}$ （理想情况，忽略界面电阻，电解质完全解离。）

<img src="http://lacey.se/img/science/transportnumber5.png" alt="Current flow during polarisation of a symmetrical cell" style="zoom:25%;" />



但以上只针对理想情况。

在真实体系中存在两个问题：

1. 存在界面阻抗，这些电阻也会随着时间和浓度的变化而变化。
2. 电解质并不完全满足Arrhenius公式，即并不是完全解离，存在诸如[LiX]的中性对，抑或是[Li~2~X]^+^或[LiX~2~]^-^。





------

**方法**

最常用的是Bruce-Vincent方法，但是它应用的前提条件是稀溶液（完全电离），满足Arrhenius公式：$\sigma_i = \frac{\left|z_i\right|^2 F^2 c_i}{RT} D_i$

> More specifically, that the electrolyte obeys the Nernst-Einstein equation, which relates the conductivity (and the electrical mobility) of an ion to its diffusion coefficient.
>
> Regardless of how carefully the experiment is set up, is that assumption of adherence to the Nernst-Einstein equation. This equation assumes that the ions do not interact with each other when they are dissolved, but this is only even approximately true in very dilute solution, for example concentrations **< 0.01 M.**

<img src="http://lacey.se/img/science/transportnumber2.png" alt="Concentration gradient in a symmetrical cell" style="zoom:25%;" />

**过程：**

1. 施加一个很小的电压时（<10mV），得到初始电流与稳态电流。
2. 测量初始与稳态之后的电阻，理想情况下会得到这样的电阻：

<img src="http://lacey.se/img/science/transportnumber4.png" alt="Impedance spectra of symmetrical cells" style="zoom:25%;" />

其中Rs为电解质的离子阻抗（ionic resistance of electrolyte），Rp为界面电阻。

此时，初始电流为 $I_0 = \frac{\Delta V}{k/\sigma + R_{p,0}}$，稳态电流为 $I_{ss} = \frac{\Delta V}{k/t_+ \sigma + R_{p,ss}}$；利用$\sigma$相等换算公式为 $t_+ = \frac{I_{ss}\left(\Delta V - I_0 R_{p,0}\right)}{I_0 \left(\Delta V - I_{ss} R_{p,ss}\right)}$。这就是**Bruce-Vincent Equation**。

> **Ref**
>
> 1. Evans, James et al. "Electrochemical Measurement Of Transference Numbers In Polymer Electrolytes". *Polymer*, vol 28, no. 13, 1987, pp. 2324-2328. *Elsevier BV*, doi:10.1016/0032-3861(87)90394-6. Accessed 22 Jan 2021.
> 2. Bruce, P., & Vincent, C. (1987). Steady state current flow in solid binary electrolyte cells. Journal Of Electroanalytical Chemistry And Interfacial Electrochemistry, 225(1-2), 1-17. doi: 10.1016/0022-0728(87)80001-3
> 3. Lacey, M. (2021). Transport and transference in battery electrolytes. Retrieved 22 January 2021, from http://lacey.se/science/transference/



对于不能完全解离的电解质，存在诸如[LiX]的中性对，抑或是[Li~2~X]^+^或[LiX~2~]^-^，先不论这些物质是否真实存在，移动一个正电荷带了两个Li^+^，所以，这些物质拥有他们自己的 t^+^，

对于此类体系，要区分 *transference number* （后文用 T）和  *transport number*（后文用t）。前者是指移动单位法拉电荷所需要的锂离子摩尔数。

> The *transference number* for lithium, for example, is defined as the **number of moles of lithium transferred *by migration* per Faraday of charge**

对于上述体系中，它们的关系为 $T_+ = t_{\text{Li}^+} + 2t_{[\text{Li}_2\text{X}]^+} - t_{[\text{LiX}_2]^-}$，其表述所有含锂物种在电解液中迁移的净transference。在理想体系中，没有ion association，*T^+^* = *t^+^*。

同样，T^+^+T^−^=1。值得一提的是T^+^或T^−^<0的过程理论上也存在。中性的[LiX]的扩散没有考虑在T^+^之中，但是其仍会扩散至低浓度区域。



注：利用实际上测定的是Bruce和Vincent称为"limiting current fraction"的参数 *F~+~*，该参数是否有意义仍在讨论。



<img src="D:\Github Repository\Mikoto\迁移数图.PNG" alt="捕获" style="zoom: 50%;" />

迁移数在论文中一个典型的图。（如果图片挂掉了，就在下面这篇文献的支持信息里找Fig.S6）

>Holoubek, J.; Liu, H.; Wu, Z.; Yin, Y.; Xing, X.; Cai, G.; Yu, S.; Zhou, H.; Pascal, T. A.; Chen, Z.; Liu, P. Tailoring Electrolyte Solvation for Li Metal Batteries Cycled at Ultra-Low Temperature. *Nature Energy* **2021**. https://doi.org/10.1038/s41560-021-00783-z.



**测量真实迁移数的方法**

**Hittorf method**

一定量的电荷通过电池，电解质被分为四部分。在聚合物电解质中更容易实现。需要装Hittorf电池。

中间两个参比区域的盐浓度需要一致。在电荷转移过程中，电场将阴离子或者阳离子迁移至电极表面，如果此过程由于在参比区域中形成的浓度梯度而使阴阳离子在过程中停了下来，那么来到电极表面的阴阳离子的转移只可能是电迁移所致的，而非扩散。

此方法不需要电解质满足一定的前提条件。可以适用于高浓。

<img src="http://lacey.se/img/science/hittorf.png" alt="Schematic of a Hittorf experiment" style="zoom:25%;" />

其计算公式为： $T_- = \frac{-\Delta \text{moles}_\text{Li} F}{Q}$。故如果能确定各区域中的盐浓度，即可计算T~+~与T~-~。

> Bruce, P., Hardgrave, M., & Vincent, C. (1992). The determination of transference numbers in solid polymer electrolytes using the Hittorf method. *Solid State Ionics*, *53-56*, 1087-1094. doi: 10.1016/0167-2738(92)90295-z



**NMR方法**

> Quantifying Mass Transport during Polarization in a Li Ion Battery Electrolyte by in Situ 7Li NMR Imaging. (2021). Retrieved 22 January 2021, from https://pubs.acs.org/doi/10.1021/ja305461j



**基于高浓溶液理论的电化学方法**（测试参数多，实验误差可能较大）

> Nitash P. Balsara and John Newman. Relationship between Steady-State Current in Symmetric Cells and Transference Number of Electrolytes Comprising Univalent and Multivalent Ions. 2015 *J. Electrochem. Soc.* 162 A2720 https://iopscience.iop.org/article/10.1149/2.0651514jes