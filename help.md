## Manual of Flamingo

[中文帮助手册请点我](https://openfibers.github.io/flamingo/help_cn)

### To Use Keyboard Mapping, Add Flamingo to Accessability

1. Open System Preferences.app  
2. Go to "Security & Privacy -> Privacy -> Accessability"  
3. Add Flamingo.app to allowed list   
* You can still map mouse button to any key without doing this.  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/privacy_en.png" alt="privacy_en" style="width: 668px;"/>

### Keyboard Map

Let's make a simple keyboard map, we press 1, it goes to 2.  
First, open Preferences:  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/preferences.png" alt="preferences" style="width: 303px;"/>

Preferences window looks like this: 

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/keymap1.png" alt="keymap1" style="width: 480px;"/>

Add lines into configrations, and click "Save":  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/keymap2.png" alt="keymap2" style="width: 480px;"/>

If there's no JSON syntax error detected, switch to "Map List" page, it will look like this:  

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/keymap3.png" alt="keymap3" style="width: 480px;"/>

And just have a try to tap '1' : )

### Mouse Button Map

You can also map mouse button. 

For example: press mouse right button, goes to whitespace:

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
Or press whitespace, goes to mouse right button:

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

### Configuration alias

Use "alias" to remember what a mapping do. For example, note the mapping we made as "Right button to whitespace":
```
{
  "map" : [
    {
      "alias" : "Right button to whitespace",
      "from" : "mouse1",
      "to" : "space"
    }
  ]
}
```

<img src="https://github.com/OpenFibers/flamingo/raw/master/Images/alias.png" alt="alias" style="width: 480px;"/>

### Combination press

Flamingo supports modifier keys. Make a map control + P to up (which makes every app work like emacs):

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

Or Control + Shift + p to Shift + Up:

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

* Flamingo do not support only modifier key map to other keys.

### Macro

Press option + H, enter a "hello":

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

Press option + W, enter a "hello", and wait for 500 milliseconds, enter a "world", and press command + s to save:

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

### Shell Script Hotkey

Use "script" to execute shell script in Terminal.app. For example, press control + 0, open Terminal, execute cd ~/project && git pull:  

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

### AppleScript Hotkey

[AppleScript](https://developer.apple.com/library/archive/documentation/AppleScript/Conceptual/AppleScriptLangGuide/introduction/ASLR_intro.html) is a scripting language created by Apple. It allows users to directly control scriptable Macintosh applications, as well as parts of macOS itself. Users can do almost anything to macOS by using AppleScript.

Use "AppleScript" to execute an AppleScript. For example, press control + 1, execute an AppleScript to read "Hello World":  

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

### All Key Definations

Normal keys:   
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

Mouse Buttons:
(mouse0 is left button, mouse1 is right button, mouse2 is middle button, other mouse buttons from mouse3):
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

Modifier Keys:  
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
