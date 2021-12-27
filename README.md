# jctpapi-msvc

### 在Windows环境下使用VisualStudio(MSVC)编译Java调用上期技术CTP-API的JNI（C++）源码

#### 简介

本仓库提供 [redtorch](https://github.com/sun0x00/redtorch) 项目的rt-gateway-ctp模块的具体代码生成方法和跨平台运行方案细节。

#### 使用方法
+ 克隆本仓库
+ 使用Visual Studio 2022 直接打开解决方案


#### 提示
+ 本仓库中提供的JNI(C++)源码来自仓库 [swig-java-ctp](https://github.com/sun0x00/swig-java-ctp)
+ 本仓库中提供的CTP链接库lib文件来自[上期技术官网](http://www.sfit.com.cn)提供的各对应版本的SDK压缩包
+ 本项目使用的iconv.lib和iconv.dll来自仓库 [libiconv-win-build](https://github.com/sun0x00/libiconv-win-build)
+ Linux环境下的编译方法请访问仓库 [jctpapi-linux](https://github.com/sun0x00/jctpapi-linux)
+ 本仓库中提供的JNI(C++)源码已经解决CTP结算单乱码问题，具体实现细节请访问仓库 [swig-java-ctp](https://github.com/sun0x00/swig-java-ctp)
+ Windows环境下编译的Java-CTP链接库在使用时需要加载iconv.dll
+ 编译后的Java-CTP链接库使用方法请参阅[redtorch](https://github.com/sun0x00/redtorch) 项目的rt-gateway-ctp模块


#### 如何在Visual Studio中添加新版本的CTP项目？

+ 新建dll项目

+ 复制JDK目录中的jni.h jni_md.h 添加到项目目录

+ 参考现有项目复制资源项， iconv.lib， iconv.h

+ 复制加入上期技术提供的对应版本的lib文件

+ 搜索修改CPP文件，将jni.h的引入方式由```include <jni.h>``` 改为 ```include "jni.h"```

+ 项目属性->配置属性->C/C++->代码生成->运行库 选择：多线程（/MT）

+ 项目属性->配置属性->C/C++->预编译头->预编译头 改为 不使用编译头

+ 项目属性->配置管理器（右上角）->全改为Release x64（默认64位环境）
