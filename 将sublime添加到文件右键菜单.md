# 将sublime添加文件右键菜单

## 方法一：

新建sublime_addright.reg文件 编辑后双击打开就OK

括号内是sublime安装路径

open sublimeText3 是提示文字

```txt
Windows Registry Editor Version 5.00
[HKEY_CLASSES_ROOT\*\shell\SublimeText3]
@="open SublimeText3 "
"Icon"="(D:\\software\\Sublime Text 3\\sublime_text.exe),0"
[HKEY_CLASSES_ROOT\*\shell\SublimeText3\command]
@="(D:\\software\\Sublime Text 3\\sublime_text.exe) %1"
[HKEY_CLASSES_ROOT\Directory\shell\SublimeText3]
@="open SublimeText3 "
"Icon"="(D:\\software\\Sublime Text 3\\sublime_text.exe),0"
[HKEY_CLASSES_ROOT\Directory\shell\SublimeText3\command]
@="(D:\\software\\Sublime Text 3\\sublime_text.exe) %1"
```

## 方法二：

### 1. 先打开regedit注册表

在`win+R`输入regedit打开注册表

### 2. 依次找到HKEY_CLASSESS_ROOT->*->Shell，下面新建项，命名为Edit with Sublime Text3。

### 3. .在项“Edit with Sublime Text”下新建字符串值，命名为Icon，值为 E:\百度云同步盘\前端软件\64位sublime text3\Sublime Text 3\sublime_text.exe,0 

PS:0前边的是sublime text在你电脑上的安装位置

### 4. .在项“Edit with Sublime Text”下新建项Command，Command项下默认值修改为 E:\百度云同步盘\前端软件\64位sublime text3\Sublime Text 3\sublime_text.exe %1

### 5. 设置完成后，确定，退出。现在右键菜单中就出现了”Edit with sublime text3".(亲测有效，嘿嘿）





