FROM ubuntu:20.04
RUN apt update
RUN apt install default-jdk -y
RUN apt install maven -y
RUN apt install git -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package -f boxfuse-sample-java-war-hello/
ENTRYPOINT ["cp", "boxfuse-sample-java-war-hello/target/hello-1.0.war", "/webapps"]