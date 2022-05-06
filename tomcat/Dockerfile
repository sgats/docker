FROM --platform=linux/amd64 daduber/centos7.8.2003:latest

#指定镜像创建者信息
MAINTAINER yanyu

#切换工作目录
ADD jdk1.8.tgz /opt/jdk
ADD tomcat8test1.tgz /opt/tomcat
#配置java环境变量
ENV JAVA_HOME /opt/jdk/jdk1.8.0_121
ENV CLASSPATH $JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH $PATH:$JAVA_HOME/bin

RUN chmod +x /opt/tomcat/apache-tomcat-8.5.3/bin/*.sh 
EXPOSE 8080 
CMD [ "/bin/sh","-c","/opt/tomcat/apache-tomcat-8.5.3/bin/catalina.sh run" ]
