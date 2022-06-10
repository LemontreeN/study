$$
\int_{-\infty}^{+\infty}e^{-x^2}dx=\sqrt{\pi}
$$

$$
\Gamma 函数:\\
定义:\Gamma (a)=\int_0^{+\infty}x^{a-1}e^{-x}dx\quad (a>0)\\
性质:\Gamma (a+1)=a\Gamma (a),\Gamma (1)=\Gamma (2)=1,\Gamma (n)=(n-1)!,\Gamma (\frac{1}{2})=\sqrt{\pi}\\
使用时注意,\int_0^{+\infty}x^2e^{-\lambda x}dx=\frac{1}{\lambda^3}(\lambda x)^2e^{-\lambda x}d(\lambda x)=\frac{2}{\lambda^3}
$$

[TOC]

### 第一章:随机事件和概率

$$
A-B=A\overline{B}
$$

##### 事件的运算性质

> 一般的运算顺序: $括号\rightarrow 逆\rightarrow 积\rightarrow 和或差$

$$
分配律:(A\cup B)\cap C=(A\cap C)\cup (B\cap C)\\
(A\cap B)\cup C=(A\cup C)\cap (B\cup C)\\
对偶律:\overline{A\cup B}=\overline{A}\ \overline{B}\\
\overline{A_1\cup A_2...\cup A_n}=\overline{A_1}\cap\overline{A_2}...\cap\overline{A_n}\\
\overline{A\cap B}=\overline{A}\cup \overline{B}\\
\overline{A_1\cap A_2...\cap A_n}=\overline{A_1}\cup\overline{A_2}...\cup\overline{A_n}\\
$$

#####  概率运算

$$
减法公式:P(A-B)=P(A)-P(AB) \\
加法公式:
P(A+B)=P(A)+P(B)-P(AB)\\
P(A+B+C)=P(A)+P(B)+P(C)-P(AB)-P(AC)-P(BC)+P(ABC)\\
乘法公式:P(A|B)P(B)=P(AB),P(B|A)P(A)=P(AB)\\
P(A_1A_2...A_n)=P(A_1cc)P(A_2|A_1)...P(A_n|A_1A_2...A_{n-1})
$$

 

### 第二章:随机变量及其分布

<div style="background:#cce1f3">几何分布</div>

$$
P\{X=k\}=pq^{n-1},称X服从参数为p的几何分布\\
其中0\lt p\lt 1,q=1-p
$$



<div style="background:#cce1f3">泊松分布</div>

$$
P\{X=k\}=\frac{\lambda ^k}{k!}e^{-\lambda},k=0,1,2,...\\
其中\lambda>0,称X服从参数为\lambda的泊松分布,记作X\sim P(\lambda)
$$

> 对于二项分布$X\sim B(n,p)$,如果$n$很大,$p$很小时,可以由$\lambda=np$的泊松分布近似估计$(n\ge100,np\le10)$,即
> $$
> C_{n}^{k}p^k(1-p)^{n-k}\approx \frac{\lambda^ke^{-\lambda}}{k!}(\lambda=np)
> $$

> 对于超几何分布,如果$N$很大,$n$很小,那么超几何分布可以近似看做二项分布

<div style="background:#cce1f3">指数分布</div>

$$
X的概率密度函数:f(x)=\left\{\begin{matrix}
\lambda e^{-\lambda x},x>0\\
0,x\le 0
\end{matrix}\right.,其中\lambda >0\\
则称X服从参数为\lambda的指数分布,记作X\sim E(\lambda)\\
X的分布函数为:F(x)=\left\{\begin{matrix}
1-e^{-\lambda x},x>0\\
0,x\le 0
\end{matrix}\right.
$$

<div style="background:#cce1f3">正态分布</div>

$$
X的概率密度函数:f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}},\ (-\infty<x<+\infty)\\
其中\sigma>0,简记为X\sim N(\mu,\sigma^2)\\
当\mu=0,\sigma=1,时X服从标准正态分布,记为X\sim N(0,1)\\
此时\varphi(x)=\frac{1}{\sqrt{2\pi}}e^{\frac{x^2}{2}}(-\infty<x<+\infty)
$$

> 性质

$$
若X\sim N(\mu,\sigma^2)\\
x=\mu为f(x)的驻点,且取到最大值f(\mu)=\frac{1}{\sqrt{2\pi}\sigma}\\
在x=\mu\pm\sigma处为f(x)的拐点\\
概率密度曲线关于x=\mu对称\\
若X\sim N(0,1)\\
则\Phi(x)=1-\Phi(-x)\\
若X\sim N(\mu_1,\sigma_1^2),Y\sim N(\mu_2,\sigma_2^2),则X+Y\sim N(\mu_1+\mu_2,\sigma_1^2+\sigma_2^2)
$$

> 一般正态分布与标准正态分布转换关系

$$
\varphi(x)=\frac{1}{\sigma}\varphi_0(\frac{x-\mu}{\sigma})\\
\Phi(x)=\Phi_0(\frac{x-\mu}{\sigma})\\
例如,X\sim N(1,4),则\mu=1,\sigma=2,\Phi(2)=\Phi_0(\frac{2-1}{2})=\Phi_0(\frac{1}{2})
$$

> 举例$X\sim N(\mu,\sigma^2),Y=aX+b,a\ne0$

