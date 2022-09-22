
动画文件发布,输出各项实体数据

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
![](../../sources/image/animation/animation_4.jpg ':size=80%')


## 任务选择
筛选出了所有的动画任务，根据场次、镜头号双击进入任务发布窗口
![](../../sources/image/animation/animation_6.jpg ':size=80%')

## 任务上传
发布动画文件`摄像机` `资产` `场景` 缓存信息等等内容
![](../../sources/image/animation/animation_7.jpg ':size=80%')

+ 文件发布分为 新版本上传和当前版本更新
+ 新版本上传 生成最新版的版本号
+ 当前版本更新，不生成新的版本号，并覆盖最新版的文件和缓存
+ 屏幕截图 截取当前文件的屏幕以作为缩略图
+ 上传描述信息 简单介绍当前任务文件的发布内容
+ 点击发布

## 动画文件发布注意事项
?> 发布文件后，数据信息会同步到数据库上，需要提取给到尤尼提并同步数据库(提取方法另行介绍)
