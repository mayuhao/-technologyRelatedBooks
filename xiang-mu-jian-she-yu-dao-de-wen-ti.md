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