$$
a>0时,F_Y(x)=P\{Y\le x\}=P\{aX+b\le x\}=P\{X\le \frac{x-b}{a}\}=\Phi(\frac{x-b}{a})\\
两侧同时求导可得f_Y(x)=\phi(\frac{x-b}{a})\frac{1}{a}=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(\frac{x-b}{a}-u)^2}{2\sigma^2}}\frac{1}{a}\\
=\frac{1}{\sqrt{2\pi}a\sigma}e^{-\frac{(x-(b+a\mu))^2}{2a^2\sigma^2}}=\frac{1}{\sqrt{2\pi}a\sigma}e^{-\frac{(x-(b+a\mu))^2}{2(a\sigma)^2}}\\
同理可得a<0时,f_Y(x)=\frac{1}{\sqrt{2\pi}(-a\sigma)}e^{-\frac{(x-(b+a\mu))^2}{2a^2\sigma^2}}\\
综上f_Y(x)=\frac{1}{\sqrt{2\pi}|a|\sigma}e^{-\frac{(x-(b+a\mu))^2}{2a^2\sigma^2}},\quad Y\sim N(a\mu+b,a^2\sigma^2)
$$

> 分布函数法

$$
F_Y(y)=P\{g(X)\le y\}=P\{X\ opt\ g^{-1}(y)\}=opt (F_X(g^{-1}))=\int_{g(x)\le y}f(x)dx\\
两侧同时求导得到f_Y(y)
$$

