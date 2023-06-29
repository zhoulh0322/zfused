为场景内模型按照模型原本材质颜色赋予不同颜色的lamber材质球

### 启动插件
- 菜单启动 
    `zfused_maya` > `shading` > `shading engine color`
- 代码启动
    ```python
    import zfused_maya.tool.modeling.shadingcolor as shadingcolor
    ui = shadingcolor.ShadingColor()
    ui.show()
    ```
### UI  
![](pipeline/../../../images/shading/shading_engine_color/ui.png ':size=400')

### 使用方法  
1. 打开文件后点击工具，工具会自动分析生成当前场景内的材质引擎列表，并为材质生成相近颜色的纯色信息，点击着色引擎列表中的会选中对应模型的节点
2. 在提取颜色处可以手动修改当前材质的纯色信息
3. 点击显示纯色材质球可以将所有材质转换为对应的纯色lambert材质，点击还原自身材质球会还原材质

![](pipeline/../../../images/shading/shading_engine_color/compare.png ':size=400')
