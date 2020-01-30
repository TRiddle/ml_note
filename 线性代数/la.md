[toc]

## 1 线形方程组

### 1.1 线性方程组

![](./pic/1.1.1.png)

![](./pic/1.1.2.png)

![](./pic/1.1.3.png)

### 1.2 行化简与阶梯形矩阵

![](./pic/1.2.1.png)

![](./pic/1.2.2.png)

![](./pic/1.2.3.png)

#### 行化简算法

![](./pic/1.2.5.png)

#### 线性方程组的解

![](./pic/1.2.6.png)

**例1.2.4**：求方程组的解，该方程组的增广矩阵已经化为

$\left(\begin{matrix}1&6&2&-5&-2&-4\\0&0&2&-8&-1&3\\0&0&0&0&1&7\end{matrix}\right)$

解：将其化为简化阶梯形：

$\left(\begin{matrix}1&6&0&3&0&0\\0&0&1&-4&0&5\\0&0&0&0&1&7\end{matrix}\right)$

主元列为1，3，5列，基本变量为$x_1, x_3, x_5$，自由变量为：$x_2, x_4$，其对应的方程组为：

$x_1+6x_2+3x_4=0\\x_3-4x_4=5\\x_5=7$

通解为

$x_1+6x_2+3x_4=0$

$x_2$ 为自由变量

$x_3-4x_4=5$

$x_4$ 为自由变量

$x_5=7$

#### 存在与唯一性问题

![](./pic/1.2.4.png)

**例1.2.5**：确定方程组的解是否存在且唯一。方程组的增广矩阵化简为：

$\left(\begin{matrix}3&-9&12&-9&6&15\\0&2&-4&4&2&-6\\0&0&0&0&1&4\end{matrix}\right)$

解：因为没有不相容的方程组，所以方程组有解。因为存在自由变量，所以方程组的解不是唯一的。

### 1.3 向量方程

### 1.4 矩阵方程Ax=b

### 1.5 线性方程组的解集

![](./pic/1.5.1.png)

**例1.5.1**：确定下列其次线性方程组是否有平凡解，并描述他的子集

$3x_1+5x_2-4x_3=0\\-3x_1-2x_2+4x_3=0\\6x_1+x_2-8x_3=0$

解：写出增广矩阵(A 0)

$\left(\begin{matrix}3&5&-4&0\\-3&-2&4&0\\6&1&-8&0\end{matrix}\right)$

施以行变换，化为阶梯形

$\left(\begin{matrix}3&5&-4&0\\0&3&0&0\\0&0&0&0\end{matrix}\right)$

$x_3$ 是自由变量，因此Ax = 0有平凡解。继续施以行变换，化为简化阶梯形：

$\left(\begin{matrix}1&0&-\frac{4}{3}&0\\0&1&0&0\\0&0&0&0\end{matrix}\right)$

用自由变量表示基本变量

$x = \left(\begin{matrix}\frac{4}{3}\\0\\1\end{matrix}\right)x_3$

**例1.5.3** ：描述Ax = b的解，其中

$A = \left(\begin{matrix}3&5&-4\\-3&-2&4\\6&1&-8\end{matrix}\right), b = \left(\begin{matrix}7\\-1\\-4\end{matrix}\right)$

解：写出增广矩阵(A b)

$\left(\begin{matrix}3&5&-4&7\\-3&-2&4&-1\\6&1&-8&4\end{matrix}\right)$

施以行变换，化为简化阶梯形

$\left(\begin{matrix}1&0&-\frac{4}{3}&-1\\0&1&0&2\\0&0&0&0\end{matrix}\right)$

$x_3$ 为自由变量，Ax = b的通解为

$x = \left(\begin{matrix}-1\\2\\0\end{matrix}\right) + \left(\begin{matrix}\frac{4}{3}\\0\\1\end{matrix}\right)x_3$

![](./pic/1.5.2.png)

## 2 矩阵代数

### 2.2 矩阵的逆

![](./pic/2.2.1.png)

![](./pic/2.2.2.png)

**例2.2.2** ：求 $A = \left(\begin{matrix}3&4\\5&6\end{matrix}\right)$ 的逆。

解：$det A = -2 \ne 0$ ，故A可逆，且

$A^{-1} = -\frac{1}{2}\left(\begin{matrix}6&-4\\-5&3\end{matrix}\right) = \left(\begin{matrix}-3&2\\\frac{5}{2}&-\frac{3}{2}\end{matrix}\right)$ 

![](./pic/2.2.3.png)

**例2.2.4** ：解方程：

$3x_1+4x_2=3\\5x_1+6x_2=7$

解：

方程可以写成矩阵的形式：

 $Ax = \left(\begin{matrix}3&4\\5&6\end{matrix}\right)\left(\begin{matrix}x_1\\x_2\end{matrix}\right)=\left(\begin{matrix}3\\7\end{matrix}\right) = b$ 

$x = A^{-1}b = \left(\begin{matrix}-3&2\\\frac{5}{2}&-\frac{3}{2}\end{matrix}\right)\left(\begin{matrix}3\\7\end{matrix}\right) = \left(\begin{matrix}5\\-3\end{matrix}\right)$ 

![](./pic/2.2.4.png)

![](./pic/2.2.5.png)

![](./pic/2.2.6.png)

#### 初等矩阵

![](./pic/2.2.7.png)

![](./pic/2.2.8.png)

**例2.2.6**：求$E = \left(\begin{matrix}1&0&0\\0&1&0\\-4&0&1\end{matrix}\right)$ 的逆

解：为把E变成I，需要对E施加的初等行变换为：将第1行的4倍加到第3行中去，其对应的初等矩阵即E的逆：

$E^{-1} = \left(\begin{matrix}1&0&0\\0&1&0\\4&0&1\end{matrix}\right)$

#### 求$A^{-1}$ 的算法 

![](./pic/2.2.9.png)

![](./pic/2.2.10.png)

  **例2.2.7**：若矩阵 $ \left(\begin{matrix}0&1&2\\1&0&3\\4&-3&8\end{matrix}\right)$ 的逆存在的话，求其逆

解： $ \left(\begin{matrix}A&I\end{matrix}\right) = \left(\begin{matrix}0&1&2&1&0&0\\1&0&3&0&1&0\\4&-3&8&0&0&1\end{matrix}\right) \sim \left(\begin{matrix}1&0&0&-9/2&7&-3/2\\0&1&0&-2&4&-1\\0&0&1&3/2&-2&1/2\end{matrix}\right)$

根据定理7，因为$A \sim I$ 所以A可逆，且

