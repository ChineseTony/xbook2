# 应用程序开发流程
更新日期：2020/6/26

## 流程简介
在**xbook2**中，应用程序即用户态进程，既可以是普通的应用，也可以是服务进程。普通应用一般需要在**shell**程序中启动。而服务进程则根据服务类型来确定。

### 1.搭建应用程序项目
在**user**目录下面复制**template**这个模板，可以方便开发。复制后，修改成自己应用程序的名字。例如：**hello**。 
修改打开makefile，修改BIN对应的名字，**BIN = $(DIR_ROM)/bin/hello**。

### 2.编译流程
打开**hello/cmd.bat**或者是在**hello**中打开终端都可以，然后输入**make**，就可以编译程序了，编译后会把可执行文件写入到**develop/rom**目录，可以在os中查看到。输入**make clean**清除编译过程中产生的.o文件和可执行文件。

### 3.启动流程
在**xbook2**目录下面打开终端，输入**make run**即可在**qemu**虚拟机中启动系统内核。启动后会默认打开一个终端，输入程序名即可运行。