> 例题:
> $$
> Y=\ln X,F_X(x)=\left\{\begin{matrix}
> 0,\quad \ \ \ \ \ \ x\le 1\\
> 1-x^{-\lambda},x>1
> \end{matrix}\right.\\
> $$
>
> + 解答:
>
> $$
> \begin{aligned}
> F_Y(y)&=P\{Y\le y\}=P\{\ln X\le y\}=P\{X\le e^y\}\\
> &=F_X(e^y)=\left\{\begin{matrix}
> 0,\quad \ \ \ \ \ \ e^y\le 1\\
> 1-(e^y)^{-\lambda},e^y>1
> \end{matrix}\right.
> =\left\{\begin{matrix}
> 0,\quad \ \ \ \ \ \ y\le 0\\
> 1-e^{-\lambda y},y>0
> \end{matrix}\right.\\
> f_Y(y)&=F_Y'(y)=\left\{\begin{matrix}
> 0,\quad \ \ \ \ \ \ y\le 0\\
> \lambda e^{-\lambda y},y>0
> \end{matrix}\right.
> \end{aligned}
> $$

> 公式法

$$
若y=g(x)严格单调时,h(y)为g(x)的反函数\\
f_Y(y)=\left\{\begin{matrix}
f_X[h(y)]|h'(y)|,\quad \alpha<y<\beta\\
0,\quad \quad \quad \quad else
\end{matrix}\right.\\
其中[\alpha,\beta]是g(x)在X上的值域
$$

### 第三章:多维随机变量分布

##### 概述

$$
设(X,Y)为二维随机变量\\联合分布函数:F(x,y)=P\{X\le x,Y\le y\},\ \ -\infty <x,y<+\infty
$$

> 性质

$$
F(x,y)关于x和y右连续,即F(x+0,y)=F(x,y)=F(x,y+0)\\
随机点(X,Y)落在矩形域G=\{(x,y)|x_1\lt X\le x_2,y_1\lt Y\le y_2\}上的概率为\\
\begin{aligned}
P\{(X,Y)\in G\}&=P\{x_1\lt X\le x_2,y_1\lt Y\le y_2\}\\
&=F(x_2,y_2)-F(x_2,y_1)-F(x_1,y_2)+F(x_1,y_1)
\end{aligned}
$$

<div style="background:#cce1f3">边缘分布函数</div>

$$
F_X(x)=P\{X\le x\}=P\{X\le x,Y\lt +\infty\}=F(x,+\infty)=\lim_{y\to +\infty}F(x,y)\\
F_Y(y)=P\{Y\le y\}=P\{X\lt +\infty,Y\le y\}=F(+\infty,y)=\lim_{x\to +\infty}F(x,y)
$$

##### 二维连续型随机变量

> 定义:

设二维随机变量$(X,Y)$的分布函数为$F(x,y)$,如果存在非负的可积函数$f(x,y)$使得对于任意$x,y$有
$$
F(x,y)=\int_{-\infty}^x\int_{+\infty}^yf(u,v)dudv
$$
则称$(X,Y)$为**二维连续型随机变量**,$f(x,y)$为它的概率密度

> 性质

$$
f(x,y)\ge0\\
若f(x,y)在点(x,y)处连续,则\frac{\partial^2F(x,y)}{\partial x\partial y}=f(x,y)
$$

  <div style="background:#cce1f3">边缘分布</div>

$$
边缘分布函数:F_X(x)=F(x,+\infty)=\int_{-\infty}^x[\int_{-\infty}^{+\infty}f(x,y)dy]dx\\
边缘概率密度:f_X(x)=\int_{-\infty}^{+\infty}f(x,y)dy
$$

<div style="background:#cce1f3">条件概率密度</div>

$$
在条件Y=y下X的条件概率密度:f_{X|Y}(x,y)=\frac{f(x,y)}{f_Y(y)}\\
分布函数:F_{X|Y}(x,y)=\int_{-\infty}^x\frac{f(t,y)}{f_Y(y)}dt\\
密度乘法公式:f(x,y)=f_X(x)f_{Y|X}(y|x)=f_Y(y)f_{X|Y}(x|y)\quad (f_X(x),f_Y(y)>0)\\
可用于求联合概率密度
$$

##### 独立性

$$
若P\{X\le x,Y\le y\}=P\{X\le x\}P\{Y\le y\}\\
F(x,y)=F_X(x)F_Y(y)\\
则称随机变量X,Y相互独立
$$

> 性质

$$
若随机变量X_1,..,X_m相互独立,它们的函数g_1(x_1),..,g_m(X_m)也相互独立
$$

##### 卷积公式:对于$X+Y$

$$
若X,Y为随机变量,则对于Z=X+Y,有\\
f_Z(z)=\int_{-\infty}^{+\infty}f(x,z-x)dx=^{若X,Y独立}\int_{-\infty}^{+\infty}f_X(x)f_Y(z-x)dx\\
=\int_{-\infty}^{+\infty}f(z-y,y)dy=^{若X,Y独立}\int_{-\infty}^{+\infty}f_X(z-y)f_Y(y)dy\\
常记作f_X*f_Y=\int_{-\infty}^{+\infty}f_X(x)f_Y(z-x)dx=\int_{-\infty}^{+\infty}f_X(z-y)f_Y(y)dy
$$

> 被积函数变元之和为$z$

##### 对于$Z=X-Y,Z=Y-X$

$$
设(X,Y)的概率密度为f(x,y)\\
\begin{aligned}
Z_1=X-Y的概率密度为\\
f_1(z)&=\int_{-\infty}^{+\infty}f(x,x-z)dx=\int_{-\infty}^{+\infty}f(x+z,x)dx\\
&=^{独立}\int_{-\infty}^{+\infty}f_X(x+z)f_Y(x)dx\\
Z_2=Y-X的概率密度为\\
f_2(z)&=\int_{-\infty}^{+\infty}f(x,x+z)dx\\
&=^{独立}\int_{-\infty}^{+\infty}f_X(x)f_Y(x+z)dx
\end{aligned}
$$

> 被积函数变元之差为$z$

##### 对于$Z=XY$

$$
设(X,Y)是二维连续性随机变量,概率密度为f(x,y)\\
则Z=XY仍为连续性随机变量,概率密度为\\
\begin{aligned}
f_{XY}(z)&=\int_{-\infty}^{+\infty}\frac{1}{|x|}f(x,\frac{z}{x})dx\\
&=^{独立}\int_{-\infty}^{+\infty}\frac{1}{|x|}f_X(x)f_Y(\frac{z}{x})dx
\end{aligned}
$$

> 被积函数变元之积为$z$

##### 对于$\max{X,Y}$和$\min{X,Y}$

$$
设M=\max\{X,Y\},N=\min\{X,Y\},\quad X,Y独立\\
\begin{aligned}
F_M(z)&=P\{M\le z\}=P\{X\le z,Y\le z\}=P\{X\le z\}P\{Y\le z\}\\
&=F_X(z)F_Y(z)\\
F_N(z)&=P\{N\le z\}=1-P\{N>z\}=1-P\{x>z,y>z\}\\
&=1-P\{X>z\}P\{Y>z\}=1-(1-P\{X\le z\})(1-P\{Y\le z\})\\
&=1-(1-F_X(z))(1-F_Y(z))
\end{aligned}
$$

##### 分布的可加性

> 相互独立且服从同类型分布的随机变量其和的分布也是同类型的
>
> 二项分布 / 泊松分布 / 正态分布 / 和 $\chi^2$分布

$$
\begin{aligned}
&若X\sim B(n,p),Y\sim B(m,p),&X+Y\sim B(n+m,p)\\
&若X\sim P(\lambda_1),Y\sim P(\lambda_2),&X+Y\sim P(\lambda_1+\lambda_2)\\
&若X\sim N(\mu_1,\sigma_1^2),Y\sim N(\mu_2,\sigma_2^2),&X+Y\sim B(\mu_1+\mu_2,\sigma_2^2+\sigma_2^2)\\
&若X\sim \chi^2(n),Y\sim \chi^2(m),&X+Y\sim \chi^2(n+m)\\
\end{aligned}
$$

> 上述结论对n个相互独立同分布的随机变量也成立
>
> 泊松分布证明:

$$
X,Y独立,且分别服从参数为\lambda_1,\lambda_2的泊松分布,求Z=X+Y的分布\\
P\{Z=k\}=\sum_{i=0}^kP\{X=i,Y=k-i\}=\sum_{i=0}^kP\{X=i\}P\{Y=k-i\}\\
=\sum_{i=0}^k\frac{\lambda_1^i}{i!}e^{-\lambda_1}\frac{\lambda_2^{k-i}}{(k-i)!}e^{-\lambda_2}=\frac{(\lambda_1+\lambda_2)^k}{k!}e^{-(\lambda_1+\lambda_2)}\\
所以Z\sim P(\lambda_1+\lambda_2)
$$

> 正态分布证明:

$$
X\sim N(0,1),Y\sim N(0,1),X,Y独立,求Z=X+Y\\
\begin{aligned}
解:\varphi_Z(z)&=\int_{-\infty}^{+\infty}\varphi_X(x)\varphi_Y(z-x)dx\\
&=\int_{-\infty}^{+\infty}\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}\frac{1}{\sqrt{2\pi}}e^{-\frac{(z-x)^2}{2}}dx\\
&=\int_{-\infty}^{+\infty}\frac{1}{2\pi}e^{-\frac{z^2}{4}}e^{-(x-\frac{z}{2})^2}d(x-\frac{\pi}{2})\\
&=\frac{1}{\sqrt{2\pi}\sqrt{2}}e^{-\frac{z^2}{2(\sqrt{2})^2}}\\
所以Z\sim N(0,2)
\end{aligned}
$$

### 第四章:随机变量的数字特征

##### 数学期望

<div style="background:#cce1f3">离散型随机变量</div>

$$

$$



<div style="background:#cce1f3">连续型随机变量</div>

$$
设连续性随机变量X的概率密度为f(x),如果\int_{-\infty}^{+\infty}xf(x)dx绝对收敛\\
那么称此反常积分的值为随机变量X的数学期望\\
即EX=\int_{-\infty}^{+\infty}xf(x)dx\\
二维:如果\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}g(x.y)f(x,y)dxdy绝对收敛,Z=g(x,y)\\
EZ=E[g(x,y)]=\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}g(x.y)f(x,y)dxdy
$$

> 性质:

$$
E(kX+b)=kEX+b\\
E(X\pm Y)=EX\pm EY\\
X,Y独立,则E(XY)=E(X)E(Y)
$$

<div style="background:#cce1f3">条件期望</div>

$$
\begin{aligned}
离散型:E(X|Y=y_j)&=\sum x_iP(X=x_i|Y=y_j)\\
E(Y|X=x_i)&=\sum y_jP(Y=y_j|X=x_i)\\
连续型:E(X|Y=y)&=\int_{-\infty}^{+\infty}xf(x|y)dx\\
E(Y|X=x)&=\int_{-\infty}^{+\infty}yf(y|x)dy
\end{aligned}
$$

#### 方差

$$
DX=E(X-EX)^2\ (定义)\ =EX^2-(EX)^2
$$

> 性质:

$$
D(kX+b)=k^2DX\\
D(X\pm Y)=D(X)+D(Y)\pm 2Cov(X,Y)\\
X,Y独立,则D(X\pm Y)=D(X)+D(Y)\\
标准化:对于X^*=\frac{X-EX}{\sqrt{DX}},EX^*=0,DX^*=1
$$

##### 常见离散型的期望和方差

$$
\begin{aligned}
0-1分布:&EX=p,&DX=pq\\
二项分布:&EX=np,&DX=npq\\
几何分布:&EX=\frac{1}{p},&DX=\frac{1-p}{p^2}\\
泊松分布:&EX=\lambda,&DX=\lambda
\end{aligned}
$$

##### 常见连续型的期望和方差

$$
均匀分布:EX=\frac{a+b}{2},DX=\frac{(b-a)^2}{12}\\
指数分布:EX=\frac{1}{\lambda},DX=\frac{1}{\lambda^2}\\
正态分布:EX=\mu,DX=\sigma^2
$$

##### 协方差和相关系数

<div style="background:#cce1f3">协方差</div>


$$
Cov(X,Y)=E[(X-EX)(Y-EY)]\ (定义)\ =E(XY)-EXEY
$$

> 性质:

$$
Cov(aX,bY)=abCov(X,Y)\\
Cov(X_1+X_2,Y)=Cov(X_1,Y)+Cov(X_2,Y)\\
Cov(C,X)=0\\
若X,Y独立,则Cov(X,Y)=0\\
协方差会受到单位的影响\\
Cov(X,X)=DX
$$

<div style="background:#cce1f3">相关系数</div>

$$
\rho=\frac{Cov(X,Y)}{\sqrt{DX}\sqrt{DY}}
$$

> 性质:

$$
[E(XY)]^2\le EX^2EY^2\\
|\rho|\le1 \\
|\rho=1|\Leftrightarrow X与Y以\rho=1成线性关系,即P(Y=aX+b)=1\\
对于二维正态分布(X,Y)或者两个0-1分布X,Y,独立和不相关等价
$$

##### 原点矩与中心矩

$$
原点矩:E(x^k)\\
中心矩:E(X-EX)^k
$$

### 第五章:大数定律与中心极限定理

<div style="background:#cce1f3">切比雪夫不等式</div>

$$
若EX和DX存在,则对于\forall \varepsilon >0,都有\\
P\{|X-EX|\ge \varepsilon\}\le\frac{DX}{\varepsilon ^2}
$$

##### 大数定律

<div style="background:#cce1f3">伯努利大数定律</div>

$$
设随机变量X_n\sim B(n,p),\mu_n为n次实验中事件A发生的次数\\
则对于\forall\varepsilon>0,都有\\
\lim_{n\to \infty}P\{|\frac{\mu_n}{n}-p|<\varepsilon\}=1
$$

<div style="background:#cce1f3">切比雪夫大数定律 </div>

$$
设随机变量X_1,X_2,...X_n不相关,期望EX_i,D_i都存在,并且方差有公共上界\\
即DX_i\le c,i=1,2...,则对于\forall\varepsilon >0,都有\\
\lim_{n\to \infty}P\{|\frac{1}{n}\sum_{i=1}^n X_i-\frac{1}{n}\sum_{i=1}^n EX_i|<\varepsilon\}=1
$$

<div style="background:#cce1f3">辛钦大数定律</div>

$$
设随机变量X_1,X_2,...X_n相互独立同分布,期望EX存在且为\mu\\
则对任意\varepsilon>0,都有\\
\lim_{n\to \infty}P\{\frac{1}{n}\sum_{i=1}^nX_i-\mu<\varepsilon\}=1
$$

##### 中心极限定理

<div style="background:#cce1f3">独立同分布</div>

> 列维-林德伯格定理

$$
设随机变量X_1,..,X_n独立同分布,数学期望/方差存在\\
E(X_k)=\mu,D(X_k)=\sigma^2>0,(k=0,1,2..)\\
则对任实数x,恒有\\
\lim_{n\to \infty}P\{\frac{1}{\sigma\sqrt{n}}(\sum_{i=1}^nX_i-n\mu)\le x\}=\Phi(x)\\
其中\Phi(x)为标准正态分布的分布函数
$$

> $$
> n很大时,独立同分布随机变量的和\sum_{i=1}^nX_i近似服从正态分布N(n\mu,n\sigma^2)\\
> 且标准化后的\frac{1}{\sigma\sqrt{n}}(\sum_{i=1}^nX_i-n\mu)近似服从标准正态分布N(0,1)
> $$
>
> 

<div style="background:#cce1f3">二项分布</div>

> 棣莫夫-拉普拉斯定理

$$
设随机变量Y_n服从参数为n,p(0<p<1,n=1,2,...)的二项分布\\
则对于任意实数x,都有\\
\lim_{n\to\infty}P\{\frac{Y_n-np}{\sqrt{np(1-p)}}\le x\}=\Phi(x)\\
其中\Phi(x)为标准正态分布的分布函数
$$

> 理解:把二项分布的$Y_n$看做$\sum_{x=i}^nX_i$,其中$X_i=\left\{\begin{matrix}
> 1,发生\\0,未发生\end{matrix}\right.\\$
>
> 可以看出,此定理为上面`列维-林德伯格定理`的特殊情形

> 例题:
> $$
> 每个人死亡概率为0.005,共1万人,求死亡人数\le70的概率\\
> \begin{aligned}
> P(X\le 70)&=\sum_{k=0}^{70}C_{10000}^k0.005^k0.995^{10000-k}\\
> &=P(\frac{x-np}{\sqrt{np(1-p)}}\le\frac{70-np}{\sqrt{np(1-p)}})\\
> &=\Phi_0(2.84)=0.9977\\
> P(X=k)&=P(k-\frac{1}{2}<x<k+\frac{1}{2})\\
> &=P(\frac{k-\frac{1}{2}-np}{\sqrt{np(1-p)}}<\frac{x-np}{\sqrt{np(1-p)}}<\frac{k+\frac{1}{2}-np}{\sqrt{np(1-p)}})\\
> &=\Phi_0(\frac{k+\frac{1}{2}-np}{\sqrt{np(1-p)}})-\Phi_0(\frac{k-\frac{1}{2}-np{}}{\sqrt{np(1-p)}})
> \end{aligned}
> $$

### 第六章:数理统计的基本概念

##### 简单随机样本的概率分布

$$
如果总体分布函数F(x),概率密度为f(x)\\
X_1,X_2,..,X_n是来自总体X的简单随机样本,则\\
它们的联合分布函数为F(x_1,..,x_n)=\prod_{i=1}^nF(x_i),x_i\in R(i=1,2,..,n)\\
它们的联合概率密度为f(x_1,..,x_n)=\prod_{i=1}^nf(x_i),x_i\in R(i=1,2,..,n)\\
如果总体X的概率密度为P\{X=a_j\}=p_j(j=1,2,...)\\
则样本的联合概率分布为P\{X_1=x_1,X_2=x_2,..,X_n=x_n\}=\prod_{i=1}^nP\{X_i=x_i\}\\
其中x_i取a_1,a_2,...中的某一个数
$$

$$
方差:S^2=\frac{1}{n-1}\sum_{i=1}^n(X_i-\bar{X})^2=\frac{1}{n-1}(\sum_{i=1}^nX_i^2-n\bar{X}^2)
$$


$$
E(\bar{X})=EX=\mu\\
D(\bar{X})=\frac{DX}{n}=\frac{\sigma^2}{n}\\
ES^2=\sigma^2(样本方差的期望)
$$

#### 抽样分布

##### 卡方分布

> $\chi^2$分布:   $\chi^2(n):自由度为n$

> 有用的性质:

$$
对于\chi^2(n),EX=n,DX=2n\\
由中心极限定理,若X\sim\chi^2(n),n充分大时,\frac{x-n}{\sqrt{2n}}\sim N(0,1)\\
设随机变量X_1,X_2,..,X_n独立,且都服从标准正态分布N(0,1)\\
则\sum_{i=1}^n x_i^2\sim\chi^2(n)\\
若X\sim\chi^2(n),Y\sim\chi^2(m),X,Y独立,则X+Y\sim\chi^2(m+n)
$$

> 上$\alpha$分位点

$$
P\{\chi^2>\chi^2_\alpha(n)\}=\int_{\chi^2_\alpha(n)}^{+\infty}f(t)dt=\alpha\\
例如\chi^2_{0.05}(10)=18.3,意思是n=10时,\\
\int_{18.3}^{+\infty}f(t)dt=0.05,其中f(t)为\chi^2(10)的概率密度函数
$$

> 一般没用的性质

$$
单峰曲线,\chi^2(n)在n-2取得最大值\\
n增大,峰向右移动,n很大时可用正态分布近似\\
\chi^2(2)是一个\lambda=\frac{1}{2}的指数分布\\
$$

##### $t$分布

> 定义:

$$
设X\sim N(0,1),Y\sim\chi^2(b),且X和Y独立\\
那么随机变量t=\frac{X}{\sqrt{Y/n}}为自由度为n的t分布,记作t\sim t(n)
$$

> 性质

$$
t_{1-\alpha}(n)=-t_\alpha(n)
$$

##### $F$分布

> 定义:

$$
设X\sim\chi^2(n_1),Y\sim\chi^2(n_2),且X,Y独立\\
那么随机变量F=\frac{X/n_1}{Y/n_2}为自由度为(n_1,n_2)的F分布,记作F\sim F(n_1,n_2)
$$

> 性质:

$$
若F\sim F(n_1,n_2),则\frac{1}{F}\sim F(n_2,n_1)\\
F_{1-\alpha}(n_1,n_2)=\frac{1}{F_\alpha(n_2,n_1)}
$$

##### 正态总体下的抽样分布

<div style="background:#cce1f3">单个正态总体</div>

> $$
> 设X\sim N(\mu,\sigma^2),X_1,X_2,..,X_n是来自总体X的简单随机样本,\\
> \bar{X}=\frac{1}{n}\sum_{i=1}^n X_i与S^2=\frac{1}{n-1}\sum_{i=1}^n(X_i-\bar{X})^2分别为对应样本均值和方差\\
> $$

$$
样本均值的分布:\bar{X}\sim N(\mu,\sigma^2/n),\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}\sim N(0,1)\\
\frac{\bar{X}-\mu}{S/\sqrt{n}}\sim t(n-1)\\
样本方差的分布:\frac{(n-1)S^2}{\sigma^2}=\sum_{i=1}^n(\frac{X_i-\bar{X}}{\sigma})^2\sim\chi^2(n-1)\\
\frac{1}{\sigma^2}\sum_{i=1}^n(X_i-\mu)^2\sim\chi^2(n)\\
\bar{X}与S^2相互独立
$$

> 为什么上面两个相似的式子中一个自由度为$n-1$,一个为$n$?
> $$
> 因为\bar{X}=\sum_{i=1}^nX_i,相当于方程中多了一个约束,因此自由未知量减少1
> $$

<div style="background:#cce1f3">两个正态总体</div>

> $$
> 设X_1,..,X_{n_1}与Y_1,..Y_{n_2}分别是来自正态总体N(\mu_1,\sigma_1^2)和N(\mu_2,\sigma_2^2)的样本\\
> 且这两个样本相互独立(指随机变量相互独立)\\
> 设\bar{X},S_X^2,\bar{Y},S_Y^2是相应的样本均值和样本方差,S_{XY}是X和Y总体的联合样本方差\\
> 记\bar{X}=\frac{1}{n_1}\sum_{i=1}^{n_1}X_i,\bar{Y}=\frac{1}{n_2}\sum_{i=1}^{n_2}Y_i\\
> S_X^2=\frac{1}{n_1-1}\sum_{i=1}^{n_1}(X_i-\bar{X})^2,S_Y^2=\frac{1}{n_2-1}\sum_{i=1}^{n_2}(Y_i-Y)^2\\
> S_{XY}^2=\frac{(n_1-1)S_X^2+(n_2-1)S_Y^2}{n_1+n_2-2}
> $$

$$
样本均值差的抽样分布:\bar{X}-\bar{Y}\sim N(\mu_1-\mu_2,\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2})\\
\frac{\bar{X}-\bar{Y}-(\mu_1-\mu_2)}{\sqrt{\sigma_1^2/n_1+\sigma^2/n_2}}\sim N(0,1)\\
样本方差比的抽样分布:F=\frac{S_X^2/\sigma_1^2}{S_Y^2/\sigma^2}\sim F(n_1-1,n_2-1)\\
若\sigma_1=\sigma_2=\sigma时,有T=\frac{(\bar{X}-\bar{Y}-(\mu_1-\mu_2))}{S_{XY}\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}\sim t(n_1+n_2-2)\\
W=\frac{(n_1+n_2-2)S_{XY}^2}{\sigma^2}\sim \chi^2(n_1+n_2-2)
$$

