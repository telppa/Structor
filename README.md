# Structor  
  
轻松获取结构体大小、偏移、常量值的工具。  
  
  
  
## 简介  
  
![Structor](https://raw.githubusercontent.com/telppa/Structor/main/Img/1.png)  
![Verifier](https://raw.githubusercontent.com/telppa/Structor/main/Img/2.png)  
  
本工具提取自 [Adventure IDE – 3.0.4](https://sourceforge.net/projects/autogui/) ，作者 alguimistf 。  
  
为实现工具便携性与使用傻瓜化，我修改了部分代码，并集成了最新的 MSVC2022 编译器及 WIN10 SDK 。  
  
简单说就是，现在你只需要下载解压就可以使用了。  
  
  
  
## 功能1：创建结构体并从中读取内容。  
  
当我们想在 ahk 中使用一个结构体，例如 URL_COMPONENTS 时。  
  
1. 首先在 MSDN 也就是微软官网找到 URL_COMPONENTS 的页面。  
  
2. 复制结构体到工具中。  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/3.png)  
  
3. 根据页面最下方的提示在工具中添加对应的头文件（页面无提示则可以不添加）。  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/4.png)  
  
4. 点击 Compile 按钮，等待结果出现再点击 Copy 按钮。  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/5.png)  
  
此时剪贴板中就得到了可以让你像变量一样使用该结构体的代码了。  
  
  
  
## 功能2：获取数据类型的大小。  
  
例如我们想知道， DWORD 类型在32位下的大小时。  
  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/6.png)  
  
需要注意， DWORD 之类的内容是大小写敏感的。  
  
  
  
## 功能3：获取成员的偏移量。  
  
例如我们想知道，结构体 URL_COMPONENTS 的成员 nPort 在64位下的偏移量时。  
  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/7.png)  
  
需要注意，本例中的结构体 URL_COMPONENTS 需要头文件 winhttp.h ，所以在 Includes 中要自己加上。  
  
同样的， URL_COMPONENTS.nPort 之类的内容是大小写敏感的。  
  
  
  
## 功能4：获取常量值。  
  
例如我们想知道，常量 LVM_GETHEADER 在32位下的具体值时。  
  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/8.png)  
  
需要注意，本例中的 LVM_GETHEADER 需要头文件 commctrl.h ，所以在 Includes 中要自己加上。  
  
同样的， LVM_GETHEADER 之类的内容是大小写敏感的。  
  
  
  
## 功能5：批量模式。  
  
例如我们想知道，DWORD WORD HANDLE 3种类型的大小时。  
  
新建一个文本文档，每行写一种类型，像这样。  
  
```
WORD
DWORD
HANDLE
```
  
![](https://raw.githubusercontent.com/telppa/Structor/main/Img/9.png)  
  
同理，也可以批量获取成员偏移量和常量值。  
  
  
  
## 更新日志  
#### 2022.05.12
* 为 StrGet 与 StrPut 提供 Plan B 。
* 版本号 1.2.2 。
#### 2022.04.18
* 修复了原版数个 BUG 。
* 打包了编译器和 SDK 。
* 增强了类型识别功能。
* 实现了工具便携性。
* 版本号 1.2.1 。
  
  
  
## 下载地址  
  
[Github Releases](https://github.com/telppa/Structor/releases)
