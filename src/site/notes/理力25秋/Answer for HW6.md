---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW6/","noteIcon":"default","created":"2025-12-01T13:38:25.796+08:00","updated":"2025-11-13T21:08:38.648+08:00"}
---

前三题的解析是鞠国兴解读的教材原内容。注意，它采用了一个奇怪的记号，即用 M 来表示角动量。
# 1 T1~T3：有心力场
## 1.1 前情提要
如果作用在质点上的力的方向总是沿着质点的径矢，这样的力称为有心力。如果该力的大小仅仅与质点到固定点的距离有关，则有
$$
\mathbf{F} = - \frac{\partial U(r)}{\partial r} \mathbf{e}_r = - \frac{\text{d} U}{\text{d} r} \mathbf{e}_r
$$
在有心力场中，质点的运动位于一个固定平面内，该平面垂直于角动量 $\mathbf{M}$。采用平面极坐标，有拉格朗日函数
$$
L = \frac{m}{2} (\dot{r}^2 + r^2 \dot{\varphi}^2) - U(r)
$$
$\varphi$ 是循环坐标，且 $L$ 不显含时间，有两个运动积分，即角动量守恒和机械能守恒
$$
p_\varphi = M = m r^2 \dot{\varphi} = \text{const}
$$
$$
E = \frac{1}{2} m (\dot{r}^2 + r^2 \dot{\varphi}^2) + U(r) = \frac{1}{2} m \dot{r}^2 + \frac{1}{2} m r^2 \left(\frac{M}{m r^2}\right)^2 + U(r) = \frac{1}{2} m \dot{r}^2 + \frac{M^2}{2 m r^2} + U(r)
$$
坐标 $r$ 与时间 $t$ 的关系为
$$
t = \int \frac{\text{d} r}{\sqrt{\frac{2}{m} \left[ E - U(r) \right] - \frac{M^2}{m^2 r^2}}} + \text{const} \tag{1}
$$
运动的轨道方程为
$$
\varphi = \int \frac{(M/r^2) \text{d} r}{\sqrt{2m [E - U(r)] - M^2 / r^2}} + \text{const} = \int \frac{(M/r^2) \text{d} r}{\sqrt{2m [E - U_{\text{eff}}]}} + \text{const} \tag{2}
$$
其中
$$
U_{\text{eff}} = U(r) + \frac{M^2}{2 m r^2};
$$
称为有效势能，而 $M^2 / (2 m r^2)$ 称为离心势能。  

$\dot{r} = 0$ 或者满足条件 $U_{\text{eff}} = E$ 的点是运动轨道的转折点，即所谓的转折点方程为
$$
U(r) + \frac{M^2}{2 m r^2} = E. 
$$
根据转折点以及质点的运动范围, 可以分为有界运动和无界运动。有界运动通常有两个转折点。

对于 $r_{\min} < r < r_{\max}$ (这里 $r_{\min}, r_{\max}$ 是两个转折点与力心的距离) 的有界运动, 轨道可以是封闭的或开口的。轨道封闭的条件为
$$ 
\Delta \varphi = 2 \int_{r_{\min}}^{r_{\max}} \frac{(M/r^2) \text{d} r}{\sqrt{2m (E - U(r)) - \frac{M^2}{r^2}}}  \tag{3}
$$
等于 $2 \pi$ 的有理数倍, 即 $\Delta \varphi = \frac{2 \pi p}{q}$, 其中 $p$ 和 $q$ 是整数。仅对势能与 $\frac{1}{r}$ 或者 $r^2$ 成正比的两种有心力场, 其中有界运动的轨道是封闭的。这通常称为 Bertrand 定理。

质点可以坠落至场中心, 即 $r$ 可能趋于零的条件是
$$
[r^2 U(r)]|_{r \to 0} < - \frac{M^2}{2 m}. 
$$

## 1.2 T1
> [!T1]
>  质点在场 $U = - \alpha / r$ 内沿着抛物线运动，能量 $E=0$，试求质点坐标对时间的依赖关系。  

