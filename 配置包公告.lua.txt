local version=getInt("xx12d配置包版本",0)

-- 获取当前时间戳
local time = math.floor(os.time())
--获取上次显示时间
local last_time=getInt(version.."消息弹窗",0)
--获取时间差
local time_difference=time-last_time
--如果时间差大于1天 显示弹窗
if  time_difference>86400 then
--记录本次时间
setInt(version.."消息弹窗",time)
diaLogs("欢迎使用","配置包只设置了基础数据，如有更新可自行阅读配置包修改，添加，如果不懂到地方加群了解")
.setNeutralButton("加入Q群",
"openUrl('https://qm.qq.com/q/iYruxxYiyI')")
.setNegativeButton("复制群号",
"copy('869436540')"
.."Toast('已复制')")
.setPositiveButton("关闭")
.show()
end



if version<12 then
local dialogs=diaLogs("配置包发现新版本","1.修复节点[贴花]下关键词重复\n2.github使用镜像网站加速")
dialogs.setNeutralButton("加入Q群",
"openUrl('https://qm.qq.com/q/iYruxxYiyI')")
dialogs.setNegativeButton("下载","openUrl('https://fs-im-kefu.7moor-fs1.com/ly/4d2c3f00-7d4c-11e5-af15-41bf63ae4ea0/1737047566571/1.15配置包_12.zip')")
dialogs.setPositiveButton("关闭")

if getAppVersion()<56 then
dialogs.setPopupClosable(false) end

dialogs.show()
end