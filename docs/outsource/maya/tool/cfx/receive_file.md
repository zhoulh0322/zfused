获取初始版本解算文件或指定版本解算文件

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

## 首次领取
首次领取，可能会直接打开动画文件或参考动画文件，根据项目需求设置

![](../../sources/image/cfx/cfx4.jpg)
+ 首次领取分为最新版本或无版本选择
+ 无版本为领取的上游文件的无版本文件（无版本号）
+ 最新版本文件为上游文件的最新版本文件(最新版本号)

## 领取旧版解算文件

![](../../sources/image/cfx/cfx3.jpg)

+ 领取文件会自动保存到项目设置路径，默认路径为D盘，请确保D盘有足够的空间

## 解算文件领取注意事项



