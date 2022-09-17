场景文件参考统一化配置系统

## 启动插件
- 菜单启动 
    `zfused_maya` > `utility` > `assembly management`
- 代码启动
    ```python
    from zfused_maya.tool.utility import assemblymanage
    window = assemblymanage.AssemblyManageWidget()
    window.show()
    ```