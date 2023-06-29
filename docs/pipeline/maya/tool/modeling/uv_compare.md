### 启动插件
- 菜单启动 
    `zfused_maya` > `modeling` > `UVs comparison`
- 代码启动
    ```python
    from zfused_maya.tool.modeling.uvs_tool import uvs_comparison
    from zcore import reload
    reload(uvs_comparison)
    ui = uvs_comparison.UvsComparison()
    ui.show()
    ```
### UI  
![](pipeline/../../../images/modeling/uv_compare.png ':size=400')

### 使用方法  
1. 选择第一个模型，点击`load1`，将模型加载到模型框内
2. 选择另一个模型，点击`load2`，将模型加载到另一个模型框内
3. 点击`Comparison`，开始比较，界面会弹窗告知uv是否一致


### 注意
> 请保证两个相同层级模型对比，否则就算两模型UV一致也会报错