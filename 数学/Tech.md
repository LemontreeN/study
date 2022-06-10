##### 等价无穷小问题:注意 '1'

##### 积分技巧

对于形如$\int xdV$,可以利用质心/形心公式化为$\bar{x}\int 1dV$转化为求几何体面积/体积

##### 怎么把极坐标$\int d\theta\int Fdr$交换积分次序

$$
画出\theta Or平面图像,类似于xOy平面进行处理
$$

##### 对含有$\sqrt{x^2+y^2}$的式子求导

$$
令r=\sqrt{x^2+y^2},则r'_x=\frac{x}{r},r'_y=\frac{y}{r}\\
可大幅度简化运算
$$

##### 求形如$\int\frac{\sin x}{a\sin x+b\cos x}dx$的积分

$$
设\sin x=k(a\sin x+b\cos x)+p(a\sin x+b\cos x)'\\
=(ka-pb)\sin x+(kb+pa)\cos x\\
令ka-pb=1,kb+pa=0,则k=\frac{a}{a^2+b^2},p=\frac{-b}{a^2+b^2}\\
I=\int\frac{k(a\sin x+b\cos x)}{a\sin x+b\cos x}+\int\frac{p(a\sin x+b\cos x)'}{a\sin x+b\cos x}dx\\
=k\int dx+p\int \frac{1}{a\sin x+b\cos x}d(a\sin x+b\cos x)\\
=kx+p\ln|a\sin x+b\cos x|+C\\
=\frac{a}{a^2+b^2}x+\frac{-b}{a^2+b^2}\ln|a\sin x+b\cos x|+C
$$

##### 函数周期

> 660第195题CD选项

$$
设f(x)在(-\infty,+\infty)上连续,以T为周期且为奇函数,则\int_0^x f(t)dt也是以T为周期的奇函数\\
设f(x)在(-\infty,+\infty)上连续,以T为周期且\int_0^\infty f(x)dx收敛,则\int_0^x f(t)dt也是以T为周期的奇函数
$$

##### 要背的知识点:

> 这个证明很麻烦

$$
\int \frac{dx}{\sqrt[]{x^2\pm a^2} }&=\ln \vert\  x+\sqrt[]{x^2\pm a^2}\ \vert+C\\
$$

