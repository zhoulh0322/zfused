内部环境发布的动画文件为带版本号的绑定资产，由于动画制作周期较长，绑定版本更新迭代，可能会导致制片提取资产文件的时候遗漏
所以需要供应商公司在打开动画文件的时候切换到无版本号的绑定资产
# 启动插件
- 菜单启动  
`zfused_outsource`>`utility`>`打开无版本资产文件`

- 代码启动  
```python
from  zfused_maya.tool.technology.re_version import re_version
re_version.without_version_open_file()
  ```

# UI
![](../../images/utility/no_version_file/no_version1.jpg ':size=600')

![](../../images/utility/no_version_file/no_version2.jpg ':size=600')
- 通过选择路径文件，选择需要打开的文件

# 注意事项
- 该功能只能打开编码为ASCII 的ma文件，mb文件由于编码无法打开，会导致文件错误
- 如果使用中有遇到问题，请及时联系优尼提