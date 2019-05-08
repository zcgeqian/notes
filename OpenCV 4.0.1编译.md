### OpenCV 4.0.1编译（windows）

____

编译动机：OpenCV官网下载的OpenCV windows版编译程序是不包含QT环境的编译，不能使用QT相关代码，因此重新编译，编译器使用MSVC。

____

##### 软件环境

* win10 专业版 1809

* OpenCV 4.0.1

* CMake GUI 3.13.3

* QT 5.12.1 MSVC版

* VS 2017

  OpenCV和QT加入系统环境变量

____

##### 编译步骤

CMake 源码位置：`D:/opencv4/sources`，目标位置：`D:/opencv4/qt_build`

选择`Configure`，等待完成。

编译后生成一个world文件库，而不是每个模块分别生成库，`BUILD_opencv_world`打钩，带QT编译，搜索`WITH_QT`，打钩，重新选择`Configure`，此时会寻找QT相关目录，注意查看更新值为红色标记，并查看汇总信息里，GUI字段，QT 配置是否为YES，如果报错，OpenGL选项根据需要选择，在选项里手动指定，直至configure后无标红的配置。

完成后`Generate`，VS打开项目，选择`install` 生成，编译后的文件生成在项目目录的`install`文件夹中。

