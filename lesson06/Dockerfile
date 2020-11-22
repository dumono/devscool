FROM ubuntu:18.04
RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install default-jdk wget git maven
RUN wget -c https://downloads.apache.org/tomcat/tomcat-9/v9.0.40/bin/apache-tomcat-9.0.40.tar.gz -O /usr/local/tomcat.tar.gz
RUN mkdir /usr/local/tomcat
RUN tar -C /usr/local/tomcat -zxvf /usr/local/tomcat.tar.gz --strip-components 1
RUN mkdir /work
WORKDIR /work
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /work/boxfuse-sample-java-war-hello/
RUN mvn package
RUN cp ./target/hello-1.0.war /usr/local/tomcat/webapps/
EXPOSE 8080
CMD  ["/usr/local/tomcat/bin/catalina.sh", "run"]
