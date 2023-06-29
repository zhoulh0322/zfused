资产文件参考统一化配置系统

### 启动插件
- 菜单启动 
    `zfused_maya` > `utility` > `asset management`
- 代码启动
    ```python
    from zfused_maya.tool.utility import assetmanage
    window = assetmanage.AssetManageWidget()
    window.show()
    ```

### UI
![](pipeline/../../../images/utility/asset_management/ui.png ':size=850')

### 使用说明
- 资产领取
  1. 筛选`资产类型`和`任务环节`
  2. 勾选`只显示带有版本的`，可以筛选出已经发布过的资产，没有发布过的将不显示在右侧任务栏中
  3. 在右侧任务栏中找到对应的任务，任务较多不好找的情况下可以输入关键字搜索相关任务，支持中文名与代号搜索，找到任务之后双击即可打开任务详情界面
  4. 详情界面会列出该资产所有发布过的历史版本，可以选择要领取的版本
  5. 每个版本的修改信息与上传备注都有记录
  6. 可以选择参考模型文件或者发布的abc文件，会将所选的文件以`参考`形式领下来，以供使用

    ![](pipeline/../../../images/utility/asset_management/step.png ':size=960')