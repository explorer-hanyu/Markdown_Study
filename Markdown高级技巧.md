# Markdown高级技巧
## 支持HTML元素
目前支持的HTML元素有`<kbd> <b> <i> <em> <sup> <sub> <br>`等。

eg:
使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑

## 转义
某些也是符号表示特定的意义，如需显示需要通过`\`进行转义：

```
\   反斜线
`   反引号
*   星号
_   下划线
{}  花括号
[]  方括号
()  小括号
#   井字号
+   加号
-   减号
.   英文句点
!   感叹号
```

## 公式
公式分隔符如下：
`$...$`或者`\(...\)`中的数学表达式将会在行内显示。eg:
$f(x)=sin(x)+12$
\( f(x)=sin(x)+12 \)


`$$...$$`或者 `\[...\]`或者```math 中的数学表达式将会在块内显示。eg:
$$
\begin{Bmatrix}
   a & b \\
   c & d
\end{Bmatrix}
$$

\[
\begin{CD}
   A @>a>> B \\
@VbVV @AAcA \\
   C @= D
\end{CD}
\]

 ```math 
\begin{Bmatrix}
   a & b \\
   c & d
\end{Bmatrix}
 ``` 