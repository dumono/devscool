FROM tomcat:9.0
RUN apt install default-jdk git maven -y
RUN cd /tmp; git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package /tmp/boxfuse-sample-java-war-hello/pom.xml
RUN cp /tmp/boxfuse-sample-java-war-hello/target/hello-1.0.war /var/lib/tomcat9/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]
