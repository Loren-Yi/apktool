# apktool
APK反编译工具

一、APK反编译 

（需要安装java环境:例如jdk-8u191-windows-x64）

1.反编译APK，生成APK反编译后的文件夹

命令：java -jar apktool.jar d -f APK文件

2.回编译，生成的新APK在文件夹的dist目录

命令：java -jar apktool.jar b -f 文件夹名称

以上是常规APK反编译，回编译成功提示用户自行去签名即可。

以下是系统APK反编译，需要添加框架说明：

首先要加载/system/framework下的所有apk框架，再进行对APK反编译

命令：apktool if 框架APK

反编译回编译如上，回编译后需要把APK反编译生成文件夹中的original目录下的原始签名和AndroidManifest.xml配置文件替换回新生成的apk中即可，无需再次签名。
