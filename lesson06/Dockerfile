FROM tomcat:9.0
RUN apt update
RUN apt install default-jdk git maven -y
RUN cd /tmp; git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN cd /tmp/boxfuse-sample-java-war-hello/; mvn package
RUN cp /tmp/boxfuse-sample-java-war-hello/target/hello-1.0.war /usr/local/tomcat/webapps/
EXPOSE 8888
CMD ["catalina.sh", "run"]