### 第七章:参数估计和假设检验

#### 点估计

##### 矩估计法

> $n$阶原点矩为$A_n$,$n$阶中心距为$B_n$
>
> 以$X\sim N(\mu,\sigma^2)$为例

$$
总体一阶矩:EX=\mu\\
样本一阶矩:\bar{X}=\frac{1}{n}\sum_{i=1}^nx_i\\
总体二阶矩:EX^2=DX+(EX)^2=\sigma^2+\mu^2\\
样本二阶矩:A_2=\frac{1}{n}\sum_{i=1}^nx_i^2\\
则\hat{\mu}=\bar{X},\\
\hat{\sigma}^2=A_2-\hat{\mu}^2=\frac{1}{n}\sum_{i=1}^nx_i^2-\bar{X}^2=\frac{1}{n}\sum_{i=1}^n(X_i-\bar{X})^2=B_2
$$

##### 极大似然估计

> 步骤:
>
> 1. 写出概率密度函数
>
> 2. 写出似然函数
>
> 3. 两边取$\ln$
>
> 4. 对参数求(偏)导$=0$,求出参数估计值

##### 点估计的优良性准则

无偏性
$$
总体X,EX=\mu,DX=\sigma^2 (X_1,X_2,..X_n)\\
\bar{X}是\mu的无偏估计\\
样本方差S^2是\sigma^2的无偏估计\\
未修正方差S_0^2是\sigma^2的有偏估计\\
$$

