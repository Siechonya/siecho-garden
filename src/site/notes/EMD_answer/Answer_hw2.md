---
{"dg-publish":true,"permalink":"/EMD_answer/Answer_hw2/","noteIcon":"default","created":"2025-10-23T14:23:44.419+08:00","updated":"2025-06-16T16:58:31.347+08:00"}
---



 $yry0204@mail.ustc.edu.cn$

- [[#一. hw solution]]
- [[#1.]]
- [[#2. 洛伦兹标量]] <font color="#ff0000">(建议阅读其中的 tips)</font>
- [[#3. 洛伦兹变换]]
- [[#4. 张量变换]]
- [[#5. 速度变换]]
- [[#6. 麦克斯韦方程组的近似]]
- [[#7. QFT 的洛伦兹不变量]]
- [[#二. 补充阅读]]
- [[#1. $Lorentz Group$]]
- [[#2. '邪教' $ict$]] <font color="#ff0000">(建议阅读)</font>

# 一. HW solution
## 1. 
### 6.2
从洛伦兹变换的微分形式可以得到速度变换:
$$
\left\{
\begin{array}{l}
c \mathrm{d}t = \gamma c\mathrm{d} t' + \gamma\beta \mathrm{d}x' \\
\mathrm{d}x = \gamma\mathrm{d}x' + \gamma\beta c\mathrm{d}t'
\end{array}
\overset{div}{\quad\to\quad}
\frac{v_x}{c} = \frac{{\frac{v_x'}{c} + \beta}}{1 + \beta \frac{v_x'}{c}}
\right.
$$
取 $v_x = -v$, 于是
$$
v_x' = - \frac{2v}{1+ \left( \frac{v}{c}\right)^2 }
\quad\to\quad
l = \gamma^{-1}l_0 = \sqrt{1-\left( \frac{v_x'}{c} \right)^2 }l_0 = \frac{{1 - \left( \frac{v}{c}\right)^2 }}{{1+ \left( \frac{v}{c}\right)^2 }} l_0
$$
### 6.4
标记事件: A(电火花产生), B(到达左塔), C(到达右塔), 地面系中 $\Delta t_{AB} = \Delta t_{AC}  = \frac{l_0}{c}$, 于是运动系中:
$$
\begin{aligned} 
\Delta t_{AB}' = \gamma \Delta t_{AB} - \frac{\gamma \beta \Delta x_{AB}}{c} = \frac{\gamma l_0}{c} (\beta + 1) \\
\Delta t_{AC}' = \gamma \Delta t_{AC} - \frac{\gamma \beta \Delta x_{AC}}{c} = \frac{\gamma l_0}{c} (\beta + 1)
\end{aligned}
$$
相减得
$$
\Delta t = \Delta t_{AB}' - \Delta t_{Ac}' = \frac{2\gamma\beta l_0}{c}
$$
### 6.7
$$
\left\{
\begin{aligned} \mathrm{d}y' &= \mathrm{d} y \\ 
\mathrm{d}x' &= \gamma^{-1} \mathrm{d} x
\end{aligned}
\quad\to\quad
\tan\theta' = \gamma \tan\theta
\right.
$$
## 2. 洛伦兹标量
### (a)缩并
注意到 $\Lambda_{\alpha}^{~~\gamma} \Lambda^\alpha_{~~\beta} = \delta^\gamma_\beta$, 于是
$$
A^\alpha B_\alpha = \Lambda_{\alpha}^{~~\gamma} B'_{\gamma} \Lambda^\alpha_{~~\beta} A^{'\beta} = A^{'\beta} B'_{\beta}
$$
即缩并两个四维矢量得到一个洛伦兹标量.

<font color="#ff0000">tips 1:</font>
注意到 $\eta^{\alpha\beta} \eta_{\alpha\rho} = \delta^\beta_\rho$, 于是 $A^\alpha B_\alpha = \eta^{\alpha\beta} A_\beta \eta_{\alpha\rho} B^\rho = A_\beta B^\beta$, 这意味着可以将哑指标的上下位置随意调换.

<font color="#ff0000">tips 2:</font>
有的同学可能会混淆 $\Lambda_{~~\nu}^\mu$ 和 $\Lambda_{\alpha}^{~~\beta}$, 已经知道:
$$
x^\mu = \Lambda_{~~\nu}^\mu x'^\nu
$$
那么
$$
x_\alpha = \eta_{\alpha\mu} x^\mu = \eta_{\alpha\mu} \Lambda_{~~\nu}^\mu x'^\nu = \eta_{\alpha\mu} \Lambda_{~~\nu}^\mu \eta^{\nu\beta} x'_\beta = \Lambda_{\alpha}^{~~\beta} x'_\beta
$$
也就是说 $\Lambda_{~~\nu}^\mu$ 和 $\Lambda_{\alpha}^{~~\beta}$ 其实分别对应于对逆变分量和协变分量的 $Lorentz$ 变换, 并且
$$
\Lambda_{\alpha}^{~~\beta} = \eta_{\alpha\mu} \Lambda_{~~\nu}^\mu \eta^{\nu\beta}
= diag(1,-1,-1,-1)  \begin{bmatrix} \gamma & \gamma\beta &  & \\   \gamma\beta & \gamma &  & \\    &  & 1 &  \\     &  & & 1 \end{bmatrix}  diag(1, -1,-1,-1)
= \begin{bmatrix} \gamma & -\gamma\beta &  & \\   -\gamma\beta & \gamma &  & \\    &  & 1 &  \\  &  & & 1 \end{bmatrix}
= (\Lambda_{~~\nu}^\mu)^{-1}
$$
意味着两者的矩阵形式恰好互逆.

<font color="#ff0000">tips 3:</font>
对于混合指标, 我们一般不提及他们的对称还是不对称, 比如我们很少说 $\Lambda_{~~\nu}^\mu$ 关于上标 $\mu$ 和下标 $\nu$ 是对称的(即使看起来是如此), 因为协变和逆变是两种不同的指标. 所以只说同类指标的对称性(比如 $\eta_{\alpha\beta}$ 关于下指标对称). 

有些时候(不常见), 在四维空间中, 如果一个混合形式的张量满足 $T_{~~\alpha}^{\beta} = T_{\alpha}^{~~\beta}$, 我们才会说 $T$ 关于指标 $\alpha$ 和 $\beta$ 对称, 这种情况成立仅当
$$
T_{~~\alpha}^{\beta} = \eta_{\alpha\mu} T^{\beta\mu} = \eta_{\alpha\mu} T^{\mu\beta} = T_{\alpha}^{~~\beta}
$$
时成立, 也就是 $T^{\mu\nu} = T^{\nu\mu}$ 关于两个上指标对称时才成立. 后面课程可能会接触到的能动张量, 它就满足这个性质, 这种情况下, 可以直接记 $T_\alpha^\beta = T_{~~\alpha}^{\beta} = T_{\alpha}^{~~\beta}$, 也就是说上下指标不必错位来写, 就像我们会写 $\delta_\alpha^\beta$ 而不是 $\delta_\alpha^{~~\beta}$ 或者 $\delta_{~~\alpha}^{\beta}$ 一样.

此外, 除非不得不涉及到一些数学证明, 才会非严格地说: $\Lambda = \Lambda^T$, 这时最好把 $\Lambda$ 展开成具体矩阵形式, 并且小心操作为好.
### (b)四维间隔
注意到
$$
\mathrm{d}s^2 = \mathrm{d}x_\alpha \mathrm{d}x^\alpha \overset{ref.(1)}{=} \mathrm{d}x'_\alpha \mathrm{d}x'^\alpha
$$
### (c)四维体积
$\mathrm{d}\Omega = c\mathrm{d}t\mathrm{d}x\mathrm{d}y\mathrm{d}z = J {c\mathrm{d}t'\mathrm{d}x'\mathrm{d}y'\mathrm{d}z'}$, 其中:
$$
J = \left|\frac{ \partial (ct,x,y,z) }{ \partial (ct',x',y',z') }\right| = \begin{vmatrix}   \gamma & \gamma\beta &  & \\   \gamma\beta & \gamma &  & \\    &  & 1 &  \\     &  &  & 1 \end{vmatrix} = \det(\Lambda) = 1
$$
## 3. 洛伦兹变换
根据洛伦兹变换有:
$$
\begin{aligned} 
&(1)~\vec r_{\parallel} = \gamma\vec \beta ct' + \gamma \vec r_{\parallel}' = \frac{{\vec r \cdot \vec V}}{V} \vec V^0 \\
&(2)~ct = \gamma ct' + \gamma\vec \beta \cdot \vec r_{\parallel}' \\
&(3)~\vec r_{\bot} = \vec r_{\bot}' = \vec r' - \frac{{\vec r' \cdot \vec V}}{V} \vec V^0
\end{aligned}
$$
$(1)的第一个等号 + (3)的第二个等号$ 得到 $\vec r$ 的变换, 将(1): $\vec r'_{\parallel} = \frac{{\vec r' \cdot \vec V}}{V} \vec V^0$ 代入 $(2)$ 得到 $t$ 的变换:  
$$
\vec r = \gamma \vec V t' + (\gamma-1) \frac{{\vec r'\cdot \vec V}}{V}{\vec V}^0 + \vec r',\quad
ct = \gamma\left( ct' + {\vec r' \cdot \vec \beta} \right)
$$
## 4. 张量变换
即计算 $A^{\alpha'\beta'} = \Lambda^\alpha_{~\rho} A^{\rho\sigma} \Lambda_{~\sigma}^{\beta}$, 注意对称张量只需要写 10 个上对角元, 反对称张量需要写 6 个严格上对角元. 注意到
$$
B'^0C'^0 = (\gamma B^0 + \gamma\beta B^1 )(\gamma C^0 + \gamma\beta C^1 ) = \gamma^2 (B^0C^0 + 2\beta B^0C^1 + \beta^2 B^1C^1)
$$
于是
$$
A^{0'0'} = \gamma^2 (A^{00} + 2\beta A^{01} + \beta^2 A^{11})
$$
其他分量类似.
## 5. 速度变换
已知四维速度的洛伦兹变换
$$
\begin{aligned} 
u^0 &= \gamma_v (u'^0 + \beta_v u'^1)
\\ 
u^1 &= \gamma_v (\beta_v u'^0 + u'^1)
\\
u^2 &= u'^2 \\
u^3 &= u'^3 
\end{aligned}
$$
其中 $\gamma_v = \frac 1 {\sqrt{1-\beta_v^2}}, \ \beta_v = \frac{V}{c}, \ \gamma = \frac{1}{\sqrt{1-\beta^2}}, \ \beta = \frac{v}{c}, \ \gamma' = \frac{1}{\sqrt{1-\beta'^2}}, \ \beta' = \frac{v'}{c}$, 根据 $u^\alpha = \gamma(c,v_x,v_y, v_z)$ 可得:
$$
\left\{
\begin{aligned} 
c &= \frac{\gamma_v \gamma'}{\gamma} \left(  c + \beta_v v'_x \right)
\\ 
v_x &= \frac{\gamma_v \gamma'}{\gamma} (\beta_v c + v_x')
\\
v_y &= \frac{\gamma'}{\gamma} v_y' \\
v_z &= \frac{\gamma'}{\gamma} v_z' 
\end{aligned}
\right.
\quad\to\quad
\left\{
\begin{aligned} 
\frac{\gamma'}{\gamma} &= \frac{\sqrt{1-\left( \frac{V}{c} \right)^2}}{1+\frac{Vv_x'}{c^2}}
\\ 
v_x &= \frac{{v_x' + V}}{1+\frac{Vv_x'}{c^2}}
\\
v_y &= \frac{\sqrt{1-\left( \frac{V}{c} \right)^2}}{1+\frac{Vv_x'}{c^2}} v_y' \\
v_z &= \frac{\sqrt{1-\left( \frac{V}{c} \right)^2}}{1+\frac{Vv_x'}{c^2}} v_z' 
\end{aligned}
\right.
$$
## 6. 麦克斯韦方程组的近似
### (a)洛伦兹协变的电磁场
注意到
$$
\begin{aligned} 
\vec E = \gamma (\vec E' + \beta c \vec B' \times \vec e_x) - \frac{\gamma^2 \beta^2}{\gamma+1} E_x' \vec e_x
\\ 
\vec B = \gamma \left( \vec B' - \frac{\beta}{c} \vec E' \times \vec e_x \right) - \frac{\gamma^2 \beta^2}{\gamma+1} B_x' \vec e_x
\end{aligned}
$$
以及
$$
\begin{aligned}
\partial_\alpha = \Lambda_\alpha^{~~\beta}\partial_\beta'
\quad\to\quad
\partial_t &= \gamma\partial_t' - \gamma\beta c\partial_x' \\
\nabla &= \nabla' + \vec e_x\left[ (\gamma - 1)\partial_x' - \frac{\gamma\beta}{c} \partial_t' \right]
\end{aligned}
$$
假设带 ' 的 $maxswell$ 方程均被满足, 那么
$$
\begin{aligned}
\nabla \cdot \vec E 
&= \left(\nabla' + \vec e_x\left[ (\gamma - 1)\partial_x' - \frac{\gamma\beta}{c} \partial_t' \right]\right) \cdot \left( \gamma (\vec E' + \beta c \vec B' \times \vec e_x) - \frac{\gamma^2 \beta^2}{\gamma+1} E_x' \vec e_x \right) \\
&=
\gamma \nabla' \cdot \vec E' + \gamma\beta c (\nabla' \times \vec B')_{x'} - \frac{\gamma^2 \beta^2}{\gamma+1} \partial_x' E_x' + \left[ (\gamma - 1)\partial_x' - \frac{\gamma\beta}{c} \partial_t' \right]E_x'
\\
&= \gamma \nabla' \cdot \vec E' + \gamma V \left[ (\nabla' \times \vec B')_{x'} -\frac{1}{c^2} \frac{ \partial E_x' }{ \partial t' } \right]\\
 &=0
\end{aligned}
$$
同理可得
$$
\nabla \cdot \vec B = \gamma \nabla' \cdot \vec B' - \frac{\gamma\beta}{c}\left[ \frac{ \partial B_x' }{ \partial t' } + (\nabla' \times \vec E')_x \right]
=0
$$
$$
\nabla \times \vec E + \partial_t \vec B = \left\{
\begin{aligned}  
&(\nabla' \times \vec E')_{x} - V \nabla' \cdot \vec B' + \frac{ \partial B_x' }{ \partial t' }=0
\\ 
&(\nabla' \times \vec E')_{y}+ \frac{ \partial B_y' }{ \partial t' }=0 
\\
& (\nabla' \times \vec E')_{z}+ \frac{ \partial B_z' }{ \partial t' }=0
\end{aligned}
\right.
$$
$$
\nabla \times \vec B - \frac{1}{c^2}\frac{ \partial \vec E }{ \partial t }
=
\left\{
\begin{aligned}  
&(\nabla' \times c^2\vec B')_{x} + V \nabla' \cdot \vec E' - \frac{ \partial E_x' }{ \partial t' }=0
\\ 
&(\nabla' \times c^2\vec B')_{y} - \frac{ \partial E_y' }{ \partial t' }=0 
\\
&(\nabla' \times c^2\vec B')_{z} - \frac{ \partial E_z' }{ \partial t' }=0
\end{aligned}
\right.
$$
### (b)伽利略协变的电磁场
伽利略变换下
$$
\left\{
\begin{aligned}
t &= t'
\\ 
x_i &= x_i' + V_it'
\end{aligned}
\right.
\quad\to\quad
\begin{aligned} 
\frac{ \partial x_i }{ \partial t' } = V_i(i=x,y,z),
\quad
\frac{ \partial t' }{ \partial t } = 
\frac{ \partial x' }{ \partial x } = 
\frac{ \partial y' }{ \partial y } = \frac{ \partial z' }{ \partial z } = 1,\quad
\frac{ \partial t }{ \partial x_i' } = 0
\end{aligned}
$$
于是有
$$
\nabla' = \vec e_i \frac{ \partial  }{ \partial x_i' } 
= \vec e_i \left[  \frac{ \partial x_j }{ \partial x_i' }\frac{ \partial  }{ \partial x_j } + \frac{ \partial t }{ \partial x_i' }\frac{ \partial  }{ \partial t } \right]
= \nabla
$$
$$
\frac{ \partial  }{ \partial t' } = \frac{ \partial x_j }{ \partial t' }\frac{ \partial  }{ \partial x_j } + \frac{ \partial t }{ \partial t' }\frac{ \partial  }{ \partial t }
= \vec V \cdot \nabla + \frac{ \partial  }{ \partial t }
$$
- 如果不考虑电磁场的变换, 则
$$
\begin{aligned}
0 &= \nabla' \times \vec E' + \partial_t \vec B'
\\
&=  \nabla \times \vec E + \vec V \cdot \nabla \vec B + \partial_t \vec B
\end{aligned}
$$
- 如果 $\vec E = \vec E' + \vec B' \times \vec V$, 则 $\vec E' = \vec E - \vec B \times \vec V$, 于是
$$
\begin{aligned}
0 &= \nabla' \times \vec E' + \partial_{t'} \vec B'
\\
&=  [\nabla \times \vec E - \nabla \times (\vec B \times \vec V)] + [\vec V \cdot \nabla \vec B + \partial_t \vec B]
\\
&\quad \Downarrow \tiny{\color{blue}
\nabla \times (\vec B \times \vec V) = [(\vec V \cdot \nabla) + (\nabla \cdot \vec V)]\vec B - [(\vec B \cdot \nabla) + (\nabla \cdot \vec B)] \vec V  = (\vec V \cdot \nabla)\vec B\quad '先中间后外边'
}
\\
&=  [\nabla \times \vec E - \vec V \cdot \nabla \vec B] + [\vec V \cdot \nabla \vec B + \partial_t \vec B]\\
&= \nabla \times \vec E + \partial_t \vec B
\end{aligned}
$$
### (c)洛伦兹协变的低速近似
对洛伦兹变换做一阶近似, $\gamma \approx 1+\frac{1}{2}\epsilon^2 \approx 1$:
$$
\Lambda^\mu_{~\nu} = 
\begin{bmatrix}   \gamma & \gamma\epsilon &  & \\   \gamma\epsilon & \gamma &  & \\    &  & 1 &  \\     &  &  & 1 \end{bmatrix} 
\approx
\begin{bmatrix}   1 & \epsilon &  & \\  \epsilon & 1 &  & \\    &  & 1 &  \\     &  &  & 1 \end{bmatrix} 
\quad\to\quad
\left\{
\begin{aligned}
t &= t' + \frac{v}{c^2}x'
\\ 
x &= x' + vt'
\\
y &= y' \\
z &= z' 
\end{aligned}
\right.
\quad\to\quad
\left\{
\begin{aligned} 
\frac{ \partial x }{ \partial t' } &= v\\
\frac{ \partial t' }{ \partial t } &= 
\frac{ \partial x' }{ \partial x } = 
\frac{ \partial y' }{ \partial y } = \frac{ \partial z' }{ \partial z } = 1 \\
\frac{ \partial t }{ \partial x' } &= \frac{v}{c^2}
\end{aligned}
\right.
$$
$$
\Downarrow
$$
$$
\nabla' = \vec e_i \frac{ \partial  }{ \partial x_i' } 
= \vec e_i \left[  \frac{ \partial x_j }{ \partial x_i' }\frac{ \partial  }{ \partial x_j } + \frac{ \partial t }{ \partial x_i' }\frac{ \partial  }{ \partial t } \right]
= \left( 
\frac{ \partial  }{ \partial x } + \frac{v}{c^2}\frac{ \partial  }{ \partial t },\ \ 
\frac{ \partial  }{ \partial y },\ \ 
\frac{ \partial  }{ \partial z }
 \right)
= \nabla + \vec e_x \frac{v}{c^2}\frac{ \partial  }{ \partial t }
$$
$$
\frac{ \partial  }{ \partial t' } = \frac{ \partial x_j }{ \partial t' }\frac{ \partial  }{ \partial x_j } + \frac{ \partial t }{ \partial t' }\frac{ \partial  }{ \partial t }
= v \frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial t }
$$
于是
$$
\begin{aligned}
\nabla' \times \vec E'
&= 
\left( \nabla + \vec e_x \frac{v}{c^2}\frac{ \partial  }{ \partial t } \right) \times \left( \vec E - \vec B \times v\vec e_x \right) \\
&= 
\nabla \times \left( \vec E - \vec B \times \vec v \right) 
+\frac{v}{c^2}\frac{ \partial  }{ \partial t } (\vec e_x \times \vec E - \vec e_x \times\vec B \times v\vec e_x )
\\&=
\nabla \times \left( \vec E - \underbrace{\vec B \times \vec v} \right) 
+\frac{v}{c^2}\frac{ \partial  }{ \partial t } (\vec e_x \times \vec E) -\frac{v^2}{c^2}\frac{ \partial  }{ \partial t } (\vec e_x \times\vec B \times \vec e_x) 
\\
&\quad\quad\quad\quad\quad\quad \Downarrow \tiny{\color{blue}
\nabla \times (\vec B \times \vec V) = [(\vec V \cdot \nabla) + (\nabla \cdot \vec V)]\vec B - [(\vec B \cdot \nabla) + (\nabla \cdot \vec B)] \vec V  = (\vec V \cdot \nabla)\vec B = v\partial_x\vec B
}
\\&\approx
\nabla \times \vec E - \overbrace{v\partial_x\vec B}
+\frac{v}{c^2}\frac{ \partial  }{ \partial t } (\vec e_x \times \vec E)
\\\\
\partial_{t'} \vec B' 
&= 
\left( v \frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial t }\right)
\left( \vec B + \vec E \times \frac{ \vec v}{c^2} \right)
\\&=
\partial_t \vec B + v\partial_x\vec B + \frac{v}{c^2}\frac{ \partial  }{ \partial t }(\vec E \times \vec e_x) + \frac{v^2}{c^2} \frac{ \partial  }{ \partial x }\vec E \times { \vec e_x} \\
&\approx
\partial_t \vec B + v\partial_x\vec B + \frac{v}{c^2}\frac{ \partial  }{ \partial t }(\vec E \times \vec e_x)
\end{aligned}
$$
注意上述推导中二阶项 $\frac{v^2}{c^2}$ 被忽略, 两者相加可得到法拉第定律是 $Lorentz$ 协变的:
$$
\begin{aligned}
0 
= \nabla' \times \vec E' + \partial_{t'} \vec B'
= \nabla \times \vec E + \partial_t \vec B
\end{aligned}
$$
### (d)线性变换协变的电磁场
坐标变换矩阵可以写作:
$$
\Lambda_{~\nu}^{\mu}
=
\begin{pmatrix}
A & B c & & \\
D / c & C & & \\
& & 1 & \\
& & & 1
\end{pmatrix}
$$
于是电磁张量在该变换下保持协变的性质可以表述为:  
$$
\begin{array}{l}
F^{\mu \nu}= \Lambda_{~\alpha}^{\mu} F^{'\alpha \beta} \Lambda_{~\beta}^{\nu} \\
=
\left(\begin{array}{cccc}
A & B c & & \\
D / c & C & & \\
& & 1 & \\
& & & 1
\end{array}\right)\left(\begin{array}{cccc}
0 & -E_{x}^{\prime} / c & -E_{y}^{\prime} / c & -E_{z}^{\prime} / c \\
E_{x}^{\prime} / c & 0 & -B_{z}^{\prime} & B_{y}^{\prime} \\
E_{y}^{\prime} / c & B_{z}^{\prime} & 0 & -B_{x}^{\prime} \\
E_{z}^{\prime} / c & -B_{y}^{\prime} & B_{x}^{\prime} & 0
\end{array}\right)\left(\begin{array}{cccc}
A & D / c & \\
B c & C & & \\
& & 1 & \\
& & & 1
\end{array}\right) \\
=
\left(\begin{array}{cccc}
0 & (B D-A C) E_{x}^{\prime} / c & -A E_{y}^{\prime} / c-B c B_{z}^{\prime} & -A E_{z}^{\prime} / c+B c B_{y}^{\prime} \\
-(B D-A C) E_{x}^{\prime} / c & 0 & -C B_{z}^{\prime}-D E_{y}^{\prime} / c^{2} & C B_{y}^{\prime}-D E_{z}^{\prime} / c^{2} \\
A E_{y}^{\prime} / c+B c B_{z}^{\prime} & C B_{z}^{\prime}+D E_{y}^{\prime} / c^{2} & 0 & -B_{x}^{\prime} \\
A E_{z}^{\prime} / c-B c B_{y}^{\prime} & -C B_{y}^{\prime}+D E_{z}^{\prime} / c^{2} & B_{x}^{\prime} & 0
\end{array}\right) \\
=
\left(\begin{array}{cccc}
0 & -E_{x} / c & -E_{y} / c & -E_{z} / c \\
E_{x} / c & 0 & -B_{z} & B_{y} \\
E_{y} / c & B_{z} & 0 & -B_{x} \\
E_{z} / c & -B_{y} & B_{x} & 0
\end{array}\right)
\end{array}
$$
即
$$
\left\{
\begin{aligned}
E_{x} & =(AC - BD) E_{x}^{\prime} \\
E_{y} & =A E_{y}^{\prime}+B c^{2} B_{z}^{\prime} \\
E_{z} & =A E_{z}^{\prime}-B c^{2} B_{y}^{\prime}
\end{aligned}
\right.
\quad and \quad
\left\{
\begin{aligned}
B_{x} & =B_{x}^{\prime} \\
B_{y} & =C B_{y}^{\prime}-\frac{D}{c^{2}} E_{z}^{\prime} \\
B_{z} & =C B_{z}^{\prime}+\frac{D}{c^{2}} E_{y}^{\prime}
\end{aligned}
\right.
$$
## 7. QFT 的洛伦兹不变量
### (a) 能量-动量的三角关系
根据第二题可知, 两个四维矢量的缩并是洛伦兹标量. 量子力学中粒子的 4-动量写作 $p^\alpha = \left( \frac{\varepsilon}{c}, \vec p \right) = \left( \frac{ \hbar\omega}{c},  \hbar\vec k \right)$ , 则 $p^\alpha p_\alpha = \frac{\hbar^2}{c^2}(\omega^2 - k^2c^2)$ 为洛伦兹标量. 对应于相对论的 $E^2 = (pc)^2 + (mc^2)^2$.
### (b) 相位
显然 $p_\alpha x^\alpha = \left( \frac{ \hbar\omega}{c},  -\hbar\vec k \right)\cdot (ct, \vec x) = -\hbar (\vec k \cdot \vec x - \omega t)$ 也是洛伦兹标量.
## 8. 双生子佯谬
![[Capture_20250320_225944.jpg#pic_center|825]]

# 二. 补充阅读
## 1. $Lorentz\ Group$
### 李群和李代数
对于一个无限小变换, 可根据 $Taylor$ 展开表示为：
$$
g(\epsilon) = 1+\epsilon X
$$
$X$ 称为生成元. 对于有限旋转 $\theta=N\epsilon,\ N\to \infty, \ \epsilon \to 0$:
$$
R(\theta) = \left[ g\left( \frac{\theta}{N} \right) \right]^N = 
\\lim_{ N \to \infty } \left( 1+ \frac{\theta X}{N} \right)^N
= e^{\theta X}
$$
即有限旋转都可以由 $e$ 指数表示. 

从物理上非严格地理解, 所谓群, 指的是一个集合, 它的元素(称为群元)作用于某些物理量, 或者说对某些物理量进行一些<font color="#ff0000">连续的变换</font>, 上面的旋转就是一个典型的例子; 而李代数也是类似地作用于某些物理量, 但是对物理量进行<font color="#ff0000">无穷小的变换</font>, 李代数也是一个集合, 它的元素称为生成元(像是从无穷小变换的累加而"生成"了一个连续变换). 这么说不容易理解, 举一个典型的例子.

考虑一个三维空间的旋转变换, 变换矩阵记为 $O$ ("$O$"意为"$orthogonal$"(正交)), 这个变换的集合是三维旋转群, 记号是 $SO(3)$. 关于 $z$ 轴的旋转矩阵自然是
$$
O_z = \begin{pmatrix} \cos\theta & -\sin\theta &  \\ \sin\theta & \cos\theta &   \\  &  & 1 \end{pmatrix}
$$
取无穷小变换, $\theta \to 0$, 得到
$$
O_z \approx \begin{pmatrix} 1 & -\theta &  \\ \theta & 1 &   \\  &  & 1 \end{pmatrix} = \boldsymbol{I} + \begin{pmatrix}  & -\theta &  \\ \theta &  &   \\  &  & \end{pmatrix} = \boldsymbol{I} + \theta J_z
$$
其中
$$
J_z = \begin{pmatrix}  & -1 &  \\ 1 &  &   \\  &  & \end{pmatrix}
$$
是与群元 $O_z$ 对应的李代数的生成元 $J_z$, 即 $O_z = e^{\theta J_z} \approx 1+\theta J_z$, 于是可以建立一个通俗定义:
```col
> [!info] Lie 代数
>  $Lie$群 $G$ 的群元是 $n \times n$ 变换矩阵,  其对应的的 $Lie$代数 $\mathfrak{g}$ 是满足如下条件的 $n \times n$ 矩阵 $X$ 的集合:
> $
> \mathrm{e}^{t \mathfrak{g}} \in G,\ t \in \mathbb{R}
> $
```
### 洛伦兹群
洛伦兹群是狭义相对论中描述时空对称性的核心数学结构, 它由所有保持**闵可夫斯基时空间隔** $ds^2 = c^2 dt^2 - dx^2 - dy^2 - dz^2$ 不变的线性变换构成, 包括：
- **空间旋转**（三维欧氏空间旋转）  
- **Boost 变换**（课上学的洛伦兹变换）

略微严格来说, 洛伦兹群是这样定义:
```col
> [!info] Lorentz 群 $\Lambda$
> 洛伦兹群是作用是四维 $Minkowski$ 空间, 并且保持其内积不变的线性变换$\Lambda^\mu_{~\nu}$的集合: $x^\mu \to x'^\mu = \Lambda^\mu_{~\nu} x^\nu   \ \Rightarrow\     x'^\mu\eta_{\mu\nu}x'^{\nu}=x^\mu\eta_{\mu\nu}x^{\nu}$, 洛伦兹群一般记为$O(1,3)$, 括号里的1和3分别代表时间和空间分量.
```

上述定义等价于:
$$
\Lambda_{~~\mu}^{\sigma} \eta_{\sigma \rho} \Lambda_{~~\nu}^{\rho} = \eta_{\mu \nu}
$$

或者写成矩阵形式 :
$$
\Lambda^{T} \eta \Lambda = \eta
$$

对上式取行列式可得：
$$
\begin{aligned}
\operatorname{det}(\Lambda) \underbrace{\operatorname{det}(\eta)}_{=-1} \operatorname{det}(\Lambda)=\underbrace{\operatorname{det}(\eta)}_{=-1} 
& \rightarrow \operatorname{det}(\Lambda)^{2} = 1 \\
& \rightarrow \operatorname{det}(\Lambda) = \pm 1
\end{aligned}
$$

另外若取度规的 $\mu=\nu=0$ 分量 :
$$
\begin{array}{l}
& \Lambda_{~~0}^{\sigma} \eta_{\sigma \rho} \Lambda_{~~0}^{\rho} = \underbrace{\eta_{00}}_{=1} \\
\to  & \Lambda_{~~0}^{\sigma} \eta_{\sigma \rho} \Lambda_{~~0}^{\rho}=\left(\Lambda_{~~0}^{0}\right)^{2}-\sum_{i\neq0}\left(\Lambda_{~~0}^{i}\right)^{2} = 1 \\
\to  & \Lambda_{~~0}^{0} = \pm \sqrt{1+\sum_{i\neq0}\left(\Lambda_{~~0}^{i}\right)^{2}}
\end{array}
$$
根据上述两个约束的正负号可以把 $Lorentz$ 群分成 $4$ 个分支. 课上所学的是其中特殊的一支, 它同时满足 $\operatorname{det}(\Lambda) = 1$ 和 $\Lambda^0_0\geq 0$, 也就是时间方向是正的, 同时空间采取右手坐标系. 这四个分支一般这样区分:
```col
> [!info] $SO(1,3)^\uparrow$
> 满足 $\operatorname{det}(\Lambda) = 1$ 和 $\Lambda^0_0\geq 0$ 称为正规 $Lorentz$ 群 $SO(1,3)^\uparrow$. "$S$"即 $special$.
```

可以引入宇称变换(也就是空间坐标反演)和时间反演变换 :
$$
\Lambda_P = diag(1,-1,-1,-1),\ \ \Lambda_T=diag(-1,1,1,1)
$$
$\Lambda_{0}^{0} = \pm \sqrt{1+\sum_{i\neq0}\left(\Lambda_{0}^{i}\right)^{2}}$ 的正负选取之间差一个时间反演, 我们把空间反演留给 $\operatorname{det}(\Lambda) = \pm 1$ 的正负选取. 于是洛伦兹群 $O(1,3)$ 就可以表示为四个分支的集合:
$$
O(1,3) = \{SO(1,3)^\uparrow,\ \Lambda_P SO(1,3)^\uparrow,\ \Lambda_T SO(1,3)^\uparrow,\ \Lambda_P \Lambda_T SO(1,3)^\uparrow \}
$$
### boost 的双曲旋转形式
考虑无穷小变换 : 
$$
\Lambda_{~~\rho}^\mu = \delta_\rho^\mu + \epsilon K_{~~\rho}^\mu
$$
$\epsilon$ 是小量, 即作用对象原本的部分不变( $\delta_\rho^\mu$ ), 加上一个极小的线性变换 $\epsilon K_\rho^\mu$, 这一点也可以从李代数和李群的关系 $e^x\approx 1+x$ 来理解.

使其满足 $\Lambda_{\mu}^{\sigma} \eta_{\sigma \rho} \Lambda_{\nu}^{\rho} = \eta_{\mu \nu}$, 显然意味着 $\operatorname{det}(\Lambda) = 1,\ \Lambda_{0}^{0} = \sqrt{1+\sum_{i\neq0}\left(\Lambda_{0}^{i}\right)^{2}}$, 即对应 $SO(1,3)^\uparrow$ .

代入 $\Lambda_{\mu}^{\sigma} \eta_{\sigma \rho} \Lambda_{\nu}^{\rho} = \eta_{\mu \nu}$ , 并忽略 $\epsilon^2$ 得到 :
$$
\begin{array}{c}
K_{~~\rho}^\mu \eta_{\mu\sigma} + \eta_{\rho\nu}K_{~~\sigma}^\nu = 0 \\ \\
{\small or}: \quad K^T\eta + \eta K = 0
\end{array}
$$
英文中常常称 $Lorentz$ 变换为 "**boost**", 先考虑关于 $x$ 轴的 $boost$, 即 $y'=y, z'=z$, 其生成元可以假设为 :
$$
K_x
= \begin{pmatrix} \underset{记作\ k_x}{\underbrace{\begin{pmatrix} a & b \\  c & d \end{pmatrix}} }  &  \\   & \begin{pmatrix} 0 & 0 \\  0 & 0 \end{pmatrix} \end{pmatrix}
$$
代入 $K^T\eta + \eta K = 0$ 得到 :
$$
K_x = \begin{pmatrix} 0 & 1 & 0 & 0 \\ 1 & 0 &  0 & 0\\ 0 & 0 & 0 & 0 \\  0 & 0 & 0 & 0 \end{pmatrix}
$$
类似的有 :
$$
K_y = \begin{pmatrix} 0 & 0 & 1 & 0 \\ 0 & 0 &  0 & 0\\ 1 & 0 & 0 & 0 \\  0 & 0 & 0 & 0 \end{pmatrix}, \quad
K_z = \begin{pmatrix} 0 & 0 & 0 & 1 \\ 0 & 0 &  0 & 0\\ 0 & 0 & 0 & 0 \\  1 & 0 & 0 & 0 \end{pmatrix}
$$
根据 $Lie$ 代数和 $Lie$ 群的关系 $\Lambda_x = e^{\phi K_x}$, 可以得到 $boost$ 群元的矩阵表示. 注意到 $k_x^2=I_{2\times 2}$, 那么
$$
 \begin{aligned}
\Lambda_{x}(\phi)  =\mathrm{e}^{\phi k_{x}}
&=\sum_{n=0}^{\infty} \frac{\phi^{n} k_{x}^{n}}{n!}=\sum_{n=0}^{\infty} \frac{\phi^{2 n}}{(2 n)!} \underbrace{k_{x}^{2 n}}_{=1}+\sum_{n=0}^{\infty} \frac{\phi^{2 n+1}}{(2 n+1)!} \underbrace{k_{x}^{2 n+1}}_{=k_{x}} \\
& =\left(\sum_{n=0}^{\infty} \frac{\phi^{2 n}}{(2 n)!}\right) I+\left(\sum_{n=0}^{\infty} \frac{\phi^{2 n+1}}{(2 n+1)!}\right) k_{x} \\ \\
& =\left(\begin{array}{cc}
\cosh (\phi) & 0 \\
0 & \cosh (\phi)
\end{array}\right)+\left(\begin{array}{cc}
0 & \sinh (\phi) \\
\sinh (\phi) & 0
\end{array}\right) \\ \\
& =\left(\begin{array}{cc}
\cosh (\phi) & \sinh (\phi) \\
\sinh (\phi) & \cosh (\phi)
\end{array}\right)
\end{aligned}
$$
即 :
$$
\Lambda_x(\phi) = \left(\begin{array}{cc}
\mathrm{ch} \phi & \mathrm{sh} \phi & &\\
\mathrm{sh} \phi & \mathrm{ch} \phi & & \\
& & 1 & \\
& & & 1
\end{array}\right)
$$
对应的正是洛伦兹变换的双曲旋转形式.
## 2. '邪教' $ict$
狭义相对论($SR$)当中的度规一般有两种形式: $(-,+,+,+)$ 和 $(+,-,-,-)$,  这两种描述体系并无多大区别. 然而还有第三种描述, 它把时空坐标记为 $(ict, \vec x)$. 这样做有几个好处:

- <font color="#92d050">复欧氏空间的结构</font>

四维间隔在这种描述下变为 $ds^2 = g_{\alpha\beta} \mathrm{d}x^\alpha \mathrm{d}x^\beta = (ict)^2 + x^2 + y^2 + z^2$, 也就是说度规就是单位矩阵, 这和欧式空间度量距离的方式是一致的, 只不过因为引入了复数而变成了复欧式空间. 这也意味着协变和逆变指标是不必要的, 我们完全可以像欧氏空间一样只使用一种指标.

- <font color="#92d050">双曲旋转的自然引入</font>

在复欧式空间做旋转, 自然就会变成双曲旋转的形式, 即:
$$
\begin{bmatrix} ict' \\ x' \\ y' \\ z' \end{bmatrix}
=
\begin{bmatrix} \cos\phi & -\sin\phi & & \\ \sin\phi & \cos\phi & &  \\  &  & 1 \\  &  & & 1 \end{bmatrix}
\begin{bmatrix} ict \\ x \\ y \\ z \end{bmatrix}
\quad\to\quad
\begin{aligned}
x'&=cosh(i\phi)\cdot x-sinh(i\phi)\cdot ct\\
ct'&=-sinh(i\phi)\cdot x+cosh(i\phi)\cdot ct
\end{aligned}
$$
如果选取旋转角度等于此时的 $-i\phi$, 那么上式就是洛伦兹变换的复双曲旋转形式.

- <font color="#92d050">洛伦兹变换的正交性</font>

复欧氏空间的旋转矩阵显然也是正交的, 意味着可以运用正交变换的工具对其进行分析, 它可以表示成:
$$
\begin{bmatrix} ict' \\ x' \\ y' \\ z' \end{bmatrix}
=
\begin{bmatrix} \gamma & -i\beta\gamma & & \\ i\beta\gamma & \gamma & &  \\  &  & 1 \\  &  & & 1 \end{bmatrix}
\begin{bmatrix} ict \\ x \\ y \\ z \end{bmatrix}
$$

那么, 既然 $(ict, \vec x)$ 的表述如此清晰, 为什么被一些人称为"邪教"?

- <font color="#92d050">物理意义模糊</font>

复数时间是什么? 时间的方向性淹没在虚数单位中, 该如何得到时空的因果关系(光锥, 类时/类空间隔)? 虚数空间的描述无法解决这两个问题.

- <font color="#92d050">与广义相对论的不兼容</font>

在广义相对论($GR$)中, 时空是动态弯曲的, 其几何由爱因斯坦场方程描述, 但是基于平直欧式时空的 $ict$ 似乎不容易直接推广到 $GR$ (如果你能做到或许可以发几篇 $paper$). 相比之下, 从狭相的闵可夫斯基空间向广相的黎曼空间的推广是已经成熟且成功的.

- <font color="#92d050">经典教材的排斥</font>

朗道, 格里菲斯, 费曼等的教材都采用了四维描述, $ict$ 似乎是一种更为小众的选择.

所以:
![[1742564912998.jpg#pic_center|550]]



# 参考
- *电动力学讲义* by 陶鑫
- *Physics from Symmetry* by Jakob Schwichtenberg.
- *广义相对论基础* by 赵峥,刘文彪.
- *电动力学导论* by griffth.

