# SimulationLocation

## Install XCode

macOS 版本对应的 Xcode 版本 [macos-xcode-version](https://uovol.com/macos-xcode-version)

使用 macOS 解压 xip 文件

```bash
$ xip -x Xcode_13.xip
```

在解压出来的 Xcode.app 中删除不必要的平台

```bash
$ find . -name '*.platform'|xargs du -h -d
$ find . -name '*.platform'|grep -v chain|grep -v MacOSX|grep -v DriverKit|xargs rm -r
$ find . -name 'external'|xargs rm -rf
```


## IPhone 地理位置修改

1. 获取经纬度
https://api.map.baidu.com/lbsapi/getpoint/index.html

2. XCode 打开项目， 修改 Location.gpx

    - lat
    - lon

3. 连接并在xcode中选择设备

4. Product -> Scheme -> Edit Scheme -> Run-Option-> Core Location -> 选择 Location 

5. Build and then run the current Scheme
