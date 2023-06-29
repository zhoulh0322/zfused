批量导出摄像机文件,支持格式 `ma` `mb` `fbx` `alembic`

### 注意
?> 每个文件只识别一个后缀为`_cam`的摄像机，请确保摄像机唯一且正确

### 启动插件
- 菜单启动 
    `zfused_maya` > `animation` > `batch export camera`
- 代码启动
    ```python
    from zcore import reload
    from zfused_maya.tool.animation import export_camera
    reload(export_camera)
    window = export_camera.ExportCamera()
    window.show()
    ```

### UI
![](../../images/animation/export_cam.png
':size=50%')  

### 导出当前文件摄像机  
（图中<u>红色数字</u>步骤）
1. 设置`导出文件夹路径`，摄像机将会导出到该路径下
2. 设置`导出格式`
3. 点击`导出当前场景摄像机`

### 批量导出文件夹内摄像机  
（图中<u>黄色数字</u>步骤）
1. 设置`批量.ma文件夹`，界面会列出此文件夹下所有ma文件，最终导出这些文件的摄像机
2. 设置`导出文件夹路径`，所有摄像机将会导出到该路径下
3. 设置`导出格式`
4. 点击`批量导出文件夹下摄像机`