解：本题要求抛物线轨道相应的参数方程。由式 $(1)$ 代入 $E=0$，得
$$
t = \int \frac{r \text{d} r}{\sqrt{\frac{2\alpha}{m} r - \frac{M^2}{m^2}}}
$$
作变量代换 $r = \frac{1}{2} p (1+\eta^2)$, $p = \frac{M^2}{m \alpha^2}$, 则有 $\text{d} r = p \eta \text{d} \eta$, 于是上式可变为
$$
t = \frac{1}{2} \sqrt{\frac{m p^3}{\alpha}} \int (1+\eta^2) \text{d} \eta = \sqrt{\frac{m p^3}{\alpha}} \frac{1}{2} \eta \left( 1+ \frac{1}{3} \eta^2 \right).
$$
其实也可以直接利用积分公式 $\int \frac{x \text{d} x}{\sqrt{a x - b}} = \frac{2}{3 a} \left(  \frac{2b}{a} + x \right) \sqrt{a x - b}$ 进行求解，这样就可以得到
$$
t = \frac{m}{3 \alpha} \left( \frac{M^2}{m \alpha} + r \right) \sqrt{\frac{2 \alpha}{m} r - \frac{M^2}{m^2}}.
$$
作前述的变量变换可得与前面相同的结果。因为 $x = r \cos \varphi$，利用轨道方程 $p/r = 1 + \cos \varphi$，则有
$$
x = r \cos \varphi = p - r = p - \frac{1}{2} p (1+\eta^2) = \frac{1}{2} p (1-\eta^2).
$$
利用关系 $x^2 + y^2 = r^2$，有
$$
y = \sqrt{r^2 - x^2} = \sqrt{\left[ \frac{1}{2} p (1+\eta^2) \right]^2 - \left[ \frac{1}{2} p (1-\eta^2) \right]^2} = p \eta.
$$
注意，因为 $r$ 的取值范围是 $[0, \infty)$，则有 $-\infty < \eta < \infty$.
## 1.3 T2    
> [!info] T2
> 质点在有心力场 $U = - \alpha/r^2 \, (\alpha > 0)$ 内运动, 试求积分形式运动方程。

解：将函数代入式 $(1)$, 得
$$
\begin{aligned}
t &= \int \frac{\text{d} r}{\sqrt{\frac{2}{m} \left( E - U - \frac{M^2}{2 m r^2} \right)}} = \sqrt{\frac{m}{2}} \int \frac{\text{d} r}{\sqrt{E + \frac{\alpha}{r^2} - \frac{M^2}{2 m r^2}}} \\
&= \sqrt{\frac{m}{2}} \int \frac{r \text{d} r}{\sqrt{E r^2 + \left( \alpha - \frac{M^2}{2 m} \right)}}
= \sqrt{\frac{m}{2}} \frac{1}{E} {\sqrt{E r^2 + \alpha - \frac{M^2}{2 m}}}.
\end{aligned}
$$
这给出了 $r$ 与时间 $t$ 的关系 $r = r(t)$,
$$
r = \sqrt{\frac{2 E}{m} t^2 - \frac{\alpha}{E} + \frac{M^2}{2 m E}}
$$
为求 $\varphi$ 与时间 $t$ 的关系 $\varphi = \varphi(t)$, 先求 $r = r(\varphi)$。由式 $(2)$, 适当选取 $\varphi$ 的起始线可以使得其中的 $\text{const} = 0$, 则有
$$
\boxed{
\varphi = \int \frac{M \text{d} r/r^2}{\sqrt{2m \left( E + \frac{\alpha}{r^2} - \frac{M^2}{2 m r^2} \right)}} = \int \frac{- M \text{d} u}{\sqrt{2m \left[ E + \left( \alpha - \frac{M^2}{2 m} \right) u^2 \right]}}
}
$$
积分的结果取决于参数的取不同值, 可以分为几种情况.  

