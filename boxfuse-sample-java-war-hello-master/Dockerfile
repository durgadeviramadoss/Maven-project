FROM centos

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN curl -O https://www-eu.apache.org/dist/tomcat/tomcat-8/v8.5.41/bin/apache-tomcat-8.5.41.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-8.5.41/* /opt/tomcat/.
RUN yum -y install  java-1.8.0-openjdk java-1.8.0-openjdk-devel
RUN java -version

WORKDIR /opt/tomcat/webapps
COPY boxfuse-sample-java-war-hello-master/hello-1.0.war  /opt/tomcat/webapps/

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
