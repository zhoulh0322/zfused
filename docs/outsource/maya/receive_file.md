环节文件自动组装

?> 以灯光文件组装为案例

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
![](images/lighting/lighting1.jpg ':size=600')

## 任务选择
筛选出所有的解算任务，根据场次、镜头号双击进入任务发布窗口
亦可根据场次、镜头号搜索、筛选任务，双击进入任务发布窗口

![](images/lighting/lighting3.jpg ':size=600')

## 首次组装
首次领取，可能会直接打开动画文件或参考动画文件，根据项目需求设置

![](images/lighting/lighting2.jpg ':size=600')

+ 首次领取勾选左下角首次领取
+ 首次领取分为最新版本或无版本选择
+ 无版本为领取的上游文件的无版本文件（无版本号）
+ 最新版本文件为上游文件的最新版本文件(最新版本号)
+ 领取资产的材质文件或上游环节的abc文件进行处理
+ 领取场景assembly整合文件
+ 领取动画发布的摄像机abc
+ 点击领取文件

## 更新组装
待定。。。

## 文件组装注意事项
+ 领取组装会自动保存到项目设置路径，默认路径为D盘，请确保D盘有足够的空间
+ 如果点击首次领取，将会重新组装文件


