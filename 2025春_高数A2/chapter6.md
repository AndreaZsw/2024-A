---
 title: 高等数学讲义(下)
author: 胡煜成
description: 首都师范大学2025秋季学期高等数学A
"og:description": 浏览器版和手机版
"og:image": https://vlook-doc.pages.dev/pic/vlook-og.png
keywords:
- 高等数学,微积分,讲义
vlook-chp-autonum: h1{{第 ### 节 }},h3{{### }}
vlook-query: vdl=on
vlook-query: ws=off
---

[回到主页面](index.html)


# §12无穷级数

- 常数项级数
- 函数项级数

## 常数项级数的概念和性质

> [!tip]
>
> 例：手里的棒子有多长？
>$$
\begin{aligned}
& S_1=\frac{1}{2} \\
& S_2=\frac{1}{2}+\frac{1}{4}=\frac{3}{4} \\
& S_3=\frac{1}{2}+\frac{1}{4}+\frac{1}{8}=\frac{7}{8} \\
& \cdots \\
& S_n=\frac{1}{2}+\frac{1}{4}+\cdots+\frac{1}{2^n}=\frac{\frac{1}{2}\left(1-\left(\frac{1}{2}\right)^n\right)}{1-\frac{1}{2}}=1-\frac{1}{2^2} \\
& \lim _{n \rightarrow \infty} S_n=1
\end{aligned}
$$
>




> [!important]
>
> 定义: $\displaystyle a_n=\frac{1}{2^n}, ~ S_n=\sum_{i}^{\ n} a_n \quad n \rightarrow \infty$ ，称为$a_n$的无穷级数，简称级数。
>
>如果 $\left\{S_n\right\}$ 有极限， $\lim _{n \rightarrow \infty} S_n=S$ ，称级数收敛。

>[!tip]
>

解：需要补充过程。
>P253 例1. 计算等比数列
>$$
S_n=\sum_{i=2}^{\ n} a q^i, a \neq 0
>$$
>

>$q \neq 1 \quad S_n=\frac{a}{1-q}-\frac{a q^n}{1-q}$
>
>$|q|<1$ ,收敛
>
>$$
q=1 \quad \text { 较流 }
>$$
>$|q|>1$ 。发散
$q=-1 \quad$ 发散。

>p253．例2：$\displaystyle S_n=\sum_{i=1}^{\ n} i$, 发散

>P253．例3：
>$$
>\quad S_n=\frac{1}{1 \cdot 2}+\frac{1}{2 \cdot 3}+\cdots+\frac{1}{n(n+1)}$$
>$$
\begin{aligned}
& =\frac{1}{1}-\frac{1}{2}+\frac{1}{2}-\frac{1}{3}+\cdots+\frac{1}{n}-\frac{1}{n+1} \\
& =1-\frac{1}{n+1} \rightarrow 1 \quad \text { 收敛. }
\end{aligned}
>$$

>[!tip]
>通过计算题判断级数收敛——有时可行，有时不可行
>
>用别的办法（不计算）来判断收敛

>[!important](没有性质4？)
>
>性质1：$\quad \sum u_n=s . \quad \sum k u_n=k s.$
>
>性质2：已知$\sum u_n=s, \sum U_n=δ,有
\sum\left(u_n+v_n\right)=s+δ.
$
>
>性质3：改变级数有限项不影响收敛性.
>
>性质 5 :
>$$级数收敛 \displaystyle \Longrightarrow \lim _{n \rightarrow \infty} a_n \Rightarrow 0.$$
>
> $$例\quad \frac{1}{2}-\frac{2}{3}+\frac{3}{4}-\cdots+(-1)^{n-1} \frac{n}{n+1}$$
>
>
>$$\lim _{n \rightarrow \infty} a_n=0 \nRightarrow \text { 级数收敛. } $$
>
>$$
>例\ \ 1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}
>$$







## 审敛法
### 1.正项级数

>定理1：正项级数 $\displaystyle \sum_{n=1}^{\infty} u_n$ 收敛的充要条件是 $S_n$ 有界。
>
>单调有界有极限。

>定理2：$\sum u_n$ 和 $\sum v_n$ 都是正项级数，$u_n \leqslant v_n$
则 
>
>$$\sum  V_n收敛 \Rightarrow \sum  U_n收领$$
>$$
\sum u_n \text { 发散 } \Rightarrow \sum v_n \text { 发散. }
>$$


注:与前 $N$ 项无关

>$P 260$
>例2：$\sum \frac{1}{\sqrt{n(n+1)}}$

$\frac{1}{n+1}<\frac{1}{\sqrt{n(n+1)}}<\frac{1}{\sqrt{n n}}$


>[!impartant]
>
>定理3： $\lim _{n \rightarrow \infty} \frac{u_n}{v_n}=l$ ，$l>0$ ，则 $u_n \sim v_n$，即二者同收敛.


>[!tip]
>
>P261例3．$\sum_{n=1}^{\infty} \sin \frac{1}{n}$
>
>解：
>$$
\lim \frac{\sin \frac{1}{n}}{\frac{1}{n}}=1 . \quad \sum \sin \frac{1}{n} 发散
$$
>[!impartant]
>
>定理4．已知$\quad \lim _{n \rightarrow 0} \frac{u_{n+1}}{u_n}=ρ$
>$$
>\begin{array}{ll}
>ρ<1 . & \text { 收敌. } \\
>ρ>1 . & \text { 发散. } \\
>ρ=1 . & \text { 不确定.}
>\end{array}
>$$

>[!tips]
例4．$P263 . \quad 1+\frac{1}{1}+\frac{1}{1· 2}+\frac{1}{1·2·3}+\cdots+\frac{1}{(n-1)!}+\dots$
>
>$$
\lim _{n \rightarrow \infty} \frac{u_{n+1}}{u_n}=\lim _{n \rightarrow \infty} \frac{(n-1)!}{n!}=\lim _{n \rightarrow \infty} \frac{1}{n}=0 \quad \text {, 收敛. }
$$


>例5．$\quad \frac{1}{10}+\frac{1·2}{10^2}+\frac{1·2·3}{10^3}+\cdots+\frac{n!}{10^n}$
>$$
\lim _{n \rightarrow \infty} \frac{u_{n+1}}{u_n}=\lim _{n \rightarrow \infty} \frac{(n+1)}{10}=\infty \text {, 发散. }
$$
### 2．交错级数
>[!important]
>
>定理7莱布尼茨定理：对$\sum_{n=1}^{\infty}(-1)^{n-1} u_n$
>
>若 $ u_n \geqslant u_{n+1} . \quad \lim _{n \rightarrow \infty} u_n=0$,则级数收敛.

>例:
>
>
>$$
\begin{aligned}
& 1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots+(-1)^{n-1} \frac{1}{n}+\cdots \\
& u_n=\frac{1}{n}, \quad u_n>u_{n+1} \quad \lim _{n+1} u_n=0
\end{aligned}
$$


### 3. 绝收数与条件收敛
>绝对收敛： $\displaystyle \sum_{n=1}^{\infty}\left|u_n\right|$ 收敛
>
>条件收敛：  $\displaystyle \sum_{n=1}^{\infty} u_n$ 收敛
>
>$$
\text { 绝对收敛 } \Rightarrow \text { 条件收敛 }
$$
>[!tip]
>
>p268．例9．$\quad \sum \frac{\sin n \alpha}{n^2}$
>
>解：
>$$
因\sum\left|\frac{\sin \alpha}{n^2}\right| \leqslant \sum \frac{1}{n^2}, 故收敛
$$


[回到主页面](index.html)