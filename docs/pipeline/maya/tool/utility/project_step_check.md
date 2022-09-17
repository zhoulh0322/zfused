项目环节检查

## 启动插件
- 菜单启动 
    `zfused_maya` > `utility` > `asset management`
- 代码启动
    ```python
    from zfused_maya.tool.utility import check_manage
    window = check_manage.CheckManageWidget()
    window.show()
    ```