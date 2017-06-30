

出现错误：安装 openjdk-7-jdk 出现错误：没有可安装候选 

执行命令：
```
sudo add-apt-repository ppa:openjdk-r/ppa  
sudo apt-get update   
sudo apt-get install openjdk-7-jdk 
```

下载源码
https://android.googlesource.com/

platform/build
platform/build/blueprint
platform/build/kati
platform/build/soong
platform/development
platform/frameworks/base


将 `idegen.jar` 放入 `out/host/linux-x86/framework/` 目录下

初始化编译环境

```
. build/envsetup.sh
```

生成 `android.iml` 和 `android.ipr`
```
development/tools/idegen/idegen.sh
```


导入前配置

```
<!-- excludeFolder: 不导入某些模块 -->
<!-- 自定义配置：只导入了framworks和packages模块 -->
<excludeFolder url="file://$MODULE_DIR$/abi" />
<excludeFolder url="file://$MODULE_DIR$/art" />
<excludeFolder url="file://$MODULE_DIR$/bionic" />
<excludeFolder url="file://$MODULE_DIR$/bootable" />
<excludeFolder url="file://$MODULE_DIR$/build" />
<excludeFolder url="file://$MODULE_DIR$/cts" />
<excludeFolder url="file://$MODULE_DIR$/dalvik" />
<excludeFolder url="file://$MODULE_DIR$/developers" />
<excludeFolder url="file://$MODULE_DIR$/development" />
<excludeFolder url="file://$MODULE_DIR$/device" />
<excludeFolder url="file://$MODULE_DIR$/docs" />
<excludeFolder url="file://$MODULE_DIR$/external" />
<excludeFolder url="file://$MODULE_DIR$/hardware" />
<excludeFolder url="file://$MODULE_DIR$/libcore" />
<excludeFolder url="file://$MODULE_DIR$/libnativehelper" />
<excludeFolder url="file://$MODULE_DIR$/ndk" />
<excludeFolder url="file://$MODULE_DIR$/out" />
<excludeFolder url="file://$MODULE_DIR$/pdk" />
<excludeFolder url="file://$MODULE_DIR$/prebuilt" />
<excludeFolder url="file://$MODULE_DIR$/prebuilts" />
<excludeFolder url="file://$MODULE_DIR$/sdk" />
<excludeFolder url="file://$MODULE_DIR$/system" />
<excludeFolder url="file://$MODULE_DIR$/tools" />
```


导入源码到 `Android Studio`

打开 `Android Studio`，点击 `File > Open`，选择刚刚生成的 `android.ipr` 打开