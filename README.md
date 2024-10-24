# Cat-LUAmacro-API
cat Lua API是一组使用Lua编程语言的函数,可以轻松对键鼠进行各种宏操作。
***
# 脚本的事件处理函数
在 cat Lua 中你需要实施 setup() 和 loop() 。
```
function setup() --初始化
 --添加代码
end

function loop() --连续运行
    --添加代码
    Sleep(1) --添加休眠来节约cpu资源
end 
```
## setup()
setup() 他会在最开始运行，且只运行一次。
## loop()
loop() 他会在setup后运行，且无限循环。
***
# BlockedMouse()
BlockedMouse()函数用于屏蔽鼠标按键
```
BlockedMouse( keyCode [,keyCode] )
BlockedMouse( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
BlockedMouse(272)
BlockedMouse("BTN_LEFT")
BlockedMouse("BTN_LEFT", "BTN_RIGHT") 
```
***
# UnblockedMouse()
UnblockedMouse()函数用于取消屏蔽鼠标按键
```
UnblockedMouse( keyCode [,keyCode] )
UnblockedMouse( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
UnblockedMouse(272)
UnblockedMouse("BTN_LEFT")
UnblockedMouse("BTN_LEFT", "BTN_RIGHT") 
```
***
# BlockedKey()
BlockedMouse()函数用于屏蔽键盘按键
```
BlockedKey( keyCode [,keyCode] )
BlockedKey( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
BlockedKey(30)
BlockedKey("KEY_A")
BlockedKey("KEY_A", "KEY_B") 
```
***
# UnblockedKey()
UnblockedKey()函数用于取消屏蔽键盘按键
```
UnblockedKey( keyCode [,keyCode] )
UnblockedKey( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
UnblockedKey(30)
UnblockedKey("KEY_A")
UnblockedKey("KEY_A", "KEY_B") 
```
***
# PressKey()
PressKey()函数用于模拟点击键盘按键。
```
PressKey( keyCode [,keyCode] )
PressKey( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
PressKey()(30)
PressKey()("KEY_A")
PressKey()("KEY_A", "KEY_B") 
```
***
# ReleaseKey()
ReleaseKey()函数用于模拟释放键盘按键。
```
ReleaseKey( keyCode [,keyCode] )
ReleaseKey( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
ReleaseKey()(30)
ReleaseKey()("KEY_A")
ReleaseKey()("KEY_A", "KEY_B") 
```
***
# PressAndReleaseKey()
PressAndReleaseKey()函数用于模拟释放键盘按键。   
默认按下50ms后释放，可以使用time指定按下时间。
```
PressAndReleaseKey( keyCode )
PressAndReleaseKey( keyName )
PressAndReleaseKey( keyCode, time )
PressAndReleaseKey( keyName, time )
PressAndReleaseKey( time, keyCode [,keyCode] )
PressAndReleaseKey( time, keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。

time    
按下多少ms后释放
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
PressAndReleaseKey()(30)
PressAndReleaseKey()(30, 50)
PressAndReleaseKey()("KEY_A")
PressAndReleaseKey()("KEY_A", 50) 
PressAndReleaseKey()(50, 30, 31) 
PressAndReleaseKey()(50, "KEY_A",  "KEY_B") 
```
***
# PressMouseButton()
PressMouseButton()函数用于模拟点击鼠标按键。
```
PressMouseButton( keyCode [,keyCode] )
PressMouseButton( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
PressMouseButton()(272)
PressMouseButton()("BTN_LEFT")
PressMouseButton()("BTN_LEFT", "BTN_RIGHT") 
```
***
# ReleaseMouseButton()
ReleaseMouseButton()函数用于模拟释放鼠标按键。
```
ReleaseMouseButton( keyCode [,keyCode] )
ReleaseMouseButton( keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
ReleaseMouseButton()(272)
ReleaseMouseButton()("BTN_LEFT")
ReleaseMouseButton()("BTN_LEFT", "BTN_RIGHT") 
```
***
# PressAndReleaseMouseButton()
PressAndReleaseKey()函数用于模拟释放鼠标按键。   
默认按下50ms后释放，可以使用time指定按下时间。
```
PressAndReleaseMouseButton( keyCode )
PressAndReleaseMouseButton( keyName )
PressAndReleaseMouseButton( keyCode, time )
PressAndReleaseMouseButton( keyName, time )
PressAndReleaseMouseButton( time, keyCode [,keyCode] )
PressAndReleaseMouseButton( time, keyName [,keyName] )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。

time    
按下多少ms后释放
## 返回值
无
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
PressAndReleaseMouseButton()(272)
PressAndReleaseMouseButton()(272, 50)
PressAndReleaseMouseButton()("BTN_LEFT")
PressAndReleaseMouseButton()("BTN_LEFT", 50) 
PressAndReleaseMouseButton()(50, 272, 273) 
PressAndReleaseMouseButton()(50, "BTN_LEFT",  "BTN_RIGHT") 
```
***
# MoveMouseWheel()
MoveMouseWheel()函数用于模拟鼠标滚轮的移动。
```
MoveMouseWheel( click )
```
## 参数
click  
鼠标滚轮的滚动次数。
## 返回值
无
## 备注
正值表示滚轮向上移动。  
负值表示滚轮向下移动。
## 示例
```
MoveMouseWheel(3)
MoveMouseWheel(-1)
```
***
# MoveMouseRelative()
MoveMouseRelative()函数用于模拟鼠标的相对移动。
```
MoveMouseRelative( x, y )
```
## 参数
x   
沿x轴移动

