# Markdown图片
Markdown图片语法如下：
`![替代文字](图片路径)`
`![替代文字](图片路径 "图片标题")`

注：图片路径可使用相对路径或绝对路径。

支持直接引用网络图片，eg：
![RUNOOB 图标](https://static.jyshare.com/images/runoob-logo.png "RUNOOB")

## 图片尺寸设置
Markdown可通`<img>`标签的方式设置图片的高度和宽度，eg：

比例缩放：
<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" width="50%">

<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" width="100">

强制拉伸：
<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" width="100" height="30">

## 使用CDN服务
- 操作步骤：
  1. 新建 GitHub 仓库（公开），新建 images 文件夹，上传图片
  2. 复制图片 raw 链接，替换为 JSDelivr 加速地址
- 格式模板：
`![示例图片][https://cdn.jsdelivr.net/gh/用户名/仓库名/文件路径]`
eg:`![示例图片](https://cdn.jsdelivr.net/gh/user/repo/image.png)`

## 图片替代文字作用
Alt文本（替代文字）在图片无法显示时提供替代信息，eg：
![用户登录界面，包含用户名和密码输入框](./screenshots/login-page.png)

# 图片尺寸控制
Markdown图像尺寸控制通过HTML标签的方式实现。

## 使用HTML img标签

<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="描述文字" width="300" height="200">

<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="描述文字" width="50%">

<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="描述文字" style="width: 300px; height: auto;">

## 响应式图片

<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="描述文字" style="max-width: 100%; height: auto;">

## 图片对齐
<!-- 居中对齐 -->
HTML + CSS：
<div align="center">
  <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="居中图片" width="50%">
</div>

通过 HTML 对齐属性：
<p align="center">
  <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="居中图片" width="400">
</p>

<!-- 左对齐（默认） -->
<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="左对齐图片" width="50%" style="float: left; margin-right: 20px;">

<!-- 右对齐 -->
<img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4" alt="右对齐图片" width="50%" style="float: right; margin-left: 20px;">

<!-- 清除浮动效果，避免后续文字与图片交叉显示 -->
<div style="clear: both;"></div>

# 链接和图片的高级用法
## 图片链接组合
图片与链接组合基本语法如下：
`[![图片alt文本](图片URL)](链接URL)`
实例：
[![GitHub项目截图](./images/project-screenshot.png)](https://github.com/username/project)
[![访问官网](https://example.com/logo.png)](https://example.com "点击访问官网")