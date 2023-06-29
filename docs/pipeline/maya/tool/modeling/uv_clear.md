清除模型内非`map1`的不规范uvset

### 启动插件
- 菜单启动 
    `zfused_maya` > `modeling` > `uvs clears`
- 代码启动
    ```python
    from zcore import reload
    import zfused_maya.tool.modeling.uvs_tool.uvs_clears as uvs_clears
    reload(uvs_clears)
    ui = uvs_clears.UvsClear()
    ui.show()
    ```
### UI  
![](pipeline/../../../images/modeling/uv_clear.png ':size=400')

### 使用方法  
1. 选择要清理的模型（提供快捷方式可以`全选`或`反选`或`清空`对目前所选择的模型进行快捷选择）
2. 点击`执行`会清除除`map1`之外的uvset

