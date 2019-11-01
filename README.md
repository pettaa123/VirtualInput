# VirtualInput (<a href='https://qtcentre.org/threads/49181-virtual-keyboard-in-QT-Application'>qtcentre.org</a>)
virtual keyboard for QT Applications **LINUX**

This is a fork for linux, removing some linux specific errors and depcreated warnings by the windows remote. Make sure you have: 
* sudo apt-get install qtbase5-private-dev  if qpa/qplatforminputcontext.h etc. is missing
* sudo apt-get install qttools5-dev if QtUiPlugin/QDesignerExportWidget is missing

numpad layout:
* <img src=numpad.png />
keyboard layout:
* <img src=keyboard.png />

Virtual Keyboard for touch-screen devices written in C/C++ Qt, compatible with 5.x
The keyboard only works with QLineEdit.

the widget is written by (<a href='https://qtcentre.org/members/36463-StrikeByte'>StrikeByte</a>) 
I added a simple example to show the usage.

How to use:
* Build the library
* copy the libVirtualInput.so to platforminputcontexts in your application or to plugins/platforminputcontexts in your QtDir (/usr/lib/x86_64-linux-gnu/qt5/plugins/platforminputcontexts/ in my case)
* Add a custom property named "keyboard" (without the quotes) of the type bool to the QLineEdit and set it to enabled
* For text you can set the maxLength property
* For values you can add a QIntValidator to the QLineEdit

**WINDOWS**

* #include QValidator in numpad.h when using minGW compiler
* copy VirtualInput.dll next to the .exe into a selfcreated folder "platforminputcontexts"


