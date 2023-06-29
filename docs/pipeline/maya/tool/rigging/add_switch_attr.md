在控制器上添加一个新的属性用来在几个模型之间切换显示

### 启动插件
- 菜单启动 
    `zfused_maya` > `rigging` > `add switch attr`
- 代码启动
    ```python
    from zcore import reload
    from zfused_maya.tool.rigging import add_switch_attr
    reload(add_switch_attr)
    add_switch_attr.run()
    ```
### UI  
![](pipeline/../../../images/rigging/add_switch_attr.png ':size=300')

### 使用方法  
1. 选择控制器，点击控制器右方的`<<`
2. 选择所有需要被控制的模型，点击模型右方的`<<`
3. 设置属性参数名称，将在控制器上添加这个属性用来设置要显示的模型
4. 点击添加，属性将被添加
   
![](pipeline/../../../images/rigging/add_switch_attr_ed.png ':size=300')