<font color="#ff0000">a)</font> 当 $E > 0$, $\frac{M^2}{2 m} - \alpha = \beta > 0$ 时, 则上式变为
$$
\varphi = - \frac{M}{\sqrt{2 m \beta}} \int \frac{\text{d} u}{\sqrt{\frac{E}{\beta} - u^2}} = \frac{M}{\sqrt{2 m \beta}} \arccos \frac{u}{\sqrt{E/\beta}},
$$
即
$$
\frac{1}{r} = u = \sqrt{\frac{E}{\beta}} \cos \left( \frac{\sqrt{2 m \beta}}{M} \varphi \right) = \sqrt{\frac{2 m E}{M^2 - 2 m \alpha}} \cos \left( \varphi \sqrt{1 - \frac{2 m \alpha}{M^2}} \right).
$$
当 $\varphi=0$ 时, $r$ 有极小值
$$
r_{\min} = \sqrt{\frac{M^2 - 2 m \alpha}{2 m E}}, \tag {i}
$$
即 $\varphi=0$ 所在位置是近心点与力心的连线。因为 $r > 0$, 则 $\varphi$ 的取值受到限制. 当 $\cos \left( \varphi \sqrt{1 - \frac{2 m \alpha}{M^2}} \right) = 0$, 即 $\varphi = \pm \frac{\pi}{2} / \sqrt{1 - \frac{2 m \alpha}{M^2}}$ 时, $r \to \infty$, 故 $\varphi$ 的取值范围为
$$
- \frac{\pi}{2} / \sqrt{1 - \frac{2 m \alpha}{M^2}} < \varphi < \frac{\pi}{2} / \sqrt{1 - \frac{2 m \alpha}{M^2}}.
$$
这种情况下的典型轨道是螺线, 常称为 Cotes 螺线。图例： 

```desmos-graph
r = \sec(0.05 \theta + 1)|0<\theta< 10
```
![zz_figure/Pasted image 20251026135622.png](/img/user/zz_figure/Pasted%20image%2020251026135622.png)  

<font color="#ff0000">b)</font> 当 $E > 0$, $\alpha - \frac{M^2}{2 m} = \beta > 0$ 时, 则有  
$$
\varphi = - \frac{M}{\sqrt{2 m \beta}} \int \frac{\text{d} u}{\sqrt{\frac{E}{\beta} + u^2}} = - \frac{M}{\sqrt{2 m \beta}} \text{arsinh} \frac{u}{\sqrt{E/\beta}},
$$
即
$$
\frac{1}{r} = u = - \sqrt{\frac{E}{\beta}} \sinh \left( \frac{\sqrt{2 m \beta}}{M} \varphi \right) = - \sqrt{\frac{2 m E}{2 m \alpha - M^2}} \sinh \left( \varphi \sqrt{\frac{2 m \alpha}{M^2} - 1} \right).
$$
同样 $\varphi$ 的取值也受到限制以保证 $r > 0$, 这里 $\varphi < 0$ 即可.  

<font color="#ff0000">c)</font> 当 $E < 0$, $\alpha - \frac{M^2}{2 m} = \beta > 0$ 时, 则有
$$
\varphi = - \frac{M}{\sqrt{2 m \beta}} \int \frac{\text{d} u}{\sqrt{u^2 - \frac{|E|}{\beta}}} = - \frac{M}{\sqrt{2 m \beta}} \text{arccosh} \frac{u}{\sqrt{|E|/\beta}},
$$
即有
$$
\frac{1}{r} = u = \sqrt{\frac{2 m |E|}{2 m \alpha - M^2}} \cosh \left( \varphi \sqrt{\frac{2 m \alpha}{M^2} - 1} \right).
$$
当 $\varphi=0$ 时, $r$ 有极大值
$$
r_{\max} = \sqrt{\frac{2 m \alpha - M^2}{2 m |E|}},
$$
即 $\varphi=0$ 所在位置是远心点与力心的连线。  

需要说明的是:  
- (i) $E < 0$, $\frac{M^2}{2m} - \alpha = \beta > 0$ 这种情况需要排除, 因为这将导致复数的 $\varphi$. 
- (ii) 在 b) 和 c) 两种情况下, 当 $|\varphi| \to \infty$ 时, 均有 $r \to 0$, 即质点可以“坠落”到力心. 
- (iii) 本问题用 Binet 公式可以比较方便的求解, 参见本节 T3.