$A^{-1} = \left(\begin{matrix}-9/2&7&-3/2\\-2&4&-1\\3/2&-2&1/2\end{matrix}\right)$

#### 逆矩阵的另一个观点

![](./pic/2.2.11.png)

## 3 行列式

## 4 向量空间

### 4.1 向量空间与子空间

![](./pic/4.1.1.png)

**例4.1.5**：设V是定义在集合D上的全实函数的集合（D的例子有实数集，实轴上的区间），加法的结果f+g仍为函数，在D中t点的值为f(t)+g(t)，同样，标量乘法的结果cf仍为函数，在t的值为cf(t)。例如，若$D=R,f(t)=1+\sin t,g(t)=2+0.5t$ ，则$(f+g)(t)=3+\sin 2t+0.5t, (2g)(t)=4+t$。证明V为一个向量空间。

证明：

1. f+g仍在V中（显然）
2. f+g=g+f（实数性质）
3. (f+g)+h=f+(g+h)（实数性质）
4. 零向量为f(t)=0
5. f的负向量为(-1)f
6. cf在V中（显然）
7. c(f+g)=cf+cg（实数性质）
8. (c+d)f=cf+df（实数性质）
9. c(df)=(cd)f（实数性质）
10. 1f=f（实数性质）

#### 子空间

![](./pic/4.1.2.png)

![](./pic/4.1.3.png)

#### 由集合生成的子空间

![](./pic/4.1.4.png)

**例4.1.11**：令H是所有形如(a-3b, b-a, a, b)的向量的集合，这里a, b是任意数，即$H=\{(a-3b,b-a,a,b):a,b\in R\}$，证明H是$R^4$ 的一个子空间。

证明：$\left(\begin{matrix}a-3b\\b-a\\a\\b\end{matrix}\right)=a\left(\begin{matrix}1\\-1\\1\\0\end{matrix}\right)+b\left(\begin{matrix}-3\\1\\0\\1\end{matrix}\right) = av_1+bv_2$ ，因此$H=Span\{v_1, v_2\}$ ，根据定理1，H是$R^4$ 的子空间。

### 4.2 零空间、列空间和线性变换

#### 矩阵的零空间

![](./pic/4.2.1.png)

例4.2.1： $A = \left(\begin{matrix}1 & 2 & 3\\4 & 5 & 6\\7 & 8 & 9  \end{matrix}\right), u=\left(\begin{matrix}5\\3\\-2\end{matrix}\right)$ ，确认u是否属于A的零空间。

 解：Au = 0，故u属于A的零空间

![](./pic/4.2.2.png)

**例4.2.2**：令H是$R^4$ 中满足坐标a, b, c, d满足方程a-2b+5c=d且c-a=b的所有向量的集合，证明H是$R^4$ 的一个子空间。

解：上述方程等价于 $\left(\begin{matrix}1&-2&5&-1\\-1&-1&1&0\end{matrix}\right) \left(\begin{matrix}a\\b\\c\\d\end{matrix}\right) = 0$ ，因此H是$R^4$ 的一个子空间

**例4.2.3**：求矩阵$A = \left(\begin{matrix}-3&6&-1&1&-7\\1&-2&2&3&-1\\2&-4&5&8&-4\end{matrix}\right)$ 的零空间的生成集。

对增广矩阵施以行变换，得到简化阶梯形

$\left(\begin{matrix}1&-2&0&-1&3&0\\0&0&1&2&-2&0\\0&0&0&0&0&0\end{matrix}\right)$

自由变量为$x_2, x_3, x_4$ ，解集为

$x = \left(\begin{matrix}2\\1\\0\\0\\0\end{matrix}\right)x_2+\left(\begin{matrix}1\\0\\-2\\1\\0\end{matrix}\right)x_3+\left(\begin{matrix}-3\\0\\2\\0\\1\end{matrix}\right)x_4=ux_2+vx_3+wx_4$

因为u, v, w的任意线性组合都在Nul A中，所以Nul A的一个生成集为

{u, v, w}

![](./pic/4.2.3.png)

#### 矩阵的列空间

![](./pic/4.2.4.png)

**例4.2.4**：求一个矩阵A使得W=Col A，其中

$W = \left\{\left(\begin{matrix}6a-b\\a+b\\-7a\end{matrix}\right):a,b\in R\right\}$

解：

$W = \left\{\left(\begin{matrix}6\\1\\-7\end{matrix}\right)a+\left(\begin{matrix}-1\\1\\0\end{matrix}\right)b:a,b\in R\right\} = Span\left\{\left(\begin{matrix}6\\1\\-7\end{matrix}\right), \left(\begin{matrix}-1\\1\\0\end{matrix}\right)\right\}$

可以看出，W为两个向量的线性组合，即

$W = Span\left\{\left(\begin{matrix}6\\1\\-7\end{matrix}\right), \left(\begin{matrix}-1\\1\\0\end{matrix}\right)\right\}$

用生成集中的向量作为A的列就有

$A = \left(\begin{matrix}6&-1\\1&1\\-7&0\end{matrix}\right)$

#### 线性变换的核与值域

![](./pic/4.2.5.png)

![](./pic/4.2.6.png)

![](./pic/4.2.7.png)

### 4.3 线性无关集和基

![](./pic/4.3.1.png)

**例4.3.1**：$p_1(t)=1,p_2(t)=t,p_3(t)=4-t$ ，证明$\{p_1,p_2,p_3\}$ 线性相关。

证明：因为$p_3=4p_1-p_2$ ，故命题得证

![](./pic/4.3.2.png)

**例4.3.2**：令$v_1 = \left(\begin{matrix}3\\0\\-6\end{matrix}\right), v_2 = \left(\begin{matrix}-4\\1\\7\end{matrix}\right), v_3 = \left(\begin{matrix}-2\\1\\5\end{matrix}\right)$，判断$\{v_1, v_2, v_3\}$ 是$R^3$ 的一个基。

解：根据可逆矩阵定理，若 $A = (v_1\ v_2\ v_3)$ 可逆则能构成基。因为$Det A = 6 \ne 0$，所以 $\{v_1, v_2, v_3\}$ 是$R^3$ 的一个基

#### 生成集定理

![](./pic/4.3.3.png)

![](./pic/4.3.4.png)

#### NulA和ColA的基

![](./pic/4.3.5.png)

![](./pic/4.3.6.png)

**例4.3.9**：已知$A = \left(\begin{matrix}a_1&a_2&a_3&a_4&a_5\end{matrix}\right) = \left(\begin{matrix}1&4&0&2&-1\\3&12&1&5&5\\2&8&1&3&2\\5&20&2&8&8\end{matrix}\right)$ ，求ColA的一个基

