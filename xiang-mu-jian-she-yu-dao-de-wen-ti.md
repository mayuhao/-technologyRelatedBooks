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

4 本地测试流程

1.准备好controller方法

2.写好对应的test页面

3.点击“电脑端登陆”，可在chrome的f12-&gt;application标签的cookie下查看到当前的token（因为不登陆的话，token为空）

4.将最新的token填入test.jsp,点击要测试的功能，如果session不一致（console里会提示，将其修改为一致）

5.重启本地tomcat，应该就可以正常测试了



5查找当前最新的改动

1.idea project栏下选择对应文件，右键，选择 show changes

