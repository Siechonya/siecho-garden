---
{"dg-publish":true,"permalink":"/理力25秋/Answer for HW7/","noteIcon":"default","created":"2025-12-01T13:39:23.665+08:00","updated":"2025-11-19T19:53:21.747+08:00"}
---

# 1 HW 7-1    
## 1.1 估算行星质量  
将行星 $m$ 和恒星 $M$ 视为双星系统，两者距离为 $r$，对于近似圆周运动，视向速度为三角函数，满足：  
$$
v  = \frac{2\pi r_M}{T} = \frac{2\pi}{T} \cdot \frac{m}{m+M}r
$$
双星的角速度容易根据万有引力 $=$ 向心力算出为：  
$$
\omega = \sqrt{\frac{G(m+M)}{r^3}} = \frac{2\pi}{T},\quad 该式亦为开三定律
$$
于是结合上述两式，消去其中的 $r$ 可得到：  
$$
v = \left( \frac{2\pi G}{T(m+M)^2} \right)^{1/3} m \approx \left( \frac{2\pi G}{TM^2} \right)^{1/3} m
\quad\to\quad
m \approx v\left( \frac{TM^2}{2\pi G} \right)^{1/3}
$$
得到  
$$
m \approx 57 \cdot\left( \frac{(4.23\times 24 \times 60 \times 60) \cdot (1.06 \times 1.989 \times 10^{30})^2}{2\pi \cdot 6.674 \times 10^{-11}} \right)^{1/3}  ~\text{kg} \approx 8.95 \times 10^{26} ~\text{kg} \approx 0.47 M_{Jupiter}
$$
## 1.2 势散射  
见朗道力学  
#### 前情提要  
![zz_figure/Pasted image 20251104210409.png](/img/user/zz_figure/Pasted%20image%2020251104210409.png)
#### (a)
![zz_figure/Pasted image 20251101115328.png](/img/user/zz_figure/Pasted%20image%2020251101115328.png)
![zz_figure/Pasted image 20251101115352.png](/img/user/zz_figure/Pasted%20image%2020251101115352.png)  

#### (b)  
朗道书中，$\chi$ 是散射角。
![zz_figure/Pasted image 20251101120410.png](/img/user/zz_figure/Pasted%20image%2020251101120410.png)
![zz_figure/Pasted image 20251101115517.png](/img/user/zz_figure/Pasted%20image%2020251101115517.png)
![zz_figure/Pasted image 20251101115533.png](/img/user/zz_figure/Pasted%20image%2020251101115533.png)  
![zz_figure/Pasted image 20251101115553.png](/img/user/zz_figure/Pasted%20image%2020251101115553.png)  
![zz_figure/Pasted image 20251101115612.png](/img/user/zz_figure/Pasted%20image%2020251101115612.png)
ps：上面的从(7)式往后的繁琐积分是没必要的，因为 $\mathrm{d}\sigma = 2\pi \rho \mathrm{d}\rho$，确定 $\rho$ 最大可取为 $a$ 后，其积分显然为 $\pi a^2$。  
## 1.3 有心力场  
> [!info]
> 改作业时发现很多同学竟然不会用 $V_{eff}$ 判断轨道是否有界，这是力学的内容。已知  
> $$
> E = \frac{1}{2} m \dot{r}^2 + V_{eff}
> \quad\Rightarrow\quad
> 0 = m\dot{r} \frac{ \mathrm{d} \dot{r} }{ \mathrm{d} r} + \frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r}
> $$
> 所以  
> - 假设 $\dot{r}>0$，所以朝着物体移动的方向： $r$ 增大的方向，若 $\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r} > 0$ 也即 $V_{eff}$ 增加就意味着 $\frac{ \mathrm{d} \dot{r} }{ \mathrm{d} r}<0$，即速度减小，粒子被束缚。
> - 假设 $\dot{r}<0$，所以朝着物体移动的方向： $r$ 减小的方向，若 $\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} (-r)} > 0\ or\ \frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r} < 0$ 也即 $V_{eff}$ 增加就意味着 $\frac{ \mathrm{d} \dot{r} }{ \mathrm{d} r}>0\ or\ \frac{ \mathrm{d} \dot{r} }{ \mathrm{d} (-r)}>0$，即速度减小，粒子被束缚。
> 
> 上述的情形对应如下图片当中 $E_1 < E < E_2,r_1<r<r_2$ 的片段：  
> ![zz_figure/Pasted image 20251115144621.png](/img/user/zz_figure/Pasted%20image%2020251115144621.png)
> 
> 画一条水平线，它的纵坐标为 $E$，因为 $E = \frac{1}{2} m \dot{r}^2 + V_{eff}$，所以若此时 $V_{eff}$ 曲线在该水平线下侧，那么水平线与 $V_{eff}$ 曲线的差距就是径向动能 $\frac{1}{2} m\dot{r}^2$，所以若初始时轨道在 $E_1 < E < E_2,r_1<r<r_2$ 的片段，那么运动就无法跨过区间两侧的势垒，否则 $\frac{1}{2} m\dot{r}^2<0$，物体被束缚。  
> 
> 若刚好 $E=E_2$，那么物体就只能待在极小值点，也就是做圆轨道运动。若 $E>E_1$ 并且从 $r<r_1$ 开始运动，那么就可以轻而易举地跨越势垒，导致运动无界。若 $E<E_1$，但物体没有运动到被束缚的区间 $r_1<r<r_2$，而是运动在 $r>r_2$，那么朝着 $r$ 增大的方向，径向动能 $\frac{1}{2} m\dot{r}^2$ 越大，轨道也是无界的。开普勒运动中，就是这样来区分三种轨道的。

