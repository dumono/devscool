FROM ubuntu:18.04
RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install default-jdk wget git maven
WORKDIR /work
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package -f /work/boxfuse-sample-java-war-hello/pom.xml
