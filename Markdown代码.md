# 行内代码
可通过反引号“`”将段落内的函数或片段代码包起来表示，eg：

使用`print()`函数输出信息

# 特殊字符转义
当需要在行内代码中显示反引号或其它特殊字符时，需要进行转义处理，通过双反引号“``”包围，eg：

``使用`反引号`包围代码``

需要显示双反引号时通过多个反引号包围，eg：
```包含``双反引号``的代码```  

# 代码区块
代码区块使用4个空格或一个制表符(Tab)表示，eg:
正常文本段落

    这是缩进式的代码块
    每行前面四个空格
    保持代码的原始格式

注意：所有代码行保持一致的缩进，在列表中使用时需要缩进8个空格。

# 三反引号代码块
通过首行和尾行添加三个反引号来标注代码块，eg：
```
多行代码内容
可以包含空行

 可以保持缩进
```

可以通过三反引号指定语言，启动高亮功能，eg：
```javascript
$(document).ready(function () {
    alert('RUNOOB');
});
```
注：可指定包含javascript/js，python/py，html，sql，json，xml，yaml/yml，bash/shell，cpp/c++在内的多种语言格式。

# 代码块的高级特性
## 行号显示
某些Markdown渲染器支持显示行号，通过{.line-numbers}语法实现，eg：
```javascript {.line-numbers}
function fibonacci(n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

console.log(fibonacci(10));
```

## 代码差异对比
通过diff语法用于显示代码的添加、删除或修改，展示版本变更，eg:

```diff
function calculateTotal(items) {
-   let total = 0;
+   let total = 0.0;
    
    for (let item of items) {
-       total += item.price;
+       total += parseFloat(item.price);
    }
    
+   // 保留两位小数
+   total = Math.round(total * 100) / 100;
    return total;
}
```

注：在变更行首位通过+或-标记变更状态,通常不能和语言标记通用。