解算文件发布，输出解算缓存、文件等实体数据

## 启动插件
- 菜单启动
  `zfused_outsource` > `utility` > `task manage`
- 代码启动
    ```python
    from zfused_maya.tool.utility.taskmanage import taskmanagewidget
    window = taskmanagewidget.TaskManageWidget()
    window.show()
    ```
## UI

![](../../sources/image/cfx/cfx2.jpg)

## 任务选择
筛选出所有的解算任务，根据场次、镜头号双击进入任务发布窗口
亦可根据场次、镜头号搜索、筛选任务，双击进入任务发布窗口

![](../../sources/image/cfx/cfx1.jpg)

## 任务上传
发布解算文件的布料缓存、毛发缓存、文件等资产信息

![](../../sources/image/animation/animation_7.jpg)

+ 文件发布分为 新版本上传和当前版本更新
+ 新版本上传 生成最新版的版本号
+ 当前版本更新，不生成新的版本号，并覆盖最新版的文件和缓存
+ 屏幕截图 截取当前文件的屏幕以作为缩略图
+ 上传描述信息 简单介绍当前任务文件的发布内容
+ 点击发布

## 解算文件发布注意事项
?> 发布文件后，数据信息会同步到数据库上，需要提取给到尤尼提并同步数据库(提取方法另行介绍)
