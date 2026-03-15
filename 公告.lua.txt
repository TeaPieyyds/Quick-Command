if getAppVersion()<62 then
local dialogs=diaLogs("发现新版本","1.优化初次使用配置包报错\n2.优化配置包报错弹窗大量弹出，现在会一个一个展示\n3.github文件访问镜像网站加速")

dialogs.setNegativeButton("下载","openUrl('https://fs-im-kefu.7moor-fs1.com/ly/4d2c3f00-7d4c-11e5-af15-41bf63ae4ea0/1737084791397/RWMOD_11.5.apk')")

dialogs.setPositiveButton("关闭")

dialogs.show()
end