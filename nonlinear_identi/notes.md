# Identification of polynomial nonlinear systems based on center manifold✩
## Significanse:
  1. The nonlinear SS model is identified analytically and the identification error can be rendered arbitrarily small with abosent and ignored transient response
  2. Under the paper's assumption, the CT systems, can be both applied to CT & DT systems.
  3. Drive an explicit condition characterizing how the frequency number can be satisfied to PE condition.

# Nonlinearities Enhance Parameter Convergence in Output-Feedback Systems
## Significanse:
  1. 对于参考输入，设计了一种开环回归将信号丰富度和PE条件联系起来。
  2. 区别于线性系统，并没有得到参考信号越丰富，越能保证收敛；相反，阐述了非线性项可以减少所需要的参考输入信号的数量，也就是非线性项可以提高闭环系统的参数收敛性

# Robust Variable Projection Algorithm for the Identification of Separable Nonlinear Models
## Significanse：
  1. 设计了一种基于Variable Projection的鲁棒回归（RoVP）参数估计算法，解决SNLLS 问题
  2. 提出的RoVP算法能够对于线性和非线性参数之间解耦。
  3. 提出的VP方法消除线性参数时，可以减少算法在narrow valley上的停留。

# Interconnection-based model order reduction - a survey
## Significanse：
  1. 对于线性系统模型降阶方法做了概括：Hankel operator， proper orthogonal decomposition和rational interpolation。
  2. 对于非线性系统则总结了一些方法：Balancing and balanced approximation，Hankel-norm近似，正交分解（POD）
  3. 基于上述方法，针对线性和非线性以及Loewner提出了一种interconnection framework
  4. 
# Nonlinear system identification in coherence with nonlinearity measure for dynamic physical systems—case studies
## Significanse：
 1. 对于物理非线性系统的辨识，提出了
    - data-driven kSINDYc
    - Neural network-based NARX
    - parametric NL2SQ
 2.  对特定工作区域适用nonlinearity measure CANM来进行非线性度的测量。
    - CANM Convergence-area-based Nonlinearity Measure，量化非线性程度，即偏离其线性化近似的程度
 4.  对于非线性系统的辨识 适用一种nonlinearity level  $\varDelta_0$  产生最小均方误差。
 5.  对于nonlinear metrix非线性度量 CANM 在这篇文章得到了升级。

## Nonlinear metric- CANM Convergence-area-based Nonlinearity Measure：  $\varDelta_0$
- 在j工作点，真实输出和线性化近似输出的差值比值:  $\varDelta _{0j}=\frac{\left| \int_0^{t_f}{y_{True}dt} \right|-\left| \int_0^{t_f}{y_{lin}dt} \right|}{\left| \int_0^{t_f}{y_{True}dt} \right|}$  
- 所有工作点的非线性程度:  $\varDelta _{0nom}=\frac{\sum{\varDelta _{0P_j}}}{m}$  
- CANM依赖于工作点的非线性metric（度量）
- 初始值和激励输入会影响  $\varDelta_0$
- 本文基于SISO model进行仿真，对于stable unstable和marginally stable的  $\varDelta_0$  进行了更新
### for stable system
这样的稳定的系统存在settling time  $t_f$
### for marginally stable system
这样的系统特征根在虚轴上（中心流形）, 他们的响应通常是持续震荡的，所以寻找  $t_f$  变为寻找  $t_cycle$  ：  $\varDelta _{0_{margstable}=\frac{\left| \int_0^{t_{cycle}}{y_{True}dt} \right|-\left| \int_0^{t_{cycle}}{y_{lin}dt} \right|}{\left| \int_0^{t_{cycle}}{y_{True}dt} \right|}$
### for unstable system
nonlinear metric  $\varDelta_0$  变为分析他的输出轨迹，通过分成n个时间间隔  $(t_1, t_2,\cdots,t_x,\cdots,t_n)$  
对于每个时间间隔  $t_x$  和  $t_{x-1}$  得到  $\varDelta_{R_x}$  , 最后得到  $\varDelta _{0_unstable}=\frac{\sum{\varDelta _{0R_x}}}{n}$
### Nonlinearity level
<img width="418" height="85" alt="image" src="https://github.com/user-attachments/assets/9267f93e-1109-4d2c-8792-56f04ed75f53" />


