---
{"dg-publish":true,"permalink":"/A_symmetry_自然界的对称性/杂记/3-D Laplace Equation And Spherical Harmonic Function/","noteIcon":"default","created":"2025-03-23T22:36:48.350+08:00","updated":"2025-12-10T18:48:05.427+08:00"}
---



```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 6 # Include headings up to the specified level
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```

# 1 3D Laplace Equation    
三维拉普拉斯方程方程可记成多种形式:
$$
\begin{aligned}
\Delta u &= \nabla^2 u = \nabla \cdot \nabla u = 0 \\
&= 
\frac{1}{r^2} \frac{ \partial  }{ \partial r }\left( r^2 \frac{ \partial u }{ \partial r } \right) 
+ \frac{1}{r^2 \sin\theta}\frac{ \partial  }{ \partial \theta }\left( \sin\theta\frac{ \partial u }{ \partial \theta } \right) 
+ \frac{1}{r^2 \sin^2\theta} \frac{ \partial^2 u }{ \partial^2 \varphi }
\end{aligned}
$$
对其分离变量 $u(r,\theta,\varphi) = R(r)Y(\theta,\varphi)$, 容易得到
$$
\frac{1}{R} \frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right)
= - \frac{1}{Y}  \left(\frac{1}{\sin \theta } \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right)-\frac{1}{\sin ^{2} \theta} \frac{\partial^{2} Y}{\partial \phi^{2}}\right)
= \lambda
$$
# 2 径向衰减
常常选取 $\lambda = l(l+1)$, 于是
$$
\frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right) - l(l+1)R = 0
$$
这是欧拉方程, 根据换元 $r=e^s$ 得到它的通解是
$$
R(r) = A r^l + B r^{-(l+1)}, \quad l\geq 0
$$
通常情况下, 场不会传播到无穷远处, 也就是在解 $R(r)$ 的定义域包含 $r=\infty$ 时因为 $r^l \to \infty$ 导致 $R(r)\to\infty$ 而不满足物理意义, 所以通常取 $A=0$. 同理, 在解的定义域包含 $r=0$ 时, 通常取 $B=0$.
# 3 球面谐波  
## 3.1 球谐函数的引出
由上述已知, 拉普拉斯方程的球面偏导部分是
$$
\frac{1}{\sin \theta } \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right)
-\frac{1}{\sin ^{2} \theta} \frac{\partial^{2} Y}{\partial \phi^{2}} 
+ l(l+1)Y
= 0
$$
进一步分离变量 $Y(\theta, \varphi) = \Theta(\theta)\Phi(\varphi)$, 有
$$
\left\{
\begin{array}l
\frac{ d^2 \Phi }{ d^2 \varphi} + m^2 \Phi = 0 \\[4pt]
\Phi(\varphi) = \Phi(\varphi + 2\pi)
\end{array}
\right. \tag{1}
$$
$$
\begin{array}l
\sin \theta \frac{d}{d \theta}\left(\sin \theta \frac{d \Theta}{d \theta}\right)+\left[(l+1) l \sin ^{2} \theta-m^{2}\right] \Theta=0
\end{array}\tag{2}
$$
方程(1)没什么好说的, 解是 $\Phi_m(\varphi) = e^{im\varphi}$. 对方程(2)做换元 $\theta = \arccos x$, 得到
$$
\left(1-x^{2}\right) \frac{d^{2} \Theta}{d x^{2}}-2 x \frac{d \Theta}{d x}+\left[l(l+1)-\frac{m^{2}}{1-x^{2}}\right] \Theta=0 \tag{3}
$$
这被称为连带勒让德方程. 特别的, 当 $m=0$ 时, 上式退化为勒让德方程:
$$
\Theta\to P_l:\quad
\left(1-x^{2}\right) \frac{d^{2} P_l}{d x^{2}}-2 x \frac{d P_l}{d x}+ l(l+1) P_l=0 \tag{4}
$$
该方程的解就是勒让德函数 $P_l(x)$.

对连带勒让德方程(3)做换元 $y(x) = \Theta(x) (1-x^2)^{-\frac{m}{2}}$, 可得到
$$
\begin{align}
\Theta 
&= (1-x^2)^{\frac{m}{2}} y \\[6pt]
\Theta'
&=\left(1-x^{2}\right)^{\frac{m}{2}} y^{\prime}-m\left(1-x^{2}\right)^{\frac{m}{2}-1} x y \\[6pt]
\Theta''
&=\left(1-x^{2}\right)^{\frac{m}{2}} y^{\prime \prime}-2 m\left(1-x^{2}\right)^{\frac{m}{2}-1} x y^{\prime}-m\left(1-x^{2}\right)^{\frac{m}{2}-1} y
+m(m-2)\left(1-x^{2}\right)^{\frac{m}{2}-2} x^{2} y 
\\[10pt]
&\Rightarrow
\left(1-x^{2}\right) y^{\prime \prime}-2(m+1) x y^{\prime}+[l(l+1)-m(m+1)] y=0 \tag{5}
\end{align}
$$
将该方程与勒让德方程(4)做比较, 先对勒让德方程求导 $m$ 次, 记 $P_l^{(m)}$ 表示对 $P_l$ 求 $m$ 次导, 利用莱布尼兹公式 $(uv)^{(m)} = \sum_{k=0}^{m} \binom{m}{k} u^{(m-k)} v^{(k)}$, 可以得到
$$
\begin{aligned}
0 &=
\left[ \left(1-x^{2}\right)  P^{(2)}_l-2 x P_l^{(1)}+ l(l+1) P_l \right]^{(m)}=0 
\\[4pt]
&=
{\left[ \left(1-x^{2}\right) P_l^{(m+2)} -2mx P_l^{(m+1)} -{m(m-1)} P_l^{(m)} \right]
-2\left[ x P_l^{(m+1)}+m P_l^{(m)} \right]}
+l(l+1) P_l^{(m)}
\\[4pt]
&=
\left(1-x^{2}\right) P_l^{(m+2)}-2(m+1) x P_l^{(m+1)}+\left[l(l+1)-m(m+1)\right] P_l^{(m)}
\end{aligned}
$$
这恰好和式(5)的形式一致, 也就是说方程(5)的解是  
$$
y_l^m = \frac{ d^m }{ d x^m} P_l(x), \quad |m| \leq l
$$
那么连带勒让德方程(3)的解记为连带勒让德函数 $P_l^m(x)$, 回忆前面做过换元 $y(x) = \Theta(x) (1-x^2)^{-\frac{m}{2}}$, 那么
$$
\boxed{
P_l^m(x) = (1-x^2)^{\frac{m}{2}} \frac{ d^m }{ d x^m} P_l(x), \quad |m| \leq l
}
$$
所以, 最后的球谐函数就是
$$
Y_l^m (\theta, \varphi) = P_l^m(\cos\theta)\Phi_m(\varphi)
$$
如果要归一化 $Y$, 也就是令 $\int_0^{2\pi} \mathrm{d}\varphi \int_0^{\pi} Y_l^m (\theta, \varphi) \sin\theta \mathrm{d}\theta = 1$, 则可以得到归一化的球谐函数:
$$
Y_l^m (\theta, \varphi) = \sqrt{\frac{1}{2\pi} \frac{2l+1}{2} \frac{(l-m)!}{(l+m)!}} ~P_l^m(\cos\theta) e^{\boldsymbol{i}m\varphi}
$$
于是 $\nabla^2 u = 0$ 的通解表示为
$$
u(r, \theta,\varphi) 
= R(r)Y_l^m(\theta,\varphi)
= \sum_{l=0}^{\infty} \sum_{m=-l}^{l}
\left(A r^l + B r^{-(l+1)}\right)  \sqrt{\frac{1}{2\pi} \frac{2l+1}{2} \frac{(l-m)!}{(l+m)!}} ~P_l^m(\cos\theta) e^{\boldsymbol{i}m\varphi}
\tag{6}
$$
另外, 这里列出连带勒让德函数的前几项:
$$
\begin{aligned}
P_0^0(x) &= 1, \\[3pt]
P_1^0(x) &= x, \quad P_1^1(x) = -\sqrt{1 - x^2}, \\[3pt]
P_2^0(x) &= \frac{1}{2}(3 x^2 - 1), \quad P_2^1(x) = -3 x\sqrt{1 - x^2}, \quad P_2^2(x) = 3(1 - x^2), \\[2pt]
P_3^0(x) &= \frac{1}{2}(5 x^3 - 3 x), \quad P_3^1(x) = -\frac{3}{2}(5 x^2 - 1)\sqrt{1 - x^2}, \quad
P_3^2(x) = 15 x(1 - x^2), \quad P_3^3(x) = -15(1 - x^2)^{3/2}.
\end{aligned}
$$
## 3.2 $Y_1^m$ 和偶极场
在静磁学中, 如果场点不存在电流($\nabla \times \vec B = 0$), 那么磁感应强度 $\vec B$ 可以表示成磁标势 $\Phi_m$ 的梯度 $\vec B = -\nabla \Phi_m$, 并且由于 $\nabla \cdot \vec B=0$, 所以磁标势自动满足拉普拉斯方程 $\nabla^2 \Phi_m = 0$. 在其通解形式中, 前几项球谐函数有显著的物理意义.

上述的归一化球谐函数中, $Y_1^0(\theta) = \sqrt{\frac{3}{4\pi}}\cos\theta \propto \cos\theta = \frac{z}{r}$, $R_1(r)=Ar+\frac{B}{r^2} = \frac{B}{r^2}$ (取 $A=0$). 于是 $\Phi_m$ 的一个解可以写作
$$
\Phi_{pole}(r, \theta, \varphi) = \frac{C}{r^2} \cos\theta, \quad C = \text{const}
$$
求梯度得到
$$
\vec B = - \left( \partial_r \Phi_{pole},\ \frac{1}{r}\partial_\theta\Phi_{pole},\ 0 \right)
=C\cdot \left( \frac{2\cos\theta}{r^3},\ \frac{\sin\theta}{r^3},\ 0 \right)
$$
回忆磁偶极子在远处的磁场表达式:
$$
\vec B = \frac{\mu_0}{4\pi} \frac{{3 (\vec n\cdot \vec m)\vec n - \vec m}}{r^3} 
=
\frac{\mu_0}{4\pi} \frac{{3 \cos\theta\vec e_r - \vec e_z}}   {r^3} 
=
\frac{\mu_0}{4\pi} \frac{{3 \cos\theta\vec e_r - (\cos\theta\vec e_r - \sin\theta \vec e_\theta)}}   {r^3} 
=
\frac{\mu_0}{4\pi} \frac{{2 \cos\theta\vec e_r +  \sin\theta \vec e_\theta}}   {r^3} 
$$
发现两式形式一致, 只要取 $C=\frac{\mu_0}{4\pi}$, 就可以用球谐函数 $Y_1^0$ 描述偶极磁场.

另外, 由于 $Y_1^{\pm 1}$ 是虚数, 所以为保证物理意义, 选取它们的实数线性组合 $Y_1^x = \frac{Y_1^1 + Y_1^{-1}}{\sqrt{2}}$ 和 $Y_1^y = \frac{Y_1^1 - Y_1^{-1}}{i\sqrt{2}}$, 显然 $Y_1^x \propto \sin\theta\cos\varphi = \frac{x}{r}$,  $Y_1^y \propto \sin\theta\sin\varphi = \frac{y}{r}$ 为实数. 对于三维旋转, 考察球谐函数的变换, 比如在直角坐标系中, 绕 $y$ 轴旋转的变换矩阵是
$$
   R_y(\beta) = \begin{pmatrix}
   \cos\beta & 0 & \sin\beta \\
   0 & 1 & 0 \\
   -\sin\beta & 0 & \cos\beta
   \end{pmatrix}
   $$
变换导致 $(x,y,z)\to(x',y',z'),(r,\theta,\varphi)\to(r',\theta',\varphi')$, 即:
$$
\begin{aligned}
   \theta' &= \arccos\left(\frac{z'}{r}\right) = \arccos\left(\frac{-x \sin\beta + z \cos\beta}{r}\right)\\
   & =
   \arccos\left( -\sin\theta\cos\varphi \sin\beta + \cos\theta \cos\beta \right)
   \end{aligned}
   $$
