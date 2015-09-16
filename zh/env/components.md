## 基本组件

每个应用程序都有一些关键组件，在Android中，基本组件包括：View、Activity、Fragment、Intent、ContentProvider、Service和AndroidManifest.xml文件。

### View
View是UI元素，构成界面的基本元素。View可以是一个按钮、输入框、文本等。视图也可以作为其他视图的容器，也就是多个视图可以放入一个布局的视图中，构成了看到的UI视图的层次结构。

### Activity
Activity代表活动窗体，可以理解为应用程序的一个屏幕。它通常包含一个或多个View，帮助用户完成某一操作：查看数据、创建或编辑数据等。大部分Android应用程序包含多个Activity。

### Fragment
Fragment是碎片的概念。在大屏幕上，一个Activity很难管理所有功能，此时可将屏幕分为多个碎片组合而成，分别进行管理。Fragment也可理解为子活动，一个Activity可包含多个Fragment，也可只包含一个。

### Intent
Intent代表执行某个操作的意图。一般用Intent来执行：
1. 广播消息
2. 启动Service
3. 启动Activity
4. 启动网页或查看联系人
5. 拨出或接听电话
6. ETC

Intent并不总是由应用程序发起，系统也会使用他们来进行特定事件的通知，比如收到短信等。

Intent分为显式和隐式意图。比如打开URL，系统决定哪些组件可以满足此意图，你也可以直接指定某个组件来处理该意图。故Intent将操作和操作处理松散地耦合在一起。

### ContentProvider
ContentProvider是在Android上为应用程序定义的一个标准机制来进行数据的共享，隐藏了底层的存储、结构和实现。通过使用ContentProvider，可以方便的在应用程序之间进行数据共享，通过公开数据方式，允许应用程序使用其他应用程序数据。

### Service
Service即应用服务，可长时间运行的后台进程。Android服务分为Local服务和Remote服务。Local服务只能由本服务的应用程序进行访问。Remote服务则提供给设备上运行的其他应用程序远程访问。

比如获取天气情况的服务，如果本服务只能由天气预报的应用访问，则是本地服务，而如果其他应用程序也可通过此服务来获取当前天气情况，则本服务是远程服务。

### AndroidManifest.xml
Manifest文件是xml格式来组数据，定义了应用程序的内容和行为。一般里面定义了应用程序所需要的权限、Activity、Service、Receiver及其他功能。