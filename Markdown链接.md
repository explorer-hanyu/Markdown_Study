# Markdown链接
链接创建语法如下：

1. `[链接名称](链接地址)`
2. `[链接名称](链接地址 "可选的标题")`
3. `<链接地址>`

示例如下：
1. Markdown学习网址[菜鸟教程-Markdown](https://www.runoob.com/markdown/md-link.html);
2. Markdown学习网址[菜鸟教程-Markdown](https://www.runoob.com/markdown/md-link.html "Markdown学习链接")；
3. <https://www.runoob.com/markdown/md-link.html>

注：通过第二种方法创建的链接，光标悬停时显示标题，标题文字放在双引号、单引号或括号中都可以。

## 参考链接
参考链接将链接定义与使用分离，基本语法如下：
`[链接文字][参考标签]`

`[参考标签]: URL "可选标题"`

示例如下：
我是在[菜鸟][runoob]学习的Markdown编辑方。

注：参考链接与脚注易混淆，脚注示例[^脚注标签]，脚注内容会始终显示到文档最末尾。

### 简化写法
当参考链接与链接文字相同时，可省略后面方括号里面的内容，eg：

我后续会使用[GitHub][]来管理代码，需要学习它的使用方法。

## 链接自动识别
Markdown解析器通常支持自动识别URL和邮箱地址，eg：

直接输入网址：https://www.example.com
用尖括号包围：<hanyu@163.com>

## 锚点链接的使用
锚点链接用于在同一文档内跳转，eg：
Markdown链接的创建方法参考[Markdown链接](#markdown链接)。

### 锚点规则
- 标题会自动生成锚点
- 锚点名称通常是标题的小写形式
- 空格替换为连字符-
- 移除特殊字符

### 手动创建锚点
手动创建锚点，通过`<a id="锚点名称"> </a>`实现方法如下：

<a id="custom-anchor"></a>

[跳转到自定义位置](#custom-anchor)



<!-- 链接定义区域 -->
[runoob]:http://www.runoob.com/ "菜鸟编程"
[GitHub]:https://github.com "代码管理工具"

[^脚注标签]:这是脚注的用法。