本问题中质点的运动特征也可以通过有效势能进行分析. 有效势能为
$$
U_{\text{eff}} = - \frac{\alpha}{r} + \frac{M^2}{2 m r^2} = - \left( \alpha - \frac{M^2}{2 m} \frac{1}{r} \right) \frac{1}{r}.
$$
当 $\alpha - \frac{M^2}{2 m} = \beta > 0$ 时, 有效势能为负, 表现为吸引力. 因此, 质点将冲向力心运动并最终“坠落”到力心; 当 $\alpha - \frac{M^2}{2 m} < 0$ 时, 有效势能为正, 表现为相斥力, 此时有一个转折点, 可由 $E = U_{\text{eff}} = - \left( \alpha - \frac{M^2}{2 m} \right) \frac{1}{r_{\min}^2}$ 确定, 即有
$$
r_{\min} = \sqrt{\frac{{\frac{M^2}{2 m} - {\alpha}}}{E}} = \sqrt{\frac{ M^2 - 2 m \alpha }{2 m E}}.
$$
这与式 $(i)$ 一致, 而且显然要求 $E > 0$.
## 1.4 T3
> [!info] T3
> 在势能 $U = - \alpha/r$ 上增加一个小的修正 $\delta U$, 有限运动的轨道不再封闭, 并且每运动一圈轨道的近心点都有很小的角度改变量 $\delta \varphi$。在下面的情况下求 $\delta \varphi$：    a) $\delta U = \beta/r^2$, b) $\delta U = \gamma/r^3$.

