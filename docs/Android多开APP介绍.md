---
JoplinID: 1NNYuOuCxsXH1EVnYm0A8H
NostrID: 
来源: 
tags:
  - tagaa
  - tagbb
  - android
  - mkdocs
创建: 2024-03-24 15:20
更新: 2024-03-24 17:47
---
Android多开APP介绍

### TODO，还需要考察，
* 32位APP的支持
* 不同版Android的支持
* 是否开源

以下测试是Android12，MIUI13的试用总结。

### mochicloner
包名，com.jy.x.separation.manager
版本，2.0.7
官方主页，

优点，
* 无限多开
* 占空间小
* 启动速度与系统安卓一样

缺点，
* 只能与系统原版本APP一样


### multiapp
包名，com.waxmoon.ma.gp
版本，1.3.13
官方主页，

优点，
* 无限多开
* 可以安卓不同版本，但是很多APP安卓不了
* 可以安装microg，并且运行正常

缺点，
* 占空间特别大
* 启动似乎慢一点

### 系统自带双开

缺点，
* 启动慢
* 只能开一个分身
* 只能与系统原APP一致
* 依赖OEM组件，像MIUI依赖com.miui.securitycore，这个平时是冻结的包，每次设置都要先开启
* 不开源



总结，有了前面两个APP，系统自带的就找不到再继续使用的理由了。





更新：2024-03-24 17:47 字数：495/959
