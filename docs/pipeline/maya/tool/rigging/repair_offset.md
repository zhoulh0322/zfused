dcc软件精度计算模式导致绑定位移到距离原点过远的位置后出现点线扭曲情况，本工具对部分绑定文件有效，运行后大位移点线面保持完整

![](pipeline/../../../images/rigging/repair_offset/problem.png ':size=400')

### 启动插件
- 菜单启动 
    `zfused_maya` > `rigging` > `repair_offset`
- 代码启动
    ```python
    from zcore import reload
    from zfused_maya.tool.rigging.repair_offset import window
    reload(window)
    ui = window.Window()
    ui.show()
    ```
### UI  
![](pipeline/../../../images/rigging/repair_offset/ui.png ':size=400')

### 使用方法  
1. 选择模型skin组，点击选择模型组
2. 选择控制位移的最小控制器（小环）
3. 点击运行开始计算


### 注意
> 本工具对部分不符规范的绑定文件不起效果