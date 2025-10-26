---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW6/","noteIcon":"default","created":"2025-10-23T20:07:19.910+08:00","updated":"2025-10-26T13:56:30.322+08:00"}
---

前三题的解析是鞠国兴解读的教材原内容。

# 1 开普勒运动（T1, T2）
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
r = \sqrt{\frac{2 E}{m} t^2 - \frac{\alpha}{E} + \frac{M^2}{2 m E}}.
$$
为求 $\varphi$ 与时间 $t$ 的关系 $\varphi = \varphi(t)$, 先求 $r = r(\varphi)$。由式 $(2)$, 适当选取 $\varphi$ 的起始线可以使得其中的 $\text{const} = 0$, 则有
$$
\varphi = \int \frac{M \text{d} r/r^2}{\sqrt{2m \left( E + \frac{\alpha}{r^2} - \frac{M^2}{2 m r^2} \right)}} = \int \frac{- M \text{d} u}{\sqrt{2m \left[ E + \left( \alpha - \frac{M^2}{2 m} \right) u^2 \right]}}.
$$
积分的结果取决于参数的取不同值, 可以分为几种情况.  

<font color="#ff0000">a)</font> 当 $E > 0$, $\frac{M^2}{2 m} - \alpha = \beta > 0$ 时, 则式 $(2)$ 变为
$$
\varphi = - \frac{M}{\sqrt{2 m \beta}} \int \frac{\text{d} u}{\sqrt{\frac{E}{\beta} - u^2}} = \frac{M}{\sqrt{2 m \beta}} \arccos \frac{u}{\sqrt{E/\beta}},
$$
即
$$
\frac{1}{r} = u = \sqrt{\frac{E}{\beta}} \cos \left( \frac{\sqrt{2 m \beta}}{M} \varphi \right) = \sqrt{\frac{2 m E}{M^2 - 2 m \alpha}} \cos \left( \varphi \sqrt{1 - \frac{2 m \alpha}{M^2}} \right).
$$
当 $\varphi=0$ 时, $r$ 有极小值
$$
r_{\min} = \frac{M^2 - 2 m \alpha}{\sqrt{2 m E}},
$$
即 $\varphi=0$ 所在位置是近心点与力心的连线。因为 $r > 0$, 则 $\varphi$ 的取值受到限制. 当 $\cos \left( \varphi \sqrt{1 - \frac{2 m \alpha}{M^2}} \right) = 0$, 即 $\varphi = \pm \frac{\pi}{2} / \sqrt{1 - \frac{2 m \alpha}{M^2}}$ 时, $r \to \infty$, 故 $\varphi$ 的取值范围为
$$
- \frac{\pi}{2} / \sqrt{1 - \frac{2 m \alpha}{M^2}} < \varphi < \frac{\pi}{2} / \sqrt{1 - \frac{2 m \alpha}{M^2}}.
$$
这种情况下的典型轨道是螺线, 常称为 Cotes 螺线.  

```desmos-graph
r = \sec(0.05 \theta + 1)|0<\theta< 10
```
![Pasted image 20251026135622.png](/img/user/Pasted%20image%2020251026135622.png)  

<font color="#ff0000">b)</font> 当 $E > 0$, $\alpha - \frac{M^2}{2 m} = \beta > 0$ 时, 则有
$$
\varphi = - \frac{M}{\sqrt{2 m \beta}} \int \frac{\text{d} u}{\sqrt{\frac{E}{\beta} + u^2}} = - \frac{M}{\sqrt{2 m \beta}} \text{arsinh} \frac{u}{\sqrt{E/\beta}},
$$
即
$$
\frac{1}{r} = u = - \sqrt{\frac{E}{\beta}} \sinh \left( \frac{\sqrt{2 m \beta}}{M} \varphi \right) = - \sqrt{\frac{2 m E}{2 m \alpha - M^2}} \sinh \left( \varphi \sqrt{\frac{2 m \alpha}{M^2} - 1} \right).
$$
同样 $\varphi$ 的取值也受到限制以保证 $r > 0$, 这里 $\varphi < 0$ 即可.
c) 当 $E < 0$, $\alpha - \frac{M^2}{2 m} = \beta > 0$ 时, 则有
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
需要说明的是: (i) $E < 0$, $\frac{M^2}{2m} - \alpha = \beta > 0$ 这种情况需要排除, 因为这将导致重复的 $\varphi$. (ii) 在 b) 和 c) 两种情况下, 当 $|\varphi| \to \infty$ 时, 均有 $r \to 0$, 即质点可以“坠落”到力心. (iii) 本问题用 Binet 公式可以比较方便的求解, 参见本节习题 3.

本问题中质点的运动特征也可以通过有效势能进行分析. 有效势能为
$$
U_{\text{eff}} = - \frac{\alpha}{r} + \frac{M^2}{2 m r^2} = - \left( \alpha - \frac{M^2}{2 m} \frac{1}{r} \right) \frac{1}{r}.
$$
当 $\alpha - \frac{M^2}{2 m} = \beta > 0$ 时, 有效势能为负, 表现为吸引力. 因此, 质点将冲向力心运动并最终“坠落”到力心; 当 $\alpha - \frac{M^2}{2 m} < 0$ 时, 有效势能为正, 表现为相斥力, 此时有一个转折点, 可由 $E = U_{\text{eff}} = - \left( \alpha - \frac{M^2}{2 m} \right) \frac{1}{r_{\min}^2}$ 确定, 即有
$$
r_{\min} = \sqrt{\frac{M^2}{2 m} - \frac{\alpha}{E}} / \sqrt{\frac{2 m \alpha - M^2}{2 m E}}.
$$
这与式 $(3)$ 一致, 而且显然要求 $E > 0$.