对A施以初等行变换，得到化简阶梯阵

$B= \left(\begin{matrix}b_1&b_2&b_3&b_4&b_5\end{matrix}\right) = \left(\begin{matrix}1&4&0&2&0\\0&0&1&-1&0\\0&0&0&0&1\\0&0&0&0&0\end{matrix}\right)$

故B的每个非主元列是主元列的线性组合，其中 $b_2=4b_1, b_4=2b_1-b_3$。

对应地，A的每个非主元列是主元列的线性组合，其中 $a_2=4a_1, a_4=2a_1-a_3$。

所以ColA的一个基为$\{a_1, a_3, a_5\}$

### 4.4 坐标系

![](./pic/4.4.1.png)



![](./pic/4.4.2.png)

**例4.4.1**：考虑$R^2$ 上的基$B = \{b_1, b_2\} = \{\left(\begin{matrix}1 \\ 0\end{matrix}\right), \left(\begin{matrix}1 \\ 2\end{matrix}\right)\}$ ，假设$R^2$ 中一向量x具有坐标向量$[x]_B = \left(\begin{matrix}-2\\3\end{matrix}\right)$ ，求x。

解：将基按照坐标向量做线性组合即可得到原向量：

$x = -2 \cdot \left(\begin{matrix}1 \\ 0\end{matrix}\right)+ 3 \cdot \left(\begin{matrix}1 \\ 2\end{matrix}\right) = \left(\begin{matrix}1 \\ 6\end{matrix}\right)$ 

#### 坐标的几何意义

![](./pic/4.4.3.png)

#### $R^n$中的坐标

![](./pic/4.4.4.png)

![](./pic/4.4.5.png)

#### 坐标映射

![](./pic/4.4.6.png)

![](./pic/4.4.7.png)

![](./pic/4.4.9.png)

**例4.4.7**：令$v_1 = \left(\begin{matrix}3\\6\\2\end{matrix}\right), v_2 = \left(\begin{matrix}-1\\0\\1\end{matrix}\right), x = \left(\begin{matrix}3\\12\\7\end{matrix}\right), B = \{v_1, v_2\}$ ，则B是$H = Span\{v_1, v_2\}$ 的一个基，判定x是否在H中。若在，求x相对于B的坐标向量。

解：若x在H中，则下列方程是相容的，并且其解就是x的B-坐标：

$\left(\begin{matrix}3&-1\\6&0\\2&1\end{matrix}\right) \left(\begin{matrix}c_1\\c_2\end{matrix}\right) = \left(\begin{matrix}3\\12\\7\end{matrix}\right)$

写出增广矩阵，并施以行变换

$\left(\begin{matrix}3&-1&3\\6&0&12\\2&1&7\end{matrix}\right) \sim \left(\begin{matrix}1&0&2\\0&1&3\\0&0&0\end{matrix}\right)$

可以看出方程确实是相容的，并且

$[x]_B = \left(\begin{matrix}2\\3\end{matrix}\right)$

H是$R^3$中与$R^2$同构的平面，由B确定的H上的坐标系如下图所示：

![](./pic/4.4.8.png)

### 4.5 向量空间的维数

### 4.6 秩

### 4.7 基的变换

![](./pic/4.7.1.png)

![](./pic/4.7.2.png)

**例4.7.1**：对一个向量空间V，考虑两个基$B=\{b_1, b_2\}, C=\{c_1, c_2\}$ ，满足

$b_1 = 4c_1+c_2\\b_2=-6c_1+c_2$

假设$x=3b_1+b_2$ ，也就是说$[x]_B=\left(\begin{matrix}3\\1\end{matrix}\right)$，求$[x]_C$

解：$[x]_C = [3b_1+b_2]_C = 3[b_1]_C+[b_2]_C$

$b_1 = 4c_1+c_2$ 给出了$[b_1]_C = \left(\begin{matrix}4\\1\end{matrix}\right)$

$b_2=-6c_1+c_2$ 给出了$[b_2]_C = \left(\begin{matrix}-6\\1\end{matrix}\right)$

因此$[x]_C = \left(\begin{matrix}4&-6\\1&1\end{matrix}\right)\left(\begin{matrix}3\\1\end{matrix}\right) = \left(\begin{matrix}6\\4\end{matrix}\right)$

（其中 $\left(\begin{matrix}4&-6\\1&1\end{matrix}\right)$ 就是$P_{C\leftarrow B}$）

#### $R^n$ 中的基变换

![](./pic/4.7.3.png)

![](./pic/4.7.4.png)

![](./pic/4.7.5.png)

![](./pic/4.7.6.png)

（对大矩阵而言，第一种方法会更快）

**例4.7.3**：设$b_1 = \left(\begin{matrix}1\\-3\end{matrix}\right), b_2 = \left(\begin{matrix}-2\\4\end{matrix}\right), c_1 = \left(\begin{matrix}-7\\9\end{matrix}\right), c_2 = \left(\begin{matrix}-5\\7\end{matrix}\right)$，考虑$R^2$ 中的基$B = \{b_1, b_2\}, C = \{c_1, c_2\}$ 

a. 求C到B的坐标变换矩阵

b. 求B到C的坐标变换矩阵

解：

a. 由$\left(\begin{matrix}b_1&b_2&c_1&c_2\end{matrix}\right) = \left(\begin{matrix}1&-2&7&5\\-3&4&9&7\end{matrix}\right) \sim \left(\begin{matrix}1&0&5&3\\0&1&6&4\end{matrix}\right)$ 得$P_{B\leftarrow C} = \left(\begin{matrix}5&3\\6&4\end{matrix}\right)$

b. 因为坐标变换矩阵一定是可逆的，所以$P_{C\leftarrow B} = P^{-1}_{B\leftarrow C} = \frac{1}{2}\left(\begin{matrix}4&-3\\-6&5\end{matrix}\right)= \left(\begin{matrix}2&-3/2\\-3&5/2\end{matrix}\right)$

### 4.8 差分方程中的应用

### 4.9 马尔可夫链中的应用

## 5 特征值与特征向量

### 5.1 特征向量与特征值

![](./pic/5.1.1.png)

**例5.1.3**：证明7是矩阵$A = \left(\begin{matrix}1&6\\5&2\end{matrix}\right)$ 的特征值，并求特征值7对应的特征向量

解：7是A的特征值当且仅当Ax=7x有非平凡解，方程移项得

$(A-7I)x=0$

$(A-7I) = \left(\begin{matrix}-6&6\\5&-5\end{matrix}\right)$ 列线性相关，故方程有非平凡解

对增广矩阵施以行变换

