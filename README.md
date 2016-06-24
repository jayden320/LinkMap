# LinkMap解析工具：检查每个类占用大小

## 概述

一个大型的项目，只是代码段就有可能超过100M，算上armv7和arm64架构，就会超过200M。
这时候检查到底是哪个类、哪个第三方库占用了太多空间，就显得尤为重要。

这个工具是专为用来分析项目的LinkMap文件，得出每个类或者库所占用的空间大小（代码段+数据段），方便开发者快速定位需要优化的类或静态库。


## 使用说明

1、打开LinkMap.xcodeproj，并运行，就可以看到工具界面
<img src="https://github.com/huanxsd/LinkMap/blob/master/ScreenShot1.png" alt="ScreenShot1" title="ScreenShot1">

2、点击“选择文件”按钮，选择LinkMap文件（如何生成LinkMap详见下方的：如何获得LinkMap文件）

3、点击“开始”按钮，就可以看到每个类/静态库所占用的空间大小
<img src="https://github.com/huanxsd/LinkMap/blob/master/ScreenShot2.png" alt="ScreenShot2" title="ScreenShot2">

4、点击“输出文件”，可以将结果输出到文本文档中


## 如何获得LinkMap文件

1.在XCode中开启编译选项Write Link Map File \n\
XCode -> Project -> Build Settings -> 把Write Link Map File选项设为yes，并指定好linkMap的存储位置

2.工程编译完成后，在编译目录里找到Link Map文件（txt类型)
默认的文件地址：~/Library/Developer/Xcode/DerivedData/XXX-xxxxxxxxxxxxx/Build/Intermediates/XXX.build/Debug-iphoneos/XXX.build/ \n\


## 联系我

如有问题或建议欢迎通过邮件联系我
67111677@qq.com

## 最后

如果喜欢，请顺手我一个star吧~  ：）