$$
\hat{\theta}是\theta的无偏估计,g(\hat{\theta})不一定是g(\theta)的无偏估计
$$

有效性
$$
设\hat{\theta_1},\hat{\theta_2}都是参数\theta的无偏估计\\
若D\hat{\theta_1})<D(\hat{\theta_2}),则称\hat{\theta_1}比\hat{\theta_2}更有效
$$
一致性(相合性)

#### 区间估计

##### 对$\mu$进行区间估计

> $\sigma^2$已知

$$
使用\frac{\bar{X}-\mu}{\sigma/\sqrt{n}}\sim N(0,1)\\
\mu\in[\bar{X}-\frac{\sigma}{\sqrt{n}}\mu_{\frac{\alpha}{2}},\bar{X}+\frac{\sigma}{\sqrt{n}}\mu_{\frac{\alpha}{2}}]
$$

> $\sigma^2$未知

$$
使用\frac{\bar{X}-\mu}{S/\sqrt{n}}\sim t(n-1)\\
\mu\in[\bar{X}-\frac{S}{\sqrt{n}}t_{\frac{\alpha}{2}(n-1)},\bar{X}+\frac{S}{\sqrt{n}}t_{\frac{\alpha}{2}(n-1)}]
$$



##### 对$\sigma^2$进行区间估计