$\left(\begin{matrix}-6&6&0\\5&-5&0\end{matrix}\right) \sim \left(\begin{matrix}1&-1&0\\0&0&0\end{matrix}\right)$

得到通解$x = x_2\left(\begin{matrix}1\\1\end{matrix}\right)$，凡是$x_2 \ne 0$ 的具有这种形式的向量都是特征值7对应的特征向量

![](./pic/5.1.2.png)

![](./pic/5.1.3.png)

**例5.1.4**：设 $A = \left(\begin{matrix}4&-1&6\\2&1&6\\2&-1&8\end{matrix}\right)$ ，A的一个特征值是2，求对应的特征空间的一个基

解：A - 2I的零空间就是特征值2对应的特征空间，对A-2I做行变换得

$A-2I = \left(\begin{matrix}2&-1&6\\2&-1&6\\2&-1&6\end{matrix}\right)\sim\left(\begin{matrix}2&-1&6\\0&0&0\\0&0&0\end{matrix}\right)$

所以其通解为

$x = x_2\left(\begin{matrix}1/2\\1\\0\end{matrix}\right) + x_3\left(\begin{matrix}-3\\0\\1\end{matrix}\right)$， $x_2$和$x_3$ 为任意值

故特征值2对应的特征空间的基为

$\left\{\left(\begin{matrix}1/2\\1\\0\end{matrix}\right),\left(\begin{matrix}-3\\0\\1\end{matrix}\right)\right\}$

![](./pic/5.1.4.png)

 ![](./pic/5.1.5.png)

![](./pic/5.1.6.png)

### 5.2 特征方程

**例5.2.1**：求$A = \left(\begin{matrix}2&3\\3&-6\end{matrix}\right)$的特征值

解：求特征值就是要找出所有的$\lambda$ 使得下面的矩阵方程有非平凡解

$(A - \lambda I)x = 0$

根据逆矩阵定理，这个问题等价于找出所有的$\lambda$ ，使得$A - \lambda I$不可逆。通过引入行列式，我们只需要处理一个未知数

$det(A - \lambda I) = det\left(\begin{matrix}2- \lambda&3\\3&-6- \lambda\end{matrix}\right) = (2- \lambda)(-6- \lambda) - 9 = (\lambda - 3)(\lambda + 7) = 0$

故A的特征值为3和-7

#### 行列式

![](./pic/5.2.1.png)

![](./pic/5.2.2.png)

**例5.2.2**：计算 $A = \left(\begin{matrix}1&5&0\\2&4&-1\\0&-2&0\end{matrix}\right)$ 的行列式det A

解：对A施加行变换，使其变为阶梯阵：

$A \sim \left(\begin{matrix}1&5&0\\0&-2&0\\0&0&-1\end{matrix}\right)$

因此$det A = (-1)^1(1)(-2)(-1)=-2$

#### 特征方程

![](./pic/5.2.3.png)

**例5.2.3**：求 $A = \left(\begin{matrix}5&-2&6&-1\\0&3&-8&0\\0&0&5&4\\0&0&0&1\end{matrix}\right)$ 的特征方程

解：用行列式表达特征方程：

