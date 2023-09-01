`zFused Net` 外包端安装与更新

## 客户端地址

#### zfused_net 0.0.4.8：[`下载地址`](https://pan.baidu.com/s/18T6wlriFvCMYRNuUqCQEQA?pwd=vd26)
<!-- #### zfused_net 0.0.4.3：[`下载地址`](https://pan.baidu.com/s/1utrclixzk3QMV-WZLNyt6A?pwd=tjbg) -->


## 客户端安装
  
###### **1. 自行下载软件`安装包`**
+ 安装包由云盘下载，需要联网：[`点我跳转下载`](https://pan.baidu.com/s/18T6wlriFvCMYRNuUqCQEQA?pwd=vd26)
+ 将客户端文件夹`zfused_net`解压到任意本地路径  
 ![](sources/image/install/net_install.png ':size=600')


  ###### **2. 甲方提供针对该供应商的`配置文件`**
 ![](sources/image/install/zfusedlic.png ':size=550')



## 客户端启动
关乎于项目保密与信息独立，软件使用需要绑定以公司为单位的配置文件`.zfusedlic`

1. 双击`zFusedNet.exe`执行应用程序打开界面
2. 将配置文件拖到界面中间  
    ![](sources/image/install/net_lic.png ':size=600')
3. 点击登陆
#### **注意**：  
+ 首次登录需拖配置文件，当界面内已显示配置文件后不用再进行这步操作，配置文件有更新时，也需要重新拖一次  
+ 与多个甲方有同zf平台的合作时，可以通过切换配置文件来进入不同甲方的环境  
    ![](sources/image/install/switch_lic.png ':size=250')


## 客户端更新
如果云端有客户端版本更新，该更新消息会同步到各供应商方，为确保软件功能内容一致务必更新后再使用，打开应用程序之后顶端会显示有最新版需要下载更新，点击`下载更新`会开始分析版本文件并更新，完成后点击`重新启动`，重新登录即完成更新

![](sources/image/install/net_refresh.png ':size=800')
![](sources/image/install/net_refresh_ing.png ':size=800')
![](sources/image/install/net_refresh_ed.png ':size=800')

## 插件包更新
登录软件之后，需要保证插件包**存在**且都为**最新版本**，否则软件将无法正常启动

1. 在当前所处项目正确的前提下，切换到 `插件管理` 菜单栏，这里显示的是该项目所有依赖插件包的信息，包括名称、版本及安装地址  
   **(插件包的安装根路径由配置文件决定，默认设置存放在P盘路径：`P:/zfused/packages`下，P盘不存在将无法正常更新下载安装包，此路径不强制要求，如需修改可以自行[修改配置文件](#配置文件修改))**
2. 首次安装点击 `全部更新下载` 会统一安装所有插件包的最新版本，后续更新点击 `检测更新` ，可以检查是否存在新版本，如果显示 `需要更新` 点击右面下载按钮可以下载该插件包的最新版本

![](sources/image/install/net_packages.png ':size=800')


## 配置文件修改
配置文件中包含插件包安装根路径，默认安装路径为 `P:/zfused/packages`，路径可以根据需要自行修改，考虑到公司内部多台机器资源共享的问题，如需修改建议目标路径为公司内部网络共享路径

1. 将配置文件用记事本打开
2. 如图所示位置，可以修改变量路径来自定义zfused依赖插件包安装的位置
3. 修改路径后重新保存配置文件

![](sources/image/install/net_lic_change.png ':size=800')

>  + 配置文件中包含许可信息 key.lic 如果许可到期后将无法访问，需向甲方寻求最新配置文件  
>  + 插件包安装路径需要开启读取修改权限，用于获取和更新插件

## DCC软件启动
1. 登录软件之后切换到当前制作项目
2. 在`软件管理`菜单栏中可以看到各dcc软件信息
   + 针对MAYA软件，目前支持两种安装路径：
    Autodesk默认安装路径 / 区分小版本路径（C:\Program Files\Autodesk\Maya-202x\Maya202x.x\bin）
3. 确保当前插件包皆为最新版本
4. 点击对应dcc软件的按钮即可启动对应软件

![](sources/image/install/net_dcc.png ':size=800')

## MAYA启动界面
打开MAYA后在菜单上看到 `zFused_outsource` 说明已成功启动zfused环境，点击 `zFused_outsource` ，里面包括了公司信息与各环节相关插件，点击右侧的项目名称可以修改当前项目

![](sources/image/install/net_maya.png ':size=950')

## 任务管理
显示为本供应商分配的任务信息，可以下载任务相关联的文件

![](sources/image/install/net_task_manage.png ':size=800')

## 文件管理
显示为本供应商分配的任务信息相关联的文件，可以校检更新版本文件

![](sources/image/install/net_file_manage.png ':size=800')

## 文件上传回收
文件制作完成后，上传到云上供甲方获取文件和打包文件，这里以资产的模型-预览任务为例说明步骤：

1. 打开 `zFused outsource` - `utility` - `任务管理` 
2. 筛选实体类型，以资产为例，找到资产环节
3. 筛选实体任务环节，以模型预览任务为例，勾选 模型-预览
4. 在资产列表中找到对应的资产任务，支持关键字中英文搜索
5. 在对应资产任务上右键 `任务文件上传`，在弹出的窗口中填写描述信息，说明版本提交修改的内容
6. 开始上传之后，首先进入检查程序
7. 检查如果没有通过，会弹出检查信息，需要将检查问题都排查清除之后才可以继续上传，点击`重新上传`
8. 上传成功后会弹窗显示路径地址，表示已经成功同步到甲方公司  
9. 弹窗的地址可以复制路径到本地查看，压缩包内是打包整理好的任务文件(后续将自动化云端传输处理，目前功能还在测试完善中)

![](sources/image/install/recycle.png ':size=900')
![](sources/image/install/recycle.png ':size=900')
![](sources/image/install/publish_fst.png ':size=900')
![](sources/image/install/publish_check.png ':size=900')
![](sources/image/install/publish_ed.png ':size=900')
![](sources/image/install/zip.png ':size=800')
