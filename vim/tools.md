# Windows 系统配置 shell开发环境

[cygwin](https://www.cygwin.com/)


#### cmder 配置

###### [cmder官方网址](https://cmder.net/)

###### [cmder下载地址](https://github.com/cmderdev/cmder/releases/)

###### 二、 配置Windows环境变量

###### 三、 配置右键快捷启动：

```bash
以管理员身份打开cmd，执行以下命令即可，完了以后在任意地方点击右键即可使用cmder
	// 设置任意地方鼠标右键启动Cmder
	Cmder.exe /REGISTER ALL
```

###### 四、 将命令提示改成$

1)首先在cmder的安装目录下,找到vendor/目录，然后找到clink.lua文件
3)打开后可以Ctrl+F查找下面的字段
	local lambda =
4)将local lambda =""的值替换成$

###### 五、 关于Cmder的一些常用快捷键

```bash
Tab       自动路径补全
Ctrl+T    建立新页签
Ctrl+W    关闭页签
Ctrl+Tab  切换页签
Alt+F4    关闭所有页签
Alt+Shift+1 开启cmd.exe
Alt+Shift+2 开启powershell.exe
Alt+Shift+3 开启powershell.exe (系统管理员权限)
Ctrl+1      快速切换到第1个页签
Ctrl+n      快速切换到第n个页签( n值无上限)
Alt + enter 切换到全屏状态
Ctr+r       历史命令搜索
Tab         自动路径补全
Ctrl+T      建立新页签
Ctrl+W      关闭页签
Ctrl+Tab    切换页签
Alt+F4      关闭所有页签
Alt+Shift+1 开启cmd.exe
Alt+Shift+2 开启powershell.exe
Alt+Shift+3 开启powershell.exe (系统管理员权限)
Ctrl+1      快速切换到第1个页签
Ctrl+n      快速切换到第n个页签( n值无上限)
Alt + enter 切换到全屏状态
Ctr+r       历史命令搜索
Win+Alt+P   开启工具选项视窗
```

###### 六、关于中文乱码问题：

将下面的4行命令添加到cmder/config/aliases文件末尾,如果还是不行参考前面字体设置，将前面提到的字体设置里面的Monospace的复选框不选中。还有就是养成良好的编码习惯文件命名最好不要有中文。

```bash
l=ls --show-control-chars 
la=ls -aF --show-control-chars 
ll=ls -alF --show-control-chars 
ls=ls --show-control-chars -F
```