$det(A-\lambda I) =det\left(\begin{matrix}5-\lambda&-2&6&-1\\0&3-\lambda&-8&0\\0&0&5-\lambda&4\\0&0&0&1-\lambda\end{matrix}\right) = (5-\lambda)(3-\lambda)(5-\lambda)(1-\lambda） = (5-\lambda)^2(3-\lambda)(1-\lambda) = 0$

![](./pic/5.2.4.png)

**例5.2.4**：某$6\times6$ 矩阵的特征多项式为$\lambda^6-4\lambda^5-12\lambda^4$，求特征值及重数

解：把多项式分解因式：

$\lambda^6-4\lambda^5-12\lambda^4 = \lambda^4(\lambda-6)(\lambda+2)$

可得特征值0（重数为4），6（重数为1）和-2（重数为1）

#### 相似性

![](./pic/5.2.5.png)

![](./pic/5.2.6.png)

### 5.3 对角化

![](./pic/5.3.1.png)

**例5.3.1** ：证明定理5

证明：

先证明若n维方阵A可对角化则A有n个线性无关的特征向量

假设A可对角化，也就是$P = \left(\begin{matrix}v_1& \dots &v_n\end{matrix}\right)$可逆，$D = \left(\begin{matrix}\lambda_1&\dots&0\\\vdots&&\vdots\\0&\dots&\lambda_n\end{matrix}\right)$为对角矩阵，并且$A=PDP^{-1}$。用P右乘等式两边有AP = PD。

下面应该用这个等式得A有n个线性无关的特征向量的结论。由P可逆知，$v_1, \dots, v_n$ 必然线性无关且都不为零向量（否则矩阵有0列，导致行列式为0），再分析矩阵的列

$AP = \left(\begin{matrix}Av_1& \dots &Av_n\end{matrix}\right)$

$PD = \left(\begin{matrix}\lambda_1v_1& \dots &\lambda_nv_n\end{matrix}\right)$

由列相等得

$Av_1 = \lambda_1v_1, \dots, Av_n = \lambda_nv_n$

故$v_1, \dots, v_n$ 是A的特征向量

再证明若n维方阵有n个线性无关的特征向量，则A可对角化

若A有n个线性无关的特征向量，则将这些特征向量以列向量的方式构造矩阵P，并用相应的特征值来构造对角矩阵D，这时显然有AP = PD。因为P的列线性无关，所以P可逆，进而可以推出$A = PDP^{-1}$

#### 矩阵的对角化

**例5.3.3**：可能的话，将矩阵$A = \left(\begin{matrix}1&3&3\\-3&5&-3\\3&3&1\end{matrix}\right)$对角化。即求可逆矩阵P和对角矩阵D，使得$A = PDP^{-1}$

解：

1. 求A的特征值：$0 = det(A-\lambda I) = -(\lambda-1)(\lambda+2)^2$，得到特征值为1和-2
2. 求A的3个线性无关的特征向量：解$(A-I)x = 0$ 得特征值$\lambda_1=1$的基为$v_1=\left(\begin{matrix}1\\-1\\1\end{matrix}\right)$，解$(A+2I)x = 0$得特征值 $\lambda_2=-2$的基为$v_2=\left(\begin{matrix}-1\\1\\0\end{matrix}\right),v_3=\left(\begin{matrix}-1\\0\\1\end{matrix}\right)$，可以验证$\{v_1, v_2, v_3\}$ 是线性无关的
3. 构造矩阵P：$P = \left(\begin{matrix}v_1, v_2, v_3\end{matrix}\right) = \left(\begin{matrix}1&-1&-1\\-1&1&0\\1&0&1\end{matrix}\right)$
4. 用对应的特征值构造矩阵D：$D = \left(\begin{matrix}1&0&0\\0&-2&0\\0&0&-2\end{matrix}\right)$

![](./pic/5.3.2.png)

**例5.3.5**：确定$A = \left(\begin{matrix}5&-8&1\\0&0&7\\0&0&-2\end{matrix}\right)$能否对角化

解：三角矩阵（阶梯矩阵）的特征值就在其对角线上，显然矩阵A有三个相异的特征值5, 0, -2

#### 特征值不是都相异的矩阵

![](./pic/5.3.3.png)

（特征值数小于n但仍能找到n个线性无关的特征向量的情况，见例5.3.3）

### 5.4 特征向量与线性变换

#### 线性变换的矩阵

![](./pic/5.4.1.png)

![](./pic/5.4.2.png)

![](./pic/5.4.3.png)

**例5.4.1**：设$B = \{b_1, b_2\}$ 是V的基，$C = \{c_1, c_2, c_3\}$ 是W的基。T是$V \rightarrow W$ 的线性变换，$T(b_1) = 3c_1-2c_2+5c_3, T(b_2)=4c_1+7c_2-c_3$。求T相对于基B和C的矩阵M。

解：$M = \left(\begin{matrix}[T(b_1)]_C & [T(b_2)]_C\end{matrix}\right) = \left(\begin{matrix}3&4\\-2&7\\5&-1\end{matrix}\right)$

#### V到V的线性变换

![](./pic/5.4.4.png)

**例5.4.2**：$P_2\rightarrow P_2$ 的映射T：$T(a_0+a_1t+a_2t^2)=a_1+2a_2t$ 是线性变换（微分算子）

a. 当基$B = \{1, t, t^2\}$ 时，求T的B-矩阵

b. 对$P_2$ 中的每个p，验证$[T(p)]_B = [T]_B[P]_B$

解：

a. $[T]_B = \left(\begin{matrix}[T(b_1)]_B&[T(b_2)]_B&[T(b_3)_B]\end{matrix}\right) = \left(\begin{matrix}0&1&0\\0&0&2\\0&0&0\end{matrix}\right)$

b. 不妨设一般的多项式为$p(t)=a_0+a_1t+a_2t^2$，则$[T(p)]_B = [a_1+2a_2t] =  \left(\begin{matrix}a_1\\2a_2\\0\end{matrix}\right) = \left(\begin{matrix}0&1&0\\0&0&2\\0&0&0\end{matrix}\right)\left(\begin{matrix}a_0\\a_1\\a_2\end{matrix}\right) = [T]_B[p]_B$

![](./pic/5.4.5.png)

#### $R^n$ 上的线性变换

![](./pic/5.4.6.png)

**例5.4.3**：设$A = \left(\begin{matrix}7&2\\-4&1\end{matrix}\right)$ ，$R^2\rightarrow R^2$ 的变换$T:T(x)=Ax$。求$R^2$ 的一个基B，使得T的B-矩阵是对角矩阵

解：将矩阵A对角化$A=PDP^{-1}$，可得$P = \left(\begin{matrix}1&1\\-1&2\end{matrix}\right), D =\left(\begin{matrix}5&0\\0&3\end{matrix}\right)$，根据定理8，P的列向量就是所求的基

#### 矩阵表示的相似性

![](./pic/5.4.7.png)

![](./pic/5.4.8.png)

**例5.4.4**：设$A = \left(\begin{matrix}4&-9\\4&8\end{matrix}\right), b_1 = \left(\begin{matrix}3\\2\end{matrix}\right), b_2 = \left(\begin{matrix}2\\1\end{matrix}\right)$ ，A的特征多项式是$(\lambda + 2)^2$ ，但特征值-2的特征空间只是一维的，因此A是不可以对角化的。但是基$B = \{b_1, b_2\}$ 能够使得变换$x \mapsto Ax$ 的B-矩阵是三角矩阵，求A的B-矩阵。

解：直接利用定理8的推广求A的B-矩阵：

$P = \left(\begin{matrix}b_1&b_2\end{matrix}\right) = \left(\begin{matrix}3&2\\2&1\end{matrix}\right), P^{-1} = \frac{1}{-1}\left(\begin{matrix}1&-2\\-2&3\end{matrix}\right) = \left(\begin{matrix}-1&2\\2&-3\end{matrix}\right)$

$[T]_B = P^{-1}AP = \left(\begin{matrix}-2&1\\0&-2\end{matrix}\right)$

### 5.5 复特征值

### 5.6 离散动力系统

### 5.7 微分方程中的应用

### 5.8 特征值的迭代估计

## 6 正交性和最小二乘法

### 6.1 内积，长度和正交性

#### 内积

![](./pic/6.1.1.png)

![](./pic/6.1.2.png)

#### 向量的长度

![](./pic/6.1.3.png)

![](./pic/6.1.4.png)

#### $R^n$ 空间中的距离

![](./pic/6.1.5.png)

#### 正交向量

![](./pic/6.1.6.png)

![](./pic/6.1.7.png)

#### $R^2$ 空间和$R^3$ 空间的角度

![](./pic/6.1.8.png)

![](./pic/6.1.9.png)

### 6.2 正交集

![](./pic/6.2.1.png)

![](./pic/6.2.2.png)

![](./pic/6.2.3.png)

![](./pic/6.2.4.png)

**例6.2.2**：$u_1 = \left(\begin{matrix}3\\1\\1\end{matrix}\right), u_2 = \left(\begin{matrix}-1\\2\\1\end{matrix}\right), u_3 = \left(\begin{matrix}-1/2\\-2\\7/2\end{matrix}\right)$，$S = \{u_1, u_2, u_3\}$ 是$R^3$ 中的一个正交基，将向量$y = \left(\begin{matrix}6\\1\\-8\end{matrix}\right)$ 表示称S中向量的线性组合

解：$c_1 = \frac{y\cdot u_1}{u_1\cdot u_1} = 1, c_2 = \frac{y\cdot u_2}{u_2\cdot u_2} = -2, c_3 = \frac{y\cdot u_3}{u_3\cdot u_3} = -2$，根据定理5有$y = u_1-2u_2-2u_3$

#### 正交投影

![](./pic/6.2.5.png)

**例6.2.2**：假设$y = \left(\begin{matrix}7\\6\end{matrix}\right), u = \left(\begin{matrix}4\\2\end{matrix}\right)$，找出y在u上的正交投影，然后将y写成两个正交向量之和，一个在 $Span\{u\}$ 中，另一个与u正交。并且计算y到u所在直线的距离。

解：y在u上的正交投影是

$\hat{y} = \frac{y\cdot u}{u\cdot u} \cdot u =\left(\begin{matrix}8\\4\end{matrix}\right)$ 

y垂直于u的分量为

$z = y - \hat{y} =\left(\begin{matrix}-1\\2\end{matrix}\right)$

y到u所在直线的距离为

$||z|| = \sqrt{5}$ 

#### 单位正交集

![](./pic/6.2.6.png)

![](./pic/6.2.7.png)

![](./pic/6.2.8.png)

![](./pic/6.2.9.png)

**例6.2.6**：若$U = \left(\begin{matrix}1/\sqrt2&2/3\\1/\sqrt2&-2/3\\0&1/3\end{matrix}\right), x = \left(\begin{matrix}\sqrt2\\3\end{matrix}\right)$，注意到U具有单位正交列，且$U^TU=I$ ，验证$\|Ux\|=\|x\|$

解：$Ux = \left(\begin{matrix}3\\-1\\1\end{matrix}\right), \|Ux\| = \sqrt{(Ux)\cdot(Ux)}=\sqrt{11}, \|x\| = \sqrt{x\cdot x}=\sqrt{11}$，故$\|Ux\|=\|x\|$

### 6.3 正交投影

![](./pic/6.3.1.png)

![](./pic/6.3.2.png)

**例6.3.2**：假设$u_1 = \left(\begin{matrix}2\\5\\-1\end{matrix}\right), u_2 = \left(\begin{matrix}-2\\1\\1\end{matrix}\right), y = \left(\begin{matrix}1\\2\\3\end{matrix}\right)$ ，注意到$\{u_1, u_2\}$ 是$W=Span\{u_1, u_2\}$ 的正交基，将y写成属于W的向量与正交于W的向量之和。

解：属于W的向量为$\hat y = \frac{y\cdot u_1}{u_1 \cdot u_1}u_1 + \frac{y\cdot u_2}{u_2 \cdot u_2}u_2 = \frac{3}{10}\left(\begin{matrix}2\\5\\-1\end{matrix}\right) + \frac{1}{2}\left(\begin{matrix}-2\\1\\1\end{matrix}\right) = \left(\begin{matrix}-2/5\\2\\1/5\end{matrix}\right)$

正交于W的向量为：$y - \hat y = \left(\begin{matrix}7/5\\0\\14/5\end{matrix}\right)$

#### 正交投影的性质

![](./pic/6.3.3.png)

![](./pic/6.3.4.png)

**例6.3.3**：如果 $u_1 = \left(\begin{matrix}2\\5\\-1\end{matrix}\right), u_2 = \left(\begin{matrix}-2\\1\\1\end{matrix}\right), y = \left(\begin{matrix}1\\2\\3\end{matrix}\right)$ ，求W中离y最近的点

解：根据最佳逼近定理，最接近y的$\hat y = \frac{y\cdot u_1}{u_1 \cdot u_1}u_1 + \frac{y\cdot u_2}{u_2 \cdot u_2}u_2 = \left(\begin{matrix}-2/5\\2\\1/5\end{matrix}\right)$

![](./pic/6.3.5.png)

![](./pic/6.3.6.png)

### 6.4 格拉姆-施密特方法

![](./pic/6.4.1.png)

![](./pic/6.4.4.png)

#### 标准正交基

**例6.4.2**：假设 $x_1 = \left(\begin{matrix}1\\1\\1\\1\end{matrix}\right), x_2 = \left(\begin{matrix}0\\1\\1\\1\end{matrix}\right), x_3=\left(\begin{matrix}0\\0\\1\\1\end{matrix}\right)$ 。已知 $\{x_1, x_2, x_3\}$ 线性无关，且构成$R^4$ 中子空间W的一个基，试构造W的一个正交基。

解：

1. 取$v_1 = x_1$ 和$W_1 = Span\{x_1\}=Span\{v_1\}$ 
2. 取$v_2$ 为$x_2$ 在$W_1$ 的正交补中的分量，即$v_2=x_2-proj_{W_1}x_2 = x_2-\frac{x_2\cdot v_1}{v_1\cdot v_1}v_1 = \left(\begin{matrix}-3/4\\1/4\\1/4\\1/4\end{matrix}\right), W_2 = Span\{v_1, v_2\}$
3. （可选）重新度量$v_2$：$v_2' = 4v_2 = \left(\begin{matrix}-3\\1\\1\\1\end{matrix}\right), W_2 = Span\{v_1, v_2'\}$
4. 取$v_3$ 为$x_3$ 在$W_2$ 的正交补中的分量，即$v_3=x_3-proj_{W_2}x_3 = x_3-\frac{x_3\cdot v_1}{v_1\cdot v_1}v_1 - \frac{x_3\cdot v_2}{v_2\cdot v_2}v_2 = \left(\begin{matrix}0\\-2/3\\1/3\\1/3\end{matrix}\right)$
5. （可选）重新度量$v_3$ ：$v_3'= 3v_3 =  \left(\begin{matrix}0\\-2\\1\\1\end{matrix}\right)$

