---
{"dg-publish":true,"permalink":"/_Documents/1 Plasma Waves/","noteIcon":"default","created":"2025-12-01T13:39:24.269+08:00","updated":"2026-02-12T16:31:42.546+08:00"}
---

# 总览%
```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 2 # Include headings up to the specified level
include: 
exclude: 
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```

# 约定格式说明%
本文件后续的文献整理满足以下格式, 以方便查阅/回忆:

|           | 含义                                                                          |
| --------- | --------------------------------------------------------------------------- |
| 文件名       | 论文研究方向                                                                      |
| 一 级标题     | 论文索引和论文标题  <br>后缀：<br>- 无标记. 未读<br>- have read.已读<br>- read partially. 部分已读 |
| 一级标题后面直接跟 | 论文的基本信息，采用 JGR 引用格式(见 [[_Documents/AGU引用格式\|AGU引用格式]]).                     |
| 简述        | 论文的主要技术实现和结果.                                                               |
| 链接        | 论文的本地链接                                                                     |
| 补充        | 其他说明, 包括生词本等等                                                               |

# 1 Analytical chorus wave model derived from Van Allen Probe  observations. (have read)
Wang, D., Shprits, Y. Y., Zhelavskaya, I. S., Agapitov, O. V., Drozdov, A. Y., & Aseev, N. A. (2019). Analytical chorus wave model derived from Van Allen Probe  observations. _Journal of Geophysical Research: Space Physics_, 124, 1063–1084. https://doi.org/10.1029/2018JA026183
## 1.1 简述
开发了一个 upper-band chorus (UBC; 0.5 fce < f < fce ) and lower-band chorus (LBC; 0.05 fce < f < 0.5 fce ) waves 的均方根振幅 $B_w^2$ 和频率的多项式回归 model, 使用较低阶数的多项式实现了较高的平均相关系数 $R^2(>0.9)$ 的 model 构建.   

均方根振幅 model 是以下参数的函数: Kp 指数($\leq 6$, 单独的 scale 函数); 磁纬度 $\lambda(<20^\circ)$; 磁当地时间 MLT(分为几个扇区); 在等离子层顶之外的L shell($\in [3.5/4,6]$). 拟合形式是:  
$$
\sqrt{\langle B^2_w (MLT, L, |λ| , Kp)\rangle} = f (MLT, L, |λ|)g(Kp).
$$
$$
\begin{aligned}
f (MLT, L, |λ|) &= f (A, B, L, |λ|) \\
&=a_0 + a_1 A + a_2B + a_3 L + a_4 |\lambda| + a_5 AB + a_6 AL + a_7A |\lambda| + a_8BL \\
&\quad + a_9 B |\lambda| + a_10 L^2 + a_{11}L |\lambda| + a_{12} |\lambda|^2. \\
&here,~A=\cos\left( MLT\times \frac{\pi}{12} \right),~B=\sin\left( MLT\times \frac{\pi}{12} \right)
\end{aligned}
$$
$$
g(Kp)=\frac{{g_0(Kp)}}{\frac{1}{6} \int_0^6 {g_0(Kp)}\mathrm{d}Kp},\quad 
g_0 (Kp) = b_1Kp + b_2Kp^2 + b_3 Kp^3 + b_4 Kp^4 .
$$
频率 model 是 MLT 和 $\lambda$ 的函数, 但是仅仅区分了日侧($MLTs\in [6,18)$)和夜侧(其他 MLTs), 以及低纬度($|\lambda|<10^\circ$)和中纬度($|\lambda|\in[10^\circ, 20^\circ)$). 拟合形式是:   
$$
\begin{aligned}
B^2_w ( f ) &= c_0 + c_1f + c_2 f^2 + c_3 f^3 + c_4 f^4 + c_5 f^5 + c_6 f^6 + c_7f^7.
\\
&here,~ f ~is~ the~ frequency~ normalized~ by~ the~ equatorial ~gyrofrequency. 
\end{aligned}
$$
给出的连续函数形式可以很容易地合并到 quasi-linear diffusion models 和 particle tracing codes 当中. 文章中罗列的总结是:  
> 1. In general, upper-band chorus waves have lower amplitudes than lower-band chorus waves.
> 2. MLT dependences are different for chorus waves at midlatitude and low latitude. At low latitudes or near
the equator, chorus waves are strong on the nightside and weak on the dayside; however, at midlatitudes,
dayside chorus waves are stronger than nightside chorus waves.
> 3. L-shell dependences are different for upper-band chorus waves and lower-band chorus waves at low lat-
itudes, which may be explained by different energy sources for different bands and an upflow of warm
electrons from the ionosphere (Denton et al., 2017).
> 4. For the latitudinal dependence, the intensity of upper-band chorus waves basically decreases with latitude.
Intensity of lower-band chorus decreases with latitude on the nightside but increases with latitude on the
dayside.
> 5. The Kp dependence is separated from the dependences on geomagnetic latitude, L, and MLT as a Kp scal-
ing law. In general, the intensity of chorus waves increases with Kp. However, in those regions with L > 5,
when Kp > 4, intensities of upper-band chorus waves on all MLT sectors and lower-band chorus waves
on the afternoon sector decrease with Kp. For lower-band chorus waves, this trend may be attributed to
the enhanced convection of hot electrons during strong storms, which increase their loss to the magne-
topause. For upper-band chorus waves, this may be related to the enhanced upflow of warm electrons
in high L-shell, which decrease the temperature anisotropy of warm electrons (Denton et al., 2017). This
trend at high Kp may also be attributed to the lack of statistics. The number of measurements at high Kp
is smaller than those at low Kp.
> 6. Peak frequency of lower-band chorus waves decreases with geomagnetic latitude.
> 7. At low latitudes, the main frequency domain of lower-band chorus waves on the nightside is narrower
than that on the dayside.
> 8. Upper-band chorus waves are mainly confined at low latitudes. The peak frequency of upper band cho-
rus waves are basically the same on the dayside and nightside. However, the main frequency domain of
upper-band chorus waves on the nightside is narrower than that on the dayside.

