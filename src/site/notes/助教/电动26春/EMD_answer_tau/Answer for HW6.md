---
{"dg-publish":true,"permalink":"/助教/电动26春/EMD_answer_tau/Answer for HW6/","noteIcon":"default","created":"2026-06-15T09:49:24.868+08:00","updated":"2025-11-24T15:33:32.943+08:00","dg-note-properties":{}}
---


web版: [url to HW6 Answer](https://siecho.cn/EMD_answer/Answer%20for%20HW6/)

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```


# 1 1D 电磁波解    
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
\left(\frac{1}{c^{2}} \frac{\partial^{2}}{\partial t^{2}}-\frac{\partial^{2}}{\partial r^{2}}\right) u=0 \to 
\varphi(r, t)=\frac{1}{r}[\underbrace{f(t+r / c}_{\text {会聚波 }})+\underbrace{g(t-r / c)}_{\text {发散波 }}]
$$  
对于源，会聚波可略去.
# 2 反常色散
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
&=\left(\omega_{0}^{2}+\omega_{0} \gamma \right)^{1 / 2}-\left(\omega_{0}^{2}-\omega_{0} \gamma \right)^{1 / 2} \\
&=\omega_{0}\left(1+\frac{\gamma}{\omega_{0}}\right)^{1 / 2}-\omega_{0}\left(1-\frac{\gamma}{\omega_{0}}\right)^{1 / 2} \approx {\gamma} \quad\left(\text { 当 } \gamma \ll \omega_{0} \text { 时 }\right)
\end{aligned}
$$
# 3 介质边界的电磁波
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
# 4 TM 模
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
# 5 课本题  
## 5.1 窄带双色波  
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
## 5.2 各向异性介质
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
(\vec k \times\vec  E) \times\vec E=\omega \vec B \times\vec E \Rightarrow \vec E(\vec k \cdot \vec E)-\vec{k} E^{2}=\omega \vec{B} \times \vec{E} 
$$
$$
 \because\vec k \cdot\vec E \neq 0 \quad \therefore  可见  \vec{B} \times \vec{E}  一般不与  \vec{k}  同向
$$
## 5.3 半无界波导管
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
可以得到答案的前四式. 最后, 由 $\nabla \cdot \vec E=0$ 得到:
$$
A_{x} \frac{m \pi}{a}+A_{y} \frac{n \pi}{b}+A_{z} k_{z}=0
$$
## 5.4 波导管** 2
$$
\nu_{m n}=\frac{\omega_{m n}}{2 \pi}=\frac{1}{2} c \sqrt{\frac{m^{2}}{a^{2}}+\frac{n^{2}}{b^{2}}}
=\left\{\begin{array}{l}1.5 \times 10^{8} \cdot \sqrt{\frac{m^{2}}{4 9 \times 10^{-6}}+\frac{n^{2}}{1.6 \times 10^{-6}}}=1.5 \times 10^{11} \sqrt{\frac{m^{2}}{49}+\frac{n^{2}}{16}}\mathrm{~Hz}\\
1.5 \times 10^{8} \cdot \sqrt{\frac{m^{2}}{4 9 \times 10^{-6}}+\frac{n^{2}}{36 \times 10^{-6}}}=1.5 \times 10^{11} \sqrt{\frac{m^{2}}{49}+\frac{n^{2}}{36}}\mathrm{~Hz}\end{array} \right.
$$
对于 $0.7 \times 0.4 \mathrm{~cm}^{2}: \nu_{01}=37.5 \times 10^{9} \mathrm{~Hz}>\nu_{0}=30 \times 10^{9} \mathrm{~Hz} ,\ \  \nu_{10}=21.4 \times 10^{9} \mathrm{~Hz}<\nu_{0}$.
   
对于 $0.7 \times 0.6 \mathrm{~cm}^{2}: \nu_{01}=25 \times 10^{9} \mathrm{~Hz}<\nu_{0},\ \  \nu_{10}=21.4 \times 10^{9} \mathrm{~Hz}<\nu_{0}, \ \ \nu_{11}=32 . \mathrm{9} \times 10^{\mathrm{9}} H z>\nu_{0}$.
$$
 \Rightarrow (1) T E_{10} ,\ \  (2) T E_{10} \ and\  T E_{01} 
$$
# 6 波动物理量的时间平均  
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
# 7 三种介质中的 1D电磁波  
在介质 2 中的相位变化记为 $\theta = \vec k \cdot \Delta \vec x = \frac{\omega}{c/n_2}d$, 假设波在介质 2 中反射 n 次(一个来回算一次), 那么:  
$$
\frac{E_{out,n} }{E_{in}} = TR^n
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
\frac{E_{out}}{E_{in}} &= \sum_{n=0}^{+\infty} \frac{E_{out,n}}{E_{in}} \\
&= \sum_{n=0}^{+\infty} TR^n = \frac{T}{1-R} \\
&= \frac{{ 4 n_1 n_2 e^{i\theta} }}{(n_2+n_3)(n_1+n_2)-(n_2-n_3)(n_2 - n_1) e^{i2\theta}}
\end{aligned}
$$
这里, 实际的 E 是上述的实部.  

或者, 使用边界条件求解:  
<div class="excalidraw-svg"><svg version="1.1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1262.0639970289571 187.41593629496705" width="1262.0639970289571" height="187.41593629496705" class="excalidraw-svg" style="max-width: 100%; height: auto;"><!-- svg-source:excalidraw --><metadata/><defs><style class="style-fonts">/**/</style></defs><rect x="0" y="0" width="1262.0639970289571" height="187.41593629496705" fill="#ffffff"/><g stroke-linecap="round"><g transform="translate(649.2761724213857 10) rotate(0 1.1484918101091637 82.92349152535232)"><path d="M0 0 C0.38 27.64, 1.91 138.21, 2.3 165.85 M0 0 C0.38 27.64, 1.91 138.21, 2.3 165.85" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(833.1706871890856 10) rotate(0 1.8685599355478644 83.70796814748353)"><path d="M0 0 C0.62 27.9, 3.11 139.51, 3.74 167.42 M0 0 C0.62 27.9, 3.11 139.51, 3.74 167.42" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(493.8310882949387 133.15555924967776) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M0 0 C49.61 0.27, 99.22 0.55, 137.61 0.76 M0 0 C50.22 0.28, 100.44 0.55, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(493.8310882949387 133.15555924967776) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M114.07 9.18 C122.56 6.15, 131.05 3.11, 137.61 0.76 M114.07 9.18 C122.66 6.11, 131.25 3.04, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(493.8310882949387 133.15555924967776) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M114.17 -7.92 C122.62 -4.79, 131.07 -1.66, 137.61 0.76 M114.17 -7.92 C122.72 -4.75, 131.28 -1.58, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(674.4013318097745 136.76693169463272) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M0 0 C41.31 0.23, 82.61 0.46, 137.61 0.76 M0 0 C47.35 0.26, 94.69 0.52, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(674.4013318097745 136.76693169463272) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M114.07 9.18 C121.14 6.65, 128.21 4.13, 137.61 0.76 M114.07 9.18 C122.17 6.28, 130.27 3.39, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(674.4013318097745 136.76693169463272) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M114.17 -7.92 C121.21 -5.31, 128.24 -2.71, 137.61 0.76 M114.17 -7.92 C122.24 -4.93, 130.3 -1.95, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(852.3105771770493 137.52721242561967) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M0 0 C48.85 0.27, 97.7 0.54, 137.61 0.76 M0 0 C34.97 0.19, 69.94 0.39, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(852.3105771770493 137.52721242561967) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M114.07 9.18 C122.43 6.19, 130.79 3.2, 137.61 0.76 M114.07 9.18 C120.06 7.04, 126.04 4.9, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(852.3105771770493 137.52721242561967) rotate(0 68.80676240660227 0.38014036549350294)"><path d="M114.17 -7.92 C122.49 -4.84, 130.81 -1.76, 137.61 0.76 M114.17 -7.92 C120.13 -5.71, 126.08 -3.51, 137.61 0.76" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(806.6927356150035 69.10060597361763) rotate(0 -67.66635689922833 -0.7603119092002828)"><path d="M0 0 C-40.92 -0.46, -81.84 -0.92, -135.33 -1.52 M0 0 C-39.93 -0.45, -79.86 -0.9, -135.33 -1.52" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(806.6927356150035 69.10060597361763) rotate(0 -67.66635689922833 -0.7603119092002828)"><path d="M-111.75 -9.81 C-118.88 -7.3, -126.01 -4.8, -135.33 -1.52 M-111.75 -9.81 C-118.7 -7.36, -125.66 -4.92, -135.33 -1.52" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(806.6927356150035 69.10060597361763) rotate(0 -67.66635689922833 -0.7603119092002828)"><path d="M-111.94 7.29 C-119.01 4.63, -126.09 1.96, -135.33 -1.52 M-111.94 7.29 C-118.84 4.69, -125.74 2.09, -135.33 -1.52" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(629.9240204679558 65.67928032774952) rotate(0 -67.66635689922833 -0.7603119092002828)"><path d="M0 0 C-37.09 -0.42, -74.18 -0.83, -135.33 -1.52 M0 0 C-46.45 -0.52, -92.9 -1.04, -135.33 -1.52" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(629.9240204679558 65.67928032774952) rotate(0 -67.66635689922833 -0.7603119092002828)"><path d="M-111.75 -9.81 C-118.21 -7.54, -124.68 -5.26, -135.33 -1.52 M-111.75 -9.81 C-119.84 -6.96, -127.94 -4.12, -135.33 -1.52" stroke="#1e1e1e" stroke-width="2" fill="none"/></g><g transform="translate(629.9240204679558 65.67928032774952) rotate(0 -67.66635689922833 -0.7603119092002828)"><path d="M-111.94 7.29 C-118.35 4.88, -124.76 2.46, -135.33 -1.52 M-111.94 7.29 C-119.97 4.27, -128 1.24, -135.33 -1.52" stroke="#1e1e1e" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(1046.8236522777975 91.2329604592552) rotate(0 102.62017237557984 2.5527309192965504)"><path d="M0 0 C34.21 0.85, 171.03 4.25, 205.24 5.11 M0 0 C34.21 0.85, 171.03 4.25, 205.24 5.11" stroke="#ffffff" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(445.39809541403224 94.29622918779046) rotate(0 -85.77206874932682 1.5316553008191534)"><path d="M0 0 C-59.96 1.07, -119.92 2.14, -171.54 3.06 M0 0 C-63.22 1.13, -126.45 2.26, -171.54 3.06" stroke="#ffffff" stroke-width="2" fill="none"/></g><g transform="translate(445.39809541403224 94.29622918779046) rotate(0 -85.77206874932682 1.5316553008191534)"><path d="M-148.21 -5.91 C-156.36 -2.77, -164.52 0.36, -171.54 3.06 M-148.21 -5.91 C-156.81 -2.6, -165.41 0.71, -171.54 3.06" stroke="#ffffff" stroke-width="2" fill="none"/></g><g transform="translate(445.39809541403224 94.29622918779046) rotate(0 -85.77206874932682 1.5316553008191534)"><path d="M-147.9 11.19 C-156.17 8.35, -164.43 5.51, -171.54 3.06 M-147.9 11.19 C-156.62 8.2, -165.33 5.2, -171.54 3.06" stroke="#ffffff" stroke-width="2" fill="none"/></g></g><mask/><g stroke-linecap="round"><g transform="translate(333.4419374942496 108.25118559055488) rotate(0 -161.7209687471248 -2.608404159434457)"><path d="M0 0 C-53.91 -0.87, -269.53 -4.35, -323.44 -5.22 M0 0 C-53.91 -0.87, -269.53 -4.35, -323.44 -5.22" stroke="#ffffff" stroke-width="2" fill="none"/></g></g><mask/></svg></div>
$$
\begin{aligned} 
E_{in} T_{12} + E_{2-} R_{21} &= E_{2+} \\
E_{in} R_{12} + E_{2-} T_{21} &= E_r \\
E_{2+}e^{i\theta} T_{23} &= E_{out} \\
E_{2+} e^{i\theta} R_{23} &= E_{2-}e^{-i\theta}
\end{aligned}
$$
重新记无量纲复振幅 $E_i' = \frac{E_i}{E_{in}}$, 上式给出:  
$$
\begin{bmatrix} -1 & \frac{{n_2-n_1}}{n_1+n_2} & 0 & 0 \\  0 & \frac{2n_2}{n_1+n_2} & -1 & 0 \\ e^{i\theta}  \frac{2n_2}{n_2+n_3} & 0 & 0 & -1 \\ e^{i\theta} \frac{{n_2-n_3}}{n_2+n_3} & -e^{-i\theta} & 0 & 0 \end{bmatrix}
\begin{bmatrix} E_{2+}' \\ E_{2-}' \\ E'_r \\E'_{out} \end{bmatrix}
=
\begin{bmatrix} -\frac{2n_1}{n_1+n_2} \\ -\frac{{(n_1-n_2)}}{n_1+n_2} \\ 0 \\0 \end{bmatrix}
$$
MMA 给出一致的结果:
![zz_figure/Pasted image 20250527113220.png](/img/user/zz_figure/Pasted%20image%2020250527113220.png)

当然, 也可以用最基本的边界条件:  
$$
\begin{array}c 
E_{in}+ E_r = E_{2+} + E_{2-} \\
n_1(E_{in}- E_r) = n_2 (E_{2+} - E_{2-}) \\
E_{2+}e^{i\theta} + E_{2-}e^{-i\theta} = E_{out}\\
n_2(E_{2+}e^{i\theta} - E_{2-}e^{-i\theta}) = n_3E_{out}
\end{array}
$$
会得到一样的结果.
# 8 Drude 模型
##### (a)  
注意到极化强度 $\vec P = N \vec p = N \alpha \vec E = (\epsilon_r - 1)\epsilon_0\vec E$, 得到:  
$$
\alpha = \frac{{(\epsilon_r - 1)\epsilon_0}}{N} = \frac{e^2/m}{\omega_0^2 - \omega^2 - i\omega\gamma}
$$
##### (b)
当电场驱动和阻尼可以忽略时, $\omega = \gamma = 0$:  
$$
\frac{\alpha}{4\pi \epsilon_0} = \frac{e^2\hbar^2}{4\pi \epsilon_0 m_e (\hbar\omega_0)^2} \approx 5.93 \times 10^{-31} ~m^3
$$
##### (c)  
原子极化率可以写作 $\alpha = 4\pi \epsilon_0 a_0^3$ , 于是 $\frac{\alpha}{4\pi \epsilon_0}=a_0^3\approx 1.48\times 10^{-31}~m^3$ 与上式处于同一量级.  
##### (d)  
对于实数 $\omega$: 
$$
\begin{array}{l}
k_{R}=\frac{n_{R}}{c} \omega=\frac{1}{c}\left[\omega+\frac{\omega_{p}^{2}}{2} \omega \frac{\omega_{0}^{2}-\omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+\gamma^{2} \omega^{2}}\right] \\
\therefore \frac{\nu_{\text {group }}}{c}=\left[d k_{R} / d \omega\right]^{-1} / c=\left\{\left[\omega+\frac{\omega_{e}^{2}}{2} \omega \frac{\omega_{0}^{2}-\omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+\gamma^{2} \omega^{2}}\right]_{\omega}^{\prime}\right\}^{-1} \\
~~~~~~~~~~~~=\left\{\frac{\omega_{p}^{2}}{2} \frac{\omega_{0}^{2}-3 \omega^{2}}{\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+\gamma^{2} \omega^{2}}-\frac{\omega_{p}^{2}}{2} \omega^{2} \frac{\left[2 \gamma^{2}-4\left(\omega_{0}^{2}-\omega^{2}\right)\right]\left(\omega_{0}^{2}-\omega^{2}\right)}{\left[\left(\omega_{0}^{2}-\omega^{2}\right)^{2}+\gamma^{2} \omega^{2}\right]^{2}}+1\right\}^{-1} \\
\Rightarrow \quad \nu_{g} / c=\left\{1+0.003 \frac{1-3\left(\frac{\omega}{\omega_{0}}\right)^{2}}{\left[1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right]^{2}+0.01\left(\frac{\omega}{\omega_{0}}\right)^{2}}-0.003\left(\frac{\omega}{\omega_{0}}\right)^{2} \frac{\left[0.02-4\left(1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right)\right]\left(1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right)}{\left\{\left[1-\left(\frac{\omega}{\omega_{0}}\right)^{2}\right]^{2}+0.01\left(\frac{\omega}{\omega_{0}}\right)^{2}\right\}^{2}}\right\}^{-1} \\
=\left\{\begin{array}{ll}
1.00658^{-1} \approx 0.993 & \omega=0.5 \omega_{0} \\
0.4^{-1} =2.5 & \omega=\omega_{0} \\
1.00598^{-1} \approx 0.994 & \omega=1.5 \omega_{0} \\
\end{array}\right.
\end{array}
$$
在共振区域附近, 反常色散的群速度超过了光速(为什么? 可以查阅:  [反常色散的群速度](https://zhuanlan.zhihu.com/p/509148630)).  

> 有些科普说群速度是能量传播的速度。这是错误的。要记住，群速度只是波包运动的一阶近似而已，并不能完全表述波包的演化。群速度超过光速，并不说明能量/信息超光速，而是在这种情况下，群速度已经失去了意义。

##### (e)
对于 $\hat{\vec{E}}=\hat{\vec{E}}_{0} e^{-k_{I} x} e^{i\left(k_{I} x-\omega t\right)}$ :  
$$
\left\{\begin{array}{l}k_{I} L \ll 1 ~~\text { 透明 } \\ k_{I} L\gg1 ~~~\text { 不透明 }\end{array}\right.
$$
##### (f)  
$$
n^{2}=\varepsilon_{r} \mu_r =\left.\mu_{r}\left(1+\frac{N e^{2}}{m \epsilon_{0}} \frac{1}{\omega_{0}^{2}-\omega^{2}-i \omega \gamma}\right)\right|_{\omega_{0}=0} = \mu_r\left(1- \frac{\omega_{pe}^2}{\omega^{2}+i \omega \gamma}\right) \approx 
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
=\left\{1+\frac{i \sigma / \epsilon_{0}}{\omega(1-i \omega \tau)}\right\}^{1 / 2} \\
&\xlongequal[\omega \ll \sigma / \varepsilon_{0}]{\omega \tau \ll 1} \sqrt{\frac{\sigma}{\epsilon_{0} \omega}} \cdot e^{\left(i \frac{\pi}{4}+k \pi\right)}(1-i \omega \tau)^{-\frac{1}{2}} \\
&\xlongequal[\omega \tau\ll 1]{k=0} \sqrt{\frac{\sigma}{2 \epsilon_{0} \omega}}(1+i)\left(1+\frac{1}{2} i \omega \tau\right) \\ \\
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

该式也适用于描述冷等离子体中电磁波的色散关系.  

##### (k)  
由 $(j)$ 可知, 条件是波的频率足够高/金属足够薄.  
# 9 介质中的 Maxwell's 方程组  
##### (a)
由 $\nabla \cdot \vec j+\partial \rho/ \partial t=0$ 得到:  
$$
\nabla \cdot \vec j_{p}+\partial \rho_{p} / \partial t=0\quad when\  \nabla \cdot \vec j_{f}+\partial \rho_{f} / \partial t=0
$$
而极化体电荷 $\rho_{\rho}=-\nabla \cdot \vec{P}$, 带入上式得到:
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

# 10 补充: 没有补充  
本来想写点电磁场的拉氏量, 怎么按一般步骤推导得到的来着, 但是大家有期末考试, 助教也有, 所以......  

结果放在这里, 拉氏量:  
$$
\begin{aligned} 
\mathcal{L}
&=
 -\sum_i \frac{m_i\delta(\vec x-\vec x_i)c^2}{\gamma}  - \frac{1}{4\mu_0 c} F^{\alpha\beta}F_{\alpha\beta} -\frac{{j^\mu A_\mu}}{c}
\end{aligned}
$$
以及连续性方程:  
$$
\partial_\mu T^{\mu\nu}_{E.M.field} = -F^{\nu}_{~~\mu} j^\mu = -f^\mu
$$
课上讲的四维洛伦兹力:
$$
f^\mu = F^{\mu}_{~~\nu} j^\nu = m\delta(\vec x - \vec x_0)\frac{ d u^\mu }{ d t} = (\ \frac{1}{c} \vec{j} \cdot \vec E 
,\ \ \vec j \times \vec B + \rho\vec{E}\ ) 
$$


