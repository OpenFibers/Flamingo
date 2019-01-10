## Flamingo使用手册

[For Englist Manual, Click Here](https://openfibers.github.io/flamingo/help)

### 为了按键映射能正常使用，首先将Flamingo添加到辅助功能
1. 打开系统偏好设置 App
2. 打开 "安全性与隐私 -> 隐私 -> 辅助功能"  
3. 添加 Flamingo.app 到右侧列表中  
* 即使不加到辅助功能中，也可以映射鼠标到键盘按键。  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/privacy_cn.png" alt="privacy_cn" style="width: 668px;"/>

### 按键映射

我们从最简单的开始，把1映射到2上面。  
首先打开 Preferences:  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/preferences.png" alt="preferences" style="width: 303px;"/>

打开的窗口应该是长成这样的：   

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/keymap1.png" alt="keymap1" style="width: 480px;"/>

我们写几行代表映射的配置进去，然后点击 "Save":  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/keymap2.png" alt="keymap2" style="width: 480px;"/>

如果 JSON 语法是正确的，切到 "Map List" 页面，应该是长成这样的：  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/keymap3.png" alt="keymap3" style="width: 480px;"/>

现在试试看按下 '1' 会发生什么: )

### 鼠标按键映射

Flamingo也可以用来映射鼠标按键。  
举个例子，把鼠标右键映射为空格：  

```
{
  "map" : [
    {
      "from" : "mouse1",
      "to" : "space"
    }
  ]
}
```
或者把空格映射为鼠标右键：  

```
{
  "map" : [
    {
      "from" : "space",
      "to" : "mouse1"
    }
  ]
}
```

### 给配置起个别名

使用 "alias" 字段给每条配置起名。举个例子，把我们刚才的映射起个名叫 "右键到空格":
```
{
  "map" : [
    {
      "alias" : "右键到空格",
      "from" : "mouse1",
      "to" : "space"
    }
  ]
}
```

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/alias_cn.png" alt="alias_cn" style="width: 480px;"/>

### 组合键

Flamingo 支持组合键。比如映射 control + P 到方向键上 (让emacs用户操作任何app都像emacs):

```
{
  "map" : [
    {
      "from" : "control p",
      "to" : "up"
    }
  ]
}
```

或者映射 Control + Shift + p 到 Shift + Up:

```
{
  "map" : [
    {
      "from" : "control shift p",
      "to" : "shift up"
    }
  ]
}
```

* 但是注意，Flamingo不支持单独按下修饰键映射到其他按键。

### 宏

按下 option + H, 输入 "hello":

```
{
  "map" : [
    {
      "from" : "option h",
      "to" : "h e l l o"
    }
  ]
}
```

按下 option + W, 输入 "hello", 然后等待 500 毫秒, 再输入 "world", 最后自动按下 command + s 来保存文件:

```
{
  "map" : [
    {
      "from" : "option w",
      "to" : "h e l l o sleep 500 w o r l d command s"
    }
  ]
}
```

### Shell 脚本热键

使用 "script" 在 Terminal 中来执行 shell 脚本。举个例子，按 control + 0，打开 Terminal，执行 cd ~/project && git pull:  

```
{
  "map" : [
    {
      "from" : "control 0",
      "script" : "cd ~/project && git pull"
    }
  ]
}
```

### AppleScript 脚本热键

使用 "AppleScript" 来执行一段 AppleScript 脚本. 举个例子, 按 control + 1, 读出 "Hello World":  

```
{
  "map" : [
    {
      "from" : "control 1",
      "AppleScript" : "say \"Hello World\""
    }
  ]
}
```

### 所有按键定义

普通按键:   
```
A
B
C
D
E
F
G
H
I
J
K
L
M
N
O
P
Q
R
S
T
U
V
W
X
Y
Z

1
2
3
4
5
6
7
8
9
0

F1
F2
F3
F4
F5
F6
F7
F8
F9
F10
F11
F12
F13
F14
F15

escape
backspace
tab
return

`
-
=
[
]
\
;
'
,
.
/

insert
delete
home
end
pageup
pagedown

left
right       
down
up

num0
num1
num2
num3
num4
num5
num6
num7
num8
num9
num0
num.
num+
num-
num*
num/
numlock
enter
```

鼠标按键:
(mouse0 代表左键, mouse1 代表右键, mouse2 代表中键, 从 mouse3 开始是鼠标其他按键):
```
mouse0
mouse1
mouse2
mouse3
mouse4
mouse5
...
mouse99
```

组合键的修饰键:  
```
capslock
shift
rshift
control
rcontrol
option
roption
command
rcommand
fn
```
