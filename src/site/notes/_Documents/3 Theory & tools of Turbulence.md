---
{"dg-publish":true,"permalink":"/_Documents/3 Theory & tools of Turbulence/","noteIcon":"default","created":"2025-10-20T19:17:19.143+08:00","updated":"2025-11-04T12:13:25.526+08:00"}
---


# 1 Turbulence: The legacy of A.N. Kolmogorov
Frisch, U. (1995). _Turbulence: The legacy of A.N. Kolmogorov_. Cambridge University Press. [https://doi.org/10.1017/CBO9780511623343](https://doi.org/10.1017/CBO9780511623343)  

# 2 A Practical Guide to Wavelet Analysis (read partially)  
Torrence, C., & Compo, G. P. (1998). A practical guide to wavelet analysis. _Bulletin of the American Meteorological Society_, 79(1), 61-78. doi: [10.1175/1520-0477(1998)079<0061:APGTWA>2.0.CO;2](https://doi.org/10.1175/1520-0477\(1998\)079%3C0061:APGTWA%3E2.0.CO;2)
## 2.1 简介
通过大气科学中的 El Niño–Southern Oscillation (ENSO) 现象的例子，给出了一个实用的小波变换(Wavelet Analysis)过程的指南，并包含统计显著性检验。  
### 2.1.1 Wavelet analysis
WFT(Windowed Fourier transform ) 是一种从信号中提取局部频率信息的分析工具，Window 指的是 sliding segment，对比：  

| 对比      | WFT                                                             | Wavelet analysis                                                                                               |                                        |
| ------- | --------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| 尺度特性    | 固定窗口大小 $T$，时频分辨率固定不可调。                                          | 动态调整窗口大小；高频窄窗高时间分辨率，低频宽窗高频率分辨率。尺度 $s$ 与傅里叶周期 $\lambda$ 近似相关 ($\lambda \approx 1.03s$ for Morlet $\omega_0=6$)。 |                                        |
| 时频精度    | 不准确性源于不在窗口频率范围内的高频、低频成分混叠；高频成分因窗口过宽导致时间定位模糊，低频成分因窗口过窄导致频率分辨率不足。 | 时频分辨率自适应，显著减少混叠；擅长捕捉非平稳信号；存在“影响锥 (COI)”区域（边缘效应）。                                                               |                                        |
| 计算效率    | 计算冗余高，每个时间步需分析 $T/(2\delta t)$ 个频率；需多次尝试窗口长度 $T$。               | 可通过 DFT 和卷积定理快速计算；非正交小波尺度集可由 $s_j = s_0 2^{j\delta j}$ (j=0,1,…,J) 灵活设置；可通过时间或尺度平均提高效率。                        |                                        |
| 适用场景    | 适用于平稳信号或主导频率范围固定的信号；仅提取信号局部频率信息。                                | 适用于多频率非平稳时间序列（如 Niño 3 SST）；主导频率范围广的分析；可扩展至交叉小波谱、相干性等。                                                         |                                        |
| 能量聚焦性   | 能量分散在固定时频区域，高频瞬态信号易频谱泄漏。                                        | 通过特定小波基函数实现能量高度集中；归一化小波功率谱 $\| W_n(s)\|^2/\sigma^2$ 清晰反映信号相对白噪声的功率分布。 |
| 参数调整复杂度 | 需手动选择窗函数类型和窗口长度 $T$，依赖经验，缺乏自适应性。                                | 需选择小波基函数（如 Morlet, DOG）和尺度参数 ($s_0, \delta j$)；基函数针对特定信号优化，尺度参数可通过公式确定，人为干预少。                                  |                                        |
| 多分辨率能力  | 无多分辨率分析能力；需更换窗口长度间接调整分辨率，操作繁琐。                                  | 支持多分辨率分析：时间平均得“全局小波谱”；尺度平均得特定频段功率时间序列（如 $2-8$ 年 ENSO 频段方差）；可用于滤波。                                              |                                        |

- 在时间序列两端进行零填充，可以一定程度上减小影响锥(Cone of influence (COI))范围(section 3g);
- 一般选取指数尺度集 $s_j = s_{min} 2^{j\delta j}$，对于莫雷小波 $\delta j \leq 0.5$，$s_0$ 应选择使等效傅立叶周期近似为 $2\delta t$ (section 3f & 3h);
- 重构(section 3i)
$$
x_{n}=\frac{\delta j \delta t^{1 / 2}}{C_{\delta} \psi_{0}(0)} \sum_{j=0}^{J} \frac{\Re\left\{W_{n}\left(s_{j}\right)\right\}}{s_{j}^{1 / 2}} .
$$
$x_n$ 的方差是(类似于 Fourier 变换的 Parseval 等式)：  
$$
\sigma^{2}=\frac{\delta j \delta t}{C_{\delta} N} \sum_{n=0}^{N-1} \sum_{j=0}^{J} \frac{\left|W_{n}\left(s_{j}\right)\right|^{2}}{s_{j}}
$$








## 2.2 链接
本地 [[_Documents/docs/3.2 A Practical Guide to Wavelet Analysis.pdf|2.2 A Practical Guide to Wavelet Analysis]]
## 2.3 补充
词汇 [[_Documents/words/words - A practical guide to wavelet analysis\|words - A practical guide to wavelet analysis]]