解：根据公式 $(4)$, 当 $r$ 从 $r_{\min}$ 变到 $r_{\max}$ 再变到 $r_{\min}$ 时, 角变量 $\varphi$ 的变化量 $\Delta \varphi$, 也即相邻近心点对力心的夹角为
$$
\begin{aligned}
\Delta \varphi 
&= 2 \int_{r_{\min}}^{r_{\max}} \frac{(M/r^2) \text{d} r}{\sqrt{2m [E - U(r)] - M^2/r^2}} \\
&= - 2 \frac{\partial}{\partial M} \int_{r_{\min}}^{r_{\max}} \sqrt{2m [E - U(r)] - \frac{M^2}{r^2}} \text{d} r.
\end{aligned} \tag{ii}
$$
将 $U = - \alpha/r + \delta U$ 代入上式, 注意到 $\delta U$ 为小量, 可以对上式中的被积函数作 Taylor 展开, 并保留到 $\delta U$ 的一阶项, 有
$$
\begin{aligned}
\sqrt{2m [E - U(r)] - \frac{M^2}{r^2}} &= \sqrt{2m \left( E + \frac{\alpha}{r} - \delta U \right) - \frac{M^2}{r^2}} \\
&\approx \sqrt{2m \left( E + \frac{\alpha}{r} \right) - \frac{M^2}{r^2}} - \frac{m \delta U}{\sqrt{2m \left( E + \frac{\alpha}{r} \right) - \frac{M^2}{r^2}}}.
\end{aligned}
$$
由此式 $(\text{ii})$ 变为
$$
\Delta \varphi =
- 2 \frac{\partial}{\partial M} \int_{r_{\min}}^{r_{\max}} \sqrt{2m \left( E + \frac{\alpha}{r} \right) - \frac{M^2}{r^2}} \text{d} r 
+ \frac{\partial}{\partial M} \int_{r_{\min}}^{r_{\max}} \frac{2m \delta U \text{d} r}{\sqrt{2m \left( E + \frac{\alpha}{r} \right) - \frac{M^2}{r^2}}}.
$$
其中第一项对应于在势能为 $- \alpha/r$ 的场中质点运动轨道的相邻近心点对力心的夹角, 它等于 $2 \pi$。上式中的第二项是势场修正引起的角变量的变化, 记为 $\delta \varphi$, 即
$$
\delta \varphi = \frac{\partial}{\partial M} \int_{r_{\min}}^{r_{\max}} \frac{2 m \delta U \text{d} r}{\sqrt{2 m \left( E + \frac{\alpha}{r} \right) - \frac{M^2}{r^2}}}.
\tag{iii}
$$
利用力场未受修正时 $r$ 与 $\varphi$ 之间的关系 (参见式 $(2)$)
$$
\text{d} r = \frac{r^2}{M} \sqrt{2m \left( E - U - \frac{M^2}{2 m r^2} \right)} \text{d} \varphi = \frac{r^2}{M} \sqrt{2m \left( E + \frac{\alpha}{r} - \frac{M^2}{2 m r^2} \right)} \text{d} \varphi,
$$
则式 $(\text{iii})$ 可以改写为
$$
\boxed{
\delta \varphi = \frac{\partial}{\partial M} \left( \frac{2 m}{M} \int_{0}^{\pi} r^2 \delta U \text{d} \varphi \right)
}
\tag{iv}
$$
<font color="#ff0000">a)</font> 当 $\delta U = \beta/r^2$ 时, 则有
$$
\int_{0}^{\pi} r^2 \delta U \text{d} \varphi = \int_{0}^{\pi} r^2 \frac{\beta}{r^2} \text{d} \varphi = \beta \int_{0}^{\pi} \text{d} \varphi = \pi \beta,
$$
于是由式 $(\text{iv})$ 可得
$$
\delta \varphi = \frac{\partial}{\partial M} \left( \frac{2 m}{M} \pi \beta \right) = - \frac{2 m \pi \beta}{M^2} = - \frac{2 \pi \beta}{p \alpha}. \tag{v}
$$
对于这种情况, 势能实际上为
$$
U = - \frac{\alpha}{r} + \frac{\beta}{r^2};
$$
另外，质点在该力场中的运动是可以解析求解的。为此我们采用 Binet 公式 $\frac{\mathrm{d}^{2} u(\varphi)}{\mathrm{d} \varphi^{2}}+u=-\frac{m}{M^{2}} \frac{\mathrm{~d} U(u)}{\mathrm{d} u}$ 求解, 用 $u = 1/r$ 表示时, 有
$$
U = - \alpha u + \beta u^2.
$$
$$
\frac{\text{d}^2 u}{\text{d} \varphi^2} + u = - \frac{m}{M^2} (- \alpha + 2 \beta u),
$$
即
$$
\frac{\text{d}^2 u}{\text{d} \varphi^2} + \left( 1 + \frac{2 m \beta}{M^2} \right) u = \frac{m \alpha}{M^2}.
$$
这个方程的解为齐次方程的通解和非齐次方程的特解之和, 即
$$
u = A \cos \left( \varphi \sqrt{1 + \frac{2 m \beta}{M^2}} \right) + \frac{m \alpha}{M^2 + 2 m \beta},
$$
其中 $A$ 为积分常数, 这里选取合适的初始条件使得初位相为零, 由上式, 可得
$$
r = \frac{1}{A \cos \left( \varphi \sqrt{1 + \frac{2 m \beta}{M^2}} \right) + \frac{m \alpha}{M^2 + 2 m \beta}} =  \frac{p'}{1+ e' \cos \left( \varphi \sqrt{1 + \frac{2 m \beta}{M^2}} \right)}, \tag{vi}
$$
其中
$$
p' = \frac{M^2 + 2 m \beta}{m \alpha}, \quad e' = \frac{A (M^2 + 2 m \beta)}{m \alpha}.
$$
由式 $(\text{vi})$ 可知, 轨道是有限的, 但是, 当 $\varphi$ 从 $0$ 变到 $2 \pi$ 时, $r$ 从其极小值 $r_{\min} = \frac{p'}{1 + e'}$ 变到 $r|_{\varphi=2 \pi} \ne r|_{\varphi=0} = r_{\min}$; 不回到初始的位置, 即轨道不封闭.  

从式 $(\text{vi})$ 可知, 相邻两个近心点 (或远心点) 之间的夹角 $\Delta \varphi$ 满足关系
$$
\Delta \varphi \sqrt{1 + \frac{2 m \beta}{M^2}} = 2 \pi,
$$
即
$$
\Delta \varphi = \frac{2 \pi}{\sqrt{1 + \frac{2 m \beta}{M^2}}}.
$$
当对力场没有修正，即 $\beta = 0$ 时，这个夹角应为 $2 \pi$。可见为力势的变化导致近心角的改变为
$$
\delta \varphi = \Delta \varphi - 2 \pi = 2 \pi \left[ \frac{1}{\sqrt{1 + \frac{2 m \beta}{M^2}}} - 1 \right] \approx - \frac{2 \pi m \beta}{M^2}.
$$
其中最后一个等号是假定 $\beta$ 为小量的结果, 这与式 $(\text{v})$ 是相同的。  