#### (a)  线性力 $\vec{F}=-k\vec{r}$, $U=\frac{1}{2}kr^2$  

因为切换大小写过于麻烦，所以以下讨论用 $h$ 代替 $L$，约化质量 $\mu$ 代替 $m$.  

我们使用 binet 微商方程，做如下换元：  
$$
u  \equiv \frac{1}{r^2}
$$
那么  
$$
\frac{ \mathrm{d} u }{ \mathrm{d} \phi} = -\frac{2}{r^3} \frac{ \mathrm{d} r }{ \mathrm{d} \phi}
$$
$$
\dot{r} = \frac{ \mathrm{d} r }{ \mathrm{d} \phi} \dot{\phi} = -\frac{r^3}{2} \dot{\phi} \frac{ \mathrm{d} u }{ \mathrm{d} \phi} = -\frac{r}{2 } \frac{h}{\mu} \frac{ \mathrm{d} u }{ \mathrm{d} \phi} 
$$
同时能量守恒给出：  
$$
\frac{1}{2}\mu \dot{r}^2 = \frac{1}{8} \frac{h^2}{u\mu} \left( \frac{ \mathrm{d} u }{ \mathrm{d} \phi} \right)^2
=
E - \frac{h^2}{2\mu} u - \frac{k}{2u}
$$
整理第二个等号得到：  
$$
\left( \frac{ \mathrm{d} u }{ \mathrm{d} \phi } \right)^2 + 4u^2 - \frac{8E\mu}{h^2}u = -\frac{4k\mu}{h^2}
$$
改写为：  
$$
\left[ \frac{ \mathrm{d}  }{ \mathrm{d} \phi}\left( u-\frac{E\mu}{h^2} \right) \right]^2 + 4\left( u-\frac{E\mu}{h^2} \right)^2 = -\frac{4k\mu}{h^2} + 4\left( \frac{E\mu}{h^2} \right)^2
$$
该方程可分离变量求解，得到：  
$$
u = \frac{E\mu}{h^2} + \frac{E\mu}{h^2}\left( 1-\frac{kh^2}{E^2\mu} \right)^{1/2} \cos2(\phi - \phi_0) \equiv \frac{1}{r^2}
$$
做换元 $(x,y) = r(\cos\phi,\sin\phi)$ 并取 $\phi_0=0$ 可发现上式为圆锥曲线方程，其离心率满足：  
$$
\left( 1-\frac{kh^2}{E^2\mu} \right)^{1/2} = \frac{e^2}{2-e^2}
$$
离心率 $e$，或者说 $k$ 的正负(排斥或吸引势)，将确定轨道的形状。注意 $e$ 不但大于 $0$，还要小于 $\sqrt{2}$（因为上式为平方根，要大于 0）。   

此外，本题选用拉格朗日方程的方法可更快得到结果。（采用直角坐标，发现拉格朗日方程就是简谐振动方程） 

