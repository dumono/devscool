FROM tomcat:9.0
RUN mkdir /work
WORKDIR /work
RUN apt update
RUN apt install default-jdk git maven -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /work/package boxfuse-sample-java-war-hello
RUN mvn package
RUN cp ./target/hello-1.0.war /usr/local/tomcat/webapps/

