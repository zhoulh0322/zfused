在控制器上添加一个新的属性用来影响某模型的可见性

### 启动插件
- 菜单启动 
    `zfused_maya` > `rigging` > `add visible attr`
- 代码启动
    ```python
    from zcore import reload
    from zfused_maya.tool.rigging import add_visible_attr
    reload(add_visible_attr)
    add_visible_attr.run()
    ```
### UI  
![](pipeline/../../../images/rigging/add_visible_attr.png ':size=300')

### 使用方法  
1. 选择控制器，点击控制器右方的`<<`
2. 选择需要被控制的模型，点击模型右方的`<<`
3. 设置属性参数名称，将在控制器上添加这个属性用来控制模型的可见性，默认显示为`StandVis`
4. 点击添加，属性将被添加