#### (b) 球方势阱 $V(r)=-V_{1}(r<a), V(r)=0(r>a)$  
假设 $V_1 > 0$。如果物体的瞄准距离 $d$ 大于 $a$, 显然只会<font color="#ff0000">(1)在球外做直线运动</font>，反之，轨道<font color="#ff0000">(2)在球内发生折射</font>或者<font color="#ff0000">(3)被束缚在球内</font>。

一般来说，可以分三种情形绘制如下 $V_{eff}$，以此确定轨道的有界还是无界，注意对于球外的物体，穿过球体的条件 $d<a$ 等价于 $E = \frac{1}{2}m v_{\infty}^2> \frac{L^2}{2 m a^2}$（对应于下图紫色区域，即 $E> \frac{L^2}{2m a^2}, 存在\ r<a$）  

![zz_figure/Capture_20251115_140716.jpg](/img/user/zz_figure/Capture_20251115_140716.jpg)


#### (c) 反比力  
见 [[理力25秋/Answer for HW6#1.3 T2\|HW6的T2]]，根据 $E$ 和 $\frac{h^2}{2 \mu} - k$ 的正负可确定轨道形状。通过 $V_{eff}$ 作图可以进一步确认轨道是否有界。

#### (d) Yukawa 势 $U(r)=-\frac{ke^{-\alpha r}}{r}$ 
对于 $V_{eff}(r)=\frac{h^2}{2\mu r^2}-\frac{ke^{-\alpha r}}{r}$，有  
$$
\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r} = -\frac{h^2}{\mu r^3} +k e^{-\alpha r} \frac{\alpha r+1}{r^2} = r^{-3} f(r), \ f(r) = ke^{-\alpha r}(\alpha r+1)r- \frac{h^2}{\mu}
$$
令 $\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r}=0$, 可以得到对应圆轨道的半径，在常见情形下($k>0,\alpha > 0$)，该方程有 0~2 个根（对应 $V_{eff}$ 有 0~2 个极值点）。据此可以画出 $V_{eff}(r)$ 的图像，根据直线 $V_{eff}=E$ 在途中的位置，可以将轨道分为几种类型：  

- 无界(类似抛物线/双曲线但与之偏离。或者从无穷远入射，环绕几圈后再返回无穷远); 
- 进动(类椭圆轨道的进动); 
- 圆(特殊情形，但处于势能极大时容易不稳定)。

所以根据 $\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r}=0$ 根的个数得到如下图： 

![zz_figure/Capture_20251115_141631.jpg](/img/user/zz_figure/Capture_20251115_141631.jpg)

对于最常见的第一种情形，$f(r)$ 在 $[0,+\infty)$ 区间上被 $V_{eff}$ 的两个极值点 $r_1,r_2$ 分割，符号变化为 ${\color{red} -} \to {\color{red} +} \to {\color{red} -}$，$f(r)$ 的极大值点由 $f'(r_0) = 0$ 得到, 为 $r_0 = \frac {{1+\sqrt{5}} }{ 2\alpha }$，由上述几个曲线可知，要使得轨道有界，必须存在 $\frac{ \mathrm{d} V_{eff} }{ \mathrm{d} r}=0$ 或者说存在 $f(r_{1,2}) = 0$ 成立，那么必须有  
$$
f(r_0) > 0
$$
于是得到  
$$
\alpha \frac{h^2}{\mu} < 2(2+\sqrt{5})ke^{-(\sqrt{5}+1)/2}
$$
若上式不成立，则轨道无界。反之，三种情况都有可能。

