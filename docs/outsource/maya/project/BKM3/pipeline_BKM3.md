> 1. 注意：制作过程中时常保存文件，避免maya崩溃重做
> 2. 中文版maya可能会出现无法启动zfused的情况，请切换至英文版
---
## 动画
### **1.动画文件发布**  
![](../../images/project/BKM3/animation/publish_file.png ':size=600')

> 1. 打开制作好的本地文件,如果发现文件参考文件是带版本号的，可以用[开无版本号动画文件](/outsource/maya/tool/animation/no_version_file.md)
> 2. 按照规范整理好文件，发布时会进行相关检查  

- 启动任务管理  
  `zfused_outsource` > `utility` > `任务管理（Task Manage）`
- 在`动画(animation)`环节找到当前镜头的任务
- 点击`上传文件`发布动画动画文件
- 屏幕截图，写缩略图
- 简单描述发布的消息
- 输出采样默认为1
- 上传文件

> 1. 选择动画任务时，务必选择正确，否则会导致发布缓存错误
> 2. 如发布时遇到检查无法跳过，请及时联系优尼提
> 3. 发布文件后，及时将镜头的property提取给到优尼提

## 解算  
### **1. 领取动画文件**  
![](../../images/project/BKM3/cfx/receive.png ':size=600')
- 启动任务管理  
`zfused_outsource` > `utility` > `任务管理（Task Manage）`
- 在`角色特效`环节找到当前镜头的任务
- 点击`首次领取`获取动画文件 （不点击首次领取将领到当前角色特效环节的制作过程文件）

### **2. 替换毛发绑定文件**  
有毛发解算的角色才需要替换绑定，如果没有毛发解算直接跳过这一步和下一步

![](../../images/project/BKM3/cfx/replace_hair_rig.png ':size=600')
- 启动步骤切换插件（）  
`zfused_outsource` > `utility` > `文件步骤切换（switch file）`
- 将当前`绑定-预览`切换为`绑定-毛发`
- 将`ToSim`组中的解算器起始帧改为T-pose 所在帧，即可开始调整形态  
  ![](../../images/project/BKM3/cfx/hair_set.png ':size=600')

### **3.制作并输出毛发缓存**  
- 选择 `fx`->`fur` ->`hair_root_grp`-> `hair_outputcv` ->`output_ToSim`组，输出该组曲线abc缓存，输出路径放在自己能找到得到的地方就可以
![](../../images/project/BKM3/cfx/hair_output.png)



### **4. 替换布料解算绑定**
- 启动步骤切换插件（）  
  `zfused_outsource` > `utility` > `文件步骤切换（switch file）`
- 将当前`绑定-预览`切换为`布料绑定`
- 参考替换毛发绑定
- 将`fx` ->`cloth_cfx`组中的解算器![](../../images/project/BKM3/cfx/nucleus.png)起始帧改为T-pose 所在帧，即可开始调整形态

### **5.制作并输出布料缓存**
![](../../images/project/BKM3/cfx/ncloth.png ':size=600')
- 导出布料缓存
  确定简模动态后，将`fx` ->`cloth_fx` 组中隐藏的高模导出abc缓存，输出路径自定义即可    
  ![](../../images/project/BKM3/cfx/highcache.png ':size=600')

- 在导出abc时，要注意一下选项务必勾选和选择   
  ![](../../images/project/BKM3/cfx/abc_export1.png ':size=600')
  ![](../../images/project/BKM3/cfx/abc_export2.png ':size=600')

### PS
> 1. 为方便后期渲染运动模糊，务必前后多出5帧缓存
> 2. 务必选中输出uv
> 3. 务必选中world space
> 4. 务必选中输出显示属性
> 5. 务必选中输出uv sets


### **6. 赋予缓存** ###
- 根据上述领取动画文件和替换rig的方法，领取干净的动画文件，并替换为毛发rig或布料rig
- 导入上述规则出的毛发abc 和布料abc  
  ![](../../images/project/BKM3/cfx/import_abc.png ':size=600')
  ![](../../images/project/BKM3/cfx/import_abc2.png ':size=600')

- 将上述缓存按照下列规范进行打组并隐藏  
![](../../images/project/BKM3/cfx/group_abc.png)

- 将毛发缓存`output_ToSim` 和 rig_hair组里面的`output_ToSim`做BS，注意先选缓存再选rig_hair的毛发曲线
- 做BS 时应当选择world 模式  
![](../../images/project/BKM3/cfx/bs_node.png ':size=600')

- 随机选中一根曲线，将BS节点 的属性改为1  
![](../../images/project/BKM3/cfx/bs_node2.png ':size=600')
- 将布料缓存和`char_group`->`group`->`Geometry`->具体部位的高模做BS  
![](../../images/project/BKM3/cfx/bs_node3.png ':size=600')

- 按照毛发的方法，将BS 节点属性改为1即可

### PS
> 1. 正常情况，如果资产有毛发文件，需要用毛发的rig_hair 来进行发布缓存
> 2. 如果毛发没有解算需求，也需要替换rig_hair 进行替换缓存


### **7. 发布文件** ###
- 替换好缓存后，将文件保存到本地路径  
![](../../images/project/BKM3/cfx/publish_file.png ':size=600')
- 启动任务管理  
  `zfused_outsource` > `utility` > `任务管理（Task Manage）`
- 在`角色特效`环节找到当前镜头的任务
- 点击`上传文件`发布解算文件
- 屏幕截图，写缩略图
- 简单描述发布的消息
- 输出采样默认为1
- 上传文件
---

## 后期

### **1. 领取后期文件**
- 启动任务管理  
  `zfused_outsource` > `utility` > `任务管理（Task Manage）`
- 在`灯光（rendering）`环节找到当前镜头的任务
- 点击`首次领取`获取灯光组装文件(不点击首次领取将领到当前灯光环节的制作过程文件)  
![](../../images/project/BKM3/lighting/receive_file.png ':size=600')

- 外包公司应选择无版本文件制作 

### **2. 更新后期文件**  
![](../../images/project/BKM3/lighting/update_file.png ':size=600')

- 选择更新资产，务必确定任务正确，否则可能会导致更新到错误的镜头缓存或资产
- 如果文件内只是个别资产可以选择资产后面的更新按钮如(9-1) 单独更新
- 如果文件整体更新可以选择(9-2) 全部更新

> 1. 如果领取文件没有生成文件，可能是由于没有发布动画缓存导致，请先发布动画文件
> 2. 如果动画文件已经发布，请提取镜头property给到优尼提
> 3. 如果后期文件没有解算动态，可能是由于解算缓存的property没有给到优尼提
