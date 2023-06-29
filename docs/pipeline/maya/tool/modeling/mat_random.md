为场景内所有模型随机赋予不同颜色的lamber材质球

### 启动插件
- 菜单启动 
    `zfused_maya` > `modeling` > `randommat`
- 代码启动
    ```python
    import zfused_maya.tool.modeling.randommat as randommat
    randMat = randommat.RandomMat()
    randMat.showUI()
    ```
### UI  
![](pipeline/../../../images/modeling/mat_random.png ':size=400')

### 使用方法  
1. 赋材质或者刷新随机种子，点击`赋予/刷新材质球`
2. 恢复默认材质球点击`恢复lambert1默认材质球`

