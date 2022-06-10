#### Tips:

+ 先看定义域!!!!!再看周期和奇偶性!!!!!
+ 反对幂三指
+ 定积分先看奇偶性
+ 根号下多项式用配方
+ 三角函数可以尝试万能公式
+ 上凸下凹

[Toc]

### 基础知识

$$
\begin{aligned}
三角形面积&:S=\frac{absin\theta}{2}(\theta为a,b两边夹角)\\
圆锥侧面积&:S=\pi rl\\
圆台侧面积&:S=\pi l(R+r)\\
椭圆面积&:S=\pi ab\\
液体压强&:P=\rho gh\\
两点间引力大小&:F=k\frac{m_1m_2}{r^2}\\
拐点&:f''(x_0)=0,且x_0左右f''(x)异号\\
球面方程&:(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=R^2\\
等比数列求和&:S_n=\frac{a_1(1-q^n)}{1-q}\\
&\sqrt[n]{n!}=+\infty
\end{aligned}
$$

##### 放缩关系

+ 四种平均数大小关系

> 平方平均数≥算数平均数≥几何平均数≥调和平均数

$$
\sqrt{\frac{a^2+b^2}{2}}\ge\frac{a+b}{2}\ge\sqrt{ab}\ge\frac{2}{\frac{1}{a}+\frac{1}{b}}\\
\sqrt{\frac{\sum_{i=1}^nx_i^2}{n}}\ge\frac{\sum_{i=1}^nx_i}{n}\ge\sum_{i=1}^n\sqrt[f_i]{\prod_{i=1}^{n} x_i^{f_i}}\ge\frac{n}{\sum_{i=1}^n\frac{1}{x_i}}
$$

+ 三角函数单位圆结论

$$
\sin x<x<\tan x
$$

##### 正弦定理和余弦定理

+ 正弦定理:

  $\forall \bigtriangleup ABC$,$a,b,c$分别为$\angle A,\angle B,\angle C$的对边,$R$为$\bigtriangleup ABC$的外接圆半径,则有
  $$
  \frac{a}{\sin\angle A}=\frac{b}{\sin\angle B}=\frac{c}{\sin\angle C}=2R
  $$

+ 余弦定理:

  $\forall \bigtriangleup ABC$,$三条边分别为a,b,c$,则有
  $$
  a^2=b^2+c^2-2bc\cos \alpha\\
  其中\alpha 为b,c的夹角
  $$

##### 三角函数
<div style="background:#cce1f3">二倍角公式:</div>

$$
\begin{aligned}
\sin 2\alpha&=2\sin\alpha\cos\alpha\\
\cos 2\alpha&=\cos^2 \alpha-\sin^2\alpha\\&=1-2\sin^2\alpha\\&=2\cos^2\alpha-1
\end{aligned}
$$
<div style="background:#cce1f3">辅助角公式:</div>

$$
a\sin x+b\cos x=\sqrt{a^2+b^2}\sin(x+\phi)\\
其中\sin\phi=\frac{b}{\sqrt{a^2+b^2}},\cos\phi=\frac{a}{\sqrt{a^2+b^2}},\tan\phi=\frac{b}{a}
$$

<div style="background:#cce1f3">两角和差的正余弦公式</div>

$$
\sin(\alpha\pm \beta)=\sin\alpha\cos\beta\pm\cos \alpha\sin\beta\\
cos(\alpha\pm\beta)=\cos\alpha\cos\beta\mp\sin\alpha\sin\beta
$$

<div style="background:#cce1f3">和差化积/积化和差</div>

$$
和差化积:\\
\sin\alpha+\sin\beta=2\sin\frac{\alpha+\beta}{2}\cos\frac{\alpha-\beta}{2}\\
\sin\alpha-\sin\beta=2\cos\frac{\alpha+\beta}{2}\sin\frac{\alpha-\beta}{2}\\
\cos\alpha+\cos\beta=2\cos\frac{\alpha+\beta}{2}\cos\frac{\alpha-\beta}{2}\\
\cos\alpha-\cos\beta=-2\sin\frac{\alpha+\beta}{2}\sin\frac{\alpha-\beta}{2}\\
积化和差:\\
\sin\alpha\cos\beta=\frac{1}{2}[\sin(\alpha+\beta)+\sin(\alpha-\beta)]\\
\cos\alpha\sin\beta=\frac{1}{2}[\sin(\alpha+\beta)-\sin(\alpha-\beta)]\\
\cos\alpha\cos\beta=\frac{1}{2}[\cos(\alpha+\beta)+\cos(\alpha-\beta)]\\
\sin\alpha\sin\beta=-\frac{1}{2}[\cos(\alpha+\beta)-\cos(\alpha-\beta)]\\
$$

<div style="background:#cce1f3">其他结论</div>

$$
\arctan x+\arctan\frac{1}{x}=\frac{\pi}{2}
$$

##### 三阶行列式计算

$$
\begin{vmatrix}
  a_1&  b_1& c_1\\
  a_2&  b_2& c_2\\
  a_3&  b_3& c_3
\end{vmatrix}=a_1b_2c_3+b_1c_2a_3+c_1a_2b_3-a_3b_2c_1-b_3c_3a_1-c_3a_2b_1
$$

$$
左对角线-右对角线
$$

##### 二项式定理

$$
(a+b)^n=C_{n}^0a^n+C_{n}^1a^{n-1}b+...+C_n^nb^n
$$

##### 欧拉公式

$$
e^{i\theta}=\cos\theta\pm i\sin\theta
$$

## 高数

### 第一章:极限/连续

##### 可积/可导/可微/连续/有界/极限存在

$$
\begin{aligned}
&定义:\\
&x_0极限存在:\\
&\qquad数列:\lim_{n\rightarrow \infty}x_n=A\Leftrightarrow \forall \varepsilon >0,\exists 正整数N,使得当n>N时就有\vert x_n-A\vert<\varepsilon\\
&\qquad函数:\lim_{n\rightarrow \infty}f(x)=A\Leftrightarrow \forall \varepsilon >0,\exists 正数X,使得当\vert x\vert>X时就有\vert f(x)-A\vert<\varepsilon\\
&x_0可导:\lim_{\Delta x\rightarrow0}\frac{\Delta y}{\Delta x}=\lim_{\Delta x\rightarrow0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}\qquad极限存在\\
&x_0连续:\lim_{x\rightarrow x0}f(x)=f(x_0)\qquad \lim_{x\rightarrow x0}[f(x_0+\Delta x)-f(x_0)]=0\\
&可积的充分条件:函数有界,在区间上连续或有有限个间断点\\
&[a,b]可积的必要条件:[a,b]有界\\
&性质:\\
&x_0极限存在:x_0左右极限均存在且相等\\
&x_0可导:x_0左右导数均存在且相等\\
&x_0连续:x_0左右均连续\qquad\lim_{x\rightarrow x0}f(x)=f(x_0)\\
&可积函数的积分一定连续\\
+&数列极限存在\Rightarrow 数列收敛,不存在\Rightarrow 数列发散\\
+&x_0可微\Leftrightarrow x_0可导\Rightarrow x_0连续\\
+&连续\Rightarrow可积(黎曼可积)/存在原函数,第一类间断点一定没有原函数,第二类间断点可能存在原函数\\
+&有界闭区间连续函数\Rightarrow有界\\
+&可积\Rightarrow有界(黎曼积分)\\
+&极限存在\Rightarrow数列有界
\end{aligned}
$$

##### 等价无穷小

$$
x\sim\sin x\sim \tan x\sim \arcsin x\sim\arctan x\sim e^x-1\sim\ln(1+x)\\
1-\cos x\sim\frac{1}{2}x^2\\
a^x-1\sim x\ln a\\
\sqrt[n]{1+x}-1\sim \frac{1}{n}x\\
(1+\beta x)^\alpha-1\sim\alpha\beta x\\
\log_a(1+x)\sim\frac{1}{\ln a}x
$$

##### 间断点

第一类间断点:$f(x_0+0)和f(x_0-0)$均存在

+ 可去间断点:$f(x_0+0)=f(x_0-0)\ne f(x_0)$或在$x=x_0$处无定义
+ 跳跃间断点:$f(x_0+0)\ne f(x_0-0)$

第二类间断点:$f(x_0+0)和f(x_0-0)$至少有一个不存在

+ 无穷间断点:$f(x_0+0)和f(x_0-0)$至少有一个为$\infty$
+ 振荡间断点

### 第二章:导数/微分

##### 函数导数

$$
\begin{aligned}
(a^x)'&=a^x\ln x\\
(\tan x)'&=\frac{1}{\cos^2 x}\\
(\cot x)'&=-\frac{1}{\sin^2x}\\
(\arcsin x)'&=\frac{1}{\sqrt{1-x^2}}\\
(\arccos x)'&=-\frac{1}{\sqrt{1-x^2}}\\
(\arctan x)'&=\frac{1}{1+x^2}\\
(\arccot x)'&=-\frac{1}{1+x^2}\\
(\int_{a}^{f(x)}g(t)dt)'&=g(f(x))f'(x)
\end{aligned}
$$

$$
[\ln(ax+b)]^{(n)}=(-1)^{n-1}(n-1)!\frac{a^n}{(ax+b)^n}
$$



洛必达的条件:
$$
f(x),g(x)在x=a的空心邻域可导,g'(x)\ne0
$$


### 第三章:积分

##### 常见不可积函数

$$
\int \frac{\sin x}{x}dx,\int \frac{\cos x}{x}dx,\int \sin x^2dx,\int \cos x^2dx\\
\int e^{ax^2},\int \frac{x^n}{\ln x}dx(n\ne1),\int \frac{\ln x}{x+a}dx(a\ne0),\\
\int \frac{e^x}{x}dx,\int (\sin x)^mdx(m\notin Z),\int \frac{1}{\sqrt{x^4+a}}dx(a\ne0)
$$

##### 一元函数积分学几何应用:

<div style="background:#cce1f3">平面图形的面积:</div>

$$
\begin{aligned}
极坐标方程:设&r_1(\theta),r_2(\theta)在[\alpha,\beta]连续,r_1(\theta)\le r_2(\theta)\qquad(\forall \theta\in[\alpha,\beta])\\
S&=\frac{1}{2}\int_\alpha^\beta [r_2^2(\theta)-r_1^2(\theta)]d\theta
\end{aligned}
$$

<div style="background:#cce1f3">旋转体体积</div>

$$
由曲线f(x),x=a,x=b及x轴所围图形绕x轴旋转一周形成的旋转体体积\\
V=\pi\int_a^b f^2(x)dx
$$

<div style="background:#cce1f3">旋转体侧面积</div>

$$
S=2\pi\int_a^b f(x)\sqrt{1+f'^2(x)}dx\\
=2\pi\int_\alpha^\beta y(t)\sqrt{x'^2(t)+y'^2(t)}dt\\
=2\pi\int_\alpha^\beta r(\theta)\sin\theta \sqrt{r^2(\theta)+r'^2(\theta)}d\theta
$$

<div style="background:#cce1f3">弧微分与弧长:</div>

$$
\begin{aligned}
直角坐标方程:y&=f(x)\qquad(a\le x\le b)\\
ds&=\sqrt{1+f'^2(x)}dx\\
s&=\int_a^b\sqrt{1+f'^2(x)}dx\qquad其中f(x)在[a,b]有连续的导数\\\\
参数方程:x&=x(t),y=y(t)\qquad(\alpha\le t\le \beta)\\
ds&=\sqrt{x'^2(t)+y'^2(t)}dt\\
s&=\int_\alpha^{\beta}\sqrt{x'^2(t)+y'^2(t)}dt\qquad其中x(t),y(t)在[\alpha,\beta]有连续的导数,x'^2(t)+y'^2(t)\ne 0\\\\
极坐标方程:r&=r(\theta)\qquad (\alpha\le \theta\le\beta)\\
则x&=r(\theta)\cos\theta,\ y=r(\theta)\sin\theta\qquad (\alpha\le \theta\le\beta)\\
ds&=\sqrt{r^2(\theta)+r'^2(\theta)}d\theta\\
s&=\int_\alpha^\beta\sqrt{r^2(\theta)+r'^2(\theta)}d\theta\qquad其中r=r(\theta)在[\alpha,\beta]有连续的导数
\end{aligned}
$$

<div style="background:#cce1f3">平面曲线的曲率和曲率半径:</div>

$$
\begin{aligned}
直角坐标方程:y&=y(x),\ 二阶可导\\
K&=\vert\frac{d\alpha}{ds}\vert=\frac{\vert y''\vert}{(1+y'^2)^{\frac{3}{2}}}\\\\
参数方程:x&=x(t),y=y(t)\qquad (t\in[\alpha,\beta])\\
K&=\vert\frac{d\alpha}{ds}\vert=\frac{\vert x'(t)y''(t)-x''(t)y'(t)\vert}{[x'^2(t)+y'^2(t)]^{\frac{3}{2}}}\\
曲率半径:\rho&=\frac{1}{K}
\end{aligned}
$$

<div style="background:#cce1f3">柱面被曲面所截面积公式</div>

$$
设有OXY平面上的光滑曲线L,以L为准线,母线平行于z轴作柱面\\
此柱面在xy平面与连续曲面z=f(x,y)(\ge 0)之间部分的面积为\\
S=\int_Lf(x,y)ds
$$

##### 一元函数积分学物理应用:

<div style="background:#cce1f3">平面曲线或平面的质心(形心):</div>

$$
平面曲线:\\
\bar{x}=\frac{M_y}{M}=\frac{1}{l}\int_0^l x(s)ds,\bar{y}=\frac{M_x}{M}=\frac{1}{l}\int_0^ly(s)ds\\
参数方程:
\bar{x}=\frac{\int_\alpha^\beta \varphi(t)\sqrt{\varphi'^2(t)+\psi'^2(t)}dt}{\int_\alpha^ \beta \sqrt{\varphi'^2(t)+\psi'^2(t)}dt}\\
\bar{y}=\frac{\int_\alpha^\beta \psi(t)\sqrt{\varphi'^2(t)+\psi'^2(t)}dt}{\int_\alpha^ \beta \sqrt{\varphi'^2(t)+\psi'^2(t)}dt}\\
平面:\\
\bar{x}=\frac{M_y}{M}=\frac{\int_a^b x[f(x)-g(x)]dx}{\int_a^b[f(x)-g(x)]dx}\\
\bar{y}=\frac{M_x}{M}=\frac{\frac{1}{2}\int_a^b[f^2(x)-g^2(x)]dx}{\int_a^b[f(x)-g(x)]dx}
$$

##### 函数积分:先看定义域,反对幂三指

$$
\begin{aligned}
\int_0^xf(t)dt&=[\int_0^x(x-t)f(t)dt]'\\
\int f(x)dx&=\int_a^xf(t)dt+C\qquad(f(x)为连续函数)
\end{aligned}
$$



<div style="background:#cce1f3">三角函数万能代换:</div>

$$
\begin{aligned}
t=\tan \frac{x}{2}\ ,\ x=2\arctan t\ ,\ dx&=\frac{2dt}{1+t^2}\\
\sin x=2\sin\frac{x}{2}\cos \frac{x}{2}=\frac{2\tan\frac{x}{2}}{\sec ^2\frac{x}{2}}&=\frac{2t}{1+t^2},\\
\cos x =\cos^2\frac{x}{2}-\sin^2\frac{x}{2}=\frac{1-\tan^2\frac{x}{2}}{\sec ^2\frac{x}{2}}&=\frac{1-t^2}{1+t^2}
\end{aligned}
$$

<div style="background:#cce1f3">三角函数代换结论:</div>

> $$
> (1)\int \frac{dx}{\sqrt[]{x^2\pm a^2} }&=\ln \vert\  x+\sqrt[]{x^2\pm a^2}\ \vert+C\\
> $$

$$
\begin{aligned}
(1)证明:令x=\frac{a}{\cos t},则\int \frac{dx}{\sqrt{x^2-a^2}}&=\int \frac{1}{\cos t}dt\\
&=\ln\vert \sec t+\tan t\vert+C_1\qquad&(见\int \sec x项)\\
&=\frac{1}{a}\ln \vert\  x+\sqrt[]{x^2- a^2}\ \vert+C_1\\
&=\ln \vert\  x+\sqrt[]{x^2\pm a^2}\ \vert+C\qquad&(C=C_1+\ln a)\\\\
\end{aligned}
$$

***

> $$
> (2)\int \sqrt[]{a^2-x^2}dx=\frac{a^2}{2}\arcsin \frac{x}{a}+\frac{x}{2}\sqrt[]{a^2-x^2}+C
> $$

$$
\begin{aligned}
(2)证明:令x=a\sin t,则\int \sqrt{a^2-x^2}dx&=a^2\int \cos ^2tdt=a^2\int \frac{\cos 2t+1}{2}dt\\
&=\frac{a^2}{2}(\frac{\sin 2t}{2}+t)+C\\
&=\frac{a^2}{2}\arcsin \frac{x}{a}+\frac{x}{2}\sqrt[]{a^2-x^2}+C\qquad(代回)\\
\end{aligned}
$$

> $$
> (3)\int \sqrt[]{x^2\pm a^2}dx=\frac{x}{2}\sqrt[]{x^2+a^2} \pm \frac{a^2}{2}\ln\vert\ x+\sqrt[]{x^2\pm a^2}\ \vert +C
> $$

$$
证明:
$$

> $$
> \int \sec x\ dx=\ln\vert \sec x+\tan x\vert+C
> $$

$$
\begin{aligned}
\int \sec x\ dx&=\int \frac{1}{\cos x}dx=\int \frac{1}{\cos ^2x}d(\sin x)=\int \frac{1}{1-\sin ^2x}d(\sin x)\ \ ,令\ t=\sin x\\
&=\int \frac{1}{1-t^2}dt=\frac{1}{2}\int (\frac{1}{1-t}+\frac{1}{1+t})dt=\frac{1}{2}\vert\ln(1+t)-\ln(1-t)\vert+C\ ,带回t=\sin x\\
&=\frac{1}{2}\ln\vert\frac{1+\sin x}{1-\sin x}\vert+C\\
&=\frac{1}{2}\ln\vert\frac{(1+\sin x)^2}{(1-\sin x)(1+\sin x)}\vert+C\\
&=\ln\vert\frac{1+\sin x}{\cos x}\vert+C\\
&=\ln\vert \sec x+\tan x\vert+C
\end{aligned}
$$

$$
\begin{aligned}
\int \arcsin x\ dx&=x\arcsin x -\int \frac{x}{\sqrt{1-x^2}}\ dx\\
&=x\arcsin x+\frac{1}{2}\int (1-x^2)^{-\frac{1}{2}}d(1-x^2)\\
&=x\arcsin x+\sqrt{1-x^2}+C\\
\int \arccos x\ dx&=x\arccos x+\int \frac{x}{\sqrt {1-x^2}}\ dx\\
&=x\arccos x-\sqrt{1-x^2}+C\\
\int \arctan x\ dx&=x\arctan x-\int \frac{x}{1+x^2}dx\\
&=x\arctan x-\frac{1}{2}\ln(1+x^2)+C
\end{aligned}
$$

> $$
> \arctan A+\arctan \frac{1}{A}=\frac{\pi}{2}\\
> $$


$$
\begin{aligned}
证明:&设\arctan A=a\ ,\ 则A=\tan a\\
&设\arctan \frac{1}{A}=b\ ,\ 则\frac{1}{A}=\tan b\\
&则\tan a*\tan b=1\Rightarrow \cos a\cos b-\sin a\sin b=0\\
&则\cos(a+b)=0\Rightarrow a+b=\frac{\pi}{2}
\end{aligned}
$$

##### 反常积分(广义积分)

> 常见的反常积分

$$
\int_a^{+\infty}\frac{dx}{x^p}=\left\{\begin{matrix} 
  收敛,p>1\\ 
  发散,p\le1
\end{matrix}\right.(a>0)\\
\int_a^{+\infty}\frac{dx}{x\ln ^px}=\left\{\begin{matrix} 
  收敛,p>1\\ 
  发散,p\le 1
\end{matrix}\right.(a>1)\\
\int_a^{+\infty}x^ke^{-\lambda x}dx=\left\{\begin{matrix} 
  收敛,\lambda>0\\ 
  发散,\lambda\le 0
\end{matrix}\right.(k\ge0)\\
\int_a^b\frac{dx}{(x-a)^p}=\left\{\begin{matrix} 
  收敛,p<1\\ 
  发散,p\ge 1
\end{matrix}\right.\\
$$

> 性质

$$
若\int_{-\infty}^{+\infty} f(x)dx收敛,则\int_{-\infty}^{+\infty}=\left\{\begin{matrix} 
  2\int_0^{+\infty}f(x)dx,f(x)为偶函数\\ 
  0,f(x)为奇函数
\end{matrix}\right.\\
收敛+收敛=收敛,收敛+发散=发散,发散+发散=不确定\\
若\int_{-\infty}^0f(x)dx和\int_0^{+\infty}f(x)dx均收敛,则\int_{-\infty}^{+\infty}f(x)dx收敛,其他情况\int_{-\infty}^{+\infty}f(x)dx均发散
$$



##### 华里士Wallis公式:三角函数幂次的积分

$(\cos x)^n$ 和$(\sin x)^n$的周期相同,$n$为奇数时周期为$2\pi$,$n$为偶数时周期为$\pi$`
$$
\int_0^{\frac{\pi}{2}}\sin ^nxdx=\int_0^{\frac{\pi}{2}}\cos^n xdx=\left\{\begin{matrix} 
  \frac{n-1}{n}\frac{n-3}{n-2}...\frac{1}{2}\cdot\frac{\pi}{2},n为正偶数\\ 
  \frac{n-1}{n}\frac{n-1}{n-2}...\frac{2}{3},n为大于1的奇数
\end{matrix}\right.\\\\
\int_0^\pi sin^nxdx=2\int_0^\frac{\pi}{2}\sin^nxdx\\
\int_0^\pi\cos^nxdx=\left\{\begin{matrix} 
  2\int_0^{\frac{\pi}{2}}\cos^n xdx,n为偶数\\ 
  0,n为奇数
\end{matrix}\right.\\
\int_0^{2\pi}\sin^nxdx=\int_0^{2\pi}\cos^nxdx=\left\{\begin{matrix} 
  4\int_0^{\frac{\pi}{2}}\sin^n xdx,n为偶数\\ 
  0,n为奇数
\end{matrix}\right.\\
\int_0^{\frac{\pi}{2}}f(\sin x)dx=\int_0^{\frac{\pi}{2}}f(\cos x)dx\\
\int_0^{\pi}f(\sin x)dx\ne\int_0^\pi f(\cos x)dx\\
\int_0^\pi xf(\sin x)dx=\frac{\pi}{2}\int_0^\pi f(\sin x)dx=\pi\int_0^{\frac{\pi}{2}}f(\sin x)dx
$$


### 第四章:微分中值定理

<div style="background:#cce1f3">罗尔(中值)定理</div>

> [https://baike.baidu.com/item/%E7%BD%97%E5%B0%94%E4%B8%AD%E5%80%BC%E5%AE%9A%E7%90%86/1876399?fromtitle=%E7%BD%97%E5%B0%94%E5%AE%9A%E7%90%86&fromid=7253372&fr=aladdin]

如果 $R$ 上的函数$f(x)$ 满足以下条件：

1. 在闭区间 $[a,b]$上连续，
2. 在开区间$(a,b)$ 内可导，
3. $f(a)=f(b)$

则至少存在一个 $ξ∈(a,b)$，使得$f'(ξ)=0$。

<div style="background:#cce1f3">拉格朗日中值定理</div>

>  设$f(x)$在$[a,b]$上连续,在$(a,b)$内可导,则$\exists ξ\in (a,b)$使得

$$
f(b)-f(a)=f'(ξ)(b-a)
$$


<div style="background:#cce1f3">柯西中值定理</div>

> 设$f(x),g(x)$在$[a,b]$上连续,在$(a,b)$内可导,且$g'(x)\ne 0$,则$\exists ξ\in (a,b)$使得

$$
\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(ξ)}{g'(ξ)}
$$

##### 驻点/极值点和拐点

+ 驻点:函数的一阶导数为0的点
+ 极值点:
  + 必要条件:$f'(x)=0或f'(x)$不存在
  + 

+ 拐点:函数二阶导数为0且三阶导数不为0的点
  + 必要条件:$f''(x)=0$

  + 求法:
    + $求f''(x)$
    + 令$f''(x)=0$,求出此方程在区间内的实根,并且找出区间内$f''(x)$不存在的点
    + 对于上述每一个点$x_0$,检查$f''(x_0)$左右两侧的符号,若相反,则$x_0$是拐点


##### 凹凸性

+ 定义: 设$f(x)$在$[a,b]$上连续,在$(a,b)$内可导,若对$\forall x,x_0\in (a,b)$且$x\ne x_0$恒有
  $$
  f(x_0)+f'(x_0)(x-x_0)>(<)f(x)
  $$
  则称$f(x)$在$[a,b]$上是**凸(凹)**的

+ 几何意义:若$y=f(x)$在任意点处的切线处该点外总在曲线上方.则该曲线是凸的

+ 充要条件: $f(x)$是凸函数的充要条件为$f'(x)$是单调减函数

+ 求凹凸性区间:

  + 求出$f''(x)=0和f''(x)$不存在的所有点
  + 按顺序将区间分为若干个不相交的子区间,讨论$f''(x)$在每个子区间上的符号
  + 一般用列表法

##### 渐近线

求$y=f(x)$的渐近线的方法
$$
1.x=a是垂直渐近线\Leftrightarrow \lim_{x\to a^+}f(x)=\infty或\lim_{x\to a^-}f(x)=\infty\\
2.当x\to+\infty时y=b是水平渐近线\Leftrightarrow \lim_{x\to+\infty}=b\\
3.当x\to+\infty时y=kx+b(k\ne0)是斜渐近线\Leftrightarrow \lim_{x\to+\infty}\frac{f(x)}{x}=k\ne0且\lim_{x\to+\infty}[f(x)-kx]=b\\
把2,3中的x\to+\infty换为x\to-\infty可得曲线f(x)当x\to-\infty时的水平或斜渐近线
$$

> 总结
> $$
> 1.求间断点x_0,验证极限是否为\infty,是则x=x_0为竖直渐近线\\
> 2.求\lim_{x\to\pm\infty}f(x)得到水平渐近线\\
> 3.求\lim_{x\to\infty}\frac{f(x)}{x},求出k,带回求b\\
> 其中2.和3.中的极限最多存在一个
> $$


### 第五章:泰勒公式

##### 一元皮亚诺/拉格朗日定义:

<div style="background:#cce1f3">带皮亚诺余项的n阶泰勒公式</div>

$$
\begin{aligned}
设f(x)在x=x_0处具有n阶导数,则\\
f(x)&=T_n(x)+R_n(x)\\
其中\quad x=x_0的n次泰勒多项式\quad T_n(x)&=f(x_0)+f'(x_0)(x-x_0)+...+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n\\
x=x_0处的n阶皮亚诺余项\quad R_n(x)&=o((x-x_0^n))\quad (x \rightarrow x_0),即\lim_{x\rightarrow x_0}\frac{R_n(x)}{(x-x_0)^n}=0
\end{aligned}
$$

<div style="background:#cce1f3">带拉格朗日余项的n阶泰勒公式</div>

$$
\begin{aligned}
设f(x)在包含x_0的区间(a,b)内有n+1&阶导数,在区间[a,b]上有n阶连续导数,则\forall x\in [a,b],有\\
f(x)&=T_n(x)+R_n(x)\\
其中\quad [a,b]上拉格朗日余项的n阶泰勒公式\quad T_n(x)&同皮亚诺余项\\
x=x_0处的n阶拉格朗日余项\quad R_n(x)&=\frac{1}{(n+1)!}f^{(n+1)}(\xi )(x-x_0)^{n+1}\\
\xi 在x和x_0中间,也可以表示为\xi &=x_0+\theta(x-x_0)\quad 0<\theta<1\\
***\quad n=0时,f(x)即为\textbf{拉格朗日中值}定理
\end{aligned}
$$

> 当$n=0$时上面两定理又称之为带皮亚诺余项与带拉格朗日余项的**麦克劳林公式**

### 第六章:常微分方程

<div style="background:#cce1f3">变量可分离的方程</div>

$$
y'=f(x)g(y)\\
同除g(y),分离变量,则\int \frac{dy}{g(y)}=\int f(x)dx +C
$$

<div style="background:#cce1f3">一阶线性方程</div>

$$
\begin{aligned}
形如\ y'&=p(x)y+q(x)\\
q(x)=0时,方程y'&=p(x)y为一阶线性齐次方程\\
通解:y&=Ce^{\int p(x)dx},
证明:两边同时积分\\
>>>**注释:若通解中出现&\ln\vert g(x)\vert,可以去掉绝对值\\\\
q(x)\ne 0时,方程&为一阶线性非齐次方程\\
通解:y&=e^{\int p(x)dx}[C+\int q(x)e^{- \int p(x)dx}dx] \\
证明:&常数变易法
\end{aligned}
$$

<div style="background:#cce1f3">齐次方程</div>

$$
形如y'=f(\frac{y}{x})\\
令u=\frac{y}{x},则y=ux\Rightarrow y'=u+xu'\\
原方程化为\quad xu'=f(u)-u
$$

<div style="background:#cce1f3">伯努利方程</div>

$$
形如y'=p(x)y+y^\lambda q(x)\qquad(\lambda\ne 0,1)\\
\begin{aligned}
\Rightarrow \quad&y^{-\lambda}y'=p(x)y^{1-\lambda}+q(x)\\
\Rightarrow \quad&\frac{1}{1-\lambda}(y^{1-\lambda})'=p(x)y^{1-\lambda}+q(x)\\
\Rightarrow \quad&(y^{1-\lambda})'=(1-\lambda)p(x)y^{1-\lambda}+(1-\lambda)q(x)\quad (变成一阶方程,获得新p(x)和q(x))\\
\Rightarrow \quad&通解:y^{1-\lambda}=e^{(1-\lambda)\int p(x)dx}[C+(1-\lambda)\int q(x)e^{-(1-\lambda)\int p(x)dx}dx]
\end{aligned}
$$

##### 可降阶的高阶方程:

<div style="background:#cce1f3">可降阶的高阶方程</div>

$$
形如F(x,y^{(n)},y^{(n+1)})=0\\
设y^{(n)}=u,方程转化为一阶方程F(x,u,u')=0
$$

$$
形如F(y,y',y'')=0\\
设y'=u=\frac{dy}{dx},\\
则y''=\frac{du}{dx}=\frac{du}{dy}\cdot \frac{dy}{dx}=u\frac{du}{dy}\\
方程化为一阶方程F(y,u,u\frac{du}{dy})=0
$$

##### 常系数微分方程

 <div style="background:#cce1f3">常系数齐次线性微分方程</div>

$$
y^{(n)}+a_{n-1}y^{(n-1)}+\cdot\cdot\cdot\ +a_1y'+a_0y=0\\
设其解为y=e^{\lambda x},带入并消去e^{\lambda x}可得\\特征方程:\\
\Rightarrow \quad\lambda^n+a_{n-1}\lambda^{n-1}+\cdot\cdot\cdot\ +a_1\lambda+a_0=0\\
此方程的根称为原方程的特征根\\\\
\begin{aligned}
1) &如果\lambda是单实特征根,则y=e^{\lambda x}\\
2) &如果\lambda是k重实特征根,则方程基础解系中对应的k个解\\
&y_1=e^{\lambda x},y_2=xe^{\lambda x},...,y_k=x^{k-1}e^{\lambda x}\\
3) &如果\lambda=\alpha\pm i\beta是单复特征根,则方程基础解系中对应的2个解\\
&y_1=e^{\alpha x}\cos\beta x,y_2=e^{\alpha x}\sin\beta x\\
4) &如果\lambda=\alpha\pm i\beta是k重复特征根,则方程基础解系中对应的2k个解\\
&y_1=e^{\alpha x}\cos\beta x,y_2=e^{\alpha x}\sin\beta x\\
&\qquad xe^{\alpha x}\cos\beta x,\qquad xe^{\alpha x}\sin\beta x\\
&\qquad\qquad ...\qquad\qquad\qquad ...\\
&\quad x^{k-1}e^{\alpha x}\cos\beta x, \quad x^{k-1}e^{\alpha x}\sin\beta x\\
\end{aligned}
$$

 <div style="background:#cce1f3">常系数非齐次线性微分方程</div>

$$
y^{(n)}+a_{n-1}y^{(n-1)}+\cdot\cdot\cdot\ +a_1y'+a_0y=f(x)\\
\begin{aligned}
1)& 当f(x)=P_n(x)=a_nx^n+a_{n-1}x^{n-1}+...+a_1x+a_0\\
&设y^*=x^kQ_n(x),k是0为方程特征根的重数\\
2)& 当f(x)=P_n(x)e^{\alpha x},设y^*=x^kQ_n(x)e^{\alpha x}\\
&k是\alpha为方程特征根重数\\ ***\ 
3)& 一般形式:f(x)=e^{\alpha x}[P_n(x)\cos\beta x+Q_m(x)\sin\beta x]\\
&设y^*=x^ke^{\alpha x}[P_t(x)\cos\beta x+Q_t(x)\sin\beta x]\\
&k为\alpha\pm i\beta是方程特征根的重数,t=\max\{m,n\}
\end{aligned}
$$

 <div style="background:#cce1f3">欧拉方程</div>

$$
x^ny^{(n)}+a_{n-1}x^{n-1}y^{(n-1)}+...+a_1xy'+a_0y=f(x)\\
令x=e^t,\frac{dt}{dx}=\frac{1}{x},D=\frac{d}{dt}\\
\Rightarrow \quad x^ny^{(n)}=D(D-1)...(D-n+1)y\\
带入原方程使其转换为\textbf{常系数非齐次线性微分方程}
$$

> 举例:求方程$x^2y''+4xy'+2y=\frac{1}{x}$的通解
>
> 令$x=e^t$,原方程化为$[D(D-1)+4D+2]y=e^{-t}\Rightarrow [D^2+3D+2]y=e^{-t}$
>
> 特征方程$\lambda^2+3\lambda+2=0,特征根\lambda_1=-1,\lambda_2=-2$
>
> 设特解$y^*=ate^{-t},(y^*)'=ae^{-t}-ate^{-t},(y^*)''=-2ae^{-t}+ate^{-t}$
>
> 带入方程解出$a=1$,则特解$y^*=te^{-t}$
>
> 通解$y=C_1e^{-t}+C_2e^{-2t}+te^{-t}$

### 第七章:向量代数与空间解析几何

##### 混合积性质

$$
\left\{\begin{matrix} 
  (\vec a,\vec b,\vec c)=(\vec b,\vec c,\vec a)=(\vec c,\vec a,\vec b)\\  
  (\vec a,\vec b,\vec c)=-(\vec b,\vec a,\vec c)
\end{matrix}\right.\\
$$

##### 定义:平面

<div style="background:#cce1f3">平面的一般方程</div>

$$
Ax+By+Cz+D=0\\
法向量\vec n=\{A,B,C\}
$$

<div style="background:#cce1f3">平面的点法式方程</div>

$$
A(x-x_0)+B(y-y_0)+C(z-z_0)=0\\
法向量\vec n=\{A,B,C\}
$$

<div style="background:#cce1f3">平面的截距式方程</div>

$$
\frac{x}{a}+\frac{y}{b}+\frac{z}{c}=1
$$



<div style="background:#cce1f3">平面的参数方程</div>

$$
\left\{\begin{matrix} 
  x=X_1t_1+X_2t_2+x_0\\  
  y=Y_1t_1+Y_2t_2+y_0\\
  z=Z_1t_1+Z_2t_2+z_0
\end{matrix}\right.\\
$$

<div style="background:#cce1f3">平面的向量方程</div>

$$
\vec{OP}-\vec{OM}=t_1U_1+t_2U_2,\quad P是平面\Pi上任意一点
$$

##### 定义:直线

<div style="background:#cce1f3">直线的一般方程</div>

$$
\left\{\begin{matrix} 
  A_1x+B_1y+C_1z+D_1=0 \\  
  A_2x+B_2y+C_2z+D_2=0
\end{matrix}\right.\\
法向量分别为\vec{n_1}=\{A_1,B_1,C_1\},\ \vec{n_2}=\{A_2,B_2,C_2\}\\
\vec{n_1}和\vec{n_2}不平行\\
方向向量\quad \vec{S}=\begin{vmatrix}
  \vec i&  \vec j& \vec k\\
  A_1&  B_1& C_1\\
  A_2&  B_2& C_2
\end{vmatrix}
$$

<div style="background:#cce1f3">直线的参数方程</div>

$$
\left\{\begin{matrix} 
  x=x_0+ka \\  
  y=y_0+kb\\
  z=z_0+kc
\end{matrix}\right.\\
方向向量\quad \vec{S}=\{a,b,c\}
$$

<div style="background:#cce1f3">直线的标准方程</div>

$$
\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}\\
方向向量\quad \vec{S}=\{a,b,c\}
$$

##### 求平面方程

$$
已知平面上一点M_0(x_0,y_0,z_0)和法向量\vec{n}=\{A,B,C\}\\
点法式\quad A(x-x_0)+B(y-y_0)+C(z-z_0)=0
$$

$$
已知平面上一点M(x_0,y_0,z_0),以及与平面平行的两个不共线的向量\\
\vec{U_1}=\{X_1,Y_1,Z_1\},\quad \vec{U_2}=\{X_2,Y_2,Z_2\}\\
则平面方程为\quad \begin{vmatrix}
  x-x_0&  y-y_0& z-z_0\\
  X_1&  Y_1& Z_1\\
  X_2&  Y_2& Z_2
\end{vmatrix}=0
$$

##### 求直线方程

$$
求两个平面方程,联立即为直线方程\\
形如\left\{\begin{matrix} 
  A_1x+B_1y+C_1z+D_1=0 \\  
  A_2x+B_2y+C_2z+D_2=0
\end{matrix}\right.
$$

$$
已知直线上一点和直线的方向向量S=\{l,m,n\},用参数式或标准式方程即可\\
形如\frac{x-x_0}{l}=\frac{y-y_0}{m}=\frac{z-z_0}{n}\\
或者\left\{\begin{matrix} 
  x=x_0+tl \\  
  y=y_0+tm\\
  z=z_0+tn
\end{matrix}\right.\\
$$



#### 距离类

***

##### 点到直线距离

$$
点P_0(x_0,y_0,z_0),\ 直线L:\frac{x-x_1}{l}=\frac{y-y_1}{m}=\frac{z-z_1}{n}\\
则L上定点P_1(x_1,y_1,z_1),L有方向向量\vec{S}=\{l,m,n\}\\
d=\vert\vec{P_0P_1}\vert\sin<\vec{P_0P_1},S>=\frac{\vert\vec{P_0P_1}\cp S\vert}{\vert S\vert}
$$



##### 点到平面距离

$$
平面方程:Ax+By+Cz+D=0,\ 点P(x_1,y_1,z_1)为平面外一点\\
d=\frac{\vert Ax_1+By_1+Cz_1+D\vert}{\sqrt{A^2+B^2+C^2}}
$$



#### 夹角类

***

##### 两平面的夹角

$$
即为两个平面法向量\vec{n_1}和\vec{n_2}的夹角\theta\quad(0\le\theta\le 90°)\\
\cos\theta=\frac{\vert\vec{n_1}\cdot\vec{n_2}\vert}{\vert\vec{n_1}\vert\vert\vec{n_2}\vert}
$$

##### 两直线的夹角

$$
即为两个方向向量\vec{S_1}和\vec{S_2}的夹角\theta\quad(0\le\theta\le 90°)\\
\cos\theta=\frac{\vert\vec{S_1}\cdot\vec{S_2}\vert}{\vert\vec{S_1}\vert\vert\vec{S_2}\vert}
$$

##### 直线与平面的夹角

$$
即为[\frac{\pi}{2}-直线方向向量\vec{S}与平面法向量\vec{n}的夹角]\\
\sin\theta=\frac{\vert\vec{S}\cdot\vec{n}\vert}{\vert\vec{S}\vert\vert\vec{n}\vert}
$$

#### 旋转曲面与柱面

##### 旋转曲面方程

> 求$\left\{\begin{matrix} 
>   f(x,y)=0 \\  
>   z=0
> \end{matrix}\right.\\$绕$x$轴旋转所得的旋转曲面方程

绕哪个轴,哪个轴不动

$y=\pm\sqrt{y^2+z^2}$

得到旋转曲面方程$F(x,\pm\sqrt{y^2+z^2})=0$

> 参数形式:求$\left\{\begin{matrix} 
>   x=f(t) \\  
>   y=g(t)\\z=h(t)
> \end{matrix}\right.\\$绕$z$轴旋转所得的旋转曲面方程

$$
\left\{\begin{matrix} 
  x=\sqrt{f^2(t)+g^2(t)}\cos\theta \\  
  y=\sqrt{f^2(t)+g^2(t)}\sin\theta\\
  z=h(t)
\end{matrix}\right.\\
$$

#### 投影问题TODO



#### 常用技巧

$$
\vec{\alpha},\vec\beta是平面\Pi上两个不平行的向量,则该平面上的任一向量可用\\
\vec{s}=x\vec\alpha+y\vec\beta\qquad 表示
$$

##### 克莱姆法则

对三元一次方程组
$$
\left\{\begin{matrix} 
  a_{11}x_1+a_{12}x_2+a_{13}x_3=b_1 \\  
  a_{21}x_1+a_{22}x_2+a_{23}x_3=b_2\\
  a_{31}x_1+a_{32}x_2+a_{33}x_3=b_3
\end{matrix}\right.\\
如记\alpha_1=\{a_{11},a_{21},a_{31}\},\alpha_2=\{a_{12},a_{22},a_{32}\},\alpha_3=\{a_{13},a_{23},a_{33}\},\beta=\{b_{1},b_{2},b_{3}\}\\
则方程组可改写为x_1\alpha_1+x_2 \alpha_2+x_3\alpha_3=\beta\\
因为\alpha_2\cp\alpha_3与\alpha_2,\alpha_3都垂直,用\alpha_2\times\alpha_3对上式两端做点积,有\\
x_1(\alpha_1,\alpha_2,\alpha_3)=(\beta,\alpha_2,\alpha_3)\\
当(\alpha_1,\alpha_2,\alpha_3)\ne0时,x_1=\frac{(\beta,\alpha_2,\alpha_3)}{(\alpha_1,\alpha_2,\alpha_3)}=\frac{D_{x_1}}{D}\\
类似地,x_2=\frac{(\alpha_1,\beta,\alpha_3)}{(\alpha_1,\alpha_2,\alpha_3)}=\frac{D_{x_2}}{D},x_3=\frac{(\alpha_1,\alpha_2,\beta)}{(\alpha_1,\alpha_2,\alpha_3)}=\frac{D_{x_3}}{D}\\
$$

>  若系数行列式$D\ne0$,则方程组有唯一解,若还为齐次线性方程组,则方程组只有零解

