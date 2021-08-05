# Auto program feature in Arduino Ameba platform.

Here is patched for auto program flash without push BUN and RESET buttons.

# Install ameba
You can reference below link to get started: http://www.amebaiot.com/ameba-arduino-getting-started/

# Patch your environment

* Windows

Download and replace upload_image_tool_windows.exe to your installed folder.<br/>
ex: C:\Users\xxxxxx\AppData\Local\Arduino15\packages\realtek\tools\ameba_d_tools\1.0.5

* Linux

Download and replace upload_image_tool_linux to your installed folder.<br/>
ex: ~/snap/arduino/61/.arduino15/packages/realtek/tools/ameba_d_tools/1.0.5
<font color="red">It's not work yet due to tool amebad_image_tool.<font>

* MacOS

Download and replace upload_image_tool_macos to your installed folder.<br/>
ex: ~/Library/Arduino15/packages/realtek/tools/ameba_d_tools/1.0.5
<font color="red">It's not work yet due to tool amebad_image_tool.<font>

# Hardware modication:
It needs to add special compoments likes ESP8266/ESP32 auto program circuit.
<br/>nRST => EN , BW16_Pin3
<br/>GPIO0 => LOG_TX ,BW16_Pin11

![](https://i.stack.imgur.com/fMrDh.png?raw=true)

# Other infomations:
Chip CP2012 only supports speed of 1M baudrate. It can't work on RTL8720x uart download flash mode speed 1500000.

# Known issues
1) First time upload will be failure due to amebad_image_tool.exe(no source) do something and let processor back to normal mode.
   It only happend and just onece in case when usb-serial just plug-in.

#
 Author:Joe Hsieh
 Email:jojoling@gmail.com
