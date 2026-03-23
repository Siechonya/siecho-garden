---
{"dg-publish":true,"permalink":"/电动26春/EMD_answer_phj/HW3 Answer/","noteIcon":"default","created":"2026-03-20T16:08:00.771+08:00","updated":"2026-03-20T21:41:04.292+08:00"}
---



# 1 《电磁学与电动力学》（下册）
![zz_figure/Pasted image 20260320160834.png](/img/user/zz_figure/Pasted%20image%2020260320160834.png)  
![zz_figure/Pasted image 20260320160847.png](/img/user/zz_figure/Pasted%20image%2020260320160847.png)  

![zz_figure/Pasted image 20260320160901.png](/img/user/zz_figure/Pasted%20image%2020260320160901.png)  
![zz_figure/Pasted image 20260320160912.png](/img/user/zz_figure/Pasted%20image%2020260320160912.png)  
![zz_figure/Pasted image 20260320160939.png](/img/user/zz_figure/Pasted%20image%2020260320160939.png)  

# 2 补充题  
## 2.1 单色平面波
从 Maxwell's equations 得到自由空间的电磁势演化方程为
$$
\begin{align} 
\nabla^2 \varphi + \frac{ \partial  }{ \partial t } \mathsf{C} &= 0 \tag{1} \\[4pt]
\square^2 \boldsymbol{A} - \nabla \mathsf{L} &= 0 \tag{2}
\end{align}
$$
此处 $\mathsf{C}, \mathsf{L}$ 代表库伦规范和洛伦茨规范。  

对于库伦规范 $\mathsf{C}= 0$, 得到  
$$
\begin{align} 
(1) &\quad\Longrightarrow\quad k^2\varphi_0 = 0 \overset{\text{平面波 } k \neq 0}{\quad\Longrightarrow\quad} \varphi = 0 \quad\Longrightarrow\quad \varphi 与 \boldsymbol{A} 独立
\\[4pt]
(2) &\quad\Longrightarrow\quad -k^2 + \frac{\omega^2}{c^2} = 0 \quad\Longrightarrow\quad \omega = ck\ (电磁波)
\\[4pt]
\nabla \cdot &\boldsymbol{A} = 0 \quad\Longrightarrow\quad \boldsymbol{k} \cdot \boldsymbol{A_0} = 0
\end{align}
$$
对于洛伦茨规范 $\mathsf{L}= 0$, 得到 
$$
\begin{align} 
(1) &\quad\Longrightarrow\quad\square^2 \varphi = 0 \quad\Longrightarrow\quad \omega = ck
\\[4pt]
(2) &\quad\Longrightarrow\quad -k^2 + \frac{\omega^2}{c^2} = 0 \quad\Longrightarrow\quad \omega = ck
\\[4pt]
\mathsf{L}~ &= 0 \quad\Longrightarrow\quad \varphi_0 = \frac{c^2}{\omega} (\boldsymbol{k} \cdot \boldsymbol{A}_0)
\end{align}
$$
## 2.2 能量中心平动定理  
在诺特定律里面，这个定理和 boost 对称性有关，虽然没什么卵用(refer to [[A_symmetry_自然界的对称性/Tools/Noether's Theorem and Symmetry\|Noether's Theorem and Symmetry]], boost 不变量是 $\int (w \boldsymbol{x} - c^2 t \boldsymbol{g}) dV$，题后提示所指的就是这个守恒量)。很显然，这个东西成立是需要系统是孤立的，也就是散度的体积分为 0.
$$
\int \nabla \cdot \boldsymbol{Sx} \, \mathrm{d}V = \int \nabla \cdot \boldsymbol{T} \, \mathrm{d}V = \oint_{\partial V} \boldsymbol{xS} \cdot \, \mathrm{d} \boldsymbol{\sigma} = \oint_{\partial V} \boldsymbol{T} \cdot \, \mathrm{d} \boldsymbol{\sigma} = 0
$$
先将能量方程乘以 $\vec{x}$，将动量方程乘以 $c^2 t$，注意这两个都是微分方程 
$$
\begin{align} 
\boldsymbol{x} \partial_t w + \boldsymbol{x} \nabla \cdot  \boldsymbol{S} &= - \boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E}) \\[4pt]
c^2 t \partial_t \boldsymbol{g} + c^2 t \nabla \cdot \mathsf{T} &= -c^2t (\rho \boldsymbol{E } + \boldsymbol{j}\times \boldsymbol{B})
\end{align}
$$
改写能量方程成积分形式  
$$
\begin{align} 
\partial_t \int w \boldsymbol{x} \,\mathrm{d}V 
&= - \int \boldsymbol{x} (\nabla \cdot \boldsymbol{S}) \,\mathrm{d}V - \int \boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E}) \,\mathrm{d}V \\[4pt]
&= \int \boldsymbol{S} \,\mathrm{d}V - \int \boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E}) \,\mathrm{d}V \\[4pt]
&= c^2 \boldsymbol{G} - \int \boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E}) \,\mathrm{d}V
\end{align}
$$
这里有两种方法，  

