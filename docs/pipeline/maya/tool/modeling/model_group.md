### 启动插件
- 菜单启动 
    `zfused_maya` > `modeling` > `Model Arrange`
- 代码启动
    ```python
    import zfused_maya.tool.modeling.modelArrange_new as modelArrange
    ui = modelArrange.Ui()
    ui.showUi()
    ```

### UI
![](pipeline/../../../images/modeling/ModelArrange/modelarrange.png ':size=300')

## 角色组创建

首先对原始模型进行基础清理（删除历史记录、冻结属性值等），删掉模型制作过程中的多余节点，使用干净的模型进入打组

1. 切换到角色模式（`Characters`）
2. 输入角色资产名称
3. 点击 `create` 创建角色资产空组结构
4. 在大纲中可以看到已经创建出该角色的模型组结构
5. 点击 `Control` - `Geometry Group` 开始设置具体组内的模型
6. 选择一个模型（这里选择的是`body`），点击要放入对应组的按钮（`body`组）
7. 出现`已入组`字样后，在大纲中可以看到模型已经被放到所选组内，并自动重命名为组名
8. 点击`display/hide` 可以切换已入组模型的显示与隐藏，方便与未入组模型区分
9.  装饰部分放在ass内（头饰放入`headass`,身上配饰放入`bodyass`）
10. 用打组工具创建的模型组，`_geometry_group`组上会自动创建`rendering`属性，此属性决定了组内的内容是否输出缓存进入后期渲染，正常情况只有该组会创建rendering属性并参与后期渲染，所以注意确保所有需要出缓存进入后期的模型都处于该组层级之内，确保后续缓存不会漏出
11. 如果角色模型中包含为布料解算制作的简模，请放入_solver_group组内，该组不参与后期渲染
12. 如果角色模型中包含代理模型或简模，后续需要替换为其他形式模型的部分，请放入_proxy_group组内，该组不参与后期渲染
13. 在所有模型都已入新组后可以删掉原先留下的空组

![](pipeline/../../../images/modeling/ModelArrange/chargroup.png ':size=800')

## 道具组创建

1. 输入道具资产名称
2. 切换到道具模式（Props）
3. 创建道具资产空组结构
4. 选择物体
5. 点击geometry组
6. 输入零件名称
7. 物体已被放进geometry组下对应零件组内并自动重命名

![](pipeline/../../../images/modeling/ModelArrange/propgroup.png ':size=800')

## 场景组创建
与道具组创建方式相同，只是第二步改为场景模式（Scene）

### 注意
- 相同组内的模型命名相同，后缀会自动按照`_001`格式依次往上叠加
- 角色和道具的`_geometry_group` 组上带有rendering属性用于后续环节输出渲染模型，请勿勾掉该属性

![](pipeline/../../../images/modeling/ModelArrange/rendering.png ':size=400')