## 1.2 链接
本地 [1.1 Wang et al. - 2019 - Analytical chorus wave model derived from Van Allen Probe  observations.pdf](/img/user/_Documents/docs/1.1%20Wang%20et%20al.%20-%202019%20-%20Analytical%20chorus%20wave%20model%20derived%20from%20Van%20Allen%20Probe%20%20observations.pdf)
## 1.3 补充
文章阅读中遇到的生词和略缩词在: [[_Documents/words/qld words- Analytical chorus wave model derived from Van Allen Probe  observations\|qld words- Analytical chorus wave model derived from Van Allen Probe  observations]]

# 2 Event-specific chorus wave and electron seed population models in DREAM 3D using the Van Allen Probes (have read)
Tu, W., G. S. Cunningham, Y. Chen, S. K. Morley, G. D. Reeves, J. B. Blake, D. N. Baker, and H. Spence (2014), Event-specific chorus wave and electron seed population models in DREAM 3 D using the Van Allen Probes, _Geophys. Res. Lett._, 41, 1359–1366, doi:10.1002/2013GL058819.
## 2.1 简述  
研究了 2012 年 10月 6-11 日的"double dip"事件. 基于简化版的 Fokker-Planck 方程(忽略了部分的交叉项 $D_{\alpha L}$ 和 $D_{pL}$):
$$   
\begin{aligned} 
\frac{\partial f}{\partial t} 
&= L^2 \frac{\partial}{\partial L} \left( \frac{D_{LL}}{L^2} \frac{\partial f}{\partial L} \right) + \frac{1}{p^2} \frac{\partial}{\partial p} \left( p^2 D_{pp} \frac{\partial f}{\partial p} \right) + \frac{1}{G} \frac{\partial}{\partial \alpha} \left( G D_{\alpha\alpha} \frac{\partial f}{\partial \alpha} \right)
\\
&\quad\quad- \frac{f}{\tau} + \frac{1}{p^2} \frac{\partial}{\partial p} \left( p^2 D_{p\alpha} \frac{\partial f}{\partial \alpha} \right) + \frac{1}{G} \frac{\partial}{\partial \alpha} \left( G D_{\alpha p} \frac{\partial f}{\partial p} \right)   
 \end{aligned}
$$
在三维(能量 E, 投掷角 $\alpha$, L shell)构建了 `DREAM 3D` 扩散模型, 上式的 p 是动量.  

> 该模型可解耦为两组方程：  
> 	1. 一组是固定磁矩 $\boldsymbol{\mu}$ (第一绝热不变量)和 $\boldsymbol{K}$ (第二绝热不变量)时的一维径向扩散方程;   
> 	2. 另一组是固定 $\boldsymbol{L^*}$ 时，作用于以投掷角 $\boldsymbol{\alpha}$ 和动量 $\boldsymbol{p}$ 为变量的相空间密度（PSD）的二维投掷角/动量扩散方程。  
> > 
> > 求解该方程需指定<font color="#ff0000">扩散系数</font>：
> > 	1. 径向扩散系数 $\boldsymbol{D_{LL}}$：是 Kp指数的函数，磁分量参考 *Brautigam and Albert (2000)*，电分量参考 *Brautigam et al. (2005)*；
> > 	2. 投掷角（$\boldsymbol{D_{\alpha\alpha}}$）、动量（$\boldsymbol{D_{pp}}$）和混合（$\boldsymbol{D_{\alpha p}}$）扩散系数：计算方法遵循 *Glauert and Horne (2005)*，利用统计波法向角分布（合唱波参考 *Li et al. (2011)*，嘶声波参考 *Agapitov et al. (2013)*），并采用与 *Tu et al. (2013)* 一致的统计等离子体密度模型。
> > 计算还需全球范围的<font color="#ff0000">波强度分布</font>（涵盖磁纬度(MLAT)、磁地方时(MLT) 和 $L$ 壳）。关于 DREAM 3 D 模型的标准设置细节，可参考 *Tu et al. (2013)*.

