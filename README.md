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
正值表示车轮向上移动。  
负值表示车轮向下移动。
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
elapsed GetRunningTime()

```
## 参数
无
## 返回值
elapsed     
包含以毫秒为单位的运行时间的整数值。
## 备注
您可以使用它来计算脚本中的时间。
## 示例
```
time = GetRunningTime() --获取系统运行时间
OutputLogMessage("运行时间：",time)
```
***
#