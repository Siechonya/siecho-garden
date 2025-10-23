---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW1/","noteIcon":"default","created":"2025-10-23T14:27:31.162+08:00","updated":"2025-09-25T13:16:20.465+08:00"}
---


# 1 球坐标  
## 1.1 
![z_figure/Pasted image 20250911160120.png](/img/user/z_figure/Pasted%20image%2020250911160120.png)  
首先注意到，球坐标系 $(r, \theta, \phi)$ 与直角坐标系 $(x, y, z)$ 的转换关系为：  
$$
\left\{
\begin{aligned} 
x & = r\sin\theta \cos\phi\\
y &= r \sin\theta \sin\phi \\
z &= r \cos\theta \\
\end{aligned}
\right.
$$
对应的三个正交单位矢量为：  
$$
\left\{
\begin{aligned} 
\hat{e}_r &= \frac{ \partial \vec r }{ \partial r } =  \sin\theta \cos\phi \hat{i} + \sin\theta \sin\phi \hat{j} + \cos\theta \hat{k}\\
\hat{e}_\theta &= \frac{1}{r}\frac{ \partial \vec r }{ \partial \theta  } =  \cos\theta \cos\phi \hat{i} + \cos\theta \sin\phi \hat{j} - \sin\theta \hat{k} \\
\hat{e}_\phi & = \frac{1}{r\sin\theta}\frac{ \partial \vec r }{ \partial \phi }= -\sin\phi \hat{i} + \cos\phi \hat{j}\\
\end{aligned}
\right.
$$
利用链式法则，可以求得三个单位矢量对时间的变化率：
$$
\left\{
\begin{aligned} 
\dot{\hat{e}}_r &= \dot{\theta} \hat{e}_\theta + \dot{\phi} \sin\theta \hat{e}_\phi \\
\dot{\hat{e}}_\theta &= -\dot{\theta} \hat{e}_r + \dot{\phi} \cos\theta \hat{e}_\phi\\
\dot{\hat{e}}_\phi &= -(\sin\theta \hat{e}_r + \cos\theta \hat{e}_\theta)\dot{\phi}\\
\end{aligned}
\right.
$$
## 1.2 速度表达式
位置矢量 $\vec{r} = r \hat{e}_r$ 对时间求导，得到速度矢量：
$$
\vec{v} = \dot {\vec r} = \dot r \hat{e}_r +r \dot {\hat{e}}_r
= 
\dot{r}\hat{e}_r + r\dot{\theta}\hat{e}_\theta + r\dot{\phi}\sin\theta \hat{e}_\phi
$$
## 1.3 加速度表达式
速度矢量 $\vec{v}$ 再次对时间求导，得到加速度矢量：
$$
\vec{a} 
= \dot {\vec v}
= (\ddot{r} - r\dot{\theta}^2 - r\dot{\phi}^2\sin^2\theta)\hat{e}_r + (r\ddot{\theta} + 2\dot{r}\dot{\theta} - r\dot{\phi}^2\sin\theta\cos\theta)\hat{e}_\theta + (r\ddot{\phi}\sin\theta + 2\dot{r}\dot{\phi}\sin\theta + 2r\dot{\phi}\dot{\theta}\cos\theta)\hat{e}_\phi
$$
# 2 开普勒运动常数
这一题可参阅讲义。结果是：  
$$
\frac{ \mathrm{d} v }{ \mathrm{d} \theta} = \frac{GM}{L}
$$
其中，M 是中心天体质量，L 是运动天体的(单位质量)角动量。  
# 3 双曲线轨道  
## 3.1 
![z_figure/Pasted image 20250911164445.png](/img/user/z_figure/Pasted%20image%2020250911164445.png)
如图，构造步骤：

1. 给定一个圆，圆心 $F_1$ ​，半径 $R$；取圆外一点 $F_2​$。
2. 在圆上取动点 $P$，作 $PF_2$ ​的中垂线，与 $PF_1$ ​（延长线）交于点$Q$。
3. 动点 $P$ 运动时，点 $Q$ 的轨迹即为以 $F_1​$、$F_2​$ 为焦点的双曲线。（因为 $PQ = QF_2$，所以 $|QF_2 - QF_1| = |PF_1| \equiv R$）

> [!tip]
> 和椭圆轨道一样，这里的中垂线也是双曲线轨道在 Q 点的切线。
## 3.2 
因为角动量守恒依旧成立，所以第二问的结论依旧是可用的，于是 $\Delta v \propto \Delta \theta$，得到的速度图仍然是一个圆（左图）。 
![z_figure/Pasted image 20250911210406.png](/img/user/z_figure/Pasted%20image%2020250911210406.png)  
将速度图旋转 90 度，方向与中垂线平行，同时也是双曲线的切线。随着 $\theta$ 变化，将得到的一系列切线连接，就得到轨道为双曲线。  

> [!info] 更严格一点来说
> 记 $AF_1=C$，速度圆半径为 $R$，那么根据速度圆，可以假设：  
> $$
> \vec v  =  \begin{bmatrix} v_x  \\  v_y  \end{bmatrix} = \begin{bmatrix} -R\sin\theta \\  R\cos\theta +C  \end{bmatrix}
> $$
> 将坐标系旋转到极坐标，得到：
> $$
> \vec v  
> = 
> \begin{bmatrix} v_r  \\  v_\theta  \end{bmatrix}
> =
> \begin{bmatrix} \dot r  \\  r \dot \theta  \end{bmatrix}
> =
> \begin{bmatrix} \cos\theta & \sin\theta \\  -\sin\theta & \cos\theta \end{bmatrix}
> \begin{bmatrix} v_x  \\  v_y  \end{bmatrix} 
> = 
> \begin{bmatrix} -C\sin\theta \\  C\cos\theta +R  \end{bmatrix}
> $$
> 得到：  
> $$
> \frac{ \mathrm{d} r }{ \mathrm{d} \theta} 
> =
> \frac{{{ \mathrm{d} r }/{ \mathrm{d} t}}}{{ \mathrm{d} \theta }/{ \mathrm{d} t}} = r \frac{\dot r}{r\dot\theta}
> = r \frac{C\sin\theta}{R+C\cos\theta}
> $$
> 这个方程容易通过分离 $r$ 和 $\theta$ 来求解，最后的到其满足圆锥曲线方程 $r = \frac{p}{1+e\cos\theta}$，其中 $e=\frac{C}{R}$，p 是积分常数，也就是说  
> - C < R 时，也就是 A 点在圆内时，e<1，对应椭圆；
> - 圆、双曲线、抛物线完全类似。

## 3.3 
此时，金原子核可视为固定不变，而库仑力和万有引力均为平方反比力，性质相似，所以上述讨论也成立，$\alpha$ 粒子轨迹为双曲线，原子核位于 $F_2$。  
# 4 进动  
## 4.1 
根据广义相对论修正 $F^{(GR)} = - \frac{{3(GM)^2 p}}{r^4 c^2}$,   行星在公转一周后，位矢和速度方向都会发生偏转，这个偏转就是每运行轨道一圈的进动角，记为 $\Delta$。题目缺少一个说明：广义相对论修正力 $F^{(GR)}$ 的方向和牛顿万有引力一致，加上这个说明，就得到：  
$$
\frac{\Delta}{ 2\pi} = \frac{\delta \Delta v}{ \Delta v} = \frac{{F^{(GR)}}}{F^{(Newton)}} 
=
\frac{{3(GM)^2p}}{r^4 c^2}/ \frac{{GM}}{r^2}
= 
\frac{3GMp}{r^2c^2}
$$
$\delta \Delta v$ 是在每个微小速度变化 $\Delta v$ 时，广义相对论修正带来的进动。在离心率 $e$ 较小时，$p\approx a,\ r \approx a$，于是：  
$$
\Delta \approx \frac{6\pi GM}{ac^2}
$$
## 4.2 
将题目所给数据带入上式，得到：  
$$
\Delta \approx \frac{6\pi }{5.8\times 10^7 ~km} \times 1.5 ~km \approx 4.9 \times 10^{-7} rad
$$
> [!info]
> hw1作业答案到此结束。如果感兴趣，可以往后阅读。
# Appendix 稍微严格一点的水星进动计算过程%
一般描述**单位质量**天体的运动的比耐公式是这样的：  
$$
\vec{F} = -h^2\mu^2\left(\frac{d^2\mu}{d\varphi^2} + \mu\right)\vec{e_r},\quad \mu = \frac{1}{r}
$$
已知 $F^{(GR)} = - \frac {{3(GM)^2 p}} {r^4 c^2}$ ，而 $h=\sqrt {GMp}​$ 是单位质量的角动量，得到：  
$$
\vec{F} = \vec F^{(Newton)} + \vec F^{(GR)} =  -G \frac{M}{r^2} \left( 1 + \frac{3h^2}{r^2c^2} \right) \vec{e_r}
$$
使用变量替换 $u = \frac{\color{blue}GM}{r}$，可以得到：
$$
\boxed{
\frac{ d^2 u }{ d^2 \varphi} + u = \frac{G^2M^2}{h^2} + {\color{red} \frac{3u^2}{c^2}} 
}
$$
上式的红色项正是广义相对论所带来的一阶修正。去掉该项，就是在力学中学过的、求解开普勒运动所得到的方程，我们可以发现解为 $r=  \frac{h^2/GM}{1+e\cos\varphi}$，这正是圆锥曲线。现在我们好奇，引入的项显然是一个小量，会让原轨道偏离圆锥曲线，这个偏离的曲线是什么形状？

这个方程是非线性的，不便于解析处理，考虑到 $r\gg r_g = \frac{2GM}{c^2}$，可以求其微扰解，也就是直接将零阶解 $r=  \frac{h^2/GM}{1+e\cos\varphi}$ 带入方程，注意到 $u^2 \approx \frac{1+2e\cos\varphi}{h^4/G^4M^4}$，取 $e\ll1$（尽管对于水星 $e=0.2056$ 不算特别小，但近似仍是有效的），得到：
$$
\frac{ d^2 u }{ d^2 \varphi} + u = \frac{G^2M^2}{h^2} +  3\frac{{G^4M^4}}{h^4c^2} (1+2e\cos\varphi)
$$
右侧第一项 $\frac{G^2M^2}{h^2}$ 是带有初始位移的简谐振动项，对应的正是零阶解（轨道为圆锥曲线）；后两项虽然都带有高阶小量 $\frac{G^4M^4}{h^4c^2}$，但由于 $\cos\varphi$ 是共振项(回忆力学的受迫振动：共振)，因此括号两项当中只有 $2e\cos\varphi$ 项被保留，得到的解是<font color="blue">圆锥曲线</font>+<font color="#ff0000">共振</font>：
$$
u =  \frac{{G^2M^2}}{h^2}\left[ {\color{blue}1+e\cos\varphi} + {\color{red}3\left( \frac{GM}{hc} \right)^2 e\varphi\sin\varphi }\right]
\approx
\frac{{G^2M^2}}{h^2}\left[ 1+ e\cos \left(1-3\left( \frac{GM}{hc} \right)^2\right) \varphi \right]
$$
可见当水星运行 $\Delta \varphi$ 时，相对于零阶解，新轨道的相位会超前：
$$
\frac{\Delta \varphi}{1-3\left( \frac{GM}{hc} \right)^2} - \Delta\varphi \approx 3\left( \frac{GM}{hc} \right)^2 \Delta \varphi
$$
取一周 $\Delta \varphi = 2\pi$ 得到近地点在公转一周后的进动角度：
$$
\Delta = 6\pi \left( \frac{GM}{hc} \right)^2 \approx 0.1034'' \approx 5.014\times 10^{-7} ~ rad
$$
它给出的结果是 $\Delta \approx 43.03''/ century$，幸好对水星的观测能一直追溯到 1765 年，Clemence 在 1943 年分析了这些数据，得出 $\Delta = 43.11 \pm0.45''/century$，证实了这一预言。

![z_figure/Simulation_of_precessional_motion.png](/img/user/z_figure/Simulation_of_precessional_motion.png)   