$$
\begin{aligned}
   \varphi' &= \arctan 2(y',\ x') = \arctan 2(y,\ x \cos\beta + z \sin\beta) \\
   &= 
   \arctan 2( \sin\theta\sin\varphi,\ \sin\theta\cos\varphi \cos\beta + \cos\theta \sin\beta)
 \end{aligned}
   $$
如果取 $\beta=\frac{\pi}{2}$, 就有
$$
\begin{aligned}
   \theta' =
   \arccos\left( -\sin\theta\cos\varphi \right)
   \end{aligned}
   $$
$$
\begin{aligned}
   \varphi'  =
   \arctan \left(  \frac{{\sin\theta\sin\varphi}}{\cos\theta} \right)
 \end{aligned}
   $$
也就是说, 在绕 $y$ 轴旋转 $90^\circ$ 后, $Y_1^x$ 变成了描述朝向 $z$ 轴的偶极子 $Y_1^0$ :   
$$
\begin{aligned}
Y_1^x(\theta',\varphi') \propto \sin\theta'\cos\varphi'
&=
\sin( \arccos\left( -\sin\theta\cos\varphi \right)) \ \cdot\  \cos\left( \arctan \left(  \frac{{\sin\theta\sin\varphi}}{\cos\theta} \right) \right) \\
&=
\sqrt{1-(\sin\theta\cos\varphi)^2} \ \ \cdot  \frac{1}{\sqrt{ 1+ \left( \frac{{\sin\theta\sin\varphi}}{\cos\theta} \right)^2}} \\
&=
\sqrt{1-(\sin\theta\cos\varphi)^2} \ \ \cdot  \frac{\cos\theta}{\sqrt{ \cos^2\theta+ \left( {\sin\theta\sin\varphi} \right)^2}} \\
&=
\cos\theta\\\\
&\propto
Y_1^0 (\theta)
\end{aligned}
$$
因此, $Y_1^x$ 实际上描述的是沿 $x$ 轴方向的磁偶极子, 类似的知道 $Y_1^y$ 描述沿 $y$ 轴方向的磁偶极子. 在量子力学里面, 上面的旋转操作可以用 $Winger-D$ 矩阵作用于球谐函数得到, 这个矩阵的元素很丑陋, 可以在 $MMA$ 中直接调用 $Winger-D$ 函数快速计算.
## 3.3 $Y_2^m$ 和四极场
同理, 对于归一化球谐函数 $Y_2^0(\theta) = \sqrt{\frac{5}{16\pi}} \left(3\cos^2\theta - 1\right)$, 磁标势 $\Phi_{\text{quad}}(r, \theta) = R \cdot g_2^0 \left(\frac{R}{r}\right)^3 \sqrt{\frac{5}{16\pi}} \left(3\cos^2\theta - 1\right)$, $g_2^0$ 为常数, 计算得到
$$
\begin{array}c
B_r = -\frac{\partial \Phi}{\partial r} = 3 g_2^0 \left(\frac{R^4}{r^4}\right) \sqrt{\frac{5}{16\pi}} \left(3\cos^2\theta - 1\right)
   \\