**边界条件**. $\boldsymbol{L_{\text{max}}}=11$ 处的外边界条件 $\frac{ \partial f }{ \partial L }=0$. 最后闭合漂移壳(LCDS)依赖于太阳风(SW)条件. 基于特定太阳风条件驱动的 TS04 模型计算显示, 90° 赤道投掷角电子的 LCDS在两次 Dst 下降期间被压缩至 L*=6 以内, 意味着可能存在强磁层顶遮蔽及 MeV 电子向外径向扩散, 而 Van Allen Probes 处于 LCDS 内部.

**全球合唱波模型**. 合声波被认为是由亚暴注入的低能电子激发的, 该模型使用多个NOAA卫星(覆盖宽范围的L和MLT)在低空测量的低能沉淀电子通量(30-100 keV)作为近赤道合声波全球分布的代表, 相比于统计模型, 该 proxy 模型可以体现事件中的 MeV 电子的强增强. 然而由于磁纬上的波分布不能用代理解析, 因此采用了统计模型中和声波的磁纬依赖关系.  

**嘶声波分布**. 来自 Tu 等\[2013\]使用的统计模型.  

考虑 径向扩散(RD) + chorus + hiss 的模型对事件的 MeV 电子的相空间密度(PSD)结果显示, 在10月8日结束时, PSD出现了一些在观测中没有出现的增强, 但这种增强远远小于10月9日观测到的主要增强. 表明辐射带电子局部加热到MeV能量不仅需要强大的波动，而且需要足够的种子群来加热.

**相对论性电子种子群**. 低能电子的动力学主要受对流和注入而不是扩散控制, 因此原模型无法重现 MeV 电子的增强, 即便存在强合唱波. 选取下边界 $\boldsymbol{E_{\text{min}} = 100 \, \text{keV}}$ 处的低能边界条件(文章称其为电子种子群 electron seed population).

## 2.2 链接
本地 [1.2 Tu et al. - 2014 - Event-specific chorus wave and electron seed population models in DREAM 3D using the Van Allen Probes.pdf](/img/user/_Documents/docs/1.2%20Tu%20et%20al.%20-%202014%20-%20Event-specific%20chorus%20wave%20and%20electron%20seed%20population%20models%20in%20DREAM%203D%20using%20the%20Van%20Allen%20Probes.pdf)
## 2.3 补充
文章阅读中遇到的生词以及**一些关键概念**在: [[_Documents/words/qld words- Event-specific chorus wave and electron seed population models in DREAM3D using the Van Allen Probes\|qld words- Event-specific chorus wave and electron seed population models in DREAM3D using the Van Allen Probes]]  

# 3 Calculation of pitch angle and energy diffusion coefficients with the PADIE code (have read)
Glauert, S. A., and R. B. Horne (2005), Calculation of pitch angle and energy diffusion coefficients with the PADIE code, _J. Geophys. Res._, 110, A04206, doi:10.1029/2004JA010851.
## 3.1 主要内容    
> **[部分摘要]**
> $\quad$ 提出了一种计算磁化冷等离子体(magnetized plasma)中共振波粒相互作用( resonant wave-particle interactions )的完全相对论性准线性投掷角和能量扩散系数(fully relativistic quasi-linear pitch angle and energy diffusion coefficients)的计算程序(PADIE).  与以往的代码不同，这里采用了完整的电磁色散关系( the full electromagnetic dispersion relation)，因此对于等离子体频率(plasma-frequency)与回旋频率(cyclotron frequency)的任何比值 $\omega_{pe}/|\Omega_e|$, 涉及以冷等离子体为主(predominantly cold plasma)的任何线性电磁波模式的相互作用(interactions involving any linear electromagnetic wave mode)都能得到处理. 
> $\quad$ 本文将该程序应用于地球辐射带(Earth's radiation belts), 以计算哨声模合声(whistler mode chorus), 电磁离子回旋波(electromagnetic ion cyclotron, EMIC)和Z模波(Z mode waves)引起的电子扩散(electron diffusion). 
> $\quad$ 1). 对于能量E ≥ 100 keV的哨声模合声引起的电子扩散, 即使 $\omega_{pe}/|\Omega_e|\approx 2$, <span style="background:#fff88f">高密度近似</span>(high-density approximation)也非常好, 但在低能(~ 10 keV)下会低估扩散达数个数量级. 
> $\quad$ 2). 当为 EMIC 引入传播波(propagating waves)的<span style="background:#fff88f">实际角展宽</span>(realistic angular spread)时, 与<span style="background:#fff88f">场向传播</span>(field-aligned propagation)的假设相比, 0.5 MeV左右的电子扩散仅略有减小; 但在5 MeV左右, 接近90°的投掷角(pitch angles)处的电子扩散小5倍, 而30°–80°的投掷角处的电子扩散增加数个数量级. 可见 EMIC 引起的散射应有助于分布函数(distribution function)的平坦化.   
> $\quad$ 3). 本文给出了Z模波引起的电子扩散的首个结果. 结果表明, 与哨声模波和电磁离子回旋波不同, 在小于45°的较宽投掷角范围内, 能量扩散(energy diffusion)超过投掷角扩散(pitch angle diffusion)(意味着 Z mode更倾向于改变电子的能量而不是运动方向). 结果表明, Z模波可能在磁暴期间对辐射带中的电子加速(electron acceleration)做出重要贡献.  

