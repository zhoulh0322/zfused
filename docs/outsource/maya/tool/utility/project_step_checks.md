在发布文件前，可以自主进行文件内的规范进行检查，我们会提供一些工具进行辅助，部分检查可以进行一键修复
## 项目步骤检查
### 启动插件
- 菜单启动 `zufsed_outsource`>`utility`>`工具`>`项目环节检查`

  ![](../../images/utility/project_step_check/check_start.png ':size=600')
- 代码启动
    ```python
    from zfused_maya.tool.utility.check_manage import check_manage_widget
    ui = check_manage_widget.CheckManageWidget()
    ui.show()
    ```

### UI
   ![](../../images/utility/project_step_check/check_1.png ':size=600')
### 检查
![](../../images/utility/project_step_check/check_2.png ':size=600')![](../../images/utility/project_step_check/check_3.png ':size=600')

> 1. 选择具体的步骤，模型检查会分为模型和材质，相关的检查项会不同，要分清楚
> 2. 当检查出现红色，表示为检查出错，需要修复，绿色为检查项通过
> 3. 如果忽略项高亮，则表示该项检查可以跳过，选择跳过即可，如果不能跳过，则必须通过，否则会影响到下游环节的制作
## 任务检查
### 启动插件
-  菜单启动 `zufsed_outsource`>`utility`>`工具`>`项目环节检查`

   ![](../../images/utility/project_step_check/check_start2.png ':size=600')
- 右击任务，选择任务检查
- 
   ![](../../images/utility/project_step_check/check_4.png ':size=600')

### 检查

![](../../images/utility/project_step_check/check_2.png ':size=600')

> 1. 只会显示报错的项目，顺利通过的检查项会隐藏
> 2. 如果可以修复，尽量不要忽略
> 3. 不能忽略的属于重要检查项，务必检查修改，否则会对上下游流程产生影响







## 检查项解释
略


## 注意事项
> 1. 当检查遇到问题，无法自行解决时，及时联系优尼提