B_\theta = -\frac{1}{r} \frac{\partial \Phi}{\partial \theta} = 3 g_2^0 \left(\frac{R^4}{r^4}\right) \sqrt{\frac{5}{16\pi}} \sin2\theta
\\
B_\varphi = 0 
\end{array}
$$
关于球谐系数 $g_l^m$ 的具体拟合值, 可在第 $14$ 版[国际参考地磁场(IGRF)的官方文件](https://www.ngdc.noaa.gov/IAGA/vmod/coeffs/igrf14coeffs.txt) 中查阅. 对于 $m\ne 0$ 的球谐函数, 同样选取他们的实数线性组合, 可以得到他们表示的四极场只是 $Y_2^0(\theta)$ 的旋转, 但是形式更加复杂.

# 4 球谐系数
现在需要确定系数 $B_{lm}$, 假设 $A=0$, 通解写成:
$$
u(r, \theta, \varphi)=\sum_{l=0}^{\infty} \sum_{m=-l}^{l} \frac{B_{l m}}{r^{l+1}} Y_{l}^{m}(\theta, \varphi)
$$
其中 $Y_{l}^{m}(\theta, \varphi)=\sqrt{\frac{(2 l+1)}{4 \pi} \frac{(l-m)!}{(l+m)!}} P_{l}^{m}(\cos \theta) e^{i m \varphi}$, 它是正交归一化的:
$$
\int_{0}^{2 \pi} \int_{0}^{\pi} Y_{l}^{m}(\theta, \varphi) Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi) \sin \theta d \theta d \varphi=\delta_{l l^{\prime}} \delta_{m m^{\prime}}
$$
将通解两边乘以 $Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi)$, 然后积分:
$$
\int_{0}^{2 \pi} \int_{0}^{\pi} u(r, \theta, \varphi) Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi) \sin \theta \mathrm{d} \theta \mathrm{d} \varphi =
\sum_{l=0}^{\infty} \sum_{m=-l}^{l}  \frac{B_{l m}}{r^{l+1}} \int_{0}^{2 \pi} \int_{0}^{\pi} Y_{l}^{m}(\theta, \varphi) Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi) \sin \theta \mathrm{d} \theta \mathrm{d} \varphi
$$

利用正交归一关系, 右边只剩下 $l=l^{\prime}$ 且 $m=m^{\prime}$ 时的项：
$$
\int_{0}^{2 \pi} \int_{0}^{\pi} u(r, \theta, \varphi) Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi) \sin \theta \mathrm{d} \theta \mathrm{d} \varphi = \frac{B_{l^{\prime} m^{\prime}}}{r^{l^{\prime}+1}}
$$
从而可解出:
$$
B_{l^{\prime} m^{\prime}}= \int_{0}^{2 \pi} \int_{0}^{\pi} u(r, \theta, \varphi) Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi) \sin \theta \mathrm{d} \theta \mathrm{d} \varphi 
$$

