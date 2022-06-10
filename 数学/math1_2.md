[TOC]

### 第八章:多元函数微分学

#### 性质

$$
两个偏导存在且连续\Rightarrow 可微
\\可微\Rightarrow 函数连续\\
可微\Rightarrow 偏导存在\\
其余关系均不正确
$$

> 定义判定$f(x,y)$在$(x_0,y_0)$ 是否可微
> $$
> 1. 定义判定偏导是否存在,存在进行下一步,否则不可微\\
> 2. 考察极限\lim_{(\Delta x,\Delta y)\to (0,0)}\frac{f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0)-f'_x(x_0,y_0)\Delta x-f'_y(x_0,y_0)\Delta y}{\rho}\\
> 若上式为0则可微,否则不可微
> $$
> 

##### 复合函数二阶偏导数

$$
\begin{aligned}
z=f(x,y),u&=\varphi (x,y),v=\psi(x,y),求z=f(u,v)对x的1和2阶偏导\\
一阶:\qquad\frac{\partial z}{\partial x}&=f_1^{'}\frac{\partial \varphi}{\partial x}+f_2^{'}\frac{\partial \psi}{\partial x}\\
二阶:\qquad\frac{\partial ^2z}{\partial x^2}&=
\frac{\partial }{\partial x}(f_1^{'})\frac{\partial \varphi}{\partial x}+f_1^{'}\frac{\partial ^2\varphi}{\partial x^2}+
\frac{\partial }{\partial x}(f_2^{'})\frac{\partial \psi}{\partial x}+f_2^{'}\frac{\partial ^2\psi}{\partial x^2}\\
&其中\ 
\left\{\begin{matrix} 
\frac{\partial }{\partial x}(f_1^{'})&=(f_{11}^{''}\frac{\partial \varphi}{\partial x}+f_{12}^{''}\frac{\partial \psi}{\partial x})\\
\frac{\partial }{\partial x}(f_2^{'})&=(f_{21}^{''}\frac{\partial \varphi}{\partial x}+f_{22}^{''}\frac{\partial \psi}{\partial x})
\end{matrix}\right.\\
\end{aligned}
$$

##### 隐函数求导法

如果二元函数$F(x,y)$=0满足

+ 函数$F(x,y)$在点$(x_0,y_0)$某邻域内有连续的偏导数
+ $F(x_0,y_0)=0$
+ $F'_y(x_0,y_0)\ne0$

则方程$F(x,y)=0$在点$(x_0,y_0)$某邻域能唯一确定一个连续函数$y=y(x)$,它满足$y_0=y(x_0)$,并有连续的导数,且
$$
y'=\frac{dy}{dx}=-\frac{F_x'}{F_y'}
$$
**推广**:如果三元方程$F(x,y,z)=0$满足如下三个条件

+ 函数$F(x,y,z)$在点$(x_0,y_0,z_0)$某邻域有连续偏导数
+ $F(x_0,y_0,z_0)=0$
+ $F_z'(x_0,y_0,z_0)\ne0$

则方程$F(x,y,z)=0$在点$(x_0,y_0,z_0)$某邻域能唯一确定一个连续函数$z=z(x,y)$,它满足$z_0=z(x_0,y_0)$,并有连续的导数,且
$$
\frac{\partial z}{\partial x}=-\frac{F_x'}{F_z'}\ ,\qquad \frac{\partial z}{\partial y}=-\frac{F_y'}{F_z'}
$$

$$
n个方程,m个变量组成方程组(m>n)能确定n个m-n元函数
$$

##### 拉普拉斯方程

$$
\frac{\partial ^2u}{\partial x^2}+\frac{\partial ^2u}{\partial y^2}=0\\
在极坐标变换x=r\cos\theta,y=r\sin\theta下,转化为\\
\frac{\partial ^2u}{\partial r^2}+\frac{1}{r}\frac{\partial u}{\partial r}+\frac{1}{r^2}\frac{\partial ^2u}{\partial \theta^2}=0
$$



##### 空间曲线定义& 性质

<div style="background:#cce1f3">参数方程</div>

$$
设l:\left\{\begin{matrix} 
  x=x(t) \\  
  y=y(t)\\
  z=z(t)
\end{matrix}\right.为一空间曲线,M_0为曲线上t=t_0的点\\
则l上M_0点的切线:\quad \frac{x-x_0}{x'(t_0)}=\frac{y-y_0}{y'(t_0)}=\frac{z-z_0}{z'(t_0)}\\
\vec{l}=(x'(t_0),y'(t_0),z'(t_0))为M_0点处的切向量,方向指向参数增加的方向\\
称过M_0点与切线垂直的平面为其法平面,方程为\\x'(t_0)(x-x_0)+y'(t_0)(y-y_0)+z'(t_0)(z-z_0)=0
$$

> 可以把$x$看做$x,y,z$的参数,则切向量变为$(1,y_x',z_x')$

<div style="background:#cce1f3">交面式方程</div>

$$
S:\left\{\begin{matrix} 
 F(x,y,z)=0\\
 G(x,y,z)=0
\end{matrix}\right.,M_0(x_0,y_0,z_0)是S上一点\\
则两个曲面在M_0的法向量分别为\\
\vec{n_1}=\{F'x,F'y,F'z\}|_{(x_0,y_0,z_0)},\vec{n_2}=\{G'x,G'y,G'z\}|_{(x_0,y_0,z_0)}\\
切线的方向向量为\vec{l}=\vec{n_1}\cp \vec{n_2}=\begin{vmatrix}
  i&  j& k\\
  F'x(M_0)&  F'y(M_0)&F'z(M_0) \\
  G'x(M_0)&  G'y(M_0)&G'z(M_0)\end{vmatrix}=\{a,b,c\}\\
则切线方程\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}\\
法平面方程a(x-x_0)+b(y-y_0)+c(z-z_0)=0
$$

##### 曲面的切平面和法线

$$
设S:F(x,y,z)=0为一曲面,M_0(x_0,y_0,z_0)为曲面上一点\\
M_0点的法向量\vec{n}=(F_x',F_y',F_z')\\
切平面方程为\quad (x-x_0)F_x'+(y-y_0)F_y'+(z-z_0)F_z'=0\\
法线方程为\quad \frac{x-x_0}{F_x'}=\frac{y-y_0}{F_y'}=\frac{z-z_0}{F_z'}
$$

##### 多元函数泰勒公式

$$
f(x,y)在(x_0,y_0)点处的n阶Taylor公式:\\
\begin{aligned}
f(x_0+\Delta x,y_0+\Delta y)&=f(x_0,y_0)+\frac{1}{1!}(\Delta x\frac{\partial}{\partial x}+\Delta y\frac{\partial}{\partial y})f(x_0,y_0)\\
&+\frac{1}{2!}(\Delta x\frac{\partial}{\partial x}+\Delta y\frac{\partial}{\partial y})^2f(x_0,y_0)+...\\
&+\frac{1}{n!}(\Delta x\frac{\partial}{\partial x}+\Delta y\frac{\partial}{\partial y})^{n}f(x_0,y_0)\\
&+\frac{1}{(n+1)!}(\Delta x\frac{\partial}{\partial x}+\Delta y\frac{\partial}{\partial y})^{n+1}f(x_0+\theta\Delta x,y_0+\theta\Delta y)\\
\end{aligned}\\
\theta \in (0,1)
$$

#### 极值问题

驻点:
$$
同时使f_x'(x,y)=0和f_y'(x,y)=0成立的点称为驻点
$$

##### 极值点:

$$
必要条件:驻点(邻域连续二阶偏导)\\
充分条件:f_x'(x_0,y_0)=0,f_y'(x_0,y_0)=0\\
\&\quad f_{xx}''(x_0,y_0)=A,f_{xy}''(x_0,y_0)=B,f_{yy}''(x_0,y_0)=C\\
1) B^2-AC<0时,f(x,y)在(x_0,y_0)取极值,且当A>0时取极小值,A<0时取极大值\\
2) B^2-AC>0时,(x_0,y_0)不是f(x,y)的极值点\\
3) B^2-AC=0时,f(x_0,y_0)不一定取极值,需另外讨论(一般用极值定义)
$$

##### 条件极值:拉格朗日乘数法

> 求函数$z=f(x,y)$在条件$\varphi (x,y)=0$下的最大值或最小值

$$
构造辅助函数F(x,y,\lambda)=f(x,y)+\lambda\varphi(x,y)\\
然后求解方程组\left\{\begin{matrix} 
  \frac{\partial F}{\partial x}= \frac{\partial f}{\partial x}+\lambda\frac{\partial \varphi}{\partial x}=0\\  
  \frac{\partial F}{\partial y}= \frac{\partial f}{\partial y}+\lambda\frac{\partial \varphi}{\partial y}=0\\
  \frac{\partial F}{\partial \lambda}= \varphi(x,y)=0
\end{matrix}\right.\\
所有满足此方程的解(x,y,\lambda)中(x,y)是f(x,y)在条件\varphi(x,y)=0下的可能的极值点\\
最后比较这些可能极值点(可能还有端点)的函数值求出最大最小值
$$

##### 方向导数

<div style="background:#cce1f3">方向余弦</div>

$$
\vec{l}=(a,b,c)\\
方向余弦为\cos\alpha=\frac{a}{\sqrt{a^2+b^2+c^2}},\cos\beta=\frac{b}{\sqrt{a^2+b^2+c^2}},\cos\gamma=\frac{c}{\sqrt{a^2+b^2+c^2}}\\
$$

<div style="background:#cce1f3">方向导数</div>

$$
数量场u=f(x,y,z)在P_0(x_0,y_0,z_0)上可微,则其沿任何方向\vec{l}=(\cos\alpha,\cos\beta,\cos\gamma)的方向导数均存在,且\\
\frac{\partial u}{\partial \vec{l}}|_{P_0}=f_x'(x_0,y_0,z_0)\cos\alpha+f_y'(x_0,y_0,z_0)\cos\beta+f_z'(x_0,y_0,z_0)\cos\gamma
$$

> 可微$\Rightarrow$方向导数存在, 其余均不成立$(可见P_{209})$

##### 梯度

$$
梯度是一个向量,它的方向是函数在该点的方向导数最大的方向,它的模是最大方向导数的值\\
\grad u|_{(x_0,y_0,z_0)}=(\frac{\partial u}{\partial x},\frac{\partial u}{\partial y},\frac{\partial u}{\partial z})|_{(x_0,y_0,z_0)}\\
梯度\grad u|_{P_0}垂直于P_0点的等值面
$$

### 第九章:多元函数积分

#### 二重积分

<div style="background:#cce1f3">极坐标</div>

> 一般使用情况
>
> 1. 积分区域为圆或圆环或扇形
> 2. 被积函数为$f(x^2+y^2),f(\frac{x}{y})$,可以消去其中一个变量

$$
\iint_D f(x,y)dxdy,\qquad dxdy=rd\theta dr\\
设D是OXY平面上有界闭区域,f(x,y)是D上连续函数\\
可积区域\left\{\begin{matrix} 
  a\le\ \theta\le\beta\\  
  \varphi(\theta)\le r\le\psi(\theta)
\end{matrix}\right.\\
则\iint_D f(x,y)dxdy=\int_\alpha^\beta d\theta\int_{\varphi(\theta)}^{\psi(\theta)}f(r\cos\theta,r\sin \theta)rdr
$$

<div style="background:#cce1f3">对称性</div>

$$
若D关于y=x对称,则\iint_D f(x,y)dxdy=\iint_Df(y,x)dxdy
$$

> 例:求$\int_0^{+\infin}e^{-x^2}dx$
> $$
> \begin{aligned}
> 原式&=(\int_0^{+\infin}e^{-x^2}dx\int_0^{+\infin}e^{-x^2}dx)^{\frac{1}{2}}\\
> &=(\int_0^{+\infin}e^{-x^2}dx\int_0^{+\infin}e^{-y^2}dy)^{\frac{1}{2}}\\
> &=(\iint_{0\le x\le+\infin}e^{-(x^2+y^2)}dxdy)^{\frac{1}{2}}\\
> &=(\int_0^{\frac{\pi}{2}}d\theta\int_0^{+\infin}e^{-r^2}\cdot rdr)^{\frac{1}{2}}\\
> &=\frac{\sqrt{\pi}}{2}
> \end{aligned}
> $$

<div style="background:#cce1f3">二重积分的换元法</div>

$$
x=x(u,v),y=y(u,v)均有一阶偏导\\
J(u,v)=\begin{vmatrix}
  \frac{\partial x}{\partial u}&\frac{\partial x}{\partial v} \\
  \frac{\partial y}{\partial u}&\frac{\partial y}{\partial v}
\end{vmatrix}\ne0\\
(雅可比行列式在几个点或一条线上为0,下式仍成立)\\
区域D到D'为双射\\
则\iint f(x,y)dxdy=\iint f(x(u,v),y(u,v))|J(u,v)|dudv
$$

> 例题1:
> $$
> 求x+y=c,x+y=d,y=ax,y=bx\quad (0<c<d,0<a<b)围成的面积\\
> 令u=x+y,v=\frac{y}{x},则c\le u\le d,a\le v\le b\\
> S=\int_a^bdv\int_c^dJ(u,v)du=\int_a^bdv\int_c^d\frac{u}{(1+v)^2}du\\=\int_a^b\frac{1}{(1+v)^2}dv\int_c^dudu
> $$
> 例题2:
> $$
> D:\frac{x^2}{a^2}+\frac{y^2}{b^2}=1,求\iint_D\sqrt{1-\frac{x^2}{a^2}-\frac{y^2}{b^2}}dxdy\\
> 令x=a\rho\cos\theta,y=b\rho\sin\theta,则D':\rho=1\\
> 原式=\int_0^{2\pi}d\theta\int_0^1\sqrt{1-\rho^2}J(\rho,\theta)d\rho=\int_0^{2\pi}d\theta\int_0^1\sqrt{1-\rho^2}ab\rho d\rho=\frac{2}{3}\pi ab
> $$

#### 三重积分

<div style="background:#cce1f3">柱形域</div>

$$
\left\{\begin{matrix} 
  \varphi(x,y)\le z\le\psi(x,y) \\  
  (x,y)\in D_{xy}
\end{matrix}\right.\\
\iiint_\Omega f(x,y,z)dxdydz=\iint_{D_{xy}}dxdy\int_{\varphi(x,y)}^{\psi(x,y)}f(x,y,z)dz\\
$$

<div style="background:#cce1f3">片形域</div>

$$
\left\{\begin{matrix} 
  a\le z\le b \\  
  (x,y)\in D_{z}
\end{matrix}\right.\\
\iiint_\Omega f(x,y,z)dxdydz=\int_a^bdz\iint_{D_z}f(x,y,z)dxdy\\
$$

<div style="background:#cce1f3">轮换对称性</div>

$$
若\Omega关于x,y,z具有轮换对称性,则\\
\iiint_\Omega f(x,y,z)d\Omega=\iiint_\Omega f(y,z,x)d\Omega=\iiint_\Omega f(z,x,y)d\Omega
$$

##### 球坐标

$$
(x,y,z)\longrightarrow (\rho,\theta,\phi)\\
\begin{aligned}
\rho&=c:表示以c为半径的球面\\
\phi&=c:表示与oz轴正向夹角位\phi的锥面\\
\theta&= c:表示与ox轴正向夹角位\theta的半平面\\
\end{aligned}\\
转换公式:\left\{\begin{matrix} 
  x=\rho\sin\phi\cos\theta \\  
  y=\rho\sin\phi\sin\theta\\
  z=\rho\cos\phi
\end{matrix}\right.\qquad\quad 其中:\left\{\begin{matrix} 
  \rho\ge0 \\  
  0\le \theta \le 2\pi\\
  0\le\phi\le\pi
\end{matrix}\right.\\
则x^2+y^2+z^2=\rho^2\\
dxdydz=\rho^2\sin\phi\ \cdot d\theta d\phi d\rho\\
若\left\{\begin{matrix} 
  a\le\theta\le b\\  
  c\le \phi \le d\\
  g(\theta,\phi)\le\rho\le h(\theta,\phi)
\end{matrix}\right.\\
则\iiint_\Omega f(x,y,z)dxdydz=\int_a^bd\theta\int_c^dd\phi\int_{g(\theta,\phi)}^{h(\theta,\phi)}f(\rho\sin\phi\cos\theta,\rho\sin\phi\sin\theta,\rho\cos\phi)\cdot\rho^2\sin\phi d\rho
$$

 <img width =300px src='C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220320200837566.png'>

#### 第一型积分

 <div style="background:#cce1f3">第一型曲线积分</div>

> 类似于弧微分/弧长部分

$$
1. 若曲线C:\left\{\begin{matrix} 
  x=x(t)\\  
  y=y(t)\\
  z=z(t)
\end{matrix}\right.\quad a\le t\le b\\
则\int_C f(x,y,z)ds=\int_a^b f(x(t),y(t),z(t))\sqrt{(x'(t))^2+(y'(t))^2+(z'(t))^2}dt\\
2.若C:y=y(x),a\le x\le b,则\\
\int_L f(x,y)ds=\int_a^b f(x,y(x))\sqrt{1+y'^2(x)}dx\\
3.若C:\rho=\rho(\theta),\alpha\le\theta\le\beta,则\\
\int_L f(x,y)ds=\int_\alpha^\beta f(\rho(\theta)\cos\theta,\rho(\theta)\sin\theta)\sqrt{\rho^2+\rho'^2}d\theta
$$

 <div style="background:#cce1f3">第一型曲面积分</div>

$$
S为单值连续可微曲面:z=g(x,y)\in D\\
dS=\frac{dxdy}{\vert\cos \gamma\vert}\\
曲面z=g(x,y)上任一点法向量为\{g_x',g_y',-1\}\\
\vert\cos \gamma\vert=\frac{1}{\sqrt{g_x'^2+g_y'^2+1}}\\
\iint_S f(x,y,z)dS=\iint_D f(x,y,g(x,y))\sqrt{g_x'^2+g_y'^2+1}dxdy(D为S在XOY的投影)
$$

> 例题:
> $$
> 计算I=\oiint_\Sigma(x^2+y^2)dS,其中\Sigma:x^2+y^2+z^2=2(x+y+z)\\
> 解:显然球心为(1,1,1),半径为\sqrt{3}\\
> 根据轮换对称性,原式=\frac{2}{3}\oiint_\Sigma(x^2+y^2+z^2)dS=\frac{3}{4}\oiint_\Sigma(x+y+z)dS\\
> =4\oiint_\Sigma xdS=4\bar{x}\oiint_\Sigma dS=4\cdot1\cdot4\pi(\sqrt3)^2=48\pi\\
> 形心公式:\bar{x}=\frac{\oiint_\Sigma xdS}{\oiint_\Sigma dS}
> $$

#### 第二型积分

 <div style="background:#cce1f3">第二型曲线积分</div>

$$
若曲线C:\left\{\begin{matrix} 
  x=x(t)\\  
  y=y(t)\\
\end{matrix}\right.\quad t取值为从a到b(起点到终点)\\
则\int_C P(x,y)dx+Q(x,y)dy=\int_a^b[P(x(t),y(t))x'(t)+Q(x(t),y(t))y'(t)]dt
$$

> 由曲线积分求功时,首先求出变力$F$的表达式,若已知$F$的大小$|F|$,它的方向与向量$\vec{l}$同向
>
> 则$F=|F|\frac{l}{|l|}$

 <div style="background:#cce1f3">第二型曲面积分</div>

$$
\iint_\Sigma Pdydz+Qdzdx+Rdxdy\\
=\pm\iint_{D_{yz}}P(x(y,z),y,z)dydz\pm\iint_{D_{zx}}Q(x,y(z,x),z)dzdx\pm\iint_{D_{xy}}R(x,y,z(x,y))dxdy\\
正负号取决于投影的方向,其中上侧/前侧/右侧为正号\\
=\pm\iint_{D_{xy}}[P(x,y,z(x,y))(-\frac{\part z}{\part x})+Q(x,y,z(x,y))(-\frac{\part z}{\part y})+R(x,y,z(x,y))]dxdy
$$

**注意:第二型曲线/曲面积分的奇偶性与其他不同**

 <div style="background:#cce1f3">第二型曲线积分的奇偶性</div>

$$
设L为平面上分段光滑的定向曲线,P(x,y),Q(x,y)连续\\
L关于y轴对称(x=0),则\\
\int_L Pdx=\left\{\begin{matrix} 
  0,\qquad 若P关于x为奇函数\\  
  2\int_{L_1} Pdx,若P关于x为偶函数\\
\end{matrix}\right.\\\int_L Qdy=\left\{\begin{matrix} 
  0,\qquad 若Q关于x为偶函数\\  
  2\int_{L_1} Qdy,若Q关于x为奇函数\\
\end{matrix}\right.\\
其中L_1是L在右半平面的部分
$$



 <div style="background:#cce1f3">第二型曲面积分的奇偶性</div>

$$
若\Sigma关于z=0(XoY面)对称,则\\
\left\{\begin{matrix} 
  \iint_\Sigma f(x,y,z)dxdy=0,\qquad f(x,y,z)关于z为偶函数\\  
  \iint_\Sigma f(x,y,z)dxdy=2\iint_{\Sigma'}f(x,y,z)dxdy,\ f(x,y,z)关于z为奇函数\\
\end{matrix}\right.\\
\Sigma为XoY平面上方的部分
$$

##### 一/二型积分的联系

 <div style="background:#cce1f3">第一/二型曲线积分的联系</div>

$$
设L_{\stackrel\frown{AB}}为光滑分段曲线\\
\int_{L_\stackrel\frown{AB}}Pdx+Qdy=\int_{L_\stackrel\frown{AB}}(P\cos\alpha+Q\cos\beta)ds\\
其中\cos\alpha,\cos\beta为曲线弧L_\stackrel\frown{AB}沿着A到B方向的切线的方向余弦\\
推广到空间,可得:\\
\int_{L_\stackrel\frown{AB}}Pdx+Qdy+Rdz=\int_{L_\stackrel\frown{AB}}(P\cos\alpha+Q\cos\beta+R\cos\gamma)ds\\
其中(\cos\alpha,\cos\beta,\cos\gamma)是L_\stackrel\frown{AB}上任意点(x,y,z)处指向曲线方向的单位切向量
$$

 <div style="background:#cce1f3">第一/二型曲面积分的联系</div>

$$
\cos\alpha dS=dydz,\cos\beta dS=dzdx,\cos\gamma dS=dxdy\\
\iint_\Sigma Pdydz+Qdzdx+Rdxdy=\iint_\Sigma (P\cos\alpha+Q\cos\beta+R\cos\gamma)dS\\
其中\cos\gamma =\pm\frac{1}{\sqrt{1+z_x'^2+z_y'^2}},上侧取'+'号 \\
\cos\alpha=\pm\frac{-z_x'}{\sqrt{1+z_x'^2+z_y'^2}},符号与\cos\gamma相同\\
\cos\beta=\pm\frac{-z_y'}{\sqrt{1+z_x'^2+z_y'^2}},符号与\cos\gamma相同
$$



### 第十章:多元函数积分学公式

#### 格林/高斯/斯托克斯公式

 <div style="background:#cce1f3">格林公式</div>

$$
设平面上有界闭区域D由分段光滑的曲线L围成,函数P(x,y),Q(x,y)在D有\\
连续一阶偏导数,则有:\\
\iint_D(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy=\oint _LPdx+Qdy\\
其中L是D取正向的边界曲线\\
若取P=-y,Q=x,则有S_D=\frac{1}{2}\oint_{L^+}-ydx+xdy,其中L^+取正向\\\\
对于复连通区域D,\iint_D(\frac{\part Q}{\part x}-\frac{\part P}{\part y})dxdy=\sum_{i=1}^n\int_{C_i}Pdx+Qdy\\
C_i全部取正方向
$$

> 例题1:
> $$
> 求\oint_L\frac{xdy-ydx}{x^2+y^2},L:无重复点、分段光滑且不过原点的逆时针闭曲线\\
> 解:P=\frac{-y}{x^2+y^2},Q=\frac{x}{x^2+y^2}\\
> \frac{\partial P}{\partial y}=\frac{\partial Q}{\part x}=\frac{y^2-x^2}{(x^2+y^2)^2}\\
> 1. 若原点(0,0)不在L围成的区域内,则原式=\iint_D 0dxdy=0\\
> 2. 若原点(0,0)在L围成的区域内,在原点周围取一个适当大小的圆l,半径为r\\
> 则\iint_{D-D_l}(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy=\int_{L^+}\frac{xdy-ydx}{x^2+y^2}+\int_{l^+}\frac{xdy-ydx}{x^2+y^2}=0\\
> 则\int_{L^+}\frac{xdy-ydx}{x^2+y^2}=-\int_{l^+}\frac{xdy-ydx}{x^2+y^2}=\int_{l^-}\frac{xdy-ydx}{x^2+y^2}\\
> =\int_0^{2\pi}\frac{r\cos\theta r\cos\theta+r\sin\theta r\sin\theta }{r^2}d\theta\\
> =2\pi
> $$
>
>
> 例题2:
> $$
> D:x=a\cos\theta,y=b\sin\theta,求D的面积\\
> S_D=\frac{1}{2}\oint_{L^+}-ydx+xdy\\
> =\frac{1}{2}\int_0^{2\pi}((-b\sin\theta)\cdot(-a\cos\theta)+a\cos\theta b\cos\theta)d\theta=\pi ab
> $$

 <div style="background:#cce1f3">高斯公式</div>

$$
设\Omega是空间中的有界闭区域,由分块光滑的曲面S所围成.\\
函数P(x,y,z),Q(x,y,z),R(x,y,z)在\Omega有连续的一阶偏导数,则:\\
\begin{aligned}
\iiint_\Omega(\frac{\part P}{\part x}+\frac{\part Q}{\part y}+\frac{\part R}{\part z})dV&=\iint_SPdydz+Qdzdx+Rdxdy\\
&=\iint_S(P\cos\alpha+Q\cos\beta+R\cos\gamma)dS
\end{aligned}\\
其中S是\Omega的整个边界的外侧,\cos\alpha,\cos\beta,\cos\gamma是S上点(x,y,z)处的外法向量的方向余弦\\
$$

 <div style="background:#cce1f3">斯托克斯公式</div>

$$
设\Gamma为分段光滑的有向闭曲线,S是以\Gamma为边界的分块光滑有向曲面\\
\Gamma的正向与S法向量指向符合右手螺旋\\
函数P(x,y,z),Q(x,y,z),R(x,y,z)是S+\Gamma上有连续偏导的函数,则:\\
\oint_CPdx+Qdy+Rdz\\=\iint_S(\frac{\part R}{\part y}-\frac{\part Q}{\part z})dydz+(\frac{\part P}{\part z}-\frac{\part R}{\part x})dzdx+(\frac{\part Q}{\part x}-\frac{\part P}{\part y})dxdy\\
=\iint_S\begin{vmatrix}
  dydz&  dzdx&dxdy \\
  \frac{\part}{\part x}&\frac{\part}{\part y}  &\frac{\part}{\part z} \\
  P&  Q&R
\end{vmatrix}=\iint_S\begin{vmatrix}
  \cos\alpha&  \cos\beta&\cos\gamma \\
  \frac{\part}{\part x}&\frac{\part}{\part y}  &\frac{\part}{\part z} \\
  P&  Q&R
\end{vmatrix}dS
$$

##### 与路径无关

 <div style="background:#cce1f3">平面曲线积分与路径无关</div>

$$
设D为**单连通**区域,P,Q为D上具有连续一阶偏导的函数\\
在D上以下四个结论等价:\\
\begin{aligned}
&1. D上任意闭曲线C,有\oint_C Pdx+Qdy=0\\
&2. D上第二型曲线积分\int_{\stackrel\frown{AB} }Pdx+Qdy与路径无关\\
&3. Pdx+Qdy是全微分\\
&4. \frac{\part P}{\part y}=\frac{\part Q}{\part x}
\end{aligned}\\
若为复连通区域,结论123仍然等价,4不再等价
$$

 <div style="background:#cce1f3">平面曲线积分与路径无关</div>

$$
设\Omega为空间二维单连通区域,P,Q,R为\Omega上具有连续一阶偏导的函数\\
在\Omega上以下四个结论等价:\\
\begin{aligned}
&1. \Omega上任意闭曲线C,有\oint_C Pdx+Qdy+Rdz=0\\
&2. \Omega上第二型曲线积分\int_{\stackrel\frown{AB} }Pdx+Qdy+Rdz与路径无关\\
&\qquad \qquad \qquad \qquad \int_{\stackrel\frown{AB} }Pdx+Qdy+Rdz=\\
&\int_{x_1}^{x_2}P(x,y_1,z_1)dx+\int_{y_1}^{y_2}Q(x_2,y,z_1)dy+\int_{z_1}^{z_2}R(x_2,y_2,z)dz\\
&3. Pdx+Qdy+Rdz是全微分\\
&4. \frac{\part R}{\part y}=\frac{\part Q}{\part z},\frac{\part P}{\part z}=\frac{\part R}{\part x},\frac{\part P}{\part y}=\frac{\part Q}{\part x}
\end{aligned}
$$

> 例题:
> $$
> 证明(2x+yz)dx+(4y+xz)dy+xydz是全微分,并求原函数\\
> 1.特殊路径法,解:P=2x+yz,Q=4y+xz,R=xy\\
> 验证\frac{\part R}{\part y}=\frac{\part Q}{\part z},\frac{\part P}{\part z}=\frac{\part R}{\part x},\frac{\part P}{\part y}=\frac{\part Q}{\part x}成立\\
> 所以原式是全微分,其原函数为:\\
> u(x,y,z)=\int_{(0,0,0)}^{(x,y,z)}(2x+yz)dx+(4y+xz)dy+xydz+C\\
> =\int_0^x 2xdx+\int_0^y4ydx+\int_0^zxydz+C\\
> =x^2+2y^2+xyz+c\\
> 方法2:不定积分法,\frac{\part u}{\part z}=xy,则u=xyz+P(x,y)\\
> 所以\frac{\part u}{\part x}=yz+\frac{\part P}{\part x}=2x+yz\Rightarrow P=x^2+Q(y)\\
> u=xyz+x^2+Q(y),\frac{\part u}{\part y}=xz+\frac{\part Q}{\part y}=xz+4y\Rightarrow Q=2y^2+C\\
> 综上,u=xyz+x^2+2y^2+C
> $$

#### 多元函数积分学物理应用

##### 质心与转动惯量

 <div style="background:#cce1f3">质心/形心</div>

$$
(\bar{x},\bar{y},\bar{z})=(\iiint_\Omega x\rho(x,y,z)dV,\iiint_\Omega y\rho(x,y,z)dV,\iiint_\Omega z\rho(x,y,z)dV)/\iiint_\Omega \rho dV
$$

 <div style="background:#cce1f3">转动惯量</div>

$$
J=mr^2\\
关于x轴及原点的转动惯量分别为\\
I_x=\iiint_\Omega (y^2+z^2)\rho(x,y,z)dV\\
I_o=\iiint_\Omega (x^2+y^2+z^2)\rho(x,y,z)dV
$$

##### 通量和散度

 <div style="background:#cce1f3">通量</div>



 <div style="background:#cce1f3">散度</div>

$$
div F=\frac{\part P}{\part x}+\frac{\part Q}{\part y}+\frac{\part R}{\part z}=\nabla \cdot F
$$

##### 环流量与旋度

> 设有向量场$F(x,y,z)=P(x,y,z)\vec{i}+Q(x,y,z)\vec{j}+R(x,y,z)\vec{k},$则

 <div style="background:#cce1f3">环流量</div>

$$
F沿分段光滑的闭曲线\Gamma的环流量为\\
\oint_\Gamma F\cdot\tau ds=\oint(P\cos\alpha+Q\cos\beta+R\cos\gamma)ds\\=\oint_\Gamma Pdx+Qdy+Rdz=\oint_\Gamma F\cdot ds\\
其中\tau =(\cos\alpha,\cos\beta,\cos\gamma)是\Gamma上任意点(x,y,z)处的单位切向量
$$

 <div style="background:#cce1f3">旋度</div>

$$
rot\ F=(\frac{\part R}{\part y}-\frac{\part Q}{\part z})\vec{i}+(\frac{\part P}{\part z}-\frac{\part R}{\part x})\vec{j}+(\frac{\part Q}{\part x}-\frac{\part P}{\part y})\vec{k}\\
=\nabla \cp F=\begin{vmatrix}
  \vec{i}&  \vec{j}&\vec{k} \\
  \frac{\part}{\part x}&\frac{\part}{\part y}  &\frac{\part}{\part z} \\
  P&  Q&R
\end{vmatrix}\\
若向量场A的旋度rot\ A处处为零,则称向量场A为无旋场
$$



### 第十一章:无穷级数

#### 常数项级数

##### 收敛级数的基本性质

$$
1.级数收敛的必要条件:\lim_{n\to\infty}u_n=0;若不趋于零,则必发散\\
2.若两个级数\sum_{n=1}^\infty u_n和\sum_{n=1}^\infty v_n同时收敛,则\\
\sum_{n=1}^\infty(\lambda u_n+\mu v_n)=\lambda\sum_{n=1}^\infty u_n+\mu \sum_{n=1}^\infty v_n,其中\lambda,\mu为常数\\
若两个级数一个收敛一个发散,则\sum_{n=1}^\infty(u_n\pm v_n)发散\\
若两个级数都发散,则\sum_{n=1}^\infty(u_n\pm v_n)敛散性需讨论\\
3.级数的敛散性与其有限项无关,即添加去掉改变有限项不改变敛散性\\
4.若级数收敛,其任意加括号(不改变顺序)得到的新级数仍然收敛,且和不变\\
若加括号后收敛,原级数未必收敛;若加括号后发散,原级数一定发散
$$

##### 重要级数

> 几何级数

$$
对于a\ne0,|q|<1时,a\sum_{n=0}^\infty q^n=\frac{a}{1-q}收敛,|q|\ge1时发散
$$

> 调和级数

$$
1+\frac{1}{2}+\frac{1}{3}+...+\frac{1}{n}发散\\
证明:S_{2n}-S_n=\frac{1}{n+1}+..+\frac{1}{2n}>\frac{1}{2n}*n=\frac{1}{2}\ne\lim_{n\to\infty}(S_{2n}-S_n)=0
$$

> $p$级数

$$
1+\frac{1}{2^p}+\frac{1}{3^p}+...+\frac{1}{n^p}+...\\
p\le 1发散,p>1收敛\\
证明:p>1时,\frac{1}{k^p}=\int_{k-1}^k\frac{1}{k^p}dx\le\int_{k-1}^k\frac{1}{x^p}dx\\
S_n=1+\sum_{k=2}^n\frac{1}{k^p}\le1+\sum_{k=2}^n\int_{k-1}^k\frac{1}{x^p}dx=1+\int_1^n\frac{1}{x^p}dx\\
=1+\frac{1}{p-1}(1-\frac{1}{n^{p-1}})<1+\frac{1}{p-1}有界,则收敛\\
p\le 1时,n^p\le n,\frac{1}{n^p}\ge\frac{1}{n},而\sum\frac{1}{n}为调和级数发散,则p级数发散
$$

##### 正项级数$u_n\ge0$

$$
正项级数S_n单调非减,收敛\Leftrightarrow S_n有界\\
$$

<div style="background:#cce1f3">比较审敛法</div>

$$
若\sum u_n,\sum v_n都是正项级数,且u_n\le v_n,则\left\{\begin{matrix} 
  \sum v_n收敛\Rightarrow \sum u_n收敛\\
  \sum u_n发散\Rightarrow \sum v_n发散
\end{matrix}\right.
$$

> 极限形式

$$
设u_n,v_n>0,\lim_{n\to\infty}\frac{v_n}{u_n}=A,则有\\
\left\{\begin{matrix}
  0<A<+\infty,\sum u_n,\sum v_n同时收敛或发散\\
  A=0,\sum u_n收敛\Rightarrow \sum v_n收敛\\
  A=+\infty,\sum u_n发散\Rightarrow \sum v_n发散
\end{matrix}\right.
$$

<div style="background:#cce1f3">比值和根值判别法</div>

> 比值判别法(达朗贝尔判别法)

$$
若\lim_{n\to\infty}\frac{u_{n+1}}{u_n}=\rho\left\{\begin{matrix}
  \rho<1,\sum u_n收敛\\
  \rho>1,\sum u_n发散,且\lim_{n\to\infty}u_n =+\infty\\
  \rho=1,无法判别
\end{matrix}\right.
$$

> 根值判别法(柯西判别法)

$$
若\lim_{n\to\infty}\sqrt[n]{u_n}=\rho\left\{\begin{matrix}
  \rho<1,\sum u_n收敛\\
  \rho>1,\sum u_n发散,且\lim_{n\to\infty}u_n =+\infty\\
  \rho=1,无法判别
\end{matrix}\right.
$$

<div style="background:#cce1f3">与p级数比较</div>

$$
设u_n>0,\lim_{n\to\infty}\frac{u_n}{\frac{1}{n^p}}=A\\
若0\le A<+\infty,p>1,则\sum_{n=1}^\infty u_n收敛\\
若0<A\le +\infty,p\le 1,则\sum_{n=1}^\infty发散
$$

<div style="background:#cce1f3">积分判别法</div>

$$
设\sum_{n=1}^\infty u_n为正项级数,若\exist单调下降的正值函数f(x)(x\ge 1)使得u_n=f(n)\\
n=1,2...,则级数\sum_{n=1}^\infty u_n=\sum_{n=1}^\infty f(n)收敛的充要条件是无穷积分\int_1^{+\infty}f(x)dx收敛
$$

##### 交错级数

> 定义:$u_n\gt 0,\sum_{n=1}^\infty (-1)^{n-1}u_n$

<div style="background:#cce1f3">莱布尼兹判别法</div>

$$
若u_n\ge u_{n+1}且\lim_{n\to\infty} u_n=0\\
则交错级数收敛且其和0<S<u_1,余项|r_n|<u_{r+1}\\
比较u_n和u_{n+1}可以使用求导令\lim_{n\to \infty}的方式
$$

##### 任意项级数

> 定义:$u_n$为任意实数,则$\sum_{n=1}^\infty u_n$为任意项级数

$$
若级数\sum_{n=1}^\infty |u_n|收敛,则称级数\sum_{n=1}^\infty u_n绝对收敛\\
若\sum u_n收敛,\sum|u_n|发散,则称级数\sum_{n=1}^\infty u_n条件收敛\\
绝对收敛级数与条件收敛级数之和为条件收敛级数\\
若用比值或根值法判断\sum_{n=1}^\infty |u_n|发散,则\sum_{n=1}^\infty u_n发散,否则仍需判断是否条件收敛\\
条件收敛级数的全部正项或负项构成的级数一定发散
$$

#### 幂级数

> 阿贝尔定理

$$
如果幂级数\sum_{n=0}^\infty a_nx^n当x=x_0\ne0时收敛,该幂级数在满足|x|<|x_0|的所有x处绝对收敛\\
如果幂级数\sum_{n=0}^\infty a_nx^n当x=x_1时发散,该幂级数在满足|x|>|x_1|的所有x处发散
$$

> 可能的收敛情况

$$
1.仅在x=0时收敛\\
2.在x\in(-\infty,+\infty)收敛\\
3.在|x|<R绝对收敛,两个端点x=\pm R需要单独判断\\
(-R,R)称为收敛区间,加上收敛的端点为收敛域,R称为收敛半径
$$

##### 收敛半径和收敛域求法

$$
1.求收敛半径\\
使用比值法或根值法,如果\lim_{n\to\infty}|\frac{a_{n+1}}{a_n}|=l或\lim_{n\to\infty}\sqrt[n]{|a_n|}=l,则\\
R=\left\{\begin{matrix}
  1/l,\quad 0<l<+\infty\\
  0,\qquad l=+\infty\\
  +\infty,\qquad l=0
\end{matrix}\right.\\
如果只有偶数项等特殊情况,直接比较相邻两项(带x)根据比值/根值判别法进行求解
$$

##### 幂级数的运算和函数的性质

<div style="background:#cce1f3">逐项积分</div>

$$
\sum_{n=0}^{+\infty}a_nx^n的和函数S(x)在I上可积,则\\
\int_0^xS(t)dt=\int_0^x(\sum_{n=0}^\infty a_nt^n)dt=\sum_{n=0}^\infty\int_0^xa_nt^ndt\\
=\sum_{n=0}^\infty\frac{a_n}{n+1}x^{n+1}(x\in I)\\
逐项积分后得到的新幂级数与原幂级数收敛半径相同,但端点处(收敛域)需要重新检验
$$

<div style="background:#cce1f3">逐项求导</div>

$$
S(x)在(-R,R)内可导,S'(x)=(\sum_{n=0}^\infty a_nx^n)'=\sum_{n=0}^\infty(a_nx^n)'\\
=\sum_{n=0}^\infty a_nx^{n-1}\\
逐项求导后得到的新幂级数与原幂级数收敛半径相同,但端点处(收敛域)需要重新检验
$$

> 泰勒级数和麦克劳林展开

$$
泰勒展开:f(x)=\sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n,x\in U(x_0)\\
充要条件:\lim_{n\to\infty}R_n(x)=0\\
若x_0=0,则麦克劳林展开:\\
f(x)=\sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!}x^n,x\in (-r,r)
$$

##### 常用麦克劳林展开

> 核心公式

$$
1. e^x=1+x+\frac{x^2}{2}+...+\frac{x^n}{n!},x\in(-\infty,+\infty)\\
2. \sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+...+(-1)^n\frac{x^{2n+1}}{(2n+1)!}+...,x\in(-\infty,+\infty)\\
3. \frac{1}{1-x}=1+x+x^2+x^3+...+x^n,x\in(-1,1)
$$

> 推出公式

$$
4.[3.x=-x]\frac{1}{1+x}=1-x+x^2-x^3+...+(-1)^nx^n+...,x\in (-1,1)\\
5.[对4积分]\ln(1+x)=x-\frac{x^2}{2}+\frac{x^3}{3}-...+\frac{(-1)^{n-1}}{n}x^n+..,x\in(-1,1]\\
6.[对2求导]\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}-...+(-1)^n\frac{x^{2n}}{(2n!)}+..,x\in(-\infty,+\infty)\\
7.[1.x=x\ln a]a^x=1+x\ln a+\frac{x^2(\ln a)^2}{2!}+..+\frac{x^n(\ln a)^n}{n!}+..,x\in(-\infty,+\infty)\\
8.[4.x=x^2]\frac{1}{1+x^2}=1-x^2+x^4-...+(-1)^nx^{2n}+..,x\in(-1,1)\\
9.[对8积分]\arctan x=x-\frac{x^3}{3}+\frac{x^5}{5}-...+(-1)^n\frac{x^{2n+1}}{2n+1}+,,.x\in[-1,1]
$$

#### 傅里叶级数

> 三角函数系

$$
\{1,\cos\frac{\pi}{l}x,\sin\frac{\pi}{l}x,\cos\frac{2\pi}{l}x,\sin\frac{2\pi}{l}x,...,\cos\frac{n\pi}{l}x,\sin\frac{n\pi}{l}x...\}\\
在区间[-l,l]上正交,即任在其中取两个不同的函数f(x),g(x)\\
都有\int_l^lf(x)g(x)dx=0
$$

> 傅里叶级数

$$
若f(x)以2l为周期,且下述积分存在\\
\left\{\begin{matrix}
  a_0=\frac{1}{l}\int_{-l}^lf(x)dx\\
  a_n=\frac{1}{l}\int_{-l}^lf(x)\cos \frac{n\pi}{l}xdx\\
  b_n=\frac{1}{l}\int_{-l}^lf(x)\sin \frac{n\pi}{l}xdx
\end{matrix}\right.\qquad n=1,2,..\\
则称\frac{a_0}{2}+\sum_{n=1}^\infty(a_n\cos\frac{n\pi}{l}x+b_n\sin\frac{n\pi}{l}x)为f(x)的傅里叶级数
$$

> 性质

$$
若f(x)为奇函数,则a_0=a_n=0,b_n=\frac{2}{l}\int_0^lf(x)\sin\frac{n\pi}{l}xdx,n=1,2,..\\
此时f(x)=\sum_{n=1}^\infty b_n\sin\frac{n\pi}{l}x\\
若f(x)为偶函数,则b_n=0,a_n=\frac{2}{l}\int_0^lf(x)\cos\frac{n\pi}{l}xdx,n=0,1,...\\
此时f(x)=\frac{a_0}{2}+\sum_{n=1}^\infty a_n\cos\frac{n\pi}{l}x
$$

> 收敛性(狄利克雷收敛定理)

$$
函数f(x)在区间[-l.l]上满足:\\
1.连续或只有有限个第一类间断点\\
2.只有有限个极值点\\
则f(x)在[-l,l]上的傅里叶级数收敛,并且\\
\frac{a_0}{2}+\sum_{n=1}^\infty(a_n\cos\frac{n\pi}{l}x+b_n\sin\frac{n\pi}{l}x)\\=\left\{\begin{matrix}
  f(x),若x\in (-l,l)为f(x)的连续点\\
  \frac{1}{2}[f(x+0)+f(x-0)],若x\in (-l,l)为f(x)的第一类间断点\\
  \frac{1}{2}[f(-l+0)+f(l-0)],若x=\pm l
\end{matrix}\right.
$$

##### 有限区间上函数的傅里叶级数

> $[0,l]$上的正弦型级数

$$
将f(x)奇延拓成[-l,l]上的奇函数\\
g(x)=\left\{\begin{matrix}
  f(x),x\in[0,l]\\
  -f(x),x\in[-l,0)\\
\end{matrix}\right.\\
则g(x)在[-l,l]上的F-级数就是f(x)在[0,l]上的正弦型级数\\
则a_0=a_n=0,b_n=\frac{2}{l}\int_0^lf(x)\sin\frac{n\pi}{l}xdx,n=1,2,..\\
\sum_{i=1}^\infty b_n\sin\frac{n\pi}{l}x=\left\{\begin{matrix}
  \frac{1}{2}[f(x^+)+f(x^-)],x\in(0,l)\\
  0,x=0\ or\ x=l\\
\end{matrix}\right.\\
$$

> $[0,l]$上的余弦型级数

$$
将f(x)偶延拓成[-l,l]上的偶函数\\
g(x)=\left\{\begin{matrix}
  f(x),x\in[0,l]\\
  f(-x),x\in[-l,0)\\
\end{matrix}\right.\\
则g(x)在[-l,l]上的F-级数就是f(x)在[0,l]上的余弦型级数\\
则b_n=0,a_n=\frac{2}{l}\int_0^lf(x)\cos\frac{n\pi}{l}xdx,n=0,1,...\\
\frac{a_0}{2}+\sum_{n=1}^\infty a_n\cos\frac{n\pi}{l}x=\frac{1}{2}[f(x^+)+f(x^-)],x\in[0,l]
$$



### 附录

#### 常见曲线

![1](E:\保存\考研内容\数学\1.png)

![2](E:\保存\考研内容\数学\2.png)

#### 常见曲面

##### 二次曲面

<div style="background:#cce1f3">球面</div>

$$
(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=R^2,球心为M_0(x_0,y_0,z_0)
$$

![image-20220319145642270](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319145642270.png)

<div style="background:#cce1f3">椭圆锥面</div>

$$
定义:\frac{x^2}{a^2}+\frac{y^2}{b^2}=z^2\\
常见:
$$

![image-20220319145723226](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319145723226.png)

<div style="background:#cce1f3">椭球面</div>

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1\\
其中\frac{x^2+y^2}{a^2}+\frac{z^2}{c^2}=1表示XOZ平面上的椭圆绕z轴旋转而成的椭球面
$$

![image-20220319191824958](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319191824958.png)

<div style="background:#cce1f3">单叶双曲面</div>

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=1\\
其中\frac{x^2+y^2}{a^2}-\frac{z^2}{c^2}=1表示XOZ平面上的双曲线绕z轴旋转而成的单叶双曲面
$$

![image-20220319192055952](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319192055952.png)


<div style="background:#cce1f3">双叶双曲面</div>

$$
\frac{x^2}{a^2}-\frac{y^2}{b^2}-\frac{z^2}{c^2}=1\\
其中\frac{x^2}{a^2}-\frac{y^2+z^2}{c^2}=1表示XOZ平面上的双曲线绕x轴旋转而成的双叶双曲面
$$

![image-20220319192104472](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319192104472.png)

<div style="background:#cce1f3">椭圆抛物面</div>

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=z
$$

![image-20220319192158121](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319192158121.png)

<div style="background:#cce1f3">双曲抛物面(马鞍面)</div>

$$
\frac{x^2}{a^2}-\frac{y^2}{b^2}=z\\
常见:z=xy也为马鞍面,证明:\\
令x=\frac{u+v}{\sqrt{2}},y=\frac{u-v}{\sqrt{2}},z=z\\
方程变为\frac{u^2-v^2}{2}=z,为a^2=b^2=2的马鞍面
$$

![image-20220319192248529](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319192248529.png)

##### 柱面

<div style="background:#cce1f3">圆柱面</div>

$$
x^2+y^2=R^2
$$

![image-20220319192528309](C:\Users\LemontreeN\AppData\Roaming\Typora\typora-user-images\image-20220319192528309.png)

<div style="background:#cce1f3">椭圆柱面</div>

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1
$$

<div style="background:#cce1f3">双曲柱面</div>

## TODO

#### 其他

<div style="background:#cce1f3">X+Y+Z=0图像</div>

![3](https://cdn.jsdelivr.net/gh/LemontreeN/picSources@master/Mess/202205291837832.png)

