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