> $\mu$已知

$$
使用\frac{1}{\sigma^2}\sum_{i=1}^n(X_i-\mu)^2\sim\chi^2(n)\\
给定1-\alpha,查表\chi^2_{1-\frac{\alpha}{2}}(n),\chi^2_{\frac{\alpha}{2}}(n)\\
\chi^2_{1-\frac{\alpha}{2}}(n)\le\frac{1}{\sigma^2}\sum_{i=1}^n(x_i-\mu)^2\le\chi^2_{\frac{\alpha}{2}}(n)\\
\frac{\sum_{i=1}^n(x_i-\mu)^2}{\chi^2_{\frac{\alpha}{2}}(n)}\le\sigma^2\le\frac{\sum_{i=1}^n(x_i-\mu)^2}{\chi^2_{1-\frac{\alpha}{2}}(n)}
$$

> $\mu$未知

$$
使用\chi^2=\frac{(n-1)S^2}{\sigma^2}\sim\chi^2(n-1)\\
查表获得\chi^2_{1-\frac{\alpha}{2}}(n-1),\chi^2_{\frac{\alpha}{2}}(n-1)\\
\sigma^2\in [\frac{(n-1)S^2}{\chi^2_{\frac{\alpha}{2}}(n-1)},\frac{(n-1)S^2}{\chi^2_{1-\frac{\alpha}{2}}(n-1)}]
$$