$\{v_1, v_2', v_3'\}$ 即W的一个正交基

#### 矩阵的QR分解

![](./pic/6.4.2.png)

![](./pic/6.4.3.png)

**例6.4.4**：证明QR分解定理，并求$A = \left(\begin{matrix}1&0&0\\1&1&0\\1&1&1\\1&1&1\end{matrix}\right)$的一个QR分解。

证明：若A列线性无关，那么A的列向量形成Col A的一个基$\{x_1, \dots, x_n\}$，构造W = Col A的标准正交基$\{u_1, \dots, u_n\}$ ，并取$Q = \left(\begin{matrix}u_1&\cdots&u_n\end{matrix}\right)$。

考虑A的第k个列向量，我们有$x_k$ 属于$Span\{x_1, \cdots, x_k\}$，即属于$Span\{u_1, \cdots, u_k\}$，进而$x_k$ 能被表示为 $\{u_1, \cdots, u_k\}$ 的线性组合（不妨令 $r_{kk} \ge 0$ ，若$r_{kk} < 0$ ，则对$r_{kk}$和$u_k$ 都乘-1，Q的列仍能构成标准正交基）：

$x_k=r_{1k}u_1+\dots+r_{kk}u_k = Q\left(\begin{matrix}r_{1k}&\dots&r_{kk}&0&\dots&0\end{matrix}\right)^T$

设$r_k = \left(\begin{matrix}r_{1k}&\dots&r_{kk}&0&\dots&0\end{matrix}\right)^T$，$R = \left(\begin{matrix}r_1&\cdots&r_n\end{matrix}\right)$，于是对全体$\{x_1, \dots, x_n\}$ 构成的A就有

