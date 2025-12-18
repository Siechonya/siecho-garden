---
{"dg-publish":true,"permalink":"/_Documents/3 Theory & tools & observation of Turbulence/","noteIcon":"default","created":"2025-10-23T14:37:03.120+08:00","updated":"2025-12-15T23:09:37.727+08:00"}
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
x_{n}=\frac{\delta j \delta t^{1 / 2}}{C_{\delta} \psi_{0}(0)} \sum_{j=0}^{J} \frac{\Re\left\{W_{n}\left(s_{j}\right)\right\}}{s_{j}^{1 / 2}} \tag{1}
$$
$x_n$ 的方差是(类似于 Fourier 变换的 Parseval 等式)：  
$$
\sigma^{2}=\frac{\delta j \delta t}{C_{\delta} N} \sum_{n=0}^{N-1} \sum_{j=0}^{J} \frac{\left|W_{n}\left(s_{j}\right)\right|^{2}}{s_{j}}
\tag{2}
$$
### 2.1.2 理论功率谱和显著性检验水平  
> [!tips] 红噪声和白噪声
> To determine significance levels for either Fourier or wavelet spectra, one first needs to choose an appropriate background spectrum. It is then assumed that different realizations of the geophysical process will be randomly distributed about this mean or expected background, and the actual spectrum can be compared against this random distribution. For many geophysical phenomena, an appropriate background spectrum is either white noise (with a flat Fourier spectrum) or red noise (increasing power with decreasing frequency).

一个红噪声的简单模型是单变量滞后自回归(univariate lag-1 autoregressive)：  
$$
x_n = \alpha x_{n-1} + z_n,\quad x_0 = 0, \quad z_n \in \{\text {Guassian \ white \ noise}\} \tag{3}
$$
$\alpha$ 決定序列中相邻数据点之间的关联程度(“红”度)。除以 $\frac{N}{2\sigma^2}$ 归一化得到噪声谱：  
$$
P_{k}=\frac{1-\alpha^{2}}{1+\alpha^{2}-2 \alpha \cos (2 \pi k / N)} \tag{4}
$$
lag-2 红噪同理。若上述噪声回归方程是全局的，则是傅里叶红噪声。可以使局域/很小的垂直切片满足(3)式，得到小波红噪声谱。  

> [!tips] 零假设和显著性水平
> The null hypothesis is defined for the wavelet power spectrum as follows: It is assumed that the time series has a mean power spectrum, possibly given by (4); if a peak in the wavelet power spectrum is significantly above this background spectrum, then it can be assumed to be a true feature with a certain percent confidence. For definitions, “significant at the 5% level” is equivalent to “the 95% confidence level,” and implies a test against a certain background level, while the “95% confidence interval” refers to the range of confidence about a given value.





