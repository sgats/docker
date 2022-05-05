#FROM alpine:3.15.4
#FROM daocloud.io/library/centos:6.8
FROM daduber/centos7.8.2003:latest
#COPY apache-tomcat-8.5.3 /usr/local/tomcat8.5/
#COPY jdk1.8.0_121 /usr/local/jdk/
#ENV JAVA_HOME=/usr/local/jdk \
#CLASSPATH=.:${JAVA_HOME}/lib \
#CATALINA_HOME=/usr/local/tomcat-8.5 \
#PATH=${JAVA_HOME}/bin:$CATALINA_HOME/bin:$PATH
#EXPOSE 8080
#CMD [ "/bin/sh","-c","${CATALINA_HOME}/bin/catalina.sh run" ]


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
ENTRYPOINT /opt/tomcat/apache-tomcat-8.5.3/bin/startup.sh && /bin/bash

