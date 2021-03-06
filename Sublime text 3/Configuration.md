# Sublime text 3 配置
## 基础用户配置
工具栏 Preferences – Settings-User 进入用户设置：
配置代码
```bash
"trim_trailing_white_space_on_save": true,
"ensure_newline_at_eof_on_save": true,
"font_face": "Microsoft YaHei Mono",
"disable_tab_abbreviations": true,
"translate_tabs_to_spaces": true,
"tab_size": 2,
"draw_minimap_border": true,
"save_on_focus_lost": true,
"highlight_line": true,
"word_wrap": "true",
"fade_fold_buttons": false,
"bold_folder_labels": true,
"highlight_modified_tabs": true,
"default_line_ending": "unix", 
"auto_find_in_selection": true
```
## 解释说明

`trim_trailing_white_space_on_save`

自动移除行尾多余空格，处女座更安心了。

`ensure_newline_at_eof_on_save`

文件末尾自动保留一个空行，懂的人自然知道它的用处。

`font_face`

设置字体。Microsoft YaHei Mono 是一款混合字体，专为代码优化，看起来很舒服。当然你也可以使用你自己喜欢的字体，或者删掉本行，使用默认字体。

`disable_tab_abbreviations`

设置为 true ，禁用 Emmet 的 tab 键功能（请使用 ctrl+e），系统自带的 tab 功能还是可圈可点的。当然你也可以不设置它，以完全使用 Emmet 的 tab 补全功能。

`translate_tabs_to_spaces`

很明白就是把代码 tab 对齐转换为空格对齐，tab_size 配合设置空格数。这个需求因人而异了，不喜欢可以去掉。

`draw_minimap_border`

用于右侧代码预览时给所在区域加上边框，方便识别。

`save_on_focus_lost`

窗口失焦立即保存文件，嘛嘛再也不用担心你忘记保存了。

`highlight_line`

当前行高亮。

`word_wrap`

设置自动换行。

`fade_fold_buttons`

默认显示行号右侧的代码段闭合展开三角号。

`bold_folder_labels`

侧边栏文件夹显示加粗，区别于文件。

`highlight_modified_tabs`

高亮未保存文件。

`default_line_ending: "unix"`

使用 unix 风格的换行符。

`auto_find_in_selection: true`

开启选中范围内搜索（而不是整个文档

## 默认快捷键设置

工具栏 Preferences – key Bindings-User 进入用户快捷键设置

配置代码
```bash
{ "keys": ["alt+space"], "command": "auto_complete" },
{ "keys": ["alt+space"], "command": "replace_completion_with_auto_complete", "context":
  [
    { "key": "last_command", "operator": "equal", "operand": "insert_best_completion" },
    { "key": "auto_complete_visible", "operator": "equal", "operand": false },
    { "key": "setting.tab_completion", "operator": "equal", "operand": true }
  ]
},
{ "keys": ["ctrl+alt+d"], "command": "goto_definition" },
```
ST3默认的代码提示快捷键为 ctrl + space ，但是这个快捷键在天朝一直都被输入法霸占( Mac用户泥奏凯 ，修改快捷键为alt+space 。
ST3自带跳转到函数或CSS定义功能，在DreamWeaver中使用 ctrl+d 打开CSS样式定义源面板屡试不爽。使用 ctrl+alt+d 定义这个功能，ST3默认的ctrl+d已有选择相同字符的用途。

PS.关于Emmet 及 ST3 的快捷键什么的网上一找一堆，这里举几个个人常用的快捷键：

ctrl+shift+p 所有命令

ctrl+g 跳转行

ctrl+/ 注释

ctrl+d选择相同字符

ctrl+shift+up/down 整行移动

ctrl+alt+right 跳到下一个编辑点

ctrl+u图片原始大小更新

ctrl+shift+g 批量格式生成

ctrl+shift+y直接公式计算

ctrl+up CSS数值加减1（alt+up 数值加减0.1）

## 配置shell开发环境

Sublime text 3 安装shell语法提示插件

点击“Preference”-->“Package Control”-->输入：shell-->选择"ShellScriptimproved"
![image](https://user-images.githubusercontent.com/65467296/167058625-6654df37-5b07-4abd-9bb8-a9e1e5db7e82.png)
## Sublime Text3 Terminal 调用 cmder
1.打开 Preferences>Package Control，选择Install Package

2.在搜索框输入Terminal，在搜索结果里点击Terminal 安装

3.打开 Preferences > Package setting > Terminal > Setting -User

4.输入下面的配置代码

```bash

{
    "terminal": "C:\\windows\\system32\\cmd.exe",
    "parameters": ["/START","%CWD%"]
}
```
重启Sublime Text3
在编辑的文件窗口按快捷键ctrl+shift+t打开cmd