- 其一不需要用到动量守恒方程：$\boldsymbol{R}_C$ 的分母是守恒的总能量可以不管，所以直接对 $\boldsymbol{R}_C$ 的分子部分求导：
$$
\begin{align} 
\frac{ \mathrm{d}  }{ \mathrm{d} t} \left( \sum \mathcal{E}_i \boldsymbol{x}_i + \int w \boldsymbol{x} \,\mathrm{d}V \right) 
&= \sum \left( \frac{\mathrm{d}\mathcal{E}_i}{\mathrm{d}t} \boldsymbol{x}_i + \mathcal{E}_i \boldsymbol{v}_i \right) + \left( c^2 \boldsymbol{G} - \int \boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E}) \,\mathrm{d}V \right) \\[4pt]
&=
{\color{red}\sum q_i \boldsymbol{v}_i \cdot \boldsymbol{E} \boldsymbol{x}_i} + \sum \mathcal{E}_i \boldsymbol{v}_i + c^2 \boldsymbol{G} - {\color{red}\int \boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E} ) \,\mathrm{d}V } \\[4pt]
&= 
\sum \mathcal{E}_i \boldsymbol{v}_i + c^2 \boldsymbol{G} \\[4pt]
&= 
c^2\boldsymbol{P} + c^2 \boldsymbol{G}
\end{align}
$$
所以
$$\boldsymbol{v}_C = \frac{d\boldsymbol{R}_C}{dt} = \frac{c^2 (\boldsymbol{P} + \boldsymbol{G})}{\mathcal{E} + W}$$
由于孤立系统的总动量 $\boldsymbol{P} + \boldsymbol{G}$ 和总能量 $\mathcal{E} + W$ 均为常数，故 $\boldsymbol{v}_C$ 是常矢量。

 - 其二是按照提示的意思继续写，需要改写动量方程为积分形式：
$$
\begin{align} 
\partial_t \int c^2 t \boldsymbol{g} \,\mathrm{d}V 
&= c^2 \boldsymbol{G} + \int c^2 t \partial_t \boldsymbol{g} \,\mathrm{d}V \\[4pt]
&=
c^2 \boldsymbol{G} -c^2t \int (\rho \boldsymbol{E } + \boldsymbol{j}\times \boldsymbol{B}) \,\mathrm{d} V
\end{align}
$$
将积分形式的动量方程和能量方程相减得到：  
$$
\begin{align} 
\frac{ \mathrm{d}  }{ \mathrm{d} t} \left( \int w \boldsymbol{x} \,\mathrm{d}V - c^2 t \boldsymbol{G} \right) 
&= \int \left\{ -\boldsymbol{x} (\boldsymbol{j} \cdot \boldsymbol{E}) + c^2t (\rho \boldsymbol{E } + \boldsymbol{j}\times \boldsymbol{B}) \right\} \,\mathrm{d} V \\[4pt]
&=
-\sum \boldsymbol{x}_i q_i\boldsymbol{v}_i \cdot \boldsymbol{E} + c^2t \frac{ \mathrm{d} \boldsymbol{P} }{ \mathrm{d} t}
\\[4pt]
&=
-\sum \boldsymbol{x}_i \frac{ \mathrm{d}  }{ \mathrm{d} t} \mathcal{E}_i + c^2t \frac{ \mathrm{d} \boldsymbol{P} }{ \mathrm{d} t}
\\[4pt]
&=
-\frac{ \mathrm{d}  }{ \mathrm{d} t} \sum \mathcal{E}_i \boldsymbol{x}_i + {\underset{=c^2\boldsymbol{P}}{\underbrace{\sum \mathcal{E}_i \boldsymbol{v}_i}}} + c^2t \frac{ \mathrm{d} \boldsymbol{P} }{ \mathrm{d} t} \\[4pt]
&=
-\frac{ \mathrm{d}  }{ \mathrm{d} t} \sum \mathcal{E}_i \boldsymbol{x}_i + \frac{ \mathrm{d}  }{ \mathrm{d} t} (c^2 t \boldsymbol{P})
\end{align}
$$
所以  
$$
\frac{ \mathrm{d}  }{ \mathrm{d} t} \left( \sum \mathcal{E}_i \boldsymbol{x}_i + \int w \boldsymbol{x} \,\mathrm{d}V \right) 
= 
\frac{ \mathrm{d}  }{ \mathrm{d} t} (c^2t \boldsymbol{P} + c^2t \boldsymbol{ G})
=
c^2 (\boldsymbol{P }+ \boldsymbol{G})
$$
得到和法一一致的结果。  
# 3 思考题  
## 3.1 
### 3.1.1 
验证给定的势函数是否满足 $\boldsymbol{E} = -\nabla \varphi$ 和 $\boldsymbol{B} = \nabla \times \boldsymbol{A}$ 即可
### 3.1.2 
令 $\vec{u} = \lambda\vec{x}$，则 $u_i = \lambda x_i$。
$$
\frac{d}{d\lambda} F_j(\lambda\vec{x}) = \frac{\partial F_j}{\partial u_i} \frac{du_i}{d\lambda} = \frac{\partial F_j}{\partial u_i} x_i = \frac{1}{\lambda} \left( x_i \frac{\partial F_j}{\partial x_i} \right) = \frac{1}{\lambda} (\vec{x} \cdot \nabla) F_j(\lambda\vec{x})
$$
即：$\frac{d}{d\lambda} \vec{F}(\lambda\vec{x}) = \frac{1}{\lambda} (\vec{x} \cdot \nabla) \vec{F}(\lambda\vec{x})$。