#### 假设检验

> 1. 提出原假设$H0$和备择假设$H1$
> 2. 假定$H0$成立,选取检验统计量$T$($T$的分布已知)
> 3. 给定$\alpha$,找到拒绝域和接收域
> 4. 由样本数据$(x_1,..,x_n)$求出统计量$T$的值,看落在拒绝域还是接收域

<div style="background:#cce1f3">两类错误</div>

| 决策\总体情况 | $H_0$为真 | $H_0$为假 |
| :----:| :---: | :----: |
| 接受$H_0$ | 正确决策:1-$\alpha$ | 纳伪$\beta$ |
| 拒绝$H_0$ | 弃真:$\alpha$ | 正确决策:1-$\beta$ |

##### 一个正态总体的参数假设检验

> $$
> X\sim N(\mu,\sigma^2),(X_1,..,X_n)是取自X的样本,检验水平为\alpha\\
> $$

> $\mu$的假设检验:假定检验问题为$H_0:\mu=\mu_0,H_1:\mu\ne\mu_0$

> $U$检验

$$
已知\sigma^2=\sigma_0^2,检验H_0:\mu=\mu_0\\
\begin{aligned}
第一步:&H_0:\mu=\mu_0,H_1:\mu\ne\mu_0\\
第二步:&假定H_0成立,则X\sim N(\mu_0,\sigma_0^2),取统计量U=\frac{\bar{X}-\mu0}{\sigma/\sqrt{n}}\sim N(0,1)(\bar{X}不带入)\\
第三步:&给定\alpha 由P\{|U|>U_{\frac{\alpha}{2}}\}=\alpha确定拒绝域\\
第四步:&计算U的值,|u|与u_{\frac{\alpha}{2}}比较下结论\\

&若|u|>u_{\frac{\alpha}{2}},拒绝H_0,若|u|<u_{\frac{\alpha}{2}},接受H_0,若相等则再抽样检验
\end{aligned}\\
若检验H_0:\mu\le \mu_0\\
第三步:给定\alpha,由P\{u>u_\alpha\}确定拒绝域\\
若检验H_0:\mu\ge \mu_0\\
第三步:给定\alpha,由P\{u<-u_\alpha\}确定拒绝域
$$

> $T$检验

$$
\sigma^2未知,检验H_0:\mu=\mu_0\\
\begin{aligned}
第一步:&H_0:\mu=\mu_0,H_1:\mu\ne\mu_0\\
第二步:&假定H_0成立,取统计量T=\frac{\bar{X}-\mu0}{S/\sqrt{n}}\sim t(n-1)(\bar{X}和S不带入)\\
第三步:&给定\alpha,由P\{|T|>t_{\frac{\alpha}{2}}(n-1)\}=\alpha确定拒绝域\\
第四步:&计算T的值,|t|与t_{\frac{\alpha}{2}}(n-1)比较下结论\\
\end{aligned}\\
若检验H_0:\mu\le \mu_0\\
第三步:给定\alpha,由P\{t>t_\alpha\}确定拒绝域\\
若检验H_0:\mu\ge \mu_0\\
第三步:给定\alpha,由P\{t<-t_\alpha\}确定拒绝域
$$

> $\sigma^2$的假设检验:假定检验问题为$H_0:\sigma^2=\sigma^2_0,H_1:\sigma^2\ne\sigma^2_0$

> $\chi^2$检验

$$
\mu=\mu_0已知,检验H_0:\sigma^2=\sigma_0^2\\
第一步:H_0:\sigma^2=\sigma^2_0,H_1:\sigma^2\ne\sigma_0^2\\
第二步:假定H_0成立,X\sim N(\mu_0,\sigma^2_0),取统计量\chi^2=\frac{\sum_{i=1}^n(X_i-\mu_0)^2}{\sigma^2_0}\sim \chi^2(n)\\
第三步:给定\alpha,由P\{\chi^2>\chi^2_{\frac{\alpha}{2}}(n)\}=P\{\chi^2<\chi^2_{1-\frac{\alpha}{2}}(n)\}=\frac{\alpha}{2}确定拒绝域\\
第四步:计算\chi^2的值与临界值比较下结论
$$