> 磁暴期间，等离子体层顶外的环境变化导致两个关键近似失效：
> $\quad$ 1. 高密度近似（因 $\omega_{pe}/\Omega_e \sim 1$，密度和磁场效应相当）；
> $\quad$ 2. 场向近似（因波法向角展宽，波不再严格沿磁场传播）。  
> 因此，理论模型必须放弃简单近似，考虑密度-磁场的平衡作用和<span style="background:#fff88f">多重共振</span>效应，才能准确描述磁暴期间的波 - 粒子相互作用.

论文的目的是展示代码 PADIE (Pitch Angle and Energy Diffusion of Ions and Electrons), 该程序计算了共振波粒相互作用的完全相对论性的俯仰角, 能量和混合的<span style="background:#fff88f">扩散系数</span>($D_{\alpha \alpha},D_{pp}, D_{\alpha p }$). 主要创新是"we include the full electromagnetic dispersion relation so that the equations are applicable to any linear wave mode in a magnetized plasma."  

### 3.1.1 当地投掷角和动量扩散系数
在相对论限制下的准线性扩散方程是:
$$
\begin{aligned} 
\frac{\partial f_0}{\partial t} 
= \nabla \cdot \left( \mathbf{D} \cdot \nabla f_0 \right) 
= \frac{1}{p \sin\alpha} \frac{\partial}{\partial \alpha} \left[ \sin\alpha \left( D_{\alpha\alpha} \frac{1}{p} \frac{\partial f_0}{\partial \alpha} + D_{\alpha p} \frac{\partial f_0}{\partial p} \right) \right] 
\\
+ \frac{1}{p^2} \frac{\partial}{\partial p} \left[ p^2 \left( D_{p\alpha} \frac{1}{p} \frac{\partial f_0}{\partial \alpha} + D_{pp} \frac{\partial f_0}{\partial p} \right) \right]
\end{aligned} 
$$
$\alpha$ 是投掷角(速度与场向夹角). 扩散系数可定义为: 
$$
\begin{aligned}
D_{\alpha\alpha} = \frac{p^2}{2} \left\langle \frac{(\Delta \alpha)^2}{\Delta t} \right\rangle
\\[6pt]
D_{\alpha p} = \frac{p}{2} \left\langle \frac{\Delta \alpha \Delta p}{\Delta t} \right\rangle 
\\[6pt]
D_{pp} = \frac{1}{2} \left\langle \frac{(\Delta p)^2}{\Delta t} \right\rangle   
\end{aligned}
$$
以上定义的所有扩散系数，单位为 $\boldsymbol{\text{动量}^2 \cdot \text{秒}^{-1}}$，这与描述辐射带动力学时常用的Fokker-Planck方程中扩散系数的定义不同 [例如，Schulz and Lanzerotti（1974），方程(2.16)，第56页]。  

