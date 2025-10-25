---
{"dg-publish":true,"permalink":"/_Documents/words/qld words- Calculation of pitch angle and energy diffusion coefficients with the PADIE code/","noteIcon":"default","created":"2025-08-05T23:27:42.886+08:00","updated":"2025-09-15T18:43:59.346+08:00"}
---

### 0.1.1 Calculation of pitch angle and energy diffusion coefficients with the PADIE code  


> [!info] note
> 
> <span style="background:#fff88f">yellow highlight</span>:  significant/notable viewpoints, some relatively important facts
> 
> <span style="background:#d3f8b6">green highlight</span>:  questions, why?
> 
> squiggle text:  specific terms
>
>  <u>underline text</u>:  unfamiliar words
> 
> <span style="background:#fff88f">squiggle text with yellow highlight</span>:  very important viewpoints, facts, etc.


- predominantly 绝大多数地, 主要地
- astrophysical 天体物理的
- Z mode waves 

```col
> [!info] note Z mode waves
> $\quad$磁化等离子体中的**电子回旋波**（Electron Cyclotron Wave），属于电磁波与静电波的混合模式。  **命名由来**：在冷等离子体色散关系的 **"寻常波（O-mode）–异常波（X-mode）"** 分类中，Z 模是 X-mode 在高密度区域（$\omega_{pe} > \Omega_e$）的分支解，因色散曲线呈"Z"字形得名。
> ## 冷等离子体近似（Cold Plasma Model）  
> ### 色散方程（Stix 方程）
>   $ n^2 = \frac{RL - PS}{S \sin^2 \theta + RL \cos^2 \theta} $
>   其中： $n = kc/\omega$ 为折射率, 以及:
> $
> R = 1 - \sum_s \frac{\omega_{ps}^2}{\omega(\omega + \Omega_s)} , \quad
> L = 1 - \sum_s \frac{\omega_{ps}^2}{\omega(\omega - \Omega_s)},\quad
> S = (R+L)/2 ,\quad
> P = 1 - \sum_s \frac{\omega_{ps}^2}{\omega^2} $
> 
> ### 低频分支（Slow Z-mode）
> 频率：$ \omega_{\text{LH}} < \omega < \Omega_e $
> 存在条件：$ \omega_{pe} < \Omega_e \text{（低密度磁化等离子体）}$
> 
> ## 热等离子体修正（Thermal Effects）
> ### 高频分支（Fast Z-mode）的色散关系（Vlasov 方程导出）：
>   $ D(k, \omega) = 1 - \frac{k_\parallel^2 c^2}{\omega^2} + \sum_{n=-\infty}^{\infty} \Pi_n = 0 $
> 其中 $\Pi_n$ 包含电子回旋共振项 $J_n(k_\perp \rho_e) e^{-i n \theta}$, 具体形式依赖等离子体分布函数(e.g. Maxwellian). 频率范围:
>   $ \max(\Omega_e, \omega_{pe}) < \omega < \omega_{\text{UH}} \quad (\omega_{\text{UH}} = \sqrt{\omega_{pe}^2 + \Omega_e^2}) $
> ## 物理效应对比
> 
> | **过程**     | 低频 Z 模                     | 高频 Z 模          |
> | ---------- | -------------------------- | --------------- |
> | **扩散类型**   | 投掷角扩散 ($D_{\alpha\alpha}$) | 能量扩散 ($D_{EE}$) |
> | **电子能量响应** | 10–100 keV                 | 0.1–5 MeV       |
> 
> ## 理论争议与前沿问题
> 1. **相对论效应**：
>    对 >5 MeV 电子的加速需引入**相对论性回旋共振**：
>    $ \omega = \frac{n \Omega_e}{\gamma} \quad (\gamma = 1 + E_e / m_ec^2) $
>    
> 2. **三维传播模型(?)**：
>    非均匀磁场中的射线路径方程：
>    $ \frac{d}{ds}\left( \frac{\partial D}{\partial \mathbf{k}} \right) = \frac{\partial D}{\partial \mathbf{r}} $
> 
> 
```

- flat top 
>  during storm times, electron acceleration by whistler mode waves is most efficient in regions of low density [Horne et al., 2003a, 2005] and is associated with <u>flat top</u> pitch angle distributions [Horne et al., 2003b]

指在一定的投掷角范围内（通常是中等角度，比如 30° 到 150° 之间），粒子的通量（或数量）变化很小，呈现出 “平坦” 的特征（类似一个 “平顶”）；而在接近 0° 或 180°（沿磁场方向或反方向）的角度，粒子通量可能明显降低。这种分布形态是电子被哨声波（whistler mode waves）加速后的典型特征之一，常与磁暴期间的高能电子过程相关。  

- considerably 相当地, 非常
- PADIE (Pitch Angle and Energy Diffusion of Ions and Electrons)
- spatially uniform particle distribution function 空间均匀粒子分布函数
- ambient 环境的, 周围的
- specify 明确指出; 具体说明
- integrand 被积函数
- substitute 取代, 代替
- intersect 相交, 交叉
- provided that 假如, 只要
- cutoff frequencies 截止频率
- tabulate 制成表格; 使成平面
- evaluate [生]求(方程, 公式, 函数的)数值
- integrable singularities 可积的奇异点
- bounded 有界的
- subdivide 细分, 再分割
- succession 更迭
- uncorrelated 不相关的
- stochastic [数]随机的
- net flux 通量
- pronounced 显著的
- modest 不太多的, 适中的
- omit 省略, 遗漏
- energization 通电, 激发, 激励






























