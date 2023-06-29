将场景内所有`arnold aiStandarSurface`转换为`standarSurface`

### 启动插件
- 菜单启动 
    `zfused_maya` > `modeling` > `to standar surface`
- 代码启动
    ```python
    from zfused_maya.tool.modeling import to_standard_surface
    ui = to_standard_surface.ToStandardSurface()
    ui.show()
    ```
### UI  
![](pipeline/../../../images/modeling/switch_to_standar.png ':size=400')

### 使用方法  
1. 打开文件后点击工具，工具会自动分析出当前场景内的非标准材质并罗列在界面中，点击每条材质会选中对应的材质节点供查看
2. 点击`转换至标准材质球`会将所有aiStandarSurface转换成standarSurface


### 注意
> 执行之前先自行另存文件，避免造成不可撤回的操作
> 工具目前只可以切换aiStandarSurface，不支持其他材质节点