<font color="#ff0000">b)</font> 当 $\delta U = \gamma/r^3$ 时, 有
$$
\begin{aligned}
\int_{0}^{\pi} r^2 \delta U \text{d} \varphi &= \int_{0}^{\pi} r^2 \frac{\gamma}{r^3} \text{d} \varphi = \gamma \int_{0}^{\pi} \frac{1}{r} \text{d} \varphi \\[8pt]
&= \frac{\gamma}{p} \int_0^\pi (1+e\cos\varphi)\mathrm{d}\varphi \\[8pt]
&= \frac{\gamma \pi}{p} = \frac{\gamma \pi m \alpha}{M^2},
\end{aligned}
$$
其中 $p=\frac{M^{2}}{m \alpha}, \ e=\sqrt{1+\frac{2 E M^{2}}{m \alpha^{2}}}$, 将其代入式 $(\text{iv})$ 可得
$$
\delta \varphi = \frac{\partial}{\partial M} \left( \frac{2 m}{M} \frac{\gamma \pi m \alpha}{M^2} \right) = - \frac{6 m^2 \alpha \gamma \pi}{M^4} = - \frac{6 \gamma \pi}{p^2 \alpha}.
$$
在这种情况下, 势能为
$$
U = - \frac{\alpha}{r} + \frac{\gamma}{r^3},
$$
相应地, 有心力为
$$
F = - \frac{\text{d} U}{\text{d} r} = - \frac{\alpha}{r^2} + \frac{3 \gamma}{r^4},
$$
其中第二项可以视为广义相对论对万有引力 (第一项) 的修正, 由此可以解释水星近日点的进动问题。在经典力学中该力场相关轨道的求解以及运动性质的讨论可参考有关文献。
# 2 T4  
记  
$$
\vec{Q} = \vec{L}\times\vec{A}= \vec{L} \times(\vec{ p}\times \vec{L} - \mu k \hat{ r}) = const \tag{1}
$$
其中  
$$
\vec{ L} \times (\vec{p} \times \vec{ L}) = \vec{ p}(\vec{ L}\cdot \vec{L }) - \vec{L} (\vec{L} \cdot \vec{ p}) = \vec{ p}L^2 = L^2 \mu \vec{v}
$$
代入(1)式可得到：  
$$
\vec{v} = \frac{\vec{Q}}{mL^2} + \frac{k}{L^2}(\vec{L}\times\hat{r})
$$
右侧第一项是常矢量，且由于 $\vec{L}\perp \hat{r}$，右侧第二项的模长恒为 $\frac{k}{L}$。显然，第一项就是原点偏离圆心的大小，第二项就是速度图的半径大小。  
# 3 T5： 选做题  
## 3.1 (a)  
选取坐标参数如下：  
![zz_figure/Pasted image 20251026155032.png](/img/user/zz_figure/Pasted%20image%2020251026155032.png)  

