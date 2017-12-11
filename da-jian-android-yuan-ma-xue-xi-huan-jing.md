实际使用的是sublime text2 + ctags
（最先使用android studio,没成功，无法跳转）+

mac环境下步骤：
1 安装好sublime text 2
2 装好sublime text2 的install package
3 安装ctags插件
4 下载ctag5.8,编译成可执行文件
5 将user配置文件的command项设置为ctags的可执行文件的路径
6 将android系统源代码导入sublime text2, 新建project
7 右击project，rebuild tags
8 实际可用了，选中一个要跳转的函数， shift+command+鼠标左键，进行跳转