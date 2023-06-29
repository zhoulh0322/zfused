项目环节检查

### 启动插件
- 菜单启动 
    `zfused_maya` > `utility` > `project_step_check`
- 代码启动
    ```python
    from zfused_maya.tool.utility import check_manage
    window = check_manage.CheckManageWidget()
    window.show()
    ```
### UI
![](pipeline/../../../images/utility/step_check/ui.png ':size=700')

### 使用方法
1. 筛选要检查的环节，每个环节检查项不同
2. 右方列表会列出该环节所有的检查项，有部分检查可以根据需要选择勾选`忽略`，勾选之后将跳过该条检查，暗灰色表示不可以忽略
3. 点击检查将执行文件检查，绿色表示检查通过，红色表示检查未通过，需要修改
4. 去掉勾选`显示所有检查面板`，会只显示未通过的检查方便查看
5. 点击`显示信息`中显示的节点名可以在maya中选中该节点方便纠错
6. 部分检查可以点击`修复`自动修复，其余需要人为判断修改
7. 更改完成后再次点击检查，确保所有不可忽略的检查均已通过 

    ![](pipeline/../../../images/utility/step_check/step.png ':size=700')