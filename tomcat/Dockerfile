FROM tomcat:jdk8-openjdk
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY /usr/local/tomcat/webapps/App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT/Config.properties /usr/local/tomcat/ROOT/Config.properties

EXPOSE 8080