---
layout: post_user
title: "Windows  打开方式[ 程序 ] 选择"
description: ""
category: 
tags: []
---
{% include JB/setup %}

### 问题：
  电脑有时候文件会出现打开方式错误，举例：我的电脑就在使用了一段时间后，出现了caj文件不能打开的问题
### 解决方法
  1. 使用软件--->FileTypesMan, 这个软件可以修复图标及打开方式关联的问题 <http://www.nirsoft.net/utils/file_types_manager.html>
  2. 手工修复：
     - 清除打开方式，注册表方法：regedit 呼出【注册表】-> HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\FileExts，选中想要处理的文件类型，并点击前面的加号，展开整个列表，点击OpenWithList，在右侧窗格中显示了所有可以用来打开该类型文件的程序，删除不希望在“打开方式”列表中出现的程序。
     - 修改打开方式，注册表方法：regedit 呼出【注册表】->HEKY_CLASSES_ROOT \ Application, 子项里面有各个安装程序的shell，shell下的open项内有command值，这个值就是打开时运行的命令行，在这里可以根据需要更改你需要的程序。比如我的就是["D:\Program Files\Office\CAJViewer7.2\CAJVieweru.exe" "%1"]
     - 更新默认打开方式和图标，此时，在欲打开的文件上右击-> 打开方式，选择所遇要的程序即可。 更改图标时，可使用软件**FileTypesMan**
