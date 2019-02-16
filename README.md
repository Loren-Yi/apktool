
#apk反编译工具

##APK反编译回编译<br>
（需要安装java环境:例如jdk-8u191-windows-x64）
1.反编译APK，生成APK反编译后的文件夹<br>
命令：
`java -jar apktool.jar d -f xxx.apk`
2.回编译，生成的新APK在文件夹的dist目录<br>
命令：
`java -jar apktool.jar b -f file`



PS：以上是常规APK反编译，回编译成功用户自行去签名即可。  
##以下是系统APK反编译，需要添加框架<br>
1.首先要加载/system/framework下的所有apk框架，再进行对APK反编译<br>
命令：
`apktool if framework.apk`   
2.反编译回编译如上<br>
3.回编译后需要把APK反编译生成文件夹中的original目录下的原始签名和AndroidManifest.xml配置文件替换回新生成的apk中即可，无需再次签名。<br>

![fuli](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550294259405&di=bdd7b3ff88e7e312e772ef45bb88dbc9&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01440d569e407632f875520f872519.jpg)  