Y   
沿y轴移动
## 返回值
无
## 备注
正x值模拟向右移动。  
负x值模拟向左移动。  
正y值模拟向下移动。  
负y值模拟向上移动。  
## 示例
```
-- 循环50次，模拟鼠标向下移动
for i = 0, 50 do
    MoveMouseRelative(0, 1)
    Sleep(8)
end

```
***
# IsKeyLockOn()
IsKeyLockOn()函数用于确定特定的锁定按钮当前是否在启用状态。
```
MoveMouseWheel( keyCode )
MoveMouseWheel( keyName )
```
## 参数
keyCode
指定要按下的键的数字扫描代码。

keyName
指定要按的键的预定义注释记号。   

| keyCode | keyName      | Location    |
|---------|--------------|-------------|
| 0       | “scrolllock” | Scroll Lock |
| 1       | “capslock”   | Caps Lock   |
| 2       | “numlock”    | Number Lock |

## 返回值
如果当前已启用锁定，则为True，否则为false
## 备注
None
## 示例
```
 --numlock = IsKeyLockOn(0) --键盘锁定灯光状态获取
 --capslock = IsKeyLockOn(1)
 --scrolllock = IsKeyLockOn(2)

 numlock = IsKeyLockOn("NUMLOCK")
 capslock = IsKeyLockOn("CAPSLOCK")
 scrolllock = IsKeyLockOn("SCROLLLOCK")

 OutputLogMessage("键盘灯光状态：",numlock,capslock,scrolllock)
```
***
# IsMouseButtonPressed()
IsMouseButtonPressed()函数用于确定鼠标按钮是否当前处于按下状态。
```
IsMouseButtonPressed( keyCode )
IsMouseButtonPressed( keyName )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
如果当前按下按钮，则为True，否则为false。
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
if IsMouseButtonPressed( 272 ) then --监听到鼠标左键按下
    OutputLogMessage("鼠标左键按下")
end
if IsMouseButtonPressed( "BTN_RIGHT" ) then --监听到鼠标右键按下
    OutputLogMessage("鼠标右键按下")
end
```
***
# IsKeyboardButtonPressed()
IsKeyboardButtonPressed()函数用于确定键盘按钮是否当前处于按下状态。
```
IsKeyboardButtonPressed( keyCode )
IsKeyboardButtonPressed( keyName )
```
## 参数
keyCode  
指定要按下的键的数字扫描代码。

keyName  
指定要按的键的预定义注释记号。
## 返回值
如果当前按下按钮，则为True，否则为false。
## 备注
有关扫描代码和注释记号的值，请参阅附录。
## 示例
```
if IsKeyboardButtonPressed( 30 ) then --监听到键盘A按下
    OutputLogMessage("键盘A按下")
end
if IsKeyboardButtonPressed( "KEY_B" ) then --监听到键盘B按下
    OutputLogMessage("键盘B按下")
end
```
***
# Sleep()
Sleep()将导致脚本暂停所需的时间。
```
Sleep( timeout )

```
## 参数
timeout     
睡眠总时间（毫秒）
## 返回值
无
## 备注
无
## 示例
```
Sleep(20) --延时20ms
```
***
# OutputLogMessage()
OutputLogMessage()将向脚本编辑器的控制台发送日志消息
```
OutputLogMessage( ... )

```
## 参数
 ...    
