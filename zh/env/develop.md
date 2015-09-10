## 开发环境

### Android开发环境准备

开发环境准备很简单，记住三点即可：
1. JDK（>= 1.7）
2. Android SDK
3. IDE

其中Android SDK是Android开发的工具包，里面包括各个版本的工具、第三方库等，Android SDK依赖JDK7+。

本文的IDE将以Android Studio为主，Eclipse需要插件ADT，而GOOGLE已经宣布不再维护ADT版本的更新，全面转为Android Studio，所以本文将以Android Studio为IDE进行环境的部署。

>目前Android Studio只支持64位系统，所以相应的JDK也要64位。

### JDK环境部署
Android推荐JDK版本为7+，从[JDK下载地址](www.oracle.com/technetwork/java/javase/ downloads/index.html)下载JDK并进行安装。

**Win 平台**

1. 下载exe文件并安装（注意看自身平台32位还是64位）
2. 设置环境变量


**Linux 平台**

1. 下载gz文件并解压到安装目录（建议/usr/local/jvm目录）
2. 设置环变量

也可以安装openjdk，不过推荐用上面的安装方式：
1. 命令行安装（ubuntu为例）：` sudo apt-get install openjdk-7-jdk


**Mac 平台**
1. 下载dmg文件并安装
2. 设置环境变量