$A = \left(\begin{matrix}x_1&\cdots&x_n\end{matrix}\right) = Q\left(\begin{matrix}r_{11}\\0\\\vdots\\0\end{matrix}\right) + \dots +Q\left(\begin{matrix}r_{1n}\\r_{2n}\\\vdots\\r_{nn}\end{matrix}\right) = QR$

显然R是上三角矩阵，且根据假设，其主对角线上的元素都是非负数。证明R可逆的方法（Rx = 0等式两侧左乘Q后解的结构不会发生改变吗？）：

![](./pic/6.4.5.png)

既然R可逆，则其主对角线上的元素都是正数（考虑上三角矩阵的行列式）。

解：通过格拉姆-施密特方法可得矩阵A的正交基为

$v_1 = \left(\begin{matrix}1\\1\\1\\1\end{matrix}\right), v_2 = \left(\begin{matrix}-3\\1\\1\\1\end{matrix}\right), v_3=\left(\begin{matrix}0\\-2\\1\\1\end{matrix}\right)$

将这三个向量单位化得到$u_1, u_2, u_3$ ，且用这些向量组成Q的列

$Q = \left(\begin{matrix}1/2&-3/\sqrt 12&0\\1/2&1/\sqrt 12&-2/\sqrt 6\\1/2&1/\sqrt 12&1/\sqrt 6\\1/2&1/\sqrt 12&1/\sqrt 6\end{matrix}\right)$

根据定理12，$A=QR$，Q又是单位矩阵，那么$Q^TQ=I$，进而有

$R=Q^TA = \left(\begin{matrix}2&3/2&1\\0&3/\sqrt 12&2/\sqrt{12}\\0&0&2/\sqrt 6\end{matrix}\right)$

### 6.5 最小二乘问题

### 6.6 线形模型中的应用

### 6.7 内积空间

### 6.8 内积空间的应用

## 7 对称矩阵和二次型

### 7.1 对称矩阵的对角化

![](./pic/7.1.1.png)

![](./pic/7.1.2.png)

![](./pic/7.1.3.png)

**例7.1.3**：$A = \left(\begin{matrix}3&-2&4\\-2&6&2\\4&2&3\end{matrix}\right)$ 的特征方程为$0=-(\lambda-7)^2(\lambda+2)$ ，将其正交对角化。

解：根据特征方程可得特征值：$\lambda_1=7, \lambda_2=-2$

解方程$(A - 7I)x=0$ 得$\lambda_1$ 对应的特征空间的基：$v_1=\left(\begin{matrix}1\\0\\1\end{matrix}\right), v_2=\left(\begin{matrix}-1/2\\1\\0\end{matrix}\right)$，进而得到特征空间的单位正交基：$u_1=\left(\begin{matrix}1/\sqrt 2\\0\\1/\sqrt 2\end{matrix}\right), u_2=\left(\begin{matrix}-1/\sqrt{18}\\4/\sqrt{18}\\1/\sqrt{18}\end{matrix}\right)$

解方程$(A + 2I)x=0$ 得$\lambda_2$ 对应的特征空间的基：$ v_3=\left(\begin{matrix}-1/4\\1\\1/4\end{matrix}\right)$，进而得到特征空间的单位正交基：$u_3=\left(\begin{matrix}-2/3\\-1/3\\2/3\end{matrix}\right)$

根据定理1，$u_3$ 与$u_1, u_2$ 正交，即$\{u_1, u_2, u_3\}$ 为单位正交基。令

$P = \left(\begin{matrix}u_1&u_2&u_3\end{matrix}\right) =\left(\begin{matrix}1/\sqrt 2&-1/\sqrt{18}&-2/3\\0&4/\sqrt{18}&-1/3\\1/\sqrt 2&1/\sqrt{18}&2/3\end{matrix}\right), D=\left(\begin{matrix}7&0&0\\0&7&0\\0&0&-2\end{matrix}\right)$

可得正交对角化结果：$A=PDP^{-1}$

#### 谱分解

![](./pic/7.1.4.png)

![](./pic/7.1.5.png)

**例7.1.4**：构造矩阵A的一个谱分解，已知A有以下正交对角化分解

$A = \left(\begin{matrix}7&2\\2&4\end{matrix}\right) =\left(\begin{matrix}2/\sqrt{5}&-1/\sqrt{5}\\1/\sqrt{5} &2/\sqrt{5}\end{matrix}\right)\left(\begin{matrix}8&0\\0&3\end{matrix}\right)\left(\begin{matrix}2/\sqrt{5}&1/\sqrt{5}\\-1/\sqrt{5} &2/\sqrt{5}\end{matrix}\right)$

解：将P的列记为$u_1, u_2$，则有谱分解：

$A = 8u_1u_1^T+3u_2u_2^T = \left(\begin{matrix}32/5&16/5\\16/5&8/5\end{matrix}\right) + \left(\begin{matrix}3/5&-6/5\\-65&12/5\end{matrix}\right)$

### 7.2 二次型

![](./pic/7.2.1.png)

**例7.2.2**：对属于$R^3$ 的x，取$Q(x)=5x_1^2+3x_2^2+2x_3^2-x_1x_2+8x_2x_3$，写出其$x^TAx$ 形式的二次型。

解：显然，$x_1^2, x_2^2, x_3^2$ 的系数在A的主对角线上，$x_1x_2$ 的系数要平分到$A_{12}, A_{21}$ 中去，$x_2x_3$ 的系数要平分到$A_{23}, A_{32}$ 中去。因此

$Q(x) = x^TAx = \left(\begin{matrix}x_1&x_2&x_3\end{matrix}\right) \left(\begin{matrix}5&1/2&0\\-1/2&3&4\\0&4&2\end{matrix}\right) \left(\begin{matrix}x_1\\x_2\\x_3\end{matrix}\right)$

#### 二次型的变量代换

![](./pic/7.2.2.png)

**例7.2.4**：对属于$R^3$ 的x，取$Q(x)=x_1^2-8x_1x_2-5x_2^2$，求一个变量代换将其变为一个没有交叉项的二次型。

解：先将二次型矩阵求出来：

$A = \left(\begin{matrix}1&-4\\-4&5\end{matrix}\right)$

再将矩阵A正交对角化：

$P = \left(\begin{matrix}2/\sqrt{5}&1/\sqrt{5}\\-1\sqrt{5}&2\sqrt{5}\end{matrix}\right), D = \left(\begin{matrix}3&0\\0&-7\end{matrix}\right)$

一个适当的变换是$y=P^{-1}x$使得$x^TAx=y^TDy$