1. 证明 $\vec{B} = \nabla \times \vec{A}$：
$$\nabla \times \vec{A} = -\int_0^1 \lambda \nabla \times (\vec{x} \times \vec{B}(t, \lambda\vec{x})) d\lambda$$
利用$\nabla\times(\vec A\times \vec B)=(\vec B\cdot\nabla)\vec A+(\nabla\cdot\vec B)\vec A-(\vec A\cdot\nabla)\vec B-(\nabla\cdot\vec A)\vec B$，注意此时 $\nabla \cdot \vec{B} = 0$ 且 $(\vec{x} \cdot \nabla) \vec{B}_{\lambda} = \lambda \frac{d}{d\lambda} \vec{B}_{\lambda}$：
$$\nabla \times (\vec{x} \times \vec{B}_{\lambda}) = \vec{x}(0) - \vec{B}_{\lambda}(3) + \vec{B}_{\lambda} - \lambda \frac{d}{d\lambda} \vec{B}_{\lambda} = -2\vec{B}_{\lambda} - \lambda \frac{d}{d\lambda} \vec{B}_{\lambda}$$
角标 $\lambda$ 没有其他含义，只是表示 $\lambda$ 作为当前函数的自变量之一。上式代入积分：
$$\nabla \times \vec{A} = \int_0^1 (2\lambda \vec{B}_{\lambda} + \lambda^2 \frac{d}{d\lambda} \vec{B}_{\lambda}) d\lambda = \int_0^1 \frac{d}{d\lambda} (\lambda^2 \vec{B}(t, \lambda\vec{x})) d\lambda = [\lambda^2 \vec{B}(t, \lambda\vec{x})]_0^1 = \vec{B}(t, \vec{x})$$
2. 证明 $\vec{E} = -\nabla \varphi - \partial_t \vec{A}$：

利用 $\nabla (\vec A\cdot \vec B)=\vec A\times(\nabla\times\vec B)+\vec B\times(\nabla\times\vec A)+(\vec A\cdot\nabla)\vec B+(\vec B\cdot\nabla)\vec A$ 计算 $\nabla \varphi$：
$$\nabla \varphi = -\int_0^1 \nabla (\vec{x} \cdot \vec{E}_{\lambda}) d\lambda = -\int_0^1 [\vec{E}_{\lambda} + (\vec{x} \cdot \nabla)\vec{E}_{\lambda} + \vec{x} \times (\nabla \times \vec{E}_{\lambda})] d\lambda$$
利用法拉第定律 $\nabla_u \times \vec{E} = -\partial_t \vec{B}$，得 $\nabla \times \vec{E}_{\lambda} = -\lambda \partial_t \vec{B}_{\lambda}$：
$$\nabla \varphi = -\int_0^1 [\vec{E}_{\lambda} + \lambda \frac{d}{d\lambda} \vec{E}_{\lambda} - \lambda \vec{x} \times \partial_t \vec{B}_{\lambda}] d\lambda = -\int_0^1 \frac{d}{d\lambda}(\lambda \vec{E}_{\lambda}) d\lambda + \partial_t \int_0^1 \lambda \vec{x} \times \vec{B}_{\lambda} d\lambda$$
$$\nabla \varphi = -\vec{E}(t, \vec{x}) - \partial_t \vec{A} \implies \vec{E} = -\nabla \varphi - \partial_t \vec{A}$$
证毕。.
## 3.2 
磁矢势满足 $U(1)$ 规范：$\vec{A} \to \vec{A}' = \vec{A} + \nabla \Lambda$。

将变换后的 $\vec{A}'$ 同样进行分解，由于 $\nabla \Lambda$ 本身是一个梯度场（无旋），它完全属于纵向分量。根据亥姆霍兹分解的唯一性：
$$\vec{A}'_\parallel + \vec{A}'_\perp = (\vec{A}_\parallel + \nabla \Lambda) + \vec{A}_\perp$$
横向分量 $\vec{A}_\perp$ 在规范变换下保持不变（即它是规范无关的）。  
$$\vec{B} = \nabla \times \vec{A} = \nabla \times (\vec{A}_\parallel + \vec{A}_\perp) = 0 + \nabla \times \vec{A}_\perp = \nabla \times \vec{A}_\perp$$
可以看到，磁场完全由 $\vec{A}_\perp$ 决定。
## 3.3 
参考 ppt