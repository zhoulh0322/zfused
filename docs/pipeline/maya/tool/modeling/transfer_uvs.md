组对组传递uv，可以按照点线面拓扑或大纲层级顺序来传递，当存在相同拓扑不同uv的情况时，最好使用大纲顺序传递

### 启动插件
- 菜单启动 
    `zfused_maya` > `modeling` > `transfer uvs`
- 代码启动
    ```python
    import zfused_maya.tool.modeling.transfer_uvs as transfer_uvs
    reload(transfer_uvs)
    ui = transfer_uvs.Ui()
    ui.show()
    ```
### UI  
![](pipeline/../../../images/modeling/transfer_uvs/ui.png)

### 使用方法  
1. 选择目标组
2. 选择模板组  
3. 选择传递方式，选择按大纲传递会根据组内层级顺序来对应传递，如果对应层级拓扑不同会报错，按拓扑传递会寻找相同拓扑的模型传递
4. 点击传递
5. 传递成功后会弹窗提示，若有部分模型未找到对应模板将会弹窗显示未成功的模型路径，并且在视图中高亮选择这些模型  
![](pipeline/../../../images/modeling/transfer_uvs/errorinfo.png
':size=30%')
![](pipeline/../../../images/modeling/transfer_uvs/erroselect.png
':size=30%')


### 注意
> 在大纲里选择两个组，不要在视图中框选模型
> 按拓扑传递会出现同拓扑不同uv的模型都被传递成同一个uv的问题，请按需使用