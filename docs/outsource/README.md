`zFused Net` 外包端安装与更新

## 客户端安装
甲方提供软件安装包，安装包内包含zFusedNet`客户端文件`和为每个供应商单独提供的`配置文件`

![](sources/image/install/net_pack.png ':size=550')

将客户端文件夹`zfused_net`拷贝到任意本地路径

![](sources/image/install/net_install.png ':size=600')

## 客户端启动
关乎于项目保密与信息独立，软件使用需要绑定以公司为单位的配置文件`.zfusedlic`

1. 双击`zFusedNet.exe`执行应用程序打开界面
2. 将配置文件拖到界面中间（首次需要拖配置文件进来，界面内已显示配置文件后不用再进行这步操作）
3. 点击登陆

![](sources/image/install/net_lic.png ':size=600')

## 配置文件修改
配置文件中包含插件包安装总路径，默认安装路径为 `P:/zfused/packages`，路径可以根据需要自行修改，如需修改建议目标路径为公司内部网络共享路径

1. 将配置文件用记事本打开
2. 如图所示位置，可以修改变量路径来自定义zfused依赖插件包安装的位置
3. 修改路径后重新保存配置文件

![](sources/image/install/net_lic_change.png ':size=800')

> 配置文件中包含许可信息 key.lic 如果许可到期后将无法访问，需向甲方寻求最新配置文件
> 插件包安装路径需要开启读取修改权限，用于获取和更新插件


## 客户端更新
如果云端有客户端版本更新，该更新消息会同步到各供应商方，需要更新后再使用，打开应用程序之后顶端会显示有最新版需要下载更新，点击`下载更新`会开始分析版本文件并更新，完成后点击`重新启动`，重新登录即完成更新

![](sources/image/install/net_refresh.png ':size=800')
![](sources/image/install/net_refresh_ing.png ':size=800')
![](sources/image/install/net_refresh_ed.png ':size=800')

## 插件包更新
登录软件之后，需要保证插件包存在且都为最新版本

1. 切换到 `插件管理` 菜单栏，这里显示的是所有依赖插件包的目录，插件包安装根路径由配置文件决定
2. 首次安装点击 `全部更新下载` 会统一安装所有插件包的最新版本，后续更新点击 `检测更新` ，可以检查是否存在新版本，如果显示 `需要更新` 点击右面下载按钮可以下载该插件包的最新版本

![](sources/image/install/net_packages.png ':size=800')

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
显示为本供应商分配的任务信息，可以下载任务相关联的文件

![](sources/image/install/net_file_manage.png ':size=800')