$m_3$ 在静止系中的速度是  
$$
\vec{v} = \vec{v'} + \vec \omega \times \vec{r} = (\dot{x}, \dot{y}) + \vec{\omega} \times (x,y)
$$
于是拉氏量是  
$$
\begin{aligned} 
L &= \frac{1}{2}m_3|\vec{v'} + \vec \omega \times \vec{r}|^2 - V ,
&V = -\frac{Gm_1m_3}{r_{13}} - \frac{Gm_2m_3}{r_{23}}
\\[4pt]
&=
\frac{1}{2}m_3 v'^2 + m_3 \vec{v'}\cdot (\vec \omega \times \vec{r}) - V_{eff},
&V_{eff}= V-\frac{1}{2}m_3|\vec \omega \times \vec{r}|^2 \\[4pt]
&=
\frac{1}{2}m_3(\dot{x}^2 + \dot{y}^2) + m_3\omega(x\dot{y}-y\dot{x})
\end{aligned}
$$
代入拉格朗日方程得到 $m_3$ 的运动方程：  
$$
\begin{aligned} 
m_3 \ddot{x} - 2m_3\omega\dot{y} = -\frac{ \partial V_{eff} }{ \partial x }\\[4pt]
m_3 \ddot{y} + 2m_3\omega\dot{x} = -\frac{ \partial V_{eff} }{ \partial y }
\end{aligned}
$$
显然上式第二项就是科里奥利力。对于平衡点，要求 $\dot{\vec{r}} = \ddot{\vec{r}} = 0$，即上式左侧为 0，即  
$$
\begin{align}
0&=\frac{1}{m_3}\frac{\partial v_{\mathrm{eff}}}{\partial x}
=G m_{1}  \frac{x+a\mu /m_{1}}{r_{13}^{3}}+G m_{2}  \frac{x-a \mu / m_{2}}{r_{23}^{3}}- \omega^{2} x \tag{1} \\[6pt]
0&=\frac{1}{m_3}\frac{\partial V_{\mathrm{eff}}}{\partial y}
=G m_{1}  \frac{y}{r_{13}^{3}}+G m_{2}  \frac{y}{r_{23}^{3}}- \omega^{2} y . \tag{2}
\end{align}
$$
<font color="#ff0000">i)</font> 若 $y\neq0$，(2)就意味着：
$$
G  \frac{m_{1} }{r_{13}^{3}}+G  \frac{m_{2} }{r_{23}^{3}} =  \omega^{2}
$$
代入(1)消去 $r_{13}$ 或 $r_{23}$ 就得到：  
$$
\omega^2 =  \frac{G(m_1+m_2)}{r_{13}^3} =  \frac{G(m_1+m_2)}{r_{23}^3}
$$
与 $\omega^2 = \frac{G(m_1+m_2)}{a^3}$ 对比可知  
$$
r_{13} = r_{23} = a
$$
也就是 $m_1,m_2,m_3$ 构成等边三角形，对应的解就是下图的 $L_4$ 和 $L_5$。
![zz_figure/Pasted image 20251026154032.jpg](/img/user/zz_figure/Pasted%20image%2020251026154032.jpg)
<font color="#ff0000">ii)</font> 若 $y=0$，(1)式就简化为  
$$
G m_{1}  \frac{x+a\mu /m_{1}}{|x-a \mu / m_{1}|^{3}}+G m_{2}  \frac{x-a \mu / m_{2}}{|x-a \mu / m_{2}|^{3}}- \omega^{2} x = 0
$$
该方程没有解析解，只能用数值方法去逼近，它有三个解，对应于上图的 $L_1,L_2,L_3$。当然，在限制性三体问题中 $(m_3\ll m_2 \ll m_1)$，上式有近似解，就比如常见的日-地-月三者，就构成一个这样的限制性三体系统。

