## 线性代数

[TOC]

### 第一章节:行列式

$$
\vert D\vert=\sum(-1)^{t(i_1i_2...i_n)+t(j_1j_2...j_n)}a_{i_1j_1}a_{i_2j_2}...a_{i_nj_n}\\
其中t(i_1i_2...i_n)即为i_1i_2...i_n的逆序数,t(j_1j_2...j_n)同理
$$



上三角下三角主对角线 都是 对角线相乘

副对角线以及副对角线三角形都是对角线相乘再乘$(-1)^{\frac{n(n-1)}{2}}$

##### 行列式的性质

$$
(D^T)^T=D\\
\vert cD\vert=c^n\vert D\vert\\
\vert D^T	\vert=\vert D\vert\quad (因此对行成立的性质对列也成立)\\
行列式两行互换,值变号\\
两行元素对应成比例,\vert D\vert=0\\
\begin{vmatrix}
  a&  b& c\\
  d+e&  f+g&h+i \\
  j&  k&l\end{vmatrix}=\begin{vmatrix}
  a&  b& c\\
  d&  f&h \\
  j&  k&l\end{vmatrix}+\begin{vmatrix}
  a&  b& c\\
  e&  g&i \\
  j&  k&l\end{vmatrix}\\
  某一行乘k加到另一行,行列式的值不变\\
  异乘变零定理:某一行的元素和另一行对应元素代数余子式乘积之和为0
$$

代数余子式
$$
A_{ij}=(-1)^{i+j}M_{ij}\quad (M_{ij}为余子式)
$$

##### 特殊行列式

<div style="background:#cce1f3">加边法</div>

$$
\begin{vmatrix}
  a&  b&  c \\
  d&  e&  f \\
  g&  h&  i \\\end{vmatrix}=\begin{vmatrix}
  1&1&1&1\\
  0&a&  b&  c \\
  0&d&  e&  f \\
  0&g&  h&  i \\\end{vmatrix}
$$



<div style="background:#cce1f3">范德蒙行列式</div>

$$
\begin{vmatrix}
  1&  1&  1&  ...&1 \\
  x_1&  x_2&  x_3&  ...&x_n \\
  x_1^2&  x_2^2&  x_3^2&  ...&x_n^2 \\
  ...&  ...&  ...&  ...&... \\
  x_1^n&  x_2^n&  x_3^n&  ...&x_n^n
\end{vmatrix}=\prod_{1\le j\lt i\le n}(x_i-x_j)
$$

<div style="background:#cce1f3">反对称行列式</div>

$$
a_{ij}=-a{ji}\\即主对角线全为0,对角线两侧对应为相反数\\
例如\begin{vmatrix}
  0&  3&  -2 \\
  -3&  0&  1 \\
  2&  -1&  0 \\\end{vmatrix}
$$

> 奇数阶反对称行列式为$\vert D\vert=0$

<div style="background:#cce1f3">对称行列式</div>

$$
a_{ij}=a_{ji}\\即主对角线任意,对角线两侧对应相等\\
例如\begin{vmatrix}
  1&  -1&  -2 \\
  -1&  2&  5 \\
  -2&  5&  3 \\\end{vmatrix}
$$

<div style="background:#cce1f3">三叉型行列式</div>

>  用列消去转换为上三角行列式(需要注意分母不为零的条件)

$$
\begin{vmatrix}
  a_1&  b_1&  ...&d_1 \\
  a_2&  b_2&  & \\
  ...&  &  ...& \\
  a_n&  &  &d_n
\end{vmatrix}=\begin{vmatrix}
  a_1-b_1\frac{a_2}{b_2}-\cdot\cdot\cdot-d_1\frac{a_n}{d_n}&  b_1&  ...&d_1 \\
  0&  b_2&  & \\
  ...&  &  ...& \\
  0&  &  &d_n
\end{vmatrix}
$$

$$
形如D=\begin{vmatrix}
  a_0&a_1  &a_2  &..  &a_{n-1}&a_n \\
  b_1&  c_1&0  &..  &0 &0\\
  b_2&  0&  c_2&  ..&0&0 \\
  ..&  ..&  ..&  &..&..\\
  b_n&  0&  0&  ..&0&c_n
\end{vmatrix}_n\\解法:对第一行展开D=a_0\prod_{i=1}^{n} c_i+\sum_{i=2}^{n+1}A_{1i}\\
=a_0\prod_{i=1}^{n} c_i+\sum_{i=1}^{n}(-1)^{i}M_{1(i+1)}\\
其中\quad M_{1i}=\begin{vmatrix}
  G_i&  0\\
  *&  H_i\\\end{vmatrix}\\
  G_i=\begin{vmatrix}
  b_1&  c_1&  0&  ..&0 \\
  b_2&  0&  c_1&  ..&0 \\
  ..&  ..&  ..&  &.. \\
  b_{i-1}&  0&  0&  ..&c_{i-1}\\
  b_i&..&..&0&0
\end{vmatrix}_{i}=(-1)^{i+1}b_i\begin{vmatrix}
  c_1&  0&  ..&0 \\
  0&  c_2&  ..&0 \\
  ..&  ..&  &.. \\
  0&  0&  ..&c_{i-1}
\end{vmatrix}_{i-1}\\
H_i=\begin{vmatrix}
  c_{i+1}&  0& ..&  0&0 \\
  0&  c_{i+2}&  ..&  0&0 \\
  ..&  ..&  &  ..&.. \\
  0&  ..&  ..&  0&c_n
\end{vmatrix}_{n-i}
$$



<div style="background:#cce1f3">爪型行列式</div>

$$
形如D=\begin{vmatrix}
  a_1&a_2  &a_3  &..  &a_{n-1}&a_n \\
  b_1&  c_2&0  &..  &0 &0\\
  0&  b_2&  c_3&  ..&0&0 \\
  
  ..&  ..&  ..&  &..&..\\
  0&  0&  0&  ..&b_{n-1}&c_n
\end{vmatrix}_n\\解法:对第一行展开
D=\sum_{i=1}^n(-1)^{i-1}a_iM_{1i}\\
其中\quad M_{1i}=\begin{vmatrix}
  G_i&  0\\
  0&  H_i\\\end{vmatrix}\\
  G_i=\begin{vmatrix}
  b_1&  c_2&  0&  ..&0 \\
  0&  b_2&  c_3&  ..&0 \\
  ..&  ..&  ..&  &.. \\
  0&  ..&  ..&  0&b_{i-1}
