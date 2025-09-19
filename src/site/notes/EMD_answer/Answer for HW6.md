---
{"dg-publish":true,"permalink":"/EMD_answer/Answer for HW6/","noteIcon":"default","created":"2025-05-21T20:09:17.112+08:00","updated":"2025-09-08T12:28:08.313+08:00"}
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
<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="Drawing_2025-05-27_1025.18.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.11.1","elements":[{"id":"-WdWiMZ0sjWntlP9R7Pkq","type":"line","x":-142.60831788783764,"y":-126.89545035506711,"width":2.2969836202183274,"height":165.84698305070464,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a0","roundness":{"type":2},"seed":873676591,"version":129,"versionNonce":1161396033,"isDeleted":false,"boundElements":[],"updated":1748312867557,"link":null,"locked":false,"points":[[0,0],[2.2969836202183274,165.84698305070464]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"9qchUcGkI7HjZot0Du0NF","type":"line","x":41.286196879862246,"y":-126.89545035506711,"width":3.7371198710957287,"height":167.41593629496705,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a1","roundness":{"type":2},"seed":316833647,"version":180,"versionNonce":888994017,"isDeleted":false,"boundElements":[],"updated":1748312874826,"link":null,"locked":false,"points":[[0,0],[3.7371198710957287,167.41593629496705]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"2xaUQt5X2aYFM4I3T5xaR","type":"arrow","x":-298.05340201428464,"y":-3.739891105389347,"width":137.61352481320455,"height":0.7602807309870059,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a2","roundness":null,"seed":1385082799,"version":98,"versionNonce":1748448495,"isDeleted":false,"boundElements":[],"updated":1748312814106,"link":null,"locked":false,"points":[[0,0],[137.61352481320455,0.7602807309870059]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"-E9CNEpjypGeP_agicGEQ","type":"arrow","x":-117.48315849944879,"y":-0.12851866043439486,"width":137.61352481320455,"height":0.7602807309870059,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a4","roundness":null,"seed":1941793089,"version":147,"versionNonce":1521535791,"isDeleted":false,"boundElements":[],"updated":1748312820324,"link":null,"locked":false,"points":[[0,0],[137.61352481320455,0.7602807309870059]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"8h1LGpmHe7ff0S-y77fvP","type":"arrow","x":60.426086867825916,"y":0.6317620705525542,"width":137.61352481320455,"height":0.7602807309870059,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a5","roundness":null,"seed":9243503,"version":156,"versionNonce":2127376385,"isDeleted":false,"boundElements":[],"updated":1748312823595,"link":null,"locked":false,"points":[[0,0],[137.61352481320455,0.7602807309870059]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"P-XAmZ8dV69XAdFg-jtlu","type":"arrow","x":14.808245305780133,"y":-67.79484438144948,"width":135.33271379845667,"height":1.5206238184005656,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a6","roundness":null,"seed":212853697,"version":339,"versionNonce":694935791,"isDeleted":false,"boundElements":[],"updated":1748312837391,"link":null,"locked":false,"points":[[0,0],[-135.33271379845667,-1.5206238184005656]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"-X405Avy0ne-WjfIEQ6by","type":"arrow","x":-161.96046984126758,"y":-71.21617002731759,"width":135.33271379845667,"height":1.5206238184005656,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a8","roundness":null,"seed":521016271,"version":403,"versionNonce":1683934401,"isDeleted":false,"boundElements":[],"updated":1748312849089,"link":null,"locked":false,"points":[[0,0],[-135.33271379845667,-1.5206238184005656]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"hJgm1KEj","type":"image","x":-182.1336825632108,"y":-31.8381412689248,"width":31.820190720963343,"height":18.56177792056195,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"roundness":null,"seed":87543,"version":59,"versionNonce":825460001,"updated":1748312899074,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"58594df5f7e870effceb95515aeb7af23be8ffcd","scale":[1,1],"index":"a9","frameId":null,"status":"pending","crop":null},{"id":"4NAwttox","type":"image","x":-182.17486784358545,"y":-100.2647788991402,"width":25.82019072096328,"height":20.082370560749215,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"roundness":null,"seed":82447,"version":77,"versionNonce":352592687,"updated":1748312916219,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"b9b8a6fb81d5a03cce8ada0a63e4ede1375db833","scale":[1,1],"index":"aA","frameId":null,"status":"pending","crop":null},{"id":"pkgymN6d","type":"image","x":-126.3510998796666,"y":-26.51611379558915,"width":37.12349348469729,"height":18.561746742348646,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"roundness":null,"seed":94840,"version":96,"versionNonce":864464769,"updated":1748312998922,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"8df2f35ed237ec0714dad754aa208775abbf6dc3","scale":[1,1],"index":"aB","frameId":null,"status":"pending","crop":null},{"id":"xLjcHIwI","type":"image","x":-124.07035122134556,"y":-101.78537153932746,"width":35.60293202272306,"height":17.80146601136153,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"roundness":null,"seed":72687,"version":68,"versionNonce":1831364719,"updated":1748312994189,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"57b3c2e22a31557a881b785901c6848e4a01d8ce","scale":[1,1],"index":"aC","frameId":null,"status":"pending","crop":null},{"id":"ZR9umu7u","type":"image","x":54.35951796432971,"y":-22.714616606014204,"width":34.88758579537355,"height":16.280873371174323,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"roundness":null,"seed":33663,"version":94,"versionNonce":561020559,"updated":1748312988016,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"fileId":"31d86569f8544d6d3710bb97df2a158d03f6fb17","scale":[1,1],"index":"aD","frameId":null,"status":"pending","crop":null},{"id":"XiofbelGOe5EgaslFciYy","type":"line","x":254.939161968574,"y":-45.662489895811916,"width":205.24034475115968,"height":5.105461838593101,"angle":0,"strokeColor":"#ffffff","backgroundColor":"#ffffff","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"aE","roundness":{"type":2},"seed":225316175,"version":30,"versionNonce":1686245199,"isDeleted":false,"boundElements":[],"updated":1748313038003,"link":null,"locked":false,"points":[[0,0],[205.24034475115968,5.105461838593101]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"BQlqVldt2pvv-GXINi9lx","type":"arrow","x":-346.4863948951911,"y":-42.59922116727665,"width":171.54413749865364,"height":3.0633106016383067,"angle":0,"strokeColor":"#ffffff","backgroundColor":"#ffffff","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"aF","roundness":null,"seed":643286273,"version":85,"versionNonce":6194927,"isDeleted":false,"boundElements":[],"updated":1748313052985,"link":null,"locked":false,"points":[[0,0],[-171.54413749865364,3.0633106016383067]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"arrow","elbowed":false},{"id":"S6skiZD8uel5Pvuv5Q1b2","type":"line","x":-458.44255281497374,"y":-28.64426476451223,"width":323.4419374942496,"height":5.216808318868914,"angle":0,"strokeColor":"#ffffff","backgroundColor":"#ffffff","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"aG","roundness":{"type":2},"seed":1633298209,"version":50,"versionNonce":1908025345,"isDeleted":false,"boundElements":null,"updated":1748317279228,"link":null,"locked":false,"points":[[0,0],[-323.4419374942496,-5.216808318868914]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#ffffff","currentItemBackgroundColor":"#ffffff","currentItemFillStyle":"solid","currentItemStrokeWidth":2,"currentItemStrokeStyle":"solid","currentItemRoughness":0,"currentItemOpacity":100,"currentItemFontFamily":5,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemArrowType":"sharp","scrollX":824.175925569374,"scrollY":454.20792686772603,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":20,"gridStep":5,"gridModeEnabled":false,"gridColor":{"Bold":"rgba(217, 217, 217, 0.5)","Regular":"rgba(230, 230, 230, 0.5)"},"currentStrokeOptions":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true},"objectsSnapModeEnabled":false,"activeTool":{"type":"selection","customType":null,"locked":false,"fromSelection":false,"lastActiveTool":null}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Drawing_2025-05-27_1025.18.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
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
![z_figure/Pasted image 20250527113220.png](/img/user/z_figure/Pasted%20image%2020250527113220.png)

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


