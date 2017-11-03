0 服务器地址：121.196.222.73

1 maven 依赖库无法自动获取

（1）安装maven，下载源码，本地安装后由maven加入库

（2）查找新的源，修改pom.xml

2 idea svn add to cvs报e155007错误

原因：项目非从svn check out得来

解决：重新check out 一份新的即可

3 发布代码:  
1. 提交代码  
2. 本地更新svn  
3. 在trunk 目录下输入命令 mvn clean package  
4. 在trunk/target目录把打好的war包部署到tomcat上
服务器的tomcat在/home/tomcat/tomcat9  
先停服务，然后替换war包，清空日志，最后重启

重新整理如下:
1. commmit最新代码
2. war打包
  (1)使用maven命令行,暂略
  (2)使用idea打包生成的war文件
3. 将最新war文件上传至服务器 tiangong1001$
  上传位置:/home/tomcat/tomcat9/webapps/
4. 将老的war包改名,存入/home/war_backup
5. 停服务 在tomcat的bin目录,执行./shutdown.sh
6. 删除旧的jianjian文件夹 rm -rf jianjian
7. 若有必要,删除logs下的 catalina.out日志
8. 重启服务 ./startup.sh
9. 查看tomcat进程 ps -ef | grep tomcat

4 本地测试流程

1.准备好controller方法

2.写好对应的test页面

3.点击“电脑端登陆”，可在chrome的f12-&gt;application标签的cookie下查看到当前的token（因为不登陆的话，token为空）

4.将最新的token填入test.jsp,点击要测试的功能，如果session不一致（console里会提示，将其修改为一致）

5.重启本地tomcat，应该就可以正常测试了


5查找当前最新的改动

1.idea project栏下选择对应文件夹，

2. vcs菜单，下拉选择 show changes


6 远程连接阿里云

```
ssh -p 端口号 root@xxxx.xx.xx.x
```

  Welcome to Alibaba Cloud Elastic Compute Service !