## 3.2 (b) 
这道题没有给定参数的具体值，所以同学们可以任取(比如 $m_1=m_2=m_3=1$)。这里就以地-月-卫星系统为例，因为它是限制性三体系统，所以  
$$
\left\{
\begin{aligned} 
&x_{L_1} = R - R\left( \frac{m_2}{m_2 + 3m_1} \right)^{1/3} \approx 0.84R \approx 3.2\times 10^5 km \\
&x_{L_2} = R + R\left( \frac{m_2}{m_2 + 3m_1} \right)^{1/3} \approx 1.16R \approx 4.5\times 10^5 km \\
&x_{L_3} = -R + R\left(  \frac{7m_2}{5m_2 + 12 m_1} \right) \approx -0.99 R \approx - 3.85\times 10^5 km \\
&\vec r_{L_4},\vec r_{L_5}  = \left( \frac{1}{2}R, \ \pm \frac{\sqrt{3}}{2}R \right) \approx (1.96, \pm 3.39) \times 10^5 km
\end{aligned}
\right.
$$
对应的绘图如下:
![zz_figure/Pasted image 20250507090227.png](/img/user/zz_figure/Pasted%20image%2020250507090227.png)
至于题目中的等势面，描述的其实就是相对于旋转系的速度为 0 的零速度面，我们一般称之为 Hill 曲面。它对应的表达式是(这里还是采用和第一问一样的，以质心为原点，而不是题目中以 $m_1$ 为原点)：  
$$
\frac{1}{m_3}V_{eff} = -\frac{1}{2}\omega^2(x^2 + y^2)  -\frac{Gm_1}{r_{13}} - \frac{Gm_2}{r_{23}} \equiv C
$$
绘制这个图对 C 的精度要求比较高，画出来是
![zz_figure/Pasted image 20250507092214.png](/img/user/zz_figure/Pasted%20image%2020250507092214.png)
# Appendix 代码 %
上面两幅图用 python 绘制，代码是  

```python
# 绘制拉格朗日点
import numpy as np
import matplotlib.pyplot as plt

# 相对质量
earth_mass = 1.0
moon_mass = 7.342e22/(5.972e24)
R = 1.0   # 地月距离(归一化)

earth_position = np.array([0.0, 0.0])
moon_position = np.array([R, 0.0])
lagrange_points = [
    {"name": "L1", "position": np.array([0.84, 0.0])},
    {"name": "L2", "position": np.array([1.16, 0.0])},
    {"name": "L3", "position": np.array([-1.0, 0.0])},
    {"name": "L4", "position": np.array([0.5, np.sqrt(3)/2])},
    {"name": "L5", "position": np.array([0.5, -np.sqrt(3)/2])},
]

plt.figure(figsize=(8, 8))
plt.scatter(earth_position[0], earth_position[1], color='blue', s=100, label='Earth')
plt.scatter(moon_position[0], moon_position[1], color='gray', s=30, label='Moon')

for point in lagrange_points:
    plt.scatter(point["position"][0], point["position"][1], color='red', marker='x', s=50)
    plt.text(point["position"][0], point["position"][1], point["name"], fontsize=12, ha='right')
# 绘制月球轨道
theta = np.linspace(0, 2*np.pi, 100)
r = R * np.ones_like(theta)
plt.plot(r * np.cos(theta), r * np.sin(theta), color='gray', linestyle='-', label='Moon Orbit') # ecc=0.055忽略

plt.title('Lagrange Points', fontsize=16)
plt.xlabel('X (Normalized)', fontsize=12)
plt.ylabel('Y (Normalized)', fontsize=12)
plt.legend()
plt.grid(True)
plt.axhline(0, color='black', linewidth=0.5, linestyle='--')
plt.axvline(0, color='black', linewidth=0.5, linestyle='--')
plt.xlim(-1.5, 1.5)
plt.ylim(-1.5, 1.5)
plt.show()
```


```python
# 绘制希尔曲线族
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import cm
from mpl_toolkits.mplot3d import Axes3D

G = 6.6743e-11  # m^3 kg^-1 s^-2
M = 5.972e24     # kg
m = 7.342e22     # kg
mu_1 = 398600   # km^3/s^2
mu_2 = 4903.02  # km^3/s^2
R = 3.844e5      # km
omega = np.sqrt((mu_1 + mu_2) / (R**3))  # 月球绕地球的角速度

# 网格
x = np.linspace(-6e5, 6e5, 20000)
y = np.linspace(-6e5, 6e5, 20000)
z = np.array([0])
x, y, z = np.meshgrid(x, y, z, indexing='ij')

earth_x = (m / (M + m)) * R # 假设地月质心在原点
moon_x = -(M / (M + m)) * R

# spacecraft 到地球和月球的距离
r_e = np.sqrt((x - earth_x)**2 + (y)**2 + (z)**2)
r_m = np.sqrt((x - moon_x)**2 + (y)**2 + (z)**2)
C_jacobi = 2 * mu_1 / r_e + 2 * mu_2 / r_m + omega**2 * (x**2 + y**2)  # 计算势能

def plot(C, ax):
    # 绘制希尔曲面
    mask = (C_jacobi < C) & (C_jacobi > C-0.001)
    print(f"num of points: {np.sum(mask)}")
    ax.scatter(x[mask], y[mask], marker='.', s=10, alpha=1, label=f"C={C}")

    # 设置坐标轴标签等
    ax.set_xlabel('X(km)')
    ax.set_ylabel('Y(km)')
    ax.ticklabel_format(style='sci', scilimits=(0,0), axis='both')

fig, ax = plt.subplots(figsize=(12, 12))
for i, C in enumerate([3.500, 3.343, 3.338, 3.326, 3.300, 3.159, 3.150, 3.135]):
    print(f"C={C}")
    plot(C, ax=ax)
    
plt.legend()
# plt.tight_layout()
plt.show()
```