# 2 HW 7-2    
## 2.1 三维各向同性谐振子  
#### (a)  
将 $m\omega^2$ 替换为 $k$，$m$ 替换为约化质量 $\mu$，可得到与 [[理力25秋/Answer for HW7#(a) 线性力 $ vec{F}=-k vec{r}$, $U= frac{1}{2}kr 2$\|HW7-1第三题(a)]] 一致的结果。题目要求用积分求解，助教在这里偷个懒，就不细算了。

#### (b)  
取 $\phi_0=0$，以及：  
$$
u = \frac{mE}{L^2} + \frac{mE}{L^2}\left( 1-\frac{\omega^2L^2}{E^2} \right)^{\frac{1}{2}} \cos2\phi \equiv \frac{1}{r^2}
,\quad
\left( 1-\frac{\omega^2L^2}{E^2} \right)^{\frac{1}{2}} = \frac{e^2}{2-e^2}
$$
代入 $(x,y) = r(\cos\phi,\sin\phi)$ 得到：
$$
(A+B)x^2 + \left( A-B \right)y^2 = 1,\quad A = \frac{mE}{L^2},\quad B = \frac{mE}{L^2}\left( 1-\frac{\omega^2L^2}{E^2} \right)^{\frac{1}{2}} < A 
$$
或者，  
$$
r  = \frac{p}{1+e\cos\theta},
\quad \frac{1}{a^2} = A-B>0, \quad \frac{1}{b^2} = A+B
$$
这保证了轨道是椭圆($0\leq e \leq 1$)，联立后两式可得：  
$$
E = \frac{1}{2}m\omega^2(a^2+b^2),\quad L = m\omega ab
$$

#### (c)
面积速度是  
$$
\kappa = rv_\perp = \frac{L}{m} = \omega ab
$$
而熟知的椭圆面积是  
$$
S = 2\pi ab
$$
于是得到  
$$
T = \frac{S}{\kappa} = \frac{2\pi}{\omega}
$$
而对于求解 $r=r(t)$，根据 $t = \int \frac{\text{d} r}{\sqrt{\frac{2}{m} \left[ E - U(r) \right] - \frac{L^2}{m^2 r^2}}}$ 有： 
$$
\begin{aligned}
t &= \int \frac{\text{d} r}{\sqrt{\frac{2}{m} \left( E - U - \frac{L^2}{2 m r^2} \right)}} = \sqrt{\frac{m}{2}} \int \frac{\text{d} r}{\sqrt{E - \frac{1}{2}m\omega^2 r^2 - \frac{L^2}{2 m r^2}}} \\[4pt]
&= \sqrt{\frac{m}{2}} \int \frac{r \text{d} r}{{\sqrt{ - \frac{1}{2}m\omega^2 r^4 + Er^2 - \frac{L^2}{2 m}}}} \\[4pt]
&= \frac{1}{\omega} \int \frac{r \text{d} r}{{\sqrt{ - r^4 + \frac{2E}{m\omega^2}r^2 - \frac{2L^2}{m^2\omega^2}}}}
\end{aligned}
$$
看了一眼题目给的结果，选择做换元 $u = r'^2 = r^2 - \frac{E}{m\omega^2}$ 得到  
$$
\begin{aligned}
t &= \frac{1}{2\omega} \int \frac{\text{d} u}{{\sqrt{ - u^2 +\frac{E^2}{m^2\omega^4}- \frac{2L^2}{m^2\omega^2}}}}
\end{aligned}
$$
因为分母当中 $\frac{E^2}{m^2\omega^4}- \frac{2L^2}{m^2\omega^2} \propto (a^2+b^2)^2 - 2a^2b^2>0$，所以只有唯一解：  
$$
r'^2 = -\frac{E}{m\omega^2}\sqrt{1-\frac{\omega^2L^2}{E^2}} \cos 2\omega(t-t_0)
$$
## 2.2 势散射  
#### (a)  
与 [[理力25秋/Answer for HW7#(a)\|HW7-1第2题(a)]] 同理，不赘述。  
#### (b) (c)
题目中的碰撞参数 $b$ 是瞄准距离，此题与 [[理力25秋/Answer for HW7#(b)\|HW7-1第2题(b)]] 相同，两者的结果分别是 [[理力25秋/Answer for HW7#(b)\|HW7-1第2题(b)]] 的(5)式和(6)式。
## 2.3 $r^{-2}$ 势散射
#### 2.3 (a)  
此题对应于 [[理力25秋/Answer for HW6#1.3 T2\|HW6第二题的第一种情形]]，对当时给出的结果做一下字母替换，得到同样适用于本题的结论：  
$$
\frac{1}{r} = \sqrt{\frac{2 m E}{L^2 + 2 m k}} \cos \left( \varphi \sqrt{1 - \frac{2 m L}{M^2}} \right)
$$
$$
r_{0} = \sqrt{\frac{L^2 + 2 m k}{2 m E}}, \quad \alpha = \sqrt{1 - \frac{2 m L}{M^2}}
$$
#### (b) (c) 
见朗道力学：  
![zz_figure/Pasted image 20251104210455.png](/img/user/zz_figure/Pasted%20image%2020251104210455.png)  
![zz_figure/Pasted image 20251104210507.png](/img/user/zz_figure/Pasted%20image%2020251104210507.png)
![zz_figure/Pasted image 20251105224512.png](/img/user/zz_figure/Pasted%20image%2020251105224512.png)