$$
\mu未知,检验H_0:\sigma^2=\sigma_0^2\\
第一步:H_0:\sigma^2=\sigma^2_0,H_1:\sigma^2\ne\sigma_0^2\\
第二步:假定H_0成立,X\sim N(\mu,\sigma^2_0),取统计量\chi^2=\frac{\sum_{i=1}^n(X_i-\bar{X})^2}{\sigma^2_0}\sim \chi^2(n-1)\\
第三步:给定\alpha,由P\{\chi^2>\chi^2_{\frac{\alpha}{2}}(n-1)\}=P\{\chi^2<\chi^2_{1-\frac{\alpha}{2}}(n-1)\}=\frac{\alpha}{2}确定拒绝域\\
第四步:计算\chi^2的值与临界值比较下结论
$$

##### 两个正态总体的参数假设检验

> $$
> X\sim N(\mu_1,\sigma^2_1),X_1,..,X_{n_1}是X的样本,\bar{X},S_1^2\\
> Y\sim N(\mu_2,\sigma^2_2),Y_1,..,Y_{n_2}是Y的样本,\bar{Y},S^2_2\\
> $$

<div style="background:#cce1f3">均值差异性检验</div>

> $$
> H_0:\mu_1=\mu_2,H_1:\mu_1\ne\mu_2\\
> H_0:\mu_1\le\mu_2,H_1:\mu_1\gt\mu_2\\
> H_0:\mu_1\ge\mu_2,H_1:\mu_1\lt\mu_2
> $$

> $U$检验

$$
\sigma^2_1,\sigma_2^2已知,检验H_0:\mu_1=\mu_2\\
第一步:H_0:\mu_1=\mu_2,H_1:\mu_1\ne\mu_2\\
第二步:假定H_0成立,\bar{X}-\bar{Y}\sim N(\mu_1-\mu_2,\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2})\\
取统计量U=\frac{\bar{X}-\bar{Y}-(\mu_1-\mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}}\\
=\frac{\bar{X}-\bar{Y}}{\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}}\sim N(0,1)\\
第三步:给定\alpha,由P\{|U|>u_{\frac{\alpha}{2}}\}=\alpha确定拒绝域|u|>u_{\frac{\alpha}{2}}\\
第四步:计算|u|与u_{\frac{\alpha}{2}}比较,得出结论
$$

> $T$检验法

$$
\sigma_1^2=\sigma_2^2=\sigma^2未知,检验H_0:\mu_1=\mu_2\\
第一步:H_0:\mu_1=\mu_2,H_1:\mu_1\ne\mu_2\\
第二步: 假定H_0成立,取统计量T=\frac{\frac{\bar{X}-\bar{Y}-(\mu_1-\mu_2)}{\sqrt{\frac{\sigma^2}{n_1}+\frac{\sigma^2}{n_2}}}}{\sqrt{\frac{(n_1-1)S_1^2+(n_2-1)S_2^2}{\sigma^2}/(n_1+n_2-2)}}\\
=\frac{\bar{X}-\bar{Y}}{\sqrt{[(n_1-1)S_1^2+(n_2-1)S_2^2]/(n_1+n_2-2)}\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}\sim t(n_1+n_2-2)\\
第三步:给定\alpha,由P\{|T|>t_{\frac{\alpha}{2}}\}=\alpha确定拒绝域|t|>t_{\frac{\alpha}{2}}\\
第四步:计算|t|与t_{\frac{\alpha}{2}}比较,得出结论
$$

<div style="background:#cce1f3">方差差异性检验</div>

> $$
> H_0:\sigma_1^2=\sigma_2^2,H_1:\sigma_1^2\ne\sigma_2^2\\
> H_0:\sigma_1^2\le\sigma_2^2,H_1:\sigma_1^2\gt\sigma_2^2
> $$

> $F$检验法

$$
\mu_1,\mu_2未知,检验H_0:\sigma_1^2=\sigma_2^2\\
第一步:H_0:\sigma_1^2=\sigma_2^2,H_1:\sigma_1^2\ne\sigma_2^2\\
第二步:假定H_0成立,取统计量F=\frac{S_1^2/\sigma_1^2}{S_2^2/\sigma_2^2}=\frac{S_1^2}{S_2^2}\sim F(n_1-1,n_2-1)\\
第三步:给定\alpha,由P\{F>F_{\frac{\alpha}{2}}\}=P\{F<F_{1-\frac{\alpha}{2}}\}=\frac{\alpha}{2}确定拒绝域\\
第四步:计算F与F_{\frac{\alpha}{2}},F_{1-\frac{\alpha}{2}}比较下结论\\
其中F_{1-\frac{\alpha}{2}}(n_1-1,n_2-1)=\frac{1}{F_{\frac{\alpha}{2}}(n_2-1,n_1-1)}
$$

> 若检验均值时既不知道方差,也不知道方差是否相等,则先检验方差,证明方差相等再检验均值

### 附录

常用分布的上$\alpha$分位数
| 分布 | U检验(正态) |  | $\chi^2$分布 | T分布 |
| :----:| :---: | :----: | ------| ------|
| 0.005 | 2.576 |  | 0.21 | 4.604 |
| 0.01 | 2.36 |  |              |  |
| 0.025 | 1.960 |  | 0.48 | 2.776 |
| 0.05 | 1.645 |  | 0.71 | 2.132 |
| 0.1 | 1.282 | 0.95 | 9.49 |  |
|  |  | 0.975 | 11.1 |  |
|  |  | 0.995 | 14.9 |  |