\end{vmatrix}_{i-1}为上三角行列式,\\H_i=\begin{vmatrix}
  c_{i+1}&  0& ..&  0&0 \\
  b_{i+1}&  c_{i+2}&  ..&  0&0 \\
  ..&  ..&  &  ..&.. \\
  0&  ..&  0&  b_{n-1}&c_n
\end{vmatrix}_{n-i}为下三角行列式
$$

<div style="background:#cce1f3">三斜线行列式</div>

$$
n阶三斜线行列式,形如D=\begin{vmatrix}
  a&b  &0  &..  &0&0 \\
  c&  a&b  &..  &0 &0\\
  ..&  ..&  ..&  &..&.. \\
  0&  0&  0&  ..&a&b \\
  0&  0&  0&  ..&c&a
\end{vmatrix}_n\\
\begin{aligned}
则D&=A_{11}+A_{12}\quad (第一行展开)\\
&=aD_{n-1}-M_{12}\quad (M_{12}第一列展开)\\
&=aD_{n-1}-bcD_{n-2}
\end{aligned}\\
之后使用数学归纳法或者数列技巧证明or计算
$$

<div style="background:#cce1f3">拉普拉斯特殊情形</div>

如果A和B都是方阵
$$
\begin{vmatrix}
  A&  0 \\
  *&  B \\
  \end{vmatrix}=\begin{vmatrix}
  A&  * \\
  0&  B \\
  \end{vmatrix}=\vert A\vert\vert B\vert,\quad
  \begin{vmatrix}
  0&  A \\
  B  &*\\
  \end{vmatrix}=\begin{vmatrix}
  *&  A \\
  B&  0 \\
  \end{vmatrix}=(-1)^{mn}\vert A\vert\vert B\vert
$$

##### 克莱姆Cramer法则

