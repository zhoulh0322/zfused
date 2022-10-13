用于和DCC软件交互设计的自定义变量

## ocio_aces
- 类型 `str`
- 默认数值 `None`

色彩空间方案，如需特殊色彩空间方案，配置.ocio特殊方案

## clear_unused
- 类型 `bool`
- 默认数值 `1`

制作文件方面是否自动清除未使用节点

## incremental_save
- 类型 `bool`
- 默认数值 `1`

保存文件的时候，是否开启增量保存

## is_sync_backup_external_files
- 类型 `bool`
- 默认数值 `1`

备份上传制作文件的时候，是否上传依赖扩展文件，默认`1`上传依赖文件，反则不上传依赖文件

## work_with_no_version
- 类型 `bool`
- 默认数值 `0`

制作是否带版本号制作，默认`0`为带版本号制作，`1`为不带版本号制作

## scene_panel_config
- 类型 `bool`
- 默认数值 `0`

文件保存是否保留布局等ui信息

## playblast_maya
- 类型 `dict`
- 默认数值 

## default_namespace
- 类型 `str`
- 默认数值 `__ns__00`
  
文件参考默认namespace `空间名`

`maya`自定义拍屏变量设置
```python
{
    "hud": [
        {
            "color": "#EEEEEE",
            "code": "camera",
            "cmd": "import maya.cmds as cmds\nimport maya.OpenMaya as OpenMaya\nimport maya.OpenMayaUI as OpenMayaUI\nview = OpenMayaUI.M3dView.active3dView()\ncamDag = OpenMaya.MDagPath()\nview.getCamera(camDag)\ncameraname =camDag.fullPathName().split('|')[-2]\ntext =u\"  相机  {}\".format(cameraname)\n",
            "text-align": [-1,1,0]
        },
        {
            "color": "#EEEEEE",
            "code": "image_size",
            "cmd": "text = '分辨率  1920 x 1080'",
            "text-align": [0,1,0]
        },
        {
            "color": "#EEEEEE",
            "code": "camera_focal",
            "cmd": "import maya.OpenMaya as OpenMaya\nimport maya.OpenMayaUI as OpenMayaUI\nview = OpenMayaUI.M3dView.active3dView()\ncamDag = OpenMaya.MDagPath()\nview.getCamera(camDag)\ncurrent_cam = camDag.fullPathName().split('|')[-1]\nfocal_length = cmds.getAttr(\"{}.focalLength\".format(current_cam))\ntext =u\"焦距  {:.2f}\".format(focal_length)  \n",
            "text-align": [1,1,0]
        },
        {
            "color": "#EEEEEE",
            "code": "time",
            "cmd": "import time;text = \"  日期  {}\".format(time.strftime('%Y/%m/%d', time.localtime()))",
            "text-align": [-1,-1,0]
        },
        {
            "color": "#EEEEEE",
            "code": "username",
            "cmd": "import zfused_api\n_user_id = zfused_api.zFused.USER_ID\n_user_handle = zfused_api.user.User(_user_id)\ntext = \"制作者  {}\".format(_user_handle.profile[\"NameEn\"])",
            "text-align": [0,-1,0]
        },
        {
            "color": "#EEEEEE",
            "code": "frame",
            "cmd": "import maya.cmds as cmds\n_s_t = int(cmds.playbackOptions(q = True, min = True))\n_e_t = int(cmds.playbackOptions(q = True, max = True))\n# _format = '%0' + str(len(str(_e_t))) + 'd'\n# _c_t = _format%int(cmds.currentTime(q = True))\n_c_t = int(cmds.currentTime(q = True))\ntext = u'帧数  %s|%s-%s'%(_c_t,_s_t,_e_t)  ",
            "text-align": [1,-1,1]
        },
        {
            "color": "#EEEEEE",
            "code": "fps",
            "cmd": "import pymel.core as pm\n_frame = int(pm.mel.currentTimeUnitToFPS())\ntext = \"帧率  %s\"%str(_frame)\n_s_t = int(cmds.playbackOptions(q = True, min = True))\n_e_t = int(cmds.playbackOptions(q = True, max = True))\n_c_t = int(cmds.currentTime(q = True))\ncontent_text = '帧数  %s|%s-%s'%(_c_t,_s_t,_e_t)  \n",
            "text-align": [1,-1,0]
        }
    ],
    "font-size": 20,
    "bold": true,
    "color": "#FF0000",
    "spacing": 8,
    "text-height": 25,
    "image_size": [1920,1080
    ],
    "font-family": "Microsoft YaHei UI",
    "fps": 25,
    "margin": [8,8,8,8],
    "background-color": "#222222"
}
```