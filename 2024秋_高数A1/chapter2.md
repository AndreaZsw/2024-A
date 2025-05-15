---
title: 高等数学讲义(上)
author: 胡煜成
description: 首都师范大学2024秋季学期高等数学A
"og:description": 浏览器版和手机版
"og:image": https://vlook-doc.pages.dev/pic/vlook-og.png
keywords:
- 高等数学,微积分,讲义
vlook-chp-autonum: h1{{第 ### 节 }},h3{{### }}
vlook-query: vdl=on
vlook-query: ws=off
---

[回到主页面](index.html)


> [!tip]
> 
> ---
> 
> > ==导数是一种特殊的极限==
> > 
> > 实际问题中人们经常会考虑某个函数的**极值**, 函数的**切线方向**是分析函数极值的有力工具: 
> > 
> > - 切线斜率为正时函数单调递增
> > - 切线斜率为负时函数单调递减
> > - 切线斜率为零时函数取到极值
> > 
> > 那么怎么求函数在某处**切线的斜率**呢? 这个问题困扰了数学家好多年, 直到后来有人发现**切线斜率可以看作是一个极限**, 这个极限也叫做**导数**.
> > 
> > 由此我们也可以进一步体会到**极限**的重要性. 而在后面的章节中, 我们会再次运用**极限**来构造**积分**. 因此极限的概念相当于整个微积分的基础. 
> > 
> > 右图给出了课本各部分内容之间的关系.
> 
> > ==思维导图==
> > 
> > ![微积分思维导图](media/img/chpt2_derivative.png#400h)

# 导数和导函数

> [!tip]
>
> - 导数是函数的**瞬时变化率**.
> - 导数是函数某处的**切线斜率**.
> 
> ---
> > [!note]
> > 
> > ==**导数**是研究函数性质的重要工具==
> > 
> > **问题**: 计算 $\displaystyle f(x) = \sin(x) - \frac{2x}{\pi}$ 的最大值.
> > 
> > **求解**: 如图所示, 
> > $f(0) = 0$ ... [补充解法]
> 
> > [补充函数图像]

## 导数的定义

> [!important]
>
> ---
> > ==导数的定义==
> >
> > $$
> > f'(x_0) = \lim_{\Delta x \rightarrow 0}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} = \lim_{\Delta x \rightarrow 0}\frac{\Delta y}{\Delta x}.
> > $$
>
> > [导数的几何意义: 图]
> > 
> > ![导数的几何意义](media/img/derivative.jpg)
> > 
>


> [!note]
> 
> ==由定义计算导数==
> 
> ---
> 
> > ==例1==
> > 
> > **求 $f(x) = C$ 在 $x_0=1$ 处的导数.**
> >
> > 解：根据导数的定义：$$
f'(x_0) = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} = \lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x}$$
代入 \( f(x) = C \) 和 \( x_0 = 1 \)：
$$
f'(1) = \lim_{\Delta x \to 0} \frac{f(1 + \Delta x) - f(1)}{\Delta x}= \lim_{\Delta x \to 0} \frac{C - C}{\Delta x} = \lim_{\Delta x \to 0} \frac{0}{\Delta x} = \lim_{\Delta x \to 0} 0 = 0$$
答案为：\( f'(1) = {0} \)
> 
> > ==例2==
> > 
> > **求 $f(x) = x^2$ 在 $x_0=2$ 处的导数.**
> > 
> >解：根据导数的定义：
$$
f'(x_0) = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} = \lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x}
$$
代入 \( f(x) = x^2 \) 和 \( x_0 = 2 \)：
$$
f'(2) = \lim_{\Delta x \to 0} \frac{(2 + \Delta x)^2 - 2^2}{\Delta x} = \lim_{\Delta x \to 0} \frac{4 + 4\Delta x + (\Delta x)^2 - 4}{\Delta x} 
$$
化简分子并求极限：
$$
f'(2) = \lim_{\Delta x \to 0} \frac{4\Delta x + (\Delta x)^2}{\Delta x} = \lim_{\Delta x \to 0} \frac{\Delta x(4 + \Delta x)}{\Delta x} = \lim_{\Delta x \to 0} (4 + \Delta x) = 4 + 0 = 4
$$
答案为\( f'(2) = {4} \)


## 导函数

> [!tip]
> 
> 对函数 $f(x)$ 定义域上的每一点都求导 (假设每一点的导数都存在), 得到一个**新的**_~Rd~_函数, 称为**导函数**, 记作 $f'(x)$. 可知导函数是由 $f(x)$ 衍生出来的, 正好和 Derivative (导数) 的意思一致.
> 

> [!warning]
> 
> 给定位移关于时间的函数 $s(t)$, 物体的速度 $v(t)$ 便是 $s(t)$ 的导数.
> 

> [!note]
> 
> ---
> 
> > ==例3==
> > 
> > **求 $f(x) = x^2$ 的导函数.**
> > 
> > 解：函数 \( f(x) = x^2 \) 的导数推导如下：\[f'(x) = \lim_{\Delta x \to 0} \frac{f(x+\Delta x) - f(x)}{\Delta x} = \lim_{\Delta x\to 0} \frac{(x+\Delta x)^2 - x^2}{\Delta x}\]
> > \[ =\lim_{\Delta x \to 0} \frac{x^2 + 2x\Delta x + \Delta x^2- x^2}{\Delta x} =\lim_{\Delta x \to 0} \frac{2x\Delta x + \Delta x^2}{\Delta x}\]
> >此时极限表达式变为：
   \[f'(x) = \lim_{\Delta x \to 0} (2x + \Delta x)= 2x\]
> 
> > ==例4(P78例4)==
> > 
> > **求函数 \( f(x) = \cos x \) 的导数.**
> 
> > **方法一**
> > 解：由导数的定义：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{\cos(x + \Delta x) - \cos x}{\Delta x}\]
> > 利用三角恒等式：\[\cos A - \cos B = -2 \sin\left( \frac{A + B}{2} \right) \sin\left( \frac{A - B}{2} \right)\]
> > 得到：\[\cos(x + \Delta x) - \cos x = -2 \sin\left( x + \frac{\Delta x}{2} \right) \sin\left( \frac{\Delta x}{2} \right)\]
   代入导数定义：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{-2 \sin\left( x + \frac{\Delta x}{2} \right) \sin\left( \frac{\Delta x}{2} \right)}{\Delta x}\]
> >拆分极限：
   \[f'(x) = -2 \lim_{\Delta x \to 0} \sin\left( x + \frac{\Delta x}{2} \right) \cdot \lim_{\Delta x \to 0} \frac{\sin\left( \frac{\Delta x}{2} \right)}{\Delta x}\]
> > - 第一个极限：
     \[\lim_{\Delta x \to 0} \sin\left( x + \frac{\Delta x}{2} \right) = \sin x\]
> > - 第二个极限（令 \( t = \frac{\Delta x}{2} \)）：
     \[\lim_{\Delta x \to 0} \frac{\sin\left( \frac{\Delta x}{2} \right)}{\Delta x} = \lim_{t \to 0} \frac{\sin t}{2t} = \frac{1}{2} \cdot 1 = \frac{1}{2}\]
> >合并结果：
   \[f'(x) = (\cos x)' =-2 \cdot \sin x \cdot \frac{1}{2} = -\sin x\]
>
>
> > **方法二**
> >解：
> >由导数的定义：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{\cos(x + \Delta x) - \cos x}{\Delta x}\]
   展开 \( \cos(x + \Delta x) \)并带入：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{\cos x \cos \Delta x - \sin x \sin \Delta x - \cos x}{\Delta x}\]
> >拆分分子并化简：
   \[f'(x) = \lim_{\Delta x \to 0} \left[ \cos x \cdot \frac{\cos \Delta x - 1}{\Delta x} - \sin x \cdot \frac{\sin \Delta x}{\Delta x} \right]\]
> > 计算关键极限：
> > - 已知极限：  
     \[\lim_{\Delta x \to 0} \frac{\sin \Delta x}{\Delta x} = 1\]
> >
> >- 计算 \(\frac{\cos \Delta x - 1}{\Delta x}\)：
利用三角恒等式 \( \cos \Delta x - 1 = -2\sin^2\left(\frac{\Delta x}{2}\right) \)：
   \[\frac{\cos \Delta x - 1}{\Delta x} = -2 \cdot \frac{\sin^2\left(\frac{\Delta x}{2}\right)}{\Delta x} = -\frac{\sin\left(\frac{\Delta x}{2}\right)}{\frac{\Delta x}{2}} \cdot \sin\left(\frac{\Delta x}{2}\right)\]
   令 \( t = \frac{\Delta x}{2} \)，当 \( \Delta x \to 0 \) 时 \( t \to 0 \)，则：
   \[\lim_{\Delta x \to 0} \frac{\cos \Delta x - 1}{\Delta x} = -\lim_{t \to 0} \left( \frac{\sin t}{t} \cdot \sin t \right) = -1 \cdot 0 = 0\]
> >合并结果：
   \[f'(x) = (\cos x)' =-2 \cdot \sin x \cdot \frac{1}{2} = -\sin x\]     
> 
> >用类似的方法可以求得 $\sin x$ 的导数
> >即：$$(\sin x)' = \cos x$$



> [!note]
>
> ---
>
> > ==例5(P77例2)== 
>>
> >**求正整数次幂函数 \( f(x) = x^m \) 的导数.**
> >
> >解：当 \( m = 1 \) 时：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{(x+\Delta x) - x}{\Delta x} = \lim_{\Delta x \to 0} \frac{\Delta x}{\Delta x} = 1\]
> >当 \( m > 1 \) 时：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{(x+\Delta x)^m - x^m}{\Delta x}\]
   展开多项式：
   \[(x+\Delta x)^m = x^m + m x^{m-1} \Delta x + \frac{m(m-1)}{2} x^{m-2} (\Delta x)^2 + \cdots + (\Delta x)^m\]
   代入后化简：
   \[
   f'(x) = \lim_{\Delta x \to 0} \left[ m x^{m-1} + \frac{m(m-1)}{2} x^{m-2} \Delta x + \cdots + (\Delta x)^{m-1} \right] = m x^{m-1}
   \]
>>最终结果为：  
\[(x^m)' = 
\begin{cases} 
1, & m = 1, \\
m x^{m-1}, & m > 1.
\end{cases}\]
>
>
>> ==例6(P77例3)== 
>>
>>**求函数 \( f(x) = x^\alpha \) 的导数.  (\(\alpha\in\mathbb{R} \))**
>>
>>解：由导数的定义：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{(x+\Delta x)^\alpha - x^\alpha}{\Delta x}\]
>>
>> 提取公共因子：
   \[\frac{(x+\Delta x)^\alpha - x^\alpha}{\Delta x} = x^{\alpha-1} \cdot \frac{\left( 1 + \frac{\Delta x}{x} \right)^\alpha - 1}{\frac{\Delta x}{x}}\]
>>
>>变量代换：  
   令 \( t = \frac{\Delta x}{x} \)，则当 \( \Delta x \to 0 \) 时 \( t \to 0 \)，极限转化为：\[
   f'(x) = x^{\alpha-1} \cdot \lim_{t \to 0} \frac{(1 + t)^\alpha - 1}{t}\]
>>  
>>利用幂函数展开式 \( (1 + t)^\alpha \approx 1 + \alpha t \)(当 \( t \to 0 \))：
   \[\lim_{t \to 0} \frac{(1 + \alpha t) - 1}{t} = \alpha\]
>>
>>结果为：
   \[f'(x) = \alpha x^{\alpha-1}\]



> [!note]
> 
> ---
> 
> > ==例7(P78例5)== 
> >
>>**给定函数 \( f(x) = q^x \)，其中底数 \( q \) 是大于 0 且不等于 1 的常数，求导函数 \( f'(x) \)**
>>
>>解：由导数定义：
\[f'(x) = \lim_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x}\]
>>
>>代入函数 \( f(x) = q^x \) 得：
>>\[f'(x) = \lim_{\Delta x \to 0} \frac{q^{x + \Delta x} - q^x}{\Delta x}
= \lim_{\Delta x \to 0} \frac{q^x \cdot q^{\Delta x} - q^x}{\Delta x}= q^x \cdot \lim_{\Delta x \to 0} \frac{q^{\Delta x} - 1}{\Delta x}\]
>>
>>根据极限性质，有：
>>\[\lim_{\Delta x \to 0} \frac{q^{\Delta x} - 1}{\Delta x} = \ln q\]
>>因此，$f'(x) = q^x \cdot \ln q$
>>这就是指数函数的导数公式。当 $ u = e $ 时，因 $ \ln e = 1 $，故有：$(e^x)' = e^x$
>
>---
>
>
> > ==例8(P79例6)== 
>>
>>**求对数函数 \( f(x) = \log_u x \) 的导数, 其中$u$是大于0且不等于1的常数.**
>>
>>解：由导数的定义：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{\log_u (x + \Delta x) - \log_u x}{\Delta x}\]
>>
>>应用对数性质：
   利用换底公式 \( \log_u a = \frac{\ln a}{\ln u} \)，将分子转换为自然对数：
   \[f'(x) = \lim_{\Delta x \to 0} \frac{\frac{\ln(x + \Delta x)}{\ln u} - \frac{\ln x}{\ln u}}{\Delta x} = \frac{1}{\ln u} \cdot \lim_{\Delta x \to 0} \frac{\ln\left(1 + \frac{\Delta x}{x}\right)}{\Delta x}\]
>>
>>变量代换：  
   令 \( h = \frac{\Delta x}{x} \)，当 \( \Delta x \to 0 \) 时 \( h \to 0 \)，则：
   \[f'(x) = \frac{1}{\ln u} \cdot \lim_{h \to 0} \frac{\ln(1 + h)}{x \cdot h} = \frac{1}{x \ln u} \cdot \lim_{h \to 0} \frac{\ln(1 + h)}{h}\]
>>
>>关键极限：  
$$\lim_{h \to 0} \frac{\ln(1 + h)}{h} = \lim_{h \to 0} \ln\ (1 + h)^{\frac{1}{h}}  = \ln\left( \lim_{h \to 0} (1 + h)^{\frac{1}{h}} \right) = \ln e = 1$$
>>
>>结果为：
   \[f'(x) = \frac{1}{x \ln u} \cdot 1 = \frac{1}{x \ln u}\]



> [!caution]
> 
> ==连续与可导的关系==
> 
> 可导必连续, 连续不一定可导. 
> 

> [!note]
> 
> ---
> 
> > ==反例1==
> > 
> > **$f(x) = |x|$**
>>
>> - 连续：绝对值函数在 \( x = 0 \) 处是连续的，因为：
$\displaystyle \lim_{x \to 0^-} |x| = 0, \quad \lim_{x \to 0^+} |x| = 0, \quad f(0) = 0.$
>>
>> - 可导性：\( f(x) = |x| \) 在 \( x=0 \) 处的导数
>>由导数的定义：
>>$f'(0) = \displaystyle \lim_{\Delta x \to 0} \frac{f(0+\Delta x)-f(0)}{\Delta x} = \lim_{\Delta x \to 0} \frac{|\Delta x| - 0}{\Delta x} = \lim_{\Delta x \to 0} \frac{|\Delta x|}{\Delta x}$
>>当 \( \Delta x < 0 \) 时：  
   \[\frac{|\Delta x|}{\Delta x} = \frac{-\Delta x}{\Delta x} = -1 \quad \Rightarrow \quad \lim_{\Delta x \to 0^-} \frac{|\Delta x|}{\Delta x} = -1\]
>>当 \( \Delta x > 0 \) 时：  
   \[\frac{|\Delta x|}{\Delta x} = \frac{\Delta x}{\Delta x} = 1 \quad \Rightarrow \quad \lim_{\Delta x \to 0^+} \frac{|\Delta x|}{\Delta x} = 1\]
>>由于左极限 (\(-1\)) 与右极限 (\(1\)) 不相等，故极限: $\displaystyle \lim_{\Delta x \to 0} \frac{|\Delta x|}{\Delta x}$
**不存在**。因此，函数 \( f(x) = |x| \) 在 \( x=0 \) 处**不可导**。
>>
>> **故连续不一定可导**
>
>>
> 
> > ==反例2==
> > 
> > **$f(x) = x^{\frac{1}{3}}$**
>> - 连续性：立方根函数在所有实数点（包括 \( x = 0 \)）都是连续的，因为：$\displaystyle \lim_{x \to 0} x^{\frac{1}{3}} = 0 = f(0).$
>> - 可导性  
计算$f(x)$的导数：$f'(x) = \frac{1}{3} x^{-\frac{2}{3}} \quad (x \neq 0).$
当 \( x \to 0 \) 时，\( f'(x) \to \infty \)，即导数在 \( x = 0 \) 处**不存在**（无穷大导数）。
>>
>>**故连续不一定可导**
>>
>>

> [!caution]
> 
> ==单侧导数==
>
>根据函数 \( f(x) \) 在点 \( x_0 \) 处的导数 \( f'(x_0) \) 的定义，导数  
$$
f'(x_0) = \lim_{\Delta x  \to 0} \frac{f(x_0 + \Delta x ) - f(x_0)}{\Delta x }
$$  
是一个极限，而极限存在的充分必要条件是左、右极限都存在且相等。因此，\( f'(x_0) \) 存在（即 \( f(x) \) 在点 \( x_0 \) 处可导）的充分必要条件是左、右极限  
$$
\lim_{\Delta x  \to 0^-} \frac{f(x_0 + \Delta x ) - f(x_0)}{\Delta x } \quad \text{及} \quad \lim_{\Delta x \to 0^+} \frac{f(x_0 + \Delta x ) - f(x_0)}{\Delta x }
$$  
都存在且相等。
>
> - **左导数与右导数的定义**
这两个极限分别称为函数 \( f(x) \) 在点 \( x_0 \) 处的**左导数**和**右导数**，记作 \( f'_-(x_0) \) 及 \( f'_+(x_0) \)，即  
$$
f'_-(x_0) = \lim_{\Delta x  \to 0^-} \frac{f(x_0 + \Delta x ) - f(x_0)}{\Delta x },
$$  
$$
f'_+(x_0) = \lim_{\Delta x  \to 0^+} \frac{f(x_0 + \Delta x ) - f(x_0)}{\Delta x }.
$$
>
> - **可导的充要条件**：  
函数 \( f(x) \) 在点 \( x_0 \) 处可导的充分必要条件是左导数 \( f'_-(x_0) \) 和右导数 \( f'_+(x_0) \) 都存在且相等。
>
> - **左导数和右导数统称为单侧导数**。  
> - **闭区间上的可导性**：  
  如果函数 $ f(x) $  在开区间 \( (a, b) \) 内可导, 左端点右导数 \( f'_+(a) \) 和右端点左导数 \( f'_-(b) \) 均存在, 则称 \( f(x) \) 在闭区间 \( [a, b] \) 上**可导**


# 导数的计算

## 初等函数的导数
> [!tip]
> 
> 首先我们给出初等函数的导数公式.
> 

> [!important]
> 
> ==常见初等函数的求导公式==
> 1. 幂函数
> - 如果 $f(x) = x^n$，则：
> $$f'(x) = n \cdot x^{n-1}$$
> 
> 2. 指数函数
> - 如果 $f(x) = e^x$，则：
> $$f'(x) = e^x$$
> 
> - 如果 $f(x) = a^x$，则：
> $$f'(x) = a^x \ln(a)$$
> 
> 3. 对数函数
> - 如果 $f(x) = \ln(x)$，则：
> $$f'(x) = \frac{1}{x}$$
> 
> - 如果 $f(x) = \log_a(x)$，则：
> $$f'(x) = \frac{1}{x \ln(a)}$$
> 
> 4. 三角函数
> - 如果 $f(x) = \sin(x)$，则：
> $$f'(x) = \cos(x)$$
> 
> - 如果 $f(x) = \cos(x)$，则：
> $$f'(x) = -\sin(x)$$
> 
> - 如果 $f(x) = \tan(x)$，则：
> $$f'(x) = \sec^2(x)$$
> 
> 5. 反三角函数
> - 如果 $f(x) = \arcsin(x)$，则：
> $$f'(x) = \frac{1}{\sqrt{1 - x^2}}$$
> 
> - 如果 $f(x) = \arccos(x)$，则：
> $$f'(x) = \frac{-1}{\sqrt{1 - x^2}}$$
> 
> - 如果 $f(x) = \arctan(x)$，则：
> $$f'(x) = \frac{1}{1 + x^2}$$

## 导数的四则运算

> [!tip]
> 
> 下面的导数四则法则能够方便我们计算导数. 这些法则都可以根据导数的定义加以证明.
> 

> [!important]
> 
> ==导数的四则运算法则==
> 
> **1. 和差法则（Sum and Difference Rules）**
> 若函数 $f(x)$ 和 $g(x)$ 在点 $x$ 处可导，则：
> $$
> \frac{d}{dx}[f(x) \pm g(x)] = f'(x) \pm g'(x)
> $$
> **证明：**
> 根据导数的定义：
> $$
> \frac{d}{dx}[f(x) \pm g(x)] = \lim_{h \to 0} \frac{[f(x+h) \pm g(x+h)] - [f(x) \pm g(x)]}{h}
> $$
> 分拆后：
> $$
> = \lim_{h \to 0} \left( \frac{f(x+h) - f(x)}{h} \pm \frac{g(x+h) - g(x)}{h} \right)
> $$
> 利用极限的线性性质：
> $$
> = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} \pm \lim_{h \to 0} \frac{g(x+h) - g(x)}{h}
> $$
> 所以：
> $$
> \frac{d}{dx}[f(x) \pm g(x)] = f'(x) \pm g'(x)
> $$
>
> **2. 乘积法则（Product Rule）**
> 若函数 $f(x)$ 和 $g(x)$ 在点 $x$ 处可导，则：
> $$
> \frac{d}{dx}[f(x) \cdot g(x)] = f'(x)g(x) + f(x)g'(x)
> $$
> **证明：**
> 根据导数的定义：
> $$
> \frac{d}{dx}[f(x)g(x)] = \lim_{h \to 0} \frac{f(x+h)g(x+h) - f(x)g(x)}{h}
> $$
> 加减 $f(x+h)g(x)$ 项：
> $$
> = \lim_{h \to 0} \frac{[f(x+h)g(x+h) - f(x+h)g(x)] + [f(x+h)g(x) - f(x)g(x)]}{h}
> $$
> 拆分并整理：
> $$
> = \lim_{h \to 0} \left( f(x+h) \frac{g(x+h) - g(x)}{h} + g(x) \frac{f(x+h) - f(x)}{h} \right)
> $$
> 当 $h \to 0$ 时，$f(x+h) \to f(x)$：
> $$
> = f(x) \cdot g'(x) + g(x) \cdot f'(x)
> $$
> 因此：
> $$
> \frac{d}{dx}[f(x)g(x)] = f'(x)g(x) + f(x)g'(x)
> $$
>
> **3. 商法则（Quotient Rule）**
> 若函数 $f(x)$ 和 $g(x)$ 在点 $x$ 处可导，且 $g(x) \ne 0$，则：
> $$
> \frac{d}{dx}\left[ \frac{f(x)}{g(x)} \right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}
> $$
> **证明：**
> 根据导数的定义：
> $$
> \frac{d}{dx}\left[ \frac{f(x)}{g(x)} \right] = \lim_{h \to 0} \frac{\frac{f(x+h)}{g(x+h)} - \frac{f(x)}{g(x)}}{h}
> $$
> 通分并整理：
> $$
> = \lim_{h \to 0} \frac{[f(x+h)g(x) - f(x)g(x+h)]}{h \cdot g(x)g(x+h)}
> $$
> 分拆分子：
> $$
> = \lim_{h \to 0} \left( \frac{f(x+h) - f(x)}{h} \cdot \frac{g(x)}{g(x)g(x+h)} - \frac{g(x+h) - g(x)}{h} \cdot \frac{f(x)}{g(x)g(x+h)} \right)
> $$
> 当 $h \to 0$ 时，$g(x+h) \to g(x)$：
> $$
> = \frac{f'(x)g(x)}{[g(x)]^2} - \frac{f(x)g'(x)}{[g(x)]^2}
> $$
> 因此：
> $$
> \frac{d}{dx}\left[ \frac{f(x)}{g(x)} \right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}
> $$

> [!note]
> 
>>==P86 例1== 
>>
>>**求函数 \( y = 3x^3 - 4x^2 + 5x - 9 \) 的导数 \( y' \).**
>>
>>$\begin{aligned}
>>解：y' &= (3x^3 - 4x^2 + 5x - 9)' \\
&= (3x^3)' - (4x^2)' + (5x)' - (9)' \quad  \\
&= 3 \cdot 3x^{3-1} - 4 \cdot 2x^{2-1} + 5 \cdot 1x^{1-1} - 0 \quad \\
&= 9x^2 - 8x + 5 \quad 
\end{aligned}$
> 
> 
> ==P86 例2==
>>
>>**设 $y = 2e^{x}(\sin x + 2\cos x)$，求 $y'$**
>>
>>$\begin{aligned}
解：y' &= (2e^{x})'(\sin x + 2\cos x) + 2e^{x}(\sin x + 2\cos x)' \\
&= 2e^{x}(\sin x + 2\cos x) + 2e^{x}(\cos x - 2\sin x) \\
&= 2e^{x}\sin x + 4e^{x}\cos x + 2e^{x}\cos x - 4e^{x}\sin x \\
&= 6e^{x}\cos x - 2e^{x}\sin x \\
&= 2e^{x}(3\cos x - \sin x)
\end{aligned}$
>
> ==P86 例3==
>>**求函数 \( f(x) = x^3 + 3\sin x + \frac{5}{2} \) 的导数 \( f'(x) \) 及 \( f'\left(\frac{\pi}{4}\right) \)**
>>
>>$\begin{aligned}
   解：f'(x) &= \left( x^3 + 3\sin x + \frac{5}{2} \right)' \\
   &= (x^3)' + (3\sin x)' + \left( \frac{5}{2} \right)' \quad \\
   &= 3x^2 + 3\cos x + 0 \quad \\
   &= 3x^2 + 3\cos x.
   \end{aligned}$
>>
>> $\begin{aligned}\ \ \ \ \ \ \ 
   f'\left( \frac{\pi}{4} \right) &= 3\left( \frac{\pi}{4} \right)^2 + 3\cos\left( \frac{\pi}{4} \right) \\
   &= 3 \cdot \frac{\pi^2}{16} + 3 \cdot \frac{\sqrt{2}}{2} \quad \\
   &= \frac{3\pi^2}{16} + \frac{3\sqrt{2}}{2}.
   \end{aligned}$
>
>
> ==P86 例4==
>>
>>**设 $y = \tan x$，求 $y$ 的导数 $y'$**
>>
>>解：\( y' = (\tan x)' = \left( \frac{\sin x}{\cos x} \right)' = \frac{(\sin x)' \cos x - \sin x (\cos x)'}{\cos^2 x} \)
>>
>>\[= \frac{\cos^2 x + \sin^2 x}{\cos^2 x} = \frac{1}{\cos^2 x} = \sec^2 x,\]
>>
>
>>
> ==P87 例5==
>>
>> **设 $y = \cot x $，求 $ y' $**
>>
>>解：$ y' = (\cot x)' = \left( \frac{\cos x}{\sin x} \right)' = \frac{(\cos x)' \sin x - \cos x (\sin x)'}{\sin^2 x} $
\[= \frac{(-\sin x) \sin x - \cos x (\cos x)}{\sin^2 x} = \frac{-\sin^2 x - \cos^2 x}{\sin^2 x}\]

\[= \frac{-(\sin^2 x + \cos^2 x)}{\sin^2 x} = \frac{-1}{\sin^2 x} = -\csc^2 x,\]

即

\[(\cot x)' = -\csc^2 x.\]
>>


## 复合函数求导的链式法则
> [!tip]
> 
> 非常重要!
> 

> [!important]
> 
> ==链式法则 (Chain Rule)==
> 若函数 $y = f(u)$ 在点 $u = g(x)$ 可导，且 $u = g(x)$ 在点 $x$ 可导，则：
> $$
> \frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
> $$
> **证明：**
> 根据导数的定义：
> $$
> \frac{dy}{dx} = \lim_{h \to 0} \frac{f(g(x+h)) - f(g(x))}{h}
> $$
> 添加并减去 $f(g(x) + [g(x+h) - g(x)])$：
> $$
> = \lim_{h \to 0} \frac{f(g(x) + \Delta u) - f(g(x))}{\Delta u} \cdot \frac{\Delta u}{h}
> $$
> 其中 $\Delta u = g(x+h) - g(x)$。当 $h \to 0$，$\Delta u \to 0$：
> $$
> = \frac{df}{du} \cdot \frac{dg}{dx}
> $$
> 因此：
> $$
> \frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
> $$


> [!note]
> 
> ==P90 例9== 
> 
> ==P90 例10==
> 
> ==P91 例11==
> 
> ==P92 例12==
> 
> ==P92 例13==
> 
> ==P92 例14==
> 
> ==P93 例15==


# 隐函数的导数

## 隐函数求导

> [!tip]
> 
> 隐函数将自变量 $x$ 和函数值 $y$ 通过某个等式联系起来, 从这个等式里我们可以推测 $\Delta y$ 和 $\Delta x$ 之间的关系, 一些复杂的函数的导数通过隐函数更容易计算.
> 

> [!note]
> 
> ==P101 例1==
>
> ==P102 例2==
> 
> ==P102 例3==
> 

## 反函数求导

> [!tip]
> 
> $y = f(x)$ 的导数是看 $\Delta y$ 随 $\Delta x$ 的变化率, 其反函数 $x = f(y)$ 的导数是看 $\Delta x$ 随 $\Delta y$ 的变化率, 而的 $\Delta x$ 与 $\Delta y$ 之间的关系可以通过隐函数确定.
> 

> [!note]
> 
> ==P88 例6==
> [不要用书上的做法, 用隐函数求导]
> 
> ==P88 例7==
> [不要用书上的做法, 用隐函数求导]

> [!note]
> 
> ==P103 例5==
> 
> ==P103 例6==

# 高阶导数
> [!tip]
> 
> 导函数也是函数, 所以可以继续对导函数求导, 也就是二阶导数. 二阶导数反应了导函数的变化率. 依次可以继续到三阶导数, 四阶导数, ...
> 

> [!caution]
> 
> ==二阶导数==
> 
> $f''(x) = (f'(x))'$
>
> ==常用记号==
> 
> - $f'(x)$, $f''(x)$, $f'''(x)$, $f^{(n)}(x)$, $\cdots$.
> - $\displaystyle \frac{d}{dx}f(x)$, $\displaystyle \frac{d^2}{dx^2}f(x)$, $\displaystyle \frac{d^3}{dx^3}f(x)$, $\displaystyle \frac{d^{n}}{dx^{n}}f(x)$, $\cdots$.
> 

> [!note]
> 
> ==P97 例1==
> 
> ==P97 例2==
> 
> ==P97 例4==
> 
> ==P98 例7==
> 
> ==P103 例4==

> [!warning]
> 
> ==位移, 速度和加速度==
> 
> 高阶导数一个重要的作用就是用来描述**加速度**.
> 
> [看视频]

# 利用导数来研究函数的性质

> [!tip]
> 
> 导数可以用来研究**函数的变化率**, 仅仅这一条已经很强大了, 下面的应用都源自于导数的这一功能.

## 单调性

> [!caution]
> 
> - 导数>0, 单调递增
> - 导数<0, 单调递减
> - 导数=0, 无法判断
>

> [!note]
> 
> ---
> 
> > ==P145 例1==
> > 
>
> > ==P145 例2==
> > 

## 极值

> [!caution]
> 
> - 导数=0, 二阶导数>0, 极小
> - 导数=0, 二阶导数<0, 极大
> - 导数=0, 二阶导数=0, 无法判断. 导数为0的点也称为**驻点**或**临界点**.
> 

> [!note]
> 
> ==P156 例2==
> 

> [!caution]
> 
> ==极值和最值==
> 

> [!warning]
> 
> ==光路最短原理==
> 
> 光路最短原理（也称为费马原理，Fermat's Principle）是光的传播路径遵循的基本规律。它指出：光在两点之间传播时，所走的路径是光程最短的路径。光程是指光在线路中传播所需的时间，与路径的几何长度和介质的折射率有关。
> 
> 下面我们来看折射现象如何通过光路最短原理来解释.
> 
> **P158 例5**

## 凸性

> [!important]
> 
> ==凸函数的定义==
>
> 设 $f(x)$ 是定义在实数集上的函数。如果对于定义域内任意的 $x_1, x_2$，都有：
> $$
> f\left(\frac{x_1 + x_2}{2}\right) \leq \frac{f(x_1) + f(x_2)}{2}
> $$
> 则称函数 $f(x)$ 是凸函数。
> 

> [!caution]
> 
> ==根据二阶导数判定函数的凸性==
> 
> 二阶导数>0, 凸函数
> 二阶导数<0, 凹函数
> 二阶导数=0, 可能是拐点
> 

> [!note]
> 
> ---
> 
> > ==P148 例1==
> 
> > ==P149 例2==

# 微分中值定理
> [!tip]
> 
> **微分中值定理**是微积分中的核心结论. 类似于连续函数的**介值定理**, **微分中值定理**揭示了连续且可导的函数局部和整体之间的某种联系.

> [!important]
>
> ---
>
> > **微分中值定理（拉格朗日中值定理）：**
> > 设函数 $f(x)$ 在闭区间 $[a, b]$ 上连续，并且在开区间 $(a, b)$ 上可导。那么，存在一个点 $c \in (a, b)$，使得：
> > $$
> > f'(c) = \frac{f(b) - f(a)}{b - a}
> > $$
> > 
> > 该定理的几何意义是：在曲线 $y = f(x)$ 上，至少存在一点 $c$，它的切线斜率等于割线通过点 $(a, f(a))$ 和 $(b, f(b))$ 的斜率。
> > 
> > **注意**: 该定理的结论也是**存在性**的, 并没有给出这个点 $c$ 的具体计算方法.
> > 
> > 定理的证明从略.
> > 
> > 这个定理的用处很大, 我们后面会慢慢体会到.
>
> > ![中值定理](media/img/mean_value_theorem.png#400h)
> > 

> [!note]
> 
> ---
> 
> > ==例1==
> > 
> > $f(x) = x^2$ 对任意两点 $x_1$, $x_2$.
> >
>
> > ==例2==
> > 
> > $f(x) = x^3$ 对 $x_1 = 0$, $x_2 = 1$.
> 

[回到主页面](index.html)