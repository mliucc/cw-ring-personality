# Class Widgets 高级铃声
> [!WARNING]
> 本插件目前无法检测来自其他插件的铃声，如需使用请关闭本插件并调整主程序铃声音量
## 简介
一个可以为Class Widgets提供**高级铃声**的插件
## 计划/已经实现的功能
- [x] 支持早读铃、上课铃、下课铃、预备铃、午休铃、放学铃
- [x] 新增自定义铃声配置（测试2个铃声通过，理论支持铃声数量无限)
- [x] 通过修改config.json进行配置
- [ ] 通过设置UI进行配置
## 使用指南
> [!IMPORTANT]
> 对于下文关于自定义铃声的说明：<br>
> ***序号***：**从1开始，每次增加1的整数**，如ringtone1；ringtone2 <br>
> ***配置***：插件**自带2段配置**，如需增加，请**复制自带部分并修改序号**<br>
> **注意**  请保证序号及配置的格式与**已有部分完全相同**
- **安装插件**  在Class Widgets插件广场下载插件
- **更换音频**  打开Class Widgets主程序所在目录，转到./plugin/cw-advanced-ringtones/plugin_audio，按照下面对应关系添加或更换音频，要求为**wav格式** <br>
  >早读铃→attend_school.wav<br> 上课铃→attend_class.wav <br> 下课铃→finish_class.wav <br> 预备铃→prepare_class.wav <br> 午休铃→noon.wav <br> 放学铃→finish_school.wav <br> 其他自定义铃声→ringtone***序号***.wav
- **配置铃声**  进入./plugin/cw-advanced-ringtones目录，打开**config.json**，按照下面提示进行配置： 
   > > 更改铃声大小："volume": ***1~100间的一个整数，数字越大音量越大***（默认为75）
   > 
   > > 午休铃声配置："noon_cfg": 
   > > > 午休铃声类型："noon_type": "***0或1, 0为原下课铃（即打铃后进入课间），1为原上课铃（即打铃后进入下一节课）***",
   > >  
   > > > 午休铃声对应课程："noon_class": "***主程序显示通知上的课程名称***"
   >  
   > > 早读铃声配置："attend_school_cfg": **与上述午休铃声配置同理**
   >
   > > 自定义铃声配置："extra_ringtones"：
   > > > 启用自定义铃声数量："ringtone_quanlity":***配置启用的铃声数量，≥0的整数，设置为0则禁用自定义铃声，请确认该数量与实际启用自定义铃声数量（即config.json中extra_ringtones中各ringtone_cfg中ringtone_switch值为1的数量）一致***
   > > 
   > > > 自定义铃声配置："ringtone***序号***_cfg": **与上述午休铃声配置同理**
- **启动插件**  打开Class Widgets设置页面，设置一个另外的课程表、时间线进行测试，符合用户需求后即可食用
