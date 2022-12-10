显示需要文件接收的任务版本管理  
> `zfused`使用任务文件推送版本的方式，任务迭代版本较快，文件更新会有延迟
> 
> 如果急需确认版本是否为最新，可通过此工具来检查

## 启动插件
- 菜单启动 
    `zfused_maya` > `utility` > `task receive manage`
- 代码启动
    ```python
    from zfused_maya.tool.utility.task_receive_manage import task_receive_manage_widget
    window = task_receive_manage_widget.TaskReceiveManageWidget()
    window.show()
    ```

## UI
![](outsource/../../../images/utility/task_receive_manage/Snipaste_2022-12-06_16-49-55.png ':size=600')

## 筛选任务环节
筛选任务环节，只显示筛选环节的需要接收文件的任务信息   
![](outsource/../../../images/utility/task_receive_manage/Snipaste_2022-12-06_16-55-59.png ':size=600')


## 只显示需要更新的任务
仅显示需要更新的任务   
![](outsource/../../../images/utility/task_receive_manage/Snipaste_2022-12-06_16-56-48.png ':size=600')


## 查看任务版本更新描述
双击任务，可展现出当前任务的更新描述  
![](outsource/../../../images/utility/task_receive_manage/Snipaste_2022-12-06_16-58-18.png ':size=600')


> 如果时分着急更新文件，可通过此工具查看一些更新信息