波动能谱和波法角 $\psi$ 均假设为高斯分布:  
$$
\begin{aligned}
&B^2(\omega) = 
\begin{cases} 
A^2 \exp\left[ -\left( \dfrac{\omega - \omega_m}{\delta\omega} \right)^2 \right) & \omega_{\text{lc}} \leq \omega \leq \omega_{\text{uc}} 
\\[6pt]
0 & \text{otherwise},
\end{cases}
\\[12pt]&
with ~ A^2 = \frac{|B_w|^2}{\delta\omega} \frac{2}{\sqrt{\pi}} \left[ \text{erf} \left( \frac{\omega_m - \omega_{\text{lc}}}{\delta\omega} \right) + \text{erf} \left( \frac{\omega_{\text{uc}} - \omega_m}{\delta\omega} \right) \right]^{-1}
\\[25pt]&
g(X)= 
\begin{cases}
\exp\left(-\left(\frac{X - X_{m}}{X_{w}}\right)^{2}\right) & X_{\min} \leq X \leq X_{\max}\\ 0 & \text{otherwise}, 
\end{cases} 
\\[12pt]&
with~ X=\tan(\psi)
\end{aligned}
$$
扩散系数因此可以写作(推导参见 [[_Documents/references/1-3 Appendix A\|1-3 Appendix A]]):
$$
\boxed{
\begin{align}
D_{\alpha\alpha} &= \sum_{n = n_{l}}^{n_{h}} \int_{X_{\min}}^{X_{\max}} XdXD_{\alpha\alpha}^{nX} \tag{1}\\ 
D_{\alpha p} &= D_{p\alpha} = \sum_{n = n_{l}}^{n_{h}} \int_{X_{\min}}^{X_{\max}} XdXD_{\alpha p}^{nX}\tag{2}\\ 
D_{pp} &= \sum_{n = n_{l}}^{n_{h}} \int_{X_{\min}}^{X_{\max}} XdXD_{pp}^{nX}\tag{3}
\end{align} 
}
$$
其中:
$$
\begin{align}
D_{\alpha\alpha}^{nX} &= \sum_{i} \frac{q_{\sigma}^{2} \omega_{i}^{2}}{4\pi(1 + X^{2})N(\omega_{i})} \left[ \frac{n\Omega_{\sigma}/(\gamma\omega_{i}) - \sin^{2}\alpha}{\cos\alpha} \right]^{2} 
\cdot \left. B^{2}(\omega_{i})g(X) \frac{|\Phi_{n,k}|^2}{\left|v_{\parallel} - \frac{\partial\omega}{\partial k_{\parallel}}\right|}\right|_{k_{||i}}\tag4
\\
D_{\alpha p}^{nX} &= D_{\alpha\alpha}^{nX} \left[ \frac{\sin\alpha\cos\alpha}{n\Omega_{\sigma}/(\gamma\omega_{i}) - \sin^{2}\alpha} \right]_{k_{||i}} \tag5
\\
D_{pp}^{nX} &= D_{\alpha\alpha}^{nX} \left[ \frac{\sin\alpha\cos\alpha}{n\Omega_{\sigma}/(\gamma\omega_{i}) - \sin^{2}\alpha} \right]_{k_{||i}}^{2} \tag6
\end{align}
$$
$\sigma$ 是 particles' species. $i$ 的求和意味着多重共振. ${|\Phi_{n,k}|^2}$ 依赖于具体波模式的折射率(refractive index), 参见 [[_Documents/references/1-3 Appendix A\|1-3 Appendix A]]. 以及 $\omega_i$ 必须满足共振条件和色散关系:  
$$
\omega - k_{\parallel}v_{\parallel} = n\Omega_{\sigma}/\gamma 
,\quad
\mathcal{D}(k, w, X) = 0
$$
其中, 回旋频率 $\Omega_\sigma$ 含有电荷的符号. $N(\omega_i)$ 是归一化因子, 用于保证单位频率区间上波动能量为 $B^2(\omega_i)$, 一般地, 它可由色散关系给出:
$$
\boxed{
N(\omega)=\frac{1}{2\pi^{2}}\int_{X_{\min}}^{X_{\max}}\frac{g(X)k^{2}}{(1 + X^{2})^{\frac{3}{2}}}\frac{\partial \mathcal{D}}{\partial\omega}\left[\frac{\partial \mathcal{D}}{\partial k}\right]^{-1}X\mathrm{d}X
}
$$
### 3.1.2 计算方法  
#### 输入参数
- 频率分布中的参数 $B_{w}, \omega_{m}, \delta\omega, \omega_{lc}$ 和 $\omega_{uc}$;
- 波法向角分布中的 $X_{m}, X_{\min}, X_{\max}$ 和 $X_{w}$;
- 环境磁场 $B_{0}$, 等离子体密度 $n_{e}$, 离子种类数 $\sigma$, 离子成分, 波模式和共振数 $n_{l}, n_{h}$. 为了计算[[_Documents/1 Plasma Waves#弹跳平均(bounce-averaged)后的扩散系数\|#弹跳平均(bounce-averaged)后的扩散系数]]，还须指定沿磁场的密度和离子成分. 

磁场是从如下偶极子模型得到的:
$$
B=\frac{M(1 + 3\sin^{2}\lambda)^{\frac{1}{2}}}{L^{3}R_{e}^{3}\cos^{6}\lambda},
$$
其中地球磁偶极矩是 $M = 8.033454\times10^{15}\ Tm^{3}$. 文章选取 $L = 4.5$, 此处偶极子模型能很好地近似地球磁场.
#### 计算共振频率  
指定能量 $E$ 和投掷角 $\alpha$, 从
$$
E = (\gamma - 1)m_{0\sigma}c^{2}
,\quad
p = (\gamma^{2}-1)^{\frac{1}{2}}m_{0\sigma}c
$$
得到 $\gamma=(1 - v^{2}/c^{2})^{-1/2}$ 和 $p$, 从而得到 $p_{\parallel}$ 和 $p_{\perp}$. 磁化冷等离子体的色散关系由下式给出
$$
\begin{align}
\mathcal{D}(\omega,k,X) &= (SX^{2}+P)\mu^{4}-\left[ RLX^{2}+PS(2 + X^{2})\right]\mu^{2} + PRL(1 + X^{2}) = 0,
\end{align}
$$
其中 R, L, S, P 是 Stix 参数. $\mu=\frac{{c|k|}}{\omega}$ 为折射率. 用共振条件将上式的 $k_{||}$ 替换, 得到关于 $\omega$ 的多项式表达式, 对其数值求解, 只保留落在选定频域($\omega_{lc}\leq \omega \leq \omega_{uc}$)内的正实根.  
#### 数值积分  
主要是对(1)~(3)的积分.  

对于给定的频率, 可能存在一个 $X$ (~波法角)的最大值, 超过该值, 在色散关系的所需分支上没有实解. 一个例子是共振锥角, 由下式给出
$$
\tan^{2}\psi_{r}=X_{r}^{2}(\omega)=-\frac{P}{S}.
$$
方程的积分范围很可能延伸到共振锥之外, 因此必须加以限制. 实际上, 当接近共振锥时, 被积函数可能会变得非常大, 导致数值问题. 为了克服这个问题, 对于给定的频率 $\omega$, 积分是从 $X_{\min}$ 到 $\min \{X_{\max},~ \epsilon X_{r}(\omega)\}$, 选取 $\epsilon = 0.9999$.

### 3.1.3 弹跳平均(bounce-averaged)后的扩散系数
$\alpha_{eq}$ 是赤道处的投掷角, $\tau_B$ 是粒子弹跳周期. 弹跳平均后的扩散系数由[Lyons et al., 1972]给出:  
$$
\begin{align}
\langle D_{\alpha_{eq}\alpha_{eq}}\rangle&=\frac{1}{\tau_{B}}\int_{0}^{\tau_{B}}D_{\alpha\alpha}\left(\frac{\partial\alpha_{eq}}{\partial\alpha}\right)^{2}dt\\
\langle D_{\alpha_{eq}p}\rangle&=\frac{1}{\tau_{B}}\int_{0}^{\tau_{B}}D_{\alpha p}\left(\frac{\partial\alpha_{eq}}{\partial\alpha}\right)dt\\
\langle D_{pp}\rangle&=\frac{1}{\tau_{B}}\int_{0}^{\tau_{B}}D_{pp}dt
\end{align}
$$
将积分变量由时间 t 改为磁纬度 $\lambda$, 并借助磁偶极模型可得:  
$$
\begin{align}
\langle D_{\alpha_{eq}\alpha_{eq}}\rangle&=\frac{1}{T}\int_{0}^{\lambda_{m}}D_{\alpha\alpha}\frac{\cos\alpha}{\cos^{2}\alpha_{eq}}\cos^{7}\lambda d\lambda\\
\langle D_{\alpha_{eq}p}\rangle&=\frac{1}{T}\int_{0}^{\lambda_{m}}D_{\alpha p}\frac{\cos^{4}\lambda(1 + 3\sin^{2}\lambda)^{1/4}}{\cos\alpha}d\lambda\\
\langle D_{pp}\rangle&=\frac{1}{T}\int_{0}^{\lambda_{m}}D_{pp}\frac{\cos\lambda(1 + 3\sin^{3}\lambda)^{1/2}}{\cos\alpha}d\lambda
\end{align}
$$
其中, $\lambda_m$ 是磁镜反射点纬度, $T(\alpha_{eq})$ 给出 $\tau_B$ 关于 $\alpha_{e}$ 给出 $\tau_B$ 关于 $\alpha_{eq}$ 依赖关系, 在偶极场近似下, 该关系可以写作[Hamlin et al., 1961]:
$$
T(\alpha_{eq}) = 1.30 - 0.56 \sin \alpha_{eq}
$$
反射点磁纬度可以由下述多项式方程解得:  
$$
C_l^6 + (3C_l-4) \sin^4 \alpha_{eq} =0, \quad for~ C_l = \cos^2\alpha_m
$$
### 3.1.4 能量扩散系数  
能量扩散系数和混合俯仰角 - 能量扩散系数由下式计算:
$$
\boxed{
D_{EE}=\frac{c^{2}E(E + 2E_{0})}{(E + E_{0})^{2}}D_{pp}
,\quad
D_{\alpha E}=\frac{c^{2}E}{(E + E_{0})}D_{\alpha p}
}
$$
推导过程可见 [[_Documents/references/1-3 Appendix C\|1-3 Appendix C]].  
### 3.1.5 在地球辐射带的应用  
波粒相互作用对电子损失到大气层&加速有重要作用, 在此将其分为 Chorus, EMIC, Z mode 以分别研究其波粒相互作用的特性. 主要是计算了扩散系数.
#### Whistler-Mode Chorus Waves  
在磁暴期间, 电子 PSD 的峰值被观测发现位于 $L\approx 4.5$ 带, 意味着局地电子加速, Chorus 导致的能量扩散被认为对此有贡献. 文章对比了高密度近似和完全计算(full calculation)的扩散系数, 以及弹跳平均扩散系数.  

基于CRESS 卫星的观测, 选取的参数是:  
$$
\begin{array}c
\omega_m = 0.35|\Omega_e|,\quad \delta\omega = 0.15|\Omega_e|,\quad \omega_{lc} \& \omega_{uc} = \omega_m \pm 1.5 \delta\omega,\\  
X_{m} = 0.0, \quad X_{w} = 0.577 ,\quad X_{min} = 0.0 \text{ and } X_{max} = 1.0, \\
L = 4.5,\quad B_w = 100 \,\text{ pT} ,\quad n_l \& n_h = \mp5.
\end{array}
$$
关于"对比了高密度近似和完全计算(full calculation)的扩散系数", 给出的结果包括:  
1. 给出 1MeV 能量下, 两种 $\omega_{pe}/|\Omega_{e}|$ 比率对应的相关系数结果, PADIE 代码结果与高低密度近似计算结果相近. 然而 10keV (较低能量)下, 高密度近似与 PADIE 结果有差异, 前者极大低估了扩散系数.
2. $\omega_{pe}/|\Omega_{e}| = 1.5$ 时，曲线在 $\alpha_{eq} = 70^{\circ}$ 有显著峰值，由 Landau 共振引起, 其贡献在特定俯仰角范围突出.
3. 回旋共振贡献在更大俯仰角范围分布, 形成连续曲线. $\omega_{pe}/|\Omega_{e}| = 10$ 时曲线有双峰, 因n值变化 $D_{\alpha E}$ 符号多次改变导致.

关于"对比了高密度近似和弹跳平均的扩散系数", 给出的结果包括:  
1. 与上述类似, 但低估更明显. 
2. 在损失锥附近(4.6°)的俯仰角扩散和相对大俯仰角(67.8°)的能量扩散情况显示, 俯仰角扩散在 $E < 20keV$, 能量扩散在 $E < 100keV,~\omega_{pe}/|\Omega_{e}| < 2.5$ 时, 高密度近似失效. 这与共振曲线和两种情形下的色散曲线的交点有关.
3. 1 MeV 时: 高密度下, $D_{\alpha\alpha}\gg D_{\alpha E} \gg D_{EE}$; 低密度下, 扩散率更高, $D_{\alpha\alpha}\gg D_{\alpha E} \approx D_{EE}$, 混合扩散对粒子加速不可忽视.
4.  10 keV 时: 高密度下, $D_{\alpha\alpha}$ 主导; 低密度下, 损失锥附近 $D_{\alpha\alpha}\approx D_{EE}$, 能量扩散由 Landau 共振(n=0)主导, 投掷角扩散由 n=±1 回旋共振主导.
5. 要点 3 和 4 的扩散系数顺序可通过方程(6)解释: n=0 时 $D_{pp}^{nX}/D_{\alpha\alpha}^{nX}=\tan^{-2}\alpha$, 高能时 Landau 共振发生在大 $\alpha$ 处, 故 $D_{pp}^{nX} <D_{\alpha\alpha}^{nX}$; 低能时在小俯仰角, 故 $D_{pp}^{nX} > D_{\alpha\alpha}^{nX}$. 
#### EMIC Waves  
EMIC Waves 波通常被认为是 L Mode(左旋极化模)波, 是辐射带<font color="#ff0000">电子损失</font>的一个重要原因. 代码采取多离子plasma (H⁺ 85%, He⁺ 10%, O⁺ 5%), 聚焦非场向传播, 以及 n=1 回旋共振主导. 参数参考 [Summers & Thorne (2003)] : 
$$
\begin{array}c
\omega_m = 0.6 \Omega_{H^+}, \quad
\delta\omega = 0.1 \Omega_{H^+} , \quad
\omega_{lc} = \omega_m - \delta\omega , \quad 
\omega_{uc} = \omega_m + \delta\omega , \quad 
\\
\omega_{pe}^2 = 1000 \Omega_e^2 , \quad
L = 4, \quad
B_w = 100 \, \text{pT}.
\end{array}
$$
结论:  
- 扩散差异:
	- 0.5 MeV 电子: 投掷角扩散 $D_{\alpha\alpha}$ 主导, 能量扩散幅度小一个量级(可忽略). 因此 EMIC 对电子加速无贡献, 仅对损失有贡献.
	- 5 MeV 电子:
		- 场向传播假设失效. 非场向传播下: $\alpha_{eq}=80^\circ$ 附近投掷角扩散被高估, 40°~80° 扩散被低估(投掷角扩散仍占优);
		- 投掷角扩散驱动 40°~80°区间粒子投掷角分布展平.
		- 角度展宽增加并引入高次谐波, 得到40°~80°投掷角扩散率上升, 形成双峰.
#### Z Mode Waves  
Z Mode Waves 已被确定为辐射带中电子加速和损失的潜在候选者. 人们已在内磁层 [e.g., Oya, 1991] 和等离子层顶附近 [Jones et al., 1987] 观测到这类波, 其频率接近高混杂共振频率 $\omega_{UHR}​=(\omega_{pe}^2 + \Omega_e^2)^{1/2}$. 一般地, Z mode 是频谱位于 $\omega_{UHR}$ 和 L mode 的截止频率 $\omega_L = -\frac {{|\Omega_e|}} {2} + \sqrt{\frac{|\Omega_e|^2}{4} +\omega_{pe}^2}$ 之间的 X mode(非寻常模).参数设置是:  
$$
\begin{array}{c}
\omega_{m} = 0.6 |\Omega_{e}|, \quad \delta\omega = 0.05 |\Omega_{e}|, \quad \omega_{lc} = \omega_{m} - \delta\omega, \quad \omega_{uc} = \omega_{m} + \delta\omega \\
n_l\&n_h=\mp 5  \\
\omega_{pe} = 0.5 |\Omega_{e}| ,\quad L = 4.5 , \quad B_{w} = 100 \text{ pT}
\end{array}
$$
结论:  
1. 能量扩散和投掷角扩散系数大体相近.
2. 较高能量($\geq 0.3 ~\text{MeV}$)和小投掷角($\alpha<40^\circ$)时, 能量扩散主导, 意味着在小投掷角时可以<font color="#ff0000">加速电子</font>.
3. 较低能量($\approx 100 ~\text{KeV}$)和范围投掷角($\alpha\in (\approx4^\circ(\text{损失锥}), 60^\circ)$)时, 投掷角扩散主导, 意味着在低能电子会损失, 而高能电子被捕获在磁镜中.
4. n=0 朗道共振导致损失锥附近的扩散系数峰值, 其他峰来自更高阶的共振.
5. 对于 $1 ~\text{MeV}$ 电子, 小投掷角时, Z Mode 的扩散比 Chorus 高几个数量级. 在大投掷角情况下, Z Mode 的扩散与低密度(${\omega_{pe}}/|\Omega_e|=1.5$)情况下的 Chorus 相当, 超过高密度 ${\omega_{pe}}/|\Omega_e|=10$ 情况下的扩散. 表明 Z Mode 对辐射带电子加速可能很有效.
### 3.1.6 总结  
文章给出的总结是:  
> 1. A comparison of electron diffusion rates from the PADIE code and the high-density approximation for whistler mode chorus shows that the high-density approximation is remarkably good at energies E≥100 keV, even for $ω_{pe}​/∣Ω_e​∣≈2$, but breaks down at lower energies and lower densities. At low energies (∼10 keV) and low densities, pitch angle and energy diffusion rates are higher by an order of magnitude or more at small pitch angles owing to the difference in the dispersion relations at relatively large wave-normal angles and the likelihood of omitting important resonances in the high-density approximation.
> 
 > 2. Electron diffusion by EMIC waves assuming field-aligned propagation and only one dominant resonance is good at low energies (∼0.5 MeV). Increasing the angular distribution of the waves and introducing higher harmonics slightly reduces the diffusion rates. However, at higher energies (∼5 MeV), oblique propagation reduces pitch angle diffusion at large pitch angles ∼ $80^\circ$ by a factor of 5 and increases diffusion at lower pitch angles $40^\circ-80^\circ$ by orders of magnitude. As a result, EMIC waves should contribute to flattening the pitch angle distribution.
> 
>  3. We present the first calculation of electron diffusion by Z mode waves applied to the Earth's radiation belts. For Z mode waves at frequencies $ω_{pe}​<ω<∣Ω_e​∣$, energy diffusion exceeds pitch angle diffusion over broad range of pitch angles less than $45^\circ$. The dominant resonance at low pitch angles ($<40^\circ$) is the Landau n=0 resonance; higher resonances occur at larger pitch angles. Electron pitch angle scattering into the loss cone is very effective at ∼100 keV but becomes relatively ineffective at higher energies. For the same wave power, energy diffusion by Z mode waves is comparable to that of whistler mode chorus waves in the low-density region. We suggest that Z mode waves could provide a significant contribution to electron loss at ∼100 keV and acceleration up to ∼1 MeV in the radiation belts during storm times.
> 
>  4. Diffusion in energy and mixed pitch angle energy are comparable for whistler mode waves in low densities and Z mode waves. This suggests that the mixed diffusion rate could make a significant contribution to the timescale for electron acceleration and loss and should be included into global radiation belt models such as Salammbô [Beutier and Bosher, 1995].
## 3.2 链接
本地 [Glauert & Horne - 2005 - Calculation of pitch angle and energy diffusion coefficients with the PADIE code](/img/user/_Documents/docs/1.3%20Glauert%20&%20Horne%20-%202005%20-%20Calculation%20of%20pitch%20angle%20and%20energy%20diffusion%20coefficients%20with%20the%20PADIE%20code.pdf)
## 3.3 补充
 文章阅读中遇到的生词以及**一些关键概念**在在: [[_Documents/words/qld words- Calculation of pitch angle and energy diffusion coefficients with the PADIE code\|qld words- Calculation of pitch angle and energy diffusion coefficients with the PADIE code]]  

# 4 Do oblique Alfvén/ion-cyclotron or fast-mode/whistler waves dominate the dissipation of solar wind turbulence near the proton inertial length?
He, J., Tu, C., Marsch, E., & Yao, S. (2012). Do oblique Alfvén/ion-cyclotron or fast-mode/whistler waves dominate the dissipation of solar wind turbulence near the proton inertial length? _The Astrophysical Journal Letters_, 745(1), L 8. [https://doi.org/10.1088/2041-8205/745/1/L8](https://doi.org/10.1088/2041-8205/745/1/L8)












