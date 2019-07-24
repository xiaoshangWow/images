# Flutter在Windows上的安装文档

## 安装过程若遇到问题均可参考[Flutter中文网](https://flutterchina.club/get-started/install/)！！！

## Java开发工具包的下载与安装
### 下载Java开发工具包
[Java开发工具包下载地址](https://link.juejin.im/?target=https%3A%2F%2Fwww.oracle.com%2Ftechnetwork%2Fjava%2Fjavase%2Fdownloads%2Fjdk8-downloads-2133151.html)，这个地址会随着Java升级而有所变化，如果已经改变了，请百度一下搜索java下载或者直接到[Java官网下载](https://link.juejin.im/?target=https%3A%2F%2Fwww.java.com%2Fzh_CN%2F)。

<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG71.jpeg">

首先点击红框中的圆圈，然后根据读者的系统是64位还是32位来选择版本，此处建议安装**JDK8**

### 安装Java开发工具包
首先，下载完成后双击运行进行安装，直接点击下一步下一步就可以了，安装路径读者随意；
最后，安装完成后到终端（cmd命令行）中输入java，能出现下图中的结果，说明安装成功。
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG70.jpeg">

## 使用镜像
由于在国内访问Flutter有时可能会受到限制，Flutter官方为中国开发者搭建了临时镜像，大家可以将如下环境变量加入到用户环境变量中：
```
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```
添加环境变量操作步骤如下:
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG47.jpeg">
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG48.jpeg">
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG49.jpeg">

注意： 此镜像为临时镜像，并不能保证一直可用，读者可以参考详情请参考 [Using Flutter in China](https://github.com/flutter/flutter/wiki/Using-Flutter-in-China) 以获得有关镜像服务器的最新动态。

## 系统要求
要安装并运行Flutter，您的开发环境必须满足以下最低要求:
>- **操作系统:** Windows 7 或更高版本 (64-bit)
>- **磁盘空间:** 400 MB (不包括Android Studio的磁盘空间).
>- **工具:**  Flutter 依赖下面这些命令行工具.
>    - [Git for Windows](https://git-scm.com/download/win) (Git命令行工具)  
如果已安装Git for Windows，请确保命令提示符或PowerShell中运行 git 命令，不然在后面运行flutter doctor时将出现Unable to find git in your PATH错误, 此时需要手动添加C:\Program Files\Git\bin至Path系统环境变量中。

## 获取Flutter SDK
### 方案一

1. 去flutter官网下载其最新可用的安装包，**建议下载v1.6.2版本，团队版本进行统一**，[点击下载](https://flutter.io/sdk-archive/#windows)。

2. 将安装包zip解压到你想安装Flutter SDK的路径（如：C:\src；注意，**不要**将flutter安装到需要一些高权限的路径如C:\Program Files\）。  

<!-- 3.在Flutter安装目录的flutter文件下找到flutter_console.bat，双击运行并启动**flutter命令行**，接下来，你就可以在Flutter命令行运行flutter命令了。   -->

<!-- 注意： 由于一些flutter命令需要联网获取数据，如果您是在国内访问，由于众所周知的原因，直接访问很可能不会成功。 上面的PUB_HOSTED_URL和FLUTTER_STORAGE_BASE_URL是google为国内开发者搭建的临时镜像。详情请参考 [Using Flutter in China](https://github.com/flutter/flutter/wiki/Using-Flutter-in-China) -->

要将Flutter永久添加到路径中，请参阅[更新路径](https://flutterchina.club/setup-windows/#%E6%9B%B4%E6%96%B0%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)。

要更新现有版本的Flutter，请参阅[升级Flutter](https://flutterchina.club/upgrading/)。

### 方案二

通过**git**命令下载**flutter sdk**:

1. 确保已安装和配置[Git命令行工具](https://git-scm.com/download/win)

2. 创建安装Flutter SDK的文件夹（如：C:\src\), 通过终端cd到该目录

3. 执行git命令: git clone -b master https://github.com/flutter/flutter.git

4. 执行git命令: git checkout v1.6.2 **切换到v1.6.2版本，团队版本进行统一**
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG67.jpeg">

5. 新建系统环境变量 Path： flutter\bin的全路径作为它的值,重启Windows以应用此更改
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG51.jpeg">

## 运行flutter doctor

打开一个新的命令提示符或PowerShell窗口并运行以下命令以查看是否需要安装任何依赖项来完成安装：

> flutter doctor

<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG53.jpeg">

以上为笔者的命令输出信息，读者在自己的电脑上运行flutter doctor看到的命令输出信息当中的[X]肯定会比笔者的多一些，因为读者还没有安装Android Studio（简称AS），那么接下来讲解一下如何下载安装AS。若是已经读者安装AS，可直接跳至**安装Android证书**

## 编辑器设置
使用 flutter 命令行工具，您可以使用任何编辑器来开发Flutter应用程序。输入flutter help在提示符下查看可用的工具。

我们建议使用我们的插件来获得[丰富的IDE体验](https://flutterchina.club/using-ide/)，支持编辑，运行和调试Flutter应用程序。请参阅[编辑器设置](https://flutterchina.club/get-started/editor/)了解详细步骤

## Android设置
### Android Studio下载与安装(**需v3.0及以上版本**)
理论上可以使用任何文本编辑器与命令行工具来构建Flutter应用程序。 不过，Flutter官方建议使用Android Studio和VS Code之一的编辑器以获得更好的开发体验。Flutter官方分别提供了这两款编辑器的Flutter插件，通过编辑器集成Flutter插件的方式，可获得代码补全、语法高亮、widget编辑辅助、运行和调试支持等功能，可以帮助我们极大的提高开发效率。

### 下载AS
AS安装包直接到官网上进行下载即可，[官网地址](https://link.juejin.im/?target=https%3A%2F%2Fdeveloper.android.google.cn%2Fstudio)，进入官网后点击“Android Studio”菜单栏，然后看到如下界面，点击“DOWNLOAD ANDROID STUDIO”按钮进行下载。
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/1.jpeg">

点击“我已阅读并同意上述条款及条件”，进行打勾；然后点击“下载ANDROID STUDIO FOR WINDOWS”按钮，即可下载：
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/2.jpeg">

### 安装AS
AS安装包下载完成后，双击进行安装，安装过程差不多就是点击下一步下一步，读者如果真的不会安装，请参考[AS下载安装与配置教程](https://link.juejin.im/?target=https%3A%2F%2Fwww.cnblogs.com%2Fxiadewang%2Fp%2F7820377.html)。

AS安装完成后打开CMD命令行再运行flutter doctor命令来验证是否安装成功。

### 安装Android证书
安装好AS后，再次打开CMD命令行，输入flutter doctor命令，这时候的[X]会明显减少，但是读者有可能还会遇到1~2个[X]，其中有一个就是提示没有安装Android证书，安装证书需要在CMD命令行中执行以下的命令：

flutter doctor --android-licenses

然后会提示读者选Y/N，不要犹豫，一律选择Y，就可以把证书安装成功。

### AS上安装Flutter插件
打开AS客户端，点击File > Settings > Plugins > Browse Repositories > 输入Flutter > Install
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG54.jpeg">

安装完成后，读者需要重新启动一下AS客户端。

### AS创建Flutter项目
1. 点击File > New Flutter Project
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG62.jpeg">

2. 点击Flutter application作为project类型，然后点击Next
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG55.jpeg">

3. 输入项目名称（如 myapp），然后点击Next
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG56.jpeg">

4. 点击Finish
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG57.jpeg">

5. 等待Android Studio安装SDK并创建项目

### AS运行Flutter项目
要准备在Android设备上运行并测试您的Flutter应用，您需要安装Android 4.1（API level 16）或更高版本的Android设备.

1. 开启AS的代理，这里需要科学上网，可以选择不同的代理服务
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG64.jpeg">

2. 定位到AS工具栏

3. 在target selector中，选择一个运行该应用的Android设备。如果没有列出可用，请选择Tools > Android > AVD Manager并创建一个 **建议选择图示的机型和镜像**
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG58.jpeg">
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG59.jpeg">
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG60.jpeg">
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG61.jpeg">

4. 启动项目前再次在终端运行指令 flutter doctor 检测是否通过，只需配置好一个编辑器即可
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG63.jpeg">

5. 在工具栏中点击Run或Debug图标
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG66.jpeg">

6. 由于第一次没有开启代理运行报错截图如下, [解决方案点此查看](https://github.com/alibaba/freeline/issues/434), 若是没有遇到可跳过
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG516.jpeg">

7. 在读者的真机设备或模拟器上将会看到启动的应用程序，至此Flutter环境搭建成功
<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG65.jpeg">

8. 每次新建一个flutter项目，系统会自动创建如下示例代码，若想查看更多示例代码请参考[官网教程](https://flutterchina.club/get-started/learn-more/)

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        // This is the theme of your application.
        //
        // Try running your application with "flutter run". You'll see the
        // application has a blue toolbar. Then, without quitting the app, try
        // changing the primarySwatch below to Colors.green and then invoke
        // "hot reload" (press "r" in the console where you ran "flutter run",
        // or simply save your changes to "hot reload" in a Flutter IDE).
        // Notice that the counter didn't reset back to zero; the application
        // is not restarted.
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  MyHomePage({Key key, this.title}) : super(key: key);

  // This widget is the home page of your application. It is stateful, meaning
  // that it has a State object (defined below) that contains fields that affect
  // how it looks.

  // This class is the configuration for the state. It holds the values (in this
  // case the title) provided by the parent (in this case the App widget) and
  // used by the build method of the State. Fields in a Widget subclass are
  // always marked "final".

  final String title;

  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      // This call to setState tells the Flutter framework that something has
      // changed in this State, which causes it to rerun the build method below
      // so that the display can reflect the updated values. If we changed
      // _counter without calling setState(), then the build method would not be
      // called again, and so nothing would appear to happen.
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    // This method is rerun every time setState is called, for instance as done
    // by the _incrementCounter method above.
    //
    // The Flutter framework has been optimized to make rerunning build methods
    // fast, so that you can just rebuild anything that needs updating rather
    // than having to individually change instances of widgets.
    return Scaffold(
      appBar: AppBar(
        // Here we take the value from the MyHomePage object that was created by
        // the App.build method, and use it to set our appbar title.
        title: Text(widget.title),
      ),
      body: Center(
        // Center is a layout widget. It takes a single child and positions it
        // in the middle of the parent.
        child: Column(
          // Column is also a layout widget. It takes a list of children and
          // arranges them vertically. By default, it sizes itself to fit its
          // children horizontally, and tries to be as tall as its parent.
          //
          // Invoke "debug painting" (press "p" in the console, choose the
          // "Toggle Debug Paint" action from the Flutter Inspector in Android
          // Studio, or the "Toggle Debug Paint" command in Visual Studio Code)
          // to see the wireframe for each widget.
          //
          // Column has various properties to control how it sizes itself and
          // how it positions its children. Here we use mainAxisAlignment to
          // center the children vertically; the main axis here is the vertical
          // axis because Columns are vertical (the cross axis would be
          // horizontal).
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have pushed the button this many times:',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.display1,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
}
```

## [seed.mobile](http://116.62.61.34:8888/flutter/seed.mobile)项目

<img src="https://raw.githubusercontent.com/xiaoshangWow/images/master/flutter/WechatIMG69.jpeg">

### App目录结构
>- |--lib
>    - |-- base (待确定，可能会去除)
>    - |-- blocs (bloc相关)
>    - |-- common (常用类，例如常量Constant)
>    - |-- data (网络数据层)
>    - |-- db (数据库)
>    - |-- demos (flutter demos)
>    - |-- event (事件类)
>    - |-- models (实体类)
>    - |-- res (资源文件，string，colors，dimens，styles)
>    - |-- pages (界面相关page，dialog，widgets)
>    - |-- utils (工具类)

### data网络数据层
>- |--data
>    - |-- api (url字段)
>    - |-- protocol (请求与返回实体类)
>    - |-- repository (接口请求&解析)

### 资源文件 res
>- |--res
>    - |-- colors.dart
>    - |-- dimens.dart
>    - |-- strings.dart
>    - |-- styles.dart