## 2.2 链接
本地 [[_Documents/docs/3.2 A Practical Guide to Wavelet Analysis.pdf|2.2 A Practical Guide to Wavelet Analysis]]
## 2.3 补充
词汇 [[_Documents/words/Part.3 words#2 A practical guide to wavelet analysis\|_Documents/words/Part.3 words#2 A practical guide to wavelet analysis]]

# 3 Characterization of turbulence in the Mars plasma environment with MAVEN observations  (partially)
Ruhunusiri, S., et al. (2017), Characterization of turbulence in the Mars plasma environment with MAVEN observations, _J. Geophys. Res. Space Physics_, 122, 656–674, doi:10.1002/2016JA023456.
## 3.1 简介  
> [!info] 摘要  
> 我们首次通过计算磁场波动(magnetic field fluctuations)的谱指数(slopes in the magnetic field power spectra)并确定它们随频率和在不同区域的变化，来表征火星等离子体环境中的湍流。
> 
> 与太阳风不同，在磁鞘中，我们发现惯性区缺失(an absence of the inertial range)，该区域的谱指数值等于科尔莫戈罗夫定标值 $-5/3$。相反，正如在其他行星的磁鞘中观察到的那样，我们发现谱指数从低频(低于质子回旋频率(gyrofrequency))的接近 $-0.5$ 的低负值过渡到高频(高于质子回旋频率)的远低于 $-5/3$ 的值。这表明原始太阳风(pristine solar wind)在火星弓激波处被改变，并且波动主要由磁鞘中局部产生的波动主导。
> 
> 缺乏具有科尔莫戈罗夫定标值的谱指数表明，磁鞘中的波动没有足够的时间相互作用，从而未能导致充分发展的能量级联(a fully developed energy cascade)。
> 
> 在磁场堆积边界(magnetic pileup boundary, MPB)附近，低频范围观察到接近科尔莫戈罗夫定标值的谱指数，这表明存在充分发展的能量级联。
> 
> 在尾迹(wake，不是磁尾 magnetic tail)中，我们发现低频和高频范围的谱指数大致相同，通常接近 $-2$。
> 
> 我们观察到谱指数的季节性变化，主要在上游区域，这表明质子回旋波(proton cyclotron waves)存在季节性变化。  
> 

### 3.1.1 背景介绍
### 3.1.2 方法  
- refer to the lower fre quency range ($<f_{H^+}$) as <font color="#ff0000">the MHD range</font> and the higher frequency range ($>f_{H^+}$) as<font color="#ff0000"> the kinetic range</font>.

- 使用小波变换得到幂律谱(power spectral densities (PSDs) for the magnetic field fluctuations)
$$
\operatorname{PSD}(f)=\frac{2 \Delta t}{N} \sum_{j=1}^{N}\left|W_{x}\left(t_{j}, f\right)\right|^{2}+\left|W_{y}\left(t_{j}, f\right)\right|^{2}+\left|W_{z}\left(t_{j}, f\right)\right|^{2}
$$
借助积累的数据和网格划分，得到数据密度和本地质子回旋频率 $f_{H^+}$ (中位数)的分布：
![zz_figure/Pasted image 20251207135956.png](/img/user/zz_figure/Pasted%20image%2020251207135956.png)
绘制上图选取的几个具有代表性的网格单元的谱 PSD (下图的 cdef 对应上图的 bcde 单元, 这是文章的绘图编号错误)
![zz_figure/Pasted image 20251207140133.png](/img/user/zz_figure/Pasted%20image%2020251207140133.png)
以及 spectral index value 的空间分布
![zz_figure/Pasted image 20251203224423.png](/img/user/zz_figure/Pasted%20image%2020251203224423.png)  
谱斜率的时间分布  
![zz_figure/Pasted image 20251207211416.png](/img/user/zz_figure/Pasted%20image%2020251207211416.png)

根据太阳黄经 Ls (Solar Longitude)：$Ls = 0^{\circ},90^{\circ},180^{\circ},270^{\circ}$：春分/夏至/秋分/冬至（北半球春/夏/秋/冬季开始），可以绘制谱的季节变化：  
![zz_figure/Pasted image 20251207150801.png](/img/user/zz_figure/Pasted%20image%2020251207150801.png)
可见  
> The MHD range spectral indices show seasonal variability in the upstream region and in the magneto-sheath, while the kinetic range spectral indices show seasonal variability in the upstream region and in the night-side magnetic pileup region.   

这是因为  
> During these times($Ls = 0^{\circ},90^{\circ},180^{\circ},270^{\circ}$) the distance from Sun to Mars is approximately 1.56, 1.65, 1.45, and 1.38 AU, respectively. Due to the changes in the distance between Mars and the Sun, the solar <font color="#ff0000">EUV flux</font> at Mars varies seasonally (差值约达 $\propto \left(\frac{r_{\text{Aphelion}}}{r_{\text{Perihelion}}}\right)^2-1 = \left(\frac{2.492 \times 10^8 \text{ km}}{2.067 \times 10^8 \text{ km}}\right)^2 \approx (1.205)^2-1 \approx45\%$), and the exospheric density varies accordingly.  

特定区域的谱的季节变化:  
![zz_figure/Pasted image 20251207152752.png](/img/user/zz_figure/Pasted%20image%2020251207152752.png)
这表明前面那个编号错误的图的第一行两个子图，只是上图的第一行的两个子图中 $Ls = 270^\circ$ 的特例，即距离太阳最近的时刻。$E$ 为 the upstream electric field refers to the upstream convection electric field given by $E = −V _{SW}\times B_{IMF,upstream}$，文章关注 asymmetry，所以 $E>0$ 实际上是 $Z_{MSE}>0$。  
> [!tips] newly born pickup ions should <font color="#ff0000">preferentially excite upstream waves in the positive electric field side</font>.   
> refer to \[section 5\]:  
> 
> Closer to Mars, protons are created by photoionization, charge exchange, and electron impact ionization of the neutral hydrogen exosphere. These ions are subsequently accelerated in the upstream solar wind electric field direction and neutralized by charge exchange due to the collisions with the neutral exospheric atoms. <font color="#ffc000">These drifting neutrals, which are prominently in the E > 0 region</font>, then undergo ionizations forming newly born pickup ions which excite proton cyclotron waves preferentially in the E > 0 region [Russell et al., 2006]. Thus, if the waves are generated by mechanism 2 mentioned above, they should occur more frequently in the E > 0 hemisphere.

- 谱噪声估计
> we verified that the PSDs used for computing the median lie above the MAG noise level, shown by the black curves in Figures 3c–3f(即上面编号错误的图中的黑色曲线). <font color="#ff0000">The MAG noise level was estimated as the minimum PSD value when MAVEN was upstream of the bow shock</font> during the time interval from November 2014 to April 2016.

- the sign of $B_{XMSE}$ or the X − MSE component of the magnetic field is indicative of the foreshock locations.
<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="Drawing_2025-12-07_1452.32.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.18.0","elements":[{"id":"ZJndORfzMAhIIT2OyjUso","type":"image","x":-388.5151330856088,"y":-226.3377696621702,"width":555,"height":268,"angle":0,"strokeColor":"transparent","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"index":"a0","roundness":null,"seed":383847370,"version":56,"versionNonce":637703382,"isDeleted":false,"boundElements":[{"id":"YdByXCDV4ilQPXmcWuKoK","type":"arrow"},{"id":"LHmtR_D7nYnlJVw3nAHKf","type":"arrow"},{"id":"FAIYXBMAKnrxTsQ-zs6Xk","type":"arrow"},{"id":"XTQp_4Uf8-5xEAs3xcmaV","type":"arrow"}],"updated":1765090560221,"link":null,"locked":false,"status":"pending","fileId":"f94d24792e08a22c461379eca0b575adfd070a36","scale":[1,1],"crop":null},{"id":"YdByXCDV4ilQPXmcWuKoK","type":"arrow","x":-289.0330281612921,"y":-132.42423409719657,"width":13.806923242510152,"height":14.326866691928444,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a1","roundness":null,"seed":538780042,"version":262,"versionNonce":163940886,"isDeleted":false,"boundElements":[],"updated":1765090560222,"link":null,"locked":false,"points":[[0,0],[13.806923242510152,-14.326866691928444]],"startBinding":{"elementId":"ZJndORfzMAhIIT2OyjUso","mode":"inside","fixedPoint":[0.17924703589966967,0.35042364016781197]},"endBinding":{"elementId":"ZJndORfzMAhIIT2OyjUso","mode":"inside","fixedPoint":[0.20412437507536366,0.29696518236210884]},"startArrowhead":null,"endArrowhead":"triangle","elbowed":false,"moveMidPointsWithElement":true},{"id":"LHmtR_D7nYnlJVw3nAHKf","type":"arrow","x":-280.47638162950346,"y":-120.48650457141562,"width":16.399118812072572,"height":12.612209670209666,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a4","roundness":null,"seed":1856518602,"version":273,"versionNonce":2079840086,"isDeleted":false,"boundElements":[],"updated":1765090560222,"link":null,"locked":false,"points":[[0,0],[16.399118812072572,-12.612209670209666]],"startBinding":null,"endBinding":{"elementId":"ZJndORfzMAhIIT2OyjUso","mode":"inside","fixedPoint":[0.2242123788615818,0.34790692321098843]},"startArrowhead":null,"endArrowhead":"triangle","elbowed":false,"moveMidPointsWithElement":false},{"id":"FGFJY4JWOm8Ml-SJtR_pI","type":"arrow","x":-271.2846584014027,"y":-107.4727271915523,"width":16.571010358066133,"height":9.861353923678948,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a5","roundness":null,"seed":1850592394,"version":368,"versionNonce":695432458,"isDeleted":false,"boundElements":[],"updated":1765090563287,"link":null,"locked":false,"points":[[0,0],[16.571010358066133,-9.861353923678948]],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":"triangle","elbowed":false,"moveMidPointsWithElement":false},{"id":"FAIYXBMAKnrxTsQ-zs6Xk","type":"arrow","x":-266.7619520261203,"y":-92.38316522022052,"width":17.748079100929942,"height":8.790155518447165,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a6","roundness":null,"seed":2014600010,"version":270,"versionNonce":619609238,"isDeleted":false,"boundElements":[],"updated":1765090560222,"link":null,"locked":false,"points":[[0,0],[17.748079100929942,-8.790155518447165]],"startBinding":null,"endBinding":{"elementId":"ZJndORfzMAhIIT2OyjUso","mode":"inside","fixedPoint":[0.25135362191066385,0.46703152583396457]},"startArrowhead":null,"endArrowhead":"triangle","elbowed":false,"moveMidPointsWithElement":false},{"id":"XTQp_4Uf8-5xEAs3xcmaV","type":"arrow","x":-265.63781845207245,"y":-79.11838904645646,"width":21.34530653788289,"height":0.47156707049339275,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":1,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a7","roundness":null,"seed":591807382,"version":322,"versionNonce":1516141014,"isDeleted":false,"boundElements":[],"updated":1765090560222,"link":null,"locked":false,"points":[[0,0],[21.34530653788289,-0.47156707049339275]],"startBinding":null,"endBinding":{"elementId":"ZJndORfzMAhIIT2OyjUso","mode":"inside","fixedPoint":[0.2598605786872419,0.5475664684523147]},"startArrowhead":null,"endArrowhead":"triangle","elbowed":false,"moveMidPointsWithElement":false},{"id":"6c7jwGsG","type":"image","x":-307.1828691773184,"y":-133.91774745487115,"width":19,"height":15,"angle":0,"strokeColor":"#000000","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"roundness":null,"seed":50464,"version":74,"versionNonce":1889365782,"updated":1765090590220,"isDeleted":false,"groupIds":[],"boundElements":[],"link":null,"locked":false,"frameId":null,"fileId":"d8096dcecba0279562d48f253334a25429877ae4","scale":[1,1],"index":"a8","status":"pending","crop":null}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"solid","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":0,"currentItemOpacity":100,"currentItemFontFamily":5,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"triangle","currentItemArrowType":"sharp","currentItemFrameRole":null,"scrollX":655.4753649621518,"scrollY":444.1760488723923,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":20,"gridStep":5,"gridModeEnabled":false,"gridColor":{"Bold":"rgba(217, 217, 217, 0.5)","Regular":"rgba(230, 230, 230, 0.5)"},"currentStrokeOptions":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true,"markerName":true,"markerEnabled":true},"objectsSnapModeEnabled":false,"activeTool":{"type":"selection","customType":null,"locked":false,"fromSelection":false,"lastActiveTool":null},"disableContextMenu":false},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Drawing_2025-12-07_1452.32.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
$\theta=\langle B,X_{MSE} \rangle$, When $B_{XMSE} > 0$ or when $0^\circ < θ < 90^\circ$ the quasi-parallel shock(where $\langle \vec{n}, \vec{ B}\rangle \in [0^\circ,45^\circ]$) or the foreshock region is located at $Y_{MSE} > 0$, whereas the quasi-perpendicular shock region is located at $Y_{MSE} < 0$. When $B_{XMSE} < 0$ or when $90^\circ < θ < 180^\circ$ the quasi-parallel shock region is located at $Y_{MSE} < 0$, whereas the quasi-perpendicular shock region is located at $Y_{MSE} > 0$.
>  <font color="#ff0000">In the quasi-parallel region we expect enhanced perturbations</font> due to the generation of waves via bow shock <font color="#ffc000">reflected solar wind ions</font> (<font color="#ffc000">the waves are generated efficiently when the particle populations back stream quasi-parallel to the magnetic field</font> \[Gary, 1991\]) and also reflected pickup ions from Mars’ extended hydrogen exosphere. 

在考虑不同区域的网格划分、MHD/Kinetic 尺度、季节变化之后，继续添加：准垂直/平行约束或者 $E<0\ or\ E>0$ 的区分，就得到  

| ![zz_figure/Pasted image 20251207161337.png](/img/user/zz_figure/Pasted%20image%2020251207161337.png) | ![zz_figure/Pasted image 20251207161358.png](/img/user/zz_figure/Pasted%20image%2020251207161358.png) |
| ------------------------------------ | ------------------------------------ |
| ![zz_figure/Pasted image 20251207170826.png](/img/user/zz_figure/Pasted%20image%2020251207170826.png) | ![zz_figure/Pasted image 20251207170813.png](/img/user/zz_figure/Pasted%20image%2020251207170813.png) |
发现两者很相似。
### 3.1.3 讨论  
在太阳风的 MHD range 中，谱斜率的典型值为 $-\frac{5}{3}$。对于 $Ls=0^\circ,90^\circ$ 的 upstream region 的确接近该值，但谱斜率仍然 takes a wide range，因为  
>  The quasi-parallel region can be highly disturbed due to the presence of proton cyclotron waves that can be excited by reflected solar wind protons from the bow shock. Since Mars also has an extended hydrogen exosphere which can give rise to pickup proton populations upstream of Mars, it can also contribute to the generation of upstream proton cyclotron waves. The median magnetic field spectra computed in the upstream region contain all these contributing effects

在太阳风的 Kinetic range 中，谱斜率的典型值为 $-2.8$ \[Sahraoui et al., 2010; Roberts et al., 2013; Sahraoui et al., 2013; Roberts et al., 2015\]。观测与之相近却不完全一致，These differences should be a consequence of Mars upstream phenomena which perturb the turbulence characteristics of the pristine solar wind.

## 3.2 补充  
词汇 [[_Documents/words/Part.3 words#3 Characterization of turbulence in the Mars plasma environment with MAVEN observations\|Part.3 words]]
## 3.3 链接
本地 [[_Documents/docs/3.3 Ruhunusiri et al_2017_Characterization of turbulence in the Mars plasma environment with MAVEN.pdf|3.3 Ruhunusiri et al_2017_Characterization of turbulence in the Mars plasma environment with MAVEN]]