当x取(2, -2)时，两个二次型都会得到16

![](./pic/7.2.3.png)

![](./pic/7.2.4.png)

#### 主轴的几何意义

![](./pic/7.2.5.png)

**例7.2.5**：有椭圆方程$5x_1^2-4x_1x_2+5x_2^2=48$ ，求该椭圆的主轴。

解：二次型对应的矩阵为$A = \left(\begin{matrix}5&-2\\-2&5\end{matrix}\right)$ ，可以得到其单位特征向量$u_1 = \left(\begin{matrix}1/\sqrt{2}\\1/\sqrt{2}\end{matrix}\right), u_2=\left(\begin{matrix}-1/\sqrt{2}\\1/\sqrt{2}\end{matrix}\right)$，这便是椭圆的主轴

#### 二次型的分类

![](./pic/7.2.6.png)

![](./pic/7.2.7.png)

### 7.3 条件优化

![](./pic/7.3.1.png)

![](./pic/7.3.2.png)

![](./pic/7.3.3.png)

**例7.3.3**：令$A = \left(\begin{matrix}3&2&1\\2&3&1\\1&1&4\end{matrix}\right)$，求二次型$x^TAx$ 在限制条件$x^Tx=1$ 下的最大值，以及一个可以取到该最大值的单位向量

解：根据定理6，最大值为A的最大特征值，求出A的特征多项式：

$0=-(\lambda-6)(\lambda-3)(\lambda-1)$

因此最大的特征值为$\lambda_1=6$，解$(A-6I)x=0$ 可得单位特征向量$u_1=\left(\begin{matrix}1/\sqrt{3}\\1/\sqrt{3}\\1/\sqrt{3}\end{matrix}\right)$ 

故二次型在$u_1$ 处可以取得最大值$\lambda_1$

![](./pic/7.3.4.png)

**例7.3.5**：令$A = \left(\begin{matrix}3&2&1\\2&3&1\\1&1&4\end{matrix}\right)$，已知$u_1$ 为A的最大特征值的特征向量，求二次型$x^TAx$ 在限制条件$x^Tx=1, x^Tu_1=0$ 下的最大值，以及一个可以取到该最大值

解：求出A的特征多项式：

$0=-(\lambda-6)(\lambda-3)(\lambda-1)$

根据定理7，所求最大值为第二大的特征值3

![](./pic/7.3.5.png)

**例7.3.6**：县政府计划在下一年度修建x百公里的公路和桥梁，并且修正y百英亩的公园和娱乐产所。其中x, y必须满足的限制条件为$4x^2+9y^2\le36$ 。令效用函数q(x, y) = xy（xy=c曲线又被称为无差别曲线，每个c代表一种价值观），求一个公共工作计划(x, y) 使得效用函数最大。

解：先想办法将不等式限制条件话为等式限制条件。显然，对于效用函数而言，在限制条件的边界上取值能使资源利用达到最大可能。也就是：

$4x^2+9y^2=36$

![](./pic/7.3.6.png)

虽然现在得到了等式限制，但(x, y)没有单位向量的意思，于是考虑用变量代换。重写限制条件如下：

$(\frac{x}{3})^2+(\frac{y}{2})^2=1$

再做换元$x=3x_1, y=2x_2$，于是问题就被转化为在$x^Tx=1$ 的条件下求 $Q(x)=6x_1x_2$ 的最大值，若将二次型写成$Q(x)=x^TAx$ 的形式，不难得出：

$A = \left(\begin{matrix}0&3\\3&0\end{matrix}\right)$

同样不能得出A的最大特征值为3，对应的特征向量为$u_1 = \left(\begin{matrix}1/\sqrt{2}\\1/\sqrt{2}\end{matrix}\right)$，所以效用函数的最大值3可以在$x_1=1/\sqrt{2}, x_2=1/\sqrt{2}$ 处得到，也就是在$x=3/\sqrt{2}, y=2/\sqrt{2}$ 处得到。

### 7.4 奇异值分解

![](./pic/7.4.1.png)

**例7.4.1**：若$A = \left(\begin{matrix}4&11&14\\8&7&-2\end{matrix}\right)$ ，那么线性变换$x\mapsto Ax$将$R^3$ 中的单位球$\{x:\|x\|=1\}$ 映射为$R^2$ 的椭圆，找出使得$\|Ax\|$最大的一个单位向量x，并且计算这个最大长度。

![](./pic/7.4.2.png)

解：优化$\|Ax\|$同优化$\|Ax\|^2$ 是一样的，所以我们有话更容易优化的后者，先对其做变换：

$\|Ax\|^2 = (Ax)^TAx = x^TA^TAx$

显然，$A^TA$ 是个对称矩阵，因此问题转化为，在$x^Tx=1$ 的限制下，最大化二次型$x^TA^TAx$，首先计算

$A^TA = \left(\begin{matrix}80&100&40\\100&170&140\\40&140&200\end{matrix}\right)$

这个矩阵最大的特征值为$\lambda_1=360$，对应的单位特征向量为：$v_1 = \left(\begin{matrix}1/3&2/3&2/3\end{matrix}\right)^T$，因此使得$\|Ax\|^2$ 最大的单位向量为$v_1$，最大值为360。

![](./pic/7.4.3.png)

#### $m\times n$ 矩阵的奇异值

![](./pic/7.4.4.png)

**例7.4.2**：若$A = \left(\begin{matrix}4&11&14\\8&7&-2\end{matrix}\right)$ ，求A的奇异值

解：由于$A^TA$ 的特征值为$\lambda_1=360, \lambda_2=90, \lambda_3=0$，所以A的奇异值为$\sigma_1=6\sqrt{10}, \sigma_2=3\sqrt{10}, \sigma_3=0$。

![](./pic/7.4.5.png)

![](./pic/7.4.6.png)

![](./pic/7.4.7.png)

**例7.4.3**：证明定理9

证明：要证明$\{Av_1, \dots, Av_n\}$ 是正交基，就要证明当$i\ne j$ 时$(Av_i)^T(Av_j)=0$。将其变形：

$(Av_i)^T(Av_j)=v_i^TA^TAv_j$

因为$v_j$对应$A^TA$的一个特征向量，所以

$(Av_i)^T(Av_j)=v_i^TA^TAv_j=v_i^T\lambda_jv_j$

因为$\{v_1, \dots, v_n\}$是$A^TA$ 的单位正交基，所以

$(Av_i)^T(Av_j)=v_i^T\lambda_jv_j = 0$

$\{Av_1, \dots, Av_n\}$ 是正交基得证。



#### 奇异值分解

![](./pic/7.4.8.png)

![](./pic/7.4.9.png)