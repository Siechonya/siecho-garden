---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/杂记/Green Function/","noteIcon":"default","created":"2025-11-19T12:10:15.473+08:00","updated":"2025-12-01T14:36:37.324+08:00"}
---

格林函数是场论中点源产生的基本解，这篇文章简单写一下它的应用。
# 1 格林函数的引入  
记 $\mathbf{L}$ 为一般的微分算符，对于形如  
$$
\mathbf{L} u(x^\sigma) = f(x^\sigma), \quad x^\sigma \in \mathbb{R}, \quad \sigma=0,1,2\dots,n
$$
的微分方程，可以写出其基本解方程为：  
$$
\mathbf{L} G(x^\sigma, x'^\sigma) = \delta^n(x^\sigma - x'^\sigma)
$$
从中得到的基本解一般称为格林函数，容易证明，  
$$
u(x^\sigma) = \int_{\mathbb{R}^n} G(x^\sigma, x'^\sigma) f(x'^\sigma) ~\mathrm{d}^nx' 
\tag{1}
$$
为原方程的解。
# 2 实例  
## 2.1 真空静电场  
静电场满足的泊松方程  
$$
\nabla^2 \varphi(\boldsymbol{x}) = - \frac{\rho(\boldsymbol{x})}{\epsilon_0}
$$
对应的格林函数满足  
$$
\nabla^2 G = \delta^3 (\boldsymbol{x} - \boldsymbol{x}')
$$
方便起见，记 ${\boldsymbol{r}} \equiv \boldsymbol{x} - \boldsymbol{x}' \equiv \bar{\boldsymbol{x}} = (\underset{x-x'}{\underbrace{\bar x}}, \bar y, \bar z)$, ${\boldsymbol{\rho}} = (\alpha, \beta, \gamma)$，上式变为 $\nabla^2 G({\boldsymbol{r}}) = \delta^3 ({\boldsymbol{r}})$，记，对上式做傅里叶变换(FT)，即  
$$
\begin{aligned} 
\tilde{G}(\alpha,\beta,\gamma) 
&= \iiint_{\mathbb{R}^3} G(\bar x, \bar y, \bar z) e^{-i(\alpha \bar x +\beta \bar y + \gamma \bar z)} \mathrm{d} \bar x \mathrm{d} \bar y \mathrm{d} \bar z
=  \iiint_{\mathbb{R}^3} G({\boldsymbol{r}}) e^{-i {\boldsymbol{\rho}}\cdot{\boldsymbol{r}}} \mathrm{d}^3 {\boldsymbol{r}}   \\[6pt]
G(\bar x, \bar y, \bar z) 
&=\frac{1}{(2\pi)^3} \iiint_{\mathbb{R}^3} \tilde{G}({\boldsymbol{r}}) e^{i(\bar x \alpha + \bar y\beta + \bar z \gamma)} \mathrm{d} \alpha \mathrm{d}\beta \mathrm{d}\gamma
=\frac{1}{(2\pi)^3} \iiint_{\mathbb{R}^3} \tilde{G}({\boldsymbol{r}}) e^{i{\boldsymbol{\rho}}\cdot{\boldsymbol{r}}} \mathrm{d}^3 {\boldsymbol{\rho}}
\end{aligned}
$$
正变换得到  
$$
-(\alpha^2 + \beta^2 + \gamma^2) \tilde{G } = 1 
\quad\Rightarrow \quad
\tilde{G } = -\frac{1}{\rho^2}, \quad \rho^2 = \alpha^2 + \beta^2 + \gamma^2
$$
于是反变换($RFT$)并采取球坐标  
$$
\theta = \langle \boldsymbol{\rho}, {\boldsymbol{r}} \rangle
,\quad
\alpha = \rho \sin\theta \cos\varphi , \quad
\beta = \rho\sin\theta \sin \varphi ,\quad
\gamma = \rho \cos\theta
$$
得到：  
$$
\begin{aligned} 
G(\bar x, \bar y, \bar z) 
&=
-\frac{1}{(2\pi)^3} \iiint_{\mathbb{R}^3} \frac{e^{i(\rho r \cos\theta)}}{\rho^2} \cdot \rho^2 \sin\theta ~\mathrm{d} {{\rho}} \mathrm{d} \theta \mathrm{d}\varphi \\[4pt]
&=
-\frac{1}{(2\pi)^2} \int_0^{+\infty} \mathrm{d}\rho\int_0^\pi {e^{i\rho r \cos\theta}} \sin\theta ~\mathrm{d} {{\rho}} \mathrm{d} \theta \\[4pt]
&=
-\frac{1}{2\pi^2 r} \int_0^{+\infty} \frac{{\sin r\rho}}{\rho} ~\mathrm{d} \rho  \\[4pt]
&=
-\frac{1}{4\pi r}
\end{aligned}
$$
于是根据式 (1) 得到势函数为
$$
\begin{aligned} 
\varphi(x,y,z) &= -\iiint_{\mathbb{R}^3} \frac{\rho(\boldsymbol{x'})}{4\pi\epsilon_0 |\boldsymbol{x} - \boldsymbol{x'}|}  \mathrm{d}x'\mathrm{d}y'\mathrm{d}z'
\end{aligned}
$$
正是熟悉的电磁势。

## 2.2 运动电荷的推迟势  
本节采用国际单位制，以及(+---)闵可夫斯基度规  
$$
\eta^{\mu\nu} = diag(1, -1,-1,-1)
$$
在选取洛伦茨规范时，从麦克斯韦方程组中可以得到非齐次波动方程：  
$$
\square^2 \varphi = \frac{\rho}{\epsilon_0},\quad \square^2 \boldsymbol{A} = \mu_0 \boldsymbol{j}
$$
$\square^2 = \frac{1}{c^2}\frac{ \partial^2  }{ \partial^2 t } - \nabla^2$ 为达朗贝尔算符。第二个方程中 $\boldsymbol{A}$ 的每个分量与 $\varphi$ 的波动方程没有什么形式上的区别，所以只需要讨论 $\square^2 \varphi = \frac{\rho}{\epsilon_0}$ 的解，该方程的格林函数满足：
$$
\left( \frac{1}{c^2}\frac{ \partial^2  }{ \partial^2 t } - \nabla^2  \right) G(x,t;x',t') = \delta(t-t')\delta^3(\boldsymbol{x}-\boldsymbol{x'})
$$
或者和 2.1 节一样简记为  
$$
\left( \frac{1}{c^2}\frac{ \partial^2  }{ \partial^2 t } - \nabla^2  \right) G(\bar{\boldsymbol{x}},\bar t) = \delta(\bar t)\delta^3(\bar{\boldsymbol{x}})
$$
做如下傅里叶变换：
$$
\begin{aligned} 
\tilde G(\boldsymbol{k},\omega) &= \int G(\bar{\boldsymbol{x}}, t) e^{-i(\boldsymbol{k}\cdot\bar{\boldsymbol{x}}-\omega t)}\mathrm{d}^3x\mathrm{d}t \\[4pt]
G(\bar{\boldsymbol{x}},\bar t) &= \frac{1}{(2\pi)^4}\int \tilde G({\boldsymbol{k}}, \omega) e^{i(\boldsymbol{k}\cdot\bar{\boldsymbol{x}}-\omega t)}\mathrm{d}^3k\mathrm{d}\omega
\end{aligned}
$$
于是由 FT 得到：  
$$
\tilde G(\boldsymbol{k},\omega) = \frac{1}{k^2 - \omega^2/c^2}
$$
接下来做 RFT：  
$$
G(\bar{\boldsymbol{x}} , \bar t) =  \frac{1}{(2\pi)^4}\int \frac{e^{i(\boldsymbol{k}\cdot\bar{\boldsymbol{x}}-\omega \bar t)}}{k^2 - \omega^2/c^2}  \mathrm{d}^3k\mathrm{d}\omega
$$
为求解该积分，采用球坐标：  
$$
\begin{array}c 
\theta = \langle \boldsymbol{k}, {\boldsymbol{r}} \rangle,\quad \boldsymbol{r} \equiv \bar{\boldsymbol{x}}
\\[6pt]
k_x= k \sin\theta \cos\varphi , \quad
k_y = k \sin\theta \sin \varphi ,\quad
k_z = k \cos\theta
\\[6pt]
\mathrm{d} k_x\mathrm{d} k_y\mathrm{d} k_z = k^2 \sin\theta \mathrm{d}k\mathrm{d}\theta \mathrm{d} \varphi
\end{array}
$$
得到  
$$
\begin{aligned} 
G(\bar{\boldsymbol{x}},t) 
&=  
\frac{1}{(2\pi)^4}
\int_0^{+\infty}     \mathrm{d} k  
\int_{\mathbb{R}}  \frac{k^2}{k^2 - \omega^2/c^2} e^{-i\omega \bar t}    \mathrm{d}\omega
\int_0^\pi \sin\theta e^{ikr\cos\theta}     \mathrm{d}\theta
\int_0^{2\pi}   \mathrm{d} \varphi
\\[6pt]
&=
\frac{1}{(2\pi)^3}
\int_0^{+\infty}     \mathrm{d} k  
\int_{\mathbb{R}}  \frac{k^2}{k^2 - \omega^2/c^2} e^{-i\omega \bar t}    \mathrm{d}\omega
\int_0^\pi  \sin\theta e^{ikr\cos\theta}     \mathrm{d}\theta
\\[6pt]
&=
\frac{1}{(2\pi)^3} 
\int_0^{+\infty}     \mathrm{d} k  
\int_{\mathbb{R}}  \frac{k^2}{k^2 - \omega^2/c^2} e^{-i\omega \bar t}\cdot \frac{1}{ikr}(e^{ikr} - e^{-ikr})    \mathrm{d}\omega
\\[6pt]
&=
\frac{ic^2}{(2\pi)^3 r} 
\int_0^{+\infty}  k(e^{ikr} - e^{-ikr})   \mathrm{d} k  
\int_{\mathbb{R}}   \frac{e^{-i\omega \bar t}}{(\omega + kc)(\omega - kc)}     \mathrm{d}\omega
\\[6pt]
&=
\frac{ic^2}{(2\pi)^3 r} 
\int_0^{+\infty}  k(e^{ikr} - e^{-ikr})   \cdot 2\pi i\left( -\frac{e^{-ikc \bar t}}{2kc} + \frac{e^{ikc \bar t}}{2kc} \right)
\mathrm{d} k  
\\[6pt]
&=
\frac{c}{8\pi^2 r} \int_0^{+\infty} \left(e^{ik(r-c \bar t)}+e^{-ik(r-c \bar t)}-e^{ik(r+c \bar t)}-e^{-ik(r+c \bar t)} \right) \mathrm{d}k
\\[6pt]
&=
\frac{c}{4\pi r} \left[ \delta(r-c \bar t) + \delta(r+c \bar t) \right] 
\\[6pt]
&=
\frac{1}{4\pi r} \left[ \delta\left( \bar t-\frac{r}{c} \right) + \delta\left( \bar t+\frac{r}{c} \right) \right] 
\end{aligned}
$$
对于 $t>0,r>0$，上式第二项恒为 0，得到  
$$
G(\bar{\boldsymbol{x}},\bar t) = \frac{1}{4\pi r} \delta\left( \bar t-\frac{r}{c} \right)
$$
记推迟时间 $t_r = t - \frac{r}{c} = \bar t - \frac{r}{c} + t'$，该时间参数与 $t'$ 无关，将有利于后面对 $t'$ 的积分。于是上式改写为  
$$
G(\boldsymbol{x}, t; \boldsymbol{x'}, t') = 
\left\{
\begin{aligned} 
&0, &t<t' ~(\bar t <0) \\[5pt]
&\frac{1}{4\pi} \frac{\delta(t'-t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|}, & t>t' ~(\bar t > 0)
\end{aligned}
\right.
$$
于是根据式 (1) 得到势函数为  
$$
\varphi(\boldsymbol{x},t) = \int \frac{\rho(\boldsymbol{x'}, t)}{\epsilon_0} \frac{1}{4\pi} \frac{\delta(t'-t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x \mathrm{d} t'
$$
得到含推迟时间的、与 2.1 节类似的势场  
$$
\varphi (\boldsymbol{x} , t) = \frac{1}{4\pi \epsilon_0} \int \frac{\rho(\boldsymbol{x'}, t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
$$
同理，矢势满足  
$$
\boldsymbol{A}(\boldsymbol{x}, t) = \frac{\mu_0}{4\pi } \int \frac{\boldsymbol{j}(\boldsymbol{x'}, t_r)}{|\boldsymbol{x}-\boldsymbol{x'}|} \mathrm{d}^3x'
$$
## 2.3 弱引力波
与前面不同，采用自然单位制，以及(-+++)闵可夫斯基度规  
$$
\eta^{\mu\nu} = diag(-1, 1,1,1)
$$
弱场条件  
$$
g_{\mu\nu} = \eta_{\mu\nu} + h_{\mu\nu} , \quad |h_{\mu\nu}|\ll1
$$
并且  
$$
\bar h_{\mu\nu} = h_{\mu\nu} - \frac{1}{2} \eta_{\mu\nu} h, \quad h = \eta^{\mu\nu}h_{\mu\nu}
$$
若采用谐和规范，弱引力场的引力波方程写作： 
$$
\square^2 \bar h_{\mu\nu} = \bar h_{\mu\nu,\alpha}^{~~~~~~,\alpha} = -16\pi GT_{\mu\nu}
$$
其中 $f_{,\alpha}^{~,\alpha} = \square^2 f$ 为达朗贝尔算符，下标为逗号表示普通微商，推导完全类似于 2.3 节，得到引力波振幅也满足推迟势公式：
$$
\bar{h}_{\mu\nu}(t, \boldsymbol{x} ) = 4G \int \frac{T_{\mu\nu}(t_r,\boldsymbol{x'})}{|\boldsymbol{x}- \boldsymbol{x'}|} \mathrm{d}^3x'
$$

## 2.4 Klein-Gorden 方程
本节采用单位制和度规与 2.3 节相同。

Klein-Gorden 方程用于描述自旋为 $0$ 的标量场，对于有源的 Klein-Gorden 方程：  
$$
(\square^2 - m^2) \psi(x^\mu) = \rho(x^\mu)
$$
对应的格林函数满足  
$$
(\partial^\mu \partial_\mu - m^2)G = \delta^4(x^\mu - x'^\mu)
$$
对上式做 FT：$\tilde{G}(p)=\int G(x) e^{-ip_\mu\bar{x}^\mu}\mathrm{d}^4\bar{x}, \ p_\mu = (-\omega, \boldsymbol{p})$ 得到：  
$$ 
( -p^\mu p_\mu - m^2 ) \tilde{G} = 1
\quad \Rightarrow \quad
\tilde{G}(\boldsymbol{p}, \omega) = \frac{1}{\omega^2-p^2-m^2}
$$
再做反变换  
$$
G(\bar{\boldsymbol{x}}, \bar t) = \frac{1}{(2\pi)^4}\int \frac{e^{i(\boldsymbol{p}\cdot \bar{\boldsymbol{x}} - \omega \bar t)}}{\omega^2-p^2-m^2} \mathrm{d}^3p\mathrm{d}\omega
$$
因为上述被积函数的奇点位于实轴，所以直接积分是发散的。常用的处理方式是费曼方法，它把积分变成：  
$$
G(\bar{\boldsymbol{x}}, \bar t) = \frac{1}{(2\pi)^4}\int \frac{e^{i(\boldsymbol{p}\cdot \boldsymbol{x} - \omega t)}}{\omega^2-p^2-m^2 - i\epsilon\omega} \mathrm{d}^3p\mathrm{d}\omega
$$
在上式中，$\epsilon$ 为小量，这使得奇点略微偏离实轴。这个积分依旧有些难处理，一个技巧是采用所谓的施温格参数化：  
$$
\frac{1}{A^n} = \frac{1}{\Gamma(n)} \int_0^{+\infty} s^{n-1} e^{-As} \mathrm{d}s
$$
选取 $iA=\omega^2-p^2-m^2 - i\epsilon\omega ,\  n=1$ 就得到：
$$
\frac{1}{\omega^2-p^2-m^2 - i\epsilon\omega} = -i\int_0^{+\infty} \mathrm{d}s ~ e^{is(\omega^2-p^2-m^2 - i\epsilon\omega)}
$$
于是格林函数变为：  
$$
\begin{aligned} 
G(\bar{\boldsymbol{x}}, \bar t)
&= 
-\frac{i}{(2\pi)^4}\int_0^{+\infty} e^{-im^2s}\mathrm{d}s \int e^{is(\omega^2-p^2)  + i(\boldsymbol{p}\cdot \bar{\boldsymbol{x} }- \omega \bar t) + \epsilon s \omega } {\mathrm{d}^3p\mathrm{d}\omega} \\[6pt]
&=
-i \int_0^{+\infty} e^{-im^2s}\mathrm{d}s \int e^{
i\left[  s\left( \omega - \frac{{\bar t+i\epsilon s}}{2s}  \right)^2 - \frac{(\bar t+i\epsilon s)^2}{4s} \right] -i\left[ s\left( \boldsymbol{p}-\frac{\bar{\boldsymbol{x}}}{2s} \right)^2 - \frac{\bar{\boldsymbol{x}}^2}{4s} \right] 
} {\frac{\mathrm{d}^3p}{(2\pi)^3} \frac{\mathrm{d}\omega}{2\pi}} \\[6pt]
&=
-i \int_0^{+\infty} e^{-im^2s}  \frac{1}{(4\pi i s)^2}e^{- i \frac{(\bar t+i\epsilon s)^2 - \bar{\boldsymbol{x}}^2}{4s}
} \mathrm{d}s \\[6pt]
&=
\frac{i}{16\pi^2} \int_0^{+\infty}  e^{- i \left(\frac{(\bar t+i\epsilon s)^2 - \bar{\boldsymbol{x}}^2}{4s} + m^2s \right)  
} \frac{\mathrm{d}s}{s^2}
\end{aligned} 
$$
记固有时  
$$
-\tau^2 = -\bar {t}^2 + \bar x^2
$$
舍去高阶小量 $\epsilon^2$，积分变为：  
$$
\begin{aligned} 
G(\bar{\boldsymbol{x}}, \bar t)
&=
\frac{i}{16\pi^2} \int_0^{+\infty}  e^{- i \left(\frac{\tau^2 }{4s} + m^2s \right) +\epsilon\bar t
} \frac{\mathrm{d}s}{s^2}  \\[6pt]
\end{aligned} 
$$
留意到这个积分和第二类修正贝塞尔函数的积分形式很类似，第二类修正贝塞尔函数是  
$$
\begin{aligned} 
K_\alpha(2\sqrt{pq}) 
&= \frac{1}{2} \left( \frac{q}{p} \right)^{\alpha/2} \int_0^{+\infty} e^{-(ps+q/s)} s^{-\alpha -1} \mathrm{d}s
\end{aligned}
$$
选取 $\alpha = 1,\ p=im^2,\ q=i\frac{\tau^2}{4}$，得到  
$$
K_1(m\tau) = \frac{\tau}{4m} \int_0^{+\infty} e^{- i \left(\frac{\tau^2 }{4s} + m^2s \right)} \frac{\mathrm{d}s}{s^2}
$$
$$
\Rightarrow \quad
G(\bar{\boldsymbol{x}}, \bar t)
=
\frac{ime^{\epsilon \bar t}}{4\pi^2 \tau} K_1(im\tau)  \\[6pt]
$$
根据解析延拓  
$$
K_1​(iz)= \frac{\pi}{2}[J_1​(z)+iN_1​(z)]
$$
最后忽略小量 $\epsilon$ 得到  
$$
G(\bar{\boldsymbol{x}}, \bar t) = i \frac{m}{8 \pi \tau } J_1(m\tau) - \frac{m}{8 \pi \tau } N_1(m\tau)
$$
该解作为费曼传播子。最终的 $\psi(x)$ 依照(1)式即可。  
# 3 补充  
## 3.1 通解和特解  
以上使用格林函数所得到的都是非齐次方程组的特解，比如对于 2.2 节的推迟势，  
$$
\square^2 \varphi = \frac{\rho}{\epsilon_0}
$$
其解为齐次通解+非齐次特解：  
$$
\varphi = \varphi_0 + \varphi_1
$$
它们分别满足  
$$
\square^2 \varphi_1 = \frac{\rho}{\epsilon_0}, \quad \square^2 \varphi_0 = 0
$$
$\varphi_0$ 显然是真空电磁波解，但格林函数解并不能退化为该电磁波解。这是因为式 (1) 实际上忽略了边界项，相当于认为边界趋于 $\infty$，且 $\lim_{ r \to \infty } \varphi=0$，该条件使得电磁波解不能存在。如果非要使用格林函数的解法还原 $\varphi_0$，则需要在(1)式中加入复杂的边界项，该边界项还和微分算符 $\mathbf{L}$ 有关。
## 3.2 Yukawa 势 
在 2.4 节中，如果场是非时变、球对称、且无源的，则克莱因-戈登方程退化为亥姆霍兹方程，即  
$$
(\nabla^2 - m^2) \psi(r) = 0
$$
则 $\psi(r) = A \frac{e^{-mr}}{r}$ 为熟知的 Yukawa 势。  



