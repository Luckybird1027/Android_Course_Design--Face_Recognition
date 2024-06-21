# 人脸识别签到app

该项目fork自[xiaoyou-project/android-course-design: 安卓课程设计代码-人脸识别签到 (github.com)](https://github.com/xiaoyou-project/android-course-design)，并在此基础上进行了一定的修改。

## 这是什么？

本项目(**人脸识别签到app**)是基于虹软(ArcSoft)的人脸识别SDK进行开发的人脸识别签到安卓应用，让你可以在安卓手机上**离线**、**快速**、**准确**的进行校园人脸识别，准确识别注册过的人脸信息，**支持多人**同时签到，快速识别多个人脸，在不同光照条件下进行准确的人脸识别，并自动保存和统计签到记录。

<img src=".\image\a.png" style="zoom:25%;" /><img src=".\image\c.png" style="zoom:25%;" /><img src=".\image\b.png" style="zoom:25%;" />







## 功能介绍

### 签到日历功能

<img src="./image/2.png" style="zoom:60%;" />

### 人脸录入

<img src="./image/3.png" style="zoom:60%;" />

### 签到功能

<img src="./image/4.png" style="zoom:60%;" />

### 签到详情

<img src="./image/2.jpg" style="zoom:30%;" />

### 签到数据查询

<img src="./image/3.jpg" style="zoom:30%;" />

### 图表展示

<img src="./image/4.jpg" style="zoom:30%;" />





## 如何使用

由于app的人脸识别功能需要通过虹软认证激活，故不提供apk安装包，请自行获取源码后调整SDK相关设置后自行编译打包运行。



### 限制条件

本项目使用虹软官方提供的SDK来实现离线人脸识别功能，由于官方SDK早在2020年对该项目停止维护，将开发重心转移至其他项目，故本项目**仅支持Android10及以下**安卓设备正常运行，且**仅支持arm64-v8a和armeabi-v7a**两种abi。



### 获取源码

git命令行获取

```
https://github.com/Luckybird1027/Android_Course_Design--Face_Recognition.git
```



### 开发环境配置

项目配置概览

> IDE：Android Studio
>
> Android SDK：29
>
> Gradle版本：6.5
>
> JDK：1.8（Java8）

Android studio下载链接：[下载 Android Studio 和应用工具 - Android 开发者  | Android Developers (google.cn)](https://developer.android.google.cn/studio?hl=zh-cn)

点击Android Studio页面左上角的**File**选项卡，点击**Project Structure**，可以进入Project Structure页面。

<img src=".\image\p1.png"/>

Project Structure页面的**Project**选项处，可以选择项目所使用的gradle版本。

<img src=".\image\p2.png"/>

Project Structure页面的**Modules**选项处，可以选择项目所使用的**Android SDK版本**。

<img src=".\image\p3.png"/>

在主页面**双击shift**可以调出项目级搜索界面，输入**jdk**，可以找到**Change Gradle JDK Location**，点击后可进入gradle设置界面。

<img src=".\image\p4.png"/>

在gradle配置界面中，可以选择项目的gradle所使用的**JDK**。

JDK下载链接：[Java Downloads | Oracle](https://www.oracle.com/java/technologies/downloads/)

<img src=".\image\p5.png"/>

所有选项设置完毕后，可点击页面右上角的**Sync Project With Gradle Files**进行项目构建。首次构建需要下载大量依赖库以保证项目运行，可能需要花费大量时间。构建完成后，便可以在虚拟机或其他安卓设备上运行或调试app了。

<img src=".\image\p6.png"/>



### 配置项目

前往[开发者中心 (arcsoft.com.cn)](https://ai.arcsoft.com.cn/ucenter/resource/build/index.html#/index)注册开发者账户并申请SDK使用，获取**APP_ID**与**SDK_KEY**，并下载SDK。

将app/src/main/java/com/xiaoyou/face/common/Constants.java中的**APP_ID**与**SDK_KEY**修改为从虹软官网处获得的**APP_ID**与**SDK_KEY**，并将从虹软下载的SDK包中的相应部分替换到项目中的相应部分（请查阅虹软官方的文档进行操作，本readme不赘述）。

完成后编译打包安装即可。



### 应用运行

首次打开app时需要激活人脸识别引擎，如遇人脸识别功能无法正常使用，你可以尝试点击主页右下角的logo按钮进行激活引擎，按照提示进行。
