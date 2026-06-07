# Markdown数学公式
## LaTeX数学公式基础
### 基本语法结构

在 Markdown 中，数学公式通过 LaTeX 语法来表示，基本语法结构如下：

命令：以反斜杠`\`头，如 `\alpha`、`\sum`
参数：用花括号 `{}` 包围，如 `\frac{a}{b}`
下标：使用 `_`，如 `x_1`
上标：使用 `^`，如 `x^2`
分组：用花括号将多个字符组合，如 `x_{i+1}`

### 常用LaTeX命令
`\alpha`, `\beta`, `\gamma`  希腊字母
`\sum`, `\prod`, `\int`       求和、乘积、积分
`\frac{分子}{分母}`       分数
`\sqrt{表达式}`           平方根
`\sqrt[n]{表达式}`        n次根

## 行内公式与块级公式 
### 行内公式

行内公式通过单个`$`包围，eg：
文本中的变量 $x = 5$ 和函数 $f(x) = x^2 + 2x + 1$。

### 块级公式
块级公式使用`$$`包围,eg:
$$E = mc^2$$

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

### 多行公式
使用`align`环境创建多行对齐公式，eg:
$$
    \begin{align}
    f(x) &= ax^2 + bx + c \\
    f'(x)  &= 2ax + b \\
    f''(x)  &= 2a
    \end{align}
$$

注：
- `=`前加`&`使得等号对齐

# 常用数学符号
## 基本运算符号

加减乘除：`+, -, \times, \div`
分数：`\frac{a}{b}` → $\frac{a}{b}$
根号：`\sqrt{x}, \sqrt[n]{x}` → $\sqrt{x}$, $\sqrt[n]{x}$
指数：`x^2, e^{i\pi}` → $x^2$, $e^{i\pi}$

## 比较符号

等于：`=, \neq, \equiv` → $=$, $\neq$, $\equiv$
大小：`<, >, \leq, \geq` → $<$, $>$, $\leq$, $\geq$
约等于：`\approx, \sim` → $\approx$, $\sim$

## 希腊字母
|大写|小写|LaTeX|大写|小写|LaTeX|
|----|---|-----|----|---|-----|
| α  | Α |`\alpha`| ν  | Ν |`\nu`|
| β  | Β |`\beta`| ο  | Ο |`o`|
| γ  | Γ |`\gamma`| π  | Π |`\pi`|
| δ  | Δ |`\delta`| ρ  | Ρ |`\rho`|
| ε  | Ε |`\epsilon`| σ  | Σ |`\sigma`|
| θ  | Θ |`\theta`| τ  | Τ |`\tau`|
| λ  | Λ |`\lambda`| φ  | Φ |`\phi`|
| μ  | Μ |`\mu`| ω  | Ω |`\omega`|

## 特殊符号与函数
三角函数：`\sin, \cos, \tan`
对数：`\log, \ln`
极限：`\lim_{x \to 0}`
求和：`\sum_{i=1}^{n}`
积分：`\int_{a}^{b}`
无穷：`\infty`

## 矩阵表示
矩阵使用`matrix`环境表示，eg：

$$
    \begin{pmatrix}
    a & b \\
    c & d
    \end{pmatrix}
$$

注：
- `matrix`：无括号 $\begin{matrix} a & b \\ c & d \end{matrix}$ <br>
`pmatrix`：圆括号 $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ <br>
`bmatrix`：方括号 $\begin{bmatrix} a & b \\ c & d \end{bmatrix}$ <br>
`vmatrix`：行列式 $\begin{vmatrix} a & b \\ c & d \end{vmatrix}$ 