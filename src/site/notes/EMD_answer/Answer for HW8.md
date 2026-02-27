---
{"dg-publish":true,"permalink":"/EMD_answer/Answer for HW8/","noteIcon":"default","created":"2025-12-01T13:33:10.247+08:00","updated":"2025-11-01T11:57:00.461+08:00"}
---


```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
include: 
exclude: 
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```
# 1 辐射功率交叉项   
 ![zz_figure/Pasted image 20250612113453.png](/img/user/zz_figure/Pasted%20image%2020250612113453.png)  
<font color="#ff0000">分</font>解 $\dot{\vec{\beta}}=\dot{\vec{\beta}}_{\| }+\dot{\vec{\beta}}_{\perp}$, 其中 $\dot{\vec{\beta}}_{\| } || \vec \beta$, 根据讲义的(8.148)得到:  
$$
\begin{array}{rl}
\left(\frac{d P}{ d \Omega}\right)_{cross } & \propto
\left\{\hat{e}_{R} \times\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\| }\right]\right\} \cdot\left\{\hat{e}_{R} \times\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\perp}\right]\right\} \\ 
&\downarrow~~\small {\color{grey}(\vec A\times \vec B) \cdot (\vec A\times \vec C) = A^2(\vec B\cdot \vec C) - (\vec A \cdot\vec C) (\vec A \cdot \vec B)}  \\
& =\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\| }\right] \cdot\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\perp}\right]-\left\{\hat{e}_{R} \cdot\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\perp}\right]\right\}\left\{\hat{e}_{R} \cdot\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\| }\right]\right\} \\ 
& =\left(\hat{e}_{R} × \dot{\vec{\beta}}_{\| }\right) \cdot\left[\left(\hat{e}_{R}-\vec{\beta}\right) × \dot{\vec{\beta}}_{\perp}\right] \\ 
&= \dot{\vec{\beta}}_\perp \cdot \left[(\vec e_R \times \dot{\vec{\beta}}_\|) \times (\vec e_R - \vec \beta)\right] \\
&\downarrow~~\small {\color{grey}(\vec A\times \vec B )\times \vec C = '先中间再外边'}  \\
&= \hat e_R \cdot \dot{\vec{\beta}_\perp}(\vec \beta \cdot \dot{\vec{\beta}_\|} - \hat e_R \cdot \dot{\vec{\beta}_\|})
\end{array}
$$
取 $\vec e_R = (\sin\theta\cos\varphi, \sin\theta\sin\varphi, \cos\theta)$, $\vec \beta = \beta \vec e_z$, 得到  
$$
\left(\frac{d P}{ d \Omega}\right)_{cross } \propto 
\hat{\beta}_{\parallel} (\beta - \cos \theta) \left( \hat{\beta}_{\perp x} \cos \varphi + \hat{\beta}_{\perp y} \sin \varphi \right) \sin \theta
$$
于是:  
$$
\int\left(\frac{d P}{ d \Omega}\right)_{cross } d \Omega \propto \int_{0}^{2 \pi}\left(\dot{\beta}_{\perp x} cos \varphi+\dot{\beta}_{\perp y} sin \varphi\right) d \varphi=0
$$
# 2 电子的生命周期(讲义  p154)  
![zz_figure/Pasted image 20250612113613.png](/img/user/zz_figure/Pasted%20image%2020250612113613.png)
<font color="#ff0000">加</font>速度满足:   
$$
\frac{e^{2}}{4 \pi \epsilon_{0} r^{2}}=m_{e} a_{\perp}
$$
根据拉莫公式有:  
$$
P_{\perp}=\frac{\mu_{0} e^{2}}{6 \pi c} a_{\perp}^{2}
=\frac {\mu _{0} e^{2}}{6 \pi c} \frac {e^{4}}{16 \pi ^{2} \epsilon _{0}^{2} r^{4} m_{e}^{2}}
$$
初始的能量是:  
$$
E=-\frac{1}{2} \frac{e^{2}}{4 \pi \epsilon_{0} r}
$$
有两种方式给出生命周期的估算, 第一种是:  
$$
t_1 \approx \frac{E}{P_{\perp}} \approx 10^{-11}s
$$
另一种是:  
$$
P_{\perp}(r)=-\frac{d E(r)}{ d t} = E'(r) \frac{d r}{ d t} 
\quad\longrightarrow\quad
t_2 = \int dt = \int_r^0 f(r) dr
$$
得到:  
$$
t_{2}=r_{0}^{3} \frac{4 \pi^{2} \epsilon_{0}^{2} m_{e}^{2} c^{3}}{e^{4}} \approx 10^{-11} s
$$
# 3 极相对论粒子的角最大辐射  
![zz_figure/Pasted image 20250612113626.png](/img/user/zz_figure/Pasted%20image%2020250612113626.png)
<font color="#ff0000">讲</font>义(8.133)给出:  
$$
\frac{d P}{ d \Omega}=\frac{q^{2} \mu_{0} c}{16 \pi^{2}} \frac{\dot{\beta}^{2} \sin ^{2} \theta}{(1-\beta \cos \theta)}
$$
最大辐射对应的角度由上式对 $\theta$ 的导数为 0 给出, 即:  
$$
0=\frac{d}{d \theta} \frac{\sin ^{2} \theta}{(1-\beta \cos \theta)^{5}}=\frac{\left[2 \cos \theta(1-\beta \cos \theta)-5 \beta \sin ^{2} \theta\right] \sin \theta}{(1-\beta \cos \theta)^{5}} 
$$
$$
\begin{aligned} 
\Rightarrow cos \theta &=\frac{\sqrt{1+15 \beta^{2}}-1}{3 \beta} \\
&=
\frac{1}{3} \left[ \frac{4\sqrt{1-\frac{15}{8}(1-\beta) + o(1-\beta)} - 1}{1-(1-\beta)} \right]  \\
&\downarrow~~\small {\color{grey}  1-\beta \ll 1}  \\
&=1-\frac{1-\beta}{4} \\
&= 1- \frac{\theta^2}{2} + o(\theta^3)
\end{aligned}
$$
得到:  
$$
\theta=\sqrt{\frac{1-\beta}{2}}
$$
# 4 课本题
## 4.1 零辐射的角度  
![zz_figure/Pasted image 20250612113903.png](/img/user/zz_figure/Pasted%20image%2020250612113903.png)
<font color="#ff0000">为</font>避免歧义, 将题目里面的角度 $\beta$ 记为 $\theta$, 根据讲义(8.114):  
$$
\frac{d P}{ d \Omega} \propto\left|\hat{e}_{R} \times\left[\left(\hat{e}_{R}-\vec \beta \right) \times \vec a\right]\right|^{2}
$$
假设:  
$$
\vec a = a\vec e_x
,~~
\vec \beta=\beta(\cos \alpha, \sin \alpha)
,~
\hat{e}_{R}=(\cos \theta, \sin \theta)
$$
得到:  
$$
\begin{aligned} 
\hat{e}_{R} \times\left[\left(\hat{e}_{R}-\vec \beta\right) \times \vec a\right]
&=\left(\hat{e}_{R} \cdot \vec a\right)\left(\hat{e}_{R}-\vec \beta \right)-\left[\hat{e}_{R} \cdot\left(\hat{e}_{R}-\vec \beta\right)\right] \vec a\\
&=(a\left(\beta \sin \alpha-\sin\theta \right) \sin \theta,~  a\cos\theta \left(\sin\theta -\beta \sin \alpha \right) )
=0
\\ \\
\quad&\to
\beta \sin \alpha=\sin \theta
\end{aligned}
$$
## 4.2 同步辐射  
![zz_figure/Pasted image 20250612113918.png](/img/user/zz_figure/Pasted%20image%2020250612113918.png)
<font color="#ff0000">由</font>讲义(8.155)可知:  
$$
P_{\perp} =\frac{e^{2} \mu_{0}}{6 \pi c} \frac{\gamma^{2}}{m^{2}}\left(\frac{d \vec{p}}{ d t}\right)^{2}
$$
其中:  
$$
\frac{d \vec{p}}{ d t} =e \vec{v} × \vec{B}, \quad
E =\gamma m_{e} c^{2}  = 10^{12} eV
$$
得到:  
$$
P=38~ eV \cdot s^{-1} 
$$
## 4.3 同步辐射 * 2  
![zz_figure/Pasted image 20250612113937.png](/img/user/zz_figure/Pasted%20image%2020250612113937.png)
##### (1)
根据讲义(8.164), 电子受力为辐射阻尼+洛伦兹力:  +
$$
m_e \vec{a}=\frac{\mu_{0} e^2}{6 \pi c} \dot{\vec{a}}-e \vec{v} \times \vec{B}
$$
即
$$
\dot{v}_{x}=\frac{\mu_{0} e^2}{6 \pi m_{e} c} \ddot{v}_{x}-\frac{e B}{m_{e}} v_{y} 
$$
$$
\dot{v}_{y}=\frac{\mu_{0} e}{6 \pi m_{e^2} c} \ddot{v}_{y}+\frac{e B}{m_{e}} v_{x}
$$
假定 $\tilde{v}=v_{x}+i v_{y}$, 得到  
$$
\dot{\tilde{v}}=\frac{\mu_{0} e^2}{6 \pi m_{e} c} \ddot{\tilde{v}}+i \frac{e B}{m_{e}} {\tilde{v}}
$$
这是一个常系数二阶微分方程, 其特征方程是:  
$$
\frac{\mu_{0} e}{6 \pi m_{e^2} c} \lambda^2 - \lambda+i \frac{e B}{m_{e}} = 0
$$
得到:  
$$
\begin{aligned} 
\lambda & =
\frac{{1 \pm \sqrt{1 - i \frac{e B}{m_{e}}\frac{ 2\mu_0 e^2}{3 \pi m_{e} c}}}}{ \frac{\mu_0 e^2}{3 \pi m_{e} c} }\\
&\overset{\Delta}= \frac{{1 \pm \sqrt{1 - 4i\omega_0 k}}}{2k}, \quad \left( k = \frac{\gamma}{\omega_0^2} \ll 1\right) \\
&= \frac{{1 \pm 1 \mp 2i\omega_0 k } \pm 2\omega_0^2k^2 + o(k^2)}{2k} \\
&= i\omega_0 - \gamma
\end{aligned}
$$
代入 $\tilde v = v_0 e^{\lambda t} = v_{x}+i v_{y}$, 得到:  
$$
v_x = v_0 e^{-\gamma t}\cos \omega_0 t, \quad
v_y = v_0 e^{-\gamma t}\sin \omega_0 t
$$
积分即可得到 x, y, z.  
##### (2)  
$$
\frac{ d W }{ d t} = - \frac{ d \frac{1}{2}m_e v^2 }{ d t} = -\frac{ d \frac{1}{2}m_e v_0^2 e^{-2\gamma t} }{ d t}
$$
得到  
$$
\frac{ d W }{ d t} = \gamma m_e v_0^2 e^{-2\gamma t}
$$
## 4.4 同步辐射 * 3  
![zz_figure/Pasted image 20250612113951.png](/img/user/zz_figure/Pasted%20image%2020250612113951.png)
##### (1) 
$$
P=\frac{\mu_{0} q^{2}}{6 \pi c} \frac{\gamma^{2}}{m^{2}}\left(\frac{d \vec{p}}{ d t}\right)^{2}
=\frac{\mu_{0} q^{2}}{6 \pi c} \frac{\gamma^{2}}{m^{2}} (q^{2} v^{2} B^{2})
=\frac{q^{4} B^{2}}{6 \pi \epsilon_{0} m^{2} c}\left(\gamma^{2}-1\right)
$$
##### (2)  
$$
P=-\frac{d E}{ d t}=-m c^{2} \frac{d \gamma}{d t} =\frac{q^{4} B^{2}}{6 \pi \epsilon_{0} m^{2} c}\left(\gamma^{2}-1\right)
$$
可以解得 $\gamma(t)$ , $E(t) = \gamma(t) mc^2$.
##### (3)  
对于非相对论性粒子, 有 $T= \frac{1}{2}mv^2$, 得到:  
$$
\frac{d T}{ d t}=-\frac{q^{4} B^{2}}{6 \pi \epsilon_{0} m^{2} c^{3}} v^{2}=-\frac{q^{4} B^{2}}{3 \pi \epsilon_{0} m^{3} c^{3}} T
$$
解得:  
$$
T=T_{0} exp \left[-\frac{B^{2}q^{4} }{3 \pi \epsilon_{0} m^{3} c^{3}}\left(t-t_{0}\right)\right]
$$
# 5 磁偶极辐射和电四极辐射  
![zz_figure/Pasted image 20250612114005.png](/img/user/zz_figure/Pasted%20image%2020250612114005.png)
见讲义 9.4 节.  
# 6 辐射阻尼  
![zz_figure/Pasted image 20250612114020.png](/img/user/zz_figure/Pasted%20image%2020250612114020.png)
##### (a)  
<font color="#ff0000">对</font>运动方程积分:  
$$
\int_{t-\epsilon}^{t+\epsilon} a d t=\int_{t-\epsilon}^{t+\epsilon} \tau \dot{a} d t+\int_{t-\epsilon}^{t+\epsilon} \frac{F}{m} d t
$$
当 $\varepsilon \to 0$, 由于 a 和 $\frac{F}{m}$ 是有限的, 所以左侧和右侧第二项=0, 于是右侧第一项=0:  
$$
0 = \int_{t-\epsilon}^{t+\epsilon} \tau \dot{a} d t = \tau ~ lim _{\epsilon \to 0}[a(t+\epsilon)-a(t-\epsilon)]
$$
得到 a 是连续的.   
##### (b)  
![zz_figure/Pasted image 20250612114032.png](/img/user/zz_figure/Pasted%20image%2020250612114032.png)
<font color="#ff0000">在</font> $t<0$ 时, 积分得到:  
$$
a=\tau \dot{a} \quad\Rightarrow\quad a=e^{t / \tau} a(0) 
$$
$0<t<T$时:
$$
a=\tau \dot{a}+\frac{F}{m} \quad\Rightarrow\quad a=e^{t / \tau}\left[a(0)-\frac{F}{m}\right]+\frac{F}{m}  = e^{(t-T) / \tau}\left[a(T)-\frac{F}{m}\right]+\frac{F}{m}
$$
$t>T$ 时:  
$$
a=\tau \dot{a} \quad\Rightarrow\quad a=e^{(t-T) / \tau} a(T)
$$
##### (c)  
![zz_figure/Pasted image 20250612114043.png](/img/user/zz_figure/Pasted%20image%2020250612114043.png)
<font color="#ff0000">如</font>果同时让 t < 0 和 t > T 时，a = 0, 那么 $a(T)=a(0)=0$, $0<t<T$ 时的通解将给出:  
$$
\left[0-\frac{F}{m}\right]  = e^{-T / \tau}\left[0-\frac{F}{m}\right]
$$
即 $T=0$ 这样一个平凡解.  
##### (d)  
![zz_figure/Pasted image 20250612114110.png](/img/user/zz_figure/Pasted%20image%2020250612114110.png)
<font color="#ff0000">即 </font>$a(T)=0$, 得到   
$$
\left[a(0)-\frac{F}{m}\right]  = e^{-T / \tau}\left[0-\frac{F}{m}\right]
\quad\to\quad
a(0)=\frac{F_{0}}{m}\left(1-e^{-T / \tau}\right)
$$
于是通解是:  
$$
a=
\left\{
\begin{array}l
\frac{F_{0}}{m}\left[e^{t / \tau}-e^{(t-T) / \tau}\right] , (t<0)  \\
\frac{F_{0}}{m}\left[1-e^{(t-T) / \tau}\right],  (0<t<T) \\
0, (t>T) \\
\end{array}
\right.
$$
积分得到速度:  
$$
\begin{aligned} 
v(t<0) & =0+\int_{-\infty}^{t} \frac{F_{0}}{m}\left(1-e^{-T / \tau}\right) e^{t / \tau} d t 
=\frac{F_{0} \tau}{m}\left(1-e^{-T / \tau}\right) e^{t / \tau} \\
v(0<t<T) & =\frac{F_{0} \tau}{m}\left(1-e^{-T / \tau}\right)+\int_{0}^{t} \frac{F_{0}}{m}\left[1-e^{(t-T) / \tau}\right] d t 
=\frac{F_{0} \tau}{m}\left(1-e^{(t-T) / \tau}\right)+\frac{F_{0} t}{m} 
\\
v(t>T)&=\frac{F_{0} T}{m}
\end{aligned}
$$

速度曲线示意图(所有参量均取为 1):   
  ```desmos-graph
  left=0-5; right=5;
  top=3; bottom=-3;
  ---
y=(1-e^{-1})e^x|x<0
y=(1-e^{x-1})+x|0<x<1
y=1|x>1|
  ```
加速度曲线:
```desmos-graph
left=0-5; right=5;
top=3; bottom=-3;
---
y=e^x-e^{x-1}|x<0
y=1-e^{x-1}|0<x<1
y=0|x>1
```

# 7 辐射电阻  
![zz_figure/Pasted image 20250612114122.png](/img/user/zz_figure/Pasted%20image%2020250612114122.png)
<font color="#ff0000">电</font>流是:  
$$
I=-2\frac{d q}{ d t}=2\omega q_{0} sin (\omega t)
$$
平均功率是:  
$$
< P>=\frac{1}{T} \int_{0}^{T} I^{2} R d t
= 2 \omega^{2} q_{0}^{2} R
$$
对于电偶极辐射, 讲义(9.63)给出的平均辐射功率是  
$$
< P>=\frac{\mu_{0} \omega^{4}\left(2q_{0} d\right)^{2}}{12 \pi c}
$$
令两者相等可以得到:  
$$
R=\frac{\mu_{0} \omega^{2} d^{2}}{6 \pi c}=\frac{2 \pi \mu_{0} c}{3}\left(\frac{d}{\lambda}\right)^{2} \approx 790\left(\frac{d}{\lambda}\right)^{2} \Omega
$$
对于 $f=300 kHz$ 的电磁波, 假设 $d=5 cm$ , 得到:    
$$
R \approx 2 × 10^{-6}~ \Omega
$$
# 8 电偶极子的辐射  
![zz_figure/Pasted image 20250612114137.png|750](/img/user/zz_figure/Pasted%20image%2020250612114137.png)

<font color="#ff0000">本</font>题可以视为两个在 x-y 平面以角速度 $\omega$ 匀速旋转的电荷的辐射: 
$$
\vec p = p_0 e^{-i\omega t}(\vec e_x + e^{-i\delta} \vec e_y) = \frac{\sqrt{2}}{2}p_0 e^{-i\omega t}(1 - i e^{-i\delta})\vec{e}_R + \frac{\sqrt{2}}{2}p_0 e^{-i\omega t}(1 + i e^{-i\delta})\vec{e}_L
$$
其中 $\vec{e}_R = \frac{1}{\sqrt{2}}(\vec{e}_x + i\vec{e}_y)$ 和 $\vec{e}_L = \frac{1}{\sqrt{2}}(\vec{e}_x - i\vec{e}_y)$ 分别是右圆极化和左圆极化矢量. 可以预见, 辐射的角分布是两个圆极化的叠加, 因此角分布与单个圆极化不同. 而对空间角进行积分得到的总辐射应当是与 $\delta$ 无关的(和圆极化一致).  

根据讲义(9.54)有:  
$$
\vec B = \frac{\mu_0}{4\pi c} \frac{{\ddot{\vec p} \times \vec n}}{r} e^{ikr}, \quad \vec E = c\vec B \times \vec n
$$
于是  
$$
\langle S \rangle = \frac{1}{\mu_0} <\vec E \times \vec B> = \frac{{\mu_0\vec n}}{16\pi^2 c r^2} <({\ddot{\vec p} \times \vec n})^2>
$$
上式中  
$$
\langle({\ddot{\vec p} \times \vec n})^2\rangle = <|\ddot{\vec p}|^2 - (\ddot{\vec p} \cdot \vec n)^2> = \omega^4 <|{\vec p}|^2 - ({\vec p} \cdot \vec n)^2>
$$
$$
<|{\vec p}|^2> = <p^2_0\cos^2\omega t+p^2_0\cos^2(\omega t+\delta)> = p_0^2
$$
选取 $\vec n = (\sin\theta\cos\phi, \sin\theta\sin\phi, \cos\theta)$, 得到:  
$$
\vec p​\cdot \vec n= Re(p_0​ \sin \theta e^{−iωt}[cosϕ+e^{−iδ}sinϕ])  = p_0 \sin\theta [\cos\phi \cos \omega t + \sin\phi \cos (\omega t + \delta)]
$$
$$
(\vec{p} \cdot \vec{n})^2 = p_0^2 \sin^2\theta \left[ \cos\phi \cos \omega t + \sin\phi \cos (\omega t + \delta) \right]^2
$$
$$
\begin{aligned} 
\langle (\vec{p} \cdot \vec{n})^2 \rangle 
&= p_0^2 \sin^2\theta \left\langle \cos^2\phi \cos^2 \omega t + \sin^2\phi \cos^2 (\omega t + \delta) + 2 \cos\phi \sin\phi \cos \omega t \cos (\omega t + \delta) \right\rangle \\
&= \frac{p_0^2 \sin^2\theta}{2} (1 + \sin 2\phi \cos\delta)
\end{aligned}
$$
即:  
$$
<S> = \frac{{\mu_0\vec n}}{16\pi^2 c r^2} <({\ddot{\vec p} \times \vec n})^2>
=  \frac{{\mu_0\vec n}}{32\pi^2 c r^2}(2-\sin^2\theta - \sin^2\theta\sin2\phi\cos\delta)
$$
$$
<\frac{ d P }{ d \Omega}> = <S> nr^2
$$
$$
<P> = \int <\frac{ d P }{ d \Omega}> \sin\theta\mathrm{d}\theta\mathrm{d}\phi = \frac{\mu_0\omega^4}{6\pi c}p_0^2
$$
与预期一致.  