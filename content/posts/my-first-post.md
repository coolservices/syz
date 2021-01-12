---
title: "如何创建hugo网站"
date: 2021-01-11T21:06:17+08:00
draft: true 
---

## 下载安装hugo软件
### 1.安装
#### 在https://gohugo.io/getting-started/installing 地址下根据相应的系统找到对应的文件进行下载。
#### 本篇指导以macos系统为例进行安装说明。
#### 利用Homebrew和的MacPorts软件包管理器可以分别从brew.sh或macports.org安装。本文以Homebrew为例。
#### 输入代码 brew install hugo
![安装界面](1.jpg)
### 2.建立新网站
#### 输入代码 hugo new site quickstart
![建立界面](2.jpg)

### 3.选择主题
#### 请参阅themes.gohugo.io以获取主题列表。本指导使用了Ananke主题。
#### 首先，从GitHub下载主题并将其添加到站点的themes目录中：
#### 代码如下：
#### cd quickstart
#### git init
#### git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke

##### 对于非git用户的注意事项：
##### 如果您尚未安装git，则可以从以下网址下载该主题的最新版本的存档：https : //github.com/budparr/gohugo-theme-ananke/archive/master.zip
##### 解压缩该.zip文件以获得“ gohugo-theme-ananke-master”目录。
##### 将该目录重命名为“ ananke”，并将其移至“ themes /”目录。

#### 然后，将主题添加到站点配置中：
#### 输入代码 echo 'theme = "ananke"' >> config.toml
![添加主题](3.jpg)

### 4.添加内容
#### 使用命令添加内容（例如添加标题和日期）：hugo new posts/my-first-post.md
#### 该命令用于添加第一个网页链接，之后可以在创建的文件夹中找到该md格式的文件进行进一步添加内容。

![内容添加](4.jpg)

### 5.启动Hugo服务器
#### 输入代码 hugo server -D 启动服务器

![启动服务器](4.jpg)
#### 导航至http：// localhost：1313 /的新站点。

#### 可以随意编辑或添加新内容，只需在浏览器中刷新即可快速查看更改（您可能需要在Web浏览器中强制刷新）。

### 6.自定义配置
#### 在网站发布之前，需要对网站进行美化修改。可以在根目录中找到config.toml文件进行修改
#### baseURL = "https://example.org/"
#### languageCode = "zh"
#### title = "创建一个hugo网站"
#### theme = "ananke"

### 7.建立静态页面
#### 输入代码 hugo -D
#### 完成