字符串或者变量
## 返回值
无
## 备注
无
## 示例
```
a = 123
OutputLogMessage("Hello World", 2047, a)
```
***
# GetRunningTime()
GetRunningTime()返回自系统运行时间
```
int GetRunningTime()

```
## 参数
无
## 返回值
int     
包含以毫秒为单位的运行时间的整数值。
## 备注
您可以使用它来计算脚本中的时间。
## 示例
```
time = GetRunningTime() --获取系统运行时间
OutputLogMessage("运行时间：",time)
```
***
# 键值附录

## 键盘按键对应表

| 按键名               | 值   |
|----------------------|------|
| KEY_RESERVED         | 0    |
| KEY_ESC              | 1    |
| KEY_1                | 2    |
| KEY_2                | 3    |
| KEY_3                | 4    |
| KEY_4                | 5    |
| KEY_5                | 6    |
| KEY_6                | 7    |
| KEY_7                | 8    |
| KEY_8                | 9    |
| KEY_9                | 10   |
| KEY_0                | 11   |
| KEY_MINUS            | 12   |
| KEY_EQUAL            | 13   |
| KEY_BACKSPACE        | 14   |
| KEY_TAB              | 15   |
| KEY_Q                | 16   |
| KEY_W                | 17   |
| KEY_E                | 18   |
| KEY_R                | 19   |
| KEY_T                | 20   |
| KEY_Y                | 21   |
| KEY_U                | 22   |
| KEY_I                | 23   |
| KEY_O                | 24   |
| KEY_P                | 25   |
| KEY_LEFTBRACE        | 26   |
| KEY_RIGHTBRACE       | 27   |
| KEY_ENTER            | 28   |
| KEY_LEFTCTRL         | 29   |
| KEY_A                | 30   |
| KEY_S                | 31   |
| KEY_D                | 32   |
| KEY_F                | 33   |
| KEY_G                | 34   |
| KEY_H                | 35   |
| KEY_J                | 36   |
| KEY_K                | 37   |
| KEY_L                | 38   |
| KEY_SEMICOLON        | 39   |
| KEY_APOSTROPHE       | 40   |
| KEY_GRAVE            | 41   |
| KEY_LEFTSHIFT        | 42   |
| KEY_BACKSLASH        | 43   |
| KEY_Z                | 44   |
| KEY_X                | 45   |
| KEY_C                | 46   |
| KEY_V                | 47   |
| KEY_B                | 48   |
| KEY_N                | 49   |
| KEY_M                | 50   |
| KEY_COMMA            | 51   |
| KEY_DOT              | 52   |
| KEY_SLASH            | 53   |
| KEY_RIGHTSHIFT       | 54   |
| KEY_KPASTERISK       | 55   |
| KEY_LEFTALT          | 56   |
| KEY_SPACE            | 57   |
| KEY_CAPSLOCK         | 58   |
| KEY_F1               | 59   |
| KEY_F2               | 60   |
| KEY_F3               | 61   |
| KEY_F4               | 62   |
| KEY_F5               | 63   |
| KEY_F6               | 64   |
| KEY_F7               | 65   |
| KEY_F8               | 66   |
| KEY_F9               | 67   |
| KEY_F10              | 68   |
| KEY_NUMLOCK          | 69   |
| KEY_SCROLLLOCK       | 70   |
| KEY_KP7              | 71   |
| KEY_KP8              | 72   |
| KEY_KP9              | 73   |
| KEY_KPMINUS          | 74   |
| KEY_KP4              | 75   |
| KEY_KP5              | 76   |
| KEY_KP6              | 77   |
| KEY_KPPLUS           | 78   |
| KEY_KP1              | 79   |
| KEY_KP2              | 80   |
| KEY_KP3              | 81   |
| KEY_KP0              | 82   |
| KEY_KPDOT            | 83   |
| KEY_ZENKAKUHANKAKU   | 85   |
| KEY_102ND            | 86   |
| KEY_F11              | 87   |
| KEY_F12              | 88   |
| KEY_RO               | 89   |
| KEY_KATAKANA         | 90   |
| KEY_HIRAGANA         | 91   |
| KEY_HENKAN           | 92   |
| KEY_KATAKANAHIRAGANA | 93   |
| KEY_MUHENKAN         | 94   |
| KEY_KPJPCOMMA        | 95   |
| KEY_KPENTER          | 96   |
| KEY_RIGHTCTRL        | 97   |
| KEY_KPSLASH          | 98   |
| KEY_SYSRQ            | 99   |
| KEY_RIGHTALT         | 100  |
| KEY_LINEFEED         | 101  |
| KEY_HOME             | 102  |
| KEY_UP               | 103  |
| KEY_PAGEUP           | 104  |
| KEY_LEFT             | 105  |
| KEY_RIGHT            | 106  |
| KEY_END              | 107  |
| KEY_DOWN             | 108  |
| KEY_PAGEDOWN         | 109  |
| KEY_INSERT           | 110  |
| KEY_DELETE           | 111  |
| KEY_MACRO            | 112  |
| KEY_MUTE             | 113  |
| KEY_VOLUMEDOWN       | 114  |
| KEY_VOLUMEUP         | 115  |
| KEY_POWER            | 116  |
| KEY_KPEQUAL          | 117  |
| KEY_KPPLUSMINUS      | 118  |
| KEY_PAUSE            | 119  |
| KEY_SCALE            | 120  |
| KEY_KPCOMMA          | 121  |
| KEY_HANGEUL          | 122  |
| KEY_HANGUEL          | 122  |
| KEY_HANJA            | 123  |
| KEY_YEN              | 124  |
| KEY_LEFTMETA         | 125  |
| KEY_RIGHTMETA        | 126  |
| KEY_COMPOSE          | 127  |
| KEY_STOP             | 128  |
| KEY_AGAIN            | 129  |
| KEY_PROPS            | 130  |
| KEY_UNDO             | 131  |
| KEY_FRONT            | 132  |
| KEY_COPY             | 133  |
| KEY_OPEN             | 134  |
| KEY_PASTE            | 135  |
| KEY_FIND             | 136  |
| KEY_CUT              | 137  |
| KEY_HELP             | 138  |
| KEY_MENU             | 139  |
| KEY_CALC             | 140  |
| KEY_SETUP            | 141  |
| KEY_SLEEP            | 142  |
| KEY_WAKEUP           | 143  |
| KEY_FILE             | 144  |
| KEY_SENDFILE         | 145  |
| KEY_DELETEFILE       | 146  |
| KEY_XFER             | 147  |
| KEY_PROG1            | 148  |
| KEY_PROG2            | 149  |
| KEY_WWW              | 150  |
| KEY_MSDOS            | 151  |
| KEY_COFFEE           | 152  |
| KEY_SCREENLOCK       | 152  |
| KEY_ROTATE_DISPLAY   | 153  |
| KEY_DIRECTION        | 153  |
| KEY_CYCLEWINDOWS     | 154  |
| KEY_MAIL             | 155  |
| KEY_BOOKMARKS        | 156  |
| KEY_COMPUTER         | 157  |
| KEY_BACK             | 158  |
| KEY_FORWARD          | 159  |
| KEY_CLOSECD          | 160  |
| KEY_EJECTCD          | 161  |
| KEY_EJECTCLOSECD     | 162  |
| KEY_NEXTSONG         | 163  |
| KEY_PLAYPAUSE        | 164  |
| KEY_PREVIOUSSONG     | 165  |
| KEY_STOPCD           | 166  |
| KEY_RECORD           | 167  |
| KEY_REWIND           | 168  |
| KEY_PHONE            | 169  |
| KEY_ISO              | 170  |
| KEY_CONFIG           | 171  |
| KEY_HOMEPAGE         | 172  |
| KEY_REFRESH          | 173  |
| KEY_EXIT             | 174  |
| KEY_MOVE             | 175  |
| KEY_EDIT             | 176  |
| KEY_SCROLLUP         | 177  |
| KEY_SCROLLDOWN       | 178  |
| KEY_KPLEFTPAREN      | 179  |
| KEY_KPRIGHTPAREN     | 180  |
| KEY_NEW              | 181  |
| KEY_REDO             | 182  |

## 鼠标按键对应表

| 按键名         | 值   |
|-------------|-----|
| BTN_LEFT    | 272 |
| BTN_RIGHT   | 273 |
| BTN_MIDDLE  | 274 |
| BTN_SIDE    | 275 |
| BTN_EXTRA   | 276 |
| BTN_FORWARD | 277 |
| BTN_BACK    | 278 |
| BTN_TASK    | 279 |
