### SublimeText3常用插件及快捷键总结
SublimeText可谓是前端工程师的代码编辑神器，自从用上它以后一直爱不释手，特别是它强大的插件功能，简直要逆天了。网上也有很多关于SublimeText3的各种插件介绍，其插件功能之多，让人眼花缭乱。今天我主要是来整理一下自己常用的前端插件，并打包上传至我的[github](https://github.com/Jesse121/Sublime_Plugins),欢迎大家下载交流，若有更好用的插件，还希望推荐。
好了废话不多说现在就开始惊奇的sublime之旅
#### NO.1 下载安装
点击进入[sublime官网](http://www.sublimetext.com/3),根据自己的电脑系统下载相应的版本  
将下载的压缩包解压后直接放进你要安装的文件夹，双击sublime_text.exe即可运行  
#### 获取license
虽然没有许可证也可以使用，但软件开发及维护不易，建议有条件的同学还是购买license，获得永久使用权
#### NO.2 插件安装
这是今天的重点，在安装插件之前我们需要安装package control组件

1. 在线安装  
    按<kbd>ctrl</kbd>+<kbd>`</kbd>调出console面板,粘贴以下代码（或者[SUBLIME TEXT 3](https://packagecontrol.io/installation#st3)面板中的代码）到命令行并回车
<pre>
import urllib.request,os,hashlib;h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; 
pf = 'Package Control.sublime-package'; 
ipp = sublime.installed_packages_path(); 
urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); 
by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); 
dh = hashlib.sha256(by).hexdigest(); 
print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
</pre>
重启Sublime Text 3。如果在Perferences->package settings中看到package control这一项，则安装成功。

2. 手动安装  
    如果你的电脑没有外网权限(小编就是这样)，那只能手动安装了  
    点击Preferences 选择Browse Packages… ，打开其上一级文件夹Data并进入Installed Packages文件夹  
    将下载的[Package Control.sublime-package文件](https://packagecontrol.io/Package Control.sublime-package)复制进去，再重启Sublime Text

##### 插件安装方法介绍

1. 在线安装   
    按下<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>调出命令面板，输入install选择Install Package 选项并回车，  
    再输入你要安装的插件名称(例如sublime tmpl)，然后在列表中选中要安装的插件。  
    安装成功后一般在Perferences->package settings中可看到  
    有些插件有可能在列表中搜索不到，你可以选择手动安装  
2. 手动安装  
    进入[sublimetext安装包管理器官网](https://packagecontrol.io/)在搜索框里输入你所需要的插件名称  
    进入插件的github页面（点击Details下面的github.com）,点击右侧的clone or download -> Download ZIP,将下载的压缩包解压后放在Preferences->Browse Packages（即packages文件夹）里面，并重命名（去掉文件名中的-master）  
    重启Sublimetext3即可安装成功  
**注意：**手动安装的插件不会自动添加到Package setting列表

###### There are no packages available for installation
现实中没有什么事情总是一帆风顺的，特别是计算机程序，时不时就给你来点意外情况。  
例如在在线安装步骤中选择Install Package后Sublime弹出窗口提示  
`There are no packages available for installation`  
出现的原因：据说是IPv6的原因，如果我们的Intent服务提供者（ISP）不支持IPv6就会引发上述错误，  
解决方法一：
打开C:\Windows\system32\drivers\etc\hosts文件，增加如下对应关系：50.116.34.243  sublime.wbond.net  
终极解决方法：用手动安装插件

#### 常用插件介绍
##### Alignment
使用说明：Alignment是一个代码格式化插件，它可以使多行代码中的等号对齐，也可以调整多行代码为一个缩进级别。  
快捷键：<kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>alt</kbd>+<kbd>a</kbd>

##### AutoFileName
使用说明：文件名自动补全，根据路径自动提示该路径下的文件

##### BracketHighlighter
使用说明：BracketHighlighter插件是用来匹配相对的符号，然后高亮显示，比如{ }、[ ]、" "等符号的对应高亮显

##### ConvertToUTF8
使用说明：自动转为UTF-8编码类型

##### DeleteBlankLines
使用说明：选中需要批量删除空行的部分，Ctrl + Alt + Backspace，选中部分的所有空行就都被删除了  
快捷键：<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>backspace</kbd>

#####  DocBlockr
使用说明：生成js ,php 等语言函数注释,只需要在函数上面输入`/**` ,然后按<kbd>tab</kbd> 就会自动生成注释模板

#####  Emmet
使用说明：它让编写 HTML 代码变得简单。  
Emmet用法参见[Emmet插件使用方法总结](http://www.cnblogs.com/jesse131/p/4978966.html)

##### HTML-CSS-JS Prettify
使用说明：快速格式化html css js  
快捷键：<kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>h</kbd>

##### jQuery
使用说明：会出现jquery提示

##### LESS
使用说明：支持less语法高亮

##### SCSS
使用说明：支持SCSS语法高亮

##### SideBarEnhancements
使用说明：SideBarEnhancements 是一款很实用的右键菜单增强插件，有以 diff 形式显示未保存的修改、在文件管理器中显示该文件、复制文件路径、在侧边栏中定位该文件等功能，也有基础的诸如新建文件/目录，编辑，打开/运行，显示，在选择中/上级目录/项目中查找，剪切，复制，粘贴，重命名，删除，刷新等常见功能。

##### sublime tmpl
使用说明：按指定快捷键生成模板。  
快捷键：  
<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>h</kbd> 新建html模板文件  
<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>j</kbd> 新建javascript模板文件  
<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>c</kbd> 新建css模板文件  
<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>p</kbd> 新建php模板文件  
<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>r</kbd> 新建ruby模板文件  
<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>shift</kbd>+<kbd>p</kbd> 新建python模板文件  

##### SublimeCodeInte
使用说明：Sublime​Code​Intel 是一个代码提示、补全插件，支持 JavaScript、Mason、XBL、XUL、RHTML、SCSS、Python、HTML、Ruby、Python3、XML、Sass、XSLT、Django、HTML5、Perl、CSS、Twig、Less、Smarty、Node.js、Tcl、TemplateToolkit 和 PHP 等语言，是 Sublime Text 自带代码提示功能的很好扩展。

##### SublimeLinter
使用说明：它可以帮你找出错误或编写不规范的代码  需要安装nodejs,jshint,csslint

##### SublimeLinter-csslint
使用说明：对错误的css代码在状态栏进行提示，

##### SublimeLinter-jshint
使用说明：对错误的javascript代码在状态栏进行提示，

##### View In Browser
使用说明：sublime以本地服务器方式打开网页
为了使用插件，你需要建立一个sublime-project文件，点击Project->Edit Project
粘贴以下代码(这是我的相关配置),并保存到user目录下
```
{
    "folders":
    [
        {
            "path": "D:\\wamp\\www"    
        }
    ],
    "settings":
    {
        "sublime-view-in-browser":
        {
            "baseUrl": "http://localhost"  
            "basePath": "D:\\wamp\\www",   //本地虚拟主机根目录
        }
    }
}

```
快捷键：<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>v</kbd>

#####  MarkdownEditing
使用说明：它支持Markdown语法高亮显示。

#####  OmniMarkupPreviewer
使用说明：用来在浏览器中预览markdown 编辑的效果
快捷键：<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>o</kbd>

#####  Compact​Expand​Css
使用说明：css横竖向排列切换  
快捷键：  
<kbd>ctrl</kbd>+<kbd>alt</kbd><kbd>[</kbd>横向排列  
<kbd>ctrl</kbd>+<kbd>alt</kbd><kbd>]</kbd>竖向排列

##### Codelf
下载地址：[Codelf for Sublime Text](https://github.com/unbug/codelf/archive/st-0.0.3.zip)  
使用说明：变量命名神器Codelf通过搜索在线开源平台的项目源码帮开发者给变量命名 ，有了它再也不用为了命名而绞尽脑汁了  
快捷键：鼠标右键，选择Codelf

##### CodeFormatter
使用说明：代码格式化插件，主要用于PHP代码的格式化，要求php5.6及以上
快捷键：<kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>s</kbd>

#### 待定的插件
sublime git

YUI compress

livestyle

GBKEncoding support 中文支持

Terminal

#### NO.3 Sublime Text 3 快捷键大全
##### 选择类

Ctrl+D 选中光标所占的文本，继续操作则会选中下一个相同的文本。

Alt+F3 选中文本按下快捷键，即可一次性选择全部的相同文本进行同时编辑。 

Ctrl+L 选中整行，继续操作则继续选择下一行，效果和 Shift+↓ 效果一样。

Ctrl+Shift+L 先选中多行，再按下快捷键，会在每行行尾插入光标，即可同时编辑这些行。

Ctrl+Shift+M 选择括号内的内容（继续选择父括号）。

Ctrl+M 光标移动至括号内结束或开始的位置。

Ctrl+Enter 在下一行插入新行。举个栗子：即使光标不在行尾，也能快速向下插入一行。

Ctrl+Shift+Enter 在上一行插入新行。

Ctrl+Shift+[ 选中代码，按下快捷键，折叠代码。

Ctrl+Shift+] 选中代码，按下快捷键，展开代码。

Ctrl+K+0 展开所有折叠代码。

Ctrl+← 向左单位性地移动光标，快速移动光标。

Ctrl+→ 向右单位性地移动光标，快速移动光标。

shift+↑ 向上选中多行。

shift+↓ 向下选中多行。

Shift+← 向左选中文本。

Shift+→ 向右选中文本。

Ctrl+Shift+← 向左单位性地选中文本。

Ctrl+Shift+→ 向右单位性地选中文本。

Ctrl+Shift+↑ 将光标所在行和上一行代码互换（将光标所在行插入到上一行之前）。

Ctrl+Shift+↓ 将光标所在行和下一行代码互换（将光标所在行插入到下一行之后）。

Ctrl+Alt+↑ 向上添加多行光标，可同时编辑多行。

Ctrl+Alt+↓ 向下添加多行光标，可同时编辑多行。

##### 编辑类

Ctrl+J 合并选中的多行代码为一行。举个栗子：将多行格式的CSS属性合并为一行。

Ctrl+Shift+D 复制光标所在整行，插入到下一行。

Tab 向右缩进。

Shift+Tab 向左缩进。

Ctrl+K+K 从光标处开始删除代码至行尾。

Ctrl+Shift+K 删除整行。

Ctrl+/ 注释单行。

Ctrl+Shift+/ 注释多行。

Ctrl+K+U 转换大写。

Ctrl+K+L 转换小写。

Ctrl+Z 撤销。

Ctrl+Y 恢复撤销。

Ctrl+U 软撤销，感觉和 Gtrl+Z 一样。

Ctrl+F2 设置书签

Ctrl+T 左右字母互换。

F6 单词检测拼写

##### 搜索类

Ctrl+F 打开底部搜索框，查找关键字。

Ctrl+shift+F 在文件夹内查找

Ctrl+P 打开搜索框。举个栗子：1、输入当前项目中的文件名，快速搜索文件，2、输入@和关键字，查找文件中函数名，3、输入：和数字，跳转到文件中该行代码，4、输入#和关键字，查找变量名。

Ctrl+G 打开搜索框，自动带：，输入数字跳转到该行代码。

Ctrl+R 打开搜索框，自动带@，输入关键字，查找文件中的函数名。举个栗子：在函数较多的页面快速查找某个函数。

Ctrl+： 打开搜索框，自动带#，输入关键字，查找文件中的变量名、属性名等。

Ctrl+Shift+P 打开命令框。

Esc 退出光标多行选择，退出搜索框，命令框等。

##### 显示类

Ctrl+Tab 按文件浏览过的顺序，切换当前窗口的标签页。

Ctrl+PageDown 向左切换当前窗口的标签页。

Ctrl+PageUp 向右切换当前窗口的标签页。

Alt+Shift+1 窗口分屏，恢复默认1屏（非小键盘的数字）

Alt+Shift+2 左右分屏-2列

Alt+Shift+3 左右分屏-3列

Alt+Shift+4 左右分屏-4列

Alt+Shift+5 等分4屏

Alt+Shift+8 垂直分屏-2屏

Alt+Shift+9 垂直分屏-3屏

Ctrl+K+B 开启/关闭侧边栏。

F11：全屏模式

Shift+F11 免打扰模式

