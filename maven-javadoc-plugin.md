# maven-javadoc-plugin 生成doc时，报如下错误：
Failed to execute goal org.apache.maven.plugins:maven-javadoc-plugin:2.10.3:jar (attach-javadoc) on project DocGen: MavenReportException: Error while generating Javadoc:  
[ERROR] Exit code: 1 - java.lang.IllegalArgumentException  
[ERROR] at sun.net.www.ParseUtil.decode(ParseUtil.java:189)  
[ERROR] at sun.misc.URLClassPath$FileLoader.<init>(URLClassPath.java:958)  
[ERROR] at sun.misc.URLClassPath$3.run(URLClassPath.java:328)  
[ERROR] at java.security.AccessController.doPrivileged(Native Method)  
......
原因之一：  
java环境配置有误：  
classpath:.;%JAVA_HOME%\lib;  
不要添加rt.jar,tools.jar
