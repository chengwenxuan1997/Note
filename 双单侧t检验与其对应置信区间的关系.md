# 双单侧t检验与其对应置信区间的关系

&emsp;**Bioequivalence Study in Drug Develpopment** (section 3.3.2.4) 中提到 **(Berger and Hsu,1996)**:
>&emsp;According to the **intersection-union principle** (Berger and Hsu, 1996), $H_0$ is rejected at significance level $\alpha$ in favor of $H_1$ if both hypotheses $H_{01}$ and $H_{02}$ are rejected at significance level $\alpha$:
$$T_{\delta_1}=\frac{\overline Y_T-\overline Y_R}{\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}>t_{1-\alpha,n_1+n_2-2}$$
$$T_{\delta_2}=\frac{\overline Y_T-\overline Y_R-\delta_2}{\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}<-t_{1-\alpha,n_1+n_2-2}$$
This is equivalent to
$$\overline Y_T-\overline Y_R-t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}>\delta_1$$
$$\overline Y_T-\overline Y_R+t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}<\delta_2$$
and hence to the inclusion of the two-sided $100(1-2\alpha)\%$ confidence interval for $\mu_T-\mu_R$ in the equivalence range:
$$\bigg[\overline Y_T-\overline Y_R-t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}},\overline Y_T-\overline Y_R+t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}\bigg]\subset(\delta_1,\delta_2)$$

&emsp;这是Berger和Hsu在1996年发表的论文：**Bioequivalence Trials ，Intersection-Union Tests and Equivalence Confidence Sets** (Berger and Hsu,1996)在section 5.2中，他们的叙述如下：
>We shall show that the usual $100(1-2\alpha)\%$confidence interval $[D-t_{\alpha,r}SE(D),D+t_{\alpha,r}SE(D)]$ results in a size-$\alpha$ TOST of $H_1:\theta_L<\eta_T-\eta_R<\theta_U$ because $[D-t_{\alpha,r}SE(D),D+t_{\alpha,r}SE(D)]$ is **equal-tailed**. So the relationship is deeper than the "algebraic coincidence".

令$[C^-,C^+]$代表$[D-t_{\alpha,r}SE(D),D+t_{\alpha,r}SE(D)]$，$(-\infty,C^+]$和$[C^-,\infty]$分别是TOST中的两个单侧$t$检验所对应的$(1-\alpha)\%$水平的置信区间。两个单侧$(1-\alpha)\%$的置信区间的交集$[C^-,C^+]$是一个$100(1-2\alpha)\%$的置信区间
>**Statistical Inference**(Casella and Berger) 1990 exercise 9.1 ：
&emsp;Let the data $\pmb X$ have a probability distribution that depends on a real-valued parameter $\theta$. Suppose $(-\infty,U(\pmb X)]$ is a $100(1-\alpha_1)\%$ upper confidence bound for $\theta$. Suppose $[L(\pmb X,\infty))$ is a $100(1-\alpha_2)\%$ lower confidence bound for $\theta$. Then $[L(\pmb X),U(\pmb X)]$ is a $100(1-\alpha_1-\alpha_2)\%$ confidence interval for $\theta$.
**proof**:$P(A\cap B)=P(A)+P(B)-P(A\cup B)$
"it is not so important that $[C^-,C^+]$ is a $100(1-2\alpha)\%$ confidence interval for $\theta$. **Rather, it is the fact that $(-\infty,C^+]$ and $[C^-,\infty]$ are both $100(1-\alpha_1)\%$ confidence intervals that yields a level-$\theta$ test. That is, it is important that $[C^-,C^+]$ is an equal-tailed confidence interval.**"

当$[C^-,C^+]$不是等尾区间时：令$[C_1^-,C_1^+]$为$[D-t_{\alpha_2,r}SE(D),D+t_{\alpha_1,r}SE(D)],\quad\alpha_1+\alpha_2=2\alpha$
只有当置信区间$[C_1^-,C_1^+]\subset(\theta_L,\theta_U)$有$max\{\alpha_1,\alpha_2\}$的水平时，双单侧$t$检验才会拒绝$H_0$，此时双单侧$t$检验与置信区间不一致。

$H_0$
$\alpha$
$H_1$
$H_{01}$
$H_{02}$
$$T_{\delta_1}=\frac{\overline Y_T-\overline Y_R}{\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}>t_{1-\alpha,n_1+n_2-2}$$
$$T_{\delta_2}=\frac{\overline Y_T-\overline Y_R-\delta_2}{\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}<-t_{1-\alpha,n_1+n_2-2}$$
$$\overline Y_T-\overline Y_R-t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}>\delta_1$$
$$\overline Y_T-\overline Y_R+t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}<\delta_2$$
$$\bigg[\overline Y_T-\overline Y_R-t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}},\overline Y_T-\overline Y_R+t_{1-\alpha,n_1+n_2-2}\hat\sigma\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}\bigg]\subset(\delta_1,\delta_2)$$
$\pmb X$
$\theta$
$(-\infty,U(\pmb X)]$
$100(1-\alpha_1)\%$
$[L(\pmb X,\infty))$
$100(1-\alpha_2)\%$
$[L(\pmb X),U(\pmb X)]$
$100(1-\alpha_1-\alpha_2)\%$
$100(1-2\alpha)\%$
$[C^-,C^+]$
$\theta=\eta_T-\eta_R$
$(-\infty,C^+]$
$C^+ <\theta_U$
$C^- >\theta_L$
$(-\infty,C^+]$
$[C^-,\infty]$
$[C_1^-,C_1^+]$
$$[D-t_{\alpha_2,r}SE(D),D+t_{\alpha_1,r}SE(D)$$
$\alpha_1+\alpha_2=2\alpha$
$(-\infty,C_1^+]$
$H_{02}$
$\alpha_1$
$[C_1^-,\infty]$
$H_{01}$
$\alpha_2$
$[C_1^-,C_1^+]\subset(\theta_L,\theta_U)$
$max\{\alpha_1,\alpha_2\}$
