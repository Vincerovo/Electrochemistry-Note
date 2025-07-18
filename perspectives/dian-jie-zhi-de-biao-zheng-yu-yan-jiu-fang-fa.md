# 电解质的表征与研究方法

电解质的表征与研究方法

***

> _DOC INFO_:电解质的表征与研究方法 _2021/04/14_ _Last update: 2021/04/14_ _Zhong F. U.Tokyo_ _601330948@qq.com_

***

以为例，列举了电解液的研究手段。

物理化学性质

电化学研究手段

SEI formation

GC-CA holding protocol

可以使用GC-CA holding protocol（galvanostatic cycling-chronoamperometry）来研究，主要是看寄生电流 i~~p~~（parasitic current，或漏电流）的大小。【成膜之后每一圈对电解液消耗】

\_**\[Photo here]** Fig.S1-e,f **in** \_ [_nz0c02629\_si\_001.pdf (acs.org)_](https://pubs.acs.org/doi/suppl/10.1021/acsenergylett.0c02629/suppl_file/nz0c02629_si_001.pdf)

过程是：首先电极在不同的电解液中提前循环一圈成膜，然后进行5个以下循环

放电（e.g. 1C to 50mV）——CA holding（at 50mV，24h）——充电（1C到1.5V）。

其中的假设是在CA holding结束的时候，电极上没有净alkali ion的变化。定义CA holding结束时的电流为i~~p~~。

i~~p~~表征了电极上持续不断的电解质分解（由于SEI并没有完全覆盖）。i~~p~~越大，说明在passivation过程中有更多电解质分解。比较i~~p~~的大小即可说明循环过程中电解液分解量。

CA holding的作用：在维持一个低电压之后，anode处于一个满嵌的状态，表面的反应依旧还在进行，alkali ion仍在一个不停的嵌入脱出的反应之中，这一部分的电流产生就主要来源于SEI破坏与重构。倘若anode有一部分没有包覆上SEI，那么电流就会增大，达到稳态时就可以说明整体的一个SEI破坏与重构的一个程度。【个人理解】

【问题】与库伦效率的差异有何区别？

【注】用来评估early SEI formation process，not seem to directly correlate to long-term cycling stability。其中可能的一个原因是，随着电极的循环，体积膨胀，需要更多的电解液在形成SEI。

> \[ref] https://pubs.acs.org/doi/10.1021/acsenergylett.0c02629

CE——达到同一高保持率（如99%）所需要的圈数：越快越好

initial capacity loss

通过锂化电位可以说明锂化的energy barrier，一般越高的lithiation potential对应越小的energy barrier。

EIS

一个经典的SEI的电路为\_R\_~~electrolyte~~ + _Q_~~SEI~~/_R_~~SEI~~ + _Q_~~SE~~/(_R_~~SE~~ + _W_~~d~~),

_Q_~~SEI~~/_R_~~SEI~~对应经过SEI的阻抗（resistance from the charge transport across the SEI）

_Q_~~SE~~/_R_~~SE~~对应surface electron reansfer process。

_W_~~d~~对应穿过bulk电极的扩散阻抗。

可以看R~~SEI~~的EIS在循环多少圈之后稳定下来。

SEM

如果需要看电极是否有crack或者是crack free的，可以通过SEM对应EDX mapping来观察。

XPS

主要是看SEI的成分

elasticity：mechanical property：一般通过确认SEI中聚合物或者有机物的量来判断，一般也要结合表面的crack现象。
