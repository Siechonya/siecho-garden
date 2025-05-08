---
{"dg-publish":true,"permalink":"/EMD_answer/Answer_for_HW4/","created":"2025-04-19T20:32:55.625+08:00"}
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


# 1. 带电半球受力
带电球电场:
$$
\vec E(r) = 
\left\{
\begin{aligned}
\frac{Qr}{4\pi \epsilon_0 R^3} \vec e_r, \quad r \leq R \\
\frac{Q}{4\pi\epsilon_0 r^2}\vec e_r, \quad r > R
\end{aligned}
\right.
$$
得到:
$$
T_{ij} = \epsilon_0 E_iE_j - \frac{1}{2}\epsilon_0 E^2 \delta_{ij} 
\quad\to\quad
T_{xz} = T_{yz} = 0, T_{zz} = -\frac{1}{2}\epsilon_0 E^2, at\ z=0
$$
$r \to \infty$ 时 $\int \boldsymbol{T}\cdot d\vec S \to 0$ 忽略, 则:
$$
\begin{aligned} 
\vec F = \vec e_z \int T_{zz}dS_z 
&=
\vec e_z \int_0^\infty \left( -\frac{1}{2}\epsilon_0 E^2 \right) (-2\pi r \mathrm{d} r)
\\ 
&=
\vec e_z \int_0^R \epsilon_0 \left(\frac{Qr}{4\pi \epsilon_0 R^3}\right)^2 (\pi r \mathrm{d} r) 
+ \vec e_z \int_R^\infty \epsilon_0 \left(\frac{Q}{4\pi\epsilon_0 r^2}\right)^2 (\pi r \mathrm{d} r)\\
&=
\frac{3Q^2}{64 \pi \epsilon_0 R^2} \vec e_z
\end{aligned}
$$
# 2. 磁矢势的洛伦茨规范
已知 $\vec A = \frac{\mu_0}{4\pi}\int \frac{{\vec j(\vec x')}}{|\vec r|}dV'$, 其中 $\vec r = \vec x - \vec x'$. 记 $\nabla' = \frac{ \partial  }{ \partial \vec x' }$, 有:
$$
\begin{aligned} 
\nabla \cdot \vec A 
& \propto
\nabla \cdot \int \frac{{\vec j(\vec x')}}{|\vec r|}~\mathrm{d}V'
\\ 
&=
\int  {{\vec j(\vec x')}} \nabla \frac{1}{r} ~\mathrm{d}V' \\
\small{\color{red} \nabla \frac{1}{r} = -\nabla' \frac{1}{r} \quad\to\quad}
&= - \int  {{\vec j(\vec x')}} \nabla' \frac{1}{r} ~\mathrm{d}V' \\
&=
\underset{边界无电流=0}{\underbrace{ -\int \nabla' \cdot  \frac{{\vec j(\vec x')}}{r}~\mathrm{d}V' } }
+
\int \underset{稳恒磁场\nabla \cdot \vec j = \frac{ \partial \rho }{ \partial t } = 0}{\underbrace{\frac{\nabla' \cdot  {\vec j(\vec x')}}{r}  ~\mathrm{d}V' }}
\\
&= 0
\end{aligned}
$$
因此对于静磁场, $\partial_t \phi = 0$, 得到洛伦茨规范成立:
$$
\Box \cdot  \vec A  = 0
$$
# 3. 静电场多极展开
## (1) 零阶和一阶场
已知离散形式的电场: $\vec E(\vec x - \vec x') = \frac{1}{4\pi\epsilon_0} \sum q(x') \frac {{\vec x - \vec x'}} {|\vec x - \vec x'|^3} = \vec E^0 + \vec E^1 + \cdots$, 记 $r = |\vec x| \gg |\vec x'|$, $\hat r = \frac{\vec x}{r}$, 偶极矩 $\vec p = \sum q\vec x'$, 则根据泰勒展开有:
$$
\vec E^0 = \vec E(\vec x) = \frac{1}{4\pi\epsilon_0} \sum q \frac {\hat r} {r^2}
$$
以及:
$$
\begin{aligned}
\vec E^1 &=
- \vec x' \cdot \nabla \vec E(\vec x)
\\ 
&=
- \vec x' \cdot \nabla  \frac{1}{4\pi\epsilon_0} \sum q \frac {\hat r} {r^2}
\\
&=
\frac{1}{4\pi\epsilon_0} \sum q \left[  - \frac{\hat r}{r^2} + \frac{{({3\vec x' \cdot \hat r})\hat r}}{r^3} \right] \\
&=
\frac{1}{4\pi\epsilon_0}  \frac{{-\vec p + 3\vec p \cdot \hat r \hat r}}{r^3}
\end{aligned}
$$
## (2) 小电荷体系受力矩
小电荷体系位于 $\vec r'$, 所受力矩可写作:
$$
\vec N(\vec r') = \sum\vec r'\times q\vec E(\vec r') = \sum \vec p\times \vec E(\vec r') = \vec N^0 + \vec N^1 + \cdots
$$
于是根据麦克劳林展开有:
$$
\vec N^0 = \sum q_i \vec 0 \times \vec E(0) = 0
$$
$$
\begin{aligned}  
\vec N^1 &= 
\sum \vec r' \cdot \nabla q\vec r \times E(\vec r)|_{\vec r = 0}
\\ 
&= 
\sum \nabla \left(  \vec r' \cdot q\vec r \times E(\vec r) \right)|_{\vec r = 0}   \\
&=
\sum \nabla (q\vec E(\vec r) \cdot \vec r' \times \vec r)|_{\vec r = 0}  \\
&=
\sum q \{
\vec E \times (\vec r' \times \underset{=0}{\underbrace{(\nabla \times \vec r)} }  )
+ (\vec r' \times \vec r) \times \underset{=0}{\underbrace{(\nabla \times \vec E)} }  
+ \vec r' \times \underset{=\vec E}{\underbrace{ (\vec E \cdot \nabla )\vec r} }
+ ((\vec r' \times \underset{=0}{\underbrace{ \vec r} }) \cdot \nabla)\vec E
\}
\\
&=
\sum q\vec r' \times \vec E\\
&=
\vec p \times \vec E(0)
\end{aligned}
$$
# 4. 均匀带电球的全空间能量
电荷分布
$$
\rho(r) = \left\{
\begin{aligned}
&\frac{3Q}{4\pi R^3} &r\leq R
\\
&0 & r>R
\end{aligned}
\right.
$$
于是由电场散度得到电场的分布:
$$
\vec E(r) = \left\{
\begin{aligned}
&\frac{Qr}{4\pi\epsilon_0 R^3}
&r\leq R
\\
&\frac{Q}{4\pi \epsilon_0 r^2}
& r>R
\end{aligned}
\right.
$$
电势分布
$$
\phi(r) = \left\{
\begin{aligned}
&
 \int_r^R \frac{Qr}{4\pi\epsilon_0 R^3}\mathrm{d} r + \int_R^{+\infty} \frac{Q}{4\pi \epsilon_0 r^2} \mathrm{d}r
 = \frac{Q}{4\pi \epsilon_0 R} \left( \frac{3}{2} - \frac{r^2}{2R^2} \right)
&r\leq R
\\
&- & r>R
\end{aligned}
\right.
$$
于是得到能量:
$$
W = \frac{1}{2}\int_0^R \rho(r)\phi(r) ~r^2 \mathrm{d} r \int_0^\pi \sin\theta\mathrm{d}\theta \int_0^{2\pi}\mathrm{d}\varphi
= \frac{3Q^2}{20\pi \epsilon_0 R}
$$
同理
$$
W = \frac{1}{2}\epsilon_0\int_0^{\color{red}+\infty} E^2 ~r^2 \mathrm{d} r \int_0^\pi \sin\theta\mathrm{d}\theta \int_0^{2\pi}\mathrm{d}\varphi
= \frac{3Q^2}{20\pi \epsilon_0 R}
$$
# 5. 线性介质的静电场能量密度
已知:
$$
\begin{aligned} 
\frac{ \partial w }{ \partial t } + \nabla \cdot  (\vec E \times \vec H) = -\vec E \cdot \vec j &&(1)
\\ 
\nabla \times \vec E = -\frac{ \partial \vec B }{ \partial t } &&(2)
\\
\nabla \times \vec H = \vec j  + \frac{ \partial \vec D }{ \partial t } &&(3)
\end{aligned}
$$
(3)带入(1)右侧得到:
$$
\begin{aligned}
\vec E \cdot \vec j &= \vec E \cdot \left( \nabla \times \vec H - \frac{ \partial \vec D }{ \partial t } \right) \\
&= 
(\vec E \cdot \nabla \times \vec H - \vec H\cdot \nabla \times \vec E) + \vec H\cdot \nabla \times \vec E - \vec E \cdot \frac{ \partial \vec D }{ \partial t } \\
&\overset{(2)}{=}
-\nabla \cdot (\vec E \times \vec H) - \vec H\cdot \frac{ \partial \vec B }{ \partial t } - \vec E \cdot \frac{ \partial \vec D }{ \partial t } \\
&=
-\nabla \cdot (\vec E \times \vec H) - \frac{1}{2}\frac{ \partial \vec H\cdot \vec B }{ \partial t } - \frac{1}{2}\frac{ \partial \vec E \cdot \vec D }{ \partial t }
\end{aligned}
$$
所以在没有磁场时:
$$
w = \frac{1}{2} \vec E \cdot \vec D
$$
# 6. 课本题
## 1.7
-  (1)
易知:
$$
\vec E(r)=\left\{\begin{array}{ll}
0 &r<r_{1} \\
\frac{\rho_{f}}{4\pi\epsilon} \frac{\frac{4}{3} \pi\left(r^{3}-r_{1}^{3}\right)}{r^{2}}=\frac{\rho_{f}\left(r^{3}-r_{1}^{3}\right)}{3 \varepsilon r^{2}} \vec {e}_{r}  & r<r<r_{2} \\
\frac{\rho_{f}}{4 \pi \varepsilon_{0}} \frac{\frac{4}{3}\left(r_{2}^{3}-r_{1}^{3}\right)}{r^{2}}=\frac{\rho_{f}\left(r_{2}^{3}-r_{3}^{3})\right.}{3 \varepsilon_{0} r^{2}} \vec{e}_{r} & r>r_{2}
\end{array}\right.
$$
-  (2) 
由 $\vec{p}=\left(\varepsilon-\varepsilon_{0}\right) \vec{E}$ 可得:
$$
\quad \sigma_{p}=
\left\{\begin{array}{lr}
{\left[\vec{p}\left(r<r<r_{2}\right)-\vec{p}\left(r<r_{1}\right)\right] \cdot\left(-\vec{e}_{r}\right)=-\left(\varepsilon-\varepsilon_{0}\right) \frac{\rho_{f}\left(r^{3}-r_{r}^{3}\right)}{3 \varepsilon r^{2}}=0} & r=r_{1} \\ 
{\left[\vec{p}\left(r_{1}<r<r_{2}\right)-\vec{p}\left(r>r_{2})\right] \cdot \vec{e}_{r}=\left(\varepsilon-\varepsilon_{0}\right) \frac{\rho_{f}\left(r_{2}^{3}-r_{1}^{3}\right)}{3 \varepsilon r^{2}}\right.} & r=r_{2}
\end{array}\right. 
$$
$$
\rho_{p}=-\nabla \cdot \vec{P}\left(r_{1}<r<r_{2}\right)
=-\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) \frac{\rho_{f}}{3}\left[\nabla \cdot \vec{r}-r_1^{3} \nabla \cdot  \frac{{\vec r}}{r^3} \right]=-\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) \rho_{f} \quad r_{1}<r<r_{2}
$$
## 1.9
$$
\begin{aligned}
\rho_f 
&= - \nabla \cdot \vec P  \\
&= - \nabla \cdot (\epsilon - \epsilon_0)\vec E \\
\small{\color{red} \nabla \cdot \vec E = \frac{\rho_f}{\epsilon}\quad\to\quad}
&=
-\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) \rho_{f}
\end{aligned}
$$
## 2.1
-  (1)
$$
 \rho_{p}(r<R)=-\nabla \cdot \vec{p}=-k \nabla \cdot \frac{\vec{r}}{r^{2}}=-k\left[\frac{3 r^{2}-2\left(x^{2}+y^{2}+z^{2}\right)}{r^{4}}\right]=-k / r^{2} 
$$
$$
\sigma_{p}(r=R)=\vec{p} \cdot \vec{e}_{r} |_{r=R}=k / R
$$
-  (2)
$$
\rho_{f}=\rho_{p} /\left(\frac{\varepsilon_{p}}{\varepsilon}-1\right)=\frac{k}{\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) r^{2}} \quad(r<R)
$$
-  (3)
$$
E(r)=\left\{\begin{array}{l}\int_{0}^{R} \int_{0}^{\pi} \int_{0}^{2 \pi} \rho_{f} ~r^{2} \sin \theta \mathrm{d} r \mathrm{d} \theta \mathrm{d} \varphi \cdot \frac{1}{4 \pi \varepsilon_{0} r^{2}}=\frac{k R}{\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) \varepsilon_{0} r^{2}} \vec{e}_{r} \quad r\geq R \\
\int_{0}^{r} \int_{0}^{\pi} \int_{0}^{2 \pi} \rho_{f} ~r^{2} \sin \theta \mathrm{d} r \mathrm{d} \theta \mathrm{d} \varphi \cdot \frac{1}{4 \pi \varepsilon r^{2}}=\frac{k}{\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) \varepsilon r} \vec{e}_{r} \quad 0<r<R\end{array}\right. 
$$
$$
\therefore \varphi(r)=\left\{\begin{array}{l}
\int_{r}^{+\infty} E(r\geq R) \mathrm{d} r=\frac{k R}{\left(1-\frac{\varepsilon_{0}}{\varepsilon}\right) \varepsilon_{0} r} &r\geq R \\
\int_{R}^{+\infty} E(r\geq R) \mathrm{d} r+\int_{r}^{R} E(r<R) d r=\frac{k}{\varepsilon-\varepsilon_{0}}\left(\frac{\varepsilon}{\varepsilon_{0}}+\ln \frac{R}{r}\right) & r<R
\end{array}\right.
$$
-  (4)
$$
\begin{aligned}
w=\frac{1}{2} \int \rho_{f} \varphi & =\frac{1}{2} \int_{0}^{R} \rho_{f}(r<R) \varphi(r<R) r^{2} d r \int_{0}^{\pi} \sin \theta d \theta \int_{0}^{2 \pi} d \varphi\\
&=\frac{2 \pi \varepsilon k^{2}}{\left(\varepsilon-\varepsilon_{0}\right)^{2}} \cdot \int_{0}^{R}\left(\frac{\varepsilon}{\varepsilon_{0}}+\ln \frac{R}{r}\right) d r \\
& =\frac{2 \pi \varepsilon\left(\varepsilon+\varepsilon_{0}\right) k^{2}}{\varepsilon_{0}\left(\varepsilon-\varepsilon_{0}\right)^{2}}R
\end{aligned}
$$
# 7. 场源不分离的极化场的电势
## (a)
记源点 $\vec r$, 场点 $\vec r'$, 相对位移 $\vec R = \vec r - \vec r'$, 于是单个电荷 $q,\vec r$ 在 $R_0$ 球内产生的平均电场可以写作
$$
\begin{aligned}  
\vec E_{ave} (\vec r)
&= 
\frac{1}{V'} \int \frac{q(-\vec e_R)}{4\pi\epsilon_0 R^2} dV' \\
\small{\color{red} \rho = -\frac{q}{V'} \quad\to\quad}&= 
\frac{1}{4\pi\epsilon_0}\int \frac{\rho\vec{e_R}}{R^2} dV' \\
&=
\vec E_\rho(\vec r)
\end{aligned}
$$
等于均匀带电球在球内 $\vec r$ 产生的平均电场 $\vec E_\rho$, 将 q 的数量增加到球内电荷的数目, 记每个电荷为 $q_i,\vec r_i$, 产生的等效量是 $\vec E_{\rho i}, \rho_i$, 于是由高斯定理和叠加原理得到:
$$
E_{\rho_i} \cdot 4\pi r_i^2 = \frac{\rho_i}{\epsilon_0} \cdot \frac{4}{3}\pi r_i^3
\quad\to\quad
\vec E_{ave} 
= \sum \vec E_{\rho i} 
= \sum \frac{{\rho_i \cdot \frac{4}{3}\pi r_i^3 \vec e_{ri}}}{\epsilon_0 4\pi r_i^2} 
= - \frac{\sum q_i \vec{r_i}}{4\pi\epsilon_0 R_0^3}
=- \frac{\vec{p}}{4\pi\epsilon_0 R_0^3}
$$
记极化强度 $\vec P = \frac{\vec{p}}{V'}$, 得到
$$
\vec E_{ave} = - \frac{\vec{P}}{3\epsilon_0}
$$
## (b)
设 $\vec P = P\vec e_z$, $\vec p = \vec P V$ 则 $\sigma_p = \vec P\cdot \vec n = P\cos\theta$, 求解:
$$
\nabla^2 \varphi = 0
$$
已知边界条件:
$$
\left\{
\begin{aligned}
&
\varphi(r=0) = 0 \\
&
\varphi(R_0^-) = \varphi(R_0^+)\\
&
\frac{ \partial  }{ \partial r }\varphi(R_0^-) -  \frac{ \partial  }{ \partial r }\varphi(R_0^+) = \frac{\sigma_p}{\epsilon_0}\\
&
\varphi(r\gg R_0) = \frac{{\vec p \cdot \vec r}}{4\pi \epsilon_0 r^3}
\end{aligned}
\right.
$$
得到:
$$
\begin{aligned} 
\varphi(r<R_0) &= \frac{1}{3\epsilon_0} Pz
\\
\vec E(r<R_0) &=  -\nabla \varphi (r<R_0) = - \frac{\vec{P}}{3\epsilon_0}
\end{aligned}
$$
## (c)
由于 $\vec r' \gg \vec r$, 球外电荷 $\vec r', q$ 在球内(遍历 $\vec r$)的平均电场, 与场点 $\vec r$ 处的电场相同, 即球内电场近似均匀, 同时
$$
\begin{aligned}  
\vec E_{ave}
&= 
\frac{1}{V} \int \frac{q(-\vec e_R)}{4\pi\epsilon_0 R^2} dV \\
\small{\color{red}{ \vec r' \gg \vec r ,\ \vec R = \vec r' - \vec r } \quad\to\quad}
&= 
\frac{q(-\vec e_r')}{4\pi\epsilon_0 r'^2}
\end{aligned}
$$
第二个等号只保留了零阶项, 即等于外部电荷在球心处的电场.
# 8. poison 方程猜想解
- (1)
$$
\mathcal{L} = \sum \frac{1}{2}(\partial_i \varphi)^2 - \frac{\rho\varphi}{\epsilon_0} = \frac{1}{2} (\nabla \varphi)^2 + \varphi \nabla^2 \varphi = -\frac{1}{2} (\nabla \varphi)^2 + \frac{1}{2}\nabla^2 \varphi^2
$$
- (2)
$$
\nabla^2 \varphi + \frac{\rho}{\epsilon_0}  = 0
$$
# 9. 静电势的球谐展开
数理方程中提到, 勒让德函数的母函数表示是:
$$
(1-2xt + t^2) ^{-\frac{1}{2}} = \sum_0^{+\infty} P_n(x)t^n \quad |t|<1
$$
将 $t = \frac{r'}{r},\ x = \cos\alpha$ 代入上式就可以得到 (14). 于是可以求解球谐系数:
$$
\begin{aligned} 
\phi(\vec x) 
&= \sum\sum  \frac{4\pi}{2l+1}q_{lm} r^{-(l+1)} Y_{lm} \\
&=
\frac{1}{4\pi\epsilon_0}\int \frac{\rho(\vec x')}{|\vec x - \vec x'|} \mathrm{d}V' \\
\small{\color{red}(14) \quad\to\quad}&=
\frac{1}{4\pi\epsilon_0}\int {\rho(\vec x')} \sum r'^l r^{-(l+1)} P_l(\cos\alpha) \mathrm{d}V' \\
\small{\color{red}(15) \quad\to\quad}&=
\sum\sum \frac{1}{4\pi\epsilon_0}\int {\rho(\vec x')}  r'^l r^{-(l+1)} \frac{4\pi}{2l+1}Y^*_{lm}(\theta',\varphi')Y_{lm}(\theta,\varphi) \mathrm{d}V' \\
&=
\sum\sum  \frac{4\pi}{2l+1} \left( \frac{1}{4\pi\epsilon_0}\int {\rho(\vec x')}  r'^l Y^*_{lm}(\theta',\varphi') ~\mathrm{d}V' \right) r^{-(l+1)} Y_{lm} \\
\end{aligned}
$$
于是 $q_{lm}=\frac{1}{4\pi\epsilon_0}\int {\rho(\vec x')}  r'^l Y^*_{lm}(\theta',\varphi') ~\mathrm{d}V'$. 

~~# 补充 1. 电磁场的拉氏量是猜出来的吗?~~

# 补充 2. 球谐函数
第九题的泊松方程课上已经用 green 函数求解讲过. 来看更简单的 Laplace 方程. 三维拉普拉斯方程方程在球坐标下:
$$
\begin{aligned}
\Delta u &= \nabla^2 u = \nabla \cdot \nabla u = 0 \\
&= 
\frac{1}{r^2} \frac{ \partial  }{ \partial r }\left( r^2 \frac{ \partial u }{ \partial r } \right) 
+ \frac{1}{r^2 \sin\theta}\frac{ \partial  }{ \partial \theta }\left( \sin\theta\frac{ \partial u }{ \partial \theta } \right) 
+ \frac{1}{r^2 \sin^2\theta} \frac{ \partial^2 u }{ \partial^2 \varphi }
\end{aligned}
$$
分离变量 $u(r,\theta,\varphi) = R(r)Y(\theta,\varphi)$, 得到
$$
\frac{1}{R} \frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right)
= - \frac{1}{Y}  \left(\frac{1}{\sin \theta } \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right)-\frac{1}{\sin ^{2} \theta} \frac{\partial^{2} Y}{\partial \phi^{2}}\right)
= \lambda
$$
## 1. 径向衰减
常常选取 $\lambda = l(l+1)$, 于是
$$
\frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right) - l(l+1)R = 0
$$
这是欧拉方程, 根据换元 $r=e^s$ 得到它的通解是
$$
R(r) = A r^l + B r^{-(l+1)}, \quad l\geq 0
$$
通常情况下, 场不会传播到无穷远处, 也就是说, 在解 $R(r)$ 的定义域中包含 $r=\infty$ 时, 因为 $r^l \to \infty$ 不合适, 所以通常取 $A=0$. 同理, 在解的定义域包含 $r=0$ 时, 通常取 $B=0$.
## 2. 球面谐波
由上述已知
$$
\frac{1}{\sin \theta } \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right)
-\frac{1}{\sin ^{2} \theta} \frac{\partial^{2} Y}{\partial \phi^{2}} 
+ l(l+1)Y
= 0
$$
进一步分离变量 $Y(\theta, \varphi) = \Theta(\theta)\Phi(\varphi)$, 有
$$
\begin{aligned} 
\left\{
\begin{array}l
\frac{ d^2 \Phi }{ d^2 \varphi} + m^2 \Phi = 0 \\
\Phi(\varphi) = \Phi(\varphi + 2\pi)
\end{array}
\right.
\quad and \quad
\begin{array}l
\sin \theta \frac{d}{d \theta}\left(\sin \theta \frac{d \Theta}{d \theta}\right)+\left[(l+1) l \sin ^{2} \theta-m^{2}\right] \Theta=0
\end{array}
\end{aligned}
$$
第一个方程没什么好说的, 解是 $\Phi_m(\varphi) = e^{im\varphi}$, 对第二个方程做和数理课上一样的换元 $\theta = \arccos x$, 得到
$$
\left(1-x^{2}\right) \frac{d^{2} \Theta}{d x^{2}}-2 x \frac{d \Theta}{d x}+\left[l(l+1)-\frac{m^{2}}{1-x^{2}}\right] \Theta=0 \ \cdots\cdots \color{red}(1)
$$
被称为连带勒让德方程, 特别的当 $m=0$ 时变成勒让德方程, 他的解就是勒让德函数 $P_l(x)$. 

做换元 $y(x) = \Theta(x) (1-x^2)^{-\frac{m}{2}}$, 可得到
$$
\begin{array}c
\Theta 
= (1-x^2)^{\frac{m}{2}} y \\
\Theta'
=\left(1-x^{2}\right)^{\frac{m}{2}} y^{\prime}-m\left(1-x^{2}\right)^{\frac{m}{2}-1} x y \\
\Theta''
=\left(1-x^{2}\right)^{\frac{m}{2}} y^{\prime \prime}-2 m\left(1-x^{2}\right)^{\frac{m}{2}-1} x y^{\prime}-m\left(1-x^{2}\right)^{\frac{m}{2}-1} y
+m(m-2)\left(1-x^{2}\right)^{\frac{m}{2}-2} x^{2} y \\
\Downarrow \\
\left(1-x^{2}\right) y^{\prime \prime}-2(m+1) x y^{\prime}+[l(l+1)-m(m+1)] y=0
\ \cdots\cdots \color{red}(2)
\end{array}
$$
将上式与与下面的勒让德方程(式 $(1)$)做比较, 注意下面的方程还没有做 $y(x) = \Theta(x) (1-x^2)^{-\frac{m}{2}}$ 的换元.
$$
\left(1-x^{2}\right) \frac{d^{2} P_l}{d x^{2}}-2 x \frac{d P_l}{d x}+ l(l+1) P_l=0
$$
对它求导 $m$ 次, 记 $P^{(m)}$ 表示对 $P$ 求 $m$ 次导, 注意到 $P_l(x)$ 是 $l$ 阶多项式, 可以得到
$$
\begin{aligned}
0 &= {\left[ \left(1-x^{2}\right) P_l^{(m+2)} -2mx P_l^{(m+1)} -{m(m-1)} P_l^{(m)} \right]
-2\left[ x P_l^{(m+1)}+m P_l^{(m)} \right]}
+l(l+1) P_l^{(m)}
\\
&=
\left(1-x^{2}\right) P_l^{(m+2)}-2(m+1) x P_l^{(m+1)}+[l(l+1)-m(m+1)] P_l^{(m)}
\end{aligned}
$$
恰好和 $(2)$ 式形式一致, 也就是说如果将方程 $\left(1-x^{2}\right) \frac{d^{2} \Theta}{d x^{2}}-2 x \frac{d \Theta}{d x}+\left[l(l+1)-\frac{m^{2}}{1-x^{2}}\right] \Theta=0$ 的解记为连带勒让德函数 $P_l^m(x)$, 那么
$$
\boxed{
P_l^m(x) = (1-x^2)^{\frac{m}{2}} \frac{ d^m }{ d x^m} P_l(x), \quad |m| \leq l
}
$$
最后的球谐函数就是
$$
Y_l^m (\theta, \varphi) = P_l^m(\cos\theta)\Phi_m(\varphi)
$$
如果要归一化 $Y$, 也就是令 $\int_0^{2\pi} \mathrm{d}\varphi \int_0^{\pi} Y_l^m (\theta, \varphi) \sin\theta \mathrm{d}\theta = 1$, 可以得到归一化的球谐函数:
$$
Y_l^m (\theta, \varphi) = \sqrt{\frac{1}{2\pi} \frac{2l+1}{2} \frac{(l-m)!}{(l+m)!}} ~P_l^m(\cos\theta) e^{\boldsymbol{i}m\varphi}
$$
于是通解表示为
$$
u(r, \theta,\varphi) 
= \sum_{l=0}^{\infty} \sum_{m=-l}^{l}
\left(A r^l + B r^{-(l+1)}\right)  \sqrt{\frac{1}{2\pi} \frac{2l+1}{2} \frac{(l-m)!}{(l+m)!}} ~P_l^m(\cos\theta) e^{\boldsymbol{i}m\varphi}
$$
另外, 连带勒让德函数的前几项为:
$$
\begin{aligned}
P_0^0(x) &= 1, \\
P_1^0(x) &= x, \quad P_1^1(x) = -\sqrt{1 - x^2}, \\
P_2^0(x) &= \frac{1}{2}(3 x^2 - 1), \quad P_2^1(x) = -3 x\sqrt{1 - x^2}, \quad P_2^2(x) = 3(1 - x^2), \\
P_3^0(x) &= \frac{1}{2}(5 x^3 - 3 x), \quad P_3^1(x) = -\frac{3}{2}(5 x^2 - 1)\sqrt{1 - x^2}, \quad
P_3^2(x) = 15 x(1 - x^2), \quad P_3^3(x) = -15(1 - x^2)^{3/2}.
\end{aligned}
$$
### 2.1 $Y_1^m$ 和偶极场
在静磁学中, 如果场点不存在电流, 那么磁感应强度可以表示成磁标势的梯度 $\vec B = -\nabla \Phi_m$, 并且 $\nabla^2 \Phi_m = 0$.

归一化球谐函数中, $Y_1^0(\theta) = \sqrt{\frac{3}{4\pi}}\cos\theta \propto \cos\theta = \frac{z}{r}$, $R_1(r)=Ar+\frac{B}{r^2} = \frac{B}{r^2}$ (取 $A=0$). 于是 $\Phi_m$ 的一个解可以写作
$$
\Phi_{pole}(r, \theta, \varphi) = \frac{C}{r^2} \cos\theta
$$
求梯度得到
$$
\vec B = - \left( \partial_r \Phi_{pole},\ \frac{1}{r}\partial_\theta\Phi_{pole},\ 0 \right)
=C\cdot \left( \frac{2\cos\theta}{r^3},\ \frac{\sin\theta}{r^3},\ 0 \right)
$$
回忆课上所学到的磁偶极子在远处的磁场表达式:
$$
\vec B = \frac{\mu_0}{4\pi} \frac{{3 (\vec n\cdot \vec m)\vec n - \vec m}}{r^3} 
=
\frac{\mu_0}{4\pi} \frac{{3 \cos\theta\vec e_r - \vec e_z}}   {r^3} 
=
\frac{\mu_0}{4\pi} \frac{{3 \cos\theta\vec e_r - (\cos\theta\vec e_r - \sin\theta \vec e_\theta)}}   {r^3} 
=
\frac{\mu_0}{4\pi} \frac{{2 \cos\theta\vec e_r +  \sin\theta \vec e_\theta}}   {r^3} 
$$
发现两式形式一致, 只要取 $C=\frac{\mu_0}{4\pi}$, 就可以用球谐函数描述偶极磁场.

另外, 由于 $Y_1^{\pm 1}$ 是虚数, 所以选取它们的实数线性组合 $Y_1^x = \frac{Y_1^1 + Y_1^{-1}}{\sqrt{2}}$ 和 $Y_1^y = \frac{Y_1^1 - Y_1^{-1}}{i\sqrt{2}}$, 显然 $Y_1^x \propto \sin\theta\cos\varphi = \frac{x}{r}$,  $Y_1^y \propto \sin\theta\sin\varphi = \frac{y}{r}$. 对于三维旋转, 考察球坐标的变换, 比如绕 $y$ 轴旋转矩阵, 直角坐标系中的变换矩阵是
$$
   R_y(\beta) = \begin{pmatrix}
   \cos\beta & 0 & \sin\beta \\
   0 & 1 & 0 \\
   -\sin\beta & 0 & \cos\beta
   \end{pmatrix}
   $$
即:
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
也就是说
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
因此, $Y_1^x$ 描述沿 $x$ 轴方向的磁偶极子, 类似的知道 $Y_1^y$ 描述沿 $y$ 轴方向的磁偶极子. 在量子力学里面(量C不讲这个东西), 上面的旋转操作可以用 $Winger-D$ 矩阵作用于球谐函数得到, 这个矩阵的数值形状很丑, 可以在在 $MMA$ ($Mathematica$)中直接调用 $Winger-D$ 函数快速完成.
### 2.2 $Y_2^m$ 和四极场
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

##  3. 球谐系数
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
倘若已知边界条件 $u(r,\theta,\varphi)|_{r=R} = u_R(\theta, \varphi)$, 就可解出:
$$
B_{l^{\prime} m^{\prime}}= {R^{l^{\prime}+1}} \int_{0}^{2 \pi} \int_{0}^{\pi} u(R, \theta, \varphi) Y_{l^{\prime}}^{m^{\prime} *}(\theta, \varphi) \sin \theta \mathrm{d} \theta \mathrm{d} \varphi 
$$
这就是拉普拉斯方程通解对应的球谐系数. 不同的边界条件会得到不同的系数表达式, 上述只是较为简单的一种.


