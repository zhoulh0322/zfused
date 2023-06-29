给相机添加带透明通道的黑边显示

### 启动插件
- 菜单启动 
    `zfused_maya` > `animation` > `letterbox cam preview`
- 代码启动
    ```python
    import zfused_maya.tool.animation.letterboxpreview.preview as preview
    reload(preview)
    preview.ui()
    ```

### UI
![](../../images/animation/cam_edge/ui.png
':size=30%')  

### 效果
![](../../images/animation/cam_edge/scene.png
':size=30%')  


