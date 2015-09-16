## 基本组件

每个应用程序都有一些关键组件，在Android中，基本组件包括：View、Activity、Fragment、Intent、ContentProvider、Service和AndroidManifest.xml文件。

### View
View是UI元素，构成界面的基本元素。View可以是一个按钮、输入框、文本等。视图也可以作为其他视图的容器，也就是多个视图可以放入一个布局的视图中，构成了看到的UI视图的层次结构。

### Activity
Activity代表活动窗体，可以理解为应用程序的一个屏幕。它通常包含一个或多个View，帮助用户完成某一操作：查看数据、创建或编辑数据等。大部分Android应用程序包含多个Activity。

### Fragment
Fragment是碎片的概念。在大屏幕上，一个Activity很难管理所有功能，此时可将屏幕分为多个碎片组合而成，分别进行管理。Fragment也可理解为子活动，一个Activity可包含多个Fragment，也可只包含一个。

### Intent

### ContentProvider

### Service

### AndroidManifest.xml