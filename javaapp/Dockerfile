FROM ubuntu:24.04
RUN apt-get update
RUN apt-get install openjdk-17-jdk -y
RUN apt-get install git -y
RUN apt-get install maven -y
RUN git clone https://github.com/Mximus7893265/springboot.git maxapp
RUN cd maxapp && mvn clean package spring-boot:repackage
WORKDIR /maxapp/target
ENTRYPOINT ["java", "-jar", "WebApplication-1.0.jar"]
