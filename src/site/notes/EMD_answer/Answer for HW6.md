---
{"dg-publish":true,"permalink":"/EMD_answer/Answer for HW6/","created":"2025-05-21T20:09:17.112+08:00"}
---


```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```


# 1. 1D 电磁波解    
- <font color="#00b0f0">(a) 平面波动方程:</font>
$$
\left(\frac{1}{c^{2}} \frac{\partial^{2}}{\partial t^{2}}-\frac{\partial^{2}}{\partial x^{2}}\right) \varphi=\left(\frac{1}{c} \frac{\partial}{\partial t}+\frac{\partial}{\partial x}\right)\left(\frac{1}{c} \frac{\partial}{\partial t}-\frac{\partial}{\partial x}\right) \varphi=0
$$
$$
令\  v=\left(\frac{1}{c} \frac{\partial}{\partial t}-\frac{\partial}{\partial x}\right) \varphi \to \left\{\begin{array}{l}\left(\frac{1}{c} \frac{\partial}{\partial t}+\frac{\partial}{\partial x}\right) v=0 \\ \left(\frac{1}{c} \frac{\partial}{\partial t}-\frac{\partial}{\partial x}\right) \varphi=0\end{array} \quad\right. \to  \quad  特征方程: \left\{\begin{array}{l}c d t=d x \\ c d t=-d x\end{array} \Rightarrow\left\{\begin{array}{l}\xi=x-c t \\ \eta=x+c t\end{array}\right.\right.
$$
$\Rightarrow$  原方程的解为:  
$$
\left.\begin{array}{l}\frac{\partial \psi}{\partial \xi}=0 \\ \frac{\partial \varphi}{\partial \eta}=0\end{array}\right\} \Rightarrow  \frac{\partial^{2} \varphi }{\partial \xi \partial \eta}=0 
\Rightarrow
\varphi(x, t)=\underbrace{f(x-c t)}_{\text {右行波 }}+\underbrace{g(x+c t)}_{\text {右行波 }}
$$
- <font color="#00b0f0">(b) 球面波动方程:</font>
$$
\frac{1}{c^{2}} \frac{\partial^{2}}{\partial t^{2}} \varphi=\Delta_{3} \varphi=\left(\frac{\partial^{2}}{\partial r^{2}}+\frac{2}{r} \frac{\partial}{\partial r}\right) \varphi
$$
设  $\varphi=\frac{1}{r} u(r, t)$ 代入上式得:  
$$
\left(\frac{1}{c^{2}} \frac{\partial^{2}}{\partial t^{2}}-\frac{\partial^{2}}{\partial r^{2}}\right) u=0
\varphi(r, t)=\frac{1}{r}[\underbrace{f(t-r / c}_{\text {会聚波 }})+\underbrace{g(t+r / c)}_{\text {发散波 }}]
$$  
对于源，会聚波可略去.
# 2. 反常色散
此时 $n_{r}-1=  Const  \cdot \frac{\omega_{0}^{2}-\omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+(\omega \gamma)^{2}}=  Const  \cdot f(\omega)$ :
$$  
\begin{aligned}
f^{\prime}(\omega)&=-2 \omega\left[\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+(\omega \gamma)^{2}\right]+\left(\omega^{2}-\omega_{0}^{2}\right)\left[2\left(\omega_{0}^{2}-\omega^{2}\right)(-2 \omega)+2 \gamma^{2} \omega\right] /  \tiny{没用的分母}^{2} \\
&=2 \omega\left[\left(\omega_{0}^{2}-\omega^{2}\right)^{2}-\omega_{0}^{2} \gamma^{2}\right] /  \tiny{没用的分母}^{2}
\end{aligned}
$$
 
对于 $f^{\prime}\left(\omega_{1}\right)=f^{\prime}\left(\omega_{2}\right)=0$:  
$$
\begin{aligned} 
\left|\omega_{1}-\omega_{2}\right|
&=\left(\omega_{0}^{2}+\omega_{0} r\right)^{1 / 2}-\left(\omega_{0}^{2}-\omega_{0} r\right)^{1 / 2} \\
&=\omega_{0}\left(1+\frac{\gamma}{\omega_{0}}\right)^{1 / 2}-\omega_{0}\left(1-\frac{\gamma}{\omega_{0}}\right)^{1 / 2} \approx {\gamma} \quad\left(\text { 当 } \gamma \ll \omega_{0} \text { 时 }\right)
\end{aligned}
$$
# 3. 介质边界的电磁波
- <font color="#00b0f0">(a)</font> 假设 xoz 为入射面. 设入射波 $\left\{\begin{array}{l}\vec{B}=B_{0} \vec{e}_{y}+0 \cdot \vec{e}_{x} \\ \vec{E}=E_{0} \vec{e}_{x}+0 \cdot \vec{e}_{y} \end{array}\right.$,  反射波 $E_{R}=\left(E_{R x}, E_{R y}\right)$, 透射波 $E_{T}=\left(E_{T x}, E_{T y}\right)$.

由 $\nabla \times E=-\frac{\partial B}{\partial t}$ 和 $\nabla \times \frac{B}{\mu}=\frac{\partial \varepsilon E}{\partial t} k_{0}, \ \vec{B}=\frac{\vec{n}}{c} \times \vec{E}=\sqrt{\mu \varepsilon} \hat{h} \times \vec{E}$ 得到如下边界条件:  
$$
\begin{aligned} 
\quad E_{0}+E_{R x}&=E_{T x} \\
0+E_{R y}&=E_{T y} \\
\frac{0+B_{R x}}{\mu}&=\frac{B_{T x}}{\mu^{\prime}}  \\
\frac{B_{0}+B_{R y}}{\mu}&=B_{T y} / \mu^{\prime} \\
\sqrt{\frac{\varepsilon}{\mu}} E_{R y}&=\sqrt{\frac{\varepsilon \prime}{\mu^{\prime}}} E_{T y}
\end{aligned}
$$
由第二式和最后一式可知 $E_{R y}=0, E_{T y}=0$.

- <font color="#00b0f0">(b)</font> 此时三支波均只有y分量, 有：
$$
\nabla \times E=-\frac{\partial B}{\partial t}<+\infty \quad\Rightarrow\quad  E_{0}+E_{R}=E_{T}
$$
以及 $\nabla \times \frac{B}{\mu} =\frac{\partial \varepsilon E}{\partial t}<+\infty$ 和 $\vec{B}=\sqrt{\mu \varepsilon} \hat{n} \times \vec{E}$ :
$$
\Rightarrow \sqrt{\frac{\varepsilon}{\mu}} E_{0} \cos \theta_{I}-\sqrt{\frac{\varepsilon}{\mu}} E_{R} \cos \theta_{I}=\sqrt{\frac{\varepsilon^{\prime}}{\mu^{\prime}}} E_{T} \cos \theta_{I I}
$$
上述两式结合 $\frac{\sin \theta_{II}}{\sin \theta_{I}}=\frac{n_{II}}{n_{I}}$ 得到:
$$
\left\{\begin{aligned}
\frac{E_{I}}{E_{0}}&=\frac{{2 n_{I} \cos \theta_{I}}}{n_{I} \cos \theta_{I}+\frac{\mu}{\mu^{\prime}} \sqrt{n_{II}^{2}-n_{I}^{2} \sin ^{2} \theta_{I}}} \\
\frac{E_{I}}{E_{0}}&=\frac{{n_{I} \cos \theta_{I}-\frac{\mu}{\mu^{\prime}} \sqrt{n_{I I}^{2}-n_{I}^{2} \sin ^{2} \theta_{I}}}}{n_{I} \cos \theta_{I}+\frac{\mu}{\mu^{\prime}} \sqrt{n_{I I}^{2}-n_{I}^{2} \sin ^{2} \theta_{I}}}
\end{aligned}\right.
$$
# 4. TM 模
假设方形波导管的轴向是 z 方向, 波动方程是:  
$$
\left( \frac{ \partial^2  }{ \partial^2 x }  + \frac{ \partial^2  }{ \partial^2 y } + (\mu\epsilon\omega^2 - k^2)\right) E_z = 0
$$
边界条件是 $\vec E^{||} = 0$:  
$$
\left\{
\begin{aligned} 
E_z = E_y = 0 \quad at\ x=0,a\\
E_z = E_x = 0 \quad at\ y=0,b
\end{aligned}
\right.
$$
通过分离变量 $E_z = X(x)Y(y)$, 得到:  
$$
E_z = E_0\sin{\frac{m\pi x}{a}}\sin{\frac{n\pi y}{b}}
$$
给出的截止频率在 $k=0$ 时取得, 它是:  
$$
\omega_{mn} = \pi c \sqrt{\frac{m^2}{a^2} + \frac{n^2}{b^2}}
$$
注意, 如果 $m=0\ or\ n=0$ 会使得 $E_z = 0$, 波模不存在. 所以对应的最低截止频率是 $\omega_{11}$.
# 5. 课本题  
## 1. 窄带双色波  
- <font color="#00b0f0">(1)</font> 
$$
\begin{array}{l}
\vec{A}
&=\vec{A}_{0}\left[e^{i(k x-\omega t+d k x-d \omega t)}+e^{i(k x-\omega t-d k x+d \omega t)}\right] \\ 
&=\vec{A}_{0} e^{i(k x-\omega t)}\left[e^{d k x-i d \omega t}+\overline{e^{d k x-i d \omega t}}\right] \\
&=2 \vec{A}_{0} \cos (d k \cdot x-d \omega\cdot  t) e^{i(k x-\omega t)}
\end{array}
$$
- <font color="#00b0f0">(2)</font> 从相速度对应于等相位面 $e^{i(k x-\omega t)}=const.$ , 以及群速度对应波包面 $\cos (d k \cdot x-d \omega\cdot  t)=const.$ 得到:
$$
\nu_{\text {phase }}=\omega / k, \nu_{\text {group }}=d \omega / d k 
$$
## 4. 各向异性介质
- <font color="#00b0f0">(1)</font> 对于 $\rho_{f}=J_{f}=0$ 的线性磁介质:
$$   
\nabla \cdot B=0 \Rightarrow \vec{k} \cdot \vec{B}=0
$$
$$
\nabla \cdot \vec{D}=\epsilon\nabla \cdot \vec E + \vec E\cdot \nabla \epsilon = 0 \Rightarrow k \cdot \vec{D}=0 \quad(  \nabla \epsilon \neq 0 \Rightarrow \nabla \cdot \vec E \neq 0 \Rightarrow \vec k \cdot \vec E \neq 0 )
$$
$$
\nabla \times E=-\frac{\partial B}{\partial t} \Rightarrow \vec{k} \times \vec{E}=\omega \vec{B} \Rightarrow \vec{E} \perp \vec{B} \Rightarrow \vec B \cdot \vec E=\vec B \cdot \vec D=0
$$
$$
\nabla \times \frac{B}{\mu}=\frac{\partial D}{\partial t} \Rightarrow \vec{k} \times \frac{\vec{B}}{\mu}=-\omega \vec{D} 
\Rightarrow \vec{B} \perp \vec{D} \Rightarrow B \cdot \vec{D}=0
$$
- <font color="#00b0f0">(2)</font> 由(1)已知  
$$
\vec{D}=-\frac{k}{\omega} \times \frac{\vec{B}}{\mu}=-\frac{1}{\omega^{2} \mu} \vec{k} \times(\vec{k} \times \vec{E})=\frac{1}{\omega^{2} \mu}\left[k^{2} \vec{E}-\vec{k}(\vec{k} \cdot \vec{E})\right]
$$
- <font color="#00b0f0">(3)</font> 由于 $\vec{S}=E \times H$, 对 $\vec{k} \times \vec{E}=\omega \vec{B}$ 叉乘 $\vec E$ 得到:
$$
\times E=(k \times E) \times E=\omega B \times E \Rightarrow E(k \cdot E)-\vec{k} E^{2}=\omega \vec{B} \times \vec{E} 
$$
$$
 \because k \cdot E \neq 0 \quad \therefore  可见  \vec{B} \times \vec{E}  一般不与  \vec{k}  同向
$$
## 9. 半无界波导管
求解 $\left[\frac{\partial^{2}}{\partial x^{2}}+\frac{\partial^{2}}{\partial y^{2}}+\frac{\partial^{2}}{\partial z^{2}}+\frac{\omega^{2}}{c^{2}}\right]\binom{E}{B}=0$ , 边界条件: 
$$
\left\{\begin{array}{ll}
E_{x}=E_{y}=0,\ \partial E_{z} / \partial z=0 & \text { at } z=0 \\
E_{y}=E_{z}=0 ,\ \partial E_{y}/\partial x=0& \text { at } x=0,  a   \\
E_{x}=E_{z}=0 ,\ \partial E_{y} / \partial y=0& \text { at } y=0, b 
\end{array}\right.
$$
设 $E_{z}=X(x) Y(y) Z(z)$ ,可得  
$$
\begin{array}{C}
\frac{1}{X} \frac{d^{2} X}{d x^{2}}=-k_{x}^{2}\\
\frac{1}{Y} \frac{d^{2} Y}{d y^{2}}=-k_{y}^{2} \\
\frac{1}{Z} \frac{d^{2} Z}{d z^{2}}=-k_{z}^{2} \\
k_{x}^{2}+k_{y}^{2}+k_{z}^{2}=\frac{w^{2}}{c^{2}}
\end{array}
$$
可以得到答案的前四式. 最后, 由 $\nabla \cdot E=0$ 得到:
$$
A_{x} \frac{m \pi}{a}+A_{y} \frac{n \pi}{b}+A_{z} k_{z}=0
$$
## 13. 波导管** 2
$$
\nu_{m n}=\frac{\omega_{m n}}{2 \pi}=\frac{1}{2} c \sqrt{\frac{m^{2}}{a^{2}}+\frac{n^{2}}{b^{2}}}
=\left\{\begin{array}{l}1.5 \times 10^{8} \cdot \sqrt{\frac{m^{2}}{4 p \times 10^{-6}}+\frac{n^{2}}{1.6 \times 10^{-6}}}=1.5 \times 10^{11} \sqrt{\frac{m^{2}}{49}+\frac{n^{2}}{16}}\mathrm{~Hz}\\
1.5 \times 10^{8} \cdot \sqrt{\frac{m^{2}}{4 p \times 10^{-6}}+\frac{n^{2}}{36 \times 10^{-6}}}=1.5 \times 10^{11} \sqrt{\frac{m^{2}}{49}+\frac{n^{2}}{36}}\mathrm{~Hz}\end{array} \right.
$$
对于 $0.7 \times 0.4 \mathrm{~cm}^{2}: v_{01}=37.5 \times 10^{9} \mathrm{~Hz}>v_{0}=30 \times 10^{9} \mathrm{~Hz} ,\ \  v_{10}=21.4 \times 10^{P} \mathrm{~Hz}<v_{0}$.
   
对于 $0.7 \times 0.6 \mathrm{~cm}^{2}: v_{01}=25 \times 10^{p} \mathrm{~Hz}<v_{0},\ \  v_{10}=21.4 \times 10^{p} \mathrm{~Hz}<v_{0}, \ \ v_{11}=32 . \mathrm{P} \times 10^{\mathrm{P}} H z>v_{0}$.
$$
 \Rightarrow (1) T E_{10} ,\ \  (2) T E_{10} \ and\  T E_{01} 
$$
# 6. 波动物理量的时间平均  
- <font color="#00b0f0">(1)</font> 
$$
A B=\frac{\hat{A}+\hat{A}^{*}}{2} \frac{\hat{B}+\hat{B}^{*}}{2}
$$
 - <font color="#00b0f0">(2)</font>
$$
\begin{aligned}
A B=\operatorname{Re}\left[\hat{A} e^{i \omega t}\right] \cdot \operatorname{Re}\left[\hat{B} e^{i \omega t}\right] & =\frac{1}{4}\left(\hat{A} e^{i \omega t}+\hat{A}^{*} e^{-i \omega t}\right)\left(\hat{B} e^{i \omega t}+\hat{B}^{*} e^{-i \omega t}\right) \\
& =\frac{1}{4}\left[\hat{A} \hat{B} e^{2 i \omega t}+\hat{A}^{*} \hat{B}^{*} e^{-i 2 \omega t}+\hat{A}^{*} \hat{B}+\hat{A} \hat{B}^{*}\right]
\\
&=\frac{1}{2}\left\{\operatorname{Re}\left[\hat{A} \hat{B} e^{i 2 \omega t}\right]+\operatorname{Re}\left[A B^{*}\right]\right\}
\end{aligned}
$$

可见当 A, B 的变化时间尺度 $\tau \gg t$ 时, $\langle A B\rangle=\frac{1}{2} \operatorname{Re}\left[A B^{*}\right]$. 
# 7. 三种介质中的 1D电磁波  
在介质 2 中的相位变化记为 $\theta = \vec k \cdot \Delta \vec x = \frac{\omega}{c/n_2}d$, 假设波在介质 2 中反射 n 次(一个来回算一次), 那么:  
$$
\frac{E_{out}^n}{E_{in}} = TR^n
$$
其中, T 是完全透射 $1\to 2 \to 3$ 对应的衰减:  
$$
T  = T_{12} e^{i\theta} T_{23} = \frac{2n_1}{n_1+n_2} \frac{2n_2}{n_2+n_3} e^{i\theta}
$$
R 是在介质 2 中传播一个来回的衰减:  
$$
R = R_{23} e^{i\theta} R_{21} e^{i\theta} = \frac{{n_2-n_3}}{n_2+n_3} \frac{{n_2 - n_1}}{{n_1+n_2}} e^{i2\theta}
$$
于是  
$$
\begin{aligned} 
\frac{E_{out}}{E_{in}} &= \sum_{n=0}^{+\infty} \frac{E_{out}^n}{E_{in}} \\
&= \sum_{n=0}^{+\infty} TR^n = \frac{T}{1-R} \\
&= \frac{{ 4 n_1 n_2 e^{i\theta} }}{(n_2+n_3)(n_1+n_2)-(n_2-n_3)(n_2 - n_1) e^{i2\theta}}
\end{aligned}
$$
# 8. Drude 模型
##### (a)  
注意到极化强度 $\vec P = N \vec p = N \alpha \vec E = (\epsilon_r - 1)\epsilon_0\vec E$, 得到:  
$$
\alpha = \frac{{(\epsilon_r - 1)\epsilon_0}}{N} = \frac{e^2/m}{\omega_0^2 - \omega^2 - i\omega\gamma}
$$
##### (b)
当电场驱动和阻尼可以忽略时, $\omega = \gamma = 0$:  
$$
\frac{\alpha}{4\pi \epsilon_0} = \frac{e^2\hbar^2}{4\pi \epsilon_0 m_p (\hbar\omega_0)^2} \approx 5.93 \times 10^{-31} ~m^3
$$
##### (c)  
原子极化率可以写作 $\alpha = 4\pi \epsilon_0 a_0^3$ , 于是 $\frac{\alpha}{4\pi \epsilon_0}=a_0^3\approx 1.48\times 10^{-31}$ 与上式处于同一量级.  
##### (d)  
对于实数 $\omega$:
$$
\begin{array}{l}
k_{k}=\frac{n_{R}}{c} \omega=\frac{1}{c}\left[\omega+\frac{\omega_{p}^{2}}{2} \omega \frac{\omega_{0}^{2}-\omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+\gamma^{2} \omega^{2}}\right] \\
\therefore \frac{\nu_{\text {group }}}{c}=\left[d k_{R} / d \omega\right]^{-1} / c=\left\{\left[\omega+\frac{\omega_{e}^{2}}{2} \omega \frac{\omega_{0}^{2}-\omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+\gamma^{2} \omega^{2}}\right]_{\omega}^{\prime}\right\}^{-1} \\
~~~~~~~~~~~~=\left\{\frac{\omega_{p}^{2}}{2} \frac{\omega_{0}^{2}-3 \omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+r^{2} \omega^{2}}-\frac{\omega_{p}^{2}}{2} \omega^{2} \frac{\left[2 \gamma^{2}-4\left(\omega_{0}^{2}-\omega^{2}\right)\right]\left(\omega_{0}^{2}-\omega^{2}\right)}{\left[\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+r^{2} \omega^{2}\right]^{2}}+1\right\}^{-1} \\
\Rightarrow \quad \nu_{g} / c=\left\{1+0.003 \frac{1-3\left(\frac{\omega}{\omega_{0}}\right)^{2}}{\left[1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right]^{2}+0.01\left(\frac{\omega}{\omega_{0}}\right)^{2}}-0.003\left(\frac{\omega}{\omega_{0}}\right)^{2} \frac{\left[0.02-4\left(1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right)\right]\left(1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right)}{\left\{\left[1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right]^{2}+0.01\left(\frac{\omega}{\omega_{0}}\right)^{2}\right\}^{2}}\right\}^{-1} \\
=\left\{\begin{array}{ll}
1.00658^{-1} \approx 0.993 & \omega=0.5 \omega_{0} \\
0.4^{-1} =2.5 & \omega=\omega_{0} \\
1.00598^{-1} \approx 0.994 & \omega=1.5 \omega_{0} \\
\end{array}\right.
\end{array}
$$

##### (e)
对于 $\hat{\vec{E}}=\hat{\vec{E}}_{0} e^{-k_{I} x} e^{i\left(k_{k} x-\omega t\right)}$ :
$$
\left\{\begin{array}{l}k_{I} L \ll 1 ~~\text { 透明 } \\ k_{I} L>1 ~~~\text { 不透明 }\end{array}\right.
$$
##### (f)  
$$
n^{2}=\varepsilon_{r} \mu_r =\left.\mu_{r}\left(1+\frac{N e^{2}}{m \epsilon_{0}} \frac{1}{\omega_{0}^{2}-\omega^{2}-i \omega r}\right)\right|_{\omega_{0}=0} = \mu_r\left(1- \frac{\omega_{pe}^2}{\omega^{2}+i \omega \gamma}\right) \approx 
1- \frac{\omega_{pe}^2}{\omega^{2}+i \omega \gamma}
$$
##### (g)  
由 $(7)(8) \rightarrow \sigma E=N q_{e}^{2} \frac{E}{m} \tau \Rightarrow \frac{N e^{2}}{m}=\frac{\sigma}{\tau}$, 代入(f) 得到:
$$
n^{2}=1-\frac{\sigma}{\tau \epsilon_{0}} \frac{1}{\omega(\omega+i / \tau)}=1-\frac{\sigma / \epsilon_{0}}{\omega(\omega \tau+i)}=1-\frac{\sigma / \epsilon_{0}}{i \omega(1-i \tau \omega)}
$$
##### (h)
由(g)可知  
$$
\begin{aligned}
n
&=\left\{1-\frac{\sigma / \epsilon_{0}}{\omega(\omega \tau+i)}\right\}^{1 / 2} 
=\left\{1-\frac{i \sigma / \epsilon_{0}}{\omega(1-i \omega \tau)}\right\}^{1 / 2} \\
&\xlongequal[\omega \ll \sigma / \varepsilon_{0}]{\omega \tau \ll 1} \sqrt{\frac{\sigma}{\epsilon_{0} \omega}} \cdot e^{\left(i \frac{\pi}{4}+k \pi\right)}(1-i \omega \tau)^{-\frac{1}{2}} \\
&\xlongequal[\omega \tau<c 1]{k=0} \sqrt{\frac{\sigma}{2 \epsilon_{0} \omega}}(1+i)\left(1+\frac{1}{2} i \omega \tau\right) \\ \\
\Rightarrow & n_{I}({\color{gray}虚部}) \approx \sqrt{\frac{\sigma}{2 \epsilon_{0} \omega}}\left(1+\frac{1}{2} \omega \tau\right) \approx \sqrt{\frac{\sigma}{2 \epsilon_{0} \omega}} \\
\Rightarrow & k_{I}=\frac{n_{I} \omega}{c}=\sqrt{\mu_{0} \epsilon_{0}} \cdot \sqrt{\frac{\sigma \omega}{2 \epsilon_{0}}}=\sqrt{\mu_{0} \sigma \omega / 2} \\
\Rightarrow & \delta=1 / k_{I}=\sqrt{2 / \mu_{0} \sigma \omega}
\end{aligned}
$$
##### (i)  
直接套公式有:  
$$
\delta = 
\left\{
\begin{aligned} 
6.6\times 10^{-6} \quad f=10^8 Hz\\
8.56 \times 10^{-3} \quad f=60Hz
\end{aligned}
\right.
$$
##### (j)  
根据(9), 高频近似 $\omega\tau\gg 1$ 给出:  
$$
n^2 = 1-\frac{\sigma}{\tau \epsilon_{0}} \frac{1}{\omega^2} = 1-\frac{\omega_{pe}^2}{\omega^2} \to 1
$$
$\omega\tau\gg 1$ 和 $\omega\gg \omega_{pe}$ 意味着, 电磁波的时间尺度 $\frac{1}{\omega}$ 远小于电子平均碰撞时间 $\tau$, 阻尼效应被忽略, 这导致电磁波的能量不能像课上那样迅速耗散到粒子中(其对应于 $\omega\ll \omega_{pe}$, 与这里不同), 因此波动得以维持和传播.
# 9. 介质中的 Maxwell's 方程组  
##### (a)
由 $\nabla \cdot \vec j+\partial \rho/ \partial t=0$ 得到:  
$$
\nabla \cdot \vec j_{p}+\partial \rho_{p} / \partial t=0\quad when\  \nabla \cdot \vec j_{f}+\partial \rho_{f} / \partial t=0
$$
而极化体电荷 $\rho_{\rho}=-\nabla \cdot \vec{\rho}$, 带入上式得到:
$$
\vec{j}_{p}=\partial \vec{P} / \partial t
$$
##### (b)
同理 $\nabla \cdot \vec j_{m}+\partial \rho_{m} / \partial t=0$, 磁化电流  $\vec j_{m}=\nabla \times \vec m$, 得到:
$$
-\frac{\partial \rho_{m}}{\partial t}=\nabla \cdot \nabla \times \vec m=0 
\Rightarrow
\rho_{m}=const.
$$
##### (c)  
$$
\begin{aligned} 
\nabla \cdot \vec E=\frac{\rho}{\epsilon_{0}} 
&\Rightarrow \nabla \cdot  \vec E=\left(\rho_{f}+\rho_{m}+\rho_{p}\right) / \epsilon_{0}=\left(\rho_{f}-\nabla \cdot p\right) / \epsilon_{0} \\
&\Rightarrow \nabla \cdot\left(\epsilon_{0} E+p\right)=\rho_{f} \\
&\Rightarrow \nabla \cdot \vec D=\rho_{f} 
\\\\
\nabla \times \frac{\vec B}{\mu_{0}}=\vec J+\frac{\partial \epsilon_{0} \vec E}{\partial t} 
&\Rightarrow \nabla \times \frac{\vec B}{\mu_{0}}=\vec J_{f}+\vec J_{m}+\vec J_{p}+\frac{\partial \epsilon_{0} \vec E}{\partial t}=\vec J_{f}+\nabla \times \vec M+\frac{\partial\left(\epsilon_{0} \vec E+\vec p\right)}{\partial t} \\
&\Rightarrow \nabla \times \left(\frac{\vec B}{\mu_{0}}-\vec M\right)=\vec J_{f}+\frac{\partial \vec D}{\partial t} \\
&\Rightarrow \nabla \times \vec H=\vec J_{f}+\frac{\partial \vec D}{\partial t}
\end{aligned}
$$