设含有$n$个未知数,$n$个方程的线性方程组(未知数个数与方程组个数相同)
$$
\left\{\begin{matrix} 
  a_{11}x_1+a_{12}x_2+...+a_{1n}x_n=b_1 \\  
  a_{21}x_1+a_{22}x_2+...+a_{2n}x_3=b_2\\
  a_{n1}x_1+a_{n2}x_2+...+a_{nn}x_3=b_n
\end{matrix}\right.\\
系数行列式为D=\begin{vmatrix}
  a_{11}&  a_{12}&  ...&a_{1n} \\
  a_{21}&  a_{22}&  ...&a_{2n} \\
  ...&...&...&...\\
  a_{n1}&  a_{n2}&  ...&a_{nn} \\\end{vmatrix}\\
D_j=是把D中第j列元素替换为方程组右端的常数得到的n阶行列式\\
若D\ne0\quad,则方程组有唯一解,且x_1=\frac{D_1}{D},x_2=\frac{D_2}{D},...,x_n=\frac{D_n}{D},
$$

>  若$b_1=b_2=...=b_n=0$,则方程组至少有零解,若同时$D\ne0$,则方程组只有零解
>
>  齐次方程有非零解的充要条件((未知数个数与方程组个数相同)$\quad\Leftrightarrow\quad D=0$

### 第二章:矩阵

##### 基本性质

相乘条件:左列数=右行数

中间相等取两头

如果$AB=BA$,称$AB$是可交换的
$$
矩阵运算:\\
(AB)^k\ne A^kB^k
\\
(A^T)^=A\\
(A+B)^T=A^T+B^T\\
(AB)^T=B^TA^T
$$
左乘行,右乘列
$$
设A=\alpha\beta^T,\alpha和\beta都是n维列向量,则对于正整数k有:\\
A^k=(\beta^T\alpha)^{k-1}A=(tr(A))^{k-1}A
$$

##### 特殊矩阵

<div style="background:#cce1f3">数量矩阵</div>

$$
设E为单位矩阵,k为任何实数,则称kE为数量矩阵
$$

<div style="background:#cce1f3">对角矩阵</div>

$$
主对角线以外元素均为0的矩阵,一般记为diag (a_1,a_2,..,a_n)
$$

<div style="background:#cce1f3">对称矩阵(方阵)</div>

$$
定义:a_{ij}=a_{ji}\\
性质:A^T=A\\
A,B对称,AB对阵\Leftrightarrow AB可交换
$$

<div style="background:#cce1f3">反对称矩阵(方阵)</div>

$$
定义:a_{ij}=-a_{ji}\\
性质:主对角线全为0\\
A^T=-A
$$

伴随矩阵

> 方阵才有伴随矩阵

$$
A^*=\begin{bmatrix}
  A_{11}&A_{21}  &..  &A_{n1} \\
  A_{12}&A_{22}  &..  &A_{n2} \\
  ..&..  &  &.. \\
  A_{1n}&  A_{2n}&..  &A_{nn}
\end{bmatrix}=|A|A^{-1}\\
\forall 方阵A,有AA^*=A^*A=|A|E\\
|A^*|=|A|^{n-1}(|A|=0也成立)
$$

<div style="background:#cce1f3">逆矩阵</div>

> 方阵才有逆矩阵

$$
若A为n阶方阵,\exist B使得AB=BA=E,则A^{-1}=B\\
A可逆的充要条件:|A|\ne0(非奇异,非退化,满秩)\\
A^{-1}=\frac{1}{|A|}A^*(伴随矩阵法)
$$

> 性质:

$$
\begin{aligned}
A可逆&,则A的逆矩阵A^{-1}唯一\\
A可逆&,|A^{-1}|=\frac{1}{|A|}\\
A可逆&,则A^{-1}可逆,(A^{-1})^{-1}=A\\
A可逆&,则A^T可逆,且(A^T)^{-1}=(A^{-1})^T\\
A可逆&,则A^*可逆,且(A^*)^{-1}=\frac{1}{|A|}A\\
若A,B均可逆&,则AB可逆,且(AB)^{-1}=B^{-1}A^{-1}\\
k\ne0&,则(kA)^{-1}=\frac{1}{k}A^{-1}\\
\end{aligned}
$$

> 解矩阵方程的注意事项:
>
> + 提取公因子注意方向
> + 矩阵不能和数字直接运算,要加E
> + 先判断可逆,再乘逆矩阵

##### 分块矩阵

$$
H=\begin{pmatrix}
  A&C \\
  0&B
\end{pmatrix}\\
|H|=|A||B|\ (证明:Laplace展开)
$$

>  性质

$$
A=\begin{pmatrix}
  A_1&A_2  &A_3 \\
  A_4&A_5  &A_6
\end{pmatrix},A^T=\begin{pmatrix}
  A_1^T&A_4^T\\
  A_2^T&A_5^T\\
  A_3^T&A_6^T
\end{pmatrix}  
$$

>  结论

$$
H=\begin{pmatrix}
  A&C \\
  0&B
\end{pmatrix},\quad 则H^{-1}=\begin{pmatrix}
  A^{-1}&-A^{-1}CB^{-1} \\
  0&B^{-1}
\end{pmatrix}\\
\begin{pmatrix}
  A_1&  &  & \\
  &  A_2&  & \\
  &  &  ..& \\
  &  &  &A_s
\end{pmatrix}^{-1}=\begin{pmatrix}
  A_1^{-1}&  &  & \\
  &  A_2^{-1}&  & \\
  &  &  ..& \\
  &  &  &A_s^{-1}
\end{pmatrix}
$$

##### 初等变换

$$
行初等变换\left\{\begin{matrix} 
\begin{aligned}
  &交换两行 &E(i,j)\\  
  &用k(\ne0)乘某一行&E(i(k)),k\ne0 \\
  &某一行的l倍加到另一行上&E(i,j(k))
  \end{aligned}
\end{matrix}\right.\\
$$

> 性质

$$
|E(i,j)|=-1,\quad |E(i(k))|=k(\ne0),\quad |E(i,j(k))|=1\\
E(i,j)^{-1}=E(i,j),\quad E(i(k))^{-1}=E(i(\frac{1}{k})),\quad E(i,j(k))^{-1}=E(i,j(-k))
$$

初等变换等价于组左右乘初等矩阵

> 定理

$$
A,B等价\Leftrightarrow \exists 可逆矩阵P,Q,\quad 使得PAQ=B\\
A可逆\Leftrightarrow A的标准型为E
$$

>  用途

$$
求矩阵的逆:\quad (A,E)\longrightarrow (E,A^{-1}) \\
注意事项:
1. 按照第一列第二列第三列...的顺序\\
2. 每次对整行进行操作\\
3. 用\longrightarrow连接
4. 只能用行变换\\
5. 如果A无法化为E,证明A不可逆\\
6. 求出A^{-1}后进行验证
$$

##### 矩阵的秩

> 定义:非零子式的最高阶数

$$
r(A)=n\Leftrightarrow 有一个r阶子式不为0,所有r+1阶均为0(更高也为0,按行展开可证)
$$

> 性质

$$
矩阵的秩r(A)=非零行的行数\\
初等变换不改变矩阵的秩\\
A为方阵且A满秩,则A可逆\\
r(A)=r(A^T)\\
A_{m\cp n},P为m阶可逆方阵,Q为n阶可逆方阵,则r(A)=r(PA)=r(AQ)=r(PAQ)\\
若AB=0,则r(A)+r(B)\le n,\quad n为A的列数(B的行数)\\
r(A^*)=\left\{\begin{matrix} 
n,\qquad 若r(A)=n\\
1,\qquad 若r(A)=n-1\\
0,\qquad 若r(A)<n-1
\end{matrix}\right.\\
$$

<div style="background:#cce1f3">阶梯型</div>

+ 若有零行,零行在非零行的下面

+ 坐起首非零元素左边零的个数随行数增加而严格增加 

$$
形如\begin{bmatrix}
  a&b  &c  &d \\
  0&e  &f  &g \\
  0&  0&  h&i \\
  0&  0&0  &0
\end{bmatrix}
$$

<div style="background:#cce1f3">行简化阶梯型</div> 

+ 是阶梯型
+ 非零行的首非零元为1
+ 首非零元所在列的其余元素全为0
+ 按照上面三步进行检验

$$
形如\begin{bmatrix}
  1&0  &0  &b \\
  0&1  &0  &c \\
  0&  0&  1&d \\
  0&  0&0  &0
\end{bmatrix}
$$

##### 其他性质

一般地,$AB=cB$时,$A^nB=c^nB$,特别地,$AB=B$时,$A^nB=B$

<div style="background:#cce1f3">矩阵分解</div>

> 当一个矩阵$B$是另一个矩阵$A$的列向量组线性组合时,可以构造一个矩阵$C$,使得$B=AC$

$$
设A=(\alpha,\beta,\gamma),B=(\alpha+2\beta-\gamma,\ 3\alpha-\beta+\gamma,\ \alpha+2\gamma)\\
令C=\begin{bmatrix}
  1&  3&1 \\
  2&  -1&0 \\
  -1&1  &2
\end{bmatrix},\quad 则B=AC
$$

#### 基本矩阵方程

$$
初等变换法\\
\begin{aligned}
1. &AX=B:(A|B)\rightarrow (E|X),X即为方程的解\\
2. &XA=B:两侧同时转置得到A^TX^T=B^T,再按第一条\\
&(A^T|B^T)\rightarrow (E|X^T)得到X^T,对X^T进行转置即可得到方程的解X
\end{aligned}
$$

> 可以看出,当$B$为单位阵$E$时,所得解$X$即为$A^{-1}$

### 第三章:向量组的线性关系与秩

$$
k\alpha=0\Leftrightarrow \quad k=0\ or\ \alpha=0
$$

##### 线性相关

>  定义:对于向量组$\alpha_1,\alpha_2,..,\alpha_n$,如果存在一组数$k_1,k_2,..,k_n$使得
> $$
> k_1\alpha_1+k_2\alpha_2+..+k_n\alpha_n=0
> $$
> 成立,则该向量组是线性相关的,否则是线性无关的

显然可以看出,向量组中如果存在$\vec{0}$,则必线性相关 

>  性质

$$
\left\{\begin{matrix} 
部分组线性相关\rightarrow整体组线性相关\\
整体组线性无关\rightarrow部分组线性无关\\
\end{matrix}\right.\\
\left\{\begin{matrix} 
线性无关的向量组的接长向量组也线性无关\\
线性相关的向量组的截断向量组也线性相关
\end{matrix}\right.\\
对于n个n维向量组成的行列式D\left\{\begin{matrix} 线性无关\Leftrightarrow D\ne0\\线性相关\Leftrightarrow D=0 \end{matrix}\right.\\
\left\{\begin{matrix} 
\alpha_1,..,\alpha_n线性相关\Leftrightarrow 至少一个向量可由其余向量表示\\
\alpha_1,..,\alpha_n线性无关,且\alpha_1,..,\alpha_n,\beta线性相关,则\beta可由\alpha_1,..,\alpha_n唯一表示
\end{matrix}\right.\\
\left\{\begin{matrix} 
替换定理:\alpha_1,..,\alpha_s线性无关,且可由\beta_1,..,\beta_t表示,则s\le t\\
逆否命题:\alpha_1,..,\alpha_s可由\beta_1,..\beta_t表示,且s>t,则\alpha_1,..,\alpha_s线性相关
\end{matrix}\right.\\
\left\{\begin{matrix} 
若m>n,则m个n维向量线性相关\\
推论:两个等价的线性无关组所含向量个数相同
\end{matrix}\right.
$$

$$
做题常用:\\
\left\{\begin{matrix} 
\beta可用(\alpha_1,..,\alpha_s)线性表示\Leftrightarrow r(\alpha_1,..,\alpha_s,\beta)=r(\alpha_1,..,\alpha_s)\\
\beta可用(\alpha_1,..,\alpha_s)唯一线性表示\Leftrightarrow r(\alpha_1,..,\alpha_s,\beta)=r(\alpha_1,..,\alpha_s)=s\\
\end{matrix}\right.\\
\left\{\begin{matrix} 
\beta_1,..,\beta_t可用\alpha_1,..,\alpha_s线性表示\Leftrightarrow r(\alpha_1,,..,\alpha_s,\beta_1,..,\beta_t)=r(\alpha_1,,..,\alpha_s) \\
\beta_1,..,\beta_t和\alpha_1,..,\alpha_s等价\Leftrightarrow r(\alpha_1,,..,\alpha_s)=r(\alpha_1,,..,\alpha_s,\beta_1,..,\beta_t)=r(\beta_1,..,\beta_t)
\end{matrix}\right.
$$

#### 向量组的秩

##### 极大线性无关组

$$
全为0的向量组没有极大线性无关组\\
线性无关的向量组的极大无关向量组就是它本身\\
任何向量组和它的极大无关向量组等价
$$

<div style="background:#cce1f3">向量组的秩</div> 

> 定义:极大线性无关组所含向量个数,即$r(\alpha_1,..,\alpha_s)$
>
> 规定:全为$0$的向量组的秩为$0$
>
> $0\le r(\alpha_1,..,\alpha_s)\le \min\{s,向量的维数\}$

$$
\left\{\begin{matrix} 
\alpha_1,..,\alpha_s线性无关\Leftrightarrow r=s\\
\alpha_1,..,\alpha_s线性相关\Leftrightarrow r<s
\end{matrix}\right.\\
\alpha_1,..,\alpha_s可由\beta_1,..\beta_t表示,则r(\alpha_1,..,\alpha_s)\le r(\beta_1,..,\beta_t)\\
两个向量组等价\longrightarrow秩相等\\
矩阵的行秩=列秩=r(A)\\
r(A\pm B)\le r(A)+r(B)\\
r(AB)\le \min\{r(A),r(B)\}\\
初等行变换不改变列向量组的线性关系
$$

<div style="background:#cce1f3">求极大线性无关组</div> 

1. 不管是行向量还是列向量,均按照列构成矩阵
2. 仅使用初等行变换化为行简化阶梯型
3. 首非零元所在列做极大线性无关组
4. 其余向量表示系数直接写出

> 例:求下面矩阵的列向量的极大线性无关组,并将其他向量用其表示
> $$
> \begin{pmatrix}
>   1&  2&  -2&3 \\
>   -2&  -4&  4&-6 \\
>   2&  8&  -2&0 \\
>   -1&  0&  3&-6
> \end{pmatrix}\longrightarrow\begin{pmatrix}
>   1&  0&  -3&6 \\
>   0&  1&  \frac{1}{2}&-\frac{3}{2} \\
>   0&  0&  0&0 \\
>   0&  0&  0&0
> \end{pmatrix}\\
> $$
>
> $$
> 则\beta_1,\beta_2是极大线性无关组\\
> 且\left\{\begin{matrix}
> \beta_3=-3\beta_1+\frac{1}{2}\beta_2\\
> \beta_4=6\beta_1-\frac{3}{2}\beta_2
> \end{matrix}\right.\\
> 则\alpha_1,\alpha_2是极大线性无关组,且\left\{\begin{matrix}
> \alpha_3=-3\alpha_1+\frac{1}{2}\alpha_2\\
> \alpha_4=6\alpha_1-\frac{3}{2}\alpha_2
> \end{matrix}\right.\quad (可以不写\beta直接写\alpha)
> $$

### 第四章:线性方程组

$$
对于一般方程组AX=\beta,\\
r(A)=r(A|\beta)\Rightarrow\left\{\begin{matrix}
r(A)=n,有唯一解\\
r(A)<n,有无穷多解
\end{matrix}\right.\\
r(A)<r(A|\beta)\Rightarrow 无解
$$

> 解线性方程组的一般步骤

1. 写出$(A|\beta)$
2. 进行初等行变换转化为阶梯型,判断是否有解
3. 若有解,继续进行初等行变换为行简化阶梯型
4. 将非零行首非零元1留在等号左面,其余放在等号右面

##### 齐次线性方程组

$r(A)=r(A|\beta)\quad (\beta=0)$,至少有零解
$$
\left\{\begin{matrix}
r(A)=n,仅有唯一零解\\
r(A)<n,有非零解
\end{matrix}\right.\\
\left\{\begin{matrix}
方程个数m<未知量个数n\Rightarrow 有非零解\\
方程个数m=未知量个数n,\ \  \left\{\begin{matrix}有非零解\Leftrightarrow |A|=0\\
只有零解\Leftrightarrow |A|\ne0\end{matrix}\right.
\end{matrix}\right.\\
$$

##### 解的结构

<div style="background:#cce1f3">齐次线性方程组</div> 

$$
对于Ax=0\\
\left\{\begin{matrix}
若\eta是它的解,则c\eta也是它的解\\
若\eta_1,\eta_2是它的解,则\eta_1+\eta_2也是它的解
\end{matrix}\right.
$$

> 基础解系

$$
定义基础解系:\eta_1,..,\eta_s\\
1.\eta_1,..,\eta_s线性无关\\
2.任何解都可以由\eta_1,..,\eta_s线性表示
$$

> 齐次线性方程组基础解系标准解法:

1. 对$A$进行初等行变换,转化为行最简阶梯型
2. 将非零行首非零元1留在等号左面,其余放在等号右面

3. 写出自由未知量(不在方程左面的未知量)
4. 令自由未知量为一组线性无关的量,求出对应的解
5. 得到$n-r(A)$个解构成基础解系

例:
$$
已知齐次线性方程组Ax=0\\
A=\rightarrow...\rightarrow\begin{pmatrix}
  1&  0&  -\frac{9}{4}&  -\frac{3}{4}&\frac{1}{4} \\
  0&  1&  \frac{3}{4}&-\frac{7}{4}  &\frac{5}{4} \\
  0&  0&  0&  0&0
\end{pmatrix}\\
则\left\{\begin{matrix}
x_1=\frac{9}{4}x_3+\frac{3}{4}x_4-\frac{1}{4}x_5\\
x_2=-\frac{3}{4}x_3+\frac{7}{4}x_4 -\frac{5}{4}x_5
\end{matrix}\right.\\
则x_3,x_4,x_5为自由未知量\\
令(x_3,x_4,x_5)^T分别取(1,0,0)^T,(0,1,0)^T,(0,0,1)^T,带入得到\\
\eta_1=(\frac{9}{4},-\frac{3}{4},1,0,0)^T,\eta_2=(\frac{3}{4},\frac{7}{4},0,1,0)^T,\eta_3=(-\frac{1}{4},-\frac{5}{4},0,0,1)^T\\
则\eta_1,\eta_2,\eta_3为Ax=0的基础解系\\
即Ax=0的任意解\eta都可以表示为\eta=c_1\eta_2+c_2\eta_2+c_3\eta_3(c1,c2,c3为任意常数)
$$

<div style="background:#cce1f3">非齐次线性方程组</div> 

$$
对于非齐次线性方程组Ax=b,称Ax=0为它的导出组\\
\left\{\begin{matrix}
若\alpha_1,\alpha_2是Ax=b的解,则\alpha_1-\alpha_2是Ax=0的解\\
若\alpha_0是Ax=b的解,\eta是Ax=0的解,则\alpha_0+\eta是Ax=b的解
\end{matrix}\right.
$$

> 解的结构

$$
\alpha_0是Ax=b的一个解(特解),\eta是Ax=0的通解\\
即\eta=c_1\eta_1+..+c_{n-r}\eta_{n-r},其中\eta_1,..,\eta_{n-r}是Ax=0的基础解系\\
则\alpha_0+c_1\eta_1+..+c_{n-r}\eta_{n-r}是Ax=b的全部解(通解)
$$

> 非齐次线性方程组的标准解法:

1. 写出$(A|b)$,只使用初等行变换化为行简化阶梯型
2. 写出同解方程组,指出自由未知量,并求出特解$\alpha_0$
3. 写出导出组的同解方程组,指出自由未知量,求出基础解系$\eta_1,..,\eta_{n-r}$
4. 得到$Ax=b$通解$\alpha_0+c_1\eta_1+..+c_{n-r}\eta_{n-r}$

##### 重要结论

> 矩阵$A_{m\cp n},B_{n\cp s},若AB=0,则r(A)+r(B)\le n\\$

$$
证明:AB=0\Rightarrow B的列向量都是AX=0的解\\
因此B的列向量是AX=0解集的子集\\
则B列向量组的秩,不大于方程组AX=0基础解系的个数\\
即r(B)\le n-r(A)\\
因此r(A)+r(B)\le n
$$

> $r(A|B)\le r(A)+r(B)$

$$
证明:设r(A|B)的列向量分别为\{\alpha_1,..,\alpha_s,\beta_1,..,\beta_t\}\\
设\{\alpha_1,..,\alpha_s,\beta_1,..,\beta_t\}的一个极大无关组为I\\
I_1为I中属于\alpha_1,..,\alpha_s中的向量组成的向量组\\
I_2为I中属于\beta_1,..,\beta_t中的向量组成的向量组\\
\begin{aligned}
从而r(A|B)&=r(\alpha_1,..,\alpha_s,\beta_1,..,\beta_t)\\
&=I向量个数\\
&=I_1向量个数+I_2向量个数\\
&\le r(\alpha_1,..,\alpha_s)+r(\beta_1,..,\beta_t)\\
&=r(A)+r(B)
\end{aligned}
$$

> $r(A\pm B)\le r(A)+r(B)$

$$
证明:r(A+B)\le r(A+B|B)\\
对矩阵(A+B|B)进行初等列变换:左边A+B各列都减去右边B的对应列,化为(A|B)\\
于是r(A+B)\le r(A+B|B)=r(A|B)\le r(A)+r(B)
$$

##### 注意事项:

先初等变换再矩阵乘积可能会改变秩

### 第五章:特征向量与特征值,相似,对角化

##### 特征值与特征向量

> 定义:

$$
A为n阶方阵,存在数\lambda和非零列向量\alpha使得A\alpha=\lambda\alpha\\
则称\lambda为\alpha的特征值,或者说\alpha为\lambda 的特征向量\\
称|\lambda E-A|=0为特征方程
$$

>  性质:

$$
如果\eta 是A的特征向量.特征值为\lambda ,则\eta也是A的任何多项式f(A)的特征向量,特征值为f(\lambda)\\
\lambda 是A的特征值,\alpha是对应的特征向量,对于\forall c\ne0,c\alpha也是\lambda的特征向量\\
若\alpha_1,\alpha_2是\lambda的特征向量,则c_1\alpha_1+c_2\alpha_2也是\lambda的特征向量\\
n阶对角型矩阵特征值为主对角线n个元素\\
若有\sum |a_{ij}|<1,i=1,..,n和\sum|a_{ij}|<1,j=1,..,n,则|\lambda_k|<1\\
对于n个特征值\lambda_1,..,\lambda_n,有\left\{\begin{matrix}
\sum_{i=1}^n\lambda_i=\sum_{i=1}^{n}a_{ii}=tr(A)\\
\lambda_1\lambda_2..\lambda_n=|A|
\end{matrix}\right.\\
互不相同的特征值\lambda_1,..,\lambda_m,对应的特征向量\alpha_1,..,\alpha_m线性无关\\
\left\{\begin{matrix}
互不相同的特征值对应的特征向量:\lambda_1对应(\alpha_{11},..\alpha_{1s}),..,\lambda_n对应(\alpha_{n1},..,\alpha_{nt}),\\则\alpha_{11},..,\alpha_{1s},..,\alpha_{n1},..,\alpha_{nt}全部放在一起仍然线性无关
\end{matrix}\right.\\
k重特征根对应的线性无关的特征向量的个数\le k\\
\left\{\begin{matrix}
A和A^T有相同的特征值\\
k\lambda是kA的特征值\\
\lambda^k是A^k的特征值\\
\frac{1}{\lambda}是A^{-1}的特征值\\
\frac{1}{\lambda}|A|是A^*的特征值\\
A可逆时,A,A^{-1},A^*的特征向量完全一样\\
A+E,A的特征值\lambda +1,A的特征向量不变
\end{matrix}\right.\\
r(A)\le 1\Rightarrow A的特征值为0,0,...,tr(A)
$$

##### 重要结论

$$
设\lambda 是n阶矩阵A的特征值,则它的重数\ge n-r(A-\lambda E)\\
\Rightarrow 特征值0的重数\ge n-r(A)\\
\Rightarrow 若r(A)=1,则重数\ge n-1,而\sum \lambda =tr(A)\\
\Rightarrow 前n-1个特征值为0,最后一个为tr(A)
$$

> 例题(完整步骤):

$$
求A=\begin{pmatrix}
  1&  -2&2 \\
  -2&  -2&4 \\
  2&  4&-2
\end{pmatrix}的特征值和特征向量\\
|\lambda E-A|=\begin{vmatrix}
  \lambda-1&2  &-2 \\
  2&\lambda+2  &-4 \\
  -2&  -4&\lambda+2
\end{vmatrix}=(\lambda +7)(\lambda-2)^2\\
则\lambda_1=-7,\lambda_2=\lambda_3=2\\
1)\lambda=-7,\lambda E-A=\begin{pmatrix}
  -8&  2&-2 \\
  2&  -5&-4 \\
  -2&  -4&-5
\end{pmatrix}\longrightarrow ...(见解的结构部分)\longrightarrow\\
得到特征向量c_1\begin{pmatrix}
 1\\
 2\\
-2
\end{pmatrix},c_1\ne0\\
2) \lambda_2=\lambda_3=2,\lambda E-A=\begin{pmatrix}
  1&  2&-2 \\
  2&  4&-4 \\
  -2&  -4&4
\end{pmatrix}\longrightarrow ...(见解的结构部分)\longrightarrow\\
得到特征向量c_2\begin{pmatrix}
 -2\\
 1\\
0
\end{pmatrix}+c_3\begin{pmatrix}
 2\\
 0\\
1
\end{pmatrix},c_2,c_3不同时为0(c_2c_3\ne0)\\
$$

##### 相似矩阵

> 定义:

$$
n的A,B方阵,若\exist n阶可逆矩阵P,使得P^{-1}AP=B,那么称A和B相似,记作A\sim B
$$

> 性质:

$$
自反性,对称性,传递性\\
数量矩阵只和自己相似\\
若A\sim B,则A和B有相同的特征值,且|A|=|B|,tr(A)=tr(B)\\
\left\{\begin{matrix}
若A\sim B\Rightarrow A^m\sim B^m\\
若A\sim B,A可逆\Leftrightarrow B可逆\\
若A,B还可逆,则A^{-1}\sim B^{-1},A^*\sim B^*\\P^{-1}A^{-1}P=B^{-1},P^{-1}A^*P=B^*\\
\end{matrix}\right.\\
若A\sim B,则\\
如果A\sim B,且P^{-1}AP=B,则\eta是A的特征向量\Leftrightarrow P^{-1}\eta是B的特征向量\\
如果A,B中有一个矩阵可逆,则AB\sim BA,证明:A^{-1}(AB)A=BA
$$

> + $A$和$B$相似,证明$A$和$B$的特征值相同
>
> $$
> 因为A\sim B,所以\exist 可逆矩阵P使得,P^{-1}AP=B\\
> 特征多项式|\lambda E-B|=|\lambda E-P^{-1}AP|=|\lambda P^{-1}EP-P^{-1}AP|\\
> =|P^{-1}(\lambda E-A)P|=|P^{-1}||\lambda E-A||P|=|\lambda E-A|\\
> 因此A和B的特征多项式相同,则特征值也相同
> $$
>
> + $B$的特征向量为$P^{-1}\eta$
>   $$
>   A\eta=\lambda\eta,而A=PBP^{-1}\\
>   PBP^{-1}\eta=\lambda\eta\ \Rightarrow B(P^{-1}\eta)=\lambda (P^{-1}\eta)\\
>   所以B的特征向量为P^{-1}\eta
>   $$

<div style="background:#cce1f3">与对角型相似</div> 

> 充要条件:

$$
A相似于对角型\Leftrightarrow A有n个线性无关的特征向量\Leftrightarrow r_i重特征根的基础解系有r_i个解
$$

> 性质:

$$
A有n个互异的特征值\lambda_1,..,\lambda_n,则A\sim\begin{pmatrix}
  \lambda_1&  &  & \\
  &  \lambda_2&  & \\
  &  &  ..& \\
  &  &  &\lambda_n
\end{pmatrix}
$$

> 例题

$$
求A=\begin{pmatrix}
  3&  2&-1 \\
  -2& -2&2 \\
  3&  6&-1
\end{pmatrix}是否相似于对角型,若相似P=?,\Lambda=?\\
|\lambda E-A|=..按上面求出特征值和特征向量=..\\
\left\{\begin{matrix}
\lambda_1=-1时,特征向量为\alpha_1=\begin{pmatrix}
 \frac{1}{3}\\
 -\frac{2}{3}\\
1
\end{pmatrix}\\
\lambda_2=\lambda_3=2时,\alpha_2=\begin{pmatrix}
-2\\
 1\\
0
\end{pmatrix},\alpha_3=\begin{pmatrix}
1\\
0\\
1
\end{pmatrix}\\
\end{matrix}\right.\\
则A相似于对角型,且P=(\alpha_1,\alpha_2,\alpha_3),对应的\Lambda=\begin{pmatrix}
  -4&  & \\
  &  2& \\
  &  &2
\end{pmatrix}
$$

$$
A=\begin{pmatrix}
  0&  1&-1 \\
  -2&  0&2 \\
  -1& 1 &0
\end{pmatrix},求A^{100}\\
此处省略一万步\\
\lambda_1=-1,\alpha_1=\begin{pmatrix}
1\\
0\\
1
\end{pmatrix},\quad
\lambda_2=0,\alpha_2=\begin{pmatrix}
1\\
1\\
1
\end{pmatrix},\quad
\lambda_3=1,\alpha_3=\begin{pmatrix}
1\\
4\\
3
\end{pmatrix}\\
P=\begin{pmatrix}
  1&  1&1 \\
  0&  1&4 \\
  1& 1 &3
\end{pmatrix},\Lambda=\begin{pmatrix}
  -1&  & \\
  &  0& \\
  &  &1
\end{pmatrix}
而P^{-1}AP=\Lambda,则A=P\Lambda P^{-1}\\
A^{100}=(P\Lambda P^{-1})^{100}=P\Lambda^{100}P^{-1}=..
$$

##### 正交矩阵

> 定义:$A$为$n$阶方阵,$A^TA=E$

> 充要条件:$A$正交$\Leftrightarrow A$的列(行)向量组是标准正交向量组
>
> 性质:

$$
内积:(\alpha,\beta)=\alpha^T\beta\\
若A为n阶正交矩阵\\
|A|=1\ or\ -1\\
A^{-1}=A^T,且A^{-1}和A^T均为正交矩阵\\
若A和B为n阶正交矩阵,则AB为正交矩阵\\
若A为正交矩阵,\alpha,\beta为列向量,则(A\alpha,A\beta)=(\alpha,\beta)
$$
<div style="background:#cce1f3">施密特正交化</div> 

> 定义:给一组线性无关的$\alpha_1,..,\alpha_s$,求与之等价的正交向量组$\beta_1,..\beta_s$

$$
\begin{aligned}
\beta_1&=\alpha_1,\\
\beta_2&=\alpha_2-\frac{(\alpha_2,\beta_1)}{\beta_1,\beta_1}\beta_1\\
\beta_3&=\alpha_3-\frac{(\alpha_3,\beta_1)}{\beta_1,\beta_1}\beta_1-\frac{(\alpha_3,\beta_2)}{\beta_2,\beta_2}\beta_2\\&......
\end{aligned}
$$

##### 实对称矩阵的对角化

> 实对称矩阵的性质:
>
> 实对称矩阵$A$的不同特征值对应的特征向量是正交的。

所有实对称矩阵都能对角化

正交向量组中不能有零向量
$$
实对称矩阵A的不同特征值\lambda_1,..,\lambda_n对应的特征向量\alpha_1,..,\alpha_s正交\\
实对称矩阵A,一定\exist 正交矩阵Q使得Q^{-1}AQ=Q^TAQ=\Lambda=\begin{pmatrix}
  \lambda_1&  & \\
  &  ..& \\
  &  &\lambda_n
\end{pmatrix}
$$

> 正交相似:$A,B$同为$n$阶矩阵,若$\exist$ 正交矩阵$P$使得$P^{-1}AP=B$,那么称$A$和$B$正交相似

> 解题过程:
>
> 求出特征值后,若全为单根,则已经正交化,只需单位化
>
> 若为单根和重根,重根需做正交化
>
> 若全为重根,则均需要正交化

### 第六章:二次型

<div style="background:#cce1f3">二次型->矩阵表达式</div> 

+ 平方项的系数直接作为主对角线元素
+ 交叉项的系数除以2放在两个对称的相应位置上

> 举例:
> $$
> x_1^2+2x_1x_2+x_2^2-x_2x_3+2x_3^2-2x_1x_3=\\
> (x_1,x_2,x_3)\begin{pmatrix}
>   1&  1&-1 \\
>   1&  1&-\frac{1}{2} \\
>   -1&  -\frac{1}{2}&2
> \end{pmatrix}\begin{pmatrix}
>  x_1\\
>  x_2\\
> x_3
> \end{pmatrix}
> $$

记作$X^TAX$,$A$称为该二次型的矩阵,且定义$A$的秩即为二次型的秩

显然,二次型矩阵一定对称,即$A^T=A$

<div style="background:#cce1f3">标准型</div> 

$$
d_1y_1^2+d_2y_2^2+...+d_ny_n^2
$$

线性替换:$X=CY$

$|C|\ne0$,称为可逆的非退化的替换

$|C|=0$,称为退化的替换

线性替换后,二次型矩阵仍对称

<div style="background:#cce1f3">正惯性指数</div>

> 给定实对称矩阵$A$,在与$A$合同的矩阵的对角线元素中,正的个数为正惯性指数,负数个数即为负惯性指数

<div style="background:#cce1f3">合同</div>

> 定义:

$$
对于n阶方阵A,B,如果存在可逆矩阵C使得C^TAC=B,那么称A和B合同\\
充要条件:对于两个实对称矩阵,他们的正负惯性指数都相同|它们的特征值正负情况相同
$$

> 性质:

$$
反身性|对称性|传递性\\
A\simeq B\Rightarrow r(A)=r(B)\\
若A\simeq B,则A^T=A\Leftrightarrow B^T=B\\
若A\simeq B,且A,B可逆,则若A^{-1}\simeq B^{-1}\\
若A\simeq B,则A^T\simeq B^T
$$

<div style="background:#cce1f3">化二次型为标准型</div> 

> 定义: 构造可逆实矩阵$C$,使得$C^TAC$为对角矩阵

> 配方法/初等变换法/正交变换法

+ 配方法

> 要点:先配$x_1,$再$x_2,..,$以此类推
>
> 配完$x_i后,x_i$应该不再出现

$$
\begin{aligned}
&x_1^2-3x_2^2+4x_3^2-2x_1x_2+2x_1x_3-6x_2x_3\\
&=x_1^2-2x_1(x_2-x_3)+(x_2-x_3)^2-(x_2-x_3)^2-3x_2^2+4x_3^2-6x_2x_3\\
&=(x_1-x_2+x_3)^2-4x_2^2-4x_2x_3+3x_3^2\\
&=(x_1-x_2+x_3)^2-(2x_2+x_3)^2+4x_3^2\\
&=y_1^2-y_2^2+4y_3^2
\end{aligned}
$$

$$
则线性替换为\left\{\begin{matrix}
\begin{aligned}
x_1&=y_1+\frac{1}{2}y_2-\frac{3}{2}y_3\\
x_2&=\frac{1}{2}y_2-\frac{1}{2}y_3\\
x_3&=y_3
\end{aligned}
\end{matrix}\right.
$$

> 对于特殊情况,如只有交叉项
> $$
> 2x_1x_2-4x_1x_3+10x_2x_3\\
> 令\left\{\begin{matrix}
> \begin{aligned}
> x_1&=y_1-y_2\\
> x_2&=y_1+y_2\\
> x_3&=y_3
> \end{aligned}
> \end{matrix}\right.带入\\
> 原式=2y_1^2-2y_2^2+6y_1y_3+14y_2y_3,此时可使用配方法求解
> $$

+ 初等变换法

> 要点:对$A$和$E$做同样的初等列变换,只对$A$做相应的初等行变换
>
> $A$化为对角型之时,$E$化为$C$

$$
A=\begin{pmatrix}
  1&  1&1 \\
  1&2  &2 \\
  1& 2 &1
\end{pmatrix}\\
\begin{pmatrix}
 A\\
E
\end{pmatrix}=\begin{pmatrix}
  1&  1&1 \\
  1&2  &2 \\
  1& 2 &1\\
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}\longrightarrow\begin{pmatrix}
  1&  0&1 \\
  0&1  &1 \\
  1& 1 &1\\
1&-1&0\\
0&1&0\\
0&0&1
\end{pmatrix}\longrightarrow\begin{pmatrix}
  1&  0&0 \\
  0&1  &1 \\
  0& 1 &0\\
1&-1&-1\\
0&1&0\\
0&0&1
\end{pmatrix}\longrightarrow\begin{pmatrix}
  1&  0&0 \\
  0&1  &0 \\
  0& 0 &-1\\
1&-1&0\\
0&1&-1\\
0&0&1
\end{pmatrix}\\
则\Lambda=\begin{pmatrix}
  1&  & \\
  &  1& \\
  &  &-1
\end{pmatrix},\quad C=\begin{pmatrix}
  1&  -1& \\
  &  1&-1 \\
  &  &1
\end{pmatrix}
$$

规范型:
$$
形如
$$

+ 正交替换法

同实对称矩阵对角化

##### 有定性

> 正定矩阵:设$A$为$n$阶方阵.,如果对任何非零向量$X$,都有$X^TAX>0$,那么称$A$为正定矩阵

> 如果$A$为实矩阵,那么$A^TA$为实对称半正定矩阵,特征值为非负实数
> $$
> 证明:设特征值为\lambda,对应的特征向量为\eta\\
> A^TA\eta=\lambda\eta\Rightarrow \eta^TA^TA\eta=\lambda\eta^T\eta\\
> 则\lambda=\frac{(A\eta,A\eta)}{(\eta,\eta)},而(A\eta,A\eta)\ge0,\ (\eta,\eta)\ge0\\
> 因此\lambda\ge 0
> $$
> 如果$A$为实反对称矩阵,那么它的特征值为$0$或者纯虚数
> $$
> 证明:A^T=-A\\
> 则A^TA=-A^2,由上文知A^TA的特征值为非负实数,因此-A^2的特征值为非负实数\\
> 则A^2的特征值为非正实数,那么A的特征值要么为0要么为纯虚数
> $$

正定二次型经过线性替换仍然正定
$$
\begin{aligned}
f(x)=X^TAX正定&\Leftrightarrow 标准型是d_1y_1^2+d_2y_2^2+...+d_ny_n^2,且d_i>0\\
&\Leftrightarrow正惯性指数为n\\
&\Leftrightarrow A\simeq E\\
&\Leftrightarrow n个特征值>0\\
&\Leftrightarrow 各阶顺序主子式>0\\
&\Rightarrow |A|>0
\end{aligned}
$$

$$
A正定\Rightarrow A^{-1}正定\\
\Rightarrow A^* 正定\\
\Rightarrow A^k 正定\\
\Rightarrow A的主对角线元素全>0\\
A正定,B(半)正定\Rightarrow A+B正定
$$



> 顺序主子式:$正定\Leftrightarrow 顺序主子式全>0$

$$
对于f(x_1,x_2,x_3)=2x_1^2+2x_1x_2+x_2^2+x_3^2\\
A=\begin{pmatrix}
  2&  1&0 \\
  1&1  &0 \\
  0& 0 &1
\end{pmatrix}\\
一阶主子式(2)>0\\
二阶主子式\begin{pmatrix}
  2&  1 \\
  1&1   \\
\end{pmatrix}=1>0\\
三阶主子式\begin{pmatrix}
  2&  1&0 \\
  1&1  &0 \\
  0& 0 &1
\end{pmatrix}=1>0\\
因此f(x_1,x_2,x_3)是正定的
$$

### 线性空间

过渡矩阵:
$$
已知\alpha_1,..,\alpha_n和\beta_1,..,\beta_n是基\\
且(\beta_1,..,\beta_n)=(\alpha_1,..,\alpha_n)\begin{pmatrix}
  a_{11}&  ..&a_{1n} \\
  ..&  &.. \\
  a_{n1}& .. &a_{nn}
\end{pmatrix}\\
那么称A=\begin{pmatrix}
  a_{11}&  ..&a_{1n} \\
  ..&  &.. \\
  a_{n1}& .. &a_{nn}
\end{pmatrix}是\alpha_1,..,\alpha_n到\beta_1,..,\beta_n的过渡矩阵
$$


### 常考点

$$
A_{ij}=a_{ij}\Rightarrow A^T=A^*\\
正交相似\rightarrow 相似\ and\ 合同\rightarrow 等价
$$

$$
n阶矩阵A满足f(A)=t且A的特征值为\lambda,则f(\lambda)=t\\
例(A-aE)(A-bE)=0,则A的特征值\lambda 满足(\lambda-a)(\lambda-b)=0\\
因此特征值\lambda 只能为a或b(不能确定有哪些,只能确定范围)
$$



##### 秩

$$
AB=0\Rightarrow r(A)+r(b)\le n\\
r(A\pm B)\le r(A)+r(B)
$$

##### 特征值与特征向量

$$
n阶矩阵A的个行元素均为k,则A[1,..,1]^T=k[1,..,1]\\
k为特征值,对应的特征向量为[1,..,1]
$$

$$
\alpha\alpha^T是一个秩为1的实对称矩阵,并且\alpha是它的特征向量
$$





##### 注意事项

由于求解方程组时只能使用初等行变换,因此如果在求$|\lambda E-A|$时用到了列变换,那么$\lambda$代回时不能代到最后化简过的式子中

P439 例5.38
