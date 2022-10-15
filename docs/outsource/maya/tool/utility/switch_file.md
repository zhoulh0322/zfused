单独或批量切换各个环节的文件，例如切换 `rig low` 至 `rig high`

## 启动插件
- 菜单启动 
    `zfused_outsource` > `utility` > `switch file`
- 代码启动
    ```python
    from zfused_maya.tool.utility.elementmanage import elementmanagewidget
    window = elementmanagewidget.ElementManageWidget()
    window.show()   
    ```

## UI
![](outsource/../../../images/utility/switch_file/main_ui.png ':size=600')


## 批量切换

1. 选择切换至的步骤 __例如需要切换至`rig/hair`__
2. 点击 `任务步骤批量更新` ，等待切换结束

![](outsource/../../../images/utility/switch_file/batch_ui.png ':size=600')