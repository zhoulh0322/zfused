供应商发布的动画文件无法及时同步到服务器上，通过插件提取发布的信息给到优尼提，可以及时更新信息
目前分为两种解决方案

> 1. 直接将本地property文件发布至云端，适合使用zfused_outsource客户端的伙伴
> 2. 离线方式提取property，打包后发给制片，传输到优尼提，适合使用zfused_alone 的伙伴

## 启动插件
- 菜单启动 `zufsed_outsource`>`utility`>`提取property`  
- 代码启动  
```python 
from zfused_maya.tool.technology.extract_info import extract_property
ui = extract_property.ExtractPropertyBar()
ui.show()
```

## UI
![](../../images/utility/extract_property/extract_property1.jpg ':size=600')

## 操作步骤
### 在线操作，发布至云端
默认选择发布至云端

**1. 点击搜索路径的浏览按钮，选择动画文件发布的根目录,如：P:\XXX(项目名)\dcc\shot\场次名**

![](../../images/utility/extract_property/extract_property1.jpg ':size=600')

![](../../images/utility/extract_property/extract_property2.jpg ':size=600')

**2. 点击提取按钮，会自动发布至云端**

![](../../images/utility/extract_property/extract_property7.jpg ':size=600')

### 离线操作，提取至本地

如有需求，可选择提取至本地

**1. 点击搜索路径的浏览按钮，选择动画文件发布的根目录,如：P:\XXX(项目名)\dcc\shot\场次名**

![](../../images/utility/extract_property/extract_property2.jpg ':size=600')

**2. 点击放置路径的浏览按钮，输入提取出的property的保存路径**

![](../../images/utility/extract_property/extract_property3.jpg ':size=600')

**3. 点击提取按钮**

![](../../images/utility/extract_property/extract_property4.jpg ':size=600')

![](../../images/utility/extract_property/extract_property5.jpg ':size=600')

**4. 正常提取出该场次所有已经发布的镜头的记录信息，将放置路径下提取的文件打包发给制片即可**

![](../../images/utility/extract_property/extract_property6.jpg ':size=600')


## 注意事项
- 在线操作请保持网络畅通
- 不要直接搜索盘符根目录，会速度很慢
- 如有问题，及时和优尼提联系