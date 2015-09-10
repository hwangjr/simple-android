## 开发环境

### Android开发环境准备

开发环境准备很简单，记住三点即可：
1. JDK（>= 1.7）
2. Android SDK
3. IDE
4. 可选NDK安装

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

**设置环境变量**
必须配置变量（以Linux为例）：
``` java
export JAVA_HOME=path_to_jdk_dir
```
可选配置环境变量（以Linux为例）：
``` java
export PATH=$PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```
在类Uinux平台下，直接在文件（/etc/profile 或者 ~/.profile 或者 ~/.bashrc）中新增。

在WIN平台下，右键电脑 -> 属性 -> 高级系统设置 -> 高级 -> 环境变量。在系统变量新建JAVA_HOME和CLASS_PATH变量，查找系统变量中Path，在末尾新增`;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;`。

**Ubuntu高级配置**
如果是Ubuntu系统且需要在各个JDK版本之间切换，在安装之后（`/usr/local/jvm`），可以使用以下命令进行配置，在各个版本之间切换:
``` bash
sudo update-alternatives --config java
```

### SDK安装
如果使用Android Studio，可以单独下载Android Studio或者下载Android Studio的bundle，bundle里面包含了：
1. 当前最新的Android studio
2. android sdk
3. android build tool
4. android virtual device images

**单独安装sdk**
单独安装SDK：
1. 去[SDK下载](http://developer.android.com/sdk)页面，选择SDK进行下载
2. 配置环境

** 配置环境**
配置系统环境，以Linux为例，其他可参考JDK的环境配置来进行配置：
``` bash
export ANDROID_HOME=/usr/local/android-sdk-linux
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools

```


``` bash

export ANDROID_NDK=/usr/local/android-ndk-r10
export PATH=$PATH:$ANDROID_NDK

export GRADLE_HOME=/usr/local/gradle/latest
export PATH=$PATH:$GRADLE_HOME/bin
```